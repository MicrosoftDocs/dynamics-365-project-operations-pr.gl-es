---
title: Modos de programación
description: Este tema fornece información sobre os modos de programación.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981433"
---
# <a name="scheduling-modes"></a><span data-ttu-id="4630d-103">Modos de programación</span><span class="sxs-lookup"><span data-stu-id="4630d-103">Scheduling modes</span></span>

<span data-ttu-id="4630d-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="4630d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4630d-105">Dynamics 365 Project Operations proporciona ás organizacións a capacidade de definir como xestionan os cambios das variables clave nas tarefas dentro da estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="4630d-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="4630d-106">En función das necesidades específicas da organización, os xestores de proxectos poden facer cambios no modo de programación cando se crea un proxecto.</span><span class="sxs-lookup"><span data-stu-id="4630d-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="4630d-107">Hai tres modos de programación dispoñibles en Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4630d-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="4630d-108">Duración fixa (este é o modo predefinido)</span><span class="sxs-lookup"><span data-stu-id="4630d-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="4630d-109">Traballo fixo</span><span class="sxs-lookup"><span data-stu-id="4630d-109">Fixed work</span></span>
  - <span data-ttu-id="4630d-110">Unidades fixas</span><span class="sxs-lookup"><span data-stu-id="4630d-110">Fixed units</span></span>

<span data-ttu-id="4630d-111">Os valores afectados pola definición dun modo de programación específico determínanse coa seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="4630d-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="4630d-112">Esforzo (*Traballo*) = duración x unidades</span><span class="sxs-lookup"><span data-stu-id="4630d-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="4630d-113">Cando define o modo de programación dun proxecto, está configurando un destes valores, que logo non se pode cambiar.</span><span class="sxs-lookup"><span data-stu-id="4630d-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="4630d-114">Manter este valor como unha constante dá prioridade a ese valor, que notifica ao sistema que non o cambie cando cambien os outros dous valores.</span><span class="sxs-lookup"><span data-stu-id="4630d-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="4630d-115">A seguinte táboa ofrece información sobre os efectos de seleccionar un modo específico.</span><span class="sxs-lookup"><span data-stu-id="4630d-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="4630d-116">**Nesta tarefa**</span><span class="sxs-lookup"><span data-stu-id="4630d-116">**In this task**</span></span>             | <span data-ttu-id="4630d-117">**Se revisa unidades**</span><span class="sxs-lookup"><span data-stu-id="4630d-117">**If you revise units**</span></span>   | <span data-ttu-id="4630d-118">**Se revisa duración**</span><span class="sxs-lookup"><span data-stu-id="4630d-118">**If you revise duration**</span></span> | <span data-ttu-id="4630d-119">**Se revisa esforzo**</span><span class="sxs-lookup"><span data-stu-id="4630d-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="4630d-120">Tarefa de unidades fixas</span><span class="sxs-lookup"><span data-stu-id="4630d-120">Fixed units task</span></span>     | <span data-ttu-id="4630d-121">A duración calcúlase de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-121">Duration is recalculated.</span></span> | <span data-ttu-id="4630d-122">O esforzo calcúlase de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-122">Effort is recalculated.</span></span>    | <span data-ttu-id="4630d-123">A duración calcúlase de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="4630d-124">Tarefa de esforzo fixo</span><span class="sxs-lookup"><span data-stu-id="4630d-124">Fixed effort task</span></span>    | <span data-ttu-id="4630d-125">A duración calcúlase de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-125">Duration is recalculated.</span></span> | <span data-ttu-id="4630d-126">As unidades calcúlanse de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-126">Units are recalculated.</span></span>    | <span data-ttu-id="4630d-127">A duración calcúlase de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="4630d-128">Tarefa de duración fixa</span><span class="sxs-lookup"><span data-stu-id="4630d-128">Fixed duration task</span></span>  | <span data-ttu-id="4630d-129">O esforzo calcúlase de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-129">Effort is recalculated.</span></span>   | <span data-ttu-id="4630d-130">O esforzo calcúlase de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-130">Effort is recalculated.</span></span>    | <span data-ttu-id="4630d-131">As unidades calcúlanse de novo.</span><span class="sxs-lookup"><span data-stu-id="4630d-131">Units are recalculated.</span></span>   |

<span data-ttu-id="4630d-132">Para obter máis información sobre as implicacións dun modo determinado, consulte [Cambiar o tipo de tarefa para unha programación máis precisa](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="4630d-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="4630d-133">No tema, o termo **Traballo** úsase no canto de **Esforzo**.</span><span class="sxs-lookup"><span data-stu-id="4630d-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="4630d-134">Cambiar o modo de programación da organización</span><span class="sxs-lookup"><span data-stu-id="4630d-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="4630d-135">Complete os seguintes pasos para definir o modo de programación dunha organización.</span><span class="sxs-lookup"><span data-stu-id="4630d-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="4630d-136">Vaia a **Configuración** \> **Xeral** \> **Parámetros** e, a seguir, seleccione o parámetro do proxecto.</span><span class="sxs-lookup"><span data-stu-id="4630d-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="4630d-137">Na páxina **Parámetros do proxecto**, seleccione o modo de programación predefinido para a organización e, a seguir, defina a capacidade do xestor de proxectos para anular a configuración ao crear un novo proxecto.</span><span class="sxs-lookup"><span data-stu-id="4630d-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="4630d-138">Cambiar a configuración do modo de programación nun proxecto</span><span class="sxs-lookup"><span data-stu-id="4630d-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="4630d-139">Se unha organización permite ao xestor de proxectos substituír o modo de programación predefinido, o xestor de proxectos pode facer ese cambio cando crea un novo proxecto.</span><span class="sxs-lookup"><span data-stu-id="4630d-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="4630d-140">Non obstante, despois de gardar o proxecto, o modo de programación non se pode cambiar.</span><span class="sxs-lookup"><span data-stu-id="4630d-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="4630d-141">Proxectos copiados</span><span class="sxs-lookup"><span data-stu-id="4630d-141">Copied projects</span></span>

<span data-ttu-id="4630d-142">Debido a que se crea un proxecto cando se realiza a acción de copiar proxecto, o xestor de proxectos non pode establecer o modo de programación.</span><span class="sxs-lookup"><span data-stu-id="4630d-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="4630d-143">O proxecto de destino sempre estará de xeito predefinido no modo definido a nivel organizativo.</span><span class="sxs-lookup"><span data-stu-id="4630d-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="4630d-144">Tarefas copiadas</span><span class="sxs-lookup"><span data-stu-id="4630d-144">Copied tasks</span></span>

<span data-ttu-id="4630d-145">Cando se copia unha tarefa dun proxecto a outro, a tarefa herda o modo de programación do proxecto de destino.</span><span class="sxs-lookup"><span data-stu-id="4630d-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
