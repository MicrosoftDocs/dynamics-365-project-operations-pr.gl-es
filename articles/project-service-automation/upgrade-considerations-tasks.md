---
title: Consideracións de actualización da estrutura de subdivisión do traballo
description: Este tema fornece información sobre a actualización da estrutura de subdivisión do traballo de Project Service Automation 2.x a 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751422"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="824c0-103">Consideracións de actualización da estrutura de subdivisión do traballo</span><span class="sxs-lookup"><span data-stu-id="824c0-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="824c0-104">Este tema fornece información sobre a actualización da estrutura de subdivisión do traballo de Project Service Automation 2.x a 3.x.</span><span class="sxs-lookup"><span data-stu-id="824c0-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="824c0-105">Este tema define o estado saudable dun proxecto en Project Service Automation (PSA) que é necesario para unha actualización con éxito.</span><span class="sxs-lookup"><span data-stu-id="824c0-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="824c0-106">Tamén hai información sobre as condicións de bloqueo frecuentes que farán que a actualización falle.</span><span class="sxs-lookup"><span data-stu-id="824c0-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="824c0-107">Para obter máis información sobre a definición das tarefas do proxecto e as súas funcións dentro dunha programación do proxecto, consulte [Programacións de proxecto](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="824c0-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="824c0-108">Entidades clave</span><span class="sxs-lookup"><span data-stu-id="824c0-108">Key entities</span></span>
<span data-ttu-id="824c0-109">Para unha estrutura de subdivisión do traballo precisa que xa está cargada con recursos, son necesarias as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="824c0-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="824c0-110">Proxecto</span><span class="sxs-lookup"><span data-stu-id="824c0-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="824c0-111">Equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="824c0-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="824c0-112">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="824c0-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="824c0-113">Atribucións de recursos</span><span class="sxs-lookup"><span data-stu-id="824c0-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="824c0-114">Dependencia da tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="824c0-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="824c0-115">Recursos reservables</span><span class="sxs-lookup"><span data-stu-id="824c0-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="824c0-116">Para definir unha estrutura de subdivisión do traballo cargada con recursos, debe realizar os seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="824c0-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="824c0-117">Cree un novo proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-117">Create a new project.</span></span> <span data-ttu-id="824c0-118">Para obter máis información sobre como crear un novo proxecto, consulte [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="824c0-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="824c0-119">Cree unha ou varias tarefas.</span><span class="sxs-lookup"><span data-stu-id="824c0-119">Create one or more tasks.</span></span> <span data-ttu-id="824c0-120">Para obter máis información sobre como crear unha tarefa, consulte [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="824c0-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="824c0-121">Defina as dependencias de tarefas.</span><span class="sxs-lookup"><span data-stu-id="824c0-121">Define the task dependencies.</span></span> <span data-ttu-id="824c0-122">Para obter máis información, consulte [Dependencia da tarefa do proxecto](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="824c0-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="824c0-123">Atribuír membros do equipo do proxecto ao proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-123">Assign project team members to the project.</span></span> <span data-ttu-id="824c0-124">Para obter máis información, consulte [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="824c0-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="824c0-125">Atribuír membros do equipo do proxecto ás tarefas.</span><span class="sxs-lookup"><span data-stu-id="824c0-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="824c0-126">Para obter máis información, consulte [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="824c0-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="824c0-127">Relacións do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="824c0-127">Project team relationships</span></span>

<span data-ttu-id="824c0-128">Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:</span><span class="sxs-lookup"><span data-stu-id="824c0-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="824c0-129">Todos os membros do equipo do proxecto deben estar asociados a un recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="824c0-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="824c0-130">Todos os membros do equipo do proxecto deben estar asociados ao mesmo proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="824c0-131">Relacións de tarefas do proxecto</span><span class="sxs-lookup"><span data-stu-id="824c0-131">Project task relationships</span></span>
<span data-ttu-id="824c0-132">Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:</span><span class="sxs-lookup"><span data-stu-id="824c0-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="824c0-133">Todas as tarefas relacionadas deben estar asociadas ao mesmo proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="824c0-134">Cada tarefa de liña debe ter unha tarefa matriz.</span><span class="sxs-lookup"><span data-stu-id="824c0-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="824c0-135">Cada tarefa de liña debe ter un proxecto matriz.</span><span class="sxs-lookup"><span data-stu-id="824c0-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="824c0-136">Condicións válidas</span><span class="sxs-lookup"><span data-stu-id="824c0-136">Valid conditions</span></span>

- <span data-ttu-id="824c0-137">Todas as duracións das tarefas deben ser maiores ou iguais a (> =) unha hora e menos de 1.800.000 minutos (1250 días).\*</span><span class="sxs-lookup"><span data-stu-id="824c0-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="824c0-138">Todas as tarefas deben ter unha data de inicio que non sexa anterior a 2000/01/01. \*</span><span class="sxs-lookup"><span data-stu-id="824c0-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="824c0-139">Todas as tarefas deben ter unha data de inicio como máximo 17 anos desde a actualidade.\*</span><span class="sxs-lookup"><span data-stu-id="824c0-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="824c0-140">Todas as tarefas deben ter unha data de inicio anterior ou igual á data de finalización.</span><span class="sxs-lookup"><span data-stu-id="824c0-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="824c0-141">Todos os tipos de transaccións en clasificacións (gasto, material, imposto e tempo) deben ter valores para **Unidade por defecto** e **Grupo de unidades**.</span><span class="sxs-lookup"><span data-stu-id="824c0-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="824c0-142">Deben evitarse os formatos de datas con letras.</span><span class="sxs-lookup"><span data-stu-id="824c0-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="824c0-143">Posibles pasos de mitigación</span><span class="sxs-lookup"><span data-stu-id="824c0-143">Potential mitigation steps</span></span>
- <span data-ttu-id="824c0-144">Use Localización avanzada para identificar tarefas de proxecto que non conteñen un ID de proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="824c0-145">Use Localización avanzada para identificar as tarefas do proxecto onde a duración programada é maior que > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="824c0-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="824c0-146">Antes de facer calquera cambio de datos, debe investigar as personalizacións asociadas á entidade que puideron dar lugar a obter os datos en mal estado.</span><span class="sxs-lookup"><span data-stu-id="824c0-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="824c0-147">Estas personalizacións deben abordarse antes de continuar con actualizacións relacionadas cos datos.</span><span class="sxs-lookup"><span data-stu-id="824c0-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="824c0-148">Para as tarefas identificadas que quedaron orfas, considere eliminar estas tarefas se non son necesarias ou se deben asociarse ao proxecto principal correcto.</span><span class="sxs-lookup"><span data-stu-id="824c0-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="824c0-149">Para calquera tarefa onde a duración sexa superior a 1250 días, considere a posibilidade de engadir varias tarefas para representar a duración total, se é viable.</span><span class="sxs-lookup"><span data-stu-id="824c0-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="824c0-150">Os elementos sinalados cun asterisco (\*) teñen límites debido a que a xestión de relacións cos clientes (CRM) só admite 7320 expansións de recorrencia.</span><span class="sxs-lookup"><span data-stu-id="824c0-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="824c0-151">Debe manterse por debaixo deste límite.</span><span class="sxs-lookup"><span data-stu-id="824c0-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="824c0-152">Relacións de atribución de recursos</span><span class="sxs-lookup"><span data-stu-id="824c0-152">Resource Assignment relationships</span></span>
<span data-ttu-id="824c0-153">Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:</span><span class="sxs-lookup"><span data-stu-id="824c0-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="824c0-154">Todas as atribucións de recursos nunha estrutura de subdivisión do traballo deben estar relacionadas co mesmo proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="824c0-155">Todas as atribucións de recursos nunha estrutura de subdivisión do traballo deben estar asociadas a membros do equipo de proxecto no mesmo proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="824c0-156">Posibles pasos de mitigación</span><span class="sxs-lookup"><span data-stu-id="824c0-156">Potential mitigation steps</span></span>
- <span data-ttu-id="824c0-157">Identifique todas as tarefas que quedan fóra das condicións descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="824c0-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="824c0-158">Deberanse eliminar todas as atribucións de recursos que xa non sexan válidas.</span><span class="sxs-lookup"><span data-stu-id="824c0-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="824c0-159">Relacións de dependencia de tarefas do proxecto</span><span class="sxs-lookup"><span data-stu-id="824c0-159">Project task dependency relationships</span></span>
<span data-ttu-id="824c0-160">Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:</span><span class="sxs-lookup"><span data-stu-id="824c0-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="824c0-161">Todas as dependencias das tarefas do proxecto deben estar relacionadas co mesmo proxecto.</span><span class="sxs-lookup"><span data-stu-id="824c0-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="824c0-162">Unha tarefa non pode facer referencia á mesma dependencia máis dunha vez.</span><span class="sxs-lookup"><span data-stu-id="824c0-162">A task can't have the same dependency referenced more than once.</span></span>
