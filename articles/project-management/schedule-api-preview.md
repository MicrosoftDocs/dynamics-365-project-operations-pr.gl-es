---
title: Usar as API de programación para realizar operacións con entidades de programación.
description: Este tema ofrece información e mostras para usar as API de programación.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950802"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="f2781-103">Usar as API de programación para realizar operacións con entidades de programación.</span><span class="sxs-lookup"><span data-stu-id="f2781-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="f2781-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="f2781-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f2781-105">Unha parte ou toda a funcionalidade sinalada neste tema está dispoñible como parte dunha versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="f2781-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="f2781-106">O contido e a funcionalidade están suxeitos a cambios.</span><span class="sxs-lookup"><span data-stu-id="f2781-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="f2781-107">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="f2781-107">Scheduling entities</span></span>

<span data-ttu-id="f2781-108">As API de programación ofrecen a capacidade de realizar, actualizar e eliminar operacións con **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="f2781-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="f2781-109">Estas entidades xestiónanse a través do motor de programación en Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="f2781-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="f2781-110">Crear, actualizar e eliminar operacións con **Entidades de programación** estaban restrinxidos en versións anteriores de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f2781-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="f2781-111">A seguinte táboa ofrece unha lista completa das **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="f2781-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="f2781-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="f2781-112">Entity name</span></span>  | <span data-ttu-id="f2781-113">Nome lóxico da entidade</span><span class="sxs-lookup"><span data-stu-id="f2781-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="f2781-114">Project</span><span class="sxs-lookup"><span data-stu-id="f2781-114">Project</span></span> | <span data-ttu-id="f2781-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f2781-115">msdyn_project</span></span> |
| <span data-ttu-id="f2781-116">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-116">Project Task</span></span>  | <span data-ttu-id="f2781-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="f2781-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="f2781-118">Dependencia da tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-118">Project Task Dependency</span></span>  | <span data-ttu-id="f2781-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="f2781-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="f2781-120">Atribución do recurso</span><span class="sxs-lookup"><span data-stu-id="f2781-120">Resource Assignment</span></span> | <span data-ttu-id="f2781-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="f2781-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="f2781-122">Depósito do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-122">Project Bucket</span></span>  | <span data-ttu-id="f2781-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="f2781-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="f2781-124">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-124">Project Team Member</span></span> | <span data-ttu-id="f2781-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="f2781-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="f2781-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="f2781-126">OperationSet</span></span>

<span data-ttu-id="f2781-127">OperationSet é un patrón de unidade de traballo que se pode empregar cando se deben procesar varias solicitudes que afectan á programación dentro dunha transacción.</span><span class="sxs-lookup"><span data-stu-id="f2781-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="f2781-128">API de programación</span><span class="sxs-lookup"><span data-stu-id="f2781-128">Schedule APIs</span></span>

<span data-ttu-id="f2781-129">A continuación móstrase unha lista das API de programación actuais.</span><span class="sxs-lookup"><span data-stu-id="f2781-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="f2781-130">**msdyn_CreateProjectV1**: Esta API pódese usar para crear un proxecto.</span><span class="sxs-lookup"><span data-stu-id="f2781-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="f2781-131">O proxecto e o depósito por defecto do proxecto créanse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f2781-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="f2781-132">**msdyn_CreateTeamMemberV1**: Esta API pódese usar para crear un membro do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="f2781-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="f2781-133">O rexistro de membro do equipo créase inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f2781-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="f2781-134">**msdyn_CreateOperationSetV1**: Esta API pode usarse para programar varias solicitudes que deben realizarse dentro dunha transacción.</span><span class="sxs-lookup"><span data-stu-id="f2781-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="f2781-135">**msdyn_PSSCreateV1**: Esta API pódese usar para crear unha entidade.</span><span class="sxs-lookup"><span data-stu-id="f2781-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="f2781-136">A entidade pode ser calquera das entidades de programación que admitan a operación de creación.</span><span class="sxs-lookup"><span data-stu-id="f2781-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="f2781-137">**msdyn_PSSUpdateV1**: Esta API pódese usar para actualizar unha entidade.</span><span class="sxs-lookup"><span data-stu-id="f2781-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="f2781-138">A entidade pode ser calquera das entidades de programación que admitan a operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="f2781-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="f2781-139">**msdyn_PSSDeleteV1**: Esta API pódese usar para eliminar unha entidade.</span><span class="sxs-lookup"><span data-stu-id="f2781-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="f2781-140">A entidade pode ser calquera das entidades de programación que admitan a operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="f2781-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="f2781-141">**msdyn_ExecuteOperationSetV1**: Esta API úsase para executar todas as operacións dentro do conxunto de operacións determinado.</span><span class="sxs-lookup"><span data-stu-id="f2781-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="f2781-142">Uso das API de programación con OperationSet</span><span class="sxs-lookup"><span data-stu-id="f2781-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="f2781-143">Como os rexistros con **CreateProjectV1** e **CreateTeamMemberV1** créanse inmediatamente, estas API non se poden empregar en **OperationSet** directamente.</span><span class="sxs-lookup"><span data-stu-id="f2781-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="f2781-144">Non obstante, pode usar a API para crear rexistros necesarios, crear un **OperationSet** e, a seguir, usar estes rexistros creados previamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f2781-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="f2781-145">Operacións compatibles</span><span class="sxs-lookup"><span data-stu-id="f2781-145">Supported operations</span></span>

| <span data-ttu-id="f2781-146">Entidade de programación</span><span class="sxs-lookup"><span data-stu-id="f2781-146">Scheduling entity</span></span> | <span data-ttu-id="f2781-147">Crear</span><span class="sxs-lookup"><span data-stu-id="f2781-147">Create</span></span> | <span data-ttu-id="f2781-148">Actualización</span><span class="sxs-lookup"><span data-stu-id="f2781-148">Update</span></span> | <span data-ttu-id="f2781-149">SUPR</span><span class="sxs-lookup"><span data-stu-id="f2781-149">Delete</span></span> | <span data-ttu-id="f2781-150">Consideracións importantes</span><span class="sxs-lookup"><span data-stu-id="f2781-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="f2781-151">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-151">Project task</span></span> | <span data-ttu-id="f2781-152">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-152">Yes</span></span> | <span data-ttu-id="f2781-153">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-153">Yes</span></span> | <span data-ttu-id="f2781-154">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-154">Yes</span></span> | <span data-ttu-id="f2781-155">Nada</span><span class="sxs-lookup"><span data-stu-id="f2781-155">None</span></span> |
| <span data-ttu-id="f2781-156">Dependencia da tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-156">Project task dependency</span></span> | <span data-ttu-id="f2781-157">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-157">Yes</span></span> | <span data-ttu-id="f2781-158">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-158">Yes</span></span> | | <span data-ttu-id="f2781-159">Os rexistros de dependencia de tarefas do proxecto non se actualizan.</span><span class="sxs-lookup"><span data-stu-id="f2781-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="f2781-160">Pola contra, pódese eliminar un rexistro antigo e pódese crear un novo rexistro.</span><span class="sxs-lookup"><span data-stu-id="f2781-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f2781-161">Atribución do recurso</span><span class="sxs-lookup"><span data-stu-id="f2781-161">Resource assignment</span></span> | <span data-ttu-id="f2781-162">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-162">Yes</span></span> | <span data-ttu-id="f2781-163">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-163">Yes</span></span> | | <span data-ttu-id="f2781-164">Non se admiten operacións cos seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="f2781-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="f2781-165">Os rexistros de atribución de recursos non se actualizan.</span><span class="sxs-lookup"><span data-stu-id="f2781-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="f2781-166">Pola contra, pódese eliminar o rexistro antigo e pódese crear un novo rexistro.</span><span class="sxs-lookup"><span data-stu-id="f2781-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f2781-167">Depósito do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-167">Project bucket</span></span> | <span data-ttu-id="f2781-168">N/D</span><span class="sxs-lookup"><span data-stu-id="f2781-168">N/A</span></span> | <span data-ttu-id="f2781-169">N/D</span><span class="sxs-lookup"><span data-stu-id="f2781-169">N/A</span></span> | <span data-ttu-id="f2781-170">N/D</span><span class="sxs-lookup"><span data-stu-id="f2781-170">N/A</span></span> | <span data-ttu-id="f2781-171">O depósito predefinido créase usando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="f2781-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="f2781-172">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-172">Project team member</span></span> | <span data-ttu-id="f2781-173">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-173">Yes</span></span> | <span data-ttu-id="f2781-174">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-174">Yes</span></span> | <span data-ttu-id="f2781-175">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-175">Yes</span></span> | <span data-ttu-id="f2781-176">Para a operación de creación, use a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="f2781-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="f2781-177">Project</span><span class="sxs-lookup"><span data-stu-id="f2781-177">Project</span></span> | <span data-ttu-id="f2781-178">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-178">Yes</span></span> | <span data-ttu-id="f2781-179">Si</span><span class="sxs-lookup"><span data-stu-id="f2781-179">Yes</span></span> | <span data-ttu-id="f2781-180">N/D</span><span class="sxs-lookup"><span data-stu-id="f2781-180">N/A</span></span> | <span data-ttu-id="f2781-181">Non se admiten operacións cos seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="f2781-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="f2781-182">Estas API pódense chamar con obxectos de entidade que inclúen campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="f2781-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="f2781-183">A propiedade de ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="f2781-183">The ID property is optional.</span></span> <span data-ttu-id="f2781-184">Se se proporciona, o sistema tenta usala e lanza unha excepción se non se pode usar.</span><span class="sxs-lookup"><span data-stu-id="f2781-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="f2781-185">Se non se proporciona, o sistema xeraraa.</span><span class="sxs-lookup"><span data-stu-id="f2781-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="f2781-186">Campos restrinxidos</span><span class="sxs-lookup"><span data-stu-id="f2781-186">Restricted fields</span></span>

<span data-ttu-id="f2781-187">As táboas seguintes definen os campos que están restrinxidos de **Crear** e **Editar.**</span><span class="sxs-lookup"><span data-stu-id="f2781-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="f2781-188">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-188">Project task</span></span>

| <span data-ttu-id="f2781-189">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="f2781-189">**Logical name**</span></span>                       | <span data-ttu-id="f2781-190">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="f2781-190">**Can create**</span></span> | <span data-ttu-id="f2781-191">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="f2781-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="f2781-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="f2781-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="f2781-193">non</span><span class="sxs-lookup"><span data-stu-id="f2781-193">no</span></span>             | <span data-ttu-id="f2781-194">non</span><span class="sxs-lookup"><span data-stu-id="f2781-194">no</span></span>               |
| <span data-ttu-id="f2781-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="f2781-196">non</span><span class="sxs-lookup"><span data-stu-id="f2781-196">no</span></span>             | <span data-ttu-id="f2781-197">non</span><span class="sxs-lookup"><span data-stu-id="f2781-197">no</span></span>               |
| <span data-ttu-id="f2781-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="f2781-198">msdyn_actualend</span></span>                        | <span data-ttu-id="f2781-199">non</span><span class="sxs-lookup"><span data-stu-id="f2781-199">no</span></span>             | <span data-ttu-id="f2781-200">non</span><span class="sxs-lookup"><span data-stu-id="f2781-200">no</span></span>               |
| <span data-ttu-id="f2781-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f2781-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="f2781-202">non</span><span class="sxs-lookup"><span data-stu-id="f2781-202">no</span></span>             | <span data-ttu-id="f2781-203">non</span><span class="sxs-lookup"><span data-stu-id="f2781-203">no</span></span>               |
| <span data-ttu-id="f2781-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f2781-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f2781-205">non</span><span class="sxs-lookup"><span data-stu-id="f2781-205">no</span></span>             | <span data-ttu-id="f2781-206">non</span><span class="sxs-lookup"><span data-stu-id="f2781-206">no</span></span>               |
| <span data-ttu-id="f2781-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="f2781-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="f2781-208">non</span><span class="sxs-lookup"><span data-stu-id="f2781-208">no</span></span>             | <span data-ttu-id="f2781-209">non</span><span class="sxs-lookup"><span data-stu-id="f2781-209">no</span></span>               |
| <span data-ttu-id="f2781-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="f2781-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="f2781-211">non</span><span class="sxs-lookup"><span data-stu-id="f2781-211">no</span></span>             | <span data-ttu-id="f2781-212">non</span><span class="sxs-lookup"><span data-stu-id="f2781-212">no</span></span>               |
| <span data-ttu-id="f2781-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="f2781-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="f2781-214">non</span><span class="sxs-lookup"><span data-stu-id="f2781-214">no</span></span>             | <span data-ttu-id="f2781-215">non</span><span class="sxs-lookup"><span data-stu-id="f2781-215">no</span></span>               |
| <span data-ttu-id="f2781-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f2781-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="f2781-217">non</span><span class="sxs-lookup"><span data-stu-id="f2781-217">no</span></span>             | <span data-ttu-id="f2781-218">non</span><span class="sxs-lookup"><span data-stu-id="f2781-218">no</span></span>               |
| <span data-ttu-id="f2781-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f2781-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f2781-220">non</span><span class="sxs-lookup"><span data-stu-id="f2781-220">no</span></span>             | <span data-ttu-id="f2781-221">non</span><span class="sxs-lookup"><span data-stu-id="f2781-221">no</span></span>               |
| <span data-ttu-id="f2781-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f2781-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="f2781-223">non</span><span class="sxs-lookup"><span data-stu-id="f2781-223">no</span></span>             | <span data-ttu-id="f2781-224">non</span><span class="sxs-lookup"><span data-stu-id="f2781-224">no</span></span>               |
| <span data-ttu-id="f2781-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="f2781-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="f2781-226">non</span><span class="sxs-lookup"><span data-stu-id="f2781-226">no</span></span>             | <span data-ttu-id="f2781-227">non</span><span class="sxs-lookup"><span data-stu-id="f2781-227">no</span></span>               |
| <span data-ttu-id="f2781-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="f2781-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="f2781-229">non</span><span class="sxs-lookup"><span data-stu-id="f2781-229">no</span></span>             | <span data-ttu-id="f2781-230">non</span><span class="sxs-lookup"><span data-stu-id="f2781-230">no</span></span>               |
| <span data-ttu-id="f2781-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="f2781-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="f2781-232">non</span><span class="sxs-lookup"><span data-stu-id="f2781-232">no</span></span>             | <span data-ttu-id="f2781-233">non</span><span class="sxs-lookup"><span data-stu-id="f2781-233">no</span></span>               |
| <span data-ttu-id="f2781-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="f2781-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="f2781-235">non</span><span class="sxs-lookup"><span data-stu-id="f2781-235">no</span></span>             | <span data-ttu-id="f2781-236">non</span><span class="sxs-lookup"><span data-stu-id="f2781-236">no</span></span>               |
| <span data-ttu-id="f2781-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="f2781-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="f2781-238">non</span><span class="sxs-lookup"><span data-stu-id="f2781-238">no</span></span>             | <span data-ttu-id="f2781-239">non</span><span class="sxs-lookup"><span data-stu-id="f2781-239">no</span></span>               |
| <span data-ttu-id="f2781-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="f2781-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="f2781-241">non</span><span class="sxs-lookup"><span data-stu-id="f2781-241">no</span></span>             | <span data-ttu-id="f2781-242">non</span><span class="sxs-lookup"><span data-stu-id="f2781-242">no</span></span>               |
| <span data-ttu-id="f2781-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="f2781-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="f2781-244">non</span><span class="sxs-lookup"><span data-stu-id="f2781-244">no</span></span>             | <span data-ttu-id="f2781-245">non</span><span class="sxs-lookup"><span data-stu-id="f2781-245">no</span></span>               |
| <span data-ttu-id="f2781-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="f2781-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="f2781-247">non</span><span class="sxs-lookup"><span data-stu-id="f2781-247">no</span></span>             | <span data-ttu-id="f2781-248">non</span><span class="sxs-lookup"><span data-stu-id="f2781-248">no</span></span>               |
| <span data-ttu-id="f2781-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f2781-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="f2781-250">non</span><span class="sxs-lookup"><span data-stu-id="f2781-250">no</span></span>             | <span data-ttu-id="f2781-251">non</span><span class="sxs-lookup"><span data-stu-id="f2781-251">no</span></span>               |
| <span data-ttu-id="f2781-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f2781-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="f2781-253">non</span><span class="sxs-lookup"><span data-stu-id="f2781-253">no</span></span>             | <span data-ttu-id="f2781-254">non</span><span class="sxs-lookup"><span data-stu-id="f2781-254">no</span></span>               |
| <span data-ttu-id="f2781-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="f2781-256">non</span><span class="sxs-lookup"><span data-stu-id="f2781-256">no</span></span>             | <span data-ttu-id="f2781-257">non</span><span class="sxs-lookup"><span data-stu-id="f2781-257">no</span></span>               |
| <span data-ttu-id="f2781-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f2781-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f2781-259">non</span><span class="sxs-lookup"><span data-stu-id="f2781-259">no</span></span>             | <span data-ttu-id="f2781-260">non</span><span class="sxs-lookup"><span data-stu-id="f2781-260">no</span></span>               |
| <span data-ttu-id="f2781-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f2781-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f2781-262">non</span><span class="sxs-lookup"><span data-stu-id="f2781-262">no</span></span>             | <span data-ttu-id="f2781-263">non</span><span class="sxs-lookup"><span data-stu-id="f2781-263">no</span></span>               |
| <span data-ttu-id="f2781-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="f2781-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="f2781-265">non</span><span class="sxs-lookup"><span data-stu-id="f2781-265">no</span></span>             | <span data-ttu-id="f2781-266">non</span><span class="sxs-lookup"><span data-stu-id="f2781-266">no</span></span>               |
| <span data-ttu-id="f2781-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f2781-267">msdyn_progress</span></span>                         | <span data-ttu-id="f2781-268">non</span><span class="sxs-lookup"><span data-stu-id="f2781-268">no</span></span>             | <span data-ttu-id="f2781-269">non (si para P4W)</span><span class="sxs-lookup"><span data-stu-id="f2781-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="f2781-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f2781-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f2781-271">non</span><span class="sxs-lookup"><span data-stu-id="f2781-271">no</span></span>             | <span data-ttu-id="f2781-272">non</span><span class="sxs-lookup"><span data-stu-id="f2781-272">no</span></span>               |
| <span data-ttu-id="f2781-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f2781-274">non</span><span class="sxs-lookup"><span data-stu-id="f2781-274">no</span></span>             | <span data-ttu-id="f2781-275">non</span><span class="sxs-lookup"><span data-stu-id="f2781-275">no</span></span>               |
| <span data-ttu-id="f2781-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f2781-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f2781-277">non</span><span class="sxs-lookup"><span data-stu-id="f2781-277">no</span></span>             | <span data-ttu-id="f2781-278">non</span><span class="sxs-lookup"><span data-stu-id="f2781-278">no</span></span>               |
| <span data-ttu-id="f2781-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f2781-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f2781-280">non</span><span class="sxs-lookup"><span data-stu-id="f2781-280">no</span></span>             | <span data-ttu-id="f2781-281">non</span><span class="sxs-lookup"><span data-stu-id="f2781-281">no</span></span>               |
| <span data-ttu-id="f2781-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="f2781-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="f2781-283">non</span><span class="sxs-lookup"><span data-stu-id="f2781-283">no</span></span>             | <span data-ttu-id="f2781-284">non</span><span class="sxs-lookup"><span data-stu-id="f2781-284">no</span></span>               |
| <span data-ttu-id="f2781-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="f2781-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="f2781-286">non</span><span class="sxs-lookup"><span data-stu-id="f2781-286">no</span></span>             | <span data-ttu-id="f2781-287">non</span><span class="sxs-lookup"><span data-stu-id="f2781-287">no</span></span>               |
| <span data-ttu-id="f2781-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="f2781-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="f2781-289">non</span><span class="sxs-lookup"><span data-stu-id="f2781-289">no</span></span>             | <span data-ttu-id="f2781-290">non</span><span class="sxs-lookup"><span data-stu-id="f2781-290">no</span></span>               |
| <span data-ttu-id="f2781-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f2781-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="f2781-292">non</span><span class="sxs-lookup"><span data-stu-id="f2781-292">no</span></span>             | <span data-ttu-id="f2781-293">non</span><span class="sxs-lookup"><span data-stu-id="f2781-293">no</span></span>               |
| <span data-ttu-id="f2781-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f2781-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="f2781-295">non</span><span class="sxs-lookup"><span data-stu-id="f2781-295">no</span></span>             | <span data-ttu-id="f2781-296">non</span><span class="sxs-lookup"><span data-stu-id="f2781-296">no</span></span>               |
| <span data-ttu-id="f2781-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f2781-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="f2781-298">non</span><span class="sxs-lookup"><span data-stu-id="f2781-298">no</span></span>             | <span data-ttu-id="f2781-299">non</span><span class="sxs-lookup"><span data-stu-id="f2781-299">no</span></span>               |
| <span data-ttu-id="f2781-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f2781-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="f2781-301">non</span><span class="sxs-lookup"><span data-stu-id="f2781-301">no</span></span>             | <span data-ttu-id="f2781-302">non</span><span class="sxs-lookup"><span data-stu-id="f2781-302">no</span></span>               |
| <span data-ttu-id="f2781-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f2781-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="f2781-304">non</span><span class="sxs-lookup"><span data-stu-id="f2781-304">no</span></span>             | <span data-ttu-id="f2781-305">non</span><span class="sxs-lookup"><span data-stu-id="f2781-305">no</span></span>               |
| <span data-ttu-id="f2781-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f2781-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f2781-307">non</span><span class="sxs-lookup"><span data-stu-id="f2781-307">no</span></span>             | <span data-ttu-id="f2781-308">non</span><span class="sxs-lookup"><span data-stu-id="f2781-308">no</span></span>               |
| <span data-ttu-id="f2781-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f2781-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f2781-310">non</span><span class="sxs-lookup"><span data-stu-id="f2781-310">no</span></span>             | <span data-ttu-id="f2781-311">non</span><span class="sxs-lookup"><span data-stu-id="f2781-311">no</span></span>               |
| <span data-ttu-id="f2781-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="f2781-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="f2781-313">non</span><span class="sxs-lookup"><span data-stu-id="f2781-313">no</span></span>             | <span data-ttu-id="f2781-314">non</span><span class="sxs-lookup"><span data-stu-id="f2781-314">no</span></span>               |
| <span data-ttu-id="f2781-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="f2781-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="f2781-316">non</span><span class="sxs-lookup"><span data-stu-id="f2781-316">no</span></span>             | <span data-ttu-id="f2781-317">non</span><span class="sxs-lookup"><span data-stu-id="f2781-317">no</span></span>               |
| <span data-ttu-id="f2781-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="f2781-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="f2781-319">non</span><span class="sxs-lookup"><span data-stu-id="f2781-319">no</span></span>             | <span data-ttu-id="f2781-320">non</span><span class="sxs-lookup"><span data-stu-id="f2781-320">no</span></span>               |
| <span data-ttu-id="f2781-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f2781-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f2781-322">non</span><span class="sxs-lookup"><span data-stu-id="f2781-322">no</span></span>             | <span data-ttu-id="f2781-323">non</span><span class="sxs-lookup"><span data-stu-id="f2781-323">no</span></span>               |
| <span data-ttu-id="f2781-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="f2781-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="f2781-325">non</span><span class="sxs-lookup"><span data-stu-id="f2781-325">no</span></span>             | <span data-ttu-id="f2781-326">non</span><span class="sxs-lookup"><span data-stu-id="f2781-326">no</span></span>               |
| <span data-ttu-id="f2781-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="f2781-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="f2781-328">non</span><span class="sxs-lookup"><span data-stu-id="f2781-328">no</span></span>             | <span data-ttu-id="f2781-329">non</span><span class="sxs-lookup"><span data-stu-id="f2781-329">no</span></span>               |
| <span data-ttu-id="f2781-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="f2781-330">msdyn_summary</span></span>                          | <span data-ttu-id="f2781-331">non</span><span class="sxs-lookup"><span data-stu-id="f2781-331">no</span></span>             | <span data-ttu-id="f2781-332">non</span><span class="sxs-lookup"><span data-stu-id="f2781-332">no</span></span>               |
| <span data-ttu-id="f2781-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="f2781-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="f2781-334">non</span><span class="sxs-lookup"><span data-stu-id="f2781-334">no</span></span>             | <span data-ttu-id="f2781-335">non</span><span class="sxs-lookup"><span data-stu-id="f2781-335">no</span></span>               |
| <span data-ttu-id="f2781-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="f2781-337">non</span><span class="sxs-lookup"><span data-stu-id="f2781-337">no</span></span>             | <span data-ttu-id="f2781-338">non</span><span class="sxs-lookup"><span data-stu-id="f2781-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="f2781-339">Dependencia da tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-339">Project task dependency</span></span>

| <span data-ttu-id="f2781-340">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="f2781-340">**Logical name**</span></span>              | <span data-ttu-id="f2781-341">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="f2781-341">**Can create**</span></span> | <span data-ttu-id="f2781-342">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="f2781-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="f2781-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="f2781-343">msdyn_linktype</span></span>                | <span data-ttu-id="f2781-344">non</span><span class="sxs-lookup"><span data-stu-id="f2781-344">no</span></span>             | <span data-ttu-id="f2781-345">non</span><span class="sxs-lookup"><span data-stu-id="f2781-345">no</span></span>           |
| <span data-ttu-id="f2781-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="f2781-346">msdyn_linktypename</span></span>            | <span data-ttu-id="f2781-347">non</span><span class="sxs-lookup"><span data-stu-id="f2781-347">no</span></span>             | <span data-ttu-id="f2781-348">non</span><span class="sxs-lookup"><span data-stu-id="f2781-348">no</span></span>           |
| <span data-ttu-id="f2781-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="f2781-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="f2781-350">si</span><span class="sxs-lookup"><span data-stu-id="f2781-350">yes</span></span>            | <span data-ttu-id="f2781-351">non</span><span class="sxs-lookup"><span data-stu-id="f2781-351">no</span></span>           |
| <span data-ttu-id="f2781-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="f2781-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="f2781-353">si</span><span class="sxs-lookup"><span data-stu-id="f2781-353">yes</span></span>            | <span data-ttu-id="f2781-354">non</span><span class="sxs-lookup"><span data-stu-id="f2781-354">no</span></span>           |
| <span data-ttu-id="f2781-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f2781-355">msdyn_project</span></span>                 | <span data-ttu-id="f2781-356">si</span><span class="sxs-lookup"><span data-stu-id="f2781-356">yes</span></span>            | <span data-ttu-id="f2781-357">non</span><span class="sxs-lookup"><span data-stu-id="f2781-357">no</span></span>           |
| <span data-ttu-id="f2781-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="f2781-358">msdyn_projectname</span></span>             | <span data-ttu-id="f2781-359">si</span><span class="sxs-lookup"><span data-stu-id="f2781-359">yes</span></span>            | <span data-ttu-id="f2781-360">non</span><span class="sxs-lookup"><span data-stu-id="f2781-360">no</span></span>           |
| <span data-ttu-id="f2781-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="f2781-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="f2781-362">si</span><span class="sxs-lookup"><span data-stu-id="f2781-362">yes</span></span>            | <span data-ttu-id="f2781-363">non</span><span class="sxs-lookup"><span data-stu-id="f2781-363">no</span></span>           |
| <span data-ttu-id="f2781-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="f2781-364">msdyn_successortask</span></span>           | <span data-ttu-id="f2781-365">si</span><span class="sxs-lookup"><span data-stu-id="f2781-365">yes</span></span>            | <span data-ttu-id="f2781-366">non</span><span class="sxs-lookup"><span data-stu-id="f2781-366">no</span></span>           |
| <span data-ttu-id="f2781-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="f2781-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="f2781-368">si</span><span class="sxs-lookup"><span data-stu-id="f2781-368">yes</span></span>            | <span data-ttu-id="f2781-369">non</span><span class="sxs-lookup"><span data-stu-id="f2781-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="f2781-370">Atribución do recurso</span><span class="sxs-lookup"><span data-stu-id="f2781-370">Resource assignment</span></span>

| <span data-ttu-id="f2781-371">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="f2781-371">**Logical name**</span></span>             | <span data-ttu-id="f2781-372">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="f2781-372">**Can create**</span></span> | <span data-ttu-id="f2781-373">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="f2781-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="f2781-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="f2781-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="f2781-375">si</span><span class="sxs-lookup"><span data-stu-id="f2781-375">yes</span></span>            | <span data-ttu-id="f2781-376">non</span><span class="sxs-lookup"><span data-stu-id="f2781-376">no</span></span>           |
| <span data-ttu-id="f2781-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="f2781-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="f2781-378">si</span><span class="sxs-lookup"><span data-stu-id="f2781-378">yes</span></span>            | <span data-ttu-id="f2781-379">non</span><span class="sxs-lookup"><span data-stu-id="f2781-379">no</span></span>           |
| <span data-ttu-id="f2781-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="f2781-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="f2781-381">non</span><span class="sxs-lookup"><span data-stu-id="f2781-381">no</span></span>             | <span data-ttu-id="f2781-382">non</span><span class="sxs-lookup"><span data-stu-id="f2781-382">no</span></span>           |
| <span data-ttu-id="f2781-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="f2781-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="f2781-384">non</span><span class="sxs-lookup"><span data-stu-id="f2781-384">no</span></span>             | <span data-ttu-id="f2781-385">non</span><span class="sxs-lookup"><span data-stu-id="f2781-385">no</span></span>           |
| <span data-ttu-id="f2781-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="f2781-386">msdyn_committype</span></span>             | <span data-ttu-id="f2781-387">non</span><span class="sxs-lookup"><span data-stu-id="f2781-387">no</span></span>             | <span data-ttu-id="f2781-388">non</span><span class="sxs-lookup"><span data-stu-id="f2781-388">no</span></span>           |
| <span data-ttu-id="f2781-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="f2781-389">msdyn_committypename</span></span>         | <span data-ttu-id="f2781-390">non</span><span class="sxs-lookup"><span data-stu-id="f2781-390">no</span></span>             | <span data-ttu-id="f2781-391">non</span><span class="sxs-lookup"><span data-stu-id="f2781-391">no</span></span>           |
| <span data-ttu-id="f2781-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f2781-392">msdyn_effort</span></span>                 | <span data-ttu-id="f2781-393">non</span><span class="sxs-lookup"><span data-stu-id="f2781-393">no</span></span>             | <span data-ttu-id="f2781-394">non</span><span class="sxs-lookup"><span data-stu-id="f2781-394">no</span></span>           |
| <span data-ttu-id="f2781-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f2781-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="f2781-396">non</span><span class="sxs-lookup"><span data-stu-id="f2781-396">no</span></span>             | <span data-ttu-id="f2781-397">non</span><span class="sxs-lookup"><span data-stu-id="f2781-397">no</span></span>           |
| <span data-ttu-id="f2781-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f2781-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="f2781-399">non</span><span class="sxs-lookup"><span data-stu-id="f2781-399">no</span></span>             | <span data-ttu-id="f2781-400">non</span><span class="sxs-lookup"><span data-stu-id="f2781-400">no</span></span>           |
| <span data-ttu-id="f2781-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f2781-401">msdyn_finish</span></span>                 | <span data-ttu-id="f2781-402">non</span><span class="sxs-lookup"><span data-stu-id="f2781-402">no</span></span>             | <span data-ttu-id="f2781-403">non</span><span class="sxs-lookup"><span data-stu-id="f2781-403">no</span></span>           |
| <span data-ttu-id="f2781-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f2781-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="f2781-405">non</span><span class="sxs-lookup"><span data-stu-id="f2781-405">no</span></span>             | <span data-ttu-id="f2781-406">non</span><span class="sxs-lookup"><span data-stu-id="f2781-406">no</span></span>           |
| <span data-ttu-id="f2781-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="f2781-408">non</span><span class="sxs-lookup"><span data-stu-id="f2781-408">no</span></span>             | <span data-ttu-id="f2781-409">non</span><span class="sxs-lookup"><span data-stu-id="f2781-409">no</span></span>           |
| <span data-ttu-id="f2781-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="f2781-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="f2781-411">non</span><span class="sxs-lookup"><span data-stu-id="f2781-411">no</span></span>             | <span data-ttu-id="f2781-412">non</span><span class="sxs-lookup"><span data-stu-id="f2781-412">no</span></span>           |
| <span data-ttu-id="f2781-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f2781-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="f2781-414">non</span><span class="sxs-lookup"><span data-stu-id="f2781-414">no</span></span>             | <span data-ttu-id="f2781-415">non</span><span class="sxs-lookup"><span data-stu-id="f2781-415">no</span></span>           |
| <span data-ttu-id="f2781-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f2781-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="f2781-417">non</span><span class="sxs-lookup"><span data-stu-id="f2781-417">no</span></span>             | <span data-ttu-id="f2781-418">non</span><span class="sxs-lookup"><span data-stu-id="f2781-418">no</span></span>           |
| <span data-ttu-id="f2781-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="f2781-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="f2781-420">non</span><span class="sxs-lookup"><span data-stu-id="f2781-420">no</span></span>             | <span data-ttu-id="f2781-421">non</span><span class="sxs-lookup"><span data-stu-id="f2781-421">no</span></span>           |
| <span data-ttu-id="f2781-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="f2781-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="f2781-423">non</span><span class="sxs-lookup"><span data-stu-id="f2781-423">no</span></span>             | <span data-ttu-id="f2781-424">non</span><span class="sxs-lookup"><span data-stu-id="f2781-424">no</span></span>           |
| <span data-ttu-id="f2781-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="f2781-425">msdyn_projectid</span></span>              | <span data-ttu-id="f2781-426">si</span><span class="sxs-lookup"><span data-stu-id="f2781-426">yes</span></span>            | <span data-ttu-id="f2781-427">non</span><span class="sxs-lookup"><span data-stu-id="f2781-427">no</span></span>           |
| <span data-ttu-id="f2781-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="f2781-428">msdyn_projectidname</span></span>          | <span data-ttu-id="f2781-429">non</span><span class="sxs-lookup"><span data-stu-id="f2781-429">no</span></span>             | <span data-ttu-id="f2781-430">non</span><span class="sxs-lookup"><span data-stu-id="f2781-430">no</span></span>           |
| <span data-ttu-id="f2781-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="f2781-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="f2781-432">non</span><span class="sxs-lookup"><span data-stu-id="f2781-432">no</span></span>             | <span data-ttu-id="f2781-433">non</span><span class="sxs-lookup"><span data-stu-id="f2781-433">no</span></span>           |
| <span data-ttu-id="f2781-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="f2781-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="f2781-435">non</span><span class="sxs-lookup"><span data-stu-id="f2781-435">no</span></span>             | <span data-ttu-id="f2781-436">non</span><span class="sxs-lookup"><span data-stu-id="f2781-436">no</span></span>           |
| <span data-ttu-id="f2781-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f2781-437">msdyn_start</span></span>                  | <span data-ttu-id="f2781-438">non</span><span class="sxs-lookup"><span data-stu-id="f2781-438">no</span></span>             | <span data-ttu-id="f2781-439">non</span><span class="sxs-lookup"><span data-stu-id="f2781-439">no</span></span>           |
| <span data-ttu-id="f2781-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="f2781-440">msdyn_taskid</span></span>                 | <span data-ttu-id="f2781-441">non</span><span class="sxs-lookup"><span data-stu-id="f2781-441">no</span></span>             | <span data-ttu-id="f2781-442">non</span><span class="sxs-lookup"><span data-stu-id="f2781-442">no</span></span>           |
| <span data-ttu-id="f2781-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="f2781-443">msdyn_taskidname</span></span>             | <span data-ttu-id="f2781-444">non</span><span class="sxs-lookup"><span data-stu-id="f2781-444">no</span></span>             | <span data-ttu-id="f2781-445">non</span><span class="sxs-lookup"><span data-stu-id="f2781-445">no</span></span>           |
| <span data-ttu-id="f2781-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="f2781-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="f2781-447">non</span><span class="sxs-lookup"><span data-stu-id="f2781-447">no</span></span>             | <span data-ttu-id="f2781-448">non</span><span class="sxs-lookup"><span data-stu-id="f2781-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="f2781-449">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="f2781-449">Project team member</span></span>

| <span data-ttu-id="f2781-450">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="f2781-450">**Logical name**</span></span>                                 | <span data-ttu-id="f2781-451">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="f2781-451">**Can create**</span></span> | <span data-ttu-id="f2781-452">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="f2781-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="f2781-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="f2781-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="f2781-454">non</span><span class="sxs-lookup"><span data-stu-id="f2781-454">no</span></span>             | <span data-ttu-id="f2781-455">non</span><span class="sxs-lookup"><span data-stu-id="f2781-455">no</span></span>           |
| <span data-ttu-id="f2781-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="f2781-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="f2781-457">non</span><span class="sxs-lookup"><span data-stu-id="f2781-457">no</span></span>             | <span data-ttu-id="f2781-458">non</span><span class="sxs-lookup"><span data-stu-id="f2781-458">no</span></span>           |
| <span data-ttu-id="f2781-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="f2781-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="f2781-460">non</span><span class="sxs-lookup"><span data-stu-id="f2781-460">no</span></span>             | <span data-ttu-id="f2781-461">non</span><span class="sxs-lookup"><span data-stu-id="f2781-461">no</span></span>           |
| <span data-ttu-id="f2781-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="f2781-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="f2781-463">non</span><span class="sxs-lookup"><span data-stu-id="f2781-463">no</span></span>             | <span data-ttu-id="f2781-464">non</span><span class="sxs-lookup"><span data-stu-id="f2781-464">no</span></span>           |
| <span data-ttu-id="f2781-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f2781-465">msdyn_effort</span></span>                                     | <span data-ttu-id="f2781-466">non</span><span class="sxs-lookup"><span data-stu-id="f2781-466">no</span></span>             | <span data-ttu-id="f2781-467">non</span><span class="sxs-lookup"><span data-stu-id="f2781-467">no</span></span>           |
| <span data-ttu-id="f2781-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f2781-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="f2781-469">non</span><span class="sxs-lookup"><span data-stu-id="f2781-469">no</span></span>             | <span data-ttu-id="f2781-470">non</span><span class="sxs-lookup"><span data-stu-id="f2781-470">no</span></span>           |
| <span data-ttu-id="f2781-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f2781-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="f2781-472">non</span><span class="sxs-lookup"><span data-stu-id="f2781-472">no</span></span>             | <span data-ttu-id="f2781-473">non</span><span class="sxs-lookup"><span data-stu-id="f2781-473">no</span></span>           |
| <span data-ttu-id="f2781-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f2781-474">msdyn_finish</span></span>                                     | <span data-ttu-id="f2781-475">non</span><span class="sxs-lookup"><span data-stu-id="f2781-475">no</span></span>             | <span data-ttu-id="f2781-476">non</span><span class="sxs-lookup"><span data-stu-id="f2781-476">no</span></span>           |
| <span data-ttu-id="f2781-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="f2781-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="f2781-478">non</span><span class="sxs-lookup"><span data-stu-id="f2781-478">no</span></span>             | <span data-ttu-id="f2781-479">non</span><span class="sxs-lookup"><span data-stu-id="f2781-479">no</span></span>           |
| <span data-ttu-id="f2781-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="f2781-480">msdyn_hours</span></span>                                      | <span data-ttu-id="f2781-481">non</span><span class="sxs-lookup"><span data-stu-id="f2781-481">no</span></span>             | <span data-ttu-id="f2781-482">non</span><span class="sxs-lookup"><span data-stu-id="f2781-482">no</span></span>           |
| <span data-ttu-id="f2781-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="f2781-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="f2781-484">non</span><span class="sxs-lookup"><span data-stu-id="f2781-484">no</span></span>             | <span data-ttu-id="f2781-485">non</span><span class="sxs-lookup"><span data-stu-id="f2781-485">no</span></span>           |
| <span data-ttu-id="f2781-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="f2781-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="f2781-487">non</span><span class="sxs-lookup"><span data-stu-id="f2781-487">no</span></span>             | <span data-ttu-id="f2781-488">non</span><span class="sxs-lookup"><span data-stu-id="f2781-488">no</span></span>           |
| <span data-ttu-id="f2781-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f2781-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="f2781-490">non</span><span class="sxs-lookup"><span data-stu-id="f2781-490">no</span></span>             | <span data-ttu-id="f2781-491">non</span><span class="sxs-lookup"><span data-stu-id="f2781-491">no</span></span>           |
| <span data-ttu-id="f2781-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="f2781-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="f2781-493">non</span><span class="sxs-lookup"><span data-stu-id="f2781-493">no</span></span>             | <span data-ttu-id="f2781-494">non</span><span class="sxs-lookup"><span data-stu-id="f2781-494">no</span></span>           |
| <span data-ttu-id="f2781-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="f2781-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="f2781-496">non</span><span class="sxs-lookup"><span data-stu-id="f2781-496">no</span></span>             | <span data-ttu-id="f2781-497">non</span><span class="sxs-lookup"><span data-stu-id="f2781-497">no</span></span>           |
| <span data-ttu-id="f2781-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="f2781-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="f2781-499">non</span><span class="sxs-lookup"><span data-stu-id="f2781-499">no</span></span>             | <span data-ttu-id="f2781-500">non</span><span class="sxs-lookup"><span data-stu-id="f2781-500">no</span></span>           |
| <span data-ttu-id="f2781-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f2781-501">msdyn_start</span></span>                                      | <span data-ttu-id="f2781-502">non</span><span class="sxs-lookup"><span data-stu-id="f2781-502">no</span></span>             | <span data-ttu-id="f2781-503">non</span><span class="sxs-lookup"><span data-stu-id="f2781-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="f2781-504">Project</span><span class="sxs-lookup"><span data-stu-id="f2781-504">Project</span></span>

| <span data-ttu-id="f2781-505">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="f2781-505">**Logical name**</span></span>                       | <span data-ttu-id="f2781-506">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="f2781-506">**Can create**</span></span> | <span data-ttu-id="f2781-507">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="f2781-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="f2781-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="f2781-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="f2781-509">non</span><span class="sxs-lookup"><span data-stu-id="f2781-509">no</span></span>             | <span data-ttu-id="f2781-510">non</span><span class="sxs-lookup"><span data-stu-id="f2781-510">no</span></span>           |
| <span data-ttu-id="f2781-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="f2781-512">non</span><span class="sxs-lookup"><span data-stu-id="f2781-512">no</span></span>             | <span data-ttu-id="f2781-513">non</span><span class="sxs-lookup"><span data-stu-id="f2781-513">no</span></span>           |
| <span data-ttu-id="f2781-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="f2781-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="f2781-515">non</span><span class="sxs-lookup"><span data-stu-id="f2781-515">no</span></span>             | <span data-ttu-id="f2781-516">non</span><span class="sxs-lookup"><span data-stu-id="f2781-516">no</span></span>           |
| <span data-ttu-id="f2781-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="f2781-518">non</span><span class="sxs-lookup"><span data-stu-id="f2781-518">no</span></span>             | <span data-ttu-id="f2781-519">non</span><span class="sxs-lookup"><span data-stu-id="f2781-519">no</span></span>           |
| <span data-ttu-id="f2781-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f2781-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="f2781-521">non</span><span class="sxs-lookup"><span data-stu-id="f2781-521">no</span></span>             | <span data-ttu-id="f2781-522">non</span><span class="sxs-lookup"><span data-stu-id="f2781-522">no</span></span>           |
| <span data-ttu-id="f2781-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f2781-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f2781-524">non</span><span class="sxs-lookup"><span data-stu-id="f2781-524">no</span></span>             | <span data-ttu-id="f2781-525">non</span><span class="sxs-lookup"><span data-stu-id="f2781-525">no</span></span>           |
| <span data-ttu-id="f2781-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="f2781-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="f2781-527">si</span><span class="sxs-lookup"><span data-stu-id="f2781-527">yes</span></span>            | <span data-ttu-id="f2781-528">non</span><span class="sxs-lookup"><span data-stu-id="f2781-528">no</span></span>           |
| <span data-ttu-id="f2781-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f2781-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="f2781-530">si</span><span class="sxs-lookup"><span data-stu-id="f2781-530">yes</span></span>            | <span data-ttu-id="f2781-531">non</span><span class="sxs-lookup"><span data-stu-id="f2781-531">no</span></span>           |
| <span data-ttu-id="f2781-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f2781-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="f2781-533">si</span><span class="sxs-lookup"><span data-stu-id="f2781-533">yes</span></span>            | <span data-ttu-id="f2781-534">non</span><span class="sxs-lookup"><span data-stu-id="f2781-534">no</span></span>           |
| <span data-ttu-id="f2781-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="f2781-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="f2781-536">non</span><span class="sxs-lookup"><span data-stu-id="f2781-536">no</span></span>             | <span data-ttu-id="f2781-537">non</span><span class="sxs-lookup"><span data-stu-id="f2781-537">no</span></span>           |
| <span data-ttu-id="f2781-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f2781-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="f2781-539">non</span><span class="sxs-lookup"><span data-stu-id="f2781-539">no</span></span>             | <span data-ttu-id="f2781-540">non</span><span class="sxs-lookup"><span data-stu-id="f2781-540">no</span></span>           |
| <span data-ttu-id="f2781-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f2781-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="f2781-542">non</span><span class="sxs-lookup"><span data-stu-id="f2781-542">no</span></span>             | <span data-ttu-id="f2781-543">non</span><span class="sxs-lookup"><span data-stu-id="f2781-543">no</span></span>           |
| <span data-ttu-id="f2781-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="f2781-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="f2781-545">non</span><span class="sxs-lookup"><span data-stu-id="f2781-545">no</span></span>             | <span data-ttu-id="f2781-546">non</span><span class="sxs-lookup"><span data-stu-id="f2781-546">no</span></span>           |
| <span data-ttu-id="f2781-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="f2781-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="f2781-548">non</span><span class="sxs-lookup"><span data-stu-id="f2781-548">no</span></span>             | <span data-ttu-id="f2781-549">non</span><span class="sxs-lookup"><span data-stu-id="f2781-549">no</span></span>           |
| <span data-ttu-id="f2781-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="f2781-550">msdyn_duration</span></span>                         | <span data-ttu-id="f2781-551">non</span><span class="sxs-lookup"><span data-stu-id="f2781-551">no</span></span>             | <span data-ttu-id="f2781-552">non</span><span class="sxs-lookup"><span data-stu-id="f2781-552">no</span></span>           |
| <span data-ttu-id="f2781-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f2781-553">msdyn_effort</span></span>                           | <span data-ttu-id="f2781-554">non</span><span class="sxs-lookup"><span data-stu-id="f2781-554">no</span></span>             | <span data-ttu-id="f2781-555">non</span><span class="sxs-lookup"><span data-stu-id="f2781-555">no</span></span>           |
| <span data-ttu-id="f2781-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f2781-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f2781-557">non</span><span class="sxs-lookup"><span data-stu-id="f2781-557">no</span></span>             | <span data-ttu-id="f2781-558">non</span><span class="sxs-lookup"><span data-stu-id="f2781-558">no</span></span>           |
| <span data-ttu-id="f2781-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f2781-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="f2781-560">non</span><span class="sxs-lookup"><span data-stu-id="f2781-560">no</span></span>             | <span data-ttu-id="f2781-561">non</span><span class="sxs-lookup"><span data-stu-id="f2781-561">no</span></span>           |
| <span data-ttu-id="f2781-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f2781-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="f2781-563">non</span><span class="sxs-lookup"><span data-stu-id="f2781-563">no</span></span>             | <span data-ttu-id="f2781-564">non</span><span class="sxs-lookup"><span data-stu-id="f2781-564">no</span></span>           |
| <span data-ttu-id="f2781-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f2781-565">msdyn_finish</span></span>                           | <span data-ttu-id="f2781-566">si</span><span class="sxs-lookup"><span data-stu-id="f2781-566">yes</span></span>            | <span data-ttu-id="f2781-567">si</span><span class="sxs-lookup"><span data-stu-id="f2781-567">yes</span></span>          |
| <span data-ttu-id="f2781-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="f2781-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="f2781-569">non</span><span class="sxs-lookup"><span data-stu-id="f2781-569">no</span></span>             | <span data-ttu-id="f2781-570">non</span><span class="sxs-lookup"><span data-stu-id="f2781-570">no</span></span>           |
| <span data-ttu-id="f2781-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="f2781-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="f2781-572">non</span><span class="sxs-lookup"><span data-stu-id="f2781-572">no</span></span>             | <span data-ttu-id="f2781-573">non</span><span class="sxs-lookup"><span data-stu-id="f2781-573">no</span></span>           |
| <span data-ttu-id="f2781-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="f2781-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="f2781-575">non</span><span class="sxs-lookup"><span data-stu-id="f2781-575">no</span></span>             | <span data-ttu-id="f2781-576">non</span><span class="sxs-lookup"><span data-stu-id="f2781-576">no</span></span>           |
| <span data-ttu-id="f2781-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="f2781-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="f2781-578">non</span><span class="sxs-lookup"><span data-stu-id="f2781-578">no</span></span>             | <span data-ttu-id="f2781-579">non</span><span class="sxs-lookup"><span data-stu-id="f2781-579">no</span></span>           |
| <span data-ttu-id="f2781-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="f2781-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="f2781-581">non</span><span class="sxs-lookup"><span data-stu-id="f2781-581">no</span></span>             | <span data-ttu-id="f2781-582">non</span><span class="sxs-lookup"><span data-stu-id="f2781-582">no</span></span>           |
| <span data-ttu-id="f2781-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="f2781-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="f2781-584">non</span><span class="sxs-lookup"><span data-stu-id="f2781-584">no</span></span>             | <span data-ttu-id="f2781-585">non</span><span class="sxs-lookup"><span data-stu-id="f2781-585">no</span></span>           |
| <span data-ttu-id="f2781-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="f2781-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="f2781-587">non</span><span class="sxs-lookup"><span data-stu-id="f2781-587">no</span></span>             | <span data-ttu-id="f2781-588">non</span><span class="sxs-lookup"><span data-stu-id="f2781-588">no</span></span>           |
| <span data-ttu-id="f2781-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="f2781-590">non</span><span class="sxs-lookup"><span data-stu-id="f2781-590">no</span></span>             | <span data-ttu-id="f2781-591">non</span><span class="sxs-lookup"><span data-stu-id="f2781-591">no</span></span>           |
| <span data-ttu-id="f2781-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="f2781-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="f2781-593">non</span><span class="sxs-lookup"><span data-stu-id="f2781-593">no</span></span>             | <span data-ttu-id="f2781-594">non</span><span class="sxs-lookup"><span data-stu-id="f2781-594">no</span></span>           |
| <span data-ttu-id="f2781-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="f2781-596">non</span><span class="sxs-lookup"><span data-stu-id="f2781-596">no</span></span>             | <span data-ttu-id="f2781-597">non</span><span class="sxs-lookup"><span data-stu-id="f2781-597">no</span></span>           |
| <span data-ttu-id="f2781-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f2781-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f2781-599">non</span><span class="sxs-lookup"><span data-stu-id="f2781-599">no</span></span>             | <span data-ttu-id="f2781-600">non</span><span class="sxs-lookup"><span data-stu-id="f2781-600">no</span></span>           |
| <span data-ttu-id="f2781-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f2781-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f2781-602">non</span><span class="sxs-lookup"><span data-stu-id="f2781-602">no</span></span>             | <span data-ttu-id="f2781-603">non</span><span class="sxs-lookup"><span data-stu-id="f2781-603">no</span></span>           |
| <span data-ttu-id="f2781-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f2781-604">msdyn_progress</span></span>                         | <span data-ttu-id="f2781-605">non</span><span class="sxs-lookup"><span data-stu-id="f2781-605">no</span></span>             | <span data-ttu-id="f2781-606">non</span><span class="sxs-lookup"><span data-stu-id="f2781-606">no</span></span>           |
| <span data-ttu-id="f2781-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f2781-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f2781-608">non</span><span class="sxs-lookup"><span data-stu-id="f2781-608">no</span></span>             | <span data-ttu-id="f2781-609">non</span><span class="sxs-lookup"><span data-stu-id="f2781-609">no</span></span>           |
| <span data-ttu-id="f2781-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f2781-611">non</span><span class="sxs-lookup"><span data-stu-id="f2781-611">no</span></span>             | <span data-ttu-id="f2781-612">non</span><span class="sxs-lookup"><span data-stu-id="f2781-612">no</span></span>           |
| <span data-ttu-id="f2781-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f2781-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f2781-614">non</span><span class="sxs-lookup"><span data-stu-id="f2781-614">no</span></span>             | <span data-ttu-id="f2781-615">non</span><span class="sxs-lookup"><span data-stu-id="f2781-615">no</span></span>           |
| <span data-ttu-id="f2781-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f2781-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f2781-617">non</span><span class="sxs-lookup"><span data-stu-id="f2781-617">no</span></span>             | <span data-ttu-id="f2781-618">non</span><span class="sxs-lookup"><span data-stu-id="f2781-618">no</span></span>           |
| <span data-ttu-id="f2781-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="f2781-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="f2781-620">non</span><span class="sxs-lookup"><span data-stu-id="f2781-620">no</span></span>             | <span data-ttu-id="f2781-621">non</span><span class="sxs-lookup"><span data-stu-id="f2781-621">no</span></span>           |
| <span data-ttu-id="f2781-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="f2781-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="f2781-623">non</span><span class="sxs-lookup"><span data-stu-id="f2781-623">no</span></span>             | <span data-ttu-id="f2781-624">non</span><span class="sxs-lookup"><span data-stu-id="f2781-624">no</span></span>           |
| <span data-ttu-id="f2781-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f2781-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="f2781-626">non</span><span class="sxs-lookup"><span data-stu-id="f2781-626">no</span></span>             | <span data-ttu-id="f2781-627">non</span><span class="sxs-lookup"><span data-stu-id="f2781-627">no</span></span>           |
| <span data-ttu-id="f2781-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="f2781-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="f2781-629">non</span><span class="sxs-lookup"><span data-stu-id="f2781-629">no</span></span>             | <span data-ttu-id="f2781-630">non</span><span class="sxs-lookup"><span data-stu-id="f2781-630">no</span></span>           |
| <span data-ttu-id="f2781-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f2781-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f2781-632">non</span><span class="sxs-lookup"><span data-stu-id="f2781-632">no</span></span>             | <span data-ttu-id="f2781-633">non</span><span class="sxs-lookup"><span data-stu-id="f2781-633">no</span></span>           |
| <span data-ttu-id="f2781-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f2781-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f2781-635">non</span><span class="sxs-lookup"><span data-stu-id="f2781-635">no</span></span>             | <span data-ttu-id="f2781-636">non</span><span class="sxs-lookup"><span data-stu-id="f2781-636">no</span></span>           |
| <span data-ttu-id="f2781-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="f2781-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="f2781-638">non</span><span class="sxs-lookup"><span data-stu-id="f2781-638">no</span></span>             | <span data-ttu-id="f2781-639">non</span><span class="sxs-lookup"><span data-stu-id="f2781-639">no</span></span>           |
| <span data-ttu-id="f2781-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="f2781-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="f2781-641">non</span><span class="sxs-lookup"><span data-stu-id="f2781-641">no</span></span>             | <span data-ttu-id="f2781-642">non</span><span class="sxs-lookup"><span data-stu-id="f2781-642">no</span></span>           |
| <span data-ttu-id="f2781-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f2781-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f2781-644">non</span><span class="sxs-lookup"><span data-stu-id="f2781-644">no</span></span>             | <span data-ttu-id="f2781-645">non</span><span class="sxs-lookup"><span data-stu-id="f2781-645">no</span></span>           |
| <span data-ttu-id="f2781-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="f2781-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="f2781-647">non</span><span class="sxs-lookup"><span data-stu-id="f2781-647">no</span></span>             | <span data-ttu-id="f2781-648">non</span><span class="sxs-lookup"><span data-stu-id="f2781-648">no</span></span>           |
| <span data-ttu-id="f2781-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="f2781-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="f2781-650">non</span><span class="sxs-lookup"><span data-stu-id="f2781-650">no</span></span>             | <span data-ttu-id="f2781-651">non</span><span class="sxs-lookup"><span data-stu-id="f2781-651">no</span></span>           |
| <span data-ttu-id="f2781-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="f2781-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="f2781-653">non</span><span class="sxs-lookup"><span data-stu-id="f2781-653">no</span></span>             | <span data-ttu-id="f2781-654">non</span><span class="sxs-lookup"><span data-stu-id="f2781-654">no</span></span>           |
| <span data-ttu-id="f2781-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="f2781-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="f2781-656">non</span><span class="sxs-lookup"><span data-stu-id="f2781-656">no</span></span>             | <span data-ttu-id="f2781-657">non</span><span class="sxs-lookup"><span data-stu-id="f2781-657">no</span></span>           |
| <span data-ttu-id="f2781-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="f2781-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="f2781-659">non</span><span class="sxs-lookup"><span data-stu-id="f2781-659">no</span></span>             | <span data-ttu-id="f2781-660">non</span><span class="sxs-lookup"><span data-stu-id="f2781-660">no</span></span>           |
| <span data-ttu-id="f2781-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="f2781-662">non</span><span class="sxs-lookup"><span data-stu-id="f2781-662">no</span></span>             | <span data-ttu-id="f2781-663">non</span><span class="sxs-lookup"><span data-stu-id="f2781-663">no</span></span>           |
| <span data-ttu-id="f2781-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="f2781-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="f2781-665">non</span><span class="sxs-lookup"><span data-stu-id="f2781-665">no</span></span>             | <span data-ttu-id="f2781-666">non</span><span class="sxs-lookup"><span data-stu-id="f2781-666">no</span></span>           |
| <span data-ttu-id="f2781-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f2781-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="f2781-668">non</span><span class="sxs-lookup"><span data-stu-id="f2781-668">no</span></span>             | <span data-ttu-id="f2781-669">non</span><span class="sxs-lookup"><span data-stu-id="f2781-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="f2781-670">Limitacións e problemas coñecidos</span><span class="sxs-lookup"><span data-stu-id="f2781-670">Limitations and known issues</span></span>
<span data-ttu-id="f2781-671">A continuación móstrase unha lista de limitacións e problemas coñecidos:</span><span class="sxs-lookup"><span data-stu-id="f2781-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="f2781-672">As API de programación só poden ser empregadas por **Usuarios con licenza Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="f2781-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="f2781-673">Non poden ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="f2781-673">They can't be used by:</span></span>
    - <span data-ttu-id="f2781-674">Usuarios da aplicación</span><span class="sxs-lookup"><span data-stu-id="f2781-674">Application users</span></span>
    - <span data-ttu-id="f2781-675">Usuario do sistema</span><span class="sxs-lookup"><span data-stu-id="f2781-675">System users</span></span>
    - <span data-ttu-id="f2781-676">Usuarios de integración</span><span class="sxs-lookup"><span data-stu-id="f2781-676">Integration users</span></span>
    - <span data-ttu-id="f2781-677">Outros usuarios que non teñen a licenza requirida</span><span class="sxs-lookup"><span data-stu-id="f2781-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="f2781-678">Cada **OperationSet** só pode ter un máximo de 100 operacións.</span><span class="sxs-lookup"><span data-stu-id="f2781-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="f2781-679">Cada usuario só pode ter un máximo de 10 **OperationSets** abertos.</span><span class="sxs-lookup"><span data-stu-id="f2781-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="f2781-680">Project Operations admite actualmente un máximo de 500 tarefas totais nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="f2781-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="f2781-681">O estado de fallo e os rexistros de fallos de **OperationSet** non están dispoñibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="f2781-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="f2781-682">As API de programación están en versión preliminar pública.</span><span class="sxs-lookup"><span data-stu-id="f2781-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="f2781-683">Microsoft non admite o uso destas API nun ambiente de produción.</span><span class="sxs-lookup"><span data-stu-id="f2781-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="f2781-684">Límites en proxectos e tarefas</span><span class="sxs-lookup"><span data-stu-id="f2781-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="f2781-685">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="f2781-685">Error handling</span></span>

   - <span data-ttu-id="f2781-686">Para revisar os erros xerados a partir dos conxuntos de operacións, vaia a **Configuración** \> **Integración de programación** \> **Conxuntos de operacións**.</span><span class="sxs-lookup"><span data-stu-id="f2781-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="f2781-687">Para revisar os erros xerados desde o servizo de programación de proxectos, vaia a **Configuración** \> **Integración de programación** \> **Rexistros de erros PSS**.</span><span class="sxs-lookup"><span data-stu-id="f2781-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="f2781-688">Escenario de exemplo</span><span class="sxs-lookup"><span data-stu-id="f2781-688">Sample scenario</span></span>

<span data-ttu-id="f2781-689">Neste escenario, creará un proxecto, un membro do equipo, catro tarefas e dúas atribucións de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2781-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="f2781-690">A continuación, actualizará unha tarefa, actualizará o proxecto, eliminará unha tarefa, eliminará unha atribución de recursos e creará unha dependencia de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f2781-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="f2781-691">Exemplos adicionais</span><span class="sxs-lookup"><span data-stu-id="f2781-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
