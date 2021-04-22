---
title: Configurar compoñentes imputables dunha liña de contrato baseado en proxecto
description: Este tema ofrece información sobre como engadir compoñentes imputables a liñas de contrato en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858471"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="ef73d-103">Configurar compoñentes imputables dunha liña de contrato baseado en proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="ef73d-104">_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="ef73d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ef73d-105">Unha liña de contrato baseado en proxecto ten compoñentes *incluídos* e compoñentes *imputables*.</span><span class="sxs-lookup"><span data-stu-id="ef73d-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="ef73d-106">Os compoñentes incluídos son compoñentes suxeitos a:</span><span class="sxs-lookup"><span data-stu-id="ef73d-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="ef73d-107">Método de facturación e divisións de clientes</span><span class="sxs-lookup"><span data-stu-id="ef73d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="ef73d-108">Límites non superables</span><span class="sxs-lookup"><span data-stu-id="ef73d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="ef73d-109">Configuración de frecuencia de facturas definida na liña de contrato baseado en proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="ef73d-110">Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="ef73d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="ef73d-111">O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de contrato:</span><span class="sxs-lookup"><span data-stu-id="ef73d-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="ef73d-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-112">Chargeable</span></span>
  - <span data-ttu-id="ef73d-113">Non imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-113">Non-chargeable</span></span>

<span data-ttu-id="ef73d-114">Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.</span><span class="sxs-lookup"><span data-stu-id="ef73d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="ef73d-115">A imputabilidade defínese nas tarefas dunha liña de contrato de proxecto e aplícase a todas as clases de transaccións incluídas na liña.</span><span class="sxs-lookup"><span data-stu-id="ef73d-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="ef73d-116">Se o campo **Incluír tarefas** dunha liña de contrato está en branco ou definido como **Todo o proxecto**, o separador **Tarefas imputables** non estará dispoñible.</span><span class="sxs-lookup"><span data-stu-id="ef73d-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="ef73d-117">A imputabilidade definida nos roles dunha liña de contrato de proxecto só se aplica á clase de transacción **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="ef73d-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="ef73d-118">Se o campo **Incluír tempo** dunha liña de contrato está en branco ou definido como **Non**, o separador **Roles imputables** non estará dispoñible.</span><span class="sxs-lookup"><span data-stu-id="ef73d-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="ef73d-119">A imputabilidade definida nas categorías de transacción dunha liña de contrato de proxecto só se aplica á clase de transacción **Gasto**.</span><span class="sxs-lookup"><span data-stu-id="ef73d-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="ef73d-120">Se o campo **Incluír gastos** dunha liña de contrato está en branco ou definido como **Non**, o separador **Categorías imputables** non estará dispoñible.</span><span class="sxs-lookup"><span data-stu-id="ef73d-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ef73d-121">Actualizar unha tarefa do proxecto como imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="ef73d-122">Unha tarefa de proxecto pode ser imputable ou non imputable nunha liña de contrato específica, o que fai posible a seguinte configuración:</span><span class="sxs-lookup"><span data-stu-id="ef73d-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="ef73d-123">Se inclúe unha liña de contrato baseado en proxecto inclúe **Tempo** e unha tarefa determinada, **T1** asóciase a ela como imputable.</span><span class="sxs-lookup"><span data-stu-id="ef73d-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="ef73d-124">Se hai unha segunda liña de contrato que inclúa **Gasto**, pode asociar a tarefa T1 á liña de contrato como non imputable.</span><span class="sxs-lookup"><span data-stu-id="ef73d-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="ef73d-125">O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos son non imputables.</span><span class="sxs-lookup"><span data-stu-id="ef73d-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="ef73d-126">O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** da liña de contrato actualizando o campo **Tipo de facturación** na subgrade de tarefas da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ef73d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="ef73d-127">Como alternativa, pode actualizar o campo **Tipo de facturación** na subgrade da tarefa Configuración de facturación dun proxecto que mostra as liñas de contrato asociadas a unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="ef73d-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ef73d-128">Actualizar un rol do proxecto como imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="ef73d-129">Un rol pode ser imputable ou non imputable nunha liña de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="ef73d-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ef73d-130">O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ef73d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="ef73d-131">Para iso, actualice o campo **Tipo de facturación** na subgrade **Roles imputables**.</span><span class="sxs-lookup"><span data-stu-id="ef73d-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ef73d-132">Actualizar unha categoría de transacción como imputable ou non imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="ef73d-133">Unha categoría de transacción pode ser imputable ou non imputable nunha liña de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="ef73d-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ef73d-134">O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de contrato baseado en proxecto.</span><span class="sxs-lookup"><span data-stu-id="ef73d-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="ef73d-135">Para iso, actualice o campo **Tipo de facturación** na subgrade **Categorías imputables**.</span><span class="sxs-lookup"><span data-stu-id="ef73d-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="ef73d-136">Resolver a imputabiidade</span><span class="sxs-lookup"><span data-stu-id="ef73d-136">Resolve chargeability</span></span>

<span data-ttu-id="ef73d-137">Unha estimación ou dato real creado para tempo só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="ef73d-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="ef73d-138">**Tempo** está incluído na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ef73d-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="ef73d-139">**Rol** está configurado como imputable na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ef73d-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="ef73d-140">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña do contrato.</span><span class="sxs-lookup"><span data-stu-id="ef73d-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="ef73d-141">Se estas tres cousas son certas, a tarefa configúrase como imputable.</span><span class="sxs-lookup"><span data-stu-id="ef73d-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="ef73d-142">Unha estimación ou dato real creado para gasto só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="ef73d-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="ef73d-143">**Gasto** está incluído na liña de contrato</span><span class="sxs-lookup"><span data-stu-id="ef73d-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="ef73d-144">**Categoría de transacción** está configurado como imputable na liña de contrato</span><span class="sxs-lookup"><span data-stu-id="ef73d-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="ef73d-145">**Tarefas incluídas** está establecido como **Tarefa seleccionada** na liña do contrato.</span><span class="sxs-lookup"><span data-stu-id="ef73d-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="ef73d-146">Se estas tres cousas son certas, a **Tarefa** configúrase como imputable.</span><span class="sxs-lookup"><span data-stu-id="ef73d-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="ef73d-147">Unha estimación ou dato real creado para material só se considera imputable se:</span><span class="sxs-lookup"><span data-stu-id="ef73d-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="ef73d-148">**Materiais** está incluído na liña de contrato</span><span class="sxs-lookup"><span data-stu-id="ef73d-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="ef73d-149">**Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña do contrato</span><span class="sxs-lookup"><span data-stu-id="ef73d-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="ef73d-150">Se estas dous cousas son certas, a **Tarefa** configúrase como imputable.</span><span class="sxs-lookup"><span data-stu-id="ef73d-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-151">
                    <strong>Inclúe tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ef73d-152">
                    <strong>Inclúe gasto</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ef73d-153">
                    <strong>Inclúe materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="ef73d-154">
                    <strong>Tarefas incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-155">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-156">
                    <strong>Categoría</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-157">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="ef73d-158">
                    <strong>Impacto na imputabilidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-159">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-160">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-161">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-162">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-163">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-164">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-165">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-166">Facturación nun dato real de tempo: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-167">Tipo de facturación no dato real de gasto: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-168">Tipo de facturación no dato real de material: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-169">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-170">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-171">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-172">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ef73d-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-174">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-175">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-176">Facturación nun dato real de tempo: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-177">Tipo de facturación no dato real de gasto: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-178">Tipo de facturación no dato real de material: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-179">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-180">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-181">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-182">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ef73d-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-183">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-184">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-185">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-186">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-187">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ef73d-188">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-189">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-190">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-191">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-192">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ef73d-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-193">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-194">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-195">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-196">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-197">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-198">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-199">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-200">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-201">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-202">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ef73d-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-203">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-204">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-205">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-206">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-207">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-208">Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-209">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-210">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-211">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-212">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="ef73d-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-213">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-214">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-215">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-216">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-217">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-218">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-220">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-221">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-222">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-223">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-224">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-225">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-226">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-227">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ef73d-228">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-230">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-231">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-232">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-233">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-234">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-235">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-236">Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-237">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-238">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-239">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ef73d-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-241">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-242">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-243">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-244">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-245">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-246">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ef73d-247">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-248">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-249">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ef73d-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ef73d-251">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-252">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-253">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-254">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-255">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-256">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-257">Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-258">Tipo de facturación no dato real de material: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-259">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-260">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ef73d-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-262">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-263">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-264">Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-265">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-266">Facturación nun dato real de tempo: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ef73d-267">Tipo de facturación no dato real de gasto: Imputable</span><span class="sxs-lookup"><span data-stu-id="ef73d-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ef73d-268">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ef73d-269">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ef73d-270">Si</span><span class="sxs-lookup"><span data-stu-id="ef73d-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ef73d-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ef73d-272">Todo o proxecto</span><span class="sxs-lookup"><span data-stu-id="ef73d-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ef73d-273">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ef73d-274">
                    <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ef73d-275">Non se pode configurar</span><span class="sxs-lookup"><span data-stu-id="ef73d-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ef73d-276">Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-277">Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ef73d-278">Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef73d-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
