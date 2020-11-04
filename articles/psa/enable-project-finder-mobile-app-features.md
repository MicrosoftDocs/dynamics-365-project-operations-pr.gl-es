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
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="f9e29-103">Activar as funcionalidades da aplicación Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f9e29-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f9e29-104">Os seus recursos poden utilizar a apl. Project Finder Mobile nos seus teléfonos con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para localizar proxectos novos nos que traballar e actualizar os seus conxuntos de cualificacións.</span><span class="sxs-lookup"><span data-stu-id="f9e29-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="f9e29-105">A aplicación está dispoñible para teléfonos [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="f9e29-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="f9e29-106">Debe definir un par de opcións na configuración de parámetros para a unidade de organización que permitan aos usuarios ver os requisitos de recurso dos proxectos e actualizar os seus coñecementos.</span><span class="sxs-lookup"><span data-stu-id="f9e29-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f9e29-107">A aplicación Project Finder Mobile só funciona con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], non con instalacións locais.</span><span class="sxs-lookup"><span data-stu-id="f9e29-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="f9e29-108">Vaia a **Project Service > Parámetros**</span><span class="sxs-lookup"><span data-stu-id="f9e29-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="f9e29-109">Prema na configuración de parámetros que desexa utilizar para permitir as funcionalidades da aplicación Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="f9e29-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="f9e29-110">Na área **Xeral** , defina **Requisitos de Recursos visibles para os recursos** en **Si**.</span><span class="sxs-lookup"><span data-stu-id="f9e29-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="f9e29-111">Defina **Permitir actualización de habilidades por recurso** en **Si**.</span><span class="sxs-lookup"><span data-stu-id="f9e29-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="f9e29-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="f9e29-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="f9e29-113">Esta é unha configuración global.</span><span class="sxs-lookup"><span data-stu-id="f9e29-113">This is a global setting.</span></span> <span data-ttu-id="f9e29-114">Os xestores de proxecto poden definir se un proxecto individual será visible na páxina dese proxecto **Equipo de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="f9e29-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="f9e29-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="f9e29-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="f9e29-116">Notificacións de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="f9e29-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="f9e29-117">envía correos referentes ás solicitudes de recursos para os destinatarios seguintes nos casos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f9e29-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="f9e29-118">Destinatario</span><span class="sxs-lookup"><span data-stu-id="f9e29-118">Recipient</span></span>|<span data-ttu-id="f9e29-119">Evento</span><span class="sxs-lookup"><span data-stu-id="f9e29-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="f9e29-120">Xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="f9e29-120">Project manager</span></span>|<span data-ttu-id="f9e29-121">-   Cando un recurso se rexistra para un proxecto coa aplicación Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="f9e29-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="f9e29-122">Recurso</span><span class="sxs-lookup"><span data-stu-id="f9e29-122">Resource</span></span>|<span data-ttu-id="f9e29-123">-  Cando o traballo do proxecto para o que o recurso se rexistrou xa foi realizado por outro recurso.</span><span class="sxs-lookup"><span data-stu-id="f9e29-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="f9e29-124">-  Cando as súas solicitudes de aprobación de coñecementos están aprobadas ou rexeitadas.</span><span class="sxs-lookup"><span data-stu-id="f9e29-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="f9e29-125">-  Cando as súas solicitudes de rexistro de proxecto están aprobadas ou rexeitadas.</span><span class="sxs-lookup"><span data-stu-id="f9e29-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="f9e29-126">Aviso de privacidade</span><span class="sxs-lookup"><span data-stu-id="f9e29-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="f9e29-127">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="f9e29-127">See Also</span></span>  
 [<span data-ttu-id="f9e29-128">Configurar recursos reservables</span><span class="sxs-lookup"><span data-stu-id="f9e29-128">Set up resources</span></span>](../psa/set-up-resources.md)
