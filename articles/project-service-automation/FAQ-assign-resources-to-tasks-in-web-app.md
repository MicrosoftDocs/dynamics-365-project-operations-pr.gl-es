---
title: Como podo atribuír un recurso reservable a unha tarefa na aplicación web
description: Unha visión xeral das formas en que pode asignar recursos reservables.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751482"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="ac2fb-103">Como podo atribuír un recurso reservable a unha tarefa na aplicación web (aplicación Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="ac2fb-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ac2fb-104">Hai dúas formas de atribuír un recurso a unha tarefa en Project Service.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="ac2fb-105">Pode reservar un recurso como un membro do equipo e, a seguir, atribuílo a unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="ac2fb-106">Tamén pode crear un membro do equipo xenérico a través de atribución de rol en tarefas, xerar un equipo e, a seguir, cumplir os requisitos de seguranza cun recurso denominado.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="ac2fb-107">Teña en conta que se se quere atribuír un recurso reservable a unha tarefa, o membro do equipo de recurso reservable debe ter suficientes reservas dispoñibles.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="ac2fb-108">O estado da reserva debe ser Tipo de compromiso reserva dura, e Estado comprometido.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="ac2fb-109">Se non hai suficiente reservas para o recurso, Project Service elimina a atribución e mostra a mensaxe de erro seguinte:</span><span class="sxs-lookup"><span data-stu-id="ac2fb-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="ac2fb-110">*Non é posible atribuír recurso á tarefa - Os seguintes recursos non teñen suficientes horas reservadas contra proxecto*</span><span class="sxs-lookup"><span data-stu-id="ac2fb-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="ac2fb-111">Reserve un recurso como un membro do equipo e, a seguir, atribúa o recurso a unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="ac2fb-112">Con este método pode engadir un recurso ao equipo de proxecto e, a seguir, atribuír as tarefas ao recurso na programación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="ac2fb-113">Aquí atopará a forma de facelo:</span><span class="sxs-lookup"><span data-stu-id="ac2fb-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="ac2fb-114">Na grade de membro do equipo, engada un novo membro do equipo seleccionando **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="ac2fb-115">Na pantalla Creación rápida de membro do equipo, seleccione o nome do recurso reservable e defina un rol.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="ac2fb-116">Seleccione as datas **Desde** e **Para**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ac2fb-117">![Captura de pantalla de engadir membro do equipo](media/FAQ-Resources-to-Tasks2-1.png "Captura de pantalla de engadir membro do equipo")</span><span class="sxs-lookup"><span data-stu-id="ac2fb-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="ac2fb-118">Seleccione un dos seguintes métodos de atribución para o reservar o recurso:</span><span class="sxs-lookup"><span data-stu-id="ac2fb-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="ac2fb-119">**Capacidade completa** reserva a capacidade completa do recurso para as datas desde e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="ac2fb-120">**Capacidade da porcentaxe** reserva unha porcentaxe da capacidade do recurso para as datas desde e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="ac2fb-121">**Por horas: distribuír uniformemente** reserva o recurso para un número de horas especificado, e distribúe o tempo de forma similar por día sobre as datas esde e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="ac2fb-122">**Por horas: carga frontal** reserva o recurso para un número de horas especificado, con carga frontal das horas por día sobre as datas desde e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="ac2fb-123">Non seleccione **Ningún** porque engade o recurso ao equipo, pero non crea ningunha reserva que absorba a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="ac2fb-124">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-124">Select **Save**.</span></span>

    <span data-ttu-id="ac2fb-125">Teña en conta que as horas da reserva deben ser suficientes para cubrir as horas de traballo e os intervalos de datas das tarefas que atribúa a este recurso.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="ac2fb-126">Se non están aliñadas, non pode atribuír o recurso á tarefa.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="ac2fb-127">Na estrutura de subdivisión do traballo (WBS) da tarefa, prema o despregable da cela de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="ac2fb-128">A seguir:</span><span class="sxs-lookup"><span data-stu-id="ac2fb-128">Then:</span></span> 

    1. <span data-ttu-id="ac2fb-129">Seleccione **Engadir**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-129">Select **Add**.</span></span>
    2. <span data-ttu-id="ac2fb-130">Seleccione o despregable en **Recursos** e seleccione o membro do equipo que engadiu anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="ac2fb-131">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-131">Select **OK**.</span></span> <span data-ttu-id="ac2fb-132">Agora, o membro do equipo agora atribuído á tarefa.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ac2fb-133">![Captura de pantalla de engadir recursos con WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de pantalla de engadir recursos con WBS")</span><span class="sxs-lookup"><span data-stu-id="ac2fb-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="ac2fb-134">Na grade de membro do equipo, verá o total das horas atribuídas do recurso Horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="ac2fb-135">Será igual ou inferior ás horas reservadas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ac2fb-136">![Captura de pantalla das horas asignadas para un recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de pantalla das horas asignadas para un recurso")</span><span class="sxs-lookup"><span data-stu-id="ac2fb-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="ac2fb-137">Se a tarefa que tenta atribuír ao recurso comeza despóis da data de fin das reservas de recursos, o recurso non aparecerán no despregable.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="ac2fb-138">Teña en conta que pode atribuír un recurso a máis horas das horas reservadas se o recurso ten capacidade restante non atribuída.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="ac2fb-139">Neste caso o recurso só se atribuirá parcialmente até as súas reservas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="ac2fb-140">Pode ver as horas de tarefa non atribuídas restantes engadindo a columna Horas sen personal á estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="ac2fb-141">Se os recursos están atribuidos ás súas horas reservadas (as súas horas reservadas serán iguais que as súas horas atribuídas), poderá ver a seguinte mensaxe de erro ao tentar atribuírlles máis tarefas:</span><span class="sxs-lookup"><span data-stu-id="ac2fb-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="ac2fb-142">*Non é posible atribuír recurso á tarefa - Os seguintes recursos non teñen suficientes horas reservadas contra proxecto.*</span><span class="sxs-lookup"><span data-stu-id="ac2fb-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="ac2fb-143">Alén diso, o membro do equipo xestor de proxecto predefinido engadido ao equipo ao crear o proxecto engádese sen ningunha reserva e non se poden atribuír a ningunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="ac2fb-144">Non se mostrará no despregable do recurso para a tarefas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="ac2fb-145">Se desexa atribuír este recurso, ten que eliminalo do equipo e, a seguir, volver a engadilo cun método de atribución que non sexa Ningún.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="ac2fb-146">O motivo de que se engada ao equipo ao crear o proxecto é para que o proxecto teña polo menos un aprobador do proxecto por defecto.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="ac2fb-147">Crear un membro do equipo xenérico a través da atribución de rol de tarefas</span><span class="sxs-lookup"><span data-stu-id="ac2fb-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="ac2fb-148">Este método garante que os recursos teñan suficientes reservas para as tarefas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="ac2fb-149">En primeiro lugar, ten que crear un marcador de posición ou recurso xenérico que describa as características do recurso denominado coas tarefas nas que desexa traballar xerando un equipo despois de atribuirde roles ás tarefas.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="ac2fb-150">Aquí atopará a forma de facelo:</span><span class="sxs-lookup"><span data-stu-id="ac2fb-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="ac2fb-151">Na estrutura de subdivisión do traballo, seleccione unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="ac2fb-152">Seleccione a icona despregable **Rol atribuído** na cela do recurso.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="ac2fb-153">Seleccione o despregable **Rol** e seleccione o rol para o recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="ac2fb-154">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ac2fb-155">![Captura de pantalla de usar WBS para engadir un recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de pantalla de usar WBS para engadir un recurso")</span><span class="sxs-lookup"><span data-stu-id="ac2fb-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="ac2fb-156">Despois de concluír a atribución de roles para as tarefas en WBS, seleccione **Xerar equipo de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="ac2fb-157">Project Service crea o mínimo número de membros do equipo xenéricos baseado nos roles, as unidades de organización de recursos e o calendario do proxecto agregando as atribucións da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ac2fb-158">![Captura de pantalla de xeración do equipo de proxecto](media/FAQ-Resources-to-Tasks2-5.png "Captura de pantalla de xeración do equipo de proxecto")</span><span class="sxs-lookup"><span data-stu-id="ac2fb-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="ac2fb-159">Na grade Membro do equipo, verá os recursos do tipo Recurso xenérico co nome de rol e posición.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="ac2fb-160">Se dous recursos necesitan un rol para concluír o traballo, a funcionalidade de Xerar equipo crea dous membros do equipo e utiliza o nome da posición para separalos.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ac2fb-161">![Captura de pantalla de engadir dous recursos xenéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de pantalla de engadir dous recursos xenéricos")</span><span class="sxs-lookup"><span data-stu-id="ac2fb-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="ac2fb-162">Pode abrir o requisito de recurso de seguranza para o membro do equipo xenérico seleccionando a ligazón en Requisitos de recurso.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ac2fb-163">![Captura de pantalla de abrir requisito de recurso de respaldo](media/FAQ-Resources-to-Tasks2-7.png "Captura de pantalla de abrir requisito de recurso de respaldo")</span><span class="sxs-lookup"><span data-stu-id="ac2fb-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="ac2fb-164">Seleccione **Reservar** para o recurso xenérico e, a seguir, pode utilizar o panel de programación para localizar e reservar un recurso real.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="ac2fb-165">Tamén pode enviar o requirimento para conclusión por un xestor de recursos seleccionando **Enviar solicitud**.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="ac2fb-166">Cando o recurso xenérico cumple cun recurso denominado, o recurso xenérico elimínase do equipo e as atribucións de tarefa para o recurso xenérico atribúense ao recurso denominado que cumplíu o requisitos de recurso do recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="ac2fb-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

