---
title: Estimar as vendas e os custos do proxecto cando un recurso reservable ten varios roles para un proxecto
description: Este tema fornece información sobre como se poden usar dimensións de prezos para soportar prezos e custos dun recurso que cumpra múltiples funcións nun proxecto.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290987"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="052dc-103">Estimar as vendas e os custos do proxecto cando un recurso reservable ten varios roles para un proxecto</span><span class="sxs-lookup"><span data-stu-id="052dc-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="052dc-104">As empresas baseadas en proxectos adoitan ter a necesidade dun recurso para realizar múltiples funcións nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="052dc-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="052dc-105">Cada unha destas funcións podería ter un prezo e un custo diferentes, o que significa que o tempo do mesmo recurso no proxecto podería obter unha estimación financeira diferente segundo as taxas de custo e facturación de cada unha das funcións.</span><span class="sxs-lookup"><span data-stu-id="052dc-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="052dc-106">Project Service Automation permite configurar os valores no rexistro do membro do equipo para o recurso nomeado e permite diferentes anulacións en cada unha das tarefas ás que está asignado o membro do equipo.</span><span class="sxs-lookup"><span data-stu-id="052dc-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="052dc-107">O seguinte exemplo explica como a simple anulación deste valor permite que un recurso teña varios roles nun proxecto con taxas de custo e facturación diferentes.</span><span class="sxs-lookup"><span data-stu-id="052dc-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="052dc-108">Crear tarefas</span><span class="sxs-lookup"><span data-stu-id="052dc-108">Create tasks</span></span>
<span data-ttu-id="052dc-109">Cree dúas tarefas de proxecto durante 40 horas cada unha, Tarefa A e Tarefa B. Seleccione a Tarefa A como predecesora da Tarefa B.</span><span class="sxs-lookup"><span data-stu-id="052dc-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="052dc-110">Configure o rol e a unidade de organización para un membro xenérico do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="052dc-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="052dc-111">Na páxina **Programar**, seleccione a fila **Tarefa** para a Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="052dc-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="052dc-112">No campo **Recursos**, seleccione **Crear** na lista despregable.</span><span class="sxs-lookup"><span data-stu-id="052dc-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="052dc-113">No campo **Creación rápida de membro do equipo**, especifique os atributos do membro do equipo xenérico que pode realizar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="052dc-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="052dc-114">Seleccione o rol e a unidade organizativa axeitados e logo seleccione **Gardar e pechar**.</span><span class="sxs-lookup"><span data-stu-id="052dc-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="052dc-115">Créase un membro xenérico do equipo que se asigna a esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="052dc-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="052dc-116">Repita estes pasos para a Tarefa B e asegúrese de que o rol e a unidade organizativa do membro do equipo xenérico creado para a Tarefa B son diferentes dos da Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="052dc-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="052dc-117">Configure o rol e a unidade de organización para unha tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="052dc-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="052dc-118">Despois de crear a Tarefa A, seleccione a tarefa e logo seleccione **Editar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="052dc-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="052dc-119">Na páxina **Detalles da tarefa**, busque os campos **Rol** e **Unidade organizativa**, engada os valores que se requiren dun recurso que realizaría esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="052dc-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="052dc-120">Se está completando estes escenarios usando os datos de demostración de Project Service Automation, seleccione **Xefe de consultoría** para o rol, e **Fabrikam US** como unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="052dc-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="052dc-121">Seleccione a Tarefa B e, a seguir, seleccione **Editar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="052dc-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="052dc-122">Na páxina **Detalles da tarefa**, busque os campos **Rol** e **Unidade organizativa**, engada os valores que se requiren dun recurso que realizaría esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="052dc-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="052dc-123">Asegúrese de que os valores dos campos **Función** e **Unidade Organizativa** para a tarefa B sexan diferentes dos valores para a tarefa A.</span><span class="sxs-lookup"><span data-stu-id="052dc-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="052dc-124">Se está completando estes escenarios usando os datos de demostración de Project Service Automation, seleccione **Técnico de rede** para o rol, e **Fabrikam US** como unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="052dc-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="052dc-125">Garde e peche a páxina **Detalles da tarefa**.</span><span class="sxs-lookup"><span data-stu-id="052dc-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="052dc-126">Comportamento do membro do equipo e estimacións</span><span class="sxs-lookup"><span data-stu-id="052dc-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="052dc-127">Na páxina **Detalles da tarefa**, en **Membro do equipo**, seleccione os dous membros xenéricos do equipo e logo seleccione **Xerar requisitos**.</span><span class="sxs-lookup"><span data-stu-id="052dc-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="052dc-128">Selecciona a fila do membro do equipo para **Xefe de consultoría** e logo seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="052dc-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="052dc-129">Ábrese o panel de programación e reserva un recurso para ese requisito.</span><span class="sxs-lookup"><span data-stu-id="052dc-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="052dc-130">Seleccione a fila do membro do equipo para **Técnico de rede** e logo seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="052dc-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="052dc-131">Ábrese o panel de programación e reserva o mesmo recurso para ese requisito.</span><span class="sxs-lookup"><span data-stu-id="052dc-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="052dc-132">Grade de Membro do equipo</span><span class="sxs-lookup"><span data-stu-id="052dc-132">Team Member grid</span></span> 
<span data-ttu-id="052dc-133">Na grade **Membro do equipo**, observe que os dous rexistros xenéricos de membros do equipo se eliminaron e se substituíron por un recurso.</span><span class="sxs-lookup"><span data-stu-id="052dc-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="052dc-134">Hai un conxunto de valores para ese recurso que mostra un conxunto de valores predefinido para **Rol** e **Unidade organizativa**.</span><span class="sxs-lookup"><span data-stu-id="052dc-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="052dc-135">Cando amplía a fila dese rexistro de membro do equipo, pode ver distintas tarefas no rexistro de membro do equipo para ambas tarefas.</span><span class="sxs-lookup"><span data-stu-id="052dc-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="052dc-136">Cada fila de atribucións ten valores específicos da tarefa para **Rol** e **Unidade organizativa**.</span><span class="sxs-lookup"><span data-stu-id="052dc-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="052dc-137">Grade de estimacións</span><span class="sxs-lookup"><span data-stu-id="052dc-137">Estimates grid</span></span> 
<span data-ttu-id="052dc-138">Cando navegue á grade **Estimacións**, notará que as dúas atribucións para o mesmo recurso teñen un prezo diferente.</span><span class="sxs-lookup"><span data-stu-id="052dc-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="052dc-139">A atribución do recurso na Tarefa A ten un prezo empregando o valor do atributo **Rol** de **Xefe de consultoría**.</span><span class="sxs-lookup"><span data-stu-id="052dc-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="052dc-140">A atribución do mesmo recurso na Tarefa B ten un prezo empregando o valor do atributo **Rol** de **Técnico de rede**.</span><span class="sxs-lookup"><span data-stu-id="052dc-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]