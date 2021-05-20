---
title: Integración de estimacións e datos reais do proxecto
description: Este tema ofrece información sobre a integración de escrita dual de Project Operations para estimacións e datos reais do proxecto.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955748"
---
# <a name="project-estimates-and-actuals-integration"></a>Integración de estimacións e datos reais do proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema ofrece información sobre a integración de escrita dual de Project Operations para estimacións e datos reais do proxecto.

## <a name="project-estimates"></a>Estimacións do proxecto

O traballo, o gasto e as estimacións de materiais do proxecto créanse e mantéñense en Microsoft Dataverse e sincronízanse coas aplicacións de Finance and Operations para fins de contabilidade. As operacións de creación, actualización e eliminación non son compatibles coas aplicacións de Finance and Operations.

A creación de estimacións require unha configuración de contabilidade válida para o proxecto. Os proxectos asociados a liñas de contrato deben ter un perfil de custos e ingresos do proxecto válido definido nas regras do perfil de custos e ingresos do proxecto. Para obter máis información, consulte [Configurar a contabilidade para proxectos facturables](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimacións de traballo

O xestor de proxectos ou o xestor de recursos crea estimacións de traballo e tamén atribúe un recurso xenérico ou nomeado á tarefa do proxecto. Os rexistros de atribución de recursos pódense revisar no separador **Atribucións de recursos** na páxina **Detalles do proxecto** en Dataverse. Os rexistros de atribución de recursos en Dataverse crean rexistros de previsión de horas nas aplicacións de Finance and Operations usando a **entidade de integración de Project Operations para estimacións de horas (msdyn\_resourceassignments)**.

   ![Integración de estimacións de traballo](./Media/DW4LaborEstimates.png)

A escrita dual sincroniza os rexistros de atribución de recursos coa táboa de transición (**ProjCDSEstimateHoursImport**) e despois usa a lóxica empresarial para crear e actualizar rexistros de previsión de horas (**ProjForecastEmpl**).

O contable do proxecto revisa os rexistros de horas da previsión creados nas aplicacións de Finance and Operations indo a **Xestión e contabilidade de proxectos** > **Todos os proxectos** > **Plan** > **Previsións de horas**.

## <a name="expense-estimates"></a>Estimacións de gastos

O xestor de proxectos crea as estimacións de gastos no separador **Estimacións de gastos** na páxina **Detalles do proxecto** en Dataverse. Os rexistros de estimación de gastos almacénanse la entidade **Liña de estimación** en Dataverse. Estes rexistros de estimación teñen a clase de transacción **Gasto** e están sincronizados cos rexistros de previsión de gastos nas aplicacións de Finance and Operations usando a **entidade de integración de Project Operations para estimacións de gastos (msdyn\_estimatelines)**.

   ![Integración de estimacións de gastos](./Media/DW4ExpenseEstimates.png)

A escrita dual sincroniza os rexistros de estimación de gastos coa táboa de transición (**ProjCDSEstimateExpenseImport**) e despois usa a lóxica empresarial para crear e actualizar rexistros de previsión de gastos (**ProjForecastCost**). As liñas da estimación rexistran a estimación de vendas e os custos por separado. A lóxica empresarial nas aplicacións de Finance and Operations enche un único rexistro de previsión de gastos usando este detalle na táboa de transición.

O contable do proxecto pode revisar os rexistros previsión de gastos nas aplicacións de Finance and Operations indo a **Xestión e contabilidade de proxectos** > **Todos os proxectos** > **Plan** > **Previsións de gastos**.

## <a name="material-estimates"></a>Estimacións de material

O xestor de proxectos crea as estimacións de material no separador **Estimacións de material** na páxina **Detalles do proxecto** en Dataverse. Os rexistros de estimación de material almacénanse la entidade **Liña de estimación** en Dataverse. Estes rexistros de estimación teñen a clase de transacción **Material** e están sincronizados cos rexistros de previsión de elementos nas aplicacións de Finance and Operations usando a **táboa de integración do proxecto para estimacións de material (msdyn\_estimatelines)**.

   ![Integración de estimacións de material](./Media/DW4MaterialEstimates.png)

A escrita dual sincroniza os rexistros de estimación de material coa táboa de transición **ProjForecastSalesImpor** e despois usa a lóxica empresarial para crear e actualizar rexistros de previsión de elementos (**ForecastSales**). As liñas da estimación rexistran a estimación de vendas e os custos por separado. A lóxica empresarial nas aplicacións de Finance and Operations enche un único rexistro de previsión de elementos usando este detalle na táboa de transición.

O contable do proxecto pode revisar os rexistros previsión de elementos nas aplicacións de Finance and Operations indo a **Xestión e contabilidade de proxectos** > **Todos os proxectos** > **Plan** > **Previsións de elementos**.

## <a name="project-actuals"></a>Datos reais do proxecto

Os datos reais do proxecto créanse en Dataverse, en función do tempo, gasto, material e actividade de facturación. Todos os atributos operativos destas transaccións, como a cantidade, o prezo de custo, o prezo de venda e o proxecto, captúranse nesta entidade de Dataverse. Para obter máis información, consulte [Datos reais](../actuals/actuals-overview.md). Os rexistros de datos reais sincronízanse coas aplicacións de Finance and Operations mediante o mapa da táboa de escritura dual **Datos reais de integración de Project Operations (msdyn\_actuals)** para a contabilidade descendente.

   ![Integración de datos reais](./Media/DW4Actuals.png)

O mapa da táboa **Datos reais de integración de Project Operations** sincroniza todos os rexistros da entidade **Datos reais** en Dataverse, co atributo **Omitir sincronización (só para uso interno)** fixado en **Falso**. Este valor de atributo establécese en Dataverse automaticamente cando se crea o rexistro. Exemplos nos que se establece este atributo como **Verdadeiro**:

  - Datos reais de custo do proxecto para transaccións entre empresas. Para obter máis información, consulte [Crear transaccións entre empresas](../project-accounting/create-intercompany-transactions.md). Estes rexistros omítense porque o sistema recrea o dato real de custo do proxecto nas aplicacións de Finance and Operations cando se publica a factura do fornecedor entre empresas.
  - Rexistros negativos de vendas sen facturar creados cando se confirma a factura proforma. Estes rexistros omítense porque libro de contabilidade auxiliar nas aplicacións de Finance and Operations non reverte o rexistro de vendas non facturadas na facturación, pero cambia o estado a totalmente facturado.

O mapa de táboa de escrita dual sincroniza os rexistros de datos reais coa táboa de transición **ProjCDSActualsImport**. Estes rexistros son procesados polo proceso periódico **Importar da táboa de transición** ao crear liñas de diario de integración de Project Operations e liñas de proposta de factura de proxecto. Para obter máis información, consulte [Diario de integración en Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse tamén captura as ligazóns entre as transaccións reais do proxecto na entidade **Conexión de transacción**. Para obter máis información, consulte [Vincular datos reais con rexistros orixinais](../actuals/linkingactuals.md). As ligazóns entre transaccións reais tamén se sincronizan coas aplicacións de Finance and Operations que usan o mapa da táboa de escrita dual **Entidade de integración para relacións de transaccións de proxectos (msdyn\_transactionconnections)**. Estes rexistros son utilizados polo proceso periódico **Importar da táboa de transición** ao crear liñas de diario de integración de Project Operations e liñas de proposta de factura de proxecto.

Contabilizar un diario de integración de Project Operations e unha proposta de factura do proxecto provoca unha actualización nos rexistros respectivos na táboa de transición **ProjCDSActualsImport**. O sistema captura e rexistra os seguintes atributos de contabilidade para as transaccións de datos reais:

- Importe de divisa de contabilidade
- Taxa de cambio
- Número do bono
- Importe do imposto de vendas

O mapa da táboa **Datos reais de integración de Project Operations** actualiza os rexistros de datos reais respectivos en Dataverse con esta información.
