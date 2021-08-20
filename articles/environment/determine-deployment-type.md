---
title: Determinar o seu tipo de despregamento
description: Este tema ofrece información para axudarlle a determinar o tipo de despregamento correcto das operacións do proxecto para a súa empresa.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 4be8e69c5b6ff1ed65e9484a9b427bb428f7ff3e6dc597c615d5586da52867ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994634"
---
# <a name="determine-your-deployment-type"></a>Determinar o seu tipo de despregamento

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

> [!IMPORTANT]
> Despois de mercar a licenza, comece aquí para determinar o mellor modelo de despregamento de Dynamics 365 Project Operations usando o [Fluxo de instalación guiado](https://aka.ms/provisionprojectoperations).
> Despois de completar o fluxo de instalación guiada, dirixiráselle ao portal de xestión correcto para completar a instalación. Vexa os detalles de despregamento para completar a instalación.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation
Project Operations inclúe as capacidades que se fornecen con Project Service Automation. Publicarase un camiño de actualización para estes clientes na onda 1 da versión de 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clientes existentes de Dynamics 365 Finance empregando a xestión e a contabilidade do proxecto 

Os clientes existentes de Finance que empregan a funcionalidade de xestión e contabilidade de proxectos poden seguir empregándoa tal como está. Consulte [Project Operations para situacións baseadas en recursos/sen fornecemento](#pma).


## <a name="deployment-regions"></a>Rexións de despregamento
Para determinar que rexións admiten o despregamento de Project Operations, consulte [Dispoñibilidade xeográfica para Dynamics 365 e informe de Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Seleccione **Ver informe** e expanda **Dynamics 365> Aplicacións de operacións > Dynamics 365 Project Operations** para ver as rexións admitidas.

## <a name="deployment-types"></a>Tipos de despregamento
Project Operations admite varias opcións de despregamento para adaptarse ás súas necesidades. Se vostede é un cliente novo ou existente de Dynamics 365, Project Operations pode atender ás súas necesidades.

O noso [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations) axudaralle a determinar o despregamento correcto. Os resultados guiarano cara a un dos seguintes tipos de despregamento:

- [Despregamento de Lite: acordo para facturación proforma](#lite)
- [Project Operations para escenarios baseados en recursos ou sen existencias](#integrated)
- [Project Operations para situacións baseadas en recursos/sen fornecemento](#pma)

Project Operations admite situacións de pedidos de produción/con fornecemento e situacións baseadas en recursos/sen fornecemento no mesmo ambiente a través de configuracións a nivel de entidade legal. Por exemplo, Contoso pode utilizar as capacidades de pedido baseadas en produción/con fornecemento na súa fábrica estadounidense (entidade legal = Contoso Manufacturing Estados Unidos). Contoso pode empregar as capacidades baseadas en recursos/sen fornecemento na súa instalación de servizo de Contoso Robotic Arms no Reino Unido (entidade legal = Contoso Robotics Reino Unido).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Despregamento de Lite: acordo para facturación proforma

O despregamento lite inclúe as seguintes capacidades:

- Proceso de vendas para proxectos que amplían as experiencias da aplicación Dynamics 365 Sales
- Planificación de proxectos mediante Microsoft Project para a web
- Prezos multidimensionais
- Xestión de recursos unificada
- Rastrexo de tempo
- Gasto básico
- Facturación proforma para revisión e edicións do xestor de proxectos 

#### <a name="deployment-steps"></a>Pasos de despregamento
Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).

Para este despregamento, consulte [Rexistro para subscricións de previsualización](lite-preview-subscription-sign-up.md) e [Fornecer a novo ambiente](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations para escenarios baseados en recursos ou sen existencias
Project Operations para situacións de recursos/sen fornecemento inclúe as seguintes capacidades:
 
- Proceso de vendas para proxectos que amplían a aplicación Dynamics 365 Sales
- Planificación de proxectos mediante Microsoft Project para a web
- Prezos multidimensionais
- Xestión de recursos unificada
- Rastrexo de tempo
- Gasto básico
- Gasto completo
- OCR de recibos
- Facturación proforma e orientada ao cliente 
- Recoñecemento de ingresos para proxectos

#### <a name="deployment-steps"></a>Pasos de despregamento
Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).

Para este despregamento, consulte [Rexistro para subscricións de previsualización](resource-sign-up-preview-subscription.md) e [Fornecer a novo ambiente](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations para situacións baseadas en recursos/sen fornecemento

- Planificación de proxectos mediante WBS
- Xestión de recursos
- Rastrexo de tempo
- Gasto completo
- OCR de recibos
- Facturación completa
- Recoñecemento de ingresos
- Pedidos de produción
- Asistencia de materiais con existencias e con inventario

#### <a name="deployment-steps"></a>Pasos de despregamento
Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).

Para este despregamento, consulte [Rexistro para subscricións de previsualización](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) e [Fornecer a novo ambiente](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]