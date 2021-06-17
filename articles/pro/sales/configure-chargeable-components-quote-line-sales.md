---
title: Configurar os compoñentes imputables dunha liña de oferta
description: Este tema ofrece información sobre a configuración de compoñentes imputables e non imputables nunha liña de oferta baseada en proxecto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003764"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="00a2f-103">Configurar os compoñentes imputables dunha liña de oferta</span><span class="sxs-lookup"><span data-stu-id="00a2f-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="00a2f-104">_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="00a2f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="00a2f-105">Unha liña de oferta baseada en proxecto ten o concepto de compoñentes *incluídos* e compoñentes *imputables*.</span><span class="sxs-lookup"><span data-stu-id="00a2f-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="00a2f-106">Os compoñentes incluídos están suxeitos a:</span><span class="sxs-lookup"><span data-stu-id="00a2f-106">Included components are subject to:</span></span>

  - <span data-ttu-id="00a2f-107">Método de facturación e divisións de clientes</span><span class="sxs-lookup"><span data-stu-id="00a2f-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="00a2f-108">Límites non superables</span><span class="sxs-lookup"><span data-stu-id="00a2f-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="00a2f-109">Configuración de frecuencia de facturas definida na liña de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="00a2f-110">Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="00a2f-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="00a2f-111">O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de oferta:</span><span class="sxs-lookup"><span data-stu-id="00a2f-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="00a2f-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-112">Chargeable</span></span>
  - <span data-ttu-id="00a2f-113">Non imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-113">Non-chargeable</span></span>

<span data-ttu-id="00a2f-114">Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.</span><span class="sxs-lookup"><span data-stu-id="00a2f-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="00a2f-115">A imputabilidade defínese nas tarefas dunha liña de oferta de proxecto e aplícase a todas as clases de transaccións incluídas nesa liña.</span><span class="sxs-lookup"><span data-stu-id="00a2f-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="00a2f-116">Se o campo **Incluír tarefas** dunha liña de contrato está definido como **Todo o proxecto** ou se deixa en branco, o separador **Tarefas imputables** non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="00a2f-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="00a2f-117">A imputabilidade defínese nos roles dunha liña de oferta de proxecto só se aplica á clase de transacción **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="00a2f-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="00a2f-118">Se o campo **Incluír tempo** está definido como **Non** nunha liña de oferta de proxecto, o separador **Roles imputables** non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="00a2f-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="00a2f-119">A imputabilidade defínese nas categorías de transacción dunha liña de oferta de proxecto e só se aplica á clase de transacción **Gasto**.</span><span class="sxs-lookup"><span data-stu-id="00a2f-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="00a2f-120">Se o campo **Incluír gastos** está definido como **Non** nunha liña de oferta de proxecto, o separador **Categorías imputables** non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="00a2f-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="00a2f-121">Actualizar unha tarefa de proxecto para que sexa imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="00a2f-122">Unha tarefa de proxecto pode ser imputable ou non imputable no contexto dunha liña de oferta baseada en proxecto específica, o que fai posible a seguinte configuración.</span><span class="sxs-lookup"><span data-stu-id="00a2f-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="00a2f-123">Se unha liña de oferta baseada en proxecto inclúe **Tempo** e a tarefa **T1**, a tarefa está asociada á liña de oferta como imputable.</span><span class="sxs-lookup"><span data-stu-id="00a2f-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="00a2f-124">Se hai unha segunda liña de oferta que inclúa **Gasto**, pode asociar a tarefa **T1** á liña de oferta como non imputable.</span><span class="sxs-lookup"><span data-stu-id="00a2f-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="00a2f-125">O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos rexistrados na tarefa son non imputables.</span><span class="sxs-lookup"><span data-stu-id="00a2f-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="00a2f-126">O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Tarefas da liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="00a2f-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="00a2f-127">Como alternativa, pode actualizar o tipo de facturación para unha tarefa de proxecto no campo **Tipo de facturación** na subgrade na configuración de facturación de tarefas que mostra as liñas de oferta asociadas a unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="00a2f-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="00a2f-128">Actualizar un rol para que sexa imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="00a2f-129">Un rol pode ser imputable ou non imputable no contexto dunha liña de oferta específica baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="00a2f-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="00a2f-130">O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Roles imputables**.</span><span class="sxs-lookup"><span data-stu-id="00a2f-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="00a2f-131">Actualizar unha categoría de transacción para que sexa imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="00a2f-132">Unha categoría de transacción pode ser imputable ou non imputable nunha liña de oferta específica.</span><span class="sxs-lookup"><span data-stu-id="00a2f-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="00a2f-133">O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Categorías imputables**.</span><span class="sxs-lookup"><span data-stu-id="00a2f-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="00a2f-134">Resolver a imputabiidade</span><span class="sxs-lookup"><span data-stu-id="00a2f-134">Resolve chargeability</span></span>
<span data-ttu-id="00a2f-135">Unha estimación ou dato real creado para tempo só se considerará imputable se:</span><span class="sxs-lookup"><span data-stu-id="00a2f-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="00a2f-136">**Tempo** está incluído na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="00a2f-137">**Rol** está configurado como imputable na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="00a2f-138">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="00a2f-139">Se estas tres cousas son certas, a **Tarefa** configúrase tamén como imputable.</span><span class="sxs-lookup"><span data-stu-id="00a2f-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="00a2f-140">Unha estimación ou dato real creado para gasto só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="00a2f-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="00a2f-141">**Gasto** está incluído na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="00a2f-142">**Categoría de transacción** está configurado como imputable na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="00a2f-143">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="00a2f-144">Se estas tres cousas son certas, a **Tarefa** configúrase tamén como imputable.</span><span class="sxs-lookup"><span data-stu-id="00a2f-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="00a2f-145">Unha estimación ou dato real creado para material só se considerará imputable se:</span><span class="sxs-lookup"><span data-stu-id="00a2f-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="00a2f-146">**Materiais** está incluído na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="00a2f-147">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="00a2f-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="00a2f-148">Se estas dúas cousas son certas, a **Tarefa** debería configurarse tamén como imputable.</span><span class="sxs-lookup"><span data-stu-id="00a2f-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-149">
                    <strong>Inclúe tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="00a2f-150">
                    <strong>Inclúe gasto</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="00a2f-151">
                    <strong>Inclúe materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="00a2f-152">
                    <strong>Tarefas incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-153">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-154">
                    <strong>Categoría</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-155">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="00a2f-156">
                    <strong>Impacto na imputabilidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-157">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-158">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-159">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-160">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-161">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-162">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-163">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-164">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-165">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-166">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-167">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-168">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-169">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-170">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="00a2f-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-171">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-172">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-174">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-175">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-176">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-177">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-178">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-179">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-180">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="00a2f-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-181">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-182">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-183">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-184">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-185">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-186">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-187">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-188">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-189">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-190">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="00a2f-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-191">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-192">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-193">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-194">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-195">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-196">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-197">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-198">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-199">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-200">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="00a2f-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-201">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-202">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-203">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-204">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-205">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-206">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-207">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-208">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-209">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-210">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="00a2f-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-211">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-212">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-213">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-214">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-215">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-216">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-218">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-219">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-220">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-221">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-222">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-223">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-224">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-225">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-226">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-228">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-229">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-230">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-231">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-232">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-233">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-234">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-235">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-236">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-237">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="00a2f-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-239">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-240">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-241">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-242">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-243">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-244">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-245">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-246">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-247">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="00a2f-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="00a2f-249">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-250">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-251">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-252">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-253">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-254">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-255">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-256">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-257">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-258">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="00a2f-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-260">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-261">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-262">Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-263">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-264">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-265">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="00a2f-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="00a2f-266">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="00a2f-267">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="00a2f-268">Si</span><span class="sxs-lookup"><span data-stu-id="00a2f-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="00a2f-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="00a2f-270">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="00a2f-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="00a2f-271">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="00a2f-272">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="00a2f-273">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="00a2f-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="00a2f-274">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-275">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="00a2f-276">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="00a2f-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
