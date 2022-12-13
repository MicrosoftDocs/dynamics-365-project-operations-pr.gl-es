---
title: Implementar Project Operations Lite
description: Este artigo ofrece información sobre como instalar o despregamento de Project Operations lite - de oferta a facturación proforma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810976"
---
# <a name="deploy-project-operations-lite"></a>Implementar Project Operations Lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_



Project Operations admite varios modelos de despregamento. Para determinar o mellor modelo de despregamento, consulte [Tipos de despregamento](determine-deployment-type.md).


> [!IMPORTANT]
> Este despregamento, o despregamento Lite - de oferta a facturación proforma, ten como resultado **Dataverse-só despregamento de Project Operations**.

- [Instalar Project Operations nun novo ambiente de Dataverse](#new)
- [Instalar nun ambiente de Dataverse existente](#existing)
- [Instala nun Dataverse entorno existente que teña compoñentes de escritura dual](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Instala Project Operations Lite nun novo Dataverse entorno

1. Como [Administrador global ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, cree un novo ambiente de Dataverse no [Centro de administración de PowerPlatform](https://admin.powerplatform.com). Asegúrese de que **Crear unha base de datos para este ambiente** e **Aplicacións de Dynamics 365** estean habilitados. Para obter información, consulte [Crear e xestionar ambientes no centro de administración de Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Seleccione **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instala Project Operations Lite nun Dataverse entorno existente 
1. Como o [Administrador global ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, localice o ambiente no [Centro de administración de PowerPlatform](https://admin.powerplatform.com) onde desexa instalar Project Operations.
1. Instale **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365. Para obter máis información, consulte [Xestionar aplicacións de Dynamics 365](/power-platform/admin/manage-apps)

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Instala Project Operations Lite nun Dataverse entorno existente onde xa hai solucións de escritura dual

Se queres seguir executando as operacións do proxecto no modo de implantación simplificada, debes seguir estes pasos:

1. Como o [Administrador global ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, localice o ambiente no [Centro de administración de PowerPlatform](https://admin.powerplatform.com) onde desexa instalar Project Operations.
1. Instale **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365. Para obter máis información, consulte [Xestionar aplicacións de Dynamics 365](/power-platform/admin/manage-apps)
1. Dado que o teu ambiente ten instalados compoñentes de escritura dual que axudan a integrar as aplicacións de financiamento e operacións, a instalación de Project Operations tamén instalará as capacidades e extensións necesarias para integrar os datos relacionados co proxecto coas aplicacións de financiamento e operacións. Dado que quere executar as operacións do proxecto na implementación Lite, estes compoñentes de integración deben eliminarse xa que crearán restricións e sobrecargas para os escenarios de implementación Lite. Desinstale manualmente as solucións **Dynamics 365 Project Operations Escritura dual** e **Dynamics 365 Project Operations Mapas de entidades de escritura dual** para eliminar estes compoñentes.
1. Vaia a **Operacións do proxecto -> Configuración -> Parámetros**. Abra a páxina de detalles do **Parámetro do proxecto** e configure o campo **Comportamento de actualización da solución** en **Lite Só**. Isto garante que as actualizacións posteriores de Project Operations non devolverán os compoñentes de integración a Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
