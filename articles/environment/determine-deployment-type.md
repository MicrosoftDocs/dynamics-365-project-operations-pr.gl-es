---
title: Tipos de despregamento
description: Este tema ofrece información para axudarlle a determinar o tipo de despregamento correcto das operacións do proxecto para a súa empresa.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948858"
---
# <a name="deployment-types"></a>Tipos de despregamento

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

> [!IMPORTANT]
> Despois de mercar a licenza, comece aquí para determinar o mellor modelo de despregamento de Dynamics 365 Project Operations usando o [Fluxo de instalación guiado](https://aka.ms/provisionprojectoperations).
> Despois de completar o fluxo de instalación guiada, dirixiráselle ao portal de xestión correcto para completar a instalación. Vexa os detalles de despregamento a seguir para completar a instalación.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation
Project Operations inclúe as capacidades que se fornecen con Project Service Automation. No futuro publicarase unha ruta de actualización para estes clientes.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clientes existentes de Dynamics 365 Finance empregando a xestión e a contabilidade do proxecto 

Os clientes existentes de Finance que empregan a funcionalidade de xestión e contabilidade de proxectos poden seguir usando isto tal como está. Consulte [Project Operations para situacións baseadas en recursos/sen fornecemento](#pma).

Project Operations admite varias opcións de despregamento para adaptarse ás súas necesidades. Se vostede é un cliente novo ou existente de Dynamics 365, Project Operations pode atender ás súas necesidades.

O noso [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations) axudaralle a determinar o despregamento correcto. Os resultados guiarano cara a un dos seguintes tipos de despregamento:

- [Despregamento de Lite: acordo para facturación proforma](#lite)
- [Project Operations para escenarios baseados en recursos ou sen existencias](#integrated)
- [Project Operations para situacións baseadas en recursos/sen fornecemento](#pma)

Project Operations admite situacións de pedidos de produción/con fornecemento e situacións baseadas en recursos/sen fornecemento no mesmo ambiente a través de configuracións a nivel de entidade legal. Por exemplo, Contoso pode aproveitar as capacidades de pedidos de produción/con forncemento nas súas instalacións de fabricación de Estados Unidos (entidade legal = Contoso Manufacturing United States) e as capacidades baseadas en recursos/sen fornecemento na súa instalación de servizos de Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics United Kingdom).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Despregamento de Lite: acordo para facturación proforma
O despregamento lite inclúe as seguintes capacidades:

- Planificación de proxectos mediante Microsoft Project para a web
- Prezos multidimensionais
- Xestión de recursos unificada
- Rastrexo de tempo
- Gasto básico
- Proposta de factura

### <a name="deployment-steps"></a>Pasos de despregamento:
Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).

Para este despregamento, consulte [Rexistro para subscricións de previsualización](lite-preview-subscription-sign-up.md) e [Fornecer a novo ambiente](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations para escenarios baseados en recursos ou sen existencias
Project Operations para situacións de recursos/sen fornecemento inclúe as seguintes capacidades:
  
- Planificación de proxectos mediante Microsoft Project para a web
- Prezos multidimensionais
- Xestión de recursos unificada
- Rastrexo de tempo
- Gasto básico
- Gasto completo
- OCR de recibos
- Facturación completa
- Recoñecemento de ingresos

### <a name="deployment-steps"></a>Pasos de despregamento:
Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).

Para este despregamento, consulte [Rexistro para subscricións de previsualización](resource-sign-up-preview-subscription.md) e [Fornecer a novo ambiente](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations para situacións baseadas en recursos/sen fornecemento

- Planificación de proxectos mediante WBS
- Xestión de recursos
- Rastrexo de tempo
- Gasto completo
- OCR de recibos
- Facturación completa
- Recoñecemento de ingresos
- Pedidos de produción
- Asistencia técnica para materiais

### <a name="deployment-steps"></a>Pasos de despregamento:
Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).

Para este despregamento, consulte [Rexistro para subscricións de previsualización](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Fornecer a novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



