---
title: Activar as funcionalidades da aplicación Project Finder Mobile
description: Como activar as funcionalidades de Project Finder Mobile para Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076139"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Activar as funcionalidades da aplicación Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Os seus recursos poden utilizar a apl. Project Finder Mobile nos seus teléfonos con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para localizar proxectos novos nos que traballar e actualizar os seus conxuntos de cualificacións.  
  
 A aplicación está dispoñible para teléfonos [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Debe definir un par de opcións na configuración de parámetros para a unidade de organización que permitan aos usuarios ver os requisitos de recurso dos proxectos e actualizar os seus coñecementos.  
  
> [!NOTE]
>  A aplicación Project Finder Mobile só funciona con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], non con instalacións locais.  
  
1. Vaia a **Project Service > Parámetros**  
  
2. Prema na configuración de parámetros que desexa utilizar para permitir as funcionalidades da aplicación Project Finder Mobile.  
  
3. Na área **Xeral** , defina **Requisitos de Recursos visibles para os recursos** en **Si**.  
  
4. Defina **Permitir actualización de habilidades por recurso** en **Si**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Esta é unha configuración global. Os xestores de proxecto poden definir se un proxecto individual será visible na páxina dese proxecto **Equipo de proxecto**.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notificacións de correo electrónico  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envía correos referentes ás solicitudes de recursos para os destinatarios seguintes nos casos seguintes:  
  
|Destinatario|Evento|  
|---------------|-----------|  
|Xestor de proxectos|-   Cando un recurso se rexistra para un proxecto coa aplicación Project Finder Mobile.|  
|Recurso|-  Cando o traballo do proxecto para o que o recurso se rexistrou xa foi realizado por outro recurso.<br />-  Cando as súas solicitudes de aprobación de coñecementos están aprobadas ou rexeitadas.<br />-  Cando as súas solicitudes de rexistro de proxecto están aprobadas ou rexeitadas.|  
  
## <a name="privacy-notice"></a>Aviso de privacidade  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Consulte tamén  
 [Configurar recursos reservables](../psa/set-up-resources.md)
