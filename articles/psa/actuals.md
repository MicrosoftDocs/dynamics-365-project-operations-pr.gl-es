---
title: Visión xeral dos datos reais
description: Neste tema se proporciona información sobre datos reais do proxecto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129766"
---
# <a name="actuals-overview"></a><span data-ttu-id="40268-103">Visión xeral dos datos reais</span><span class="sxs-lookup"><span data-stu-id="40268-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="40268-104">Os datos reais son la cantidade de traballo que realizou nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="40268-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="40268-105">É posible rastrexar os datos reais do proxecto ata os seus documentos de orixe.</span><span class="sxs-lookup"><span data-stu-id="40268-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="40268-106">Eses documentos de orixe inclúen tempo, gasto, entradas no diario e tamén facturas.</span><span class="sxs-lookup"><span data-stu-id="40268-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como se rastrexan os datos reais do proxecto ata os documentos de orixe](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="40268-108">Envío dunha entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="40268-108">Submitting a time entry</span></span>

<span data-ttu-id="40268-109">En PSA, cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario.</span><span class="sxs-lookup"><span data-stu-id="40268-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="40268-110">Unha liña é para o custo e a outra é para as vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="40268-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="40268-111">Cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="40268-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="40268-112">A lóxica para especificar prezos predefinidos reside na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="40268-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="40268-113">Todos os valores de campo dunha entrada de tempo cópianse á liña de diario.</span><span class="sxs-lookup"><span data-stu-id="40268-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="40268-114">Estes campos inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente.</span><span class="sxs-lookup"><span data-stu-id="40268-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="40268-115">Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade organizativa**, fan que se introduza o prezo adecuado por defecto na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="40268-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="40268-116">Se engade un campo personalizado na entrada de tempo e desexa que o valor de campo se propague aos datos reais, cree o campo na entidade Datos reais e utilice as asignacións de campos para copiar o campo da entrada de tempo aos datos reais.</span><span class="sxs-lookup"><span data-stu-id="40268-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="40268-117">Envío dunha entrada de gasto</span><span class="sxs-lookup"><span data-stu-id="40268-117">Submitting an expense entry</span></span>

<span data-ttu-id="40268-118">En PSA, cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario.</span><span class="sxs-lookup"><span data-stu-id="40268-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="40268-119">Unha liña é para o custo e a outra é para as vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="40268-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="40268-120">Cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="40268-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="40268-121">A lóxica para especificar os prezos predefinidos para os gastos basease na categoría de gasto seleccionada na páxina **Entrada de gasto**.</span><span class="sxs-lookup"><span data-stu-id="40268-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="40268-122">A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada.</span><span class="sxs-lookup"><span data-stu-id="40268-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="40268-123">Non obstante, para o prezo, o importe que introduce o usuario establécese directamente nas liñas de diario de gasto para custo e vendas por defecto.</span><span class="sxs-lookup"><span data-stu-id="40268-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="40268-124">Na versión actual de PSA, a especificación de prezos predeterminados por entrada segundo a categoría nas entradas de gasto non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="40268-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="40268-125">Utilización de diarios de entradas para rexistrar custos</span><span class="sxs-lookup"><span data-stu-id="40268-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="40268-126">En PSA, os diarios de entradas permiten rexistrar o custo ou os ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos.</span><span class="sxs-lookup"><span data-stu-id="40268-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="40268-127">Un diario ten un encabezado, liñas e unha acción **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="40268-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="40268-128">Este son algúns escenarios nos que podería usar un diario:</span><span class="sxs-lookup"><span data-stu-id="40268-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="40268-129">Debe rexistrar os custos reais do material e as vendas nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="40268-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="40268-130">Debe mover os datos reais de transaccións doutro sistema a PSA.</span><span class="sxs-lookup"><span data-stu-id="40268-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="40268-131">Debe rexistrar os custos que se produciron noutro sistema, como os custos de adquisición ou subcontratación.</span><span class="sxs-lookup"><span data-stu-id="40268-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40268-132">O uso de diarios de entradas para crear o datos reais debe facelo só un usuario que teña pleno coñecemento do impacto contable que teñen os datos reais no proxecto.</span><span class="sxs-lookup"><span data-stu-id="40268-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="40268-133">Isto é debido a que a aplicación non valida o tipo de liña de diario ou o prezo relacionado que se introduce na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="40268-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="40268-134">Debido ao impacto deste tipo de diario, teña a precaución adecuada sobre quen ten acceso a crear diarios de entradas.</span><span class="sxs-lookup"><span data-stu-id="40268-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="40268-135">Rexistro de datos reais baseados en eventos de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-135">Recording actuals based on project events</span></span>

<span data-ttu-id="40268-136">PSA rexistra as transaccións financeiras que se producen durante un proxecto.</span><span class="sxs-lookup"><span data-stu-id="40268-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="40268-137">Estas transaccións rexístranse como **datos reais**.</span><span class="sxs-lookup"><span data-stu-id="40268-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="40268-138">As seguintes táboas mostran os diferentes tipos de datos reais que se crean dependendo de se o proxecto é un proxecto de tempo e materiais ou de prezo fixo, de se está en fase de prevenda ou de se é un proxecto interno.</span><span class="sxs-lookup"><span data-stu-id="40268-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="40268-139">**O recurso pertence á mesma unidade organizativa que a unidade de contratación do proxecto**</span><span class="sxs-lookup"><span data-stu-id="40268-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="40268-140">Evento</span><span class="sxs-lookup"><span data-stu-id="40268-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="40268-141">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="40268-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="40268-142">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="40268-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="40268-143">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="40268-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="40268-144">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="40268-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="40268-145">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="40268-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="40268-146">Valores reais</span><span class="sxs-lookup"><span data-stu-id="40268-146">Actuals</span></span></th>
<th><span data-ttu-id="40268-147">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="40268-147">Transaction currency</span></span></th>
<th><span data-ttu-id="40268-148">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="40268-148">Fixed price</span></span></th>
<th><span data-ttu-id="40268-149">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="40268-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="40268-150">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="40268-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="40268-151">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="40268-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-152">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="40268-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="40268-153">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="40268-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="40268-154">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="40268-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="40268-155">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-155">Cost actual</span></span></td>
<td><span data-ttu-id="40268-156">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-157">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-158">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="40268-159">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-160">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-161">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="40268-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="40268-162">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="40268-163">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="40268-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="40268-164">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-164">Cost actual</span></span></td>
<td><span data-ttu-id="40268-165">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-166">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-167">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-168">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-169">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-170">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="40268-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="40268-171">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-172">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="40268-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="40268-173">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="40268-174">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="40268-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="40268-175">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="40268-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="40268-176">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-177">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="40268-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-178">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-179">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-180">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-181">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="40268-181">Billed sales</span></span></td>
<td><span data-ttu-id="40268-182">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="40268-183">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="40268-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="40268-184">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="40268-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="40268-185">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-186">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-187">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-188">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-189">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-190">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="40268-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="40268-191">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-192">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="40268-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="40268-193">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="40268-194">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="40268-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="40268-195">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="40268-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="40268-196">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="40268-197">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="40268-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="40268-198">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="40268-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="40268-199">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-200">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-201">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-202">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="40268-202">Billed sales</span></span></td>
<td><span data-ttu-id="40268-203">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="40268-204">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="40268-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="40268-205">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="40268-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="40268-206">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-207">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="40268-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="40268-208">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-209">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="40268-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="40268-210">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="40268-211">**O recurso pertence a unha unidade organizativa que é distinta da unidade de contratación do proxecto**</span><span class="sxs-lookup"><span data-stu-id="40268-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="40268-212">Evento</span><span class="sxs-lookup"><span data-stu-id="40268-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="40268-213">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="40268-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="40268-214">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="40268-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="40268-215">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="40268-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="40268-216">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="40268-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="40268-217">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="40268-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="40268-218">Valores reais</span><span class="sxs-lookup"><span data-stu-id="40268-218">Actuals</span></span></th>
<th><span data-ttu-id="40268-219">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="40268-219">Transaction currency</span></span></th>
<th><span data-ttu-id="40268-220">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="40268-220">Fixed price</span></span></th>
<th><span data-ttu-id="40268-221">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="40268-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="40268-222">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="40268-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="40268-223">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="40268-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-224">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="40268-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="40268-225">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="40268-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="40268-226">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="40268-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="40268-227">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-227">Cost actual</span></span></td>
<td><span data-ttu-id="40268-228">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="40268-229">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="40268-230">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="40268-231">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="40268-232">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-233">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="40268-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="40268-234">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-235">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="40268-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="40268-236">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="40268-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-237">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="40268-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="40268-238">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="40268-239">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="40268-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="40268-240">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-240">Cost actual</span></span></td>
<td><span data-ttu-id="40268-241">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-242">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-243">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-244">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-245">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="40268-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-246">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="40268-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="40268-247">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="40268-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-248">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="40268-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="40268-249">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="40268-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-250">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="40268-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="40268-251">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-252">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="40268-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="40268-253">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="40268-254">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="40268-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="40268-255">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="40268-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="40268-256">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-257">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="40268-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-258">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-259">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="40268-260">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-261">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="40268-261">Billed sales</span></span></td>
<td><span data-ttu-id="40268-262">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="40268-263">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="40268-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="40268-264">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="40268-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="40268-265">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-266">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-267">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-268">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="40268-269">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-270">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="40268-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="40268-271">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-272">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="40268-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="40268-273">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="40268-274">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="40268-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="40268-275">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="40268-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="40268-276">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="40268-277">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="40268-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="40268-278">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="40268-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="40268-279">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-280">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="40268-281">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="40268-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-282">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="40268-282">Billed sales</span></span></td>
<td><span data-ttu-id="40268-283">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="40268-284">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="40268-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="40268-285">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="40268-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="40268-286">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-287">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="40268-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="40268-288">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="40268-289">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="40268-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="40268-290">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="40268-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
