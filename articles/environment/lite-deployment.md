---
title: Despregar Project Operations - lite
description: 'Este artigo ofrece información sobre como instalar a implementación de Project Operations lite: xestionar a facturación proforma.'
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930316"
---
# <a name="deploy-project-operations---lite"></a>Despregar Project Operations - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_



Project Operations admite varios modelos de despregamento. Para determinar o mellor modelo de despregamento, consulte [Tipos de despregamento](determine-deployment-type.md).


> [!IMPORTANT]
> Este despregamento, o despregamento Lite - de oferta a facturación proforma, ten como resultado **Dataverse-só despregamento de Project Operations**.

- [Instala Project Operations nun novo Dataverse ambiente](#new)
- [Instalar nun existente Dataverse ambiente](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Instala Project Operations nun novo Dataverse ambiente

1. Como o [Global ou Power Platform Administrador](/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, cree unha nova Dataverse ambiente no [Centro de administración de PowerPlatform](https://admin.powerplatform.com). Asegúrate de que **Crea unha base de datos para este entorno** e **Aplicacións de Dynamics 365** están habilitados. Para obter información, consulte [Crear e xestionar ambientes no centro de administración de Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Seleccione **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instalar Project Operations nun existente Dataverse ambiente
1. Asegúrese de que o ambiente non foi configurado [escritura dual](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) xa que a instalación instalará entón o [Operacións do proxecto para escenarios baseados en recursos/non abastecidos](project-operations-integrated-deployment-overview.md) capacidades.
2. Como o [Administrador global ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, localice o ambiente no [Centro de administración de PowerPlatform](https://admin.powerplatform.com) onde desexa instalar Project Operations.
3. Instale **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365. Para obter máis información, consulte [Xestionar aplicacións de Dynamics 365](/power-platform/admin/manage-apps)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
