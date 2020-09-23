---
title: Reservar recursos reservables nomeados para un equipo de proxectos e atribuír tarefas
description: Este tema fornece información sobre a reserva de recursos nomeados para equipos de proxectos e atribuírlles tarefas.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e947986a-e83a-42f4-813e-c82bdfbec33c
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 079ba299f912c75f9ed739d4b6aa3c63189d11d0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751338"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="a8a0d-103">Reservar recursos reservables nomeados para un equipo de proxectos e atribuír tarefas</span><span class="sxs-lookup"><span data-stu-id="a8a0d-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a8a0d-104">Pode engadir un recurso nomeado ao seu equipo de proxectos reservándoo directamente ao equipo.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="a8a0d-105">Para facelo, siga os pasos que se indican a continuación:</span><span class="sxs-lookup"><span data-stu-id="a8a0d-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="a8a0d-106">En Project Service Automation, vaia a **Proxectos** e seleccione abrir o proxecto para o que vai reservar.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="a8a0d-107">Na páxina **Proxecto**, no separador **Equipo**, prema **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Engadir un membro do equipo no separador do equipo](media/RM-how-to-1.png)

3. <span data-ttu-id="a8a0d-109">Na caixa de diálogo **Creación rápida de membro do equipo de proxecto**, seleccione o recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="a8a0d-110">O campo **Rol** encherase co rol predefinido do recurso se ten un atribuído.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="a8a0d-111">Pode cambiar o rol se fose necesario.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="a8a0d-112">Seleccione as datas desde e ata nas que se necesitará o recurso e seleccione o método de atribución da capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="a8a0d-113">Se desexa que o membro do equipo sexa o responsable da a probación do proxecto, seleccione **Si** no campo **Responsable de aprobación do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="a8a0d-114">Isto suporá que o membro do equipo pode aprobar as entradas de tempo e gastos presentadas para este proxecto.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="a8a0d-115">Prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-115">Click **Save**.</span></span>

![Engadir un membro do equipo no formulario de creación rápida](media/RM-how-to-2.png)


<span data-ttu-id="a8a0d-117">Agora pode atribuír o recurso reservado a tarefas do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="a8a0d-118">Na páxina **Proxecto**, prema o separador **Programación** para atribuír tarefas ao novo recurso.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="a8a0d-119">O selector de recursos que se inicia desde o campo **Recursos** na grada de tarefas amosará os membros do equipo que pode seleccionar.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Atribución dun membro do equipo a unha tarefa no separador de programación](media/RM-how-to-3.png)

<span data-ttu-id="a8a0d-121">Na versión 3 para Project Service Automation (PSA), as reservas de recursos e as atribucións de tarefas non están moi integradas.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="a8a0d-122">Isto significa que cando utiliza o selector de recursos na programación, pode atribuír tarefas aos membros do equipo durante máis horas das que cobren as súas reservas no proxecto.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="a8a0d-123">Podes ver as diferenzas entre as reservas e atribucións dos membros do equipo no separador **Equipo** ou no separador **Reconciliación de recursos**. Tamén pode reconciliar as diferenzas entre reservas e atribucións de recursos a un nivel máis detallado.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Separador de reconciliación de recursos](media/RM-how-to-4.png)

<span data-ttu-id="a8a0d-125">Tamén pode usar o selector de recursos no separador **Programación** para buscar e seleccionar recursos reservables que xa non forman parte do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="a8a0d-126">Estes móstranse no selector de recursos como **Outros recursos**.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Atribución dun recurso que non é membro do equipo a unha tarefa](media/RM-how-to-5.png)

<span data-ttu-id="a8a0d-128">Cando fai isto, o recurso engádese ao equipo do proxecto e atribúese á tarefa, pero non se xeran reservas.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Membro do equipo con atribucións e sen reservas](media/RM-how-to-6.png)

<span data-ttu-id="a8a0d-130">Pode usar a capacidade de extensión de recursos no separador **Reconciliación** ou o **Panel de programación** para reservar a capacidade do recurso para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Extensión das reservas para un membro do equipo no separador de reconciliación de recursos](media/RM-how-to-7.png)

<span data-ttu-id="a8a0d-132">Despois de que un membro do equipo estea reservado no seu proxecto, pode manter as reservas ou usar o panel de programación para xestionar as súas reservas.</span><span class="sxs-lookup"><span data-stu-id="a8a0d-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
