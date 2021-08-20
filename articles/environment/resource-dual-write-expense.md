---
title: Integración de xestión de gastos
description: Este tema ofrece información sobre a integración de informes de gastos en Project Operations mediante a escrita dual.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986579"
---
# <a name="expense-management-integration"></a>Integración de xestión de gastos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema ofrece información sobre a integración de informes de gastos no [despregamento de datos completo](../expense/expense-overview.md) de Project Operations mediante a escrita dual.

## <a name="expense-categories"></a>Categorías de gasto

Nun despregamento de gastos completo, créanse e mantense categorías de gastos nas aplicacións de Finance and Operations. Para crear unha nova categoría de gasto, complete os seguintes pasos:

1. En Microsoft Dataverse, cree unha categoría de **Transacción**. A integración de escrita dual sincronizará esta categoría de transaccións coas aplicacións de Finance and Operations. Para obter máis información, consulte [Configurar categorías de proxecto](/dynamics365/project-operations/project-accounting/configure-project-categories) e [Integración de datos de instalación e configuración de Project Operations](resource-dual-write-setup-integration.md). Como resultado desta integración, o sistema crea catro rexistros de categoría compartidos nas aplicacións de Finance and Operations.
2. En Finance, vaia a **Xestión de gastos** > **Configuración** > **Categorías compartidas** e seleccione unha categoría compartida cunha clase de transacción **Gasto**. Configure o parámetro **Pódese usar en Gasto** como **Verdadeiro** e defina o tipo de gasto que se vai usar.
3. Usando este rexistro de categoría compartida, cree unha nova categoría de gasto indo a **Xestión de gastos** > **Configurar** > **Categorías de gasto** e seleccionando **Nova**. Cando se garda o rexistro, a escrita dual usa o mapa da táboa **Entidade de exportación de categorías de gasto do proxecto de integración de Project Operations (msdyn\_expensecategories)** para sincronizar este rexistro con Dataverse.

  ![Integración de categorías de gasto.](./media/DW6ExpenseCategories.png)

As categorías de gasto nas aplicacións de Finance and Operations son específicas da empresa ou entidade legal. Hai rexistros separados e específicos da entidade legal correspondente en Dataverse. Cando un xestor de proxectos estima gastos, non pode seleccionar as categorías de gasto creadas para un proxecto propiedade dunha empresa diferente da empresa propietaria do proxecto no que están a traballar. 

## <a name="expense-reports"></a>Informes de gastos

Os informes de gastos créanse e apróbanse nas aplicacións de Finance and Operations. Para obter máis información, consulte [Crear e procesar informes de gastos en Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Despois de que o informe de gastos sexa aprobado polo xestor do proxecto, envíase ao libro maior. En Project Operations, as liñas de informe de gastos relacionadas co proxecto contabilízanse utilizando regras especiais de contabilización:

  - O custo relacionado co proxecto (incluído o imposto non recuperable) non se contabilizan inmediatamente na conta de custos do proxecto no libro maior, senón que se contabilizan na conta de integración de gastos. Esta conta está configurada en **Xestión e contabilidade de proxectos** > **Configuración** > **Parámetros de xestión e contabilidade de proxectos**, separador **Project Operations en Dynamics 365 Customer Engagement**.
  - A escrita dual sincronízase con Dataverse usando o mapa da táboa **Entidade de exportación de gastos do proxecto de integración de Project Operations (msdyn\_expenses)**.
  - O libro auxiliar fiscal, o libro auxiliar do fornecedor e outras contabilizacións financeiras rexístranse segundo o caso no momento da contabilización do informe de gastos.

  ![Integración dos informes de gastos.](./media/DW6ExpenseReports.png)

Cando se escribe un rexistro na entidade **Gasto** en Dataverse, o sistema activa o proceso de aprobación automatizada do rexistro. Se é necesario, pódese revisar o estado do proceso de aprobación automatizado en Dataverse indo a **Configuración avanzada** > **Sistema** > **Traballos do sistema**. Despois de completar a aprobación, créanse rexistros de clases de transaccións de gastos na entidade **Datos reais**.

Os datos relacionados cos gastos son entón procesados usando o mapa de táboa de escrita dual **Datos reais de integración de Project Operations (msdyn\_actuals)**. Para obter máis información, consulte [Estimacións e datos reais do proxecto](resource-dual-write-estimates-actuals.md).

O proceso periódico **Importar desde a transición** crea liñas de diario relacionadas co informe de gastos no diario de integración de Project Operations. A conta de compensación predefinida á conta de integración de gastos. O diario de integración de contabilización borra o saldo da conta para a transacción de gastos e move o importe do gasto á conta de custos do proxecto. O sistema tamén crea transaccións de libro auxiliar do proxecto para fins de facturación e recoñecemento de ingresos.
