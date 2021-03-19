---
title: Progreso do proxecto e consumo de custos
description: Este tema ofrece información sobre o rastrexo do progreso do proxecto e o consumo de custos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283636"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="7d436-103">Progreso do proxecto e consumo de custos</span><span class="sxs-lookup"><span data-stu-id="7d436-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7d436-104">A necesidade de rastrexar o progreso cunha programación varía segundo o sector.</span><span class="sxs-lookup"><span data-stu-id="7d436-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="7d436-105">Algúns sectores rastrexan a un nivel granular, mentres que outros sectores rastrexan a un nivel máis alto.</span><span class="sxs-lookup"><span data-stu-id="7d436-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="7d436-106">Este tema mostra como programar para cumprir os requisitos da súa organización.</span><span class="sxs-lookup"><span data-stu-id="7d436-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="7d436-107">Visualización de rastrexamento do esforzo</span><span class="sxs-lookup"><span data-stu-id="7d436-107">Effort tracking view</span></span>

<span data-ttu-id="7d436-108">A vista **Rastrexo do esforzo** rastrexa o progreso das tarefas na programación.</span><span class="sxs-lookup"><span data-stu-id="7d436-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="7d436-109">Compara as horas de esforzo real dedicadas a unha tarefa coas horas de esforzo planificadas da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="7d436-110">Project Service Automation usa as seguintes fórmulas para calcular as métricas de seguimento:</span><span class="sxs-lookup"><span data-stu-id="7d436-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="7d436-111">Inicialmente na creación da tarefa: O custo planificado establecerase segundo o custo estimado ao finalizar.</span><span class="sxs-lookup"><span data-stu-id="7d436-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="7d436-112">Unha vez rexistrados os datos reais na tarefa, o seguinte será o cálculo na vista de rastrexo do esforzo</span><span class="sxs-lookup"><span data-stu-id="7d436-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="7d436-113">Porcentaxe de progreso = Esforzo real realizado ata a data ÷ Estimación ao completar (EAC)</span><span class="sxs-lookup"><span data-stu-id="7d436-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="7d436-114">Estimación para completar (ETC) = Estimación ao completar (EAC) – Esforzo real realizado ata a data</span><span class="sxs-lookup"><span data-stu-id="7d436-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="7d436-115">EAC = Esforzo restante + Esforzo real realizado ata a data</span><span class="sxs-lookup"><span data-stu-id="7d436-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="7d436-116">Varianza de esforzo proxectado = Esforzo planificado - EAC</span><span class="sxs-lookup"><span data-stu-id="7d436-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="7d436-117">Project Service Automation mostra unha proxección da varianza de esforzo na tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="7d436-118">Se a EAC supón un esforzo superior ao previsto, proxéctase que a tarefa levará máis tempo do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7d436-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="7d436-119">Polo tanto, está atrasada.</span><span class="sxs-lookup"><span data-stu-id="7d436-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="7d436-120">Se a EAC supón un esforzo inferior ao previsto, proxéctase que a tarefa levará menos tempo do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7d436-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="7d436-121">Polo tanto, está adiantada.</span><span class="sxs-lookup"><span data-stu-id="7d436-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="7d436-122">Proxectar de novo o esforzo</span><span class="sxs-lookup"><span data-stu-id="7d436-122">Reprojecting effort</span></span>

<span data-ttu-id="7d436-123">É frecuente que un xestor de proxectos revise as estimacións orixinais dunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="7d436-124">As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="7d436-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="7d436-125">Non obstante, non recomendamos que os xestores de proxectos modifiquen os números da liña base, porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.</span><span class="sxs-lookup"><span data-stu-id="7d436-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="7d436-126">Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:</span><span class="sxs-lookup"><span data-stu-id="7d436-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="7d436-127">Anular o ETC predefinido cunha nova estimación do esforzo restante real da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="7d436-128">Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="7d436-129">Cada un destes enfoques provoca un novo cálculo do ETC, EAC e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="7d436-130">Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.</span><span class="sxs-lookup"><span data-stu-id="7d436-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="7d436-131">Nova proxección do esforzo en tarefas resumo</span><span class="sxs-lookup"><span data-stu-id="7d436-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="7d436-132">Pódese proxectar de novo o esforzo en tarefas resumo ou en tarefas contedor.</span><span class="sxs-lookup"><span data-stu-id="7d436-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="7d436-133">Independentemente de que o usuario volva proxectar empregando o esforzo restante ou a porcentaxe de progreso nas tarefas resumo, comeza o seguinte conxunto de cálculos:</span><span class="sxs-lookup"><span data-stu-id="7d436-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="7d436-134">Calcúlanse o EAC, ETC e a porcentaxe progreso da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="7d436-135">O nova EAC distribúese nas tarefas dependentes na mesma proporción que o EAC orixinal estaba na tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="7d436-136">Calcúlase o novo EAC en cada unha das tarefas individuais ata as tarefas do nó folla.</span><span class="sxs-lookup"><span data-stu-id="7d436-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="7d436-137">As tarefas dependentes afectadas ata os nós folla teñen a súa ETC e a porcentaxe de progreso calculada de novo en función do valor de EAC.</span><span class="sxs-lookup"><span data-stu-id="7d436-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="7d436-138">Isto da lugar a unha nova proxección para a varianza de esforzo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="7d436-139">Calcúlanse de novo os EAC das tarefas resumo ata o nó raíz.</span><span class="sxs-lookup"><span data-stu-id="7d436-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="7d436-140">Vista de rastrexo de custo</span><span class="sxs-lookup"><span data-stu-id="7d436-140">Cost tracking view</span></span> 

<span data-ttu-id="7d436-141">A vista **Seguimento de custos** compara o custo real que se gastou nunha tarefa co custo planificado.</span><span class="sxs-lookup"><span data-stu-id="7d436-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="7d436-142">Esta vista mostra só os custos laborais e non inclúe os custos das estimacións de gastos.</span><span class="sxs-lookup"><span data-stu-id="7d436-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="7d436-143">Project Service Automation usa as seguintes fórmulas para calcular as métricas de seguimento:</span><span class="sxs-lookup"><span data-stu-id="7d436-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="7d436-144">Cando se crea unha tarefa, o custo previsto é igual ao custo estimado ao completar.</span><span class="sxs-lookup"><span data-stu-id="7d436-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="7d436-145">Despois de rexistrar os datos reais na tarefa, o seguinte calcúlase na vista de **Rastrexo** do custo:</span><span class="sxs-lookup"><span data-stu-id="7d436-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="7d436-146">Porcentaxe do custo consumido = Custo real gastado ata a data ÷ Custo estimado ao completar para a tarefa</span><span class="sxs-lookup"><span data-stu-id="7d436-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="7d436-147">Custo para completar (CTC) = Custo estimado ao completar - Custo real gastado ata a data</span><span class="sxs-lookup"><span data-stu-id="7d436-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="7d436-148">Custo estimado ao completar = CTC + Custo real gastado ata a data</span><span class="sxs-lookup"><span data-stu-id="7d436-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="7d436-149">Variación do custo proxectado = Custo planificado – Custo estimado ao completar</span><span class="sxs-lookup"><span data-stu-id="7d436-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="7d436-150">A proxección da varianza de custo móstrase na tarefa.</span><span class="sxs-lookup"><span data-stu-id="7d436-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="7d436-151">Se o custo estimado para completar supón un esforzo superior ao custo previsto, proxéctase que a tarefa custará máis do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7d436-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="7d436-152">Polo tanto, tende a superar o orzamento.</span><span class="sxs-lookup"><span data-stu-id="7d436-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="7d436-153">Se o custo estimado ao completar é inferior ao custo previsto, proxéctase que a tarefa custará menos do que estaba previsto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="7d436-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="7d436-154">Nova proxección de custos do xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="7d436-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="7d436-155">Cando se proxecta de novo o esforzo, todos os CTC, custo estimado ao completar, porcentaxe de custo consumido e varianza de custo proxectado calcúlanse de novo na vista **Rastrexo de custos**.</span><span class="sxs-lookup"><span data-stu-id="7d436-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="7d436-156">Resumo do estado do proxecto</span><span class="sxs-lookup"><span data-stu-id="7d436-156">Project status summary</span></span>

<span data-ttu-id="7d436-157">Os datos de rastrexo nas vistas **Rastrexo do esforzo** e **Rastrexo de custos** mostran o progreso e o consumo de custos aos niveis de nó raíz do proxecto, tarefas de resumo e tarefas de nó folla.</span><span class="sxs-lookup"><span data-stu-id="7d436-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="7d436-158">A sección **Estado** de páxina **Entidade do proxecto** mostra un resumo do estado a nivel de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7d436-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="7d436-159">Campos resumo do estado</span><span class="sxs-lookup"><span data-stu-id="7d436-159">Status summary fields</span></span>

<span data-ttu-id="7d436-160">O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto.</span><span class="sxs-lookup"><span data-stu-id="7d436-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="7d436-161">Emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente.</span><span class="sxs-lookup"><span data-stu-id="7d436-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="7d436-162">O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado.</span><span class="sxs-lookup"><span data-stu-id="7d436-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="7d436-163">O campo **Estado actualizado o** non se pode editar e o valor é unha marca de tempo que indica cando se actualizou o estado por última vez.</span><span class="sxs-lookup"><span data-stu-id="7d436-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="7d436-164">Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da data de rastrexo.</span><span class="sxs-lookup"><span data-stu-id="7d436-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="7d436-165">Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, pode axustar estes campos a **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="7d436-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="7d436-166">Cando o calendario e a varianza de custos para o nó raíz son negativos, pode configuralos en **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="7d436-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]