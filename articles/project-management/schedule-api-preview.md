---
title: Usar as API de programación para realizar operacións con entidades de programación.
description: Este tema ofrece información e mostras para usar as API de programación.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116795"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="3cb85-103">Usar as API de programación para realizar operacións con entidades de programación.</span><span class="sxs-lookup"><span data-stu-id="3cb85-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="3cb85-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="3cb85-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="3cb85-105">Unha parte ou toda a funcionalidade sinalada neste tema está dispoñible como parte dunha versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="3cb85-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="3cb85-106">O contido e a funcionalidade están suxeitos a cambios.</span><span class="sxs-lookup"><span data-stu-id="3cb85-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="3cb85-107">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="3cb85-107">Scheduling entities</span></span>

<span data-ttu-id="3cb85-108">As API de programación ofrecen a capacidade de realizar, actualizar e eliminar operacións con **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="3cb85-109">Estas entidades xestiónanse a través do motor de programación en Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="3cb85-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="3cb85-110">Crear, actualizar e eliminar operacións con **Entidades de programación** estaban restrinxidos en versións anteriores de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3cb85-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="3cb85-111">A seguinte táboa ofrece unha lista completa das **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="3cb85-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="3cb85-112">Entity name</span></span>  | <span data-ttu-id="3cb85-113">Nome lóxico da entidade</span><span class="sxs-lookup"><span data-stu-id="3cb85-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="3cb85-114">Project</span><span class="sxs-lookup"><span data-stu-id="3cb85-114">Project</span></span> | <span data-ttu-id="3cb85-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="3cb85-115">msdyn_project</span></span> |
| <span data-ttu-id="3cb85-116">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-116">Project Task</span></span>  | <span data-ttu-id="3cb85-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="3cb85-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="3cb85-118">Dependencia da tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-118">Project Task Dependency</span></span>  | <span data-ttu-id="3cb85-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="3cb85-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="3cb85-120">Atribución do recurso</span><span class="sxs-lookup"><span data-stu-id="3cb85-120">Resource Assignment</span></span> | <span data-ttu-id="3cb85-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="3cb85-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="3cb85-122">Depósito do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-122">Project Bucket</span></span>  | <span data-ttu-id="3cb85-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="3cb85-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="3cb85-124">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-124">Project Team Member</span></span> | <span data-ttu-id="3cb85-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="3cb85-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="3cb85-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="3cb85-126">OperationSet</span></span>

<span data-ttu-id="3cb85-127">OperationSet é un patrón de unidade de traballo que se pode empregar cando se deben procesar varias solicitudes que afectan á programación dentro dunha transacción.</span><span class="sxs-lookup"><span data-stu-id="3cb85-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="3cb85-128">API de programación</span><span class="sxs-lookup"><span data-stu-id="3cb85-128">Schedule APIs</span></span>

<span data-ttu-id="3cb85-129">A continuación móstrase unha lista das API de programación actuais.</span><span class="sxs-lookup"><span data-stu-id="3cb85-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="3cb85-130">**msdyn_CreateProjectV1**: Esta API pódese usar para crear un proxecto.</span><span class="sxs-lookup"><span data-stu-id="3cb85-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="3cb85-131">O proxecto e o depósito por defecto do proxecto créanse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3cb85-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="3cb85-132">**msdyn_CreateTeamMemberV1**: Esta API pódese usar para crear un membro do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="3cb85-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="3cb85-133">O rexistro de membro do equipo créase inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3cb85-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="3cb85-134">**msdyn_CreateOperationSetV1**: Esta API pode usarse para programar varias solicitudes que deben realizarse dentro dunha transacción.</span><span class="sxs-lookup"><span data-stu-id="3cb85-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="3cb85-135">**msdyn_PSSCreateV1**: Esta API pódese usar para crear unha entidade.</span><span class="sxs-lookup"><span data-stu-id="3cb85-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="3cb85-136">A entidade pode ser calquera das entidades de programación que admitan a operación de creación.</span><span class="sxs-lookup"><span data-stu-id="3cb85-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="3cb85-137">**msdyn_PSSUpdateV1**: Esta API pódese usar para actualizar unha entidade.</span><span class="sxs-lookup"><span data-stu-id="3cb85-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="3cb85-138">A entidade pode ser calquera das entidades de programación que admitan a operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="3cb85-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="3cb85-139">**msdyn_PSSDeleteV1**: Esta API pódese usar para eliminar unha entidade.</span><span class="sxs-lookup"><span data-stu-id="3cb85-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="3cb85-140">A entidade pode ser calquera das entidades de programación que admitan a operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="3cb85-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="3cb85-141">**msdyn_ExecuteOperationSetV1**: Esta API úsase para executar todas as operacións dentro do conxunto de operacións determinado.</span><span class="sxs-lookup"><span data-stu-id="3cb85-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="3cb85-142">Uso das API de programación con OperationSet</span><span class="sxs-lookup"><span data-stu-id="3cb85-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="3cb85-143">Como os rexistros con **CreateProjectV1** e **CreateTeamMemberV1** créanse inmediatamente, estas API non se poden empregar en **OperationSet** directamente.</span><span class="sxs-lookup"><span data-stu-id="3cb85-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="3cb85-144">Non obstante, pode usar a API para crear rexistros necesarios, crear un **OperationSet** e, a seguir, usar estes rexistros creados previamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="3cb85-145">Operacións compatibles</span><span class="sxs-lookup"><span data-stu-id="3cb85-145">Supported operations</span></span>

| <span data-ttu-id="3cb85-146">Entidade de programación</span><span class="sxs-lookup"><span data-stu-id="3cb85-146">Scheduling entity</span></span> | <span data-ttu-id="3cb85-147">Crear</span><span class="sxs-lookup"><span data-stu-id="3cb85-147">Create</span></span> | <span data-ttu-id="3cb85-148">Actualización</span><span class="sxs-lookup"><span data-stu-id="3cb85-148">Update</span></span> | <span data-ttu-id="3cb85-149">SUPR</span><span class="sxs-lookup"><span data-stu-id="3cb85-149">Delete</span></span> | <span data-ttu-id="3cb85-150">Consideracións importantes</span><span class="sxs-lookup"><span data-stu-id="3cb85-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="3cb85-151">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-151">Project task</span></span> | <span data-ttu-id="3cb85-152">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-152">Yes</span></span> | <span data-ttu-id="3cb85-153">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-153">Yes</span></span> | <span data-ttu-id="3cb85-154">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-154">Yes</span></span> | <span data-ttu-id="3cb85-155">Nada</span><span class="sxs-lookup"><span data-stu-id="3cb85-155">None</span></span> |
| <span data-ttu-id="3cb85-156">Dependencia da tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-156">Project task dependency</span></span> | <span data-ttu-id="3cb85-157">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-157">Yes</span></span> | <span data-ttu-id="3cb85-158">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-158">Yes</span></span> | | <span data-ttu-id="3cb85-159">Os rexistros de dependencia de tarefas do proxecto non se actualizan.</span><span class="sxs-lookup"><span data-stu-id="3cb85-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="3cb85-160">Pola contra, pódese eliminar un rexistro antigo e pódese crear un novo rexistro.</span><span class="sxs-lookup"><span data-stu-id="3cb85-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="3cb85-161">Atribución do recurso</span><span class="sxs-lookup"><span data-stu-id="3cb85-161">Resource assignment</span></span> | <span data-ttu-id="3cb85-162">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-162">Yes</span></span> | <span data-ttu-id="3cb85-163">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-163">Yes</span></span> | | <span data-ttu-id="3cb85-164">Non se admiten operacións cos seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="3cb85-165">Os rexistros de atribución de recursos non se actualizan.</span><span class="sxs-lookup"><span data-stu-id="3cb85-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="3cb85-166">Pola contra, pódese eliminar o rexistro antigo e pódese crear un novo rexistro.</span><span class="sxs-lookup"><span data-stu-id="3cb85-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="3cb85-167">Depósito do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-167">Project bucket</span></span> | <span data-ttu-id="3cb85-168">N/D</span><span class="sxs-lookup"><span data-stu-id="3cb85-168">N/A</span></span> | <span data-ttu-id="3cb85-169">N/D</span><span class="sxs-lookup"><span data-stu-id="3cb85-169">N/A</span></span> | <span data-ttu-id="3cb85-170">N/D</span><span class="sxs-lookup"><span data-stu-id="3cb85-170">N/A</span></span> | <span data-ttu-id="3cb85-171">O depósito predefinido créase usando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="3cb85-172">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-172">Project team member</span></span> | <span data-ttu-id="3cb85-173">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-173">Yes</span></span> | <span data-ttu-id="3cb85-174">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-174">Yes</span></span> | <span data-ttu-id="3cb85-175">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-175">Yes</span></span> | <span data-ttu-id="3cb85-176">Para a operación de creación, use a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="3cb85-177">Project</span><span class="sxs-lookup"><span data-stu-id="3cb85-177">Project</span></span> | <span data-ttu-id="3cb85-178">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-178">Yes</span></span> | <span data-ttu-id="3cb85-179">Si</span><span class="sxs-lookup"><span data-stu-id="3cb85-179">Yes</span></span> | <span data-ttu-id="3cb85-180">N/D</span><span class="sxs-lookup"><span data-stu-id="3cb85-180">N/A</span></span> | <span data-ttu-id="3cb85-181">Non se admiten operacións cos seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="3cb85-182">Estas API pódense chamar con obxectos de entidade que inclúen campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3cb85-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="3cb85-183">A propiedade de ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="3cb85-183">The ID property is optional.</span></span> <span data-ttu-id="3cb85-184">Se se proporciona, o sistema tenta usala e lanza unha excepción se non se pode usar.</span><span class="sxs-lookup"><span data-stu-id="3cb85-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="3cb85-185">Se non se proporciona, o sistema xeraraa.</span><span class="sxs-lookup"><span data-stu-id="3cb85-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="3cb85-186">Campos restrinxidos</span><span class="sxs-lookup"><span data-stu-id="3cb85-186">Restricted fields</span></span>

<span data-ttu-id="3cb85-187">As táboas seguintes definen os campos que están restrinxidos de **Crear** e **Editar.**</span><span class="sxs-lookup"><span data-stu-id="3cb85-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="3cb85-188">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-188">Project task</span></span>

| <span data-ttu-id="3cb85-189">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="3cb85-189">**Logical name**</span></span>                       | <span data-ttu-id="3cb85-190">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="3cb85-190">**Can create**</span></span> | <span data-ttu-id="3cb85-191">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="3cb85-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="3cb85-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="3cb85-193">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-193">no</span></span>             | <span data-ttu-id="3cb85-194">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-194">no</span></span>               |
| <span data-ttu-id="3cb85-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="3cb85-196">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-196">no</span></span>             | <span data-ttu-id="3cb85-197">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-197">no</span></span>               |
| <span data-ttu-id="3cb85-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="3cb85-198">msdyn_actualend</span></span>                        | <span data-ttu-id="3cb85-199">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-199">no</span></span>             | <span data-ttu-id="3cb85-200">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-200">no</span></span>               |
| <span data-ttu-id="3cb85-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="3cb85-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="3cb85-202">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-202">no</span></span>             | <span data-ttu-id="3cb85-203">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-203">no</span></span>               |
| <span data-ttu-id="3cb85-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="3cb85-205">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-205">no</span></span>             | <span data-ttu-id="3cb85-206">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-206">no</span></span>               |
| <span data-ttu-id="3cb85-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="3cb85-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="3cb85-208">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-208">no</span></span>             | <span data-ttu-id="3cb85-209">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-209">no</span></span>               |
| <span data-ttu-id="3cb85-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="3cb85-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="3cb85-211">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-211">no</span></span>             | <span data-ttu-id="3cb85-212">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-212">no</span></span>               |
| <span data-ttu-id="3cb85-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="3cb85-214">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-214">no</span></span>             | <span data-ttu-id="3cb85-215">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-215">no</span></span>               |
| <span data-ttu-id="3cb85-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="3cb85-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="3cb85-217">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-217">no</span></span>             | <span data-ttu-id="3cb85-218">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-218">no</span></span>               |
| <span data-ttu-id="3cb85-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3cb85-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="3cb85-220">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-220">no</span></span>             | <span data-ttu-id="3cb85-221">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-221">no</span></span>               |
| <span data-ttu-id="3cb85-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="3cb85-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="3cb85-223">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-223">no</span></span>             | <span data-ttu-id="3cb85-224">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-224">no</span></span>               |
| <span data-ttu-id="3cb85-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="3cb85-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="3cb85-226">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-226">no</span></span>             | <span data-ttu-id="3cb85-227">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-227">no</span></span>               |
| <span data-ttu-id="3cb85-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="3cb85-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="3cb85-229">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-229">no</span></span>             | <span data-ttu-id="3cb85-230">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-230">no</span></span>               |
| <span data-ttu-id="3cb85-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="3cb85-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="3cb85-232">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-232">no</span></span>             | <span data-ttu-id="3cb85-233">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-233">no</span></span>               |
| <span data-ttu-id="3cb85-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="3cb85-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="3cb85-235">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-235">no</span></span>             | <span data-ttu-id="3cb85-236">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-236">no</span></span>               |
| <span data-ttu-id="3cb85-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="3cb85-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="3cb85-238">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-238">no</span></span>             | <span data-ttu-id="3cb85-239">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-239">no</span></span>               |
| <span data-ttu-id="3cb85-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="3cb85-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="3cb85-241">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-241">no</span></span>             | <span data-ttu-id="3cb85-242">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-242">no</span></span>               |
| <span data-ttu-id="3cb85-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="3cb85-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="3cb85-244">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-244">no</span></span>             | <span data-ttu-id="3cb85-245">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-245">no</span></span>               |
| <span data-ttu-id="3cb85-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="3cb85-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="3cb85-247">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-247">no</span></span>             | <span data-ttu-id="3cb85-248">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-248">no</span></span>               |
| <span data-ttu-id="3cb85-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="3cb85-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="3cb85-250">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-250">no</span></span>             | <span data-ttu-id="3cb85-251">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-251">no</span></span>               |
| <span data-ttu-id="3cb85-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="3cb85-253">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-253">no</span></span>             | <span data-ttu-id="3cb85-254">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-254">no</span></span>               |
| <span data-ttu-id="3cb85-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="3cb85-256">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-256">no</span></span>             | <span data-ttu-id="3cb85-257">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-257">no</span></span>               |
| <span data-ttu-id="3cb85-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3cb85-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="3cb85-259">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-259">no</span></span>             | <span data-ttu-id="3cb85-260">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-260">no</span></span>               |
| <span data-ttu-id="3cb85-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="3cb85-262">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-262">no</span></span>             | <span data-ttu-id="3cb85-263">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-263">no</span></span>               |
| <span data-ttu-id="3cb85-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="3cb85-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="3cb85-265">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-265">no</span></span>             | <span data-ttu-id="3cb85-266">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-266">no</span></span>               |
| <span data-ttu-id="3cb85-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="3cb85-267">msdyn_progress</span></span>                         | <span data-ttu-id="3cb85-268">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-268">no</span></span>             | <span data-ttu-id="3cb85-269">non (si para P4W)</span><span class="sxs-lookup"><span data-stu-id="3cb85-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="3cb85-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="3cb85-271">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-271">no</span></span>             | <span data-ttu-id="3cb85-272">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-272">no</span></span>               |
| <span data-ttu-id="3cb85-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="3cb85-274">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-274">no</span></span>             | <span data-ttu-id="3cb85-275">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-275">no</span></span>               |
| <span data-ttu-id="3cb85-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="3cb85-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="3cb85-277">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-277">no</span></span>             | <span data-ttu-id="3cb85-278">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-278">no</span></span>               |
| <span data-ttu-id="3cb85-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="3cb85-280">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-280">no</span></span>             | <span data-ttu-id="3cb85-281">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-281">no</span></span>               |
| <span data-ttu-id="3cb85-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="3cb85-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="3cb85-283">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-283">no</span></span>             | <span data-ttu-id="3cb85-284">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-284">no</span></span>               |
| <span data-ttu-id="3cb85-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="3cb85-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="3cb85-286">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-286">no</span></span>             | <span data-ttu-id="3cb85-287">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-287">no</span></span>               |
| <span data-ttu-id="3cb85-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="3cb85-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="3cb85-289">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-289">no</span></span>             | <span data-ttu-id="3cb85-290">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-290">no</span></span>               |
| <span data-ttu-id="3cb85-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="3cb85-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="3cb85-292">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-292">no</span></span>             | <span data-ttu-id="3cb85-293">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-293">no</span></span>               |
| <span data-ttu-id="3cb85-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="3cb85-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="3cb85-295">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-295">no</span></span>             | <span data-ttu-id="3cb85-296">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-296">no</span></span>               |
| <span data-ttu-id="3cb85-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="3cb85-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="3cb85-298">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-298">no</span></span>             | <span data-ttu-id="3cb85-299">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-299">no</span></span>               |
| <span data-ttu-id="3cb85-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="3cb85-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="3cb85-301">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-301">no</span></span>             | <span data-ttu-id="3cb85-302">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-302">no</span></span>               |
| <span data-ttu-id="3cb85-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="3cb85-304">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-304">no</span></span>             | <span data-ttu-id="3cb85-305">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-305">no</span></span>               |
| <span data-ttu-id="3cb85-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="3cb85-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="3cb85-307">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-307">no</span></span>             | <span data-ttu-id="3cb85-308">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-308">no</span></span>               |
| <span data-ttu-id="3cb85-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="3cb85-310">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-310">no</span></span>             | <span data-ttu-id="3cb85-311">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-311">no</span></span>               |
| <span data-ttu-id="3cb85-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="3cb85-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="3cb85-313">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-313">no</span></span>             | <span data-ttu-id="3cb85-314">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-314">no</span></span>               |
| <span data-ttu-id="3cb85-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="3cb85-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="3cb85-316">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-316">no</span></span>             | <span data-ttu-id="3cb85-317">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-317">no</span></span>               |
| <span data-ttu-id="3cb85-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="3cb85-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="3cb85-319">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-319">no</span></span>             | <span data-ttu-id="3cb85-320">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-320">no</span></span>               |
| <span data-ttu-id="3cb85-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="3cb85-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="3cb85-322">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-322">no</span></span>             | <span data-ttu-id="3cb85-323">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-323">no</span></span>               |
| <span data-ttu-id="3cb85-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="3cb85-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="3cb85-325">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-325">no</span></span>             | <span data-ttu-id="3cb85-326">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-326">no</span></span>               |
| <span data-ttu-id="3cb85-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="3cb85-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="3cb85-328">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-328">no</span></span>             | <span data-ttu-id="3cb85-329">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-329">no</span></span>               |
| <span data-ttu-id="3cb85-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="3cb85-330">msdyn_summary</span></span>                          | <span data-ttu-id="3cb85-331">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-331">no</span></span>             | <span data-ttu-id="3cb85-332">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-332">no</span></span>               |
| <span data-ttu-id="3cb85-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="3cb85-334">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-334">no</span></span>             | <span data-ttu-id="3cb85-335">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-335">no</span></span>               |
| <span data-ttu-id="3cb85-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="3cb85-337">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-337">no</span></span>             | <span data-ttu-id="3cb85-338">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="3cb85-339">Dependencia da tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-339">Project task dependency</span></span>

| <span data-ttu-id="3cb85-340">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="3cb85-340">**Logical name**</span></span>              | <span data-ttu-id="3cb85-341">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="3cb85-341">**Can create**</span></span> | <span data-ttu-id="3cb85-342">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="3cb85-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="3cb85-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="3cb85-343">msdyn_linktype</span></span>                | <span data-ttu-id="3cb85-344">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-344">no</span></span>             | <span data-ttu-id="3cb85-345">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-345">no</span></span>           |
| <span data-ttu-id="3cb85-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="3cb85-346">msdyn_linktypename</span></span>            | <span data-ttu-id="3cb85-347">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-347">no</span></span>             | <span data-ttu-id="3cb85-348">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-348">no</span></span>           |
| <span data-ttu-id="3cb85-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="3cb85-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="3cb85-350">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-350">yes</span></span>            | <span data-ttu-id="3cb85-351">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-351">no</span></span>           |
| <span data-ttu-id="3cb85-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="3cb85-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="3cb85-353">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-353">yes</span></span>            | <span data-ttu-id="3cb85-354">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-354">no</span></span>           |
| <span data-ttu-id="3cb85-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="3cb85-355">msdyn_project</span></span>                 | <span data-ttu-id="3cb85-356">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-356">yes</span></span>            | <span data-ttu-id="3cb85-357">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-357">no</span></span>           |
| <span data-ttu-id="3cb85-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="3cb85-358">msdyn_projectname</span></span>             | <span data-ttu-id="3cb85-359">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-359">yes</span></span>            | <span data-ttu-id="3cb85-360">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-360">no</span></span>           |
| <span data-ttu-id="3cb85-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="3cb85-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="3cb85-362">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-362">yes</span></span>            | <span data-ttu-id="3cb85-363">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-363">no</span></span>           |
| <span data-ttu-id="3cb85-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="3cb85-364">msdyn_successortask</span></span>           | <span data-ttu-id="3cb85-365">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-365">yes</span></span>            | <span data-ttu-id="3cb85-366">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-366">no</span></span>           |
| <span data-ttu-id="3cb85-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="3cb85-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="3cb85-368">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-368">yes</span></span>            | <span data-ttu-id="3cb85-369">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="3cb85-370">Atribución do recurso</span><span class="sxs-lookup"><span data-stu-id="3cb85-370">Resource assignment</span></span>

| <span data-ttu-id="3cb85-371">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="3cb85-371">**Logical name**</span></span>             | <span data-ttu-id="3cb85-372">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="3cb85-372">**Can create**</span></span> | <span data-ttu-id="3cb85-373">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="3cb85-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="3cb85-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="3cb85-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="3cb85-375">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-375">yes</span></span>            | <span data-ttu-id="3cb85-376">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-376">no</span></span>           |
| <span data-ttu-id="3cb85-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="3cb85-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="3cb85-378">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-378">yes</span></span>            | <span data-ttu-id="3cb85-379">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-379">no</span></span>           |
| <span data-ttu-id="3cb85-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="3cb85-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="3cb85-381">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-381">no</span></span>             | <span data-ttu-id="3cb85-382">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-382">no</span></span>           |
| <span data-ttu-id="3cb85-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="3cb85-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="3cb85-384">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-384">no</span></span>             | <span data-ttu-id="3cb85-385">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-385">no</span></span>           |
| <span data-ttu-id="3cb85-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="3cb85-386">msdyn_committype</span></span>             | <span data-ttu-id="3cb85-387">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-387">no</span></span>             | <span data-ttu-id="3cb85-388">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-388">no</span></span>           |
| <span data-ttu-id="3cb85-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="3cb85-389">msdyn_committypename</span></span>         | <span data-ttu-id="3cb85-390">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-390">no</span></span>             | <span data-ttu-id="3cb85-391">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-391">no</span></span>           |
| <span data-ttu-id="3cb85-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="3cb85-392">msdyn_effort</span></span>                 | <span data-ttu-id="3cb85-393">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-393">no</span></span>             | <span data-ttu-id="3cb85-394">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-394">no</span></span>           |
| <span data-ttu-id="3cb85-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3cb85-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="3cb85-396">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-396">no</span></span>             | <span data-ttu-id="3cb85-397">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-397">no</span></span>           |
| <span data-ttu-id="3cb85-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="3cb85-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="3cb85-399">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-399">no</span></span>             | <span data-ttu-id="3cb85-400">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-400">no</span></span>           |
| <span data-ttu-id="3cb85-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="3cb85-401">msdyn_finish</span></span>                 | <span data-ttu-id="3cb85-402">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-402">no</span></span>             | <span data-ttu-id="3cb85-403">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-403">no</span></span>           |
| <span data-ttu-id="3cb85-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="3cb85-405">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-405">no</span></span>             | <span data-ttu-id="3cb85-406">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-406">no</span></span>           |
| <span data-ttu-id="3cb85-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="3cb85-408">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-408">no</span></span>             | <span data-ttu-id="3cb85-409">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-409">no</span></span>           |
| <span data-ttu-id="3cb85-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="3cb85-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="3cb85-411">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-411">no</span></span>             | <span data-ttu-id="3cb85-412">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-412">no</span></span>           |
| <span data-ttu-id="3cb85-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3cb85-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="3cb85-414">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-414">no</span></span>             | <span data-ttu-id="3cb85-415">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-415">no</span></span>           |
| <span data-ttu-id="3cb85-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="3cb85-417">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-417">no</span></span>             | <span data-ttu-id="3cb85-418">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-418">no</span></span>           |
| <span data-ttu-id="3cb85-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="3cb85-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="3cb85-420">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-420">no</span></span>             | <span data-ttu-id="3cb85-421">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-421">no</span></span>           |
| <span data-ttu-id="3cb85-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="3cb85-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="3cb85-423">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-423">no</span></span>             | <span data-ttu-id="3cb85-424">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-424">no</span></span>           |
| <span data-ttu-id="3cb85-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="3cb85-425">msdyn_projectid</span></span>              | <span data-ttu-id="3cb85-426">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-426">yes</span></span>            | <span data-ttu-id="3cb85-427">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-427">no</span></span>           |
| <span data-ttu-id="3cb85-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="3cb85-428">msdyn_projectidname</span></span>          | <span data-ttu-id="3cb85-429">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-429">no</span></span>             | <span data-ttu-id="3cb85-430">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-430">no</span></span>           |
| <span data-ttu-id="3cb85-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="3cb85-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="3cb85-432">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-432">no</span></span>             | <span data-ttu-id="3cb85-433">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-433">no</span></span>           |
| <span data-ttu-id="3cb85-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="3cb85-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="3cb85-435">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-435">no</span></span>             | <span data-ttu-id="3cb85-436">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-436">no</span></span>           |
| <span data-ttu-id="3cb85-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="3cb85-437">msdyn_start</span></span>                  | <span data-ttu-id="3cb85-438">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-438">no</span></span>             | <span data-ttu-id="3cb85-439">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-439">no</span></span>           |
| <span data-ttu-id="3cb85-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="3cb85-440">msdyn_taskid</span></span>                 | <span data-ttu-id="3cb85-441">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-441">no</span></span>             | <span data-ttu-id="3cb85-442">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-442">no</span></span>           |
| <span data-ttu-id="3cb85-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="3cb85-443">msdyn_taskidname</span></span>             | <span data-ttu-id="3cb85-444">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-444">no</span></span>             | <span data-ttu-id="3cb85-445">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-445">no</span></span>           |
| <span data-ttu-id="3cb85-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="3cb85-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="3cb85-447">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-447">no</span></span>             | <span data-ttu-id="3cb85-448">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="3cb85-449">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="3cb85-449">Project team member</span></span>

| <span data-ttu-id="3cb85-450">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="3cb85-450">**Logical name**</span></span>                                 | <span data-ttu-id="3cb85-451">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="3cb85-451">**Can create**</span></span> | <span data-ttu-id="3cb85-452">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="3cb85-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="3cb85-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="3cb85-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="3cb85-454">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-454">no</span></span>             | <span data-ttu-id="3cb85-455">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-455">no</span></span>           |
| <span data-ttu-id="3cb85-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="3cb85-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="3cb85-457">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-457">no</span></span>             | <span data-ttu-id="3cb85-458">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-458">no</span></span>           |
| <span data-ttu-id="3cb85-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="3cb85-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="3cb85-460">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-460">no</span></span>             | <span data-ttu-id="3cb85-461">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-461">no</span></span>           |
| <span data-ttu-id="3cb85-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="3cb85-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="3cb85-463">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-463">no</span></span>             | <span data-ttu-id="3cb85-464">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-464">no</span></span>           |
| <span data-ttu-id="3cb85-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="3cb85-465">msdyn_effort</span></span>                                     | <span data-ttu-id="3cb85-466">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-466">no</span></span>             | <span data-ttu-id="3cb85-467">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-467">no</span></span>           |
| <span data-ttu-id="3cb85-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3cb85-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="3cb85-469">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-469">no</span></span>             | <span data-ttu-id="3cb85-470">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-470">no</span></span>           |
| <span data-ttu-id="3cb85-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="3cb85-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="3cb85-472">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-472">no</span></span>             | <span data-ttu-id="3cb85-473">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-473">no</span></span>           |
| <span data-ttu-id="3cb85-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="3cb85-474">msdyn_finish</span></span>                                     | <span data-ttu-id="3cb85-475">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-475">no</span></span>             | <span data-ttu-id="3cb85-476">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-476">no</span></span>           |
| <span data-ttu-id="3cb85-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="3cb85-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="3cb85-478">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-478">no</span></span>             | <span data-ttu-id="3cb85-479">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-479">no</span></span>           |
| <span data-ttu-id="3cb85-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="3cb85-480">msdyn_hours</span></span>                                      | <span data-ttu-id="3cb85-481">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-481">no</span></span>             | <span data-ttu-id="3cb85-482">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-482">no</span></span>           |
| <span data-ttu-id="3cb85-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="3cb85-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="3cb85-484">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-484">no</span></span>             | <span data-ttu-id="3cb85-485">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-485">no</span></span>           |
| <span data-ttu-id="3cb85-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="3cb85-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="3cb85-487">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-487">no</span></span>             | <span data-ttu-id="3cb85-488">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-488">no</span></span>           |
| <span data-ttu-id="3cb85-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="3cb85-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="3cb85-490">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-490">no</span></span>             | <span data-ttu-id="3cb85-491">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-491">no</span></span>           |
| <span data-ttu-id="3cb85-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="3cb85-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="3cb85-493">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-493">no</span></span>             | <span data-ttu-id="3cb85-494">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-494">no</span></span>           |
| <span data-ttu-id="3cb85-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="3cb85-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="3cb85-496">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-496">no</span></span>             | <span data-ttu-id="3cb85-497">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-497">no</span></span>           |
| <span data-ttu-id="3cb85-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="3cb85-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="3cb85-499">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-499">no</span></span>             | <span data-ttu-id="3cb85-500">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-500">no</span></span>           |
| <span data-ttu-id="3cb85-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="3cb85-501">msdyn_start</span></span>                                      | <span data-ttu-id="3cb85-502">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-502">no</span></span>             | <span data-ttu-id="3cb85-503">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="3cb85-504">Project</span><span class="sxs-lookup"><span data-stu-id="3cb85-504">Project</span></span>

| <span data-ttu-id="3cb85-505">**Nome lóxico**</span><span class="sxs-lookup"><span data-stu-id="3cb85-505">**Logical name**</span></span>                       | <span data-ttu-id="3cb85-506">**Pode crear**</span><span class="sxs-lookup"><span data-stu-id="3cb85-506">**Can create**</span></span> | <span data-ttu-id="3cb85-507">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="3cb85-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="3cb85-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="3cb85-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="3cb85-509">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-509">no</span></span>             | <span data-ttu-id="3cb85-510">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-510">no</span></span>           |
| <span data-ttu-id="3cb85-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="3cb85-512">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-512">no</span></span>             | <span data-ttu-id="3cb85-513">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-513">no</span></span>           |
| <span data-ttu-id="3cb85-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="3cb85-515">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-515">no</span></span>             | <span data-ttu-id="3cb85-516">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-516">no</span></span>           |
| <span data-ttu-id="3cb85-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="3cb85-518">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-518">no</span></span>             | <span data-ttu-id="3cb85-519">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-519">no</span></span>           |
| <span data-ttu-id="3cb85-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="3cb85-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="3cb85-521">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-521">no</span></span>             | <span data-ttu-id="3cb85-522">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-522">no</span></span>           |
| <span data-ttu-id="3cb85-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="3cb85-524">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-524">no</span></span>             | <span data-ttu-id="3cb85-525">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-525">no</span></span>           |
| <span data-ttu-id="3cb85-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="3cb85-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="3cb85-527">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-527">yes</span></span>            | <span data-ttu-id="3cb85-528">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-528">no</span></span>           |
| <span data-ttu-id="3cb85-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="3cb85-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="3cb85-530">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-530">yes</span></span>            | <span data-ttu-id="3cb85-531">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-531">no</span></span>           |
| <span data-ttu-id="3cb85-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="3cb85-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="3cb85-533">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-533">yes</span></span>            | <span data-ttu-id="3cb85-534">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-534">no</span></span>           |
| <span data-ttu-id="3cb85-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="3cb85-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="3cb85-536">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-536">no</span></span>             | <span data-ttu-id="3cb85-537">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-537">no</span></span>           |
| <span data-ttu-id="3cb85-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="3cb85-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="3cb85-539">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-539">no</span></span>             | <span data-ttu-id="3cb85-540">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-540">no</span></span>           |
| <span data-ttu-id="3cb85-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="3cb85-542">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-542">no</span></span>             | <span data-ttu-id="3cb85-543">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-543">no</span></span>           |
| <span data-ttu-id="3cb85-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="3cb85-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="3cb85-545">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-545">no</span></span>             | <span data-ttu-id="3cb85-546">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-546">no</span></span>           |
| <span data-ttu-id="3cb85-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="3cb85-548">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-548">no</span></span>             | <span data-ttu-id="3cb85-549">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-549">no</span></span>           |
| <span data-ttu-id="3cb85-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="3cb85-550">msdyn_duration</span></span>                         | <span data-ttu-id="3cb85-551">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-551">no</span></span>             | <span data-ttu-id="3cb85-552">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-552">no</span></span>           |
| <span data-ttu-id="3cb85-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="3cb85-553">msdyn_effort</span></span>                           | <span data-ttu-id="3cb85-554">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-554">no</span></span>             | <span data-ttu-id="3cb85-555">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-555">no</span></span>           |
| <span data-ttu-id="3cb85-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3cb85-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="3cb85-557">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-557">no</span></span>             | <span data-ttu-id="3cb85-558">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-558">no</span></span>           |
| <span data-ttu-id="3cb85-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="3cb85-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="3cb85-560">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-560">no</span></span>             | <span data-ttu-id="3cb85-561">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-561">no</span></span>           |
| <span data-ttu-id="3cb85-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="3cb85-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="3cb85-563">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-563">no</span></span>             | <span data-ttu-id="3cb85-564">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-564">no</span></span>           |
| <span data-ttu-id="3cb85-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="3cb85-565">msdyn_finish</span></span>                           | <span data-ttu-id="3cb85-566">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-566">yes</span></span>            | <span data-ttu-id="3cb85-567">si</span><span class="sxs-lookup"><span data-stu-id="3cb85-567">yes</span></span>          |
| <span data-ttu-id="3cb85-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="3cb85-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="3cb85-569">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-569">no</span></span>             | <span data-ttu-id="3cb85-570">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-570">no</span></span>           |
| <span data-ttu-id="3cb85-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="3cb85-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="3cb85-572">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-572">no</span></span>             | <span data-ttu-id="3cb85-573">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-573">no</span></span>           |
| <span data-ttu-id="3cb85-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="3cb85-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="3cb85-575">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-575">no</span></span>             | <span data-ttu-id="3cb85-576">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-576">no</span></span>           |
| <span data-ttu-id="3cb85-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="3cb85-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="3cb85-578">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-578">no</span></span>             | <span data-ttu-id="3cb85-579">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-579">no</span></span>           |
| <span data-ttu-id="3cb85-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="3cb85-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="3cb85-581">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-581">no</span></span>             | <span data-ttu-id="3cb85-582">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-582">no</span></span>           |
| <span data-ttu-id="3cb85-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="3cb85-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="3cb85-584">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-584">no</span></span>             | <span data-ttu-id="3cb85-585">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-585">no</span></span>           |
| <span data-ttu-id="3cb85-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="3cb85-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="3cb85-587">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-587">no</span></span>             | <span data-ttu-id="3cb85-588">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-588">no</span></span>           |
| <span data-ttu-id="3cb85-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="3cb85-590">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-590">no</span></span>             | <span data-ttu-id="3cb85-591">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-591">no</span></span>           |
| <span data-ttu-id="3cb85-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="3cb85-593">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-593">no</span></span>             | <span data-ttu-id="3cb85-594">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-594">no</span></span>           |
| <span data-ttu-id="3cb85-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="3cb85-596">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-596">no</span></span>             | <span data-ttu-id="3cb85-597">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-597">no</span></span>           |
| <span data-ttu-id="3cb85-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3cb85-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="3cb85-599">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-599">no</span></span>             | <span data-ttu-id="3cb85-600">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-600">no</span></span>           |
| <span data-ttu-id="3cb85-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="3cb85-602">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-602">no</span></span>             | <span data-ttu-id="3cb85-603">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-603">no</span></span>           |
| <span data-ttu-id="3cb85-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="3cb85-604">msdyn_progress</span></span>                         | <span data-ttu-id="3cb85-605">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-605">no</span></span>             | <span data-ttu-id="3cb85-606">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-606">no</span></span>           |
| <span data-ttu-id="3cb85-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="3cb85-608">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-608">no</span></span>             | <span data-ttu-id="3cb85-609">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-609">no</span></span>           |
| <span data-ttu-id="3cb85-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="3cb85-611">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-611">no</span></span>             | <span data-ttu-id="3cb85-612">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-612">no</span></span>           |
| <span data-ttu-id="3cb85-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="3cb85-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="3cb85-614">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-614">no</span></span>             | <span data-ttu-id="3cb85-615">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-615">no</span></span>           |
| <span data-ttu-id="3cb85-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="3cb85-617">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-617">no</span></span>             | <span data-ttu-id="3cb85-618">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-618">no</span></span>           |
| <span data-ttu-id="3cb85-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="3cb85-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="3cb85-620">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-620">no</span></span>             | <span data-ttu-id="3cb85-621">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-621">no</span></span>           |
| <span data-ttu-id="3cb85-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="3cb85-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="3cb85-623">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-623">no</span></span>             | <span data-ttu-id="3cb85-624">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-624">no</span></span>           |
| <span data-ttu-id="3cb85-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="3cb85-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="3cb85-626">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-626">no</span></span>             | <span data-ttu-id="3cb85-627">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-627">no</span></span>           |
| <span data-ttu-id="3cb85-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="3cb85-629">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-629">no</span></span>             | <span data-ttu-id="3cb85-630">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-630">no</span></span>           |
| <span data-ttu-id="3cb85-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="3cb85-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="3cb85-632">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-632">no</span></span>             | <span data-ttu-id="3cb85-633">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-633">no</span></span>           |
| <span data-ttu-id="3cb85-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="3cb85-635">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-635">no</span></span>             | <span data-ttu-id="3cb85-636">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-636">no</span></span>           |
| <span data-ttu-id="3cb85-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="3cb85-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="3cb85-638">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-638">no</span></span>             | <span data-ttu-id="3cb85-639">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-639">no</span></span>           |
| <span data-ttu-id="3cb85-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="3cb85-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="3cb85-641">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-641">no</span></span>             | <span data-ttu-id="3cb85-642">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-642">no</span></span>           |
| <span data-ttu-id="3cb85-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="3cb85-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="3cb85-644">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-644">no</span></span>             | <span data-ttu-id="3cb85-645">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-645">no</span></span>           |
| <span data-ttu-id="3cb85-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="3cb85-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="3cb85-647">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-647">no</span></span>             | <span data-ttu-id="3cb85-648">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-648">no</span></span>           |
| <span data-ttu-id="3cb85-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="3cb85-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="3cb85-650">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-650">no</span></span>             | <span data-ttu-id="3cb85-651">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-651">no</span></span>           |
| <span data-ttu-id="3cb85-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="3cb85-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="3cb85-653">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-653">no</span></span>             | <span data-ttu-id="3cb85-654">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-654">no</span></span>           |
| <span data-ttu-id="3cb85-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="3cb85-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="3cb85-656">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-656">no</span></span>             | <span data-ttu-id="3cb85-657">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-657">no</span></span>           |
| <span data-ttu-id="3cb85-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="3cb85-659">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-659">no</span></span>             | <span data-ttu-id="3cb85-660">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-660">no</span></span>           |
| <span data-ttu-id="3cb85-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="3cb85-662">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-662">no</span></span>             | <span data-ttu-id="3cb85-663">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-663">no</span></span>           |
| <span data-ttu-id="3cb85-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="3cb85-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="3cb85-665">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-665">no</span></span>             | <span data-ttu-id="3cb85-666">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-666">no</span></span>           |
| <span data-ttu-id="3cb85-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="3cb85-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="3cb85-668">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-668">no</span></span>             | <span data-ttu-id="3cb85-669">non</span><span class="sxs-lookup"><span data-stu-id="3cb85-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="3cb85-670">Limitacións e problemas coñecidos</span><span class="sxs-lookup"><span data-stu-id="3cb85-670">Limitations and known issues</span></span>
<span data-ttu-id="3cb85-671">A continuación móstrase unha lista de limitacións e problemas coñecidos:</span><span class="sxs-lookup"><span data-stu-id="3cb85-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="3cb85-672">As API de programación só poden ser empregadas por **Usuarios con licenza Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="3cb85-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="3cb85-673">Non poden ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="3cb85-673">They can't be used by:</span></span>
    - <span data-ttu-id="3cb85-674">Usuarios da aplicación</span><span class="sxs-lookup"><span data-stu-id="3cb85-674">Application users</span></span>
    - <span data-ttu-id="3cb85-675">Usuario do sistema</span><span class="sxs-lookup"><span data-stu-id="3cb85-675">System users</span></span>
    - <span data-ttu-id="3cb85-676">Usuarios de integración</span><span class="sxs-lookup"><span data-stu-id="3cb85-676">Integration users</span></span>
    - <span data-ttu-id="3cb85-677">Outros usuarios que non teñen a licenza requirida</span><span class="sxs-lookup"><span data-stu-id="3cb85-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="3cb85-678">Cada **OperationSet** só pode ter un máximo de 100 operacións.</span><span class="sxs-lookup"><span data-stu-id="3cb85-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="3cb85-679">Cada usuario só pode ter un máximo de 10 **OperationSets** abertos.</span><span class="sxs-lookup"><span data-stu-id="3cb85-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="3cb85-680">Project Operations admite actualmente un máximo de 500 tarefas totais nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="3cb85-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="3cb85-681">O estado de fallo e os rexistros de fallos de **OperationSet** non están dispoñibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="3cb85-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="3cb85-682">Límites en proxectos e tarefas</span><span class="sxs-lookup"><span data-stu-id="3cb85-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="3cb85-683">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="3cb85-683">Error handling</span></span>

   - <span data-ttu-id="3cb85-684">Para revisar os erros xerados a partir dos conxuntos de operacións, vaia a **Configuración** \> **Integración de programación** \> **Conxuntos de operacións**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="3cb85-685">Para revisar os erros xerados desde o servizo de programación de proxectos, vaia a **Configuración** \> **Integración de programación** \> **Rexistros de erros PSS**.</span><span class="sxs-lookup"><span data-stu-id="3cb85-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="3cb85-686">Escenario de exemplo</span><span class="sxs-lookup"><span data-stu-id="3cb85-686">Sample scenario</span></span>

<span data-ttu-id="3cb85-687">Neste escenario, creará un proxecto, un membro do equipo, catro tarefas e dúas atribucións de recursos.</span><span class="sxs-lookup"><span data-stu-id="3cb85-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="3cb85-688">A continuación, actualizará unha tarefa, actualizará o proxecto, eliminará unha tarefa, eliminará unha atribución de recursos e creará unha dependencia de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3cb85-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="3cb85-689">Exemplos adicionais</span><span class="sxs-lookup"><span data-stu-id="3cb85-689">Additional samples</span></span>

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
