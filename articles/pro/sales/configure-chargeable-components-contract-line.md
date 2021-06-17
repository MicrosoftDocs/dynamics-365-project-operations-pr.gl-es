---
title: Configurar compoñentes imputables dunha liña de contrato baseado en proxecto
description: Este tema ofrece información sobre como engadir compoñentes imputables a liñas de contrato en Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003719"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="ddf63-103">Configurar compoñentes imputables dunha liña de contrato baseado en proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="ddf63-104">_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="ddf63-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ddf63-105">Unha liña de contrato baseado en proxecto ten compoñentes *incluídos* e compoñentes *imputables*.</span><span class="sxs-lookup"><span data-stu-id="ddf63-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="ddf63-106">Os compoñentes incluídos son compoñentes suxeitos a:</span><span class="sxs-lookup"><span data-stu-id="ddf63-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="ddf63-107">Método de facturación e divisións de clientes</span><span class="sxs-lookup"><span data-stu-id="ddf63-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="ddf63-108">Límites non superables</span><span class="sxs-lookup"><span data-stu-id="ddf63-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="ddf63-109">Configuración de frecuencia de facturas definida na liña de contrato baseado en proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="ddf63-110">Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="ddf63-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="ddf63-111">O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de contrato:</span><span class="sxs-lookup"><span data-stu-id="ddf63-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="ddf63-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-112">Chargeable</span></span>
  - <span data-ttu-id="ddf63-113">Non imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-113">Non-chargeable</span></span>

<span data-ttu-id="ddf63-114">Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.</span><span class="sxs-lookup"><span data-stu-id="ddf63-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="ddf63-115">A imputabilidade defínese nas tarefas dunha liña de contrato de proxecto e aplícase a todas as clases de transaccións incluídas na liña.</span><span class="sxs-lookup"><span data-stu-id="ddf63-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="ddf63-116">Se o campo **Incluír tarefas** dunha liña de contrato está en branco ou definido como **Todo o proxecto**, o separador **Tarefas imputables** non estará dispoñible.</span><span class="sxs-lookup"><span data-stu-id="ddf63-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="ddf63-117">A imputabilidade definida nos roles dunha liña de contrato de proxecto só se aplica á clase de transacción **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="ddf63-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="ddf63-118">Se o campo **Incluír tempo** dunha liña de contrato está en branco ou definido como **Non**, o separador **Roles imputables** non estará dispoñible.</span><span class="sxs-lookup"><span data-stu-id="ddf63-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="ddf63-119">A imputabilidade definida nas categorías de transacción dunha liña de contrato de proxecto só se aplica á clase de transacción **Gasto**.</span><span class="sxs-lookup"><span data-stu-id="ddf63-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="ddf63-120">Se o campo **Incluír gastos** dunha liña de contrato está en branco ou definido como **Non**, o separador **Categorías imputables** non estará dispoñible.</span><span class="sxs-lookup"><span data-stu-id="ddf63-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ddf63-121">Actualizar unha tarefa do proxecto como imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="ddf63-122">Unha tarefa de proxecto pode ser imputable ou non imputable nunha liña de contrato específica, o que fai posible a seguinte configuración:</span><span class="sxs-lookup"><span data-stu-id="ddf63-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="ddf63-123">Se inclúe unha liña de contrato baseado en proxecto inclúe **Tempo** e unha tarefa determinada, **T1** asóciase a ela como imputable.</span><span class="sxs-lookup"><span data-stu-id="ddf63-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="ddf63-124">Se hai unha segunda liña de contrato que inclúa **Gasto**, pode asociar a tarefa T1 á liña de contrato como non imputable.</span><span class="sxs-lookup"><span data-stu-id="ddf63-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="ddf63-125">O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos son non imputables.</span><span class="sxs-lookup"><span data-stu-id="ddf63-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="ddf63-126">O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** da liña de contrato actualizando o campo **Tipo de facturación** na subgrade de tarefas da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ddf63-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="ddf63-127">Como alternativa, pode actualizar o campo **Tipo de facturación** na subgrade da tarefa Configuración de facturación dun proxecto que mostra as liñas de contrato asociadas a unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="ddf63-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ddf63-128">Actualizar un rol do proxecto como imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="ddf63-129">Un rol pode ser imputable ou non imputable nunha liña de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="ddf63-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ddf63-130">O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ddf63-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="ddf63-131">Para iso, actualice o campo **Tipo de facturación** na subgrade **Roles imputables**.</span><span class="sxs-lookup"><span data-stu-id="ddf63-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ddf63-132">Actualizar unha categoría de transacción como imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="ddf63-133">Unha categoría de transacción pode ser imputable ou non imputable nunha liña de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="ddf63-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ddf63-134">O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de contrato baseado en proxecto.</span><span class="sxs-lookup"><span data-stu-id="ddf63-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="ddf63-135">Para iso, actualice o campo **Tipo de facturación** na subgrade **Categorías imputables**.</span><span class="sxs-lookup"><span data-stu-id="ddf63-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="ddf63-136">Resolver a imputabiidade</span><span class="sxs-lookup"><span data-stu-id="ddf63-136">Resolve chargeability</span></span>

<span data-ttu-id="ddf63-137">Unha estimación ou dato real creado para tempo só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="ddf63-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="ddf63-138">**Tempo** está incluído na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ddf63-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="ddf63-139">**Rol** está configurado como imputable na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ddf63-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="ddf63-140">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña do contrato.</span><span class="sxs-lookup"><span data-stu-id="ddf63-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="ddf63-141">Se estas tres cousas son certas, a tarefa configúrase como imputable.</span><span class="sxs-lookup"><span data-stu-id="ddf63-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="ddf63-142">Unha estimación ou dato real creado para gasto só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="ddf63-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="ddf63-143">**Gasto** está incluído na liña de contrato</span><span class="sxs-lookup"><span data-stu-id="ddf63-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="ddf63-144">**Categoría de transacción** está configurado como imputable na liña de contrato</span><span class="sxs-lookup"><span data-stu-id="ddf63-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="ddf63-145">**Tarefas incluídas** está establecido como **Tarefa seleccionada** na liña do contrato.</span><span class="sxs-lookup"><span data-stu-id="ddf63-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="ddf63-146">Se estas tres cousas son certas, a **Tarefa** configúrase como imputable.</span><span class="sxs-lookup"><span data-stu-id="ddf63-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="ddf63-147">Unha estimación ou dato real creado para material só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="ddf63-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="ddf63-148">**Materiais** está incluído na liña de contrato</span><span class="sxs-lookup"><span data-stu-id="ddf63-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="ddf63-149">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña do contrato</span><span class="sxs-lookup"><span data-stu-id="ddf63-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="ddf63-150">Se estas dous cousas son certas, a **Tarefa** configúrase como imputable.</span><span class="sxs-lookup"><span data-stu-id="ddf63-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-151">
                    <strong>Inclúe tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ddf63-152">
                    <strong>Inclúe gasto</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ddf63-153">
                    <strong>Inclúe materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="ddf63-154">
                    <strong>Tarefas incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-155">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-156">
                    <strong>Categoría</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-157">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="ddf63-158">
                    <strong>Impacto na imputabilidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-159">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-160">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-161">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-162">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-163">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-164">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-165">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-166">Facturación nun dato real de tempo: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-167">Tipo de facturación no dato real de gasto: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-168">Tipo de facturación no dato real de material: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-169">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-170">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-171">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-172">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ddf63-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-174">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-175">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-176">Facturación nun dato real de tempo: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-177">Tipo de facturación no dato real de gasto: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-178">Tipo de facturación no dato real de material: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-179">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-180">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-181">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-182">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ddf63-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-183">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-184">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-185">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-186">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-187">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ddf63-188">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-189">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-190">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-191">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-192">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ddf63-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-193">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-194">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-195">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-196">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-197">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-198">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-199">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-200">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-201">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-202">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ddf63-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-203">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-204">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-205">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-206">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-207">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-208">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-209">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-210">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-211">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-212">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ddf63-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-213">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-214">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-215">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-216">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-217">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-218">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-220">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-221">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-222">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-223">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-224">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-225">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-226">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-227">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ddf63-228">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-230">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-231">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-232">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-233">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-234">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-235">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-236">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-237">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-238">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-239">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ddf63-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-241">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-242">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-243">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-244">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-245">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-246">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ddf63-247">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-248">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-249">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ddf63-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ddf63-251">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-252">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-253">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-254">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-255">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-256">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-257">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-258">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-259">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-260">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ddf63-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-262">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-263">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-264">Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-265">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-266">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ddf63-267">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="ddf63-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ddf63-268">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ddf63-269">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ddf63-270">Si</span><span class="sxs-lookup"><span data-stu-id="ddf63-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ddf63-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ddf63-272">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ddf63-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ddf63-273">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ddf63-274">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ddf63-275">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ddf63-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ddf63-276">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-277">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ddf63-278">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ddf63-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
