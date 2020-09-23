---
title: Valores reais
description: Neste tema se proporciona información sobre datos reais do proxecto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751448"
---
# <a name="actuals"></a><span data-ttu-id="25833-103">Valores reais</span><span class="sxs-lookup"><span data-stu-id="25833-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="25833-104">Os datos reais son la cantidade de traballo que realizou nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="25833-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="25833-105">É posible rastrexar os datos reais do proxecto ata os seus documentos de orixe.</span><span class="sxs-lookup"><span data-stu-id="25833-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="25833-106">Eses documentos de orixe inclúen tempo, gasto, entradas no diario e tamén facturas.</span><span class="sxs-lookup"><span data-stu-id="25833-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como se rastrexan os datos reais do proxecto ata os documentos de orixe](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="25833-108">Envío dunha entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="25833-108">Submitting a time entry</span></span>

<span data-ttu-id="25833-109">En PSA, cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario.</span><span class="sxs-lookup"><span data-stu-id="25833-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="25833-110">Unha liña é para o custo e a outra é para as vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="25833-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="25833-111">Cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="25833-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="25833-112">A lóxica para especificar prezos predefinidos reside na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="25833-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="25833-113">Todos os valores de campo dunha entrada de tempo cópianse á liña de diario.</span><span class="sxs-lookup"><span data-stu-id="25833-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="25833-114">Estes campos inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente.</span><span class="sxs-lookup"><span data-stu-id="25833-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="25833-115">Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade organizativa**, fan que se introduza o prezo adecuado por defecto na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="25833-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="25833-116">Se engade un campo personalizado na entrada de tempo e desexa que o valor de campo se propague aos datos reais, cree o campo na entidade Datos reais e utilice as asignacións de campos para copiar o campo da entrada de tempo aos datos reais.</span><span class="sxs-lookup"><span data-stu-id="25833-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="25833-117">Envío dunha entrada de gasto</span><span class="sxs-lookup"><span data-stu-id="25833-117">Submitting an expense entry</span></span>

<span data-ttu-id="25833-118">En PSA, cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario.</span><span class="sxs-lookup"><span data-stu-id="25833-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="25833-119">Unha liña é para o custo e a outra é para as vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="25833-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="25833-120">Cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="25833-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="25833-121">A lóxica para especificar os prezos predefinidos para os gastos basease na categoría de gasto seleccionada na páxina **Entrada de gasto**.</span><span class="sxs-lookup"><span data-stu-id="25833-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="25833-122">A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada.</span><span class="sxs-lookup"><span data-stu-id="25833-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="25833-123">Non obstante, para o prezo, o importe que introduce o usuario establécese directamente nas liñas de diario de gasto para custo e vendas por defecto.</span><span class="sxs-lookup"><span data-stu-id="25833-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="25833-124">Na versión actual de PSA, a especificación de prezos predeterminados por entrada segundo a categoría nas entradas de gasto non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="25833-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="25833-125">Utilización de diarios para rexistrar custos</span><span class="sxs-lookup"><span data-stu-id="25833-125">Using journals to record costs</span></span>

<span data-ttu-id="25833-126">En PSA, os diarios permiten rexistrar custos ou ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos.</span><span class="sxs-lookup"><span data-stu-id="25833-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="25833-127">Un diario ten un encabezado, liñas e unha acción **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="25833-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="25833-128">Este son algúns escenarios nos que podería usar un diario:</span><span class="sxs-lookup"><span data-stu-id="25833-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="25833-129">Debe rexistrar os custos reais do material e as vendas nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="25833-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="25833-130">Debe mover os datos reais de transaccións doutro sistema a PSA.</span><span class="sxs-lookup"><span data-stu-id="25833-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="25833-131">Debe rexistrar os custos que se produciron noutro sistema, como os custos de adquisición ou subcontratación.</span><span class="sxs-lookup"><span data-stu-id="25833-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="25833-132">Rexistro de datos reais baseados en eventos de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-132">Recording actuals based on project events</span></span>

<span data-ttu-id="25833-133">PSA rexistra as transaccións financeiras que se producen durante un proxecto.</span><span class="sxs-lookup"><span data-stu-id="25833-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="25833-134">Estas transaccións rexístranse como **datos reais**.</span><span class="sxs-lookup"><span data-stu-id="25833-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="25833-135">As seguintes táboas mostran os diferentes tipos de datos reais que se crean dependendo de se o proxecto é un proxecto de tempo e materiais ou de prezo fixo, de se está en fase de prevenda ou de se é un proxecto interno.</span><span class="sxs-lookup"><span data-stu-id="25833-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="25833-136">**O recurso pertence á mesma unidade organizativa que a unidade de contratación do proxecto**</span><span class="sxs-lookup"><span data-stu-id="25833-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="25833-137">Evento</span><span class="sxs-lookup"><span data-stu-id="25833-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="25833-138">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="25833-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="25833-139">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="25833-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="25833-140">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="25833-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="25833-141">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="25833-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="25833-142">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="25833-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="25833-143">Valores reais</span><span class="sxs-lookup"><span data-stu-id="25833-143">Actuals</span></span></th>
<th><span data-ttu-id="25833-144">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="25833-144">Transaction currency</span></span></th>
<th><span data-ttu-id="25833-145">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="25833-145">Fixed price</span></span></th>
<th><span data-ttu-id="25833-146">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="25833-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="25833-147">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="25833-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="25833-148">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="25833-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-149">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="25833-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="25833-150">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="25833-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25833-151">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="25833-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25833-152">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-152">Cost actual</span></span></td>
<td><span data-ttu-id="25833-153">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-154">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-155">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="25833-156">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-157">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-158">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="25833-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="25833-159">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25833-160">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="25833-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25833-161">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-161">Cost actual</span></span></td>
<td><span data-ttu-id="25833-162">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-163">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-164">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-165">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-166">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-167">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="25833-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25833-168">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-169">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="25833-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25833-170">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25833-171">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="25833-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25833-172">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="25833-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25833-173">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-174">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="25833-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-175">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-176">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-177">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-178">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="25833-178">Billed sales</span></span></td>
<td><span data-ttu-id="25833-179">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25833-180">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="25833-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25833-181">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="25833-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25833-182">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-183">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-184">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-185">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-186">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-187">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="25833-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25833-188">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-189">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="25833-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25833-190">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25833-191">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="25833-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25833-192">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="25833-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25833-193">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="25833-194">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="25833-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="25833-195">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="25833-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="25833-196">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-197">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-198">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-199">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="25833-199">Billed sales</span></span></td>
<td><span data-ttu-id="25833-200">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25833-201">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="25833-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25833-202">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="25833-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25833-203">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-204">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="25833-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="25833-205">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-206">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="25833-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="25833-207">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="25833-208">**O recurso pertence a unha unidade organizativa que é distinta da unidade de contratación do proxecto**</span><span class="sxs-lookup"><span data-stu-id="25833-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="25833-209">Evento</span><span class="sxs-lookup"><span data-stu-id="25833-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="25833-210">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="25833-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="25833-211">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="25833-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="25833-212">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="25833-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="25833-213">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="25833-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="25833-214">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="25833-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="25833-215">Valores reais</span><span class="sxs-lookup"><span data-stu-id="25833-215">Actuals</span></span></th>
<th><span data-ttu-id="25833-216">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="25833-216">Transaction currency</span></span></th>
<th><span data-ttu-id="25833-217">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="25833-217">Fixed price</span></span></th>
<th><span data-ttu-id="25833-218">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="25833-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="25833-219">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="25833-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="25833-220">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="25833-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-221">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="25833-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="25833-222">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="25833-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="25833-223">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="25833-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25833-224">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-224">Cost actual</span></span></td>
<td><span data-ttu-id="25833-225">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="25833-226">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="25833-227">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="25833-228">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="25833-229">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-230">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="25833-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="25833-231">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-232">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="25833-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="25833-233">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="25833-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-234">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="25833-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="25833-235">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="25833-236">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="25833-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25833-237">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-237">Cost actual</span></span></td>
<td><span data-ttu-id="25833-238">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-239">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-240">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-241">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-242">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="25833-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-243">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="25833-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="25833-244">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="25833-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-245">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="25833-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="25833-246">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="25833-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-247">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="25833-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25833-248">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-249">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="25833-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25833-250">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25833-251">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="25833-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25833-252">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="25833-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25833-253">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-254">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="25833-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-255">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-256">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="25833-257">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-258">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="25833-258">Billed sales</span></span></td>
<td><span data-ttu-id="25833-259">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25833-260">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="25833-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25833-261">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="25833-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25833-262">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-263">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-264">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-265">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25833-266">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-267">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="25833-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25833-268">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-269">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="25833-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25833-270">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25833-271">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="25833-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25833-272">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="25833-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25833-273">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="25833-274">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="25833-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="25833-275">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="25833-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="25833-276">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-277">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="25833-278">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="25833-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-279">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="25833-279">Billed sales</span></span></td>
<td><span data-ttu-id="25833-280">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25833-281">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="25833-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25833-282">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="25833-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25833-283">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-284">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="25833-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="25833-285">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25833-286">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="25833-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="25833-287">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="25833-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
