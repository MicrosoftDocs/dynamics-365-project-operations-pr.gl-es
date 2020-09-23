---
title: Progreso do proxecto e consumo de custos
description: Este tema ofrece información sobre como rastrexar o progreso do proxecto e o consumo de custos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751444"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="7295f-103">Progreso do proxecto e consumo de custos</span><span class="sxs-lookup"><span data-stu-id="7295f-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7295f-104">A necesidade de rastrexar o progreso cunha programación varía segundo o sector.</span><span class="sxs-lookup"><span data-stu-id="7295f-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="7295f-105">Algúns sectores rastrexan a un nivel granular, mentres que outros sectores rastrexan a un nivel máis alto.</span><span class="sxs-lookup"><span data-stu-id="7295f-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="7295f-106">Este tema mostra como programar para cumprir os requisitos da súa organización.</span><span class="sxs-lookup"><span data-stu-id="7295f-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="7295f-107">Visualización de rastrexamento do esforzo</span><span class="sxs-lookup"><span data-stu-id="7295f-107">Effort tracking view</span></span>

<span data-ttu-id="7295f-108">A vista **Rastrexo do esforzo** rastrexa o progreso das tarefas na programación.</span><span class="sxs-lookup"><span data-stu-id="7295f-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="7295f-109">Compara as horas de esforzo real dedicadas a unha tarefa coas horas de esforzo planificadas para esa tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="7295f-110">PSA usa as seguintes fórmulas para calcular as métricas de seguimento:</span><span class="sxs-lookup"><span data-stu-id="7295f-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="7295f-111">Porcentaxe de progreso = Esforzo real realizado ata a data ÷ Esforzo planificado para a tarefa</span><span class="sxs-lookup"><span data-stu-id="7295f-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="7295f-112">Estimación para completar (ETC) = Esforzo previsto - Esforzo real realizado ata a data</span><span class="sxs-lookup"><span data-stu-id="7295f-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="7295f-113">Estimación ao completar (EAC) = Esforzo restante - Esforzo real realizado ata a data</span><span class="sxs-lookup"><span data-stu-id="7295f-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="7295f-114">Varianza de esforzo proxectado = Esforzo planificado - EAC</span><span class="sxs-lookup"><span data-stu-id="7295f-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="7295f-115">PSA mostra unha proxección da varianza de esforzo na tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="7295f-116">Se a EAC supón un esforzo superior ao previsto, proxéctase que a tarefa levará máis tempo do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7295f-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="7295f-117">Polo tanto, está atrasada.</span><span class="sxs-lookup"><span data-stu-id="7295f-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="7295f-118">Se a EAC supón un esforzo inferior ao previsto, proxéctase que a tarefa levará menos tempo do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7295f-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="7295f-119">Polo tanto, está adiantada.</span><span class="sxs-lookup"><span data-stu-id="7295f-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="7295f-120">Proxectar de novo o esforzo</span><span class="sxs-lookup"><span data-stu-id="7295f-120">Re-projecting effort</span></span>

<span data-ttu-id="7295f-121">É frecuente que un xestor de proxectos revise as estimacións orixinais dunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="7295f-122">As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="7295f-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="7295f-123">Non obstante, non recomendamos que os xestores de proxectos modifiquen os números da liña base, porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.</span><span class="sxs-lookup"><span data-stu-id="7295f-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="7295f-124">Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:</span><span class="sxs-lookup"><span data-stu-id="7295f-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="7295f-125">Anular o ETC predefinido cunha nova estimación do esforzo restante real da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="7295f-126">Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="7295f-127">Cada un destes enfoques provoca un novo cálculo do ETC, EAC e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="7295f-128">Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.</span><span class="sxs-lookup"><span data-stu-id="7295f-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="7295f-129">Nova proxección do esforzo en tarefas resumo</span><span class="sxs-lookup"><span data-stu-id="7295f-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="7295f-130">Pódese proxectar de novo o esforzo en tarefas resumo ou en tarefas contedor.</span><span class="sxs-lookup"><span data-stu-id="7295f-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="7295f-131">Independentemente de que o usuario volva proxectar empregando o esforzo restante ou a porcentaxe de progreso nas tarefas resumo, comeza o seguinte conxunto de cálculos:</span><span class="sxs-lookup"><span data-stu-id="7295f-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="7295f-132">Calcúlanse o EAC, ETC e a porcentaxe progreso da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="7295f-133">O nova EAC distribúese nas tarefas dependentes na mesma proporción que o EAC orixinal estaba na tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="7295f-134">Calcúlase o novo EAC en cada unha das tarefas individuais ata as tarefas do nó folla.</span><span class="sxs-lookup"><span data-stu-id="7295f-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="7295f-135">As tarefas dependentes afectadas ata os nós folla teñen a súa ETC e a porcentaxe de progreso calculada de novo en función do valor de EAC.</span><span class="sxs-lookup"><span data-stu-id="7295f-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="7295f-136">Isto da lugar a unha nova proxección para a varianza de esforzo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="7295f-137">Calcúlanse de novo os EAC das tarefas resumo ata o nó raíz.</span><span class="sxs-lookup"><span data-stu-id="7295f-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="7295f-138">Vista de rastrexo de custo</span><span class="sxs-lookup"><span data-stu-id="7295f-138">Cost tracking view</span></span> 

<span data-ttu-id="7295f-139">A vista **Seguimento de custos** compara o custo real que se gastou nunha tarefa co custo planificado dunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="7295f-140">Esta vista mostra só os custos laborais e non inclúe os custos das estimacións de gastos.</span><span class="sxs-lookup"><span data-stu-id="7295f-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="7295f-141">PSA usa as seguintes fórmulas para calcular as métricas de seguimento:</span><span class="sxs-lookup"><span data-stu-id="7295f-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="7295f-142">Porcentaxe do custo consumido = Custo real gastado ata a data ÷ Custo planificado para a tarefa</span><span class="sxs-lookup"><span data-stu-id="7295f-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="7295f-143">Custo para completar (CTC) = Custo planificado - Custo real gastado ata a data</span><span class="sxs-lookup"><span data-stu-id="7295f-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="7295f-144">EAC = CTC + Custo real gastado ata a data</span><span class="sxs-lookup"><span data-stu-id="7295f-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="7295f-145">Varianza do custo proxectado = Custo planificado - EAC</span><span class="sxs-lookup"><span data-stu-id="7295f-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="7295f-146">A proxección da varianza de custo móstrase na tarefa.</span><span class="sxs-lookup"><span data-stu-id="7295f-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="7295f-147">Se o EAC supón un esforzo superior ao custo previsto, proxéctase que a tarefa custará máis do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7295f-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="7295f-148">Polo tanto, tende a superar o orzamento.</span><span class="sxs-lookup"><span data-stu-id="7295f-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="7295f-149">Se o EAC supón un esforzo inferior ao custo previsto, proxéctase que a tarefa custará menos do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7295f-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="7295f-150">Polo tanto, tende a estar por debaixo do orzamento.</span><span class="sxs-lookup"><span data-stu-id="7295f-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="7295f-151">Nova proxección de custos do xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="7295f-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="7295f-152">Cando se proxecta de novo o esforzo, todos os CTC, EAC, porcentaxe de custo consumido e varianza de custo proxectado calcúlanse de novo na vista **Rastrexo de custos**.</span><span class="sxs-lookup"><span data-stu-id="7295f-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="7295f-153">Resumo do estado do proxecto</span><span class="sxs-lookup"><span data-stu-id="7295f-153">Project status summary</span></span>

<span data-ttu-id="7295f-154">Os datos de rastrexo nas vistas **Rastrexo do esforzo** e **Rastrexo de custos** mostran o progreso e o consumo de custos aos niveis de nó raíz do proxecto, tarefas de resumo e tarefas de nó folla.</span><span class="sxs-lookup"><span data-stu-id="7295f-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="7295f-155">A sección **Estado** de páxina **Entidade do proxecto** mostra un resumo do estado a nivel de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7295f-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="7295f-156">Campos resumo do estado</span><span class="sxs-lookup"><span data-stu-id="7295f-156">Status summary fields</span></span>

<span data-ttu-id="7295f-157">O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto.</span><span class="sxs-lookup"><span data-stu-id="7295f-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="7295f-158">Emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente.</span><span class="sxs-lookup"><span data-stu-id="7295f-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="7295f-159">O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado.</span><span class="sxs-lookup"><span data-stu-id="7295f-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="7295f-160">O campo **Estado actualizado o** non se pode editar e o valor é unha marca de tempo que indica cando se actualizou o estado por última vez.</span><span class="sxs-lookup"><span data-stu-id="7295f-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="7295f-161">Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da data de rastrexo.</span><span class="sxs-lookup"><span data-stu-id="7295f-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="7295f-162">Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, pode axustar estes campos a **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="7295f-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="7295f-163">Cando o calendario e a varianza de custos para o nó raíz son negativos, pode configuralos en **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="7295f-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
