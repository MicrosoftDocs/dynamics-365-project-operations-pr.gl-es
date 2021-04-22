---
title: Configurar os compoñentes imputables dunha liña de oferta
description: Este tema ofrece información sobre a configuración de compoñentes imputables e non imputables nunha liña de oferta baseada en proxecto.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858291"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="90a52-103">Configurar os compoñentes imputables dunha liña de oferta</span><span class="sxs-lookup"><span data-stu-id="90a52-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="90a52-104">_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="90a52-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="90a52-105">Unha liña de oferta baseada en proxecto ten o concepto de compoñentes *incluídos* e compoñentes *imputables*.</span><span class="sxs-lookup"><span data-stu-id="90a52-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="90a52-106">Os compoñentes incluídos están suxeitos a:</span><span class="sxs-lookup"><span data-stu-id="90a52-106">Included components are subject to:</span></span>

  - <span data-ttu-id="90a52-107">Método de facturación e divisións de clientes</span><span class="sxs-lookup"><span data-stu-id="90a52-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="90a52-108">Límites non superables</span><span class="sxs-lookup"><span data-stu-id="90a52-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="90a52-109">Configuración de frecuencia de facturas definida na liña de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="90a52-110">Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="90a52-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="90a52-111">O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de oferta:</span><span class="sxs-lookup"><span data-stu-id="90a52-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="90a52-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-112">Chargeable</span></span>
  - <span data-ttu-id="90a52-113">Non imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-113">Non-chargeable</span></span>

<span data-ttu-id="90a52-114">Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.</span><span class="sxs-lookup"><span data-stu-id="90a52-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="90a52-115">A imputabilidade defínese nas tarefas dunha liña de oferta de proxecto e aplícase a todas as clases de transaccións incluídas nesa liña.</span><span class="sxs-lookup"><span data-stu-id="90a52-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="90a52-116">Se o campo **Incluír tarefas** dunha liña de contrato está definido como **Todo o proxecto** ou se deixa en branco, o separador **Tarefas imputables** non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="90a52-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="90a52-117">A imputabilidade defínese nos roles dunha liña de oferta de proxecto só se aplica á clase de transacción **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="90a52-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="90a52-118">Se o campo **Incluír tempo** está definido como **Non** nunha liña de oferta de proxecto, o separador **Roles imputables** non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="90a52-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="90a52-119">A imputabilidade defínese nas categorías de transacción dunha liña de oferta de proxecto e só se aplica á clase de transacción **Gasto**.</span><span class="sxs-lookup"><span data-stu-id="90a52-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="90a52-120">Se o campo **Incluír gastos** está definido como **Non** nunha liña de oferta de proxecto, o separador **Categorías imputables** non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="90a52-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="90a52-121">Actualizar unha tarefa de proxecto para que sexa imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="90a52-122">Unha tarefa de proxecto pode ser imputable ou non imputable no contexto dunha liña de oferta baseada en proxecto específica, o que fai posible a seguinte configuración.</span><span class="sxs-lookup"><span data-stu-id="90a52-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="90a52-123">Se unha liña de oferta baseada en proxecto inclúe **Tempo** e a tarefa **T1**, a tarefa está asociada á liña de oferta como imputable.</span><span class="sxs-lookup"><span data-stu-id="90a52-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="90a52-124">Se hai unha segunda liña de oferta que inclúa **Gasto**, pode asociar a tarefa **T1** á liña de oferta como non imputable.</span><span class="sxs-lookup"><span data-stu-id="90a52-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="90a52-125">O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos rexistrados na tarefa son non imputables.</span><span class="sxs-lookup"><span data-stu-id="90a52-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="90a52-126">O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Tarefas da liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="90a52-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="90a52-127">Como alternativa, pode actualizar o tipo de facturación para unha tarefa de proxecto no campo **Tipo de facturación** na subgrade na configuración de facturación de tarefas que mostra as liñas de oferta asociadas a unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="90a52-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="90a52-128">Actualizar un rol para que sexa imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="90a52-129">Un rol pode ser imputable ou non imputable no contexto dunha liña de oferta específica baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="90a52-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="90a52-130">O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Roles imputables**.</span><span class="sxs-lookup"><span data-stu-id="90a52-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="90a52-131">Actualizar unha categoría de transacción para que sexa imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="90a52-132">Unha categoría de transacción pode ser imputable ou non imputable nunha liña de oferta específica.</span><span class="sxs-lookup"><span data-stu-id="90a52-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="90a52-133">O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Categorías imputables**.</span><span class="sxs-lookup"><span data-stu-id="90a52-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="90a52-134">Resolver a imputabiidade</span><span class="sxs-lookup"><span data-stu-id="90a52-134">Resolve chargeability</span></span>
<span data-ttu-id="90a52-135">Unha estimación ou dato real creado para tempo só se considerará imputable se:</span><span class="sxs-lookup"><span data-stu-id="90a52-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="90a52-136">**Tempo** está incluído na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="90a52-137">**Rol** está configurado como imputable na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="90a52-138">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="90a52-139">Se estas tres cousas son certas, a **Tarefa** configúrase tamén como imputable.</span><span class="sxs-lookup"><span data-stu-id="90a52-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="90a52-140">Unha estimación ou dato real creado para gasto só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="90a52-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="90a52-141">**Gasto** está incluído na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="90a52-142">**Categoría de transacción** está configurado como imputable na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="90a52-143">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="90a52-144">Se estas tres cousas son certas, a **Tarefa** configúrase tamén como imputable.</span><span class="sxs-lookup"><span data-stu-id="90a52-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="90a52-145">Unha estimación ou dato real creado para material só se considerará imputable se:</span><span class="sxs-lookup"><span data-stu-id="90a52-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="90a52-146">**Materiais** está incluído na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="90a52-147">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="90a52-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="90a52-148">Se estas dúas cousas son certas, a **Tarefa** debería configurarse tamén como imputable.</span><span class="sxs-lookup"><span data-stu-id="90a52-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-149">
                    <strong>Inclúe tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="90a52-150">
                    <strong>Inclúe gasto</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="90a52-151">
                    <strong>Inclúe materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="90a52-152">
                    <strong>Tarefas incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-153">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-154">
                    <strong>Categoría</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-155">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="90a52-156">
                    <strong>Impacto na imputabilidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-157">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-158">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-159">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-160">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-161">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-162">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-163">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-164">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-165">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-166">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-167">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-168">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-169">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-170">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="90a52-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-171">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-172">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-174">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-175">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-176">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-177">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-178">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-179">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-180">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="90a52-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-181">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-182">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-183">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-184">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-185">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-186">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-187">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-188">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-189">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-190">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="90a52-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-191">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-192">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-193">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-194">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-195">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-196">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-197">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-198">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-199">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-200">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="90a52-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-201">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-202">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-203">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-204">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-205">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-206">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-207">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-208">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-209">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-210">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="90a52-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-211">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-212">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-213">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-214">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-215">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-216">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-218">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-219">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-220">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-221">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-222">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-223">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-224">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-225">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-226">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-228">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-229">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-230">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-231">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-232">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-233">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-234">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-235">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-236">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-237">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="90a52-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-239">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-240">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-241">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-242">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-243">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-244">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-245">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-246">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-247">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="90a52-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90a52-249">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-250">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-251">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-252">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-253">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-254">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-255">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-256">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-257">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-258">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="90a52-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-260">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-261">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-262">Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-263">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-264">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-265">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="90a52-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90a52-266">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90a52-267">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90a52-268">Si</span><span class="sxs-lookup"><span data-stu-id="90a52-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="90a52-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90a52-270">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="90a52-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90a52-271">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90a52-272">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90a52-273">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="90a52-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90a52-274">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-275">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="90a52-276">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90a52-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
