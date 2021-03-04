---
title: Atribuír un recurso a unha tarefa
description: Este tema fornece información sobre como atribuír recursos a tarefas.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149991"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="40f64-103">Atribuír un recurso a unha tarefa</span><span class="sxs-lookup"><span data-stu-id="40f64-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="40f64-104">Hai tres formas de atribuír un recurso a unha tarefa en Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="40f64-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="40f64-105">Reservar un recurso como un membro do equipo e, a seguir, atribuír o recurso a unha tarefa</span><span class="sxs-lookup"><span data-stu-id="40f64-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="40f64-106">Pode engadir un recurso ao equipo de proxecto e, a seguir, atribuír o recurso ás tarefas na programación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="40f64-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="40f64-107">No separador **Membro do equipo**, engada un novo membro do equipo seleccionando **Novo**.</span><span class="sxs-lookup"><span data-stu-id="40f64-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="40f64-108">Iso abre o panel **Creación rápida de membro do equipo**, onde pode seleccionar o nome do recurso reservable e defina un rol.</span><span class="sxs-lookup"><span data-stu-id="40f64-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="40f64-109">Seleccione un dos seguintes métodos de atribución para a reserva do recurso:</span><span class="sxs-lookup"><span data-stu-id="40f64-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="40f64-110">**Capacidade completa** reserva a capacidade completa do recurso para as datas desde e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="40f64-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="40f64-111">**Capacidade da porcentaxe** reserva unha porcentaxe da capacidade do recurso para as datas desde e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="40f64-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="40f64-112">**Distribuír uniformemente por horas** reserva o recurso para un número de horas especificado, e distribúe o tempo de forma similar por día sobre as datas desde e ata especificadas.</span><span class="sxs-lookup"><span data-stu-id="40f64-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="40f64-113">**Por horas: carga frontal** reserva o recurso para un número de horas especificado, con carga frontal das horas por día sobre as datas desde e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="40f64-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="40f64-114">**Ningún** engade o recurso ao equipo, pero non crea ningunha reserva que absorba a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="40f64-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="40f64-115">Na grade de **Programación** para unha tarefa, seleccione a icona de **Recurso** na cela de recursos e, a seguir, baixo **Membros do equipo**, seleccione o membro do equipo que acaba de engadir.</span><span class="sxs-lookup"><span data-stu-id="40f64-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="40f64-116">Nos separadores **Membro do equipo** e **Conciliación**, o recurso mostra as horas reservadas e as horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="40f64-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="40f64-117">As horas deberían ser as mesmas, pero non é necesario, xa que as reservas e as atribucións non están totalmente emparelladas.</span><span class="sxs-lookup"><span data-stu-id="40f64-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="40f64-118">O separador **Conciliación** ofrece detalles cando son diferentes, como por exemplo se atribúe a un recurso máis horas de traballo das que ten reservadas.</span><span class="sxs-lookup"><span data-stu-id="40f64-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="40f64-119">Se é necesario, pode corrixir a información, ben estendendo as reservas do recurso ou modificando a atribución.</span><span class="sxs-lookup"><span data-stu-id="40f64-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="40f64-120">Crear un membro do equipo xenérico a través da atribución de tarefas</span><span class="sxs-lookup"><span data-stu-id="40f64-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="40f64-121">Cando cree un membro de equipo xenérico a través da atribución de tarefas, ten que crear un marcador de posición ou recurso xenérico que describa as características do recurso denominado coas tarefas nas que vostede desexa que traballe.</span><span class="sxs-lookup"><span data-stu-id="40f64-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="40f64-122">A seguir, pode xerar un requisito (ou enviar unha solicitude utilizando o requisito) que se utiliza para buscar e reservar o recurso denominado.</span><span class="sxs-lookup"><span data-stu-id="40f64-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="40f64-123">Na grade **Programación** para unha tarefa, seleccione a icona de **Recurso** na cela do recurso.</span><span class="sxs-lookup"><span data-stu-id="40f64-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="40f64-124">Escriba un nome que sirva como nome do recurso marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="40f64-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="40f64-125">Por exemplo, Xestor de programa.</span><span class="sxs-lookup"><span data-stu-id="40f64-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="40f64-126">Seleccione **Crear** e, no campo **Creación rápida de membro do equipo** de proxecto á dereita, defina o rol para o recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="40f64-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="40f64-127">Pode seguir atribuíndo tarefas a este recurso de marcador de posición seleccionando o recurso no **Selector de recursos** para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="40f64-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="40f64-128">Aparecen en **Membros do equipo**.</span><span class="sxs-lookup"><span data-stu-id="40f64-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="40f64-129">Cando termine a atribución do recurso xenérico, seleccione o recurso xenérico no separador **Equipo** e, a seguir, seleccione **Xerar requisito** para crear un requisito de recurso para o recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="40f64-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="40f64-130">Seleccione **Reservar** para o recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="40f64-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="40f64-131">Despois pode usar o panel de programación para buscar e reservar un recurso real.</span><span class="sxs-lookup"><span data-stu-id="40f64-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="40f64-132">Tamén pode enviar o requisito para conclusión por un xestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="40f64-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="40f64-133">Cando o recurso xenérico cumple cun recurso denominado, o recurso xenérico elimínase do equipo e as atribucións de tarefa para o recurso xenérico atribúense ao recurso denominado que cumplíu o requisitos de recurso do recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="40f64-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="40f64-134">Atribuír un recurso denominado da lista de todos os recursos que se poden reservar.</span><span class="sxs-lookup"><span data-stu-id="40f64-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="40f64-135">Pode utilizar a caixa de busca no **Selector de recursos** para buscar todos os recursos que se poden reservar en Project Service e atribuílos a unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="40f64-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="40f64-136">Os recursos atribuídos deste xeito engádense ao equipo sen reservas.</span><span class="sxs-lookup"><span data-stu-id="40f64-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="40f64-137">Isto é similar a engadir un membro do equipo e seleccionar Ningún como método de asignación.</span><span class="sxs-lookup"><span data-stu-id="40f64-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="40f64-138">O recurso móstrase nos separadores **Equipo** e **Conciliación** como recursos co só atribucións e sen reserva.</span><span class="sxs-lookup"><span data-stu-id="40f64-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="40f64-139">Reservaos se desexas utilizar a súa dispoñibilidade.</span><span class="sxs-lookup"><span data-stu-id="40f64-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="40f64-140">Na grade **Programación** para unha tarefa, seleccione a icona de **Recurso** na cela do recurso.</span><span class="sxs-lookup"><span data-stu-id="40f64-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="40f64-141">Comece a escribir un nome.</span><span class="sxs-lookup"><span data-stu-id="40f64-141">Start typing a name.</span></span> <span data-ttu-id="40f64-142">Os resultados de busca para o nome móstranse no **Selector de recursos** en **Outros recursos**.</span><span class="sxs-lookup"><span data-stu-id="40f64-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="40f64-143">Seleccione o recurso que desexa atribuír á tarefa.</span><span class="sxs-lookup"><span data-stu-id="40f64-143">Select the resource that you want to assign to the task.</span></span>

