---
title: Sincronizar contratos de proxectos e proxectos directamente desde Project Service Automation a Finance and Operations
description: Este tema describe o modelo e as tarefas subxacentes que se usan para sincronizar os contratos do proxecto e os proxectos directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0b3bc159fff25c4f6e5b1ed1b2eabbba675fb0f5
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642631"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar contratos de proxectos e proxectos directamente desde Project Service Automation a Finance and Operations

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tema describe o modelo e as tarefas subxacentes que se usan para sincronizar os contratos do proxecto e os proxectos directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE] 
> Se está a usar Enterprise edition 7.3.0, debe instalar KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de datos de Project Service Automation a Finanzas

> [!NOTE]
> Antes de que poida usar a solución de integración de Project Service Automation a Finanzas, debería estar familiarizado coa funcionalidade de integración de datos de Dynamics 365.

A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas. O modelo de integración dispoñible coa funcionalidade de integración de datos permite o fluxo de datos sobre contratos de proxectos, proxectos, liñas de contratos de proxectos e fitos da liña de contratos de proxectos de Project Service Automation a Finanzas.

A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.

[![Fluxo de datos para a integración de Project Service Automation con Finanzas](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Modelos e tarefas

Para acceder aos modelos dispoñibles, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.

Os seguintes modelos e as tarefas subxacentes úsanse para sincronizar os contratos de proxectos e os proxectos de Project Service Automation a Finanzas:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integración con Dynamics 365 Project Service Automation v2.x
- **Nome do modelo en integración de datos:** Proxectos e contratos (PSA a Fin e Ops)
- **Nome das tarefas do proxecto:**

    - Contratos de proxectos de PSA a Fin e Ops
    - Proxectos de PSA a Fin e Ops
    - Liñas de contratos de proxectos de PSA a Fin e Ops
    - Fitos de liñas de contratos de proxectos de PSA a Fin e Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integración con Dynamics 365 Project Service Automation v3.x
Hai un cambio de esquema en Project Service Automation que afecta ao modelo de fito da liña de contrato do proxecto e é necesario o uso da versión v2 do modelo para integrar Project Service Automation v3.x con Dynamics 365.

- **Nome do modelo en integración de datos:** Proxectos e contratos (PSA 3.x a Fin e Ops) - v2
- **Nome das tarefas do proxecto:**

    - Contratos de proxectos de PSA a Fin e Ops
    - Proxectos de PSA a Fin e Ops
    - Liñas de contratos de proxectos de PSA a Fin e Ops
    - Fitos de liñas de contratos de proxectos de PSA a Fin e Ops

Antes de que poida producirse a sincronización de contratos de proxectos e proxectos, debe sincronizar as contas.

## <a name="entity-set"></a>Conxunto de entidades

| Project Service Automation       | Finanzas                                                |
|----------------------------------|--------------------------------------------------------|
| Pedidos                           | Entidade de integración para contrato do proxecto                |
| Proxectos                         | Entidade de integración para proxecto                         |
| Liñas de pedido                      | Entidade de integración para liña de contrato do proxecto           |
| Fitos da liña de contrato do proxecto | Entidade de integración para fito de liña de contrato do proxecto |

## <a name="entity-flow"></a>Fluxo de entidades

Os contratos do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como contratos de proxecto. Como parte do modelo de integración, pode configurar a fonte de integración en Finanzas para o contrato do proxecto.

O proxecto de tempo e material e os proxectos de prezo fixo xestiónanse en Project Service Automation e sincronízanse con Finanzas como proxectos. Como parte da integración do modelo, pode configurar a fonte de integración en Finanzas para o contrato do proxecto.

As liñas do contrato do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como regras de facturación dos contratos de proxecto. Se o método de facturación é diferente do tipo de proxecto predefinido, a sincronización actualiza o tipo de proxecto para o proxecto da liña de contrato e o grupo de proxectos.

Os fitos das liñas do contrato do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como fitos das regras de facturación dos contratos de proxecto.

## <a name="project-service-automation-to-finance-integration-solution"></a>Solución de integración de Project Service Automation con Finance

O campo **ID do contrato do proxecto** está dispoñible na páxina **Contratos de proxecto**. Este campo converteuse nunha clave natural e única para apoiar a integración.

Cando se crea un novo contrato de proxecto, se o valor de **ID do contrato do proxecto** aínda non existe, xérase automaticamente usando unha secuencia de números. O valor consiste en **ORD** seguido dunha secuencia numérica crecente e despois dun sufixo de seis caracteres. Este é un exemplo: **ORD-01022-Z4M9Q0**.

O campo **Número do proxecto** está dispoñible na páxina **Proxectos**. Este campo converteuse nunha clave natural e única para apoiar a integración.

Cando se crea un novo proxecto, se o valor de **Número do proxecto** aínda non existe, xérase automaticamente usando unha secuencia de números. O valor consiste en **PRJ** seguido dunha secuencia numérica crecente e despois dun sufixo de seis caracteres. Este é un exemplo: **PRJ-01049-CCNID0**.

Cando se aplica a solución de integración de Project Service Automation con Finanzas, unha cadea de actualización establece o campo **ID do contrato do proxecto** para contratos de proxecto existentes e o campo **Número do proxecto** para proxectos existentes en Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Requisitos previos e configuración de asignación

- Antes de que poida producirse a sincronización de contratos de proxectos e proxectos, debe sincronizar as contas.
- No seu conxunto de conexións, engada unha asignación de campos clave de integración para **msdyn\_organizationalunits** a **msdyn\_name \[Nome\]**. Primeiro pode que teña que engadir un proxecto ao conxunto de conexións. Para obter máis información, consulte [Integrar datos en Common Data Service para aplicacións](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- No seu conxunto de conexións, engada unha asignación de campos clave de integración para **msdyn\_projects** a **msdynce\_projectnumber \[Número de proxecto\]**. Primeiro pode que teña que engadir un proxecto ao conxunto de conexións. Para obter máis información, consulte [Integrar datos en Common Data Service para aplicacións](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** para contratos de proxectos e proxectos pódese actualizar a un valor diferente ou eliminar da asignación. O valor predefinido do modelo é **Project Service Automation**.
- A asignación **PaymentTerms** debe actualizarse para que reflicta termos de pagamento válidas en Finanzas. Tamén pode eliminar a asignación da tarefa do proxecto. A asignación de valores predefinidos ten valores predefinidos para os datos de demostración. A seguinte táboa mostra os valores en Project Service Automation.

    | Valor | Descripción   |
    |-------|---------------|
    | 1     | Pagamento a 30 días        |
    | 2     | 2 % 10, pagamento a 30 días |
    | 3     | Pagamento a 45 días        |
    | 4     | Pagamento a 60 días        |

## <a name="power-query"></a>Power Query

Debe usar Microsoft Power Query for Excel para filtrar os datos se se cumpren as seguintes condicións:

- Vostede ten pedidos de vendas en Dynamics 365 Sales.
- Ten varias unidades organizativas en Project Service Automation e estas unidades organizativas asignaranse a varias persoas xurídicas en Finanzas.

Se debe usar Power Query, siga estas pautas:

- O modelo Proxectos e contratos (PSA a Fin e Ops) ten un filtro predefinido que só inclúe pedidos de venda do tipo **Artigo de traballo (msdyn\_ordertype = 192350001)**. Este filtro axuda a garantir que non se crean contratos de proxectos para pedidos de vendas en Finanzas. Se crea o seu propio modelo, debe engadir este filtro.
- Debe crear un filtro de Power Query que inclúa só as organizacións do contrato que deben sincronizarse coa persoa xurídica do conxunto de conexións de integración. Por exemplo, os contratos de proxectos que vostede ten coa unidade organizativa do contrato de Contoso US deben sincronizarse coa persoa xurídica USSI, pero os contratos de proxectos que teña coa unidade organizativa do contrato de Contoso Global deben sincronizarse coa persoa xurídica USMF. Se non engade este filtro á súa asignación de tarefas, todos os contratos do proxecto sincronizaranse coa persoa xurídica que se define para o conxunto de conexións, independentemente da unidade organizativa do contrato.

## <a name="template-mapping-in-data-integration"></a>Asignación de modelos na integración de datos

> [!NOTE] 
> Os campos **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** e **AddressZipCode** non están incluídos na asignación predefinida para contratos de proxectos. Pode engadir as asignacións se precisa que estes datos se sincronicen para contratos de proxectos.
>
> Os campos **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** e **ProjectType** non están incluídos na asignación predefinida para proxectos. Pode engadir as asignacións se precisa que estes datos se sincronicen para proxectos.

As seguintes ilustracións mostran exemplos das asignacións de tarefas do modelo en integración de datos. A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.

[![Asignación de modelos de contrato de proxecto](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Asignación de modelos de proxecto](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Asignación de modelos de liñas de contrato de proxecto](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Asignación de modelos de fitos de liñas de contrato de proxecto](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Asignación de fitos da liña de contrato de proxecto nos proxectos e contratos (PSA 3.x a Dynamics) - modelo v2:

[![Asignación de fitos de liñas de contrato de proxecto coa versión dúas do modelo](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
