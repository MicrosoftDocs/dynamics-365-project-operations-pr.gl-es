---
title: Guía do xestor de recursos
description: Unha guía para a xestión de recursos en Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751461"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="8ebd9-103">Guía do xestor de recursos (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8ebd9-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8ebd9-104">As capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] axudan a buscar os recursos apropiados no momento adecuado e asegúranse de que todos os recursos se utilizan de maneira eficiente.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="8ebd9-105">Despregue os consultores da súa empresa de maneira eficiente e efectiva coa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="8ebd9-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="8ebd9-106">Fornécenlle as ferramentas necesarias para programar recursos baseándose nos requisitos e programacións de proxectos de consultoría e nos coñecementos e a dispoñibilidade dos consultores.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="8ebd9-107">Pode atopar con rapidez os consultores máis cualificados que están dispoñibles para traballar en proxectos e pode ver facilmente como programalas mellor durante cada proxecto.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="8ebd9-108">A programación de recursos axúdalle a facer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8ebd9-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="8ebd9-109">Relacione recursos con proxectos, segundo as súas calificacións e niveis de coñecemento coincidan cos requisitos de recursos de proxecto.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="8ebd9-110">Relacione a programación dun recurso cun calendario de proxecto, baseándose na súa dispoñibilidade e tempo libre programado.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="8ebd9-111">O calendario con códigos de cores ofrece apuntes visuais sobre dispoñibilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="8ebd9-112">Revise a capacidade de cada consultor e determine como esa capacidade se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="8ebd9-113">Isto pode axudar a saber se un consultor ten moito ou pouco traballo, ou se se está a traballar dentro da súa capacidade.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="8ebd9-114">Atribúa unha porcentaxe ou un número específico de horas de traballo á capacidade dun traballador para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="8ebd9-115">Faga reservas de recursos de grupo.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="8ebd9-116">Reserve recursos brandos ou duros e transforme horas brandas reservadas en horas duras nun único paso.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="8ebd9-117">Forme automaticamente un equipo de proxecto segundo os recursos definidos nunha estrutura de subdivisión do traballo para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="8ebd9-118">Realice solicitudes de recurso (reservar, propoñer, atopar substitutos de recursos).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="8ebd9-119">Atribuír os recursos segundo un modelo central (o xestor de recursos atribúe) ou híbrido (o xestor de recursos e outros xestores poden atribuír).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="8ebd9-120">Para obter máis información acerca da configuración central fronte ao modelo de xestión de recursos híbrido, consulte [Configurar parámetros adicionais de configuración (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="8ebd9-121">Pode xestionar recursos de maneira eficiente en proxectos e garantir que os proxectos teñen o persoal apropiado.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="8ebd9-122">Terá que realizar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="8ebd9-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="8ebd9-123">[Xestionar solicitudes de recursos](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="8ebd9-124">Relacionar os coñecementos e as cualificacións dos consultores cos proxectos apropiados.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="8ebd9-125">[Ver dispoñibilidade do recurso](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="8ebd9-126">Comprobar a dispoñibilidade dos consultores nunha visualización de calendario.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="8ebd9-127">[Ver a utilización de recursos](../project-service/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="8ebd9-128">Ver a porcentaxe do tempo que os consultores está actualmente reservados.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="8ebd9-129">[Programar recursos para un proxecto](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="8ebd9-130">Consultores de programación para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="8ebd9-131">Para obter máis información acerca do envío de solicitudes de recursos para proxectos individuais, consulte [Enviar solicitudes de recursos](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="8ebd9-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8ebd9-132">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="8ebd9-132">See Also</span></span>  
 <span data-ttu-id="8ebd9-133">[Información xeral de Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="8ebd9-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="8ebd9-134">[Guía do administrador](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8ebd9-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="8ebd9-135">[Guía do xestor de contas](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8ebd9-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="8ebd9-136">[Guía do xestor de proxectos](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8ebd9-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="8ebd9-137">Guía de tempo, gasto e colaboración</span><span class="sxs-lookup"><span data-stu-id="8ebd9-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
