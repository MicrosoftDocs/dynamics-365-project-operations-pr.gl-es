---
title: Páxina de inicio de datos reais
description: Este tema ofrece información sobre como traballar con datos reais en Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907316"
---
# <a name="actuals"></a><span data-ttu-id="48f6c-103">Datos reais</span><span class="sxs-lookup"><span data-stu-id="48f6c-103">Actuals</span></span>

<span data-ttu-id="48f6c-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="48f6c-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="48f6c-105">Os datos reais son la cantidade de traballo que realizou nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="48f6c-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="48f6c-106">Créanse como resultado de entradas de tempo e gastos, e entradas de diario e facturas.</span><span class="sxs-lookup"><span data-stu-id="48f6c-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="48f6c-107">Liñas de diario e envío de tempo</span><span class="sxs-lookup"><span data-stu-id="48f6c-107">Journal lines and time submission</span></span>

<span data-ttu-id="48f6c-108">Para obter máis información sobre a entrada de tempo, consulte [Visión xeral da entrada de tempo](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="48f6c-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="48f6c-109">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="48f6c-109">Time and materials</span></span>

<span data-ttu-id="48f6c-110">Cando unha entrada de tempo que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.</span><span class="sxs-lookup"><span data-stu-id="48f6c-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="48f6c-111">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="48f6c-111">Fixed price</span></span>

<span data-ttu-id="48f6c-112">Cando unha entrada de tempo que se envía está ligada a un proxecto que está asignado a unha liña de contrato de prezo fixo, o sistema crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="48f6c-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="48f6c-113">Prezos predefinidos</span><span class="sxs-lookup"><span data-stu-id="48f6c-113">Default pricing</span></span>

<span data-ttu-id="48f6c-114">A lóxica para crear prezos predefinidos reside na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="48f6c-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="48f6c-115">Os valores de campo da entrada de tempo cópianse á liña de diario.</span><span class="sxs-lookup"><span data-stu-id="48f6c-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="48f6c-116">Estes valores inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente.</span><span class="sxs-lookup"><span data-stu-id="48f6c-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="48f6c-117">Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade organizativa**, utilízanse para determinar o prezo adecuado por defecto na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="48f6c-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="48f6c-118">Pode engadir un campo personalizado na entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="48f6c-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="48f6c-119">Se desexa que o valor de campo se propague aos datos reais, cree o campo na entidade Datos reais e utilice as asignacións de campos para copiar o campo da entrada de tempo aos datos reais.</span><span class="sxs-lookup"><span data-stu-id="48f6c-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="48f6c-120">Liñas de diario e envío de gastos básicos</span><span class="sxs-lookup"><span data-stu-id="48f6c-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="48f6c-121">Para obter máis información sobre a entrada de gasto, consulte [Visión xeral do gasto](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="48f6c-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="48f6c-122">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="48f6c-122">Time and materials</span></span>

<span data-ttu-id="48f6c-123">Cando unha entrada de gasto básico que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.</span><span class="sxs-lookup"><span data-stu-id="48f6c-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="48f6c-124">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="48f6c-124">Fixed price</span></span>

<span data-ttu-id="48f6c-125">Cando unha entrada de gasto básico que se envía está ligada a un proxecto que está asignado a unha liña de contrato de prezo fixo, o sistema crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="48f6c-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="48f6c-126">Prezos predefinidos</span><span class="sxs-lookup"><span data-stu-id="48f6c-126">Default pricing</span></span>

<span data-ttu-id="48f6c-127">A lóxica para introducir os prezos por defecto dos gastos baséase na categoría de gasto.</span><span class="sxs-lookup"><span data-stu-id="48f6c-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="48f6c-128">A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada.</span><span class="sxs-lookup"><span data-stu-id="48f6c-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="48f6c-129">Non obstante, por defecto, o importe que se introduce para o propio prezo establécese directamente nas liñas de diario de gasto para custo e vendas.</span><span class="sxs-lookup"><span data-stu-id="48f6c-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="48f6c-130">A especificación de prezos predeterminados por entrada segundo a categoría nas entradas de gasto non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="48f6c-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="48f6c-131">Utilizar diarios de entradas para rexistrar custos</span><span class="sxs-lookup"><span data-stu-id="48f6c-131">Use entry journals to record costs</span></span>

<span data-ttu-id="48f6c-132">Pode usar diarios de entradas para rexistrar os custos ou ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos.</span><span class="sxs-lookup"><span data-stu-id="48f6c-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="48f6c-133">Os diarios pódense usar para os seguintes fins:</span><span class="sxs-lookup"><span data-stu-id="48f6c-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="48f6c-134">Rexistra o custo real dos materiais e as vendas nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="48f6c-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="48f6c-135">Mover os datos reais de transaccións doutro sistema a Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="48f6c-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="48f6c-136">Rexistrar os custos que se produciron noutro sistema.</span><span class="sxs-lookup"><span data-stu-id="48f6c-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="48f6c-137">Estes custos poden incluír gastos de adquisición ou subcontratación.</span><span class="sxs-lookup"><span data-stu-id="48f6c-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48f6c-138">A aplicación non valida o tipo de liña de diario nin o prezo relacionado que se introduce na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="48f6c-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="48f6c-139">Polo tanto, só un usuario que coñeza perfectamente o impacto contable que teñen os datos reais no proxecto debería usar os diarios de entradas para crear datos reais.</span><span class="sxs-lookup"><span data-stu-id="48f6c-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="48f6c-140">Debido ao impacto deste tipo de diario, debe escoller con atención quen ten acceso para crear diarios de entradas.</span><span class="sxs-lookup"><span data-stu-id="48f6c-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="48f6c-141">Rexistrar datos reais baseados en eventos de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-141">Record actuals based on project events</span></span>

<span data-ttu-id="48f6c-142">Project Operations rexistra as transaccións financeiras que se producen durante un proxecto.</span><span class="sxs-lookup"><span data-stu-id="48f6c-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="48f6c-143">Estas transaccións rexístranse como datos reais.</span><span class="sxs-lookup"><span data-stu-id="48f6c-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="48f6c-144">As seguintes táboas mostran os diferentes tipos de datos reais que se crean dependendo de se o proxecto é un proxecto de tempo e materiais ou de prezo fixo, de se está en fase de prevenda ou de se é un proxecto interno.</span><span class="sxs-lookup"><span data-stu-id="48f6c-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="48f6c-145">O recurso pertence á mesma unidade organizativa que a unidade de contratación do proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="48f6c-146">Evento</span><span class="sxs-lookup"><span data-stu-id="48f6c-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="48f6c-147">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="48f6c-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="48f6c-148">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="48f6c-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="48f6c-149">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="48f6c-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="48f6c-150">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="48f6c-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="48f6c-151">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="48f6c-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="48f6c-152">Valores reais</span><span class="sxs-lookup"><span data-stu-id="48f6c-152">Actuals</span></span></th>
<th><span data-ttu-id="48f6c-153">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="48f6c-153">Transaction currency</span></span></th>
<th><span data-ttu-id="48f6c-154">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="48f6c-154">Fixed price</span></span></th>
<th><span data-ttu-id="48f6c-155">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="48f6c-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="48f6c-156">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="48f6c-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="48f6c-157">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="48f6c-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-158">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="48f6c-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="48f6c-159">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="48f6c-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="48f6c-160">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="48f6c-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="48f6c-161">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-161">Cost actual</span></span></td>
<td><span data-ttu-id="48f6c-162">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-163">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-164">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="48f6c-165">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-166">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-167">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="48f6c-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="48f6c-168">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="48f6c-169">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="48f6c-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="48f6c-170">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-170">Cost actual</span></span></td>
<td><span data-ttu-id="48f6c-171">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-172">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-173">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-174">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-175">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-176">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="48f6c-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="48f6c-177">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-178">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="48f6c-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="48f6c-179">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="48f6c-180">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="48f6c-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="48f6c-181">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="48f6c-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="48f6c-182">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-183">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="48f6c-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-184">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-185">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-186">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-187">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="48f6c-187">Billed sales</span></span></td>
<td><span data-ttu-id="48f6c-188">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="48f6c-189">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="48f6c-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="48f6c-190">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="48f6c-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="48f6c-191">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-192">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-193">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-194">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-195">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-196">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="48f6c-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="48f6c-197">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-198">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="48f6c-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="48f6c-199">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="48f6c-200">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="48f6c-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="48f6c-201">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="48f6c-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="48f6c-202">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="48f6c-203">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="48f6c-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="48f6c-204">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="48f6c-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="48f6c-205">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-206">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-207">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-208">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="48f6c-208">Billed sales</span></span></td>
<td><span data-ttu-id="48f6c-209">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="48f6c-210">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="48f6c-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="48f6c-211">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="48f6c-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="48f6c-212">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-213">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="48f6c-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="48f6c-214">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-215">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="48f6c-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="48f6c-216">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="48f6c-217">O recurso pertence a unha unidade organizativa que é distinta da unidade de contratación do proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="48f6c-218">Evento</span><span class="sxs-lookup"><span data-stu-id="48f6c-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="48f6c-219">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="48f6c-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="48f6c-220">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="48f6c-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="48f6c-221">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="48f6c-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="48f6c-222">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="48f6c-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="48f6c-223">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="48f6c-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="48f6c-224">Valores reais</span><span class="sxs-lookup"><span data-stu-id="48f6c-224">Actuals</span></span></th>
<th><span data-ttu-id="48f6c-225">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="48f6c-225">Transaction currency</span></span></th>
<th><span data-ttu-id="48f6c-226">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="48f6c-226">Fixed price</span></span></th>
<th><span data-ttu-id="48f6c-227">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="48f6c-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="48f6c-228">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="48f6c-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="48f6c-229">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="48f6c-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-230">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="48f6c-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="48f6c-231">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="48f6c-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="48f6c-232">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="48f6c-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="48f6c-233">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-233">Cost actual</span></span></td>
<td><span data-ttu-id="48f6c-234">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="48f6c-235">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="48f6c-236">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="48f6c-237">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="48f6c-238">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-239">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="48f6c-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="48f6c-240">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-241">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="48f6c-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="48f6c-242">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="48f6c-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-243">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="48f6c-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="48f6c-244">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="48f6c-245">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="48f6c-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="48f6c-246">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-246">Cost actual</span></span></td>
<td><span data-ttu-id="48f6c-247">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-248">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-249">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-250">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-251">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="48f6c-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-252">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="48f6c-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="48f6c-253">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="48f6c-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-254">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="48f6c-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="48f6c-255">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="48f6c-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-256">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="48f6c-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="48f6c-257">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-258">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="48f6c-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="48f6c-259">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="48f6c-260">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="48f6c-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="48f6c-261">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="48f6c-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="48f6c-262">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-263">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="48f6c-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-264">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-265">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="48f6c-266">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-267">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="48f6c-267">Billed sales</span></span></td>
<td><span data-ttu-id="48f6c-268">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="48f6c-269">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="48f6c-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="48f6c-270">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="48f6c-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="48f6c-271">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-272">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-273">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-274">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="48f6c-275">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-276">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="48f6c-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="48f6c-277">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-278">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="48f6c-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="48f6c-279">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="48f6c-280">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="48f6c-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="48f6c-281">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="48f6c-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="48f6c-282">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="48f6c-283">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="48f6c-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="48f6c-284">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="48f6c-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="48f6c-285">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-286">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="48f6c-287">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="48f6c-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-288">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="48f6c-288">Billed sales</span></span></td>
<td><span data-ttu-id="48f6c-289">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="48f6c-290">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="48f6c-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="48f6c-291">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="48f6c-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="48f6c-292">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-293">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="48f6c-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="48f6c-294">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="48f6c-295">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="48f6c-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="48f6c-296">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="48f6c-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
