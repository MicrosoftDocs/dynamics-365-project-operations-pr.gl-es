---
title: Integración de datos de instalación e configuración de Project Operations
description: Este tema ofrece información sobre a instalación e configuración de mapas de escrita dual de Project Operations.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938982"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integración de datos de instalación e configuración de Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema ofrece información sobre a integración de escrita dual de Project Operations para entidades de instalación e configuración.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos do proxecto, liñas de contrato e proxectos

Os contratos de proxecto, as liñas de contrato e os proxectos créanse en Dataverse e sincronízanse coas aplicacións de Finance and Operations para contabilidade adicional. Os rexistros nestas entidades só se poden crear e eliminar en Dataverse. Non obstante, os atributos contables como os valores predefinidos do grupo de impostos sobre vendas e as dimensións financeiras pódense engadir a estes rexistros nas aplicacións de Finance and Operations.

  ![Conceptos de integración de contrato de proxecto](./media/1ProjectContract.jpg)

Os clientes potenciais, as oportunidades e as ofertas da actividade de vendas rastréxanse en Dataverse e non se sincronizan coas aplicacións de Finance and Operations porque non hai ningunha contabilidade descendente asociada a esta actividade.

A funcionalidade do contrato do proxecto en Dataverse crea un rexistro de contrato de proxecto nas aplicacións de Finance and Operations que usan o mapa da táboa **Cabeceiras de contrato de proxecto (salesorders)**. Ao gardar un contrato de proxecto en Dataverse tamén comeza a creación dun rexistro da entidade cliente de contrato de proxecto. Este rexistro sincronízase coas aplicacións de Finance and Operations que usan o mapa da táboa **Orixe de financiamento do proxecto (msdyn\_projectcontractssplitbillingrules)**. Este mapa tamén sincroniza as adicións, actualizacións e eliminacións de clientes do contrato do proxecto. As porcentaxes de facturación divididas entre os clientes do contrato do proxecto só se controlan en Dataverse e non se sincronizan coas aplicacións de Finance and Operations.

Despois de crear un contrato de proxecto en Dataverse, o contable do proxecto pode actualizar os atributos contables deste contrato de proxecto nas aplicacións de Finance and Operations indo a **Xestión e contabilidade de proxectos** > **Contratos de proxecto** > **Configurar** > **Mostrar contabilidade predefinida**. O contable pode revisar os atributos do contrato de proxecto operativo, como a data de entrega solicitada e o importe do contrato seleccionando o ID do contrato do proxecto nas aplicacións de Finance and Operations que abre o rexistro do contrato de proxecto relacionado en Dataverse.

A entidade do proxecto está sincronizada coas aplicacións de Finance and Operations que usan o mapa da táboa **Proxectos V2 (msdyn\_projects)**. O contable do proxecto pode:

  - Revise os proxectos nas aplicacións de Finance and Operations indo a **Xestión e contabilidade de proxectos** > **Todos os proxectos**. 
  - Actualice os atributos de contabilidade do proxecto nas aplicacións de Finance and Operations indo a **Xestión e contabilidade de proxectos** > **Todos os proxectos** > **Configurar** > **Mostrar contabilidade predefinida**.  
  - Revise os atributos operativos do proxecto, como as datas estimadas de inicio e fin, seleccionando o ID do proxecto nas aplicacións de Finance and Operations que abre o rexistro do proxecto relacionado en Dataverse.

Un proxecto asóciase a un contrato de proxecto a través da entidade **Liña de contrato de proxecto**.

As liñas do contrato do proxecto en Dataverse crean unha regra de facturación de contrato de proxecto nas aplicacións de Finance and Operations que usan o mapa da táboa **Liñas de contrato de proxecto (salesorderdetails)**. O método de facturación define o tipo de regra de facturación do contrato do proxecto nas aplicacións de Finance and Operations:

  - As liñas de contrato do proxecto cun método de facturación de tempo e material crean unha regra de facturación de tempo e tipo de material.
  - As liñas de contrato do método de facturación de prezo fixo crean unha regra de facturación de fitos.

O contable do proxecto pode revisar as liñas de contrato do proxecto nas aplicacións de Finance and Operations indo a **Xestión e contabilidade de proxectos** > **Contratos de proxecto** > **Configurar** > **Mostrar contabilidade predefinida** e revisando os detalles no separador **Liñas de contrato**. O contable tamén pode establecer dimensións financeiras predefinidas para as liñas de contrato do método de facturación de prezo fixo.

## <a name="billing-milestones"></a>Fitos de facturación

As liñas de contrato do proxecto que utilizan o método de facturación de prezo fixo factúranse mediante fitos de facturación. Os fitos de facturación sincronízanse coas transaccións a conta do proxecto nas aplicacións de Finance and Operations usando o mapa de táboa **Fitos da liña de contrato de integración de Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integración de fitos de facturación](./media/2Milestones.jpg)

O contable pode revisar as transaccións a conta e axustar os atributos contables desas transaccións dirixíndose a **Xestión e contabilidade de proxectos** > **Contratos de proxecto** > **Manter** > **Transaccións a conta** ou **Xestión de proxectos e contabilidade** > **Todos os proxectos** > **Manter** > **Transaccións a conta**.

Cando crea por primeira vez un fito de facturación para unha liña de contrato de proxecto determinada, o sistema crea automaticamente un proxecto de estimación de ingresos de prezo fixo para o proxecto asociado a esta liña de contrato. Os proxectos de estimación de ingresos a prezo fixo pódense revisar indo a **Xestión e contabilidade de proxectos** > **Proxectos de estimación de ingresos a prezo fixo**.

### <a name="project-tasks"></a>Tarefas do proxecto

As tarefas do proxecto están sincronizadas coas aplicacións de Finance and Operations a través do mapa da táboa **Tarefas de proxecto (msdyn\_projecttasks)** só para fins de referencia. As operacións de creación, actualización e eliminación non se admiten nas aplicacións de Finance and Operations.

  ![Integración de tarefas de proxecto](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de proxecto

A entidade **Roles de recursos de proxecto** está sincronizada coas aplicacións de Finance and Operations que usan o mapa de táboa **Roles de recursos do proxecto para todas as empresas (bookableresourcecategories)** só para fins de referencia. Como os roles de recursos en Dataverse non son específicos da empresa, o sistema crea automaticamente rexistros de roles de recursos específicos da empresa nas aplicacións de Finance and Operations para todas as entidades legais incluídas no ámbito de integración de escrita dual.

![Integración de roles de recursos](./media/5Resources.jpg)

Os recursos do proxecto en Project Operations mantéñense en Dataverse e non se sincronizan coas aplicacións de Finance and Operations.

### <a name="transaction-categories"></a>Categorías de transaccións

As categorías de transaccións mantéñense en Dataverse e sincronízanse coas aplicacións de Finance and Operations que usan o mapa de táboa **Categorías de transaccións do proxecto (msdyn\_transactioncategories)**. Despois de sincronizar o rexistro de categorías de transacción, o sistema crea automaticamente catro rexistros de categorías compartidas. Cada rexistro corresponde a un tipo de transacción nas aplicacións de Finance and Operations e as liga ao rexistro da categoría de transacción.

![integración de categorías de transacción](./media/4TransactionCategories.jpg)

O uso de categorías de transaccións para estimacións e datos reais require que o contable do proxecto ou o administrador do sistema creen categorías de proxectos correspondentes en todas as entidades legais. Para obter máis información, consulte [Configurar categorías de proxecto](../project-accounting/configure-project-categories.md).
