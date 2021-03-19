---
title: Cambios de xestión de recursos (Project Service Automation 3.x)
description: Este tema ofrece información sobre os cambios na área de xestión de recursos.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284761"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="a5530-103">Cambios de xestión de recursos (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="a5530-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="a5530-104">As seccións deste tema proporcionan información sobre os cambios realizados na área de xestión de recursos de Dynamics 365 Project Service Automation versión 3.x.</span><span class="sxs-lookup"><span data-stu-id="a5530-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="a5530-105">Estimacións do proxecto</span><span class="sxs-lookup"><span data-stu-id="a5530-105">Project estimates</span></span>

<span data-ttu-id="a5530-106">En vez de basearse na entidade **msdyn\_projecttask** (**Tarefa do proxecto**), as estimacións do proxecto baséanse na entidade **msdyn\_resourceassignement** (**Atribución de recursos**).</span><span class="sxs-lookup"><span data-stu-id="a5530-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="a5530-107">As atribucións de recursos convertéronse na "fonte de verdade" para a programación de tarefas e os prezos.</span><span class="sxs-lookup"><span data-stu-id="a5530-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="a5530-108">Tarefas de liña</span><span class="sxs-lookup"><span data-stu-id="a5530-108">Line tasks</span></span>

<span data-ttu-id="a5530-109">En PSA 3.x, as tarefas de liña están obsoletas (desfasadas).</span><span class="sxs-lookup"><span data-stu-id="a5530-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="a5530-110">As atribucións apuntan a toda a tarefa en lugar das tarefas de liña.</span><span class="sxs-lookup"><span data-stu-id="a5530-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="a5530-111">O seguinte exemplo mostra como unha tarefa denominada "tarefa de proba" está atribuída aos membros do equipo A e B en versións anteriores de PSA e en PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="a5530-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="a5530-112">**Antes de PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="a5530-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="a5530-113">Tarefa de proba</span><span class="sxs-lookup"><span data-stu-id="a5530-113">Test task</span></span>

        - <span data-ttu-id="a5530-114">Tarefa de proba – tarefa de liña 1</span><span class="sxs-lookup"><span data-stu-id="a5530-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="a5530-115">Atribución a A</span><span class="sxs-lookup"><span data-stu-id="a5530-115">Assignment to A</span></span>

        - <span data-ttu-id="a5530-116">Tarefa de proba – tarefa de liña 2</span><span class="sxs-lookup"><span data-stu-id="a5530-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="a5530-117">Atribución a B</span><span class="sxs-lookup"><span data-stu-id="a5530-117">Assignment to B</span></span>

- <span data-ttu-id="a5530-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="a5530-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="a5530-119">Tarefa de proba</span><span class="sxs-lookup"><span data-stu-id="a5530-119">Test task</span></span>

        - <span data-ttu-id="a5530-120">Atribución a A</span><span class="sxs-lookup"><span data-stu-id="a5530-120">Assignment to A</span></span>
        - <span data-ttu-id="a5530-121">Atribución a B</span><span class="sxs-lookup"><span data-stu-id="a5530-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="a5530-122">Atribución non atribuída</span><span class="sxs-lookup"><span data-stu-id="a5530-122">Unassigned assignment</span></span>

<span data-ttu-id="a5530-123">En PSA 3.x, unha atribución non atribuída é unha tarefa que se atribúe a un membro do equipo **NULO** e un recurso **NULO**.</span><span class="sxs-lookup"><span data-stu-id="a5530-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="a5530-124">As atribucións sen atribuír poden ocorrer nun par de escenarios:</span><span class="sxs-lookup"><span data-stu-id="a5530-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="a5530-125">Se se creou unha tarefa, pero aínda non foi atribuída a ningún membro do equipo, sempre se crea unha atribución sen atribuír.</span><span class="sxs-lookup"><span data-stu-id="a5530-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="a5530-126">Se se eliminan todos os atribuídos nunha tarefa, créase unha tarefa non atribuída para esa tarefa.</span><span class="sxs-lookup"><span data-stu-id="a5530-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="a5530-127">Campos de programación na entidade Tarefa de proxecto</span><span class="sxs-lookup"><span data-stu-id="a5530-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="a5530-128">Os campos da entidade **msdyn\_projecttask** quedaron desfasados ou movéronse á entidade **msdyn\_resourceassignment**, ou agora faise referencia a eles dende a entidade **msdyn \_projectteam** (**Membro do equipo de proxecto**).</span><span class="sxs-lookup"><span data-stu-id="a5530-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="a5530-129">Campo desfasado en en msdyn\_projecttask (Tarefa de proxecto)</span><span class="sxs-lookup"><span data-stu-id="a5530-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a5530-130">Novo campo en msdyn\_resourceassignment (Asignación de recursos)</span><span class="sxs-lookup"><span data-stu-id="a5530-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="a5530-131">Comentario</span><span class="sxs-lookup"><span data-stu-id="a5530-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="a5530-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="a5530-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="a5530-133">Ningún</span><span class="sxs-lookup"><span data-stu-id="a5530-133">None</span></span> | |
| <span data-ttu-id="a5530-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="a5530-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="a5530-135">Ningún</span><span class="sxs-lookup"><span data-stu-id="a5530-135">None</span></span> | |
| <span data-ttu-id="a5530-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="a5530-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="a5530-137">Ningún</span><span class="sxs-lookup"><span data-stu-id="a5530-137">None</span></span> | |
| <span data-ttu-id="a5530-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="a5530-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="a5530-139">Ningún</span><span class="sxs-lookup"><span data-stu-id="a5530-139">None</span></span> | |
| <span data-ttu-id="a5530-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="a5530-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="a5530-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="a5530-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="a5530-142">Cambiouse o formato da estrutura de datos de JavaScript Object Notation (JSON) que se garda no campo.</span><span class="sxs-lookup"><span data-stu-id="a5530-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="a5530-143">Contorno de programación</span><span class="sxs-lookup"><span data-stu-id="a5530-143">Schedule contour</span></span>

<span data-ttu-id="a5530-144">O contorno de programación almacénase no campo **Traballo previsto** (**msdyn\_plannedwork**) de cada entidade **Atribución de recursos** (**msdyn \_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="a5530-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="a5530-145">Estrutura</span><span class="sxs-lookup"><span data-stu-id="a5530-145">Structure</span></span>

<span data-ttu-id="a5530-146">A nova estrutura do contorno de programación consta de franxas de tempo flexibles que se definen para cada día da programación.</span><span class="sxs-lookup"><span data-stu-id="a5530-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="a5530-147">Cada porción de tempo ten as seguintes propiedades:</span><span class="sxs-lookup"><span data-stu-id="a5530-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="a5530-148">**Inicio** - O inicio do horario laboral do día, segundo o calendario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a5530-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="a5530-149">**Final** - O final do horario laboral do día, segundo o calendario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a5530-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="a5530-150">**Horas** - O número de horas asignadas no día.</span><span class="sxs-lookup"><span data-stu-id="a5530-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="a5530-151">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a5530-151">**Example**</span></span>

<span data-ttu-id="a5530-152">Este exemplo usa un calendario de proxecto onde a xornada laboral é de 9:00 a 17:00 na zona horaria UTC-8.</span><span class="sxs-lookup"><span data-stu-id="a5530-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="a5530-153">Programación automática e programación manual</span><span class="sxs-lookup"><span data-stu-id="a5530-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="a5530-154">Se unha tarefa está programada de xeito automático, as horas son de carga frontal e pode que a duración da tarefa se reduza.</span><span class="sxs-lookup"><span data-stu-id="a5530-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="a5530-155">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a5530-155">**Example**</span></span>

<span data-ttu-id="a5530-156">A seguinte tarefa está programada de xeito automático durante 18 horas ao longo de tres días (do 3 de decembro de 2018 ao 5 de decembro de 2018).</span><span class="sxs-lookup"><span data-stu-id="a5530-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="a5530-157">Se unha tarefa está programada manualmente, as horas distribúense uniformemente en todas as datas.</span><span class="sxs-lookup"><span data-stu-id="a5530-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="a5530-158">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a5530-158">**Example**</span></span>

<span data-ttu-id="a5530-159">A seguinte tarefa está programada manualmente durante 18 horas ao longo de tres días (do 3 de decembro de 2018 ao 5 de decembro de 2018).</span><span class="sxs-lookup"><span data-stu-id="a5530-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="a5530-160">Unidade de atribución</span><span class="sxs-lookup"><span data-stu-id="a5530-160">Assignment unit</span></span>

<span data-ttu-id="a5530-161">A unidade de atribución quedou desfasada en PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="a5530-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="a5530-162">As horas de esforzo da tarefa están hoxe igualmente divididas, por día, entre todos os recursos atribuídos.</span><span class="sxs-lookup"><span data-stu-id="a5530-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="a5530-163">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a5530-163">**Example**</span></span>

<span data-ttu-id="a5530-164">Neste exemplo, a tarefa está asignada a dous recursos e está programada automaticamente durante 36 horas ao longo de tres días (do 3 de decembro de 2018 ao 5 de decembro de 2018).</span><span class="sxs-lookup"><span data-stu-id="a5530-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="a5530-165">Atribución 1:</span><span class="sxs-lookup"><span data-stu-id="a5530-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="a5530-166">Atribución 2:</span><span class="sxs-lookup"><span data-stu-id="a5530-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="a5530-167">Dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="a5530-167">Pricing dimensions</span></span>

<span data-ttu-id="a5530-168">En PSA 3.x, os campos de dimensión de prezos específicos dos recursos (como **Rol** e **Unidade organizativa**) elimináronse da entidade **msdyn \_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="a5530-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="a5530-169">Estes campos pódense recuperar dende o membro do equipo de proxecto correspondente (**msdyn \_projectteam**) da asignación de recursos (**msdyn \_resourceassignment**) cando se xeran estimacións do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a5530-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="a5530-170">Un novo campo, **msdyn\_organizationalunit**, engadiuse á entidade **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="a5530-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="a5530-171">Campo desfasado en en msdyn\_projecttask (Tarefa de proxecto)</span><span class="sxs-lookup"><span data-stu-id="a5530-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a5530-172">Campo de msdyn\_projectteam (membro do equipo de proxecto) que se utiliza no seu lugar</span><span class="sxs-lookup"><span data-stu-id="a5530-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="a5530-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a5530-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="a5530-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a5530-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="a5530-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="a5530-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="a5530-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="a5530-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="a5530-177">Contornos</span><span class="sxs-lookup"><span data-stu-id="a5530-177">Contours</span></span>

<span data-ttu-id="a5530-178">Os campos de contorno de prezos e estimacións quedaron desfasadas na entidade **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="a5530-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="a5530-179">Trasladáronse á entidade **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="a5530-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="a5530-180">Campo desfasado en en msdyn\_projecttask (Tarefa de proxecto)</span><span class="sxs-lookup"><span data-stu-id="a5530-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a5530-181">Novo campo en msdyn\_resourceassignment (Asignación de recursos)</span><span class="sxs-lookup"><span data-stu-id="a5530-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="a5530-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="a5530-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="a5530-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="a5530-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="a5530-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="a5530-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="a5530-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="a5530-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="a5530-186">Engadíronse os seguintes campos á entidade **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="a5530-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="a5530-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a5530-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="a5530-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a5530-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="a5530-189">Non se modifican os seguintes campos para o custo e as vendas planificadas, reais e restantes na entidade **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="a5530-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="a5530-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a5530-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="a5530-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a5530-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="a5530-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="a5530-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="a5530-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="a5530-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="a5530-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a5530-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="a5530-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a5530-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]