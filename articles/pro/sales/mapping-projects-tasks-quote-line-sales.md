---
title: Asignar proxectos e tarefas a unha liña de oferta baseada en proxecto
description: Este tema ofrece información sobre como asignar proxectos e tarefas a unha liña de tarefa baseada en proxecto.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130711"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="0883c-103">Asignar proxectos e tarefas a unha liña de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="0883c-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="0883c-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="0883c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0883c-105">Nas liñas de oferta baseada en proxecto, pode asignar as tarefas específicas dun proxecto que xa está asociado a unha liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="0883c-106">Cando asigna tarefas a unha liña de oferta, os seguintes elementos que definiu na liña de oferta só se aplicarán a esas tarefas:</span><span class="sxs-lookup"><span data-stu-id="0883c-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="0883c-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="0883c-107">Billing method</span></span>
- <span data-ttu-id="0883c-108">Opcións de imputabilidade</span><span class="sxs-lookup"><span data-stu-id="0883c-108">Chargeability options</span></span>
- <span data-ttu-id="0883c-109">Límites non superables</span><span class="sxs-lookup"><span data-stu-id="0883c-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="0883c-110">Clientes</span><span class="sxs-lookup"><span data-stu-id="0883c-110">Customers</span></span>

<span data-ttu-id="0883c-111">Por exemplo, pode que teña un proxecto onde unha fase é de prezo fixo e as outras fases son de tempo e materiais.</span><span class="sxs-lookup"><span data-stu-id="0883c-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="0883c-112">Neste caso, pode asociar a primeira fase e todas as tarefas secundarias á liña de oferta desa fase cun método de facturación de prezo fixo.</span><span class="sxs-lookup"><span data-stu-id="0883c-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="0883c-113">Despois pode asociar todas as outras fases á liña de oferta baseada en tempo e materiais.</span><span class="sxs-lookup"><span data-stu-id="0883c-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="0883c-114">Asociar tarefas a liñas de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="0883c-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="0883c-115">Pode asociar tarefas con liñas de oferta desde os seguintes lugares:</span><span class="sxs-lookup"><span data-stu-id="0883c-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="0883c-116">Páxina **Proxecto** > separador **Facturación de tarefas** (óptima)</span><span class="sxs-lookup"><span data-stu-id="0883c-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="0883c-117">Páxina **Liña de oferta** > separador **Tarefas imputables**</span><span class="sxs-lookup"><span data-stu-id="0883c-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="0883c-118">Desde a páxina do proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-118">From the Project page</span></span>

<span data-ttu-id="0883c-119">A páxina **Proxecto** ofrece a experiencia óptima para asociar tarefas ás liñas de oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="0883c-120">Podes usar esta páxina para seleccionar varias tarefas e asocialas todas, ademais das tarefas secundarias, á liña de oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0883c-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="0883c-121">No separador **Xeral** dunha liña de oferta baseada en proxecto, verifique que o campo **Proxecto** está cuberto.</span><span class="sxs-lookup"><span data-stu-id="0883c-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="0883c-122">No campo **Tarefas incluídas**, seleccione **Só tarefas seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="0883c-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="0883c-123">Garde a liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-123">Save the project-based quote line.</span></span> <span data-ttu-id="0883c-124">Cando o formulario se actualiza, aparece o separador **Tarefas imputables**.</span><span class="sxs-lookup"><span data-stu-id="0883c-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="0883c-125">No separador **Xeral**, seleccione a ligazón para o proxecto desde o campo **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="0883c-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="0883c-126">Na páxina **Proxecto**, seleccione o separador **Facturación de tarefas**.</span><span class="sxs-lookup"><span data-stu-id="0883c-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="0883c-127">Na segunda grade, que se aplica á configuración de facturación específica da tarefa, seleccione unha ou máis tarefas e logo seleccione **Asociar liñas de oferta**.</span><span class="sxs-lookup"><span data-stu-id="0883c-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="0883c-128">Na páxina de diálogo que aparece, seleccione unha liña de oferta que mostre as liñas de oferta baseada en proxecto da oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="0883c-129">No campo **Tipo de facturación**, indique se estas tarefas son imputables ou non imputables.</span><span class="sxs-lookup"><span data-stu-id="0883c-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="0883c-130">Seleccione a caixa de verificación para indicar se a asociación debe incluír as tarefas secundarias das tarefas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="0883c-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="0883c-131">Ao marcar a caixa asociaranse as tarefas secundarias das tarefas seleccionadas á liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="0883c-132">Seleccione **Aceptar** para pechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0883c-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="0883c-133">Desde a páxina da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="0883c-133">From the Quote line page</span></span>

<span data-ttu-id="0883c-134">Pode asociar as tarefas do proxecto ás liñas de oferta desde o separador **Tarefas imputables** na páxina **Liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="0883c-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="0883c-135">O lugar ideal para asociar tarefas de proxecto a liñas de oferta está no separador **Facturación de tarefas** na páxina **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="0883c-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="0883c-136">Se asocia as tarefas desde o separador **Tarefas imputables** na páxina **Liña de oferta**, debe asociar manualmente cada proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="0883c-137">No separador **Xeral** dunha liña de oferta baseada en proxecto, verifique que hai un proxecto seleccionado no campo **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="0883c-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="0883c-138">No campo **Tarefas incluídas**, seleccione **Só tarefas seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="0883c-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="0883c-139">Garde a liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-139">Save the project-based quote line.</span></span> <span data-ttu-id="0883c-140">Cando o formulario se actualiza, aparece o separador **Tarefas imputables**.</span><span class="sxs-lookup"><span data-stu-id="0883c-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="0883c-141">No separador **Tarefas imputables**, seleccione **Engadir unha tarefa de liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="0883c-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="0883c-142">Na páxina **Tarefa de liña de oferta**, no campo **Tarefas**, seleccione a tarefa e no campo **Tipo de facturación**, seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="0883c-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="0883c-143">Peche a páxina.</span><span class="sxs-lookup"><span data-stu-id="0883c-143">Close the page.</span></span> <span data-ttu-id="0883c-144">A tarefa seleccionada agora está asociada á liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="0883c-145">Desvincular tarefas das liñas de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="0883c-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="0883c-146">Desde a páxina do proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-146">From the Project page</span></span>

<span data-ttu-id="0883c-147">Este método ofrece a experiencia óptima para desvincular tarefas das liñas de oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="0883c-148">Pode seleccionar varias tarefas e desvinculalas todas, ademais das tarefas secundarias, da liña de oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0883c-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="0883c-149">No separador **Xeral** dunha liña de oferta baseada en proxecto, no campo **Proxecto**, seleccione unha ligazón de proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="0883c-150">Na páxina **Proxecto**, seleccione o separador **Facturación de tarefas**.</span><span class="sxs-lookup"><span data-stu-id="0883c-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="0883c-151">Na segunda grade, que se aplica á configuración de facturación específica da tarefa, seleccione unha ou máis tarefas e logo seleccione **Desvincular liñas de oferta**.</span><span class="sxs-lookup"><span data-stu-id="0883c-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="0883c-152">Na páxina de diálogo que aparece, seleccione unha liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="0883c-153">Seleccione a caixa de verificación para indicar se a asociación debe eliminarse tamén das tarefas secundarias das tarefas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="0883c-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="0883c-154">Ao marcar a caixa tamén se desvincularán as tarefas secundarias das tarefas seleccionadas á liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="0883c-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="0883c-155">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0883c-155">Select **OK**.</span></span> <span data-ttu-id="0883c-156">Unha mensaxe de advertencia infórmalle de que se elimina esta asociación, poderíanse reverter os datos reais rexistrados previamente na tarefa.</span><span class="sxs-lookup"><span data-stu-id="0883c-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="0883c-157">Seleccione **Aceptar** para continuar e eliminar a asociación entre a tarefa e a liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="0883c-158">Desde a páxina da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="0883c-158">From the Quote line page</span></span>

<span data-ttu-id="0883c-159">Tamén pode desvincular as tarefas do proxecto das liñas de oferta desde o separador **Tarefas imputables** na páxina **Liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="0883c-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="0883c-160">No separador **Tarefas imputables**, seleccione **Eliminar unha tarefa de liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="0883c-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="0883c-161">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0883c-161">Select **OK**.</span></span> <span data-ttu-id="0883c-162">Unha mensaxe de advertencia infórmalle de que se elimina esta asociación, poderíanse reverter os datos reais rexistrados previamente na tarefa.</span><span class="sxs-lookup"><span data-stu-id="0883c-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="0883c-163">Seleccione **Aceptar** para continuar e eliminar a asociación entre a tarefa e a liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="0883c-164">Este procedemento non elimina a tarefa do proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="0883c-165">Só elimina a asociación de tarefas da liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="0883c-165">It only removes the task association from the project-based quote line.</span></span>
