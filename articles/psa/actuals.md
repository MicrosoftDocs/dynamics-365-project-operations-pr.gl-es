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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146121"
---
# <a name="actuals-overview"></a><span data-ttu-id="5f5d2-103">Visión xeral dos datos reais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5f5d2-104">Os datos reais son la cantidade de traballo que realizou nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="5f5d2-105">É posible rastrexar os datos reais do proxecto ata os seus documentos de orixe.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="5f5d2-106">Eses documentos de orixe inclúen tempo, gasto, entradas no diario e tamén facturas.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como se rastrexan os datos reais do proxecto ata os documentos de orixe](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="5f5d2-108">Envío dunha entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-108">Submitting a time entry</span></span>

<span data-ttu-id="5f5d2-109">En PSA, cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5f5d2-110">Unha liña é para o custo e a outra é para as vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5f5d2-111">Cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="5f5d2-112">A lóxica para especificar prezos predefinidos reside na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="5f5d2-113">Todos os valores de campo dunha entrada de tempo cópianse á liña de diario.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="5f5d2-114">Estes campos inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="5f5d2-115">Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade organizativa**, fan que se introduza o prezo adecuado por defecto na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="5f5d2-116">Se engade un campo personalizado na entrada de tempo e desexa que o valor de campo se propague aos datos reais, cree o campo na entidade Datos reais e utilice as asignacións de campos para copiar o campo da entrada de tempo aos datos reais.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="5f5d2-117">Envío dunha entrada de gasto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-117">Submitting an expense entry</span></span>

<span data-ttu-id="5f5d2-118">En PSA, cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5f5d2-119">Unha liña é para o custo e a outra é para as vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5f5d2-120">Cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="5f5d2-121">A lóxica para especificar os prezos predefinidos para os gastos basease na categoría de gasto seleccionada na páxina **Entrada de gasto**.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="5f5d2-122">A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5f5d2-123">Non obstante, para o prezo, o importe que introduce o usuario establécese directamente nas liñas de diario de gasto para custo e vendas por defecto.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="5f5d2-124">Na versión actual de PSA, a especificación de prezos predeterminados por entrada segundo a categoría nas entradas de gasto non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="5f5d2-125">Utilización de diarios de entradas para rexistrar custos</span><span class="sxs-lookup"><span data-stu-id="5f5d2-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="5f5d2-126">En PSA, os diarios de entradas permiten rexistrar o custo ou os ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5f5d2-127">Un diario ten un encabezado, liñas e unha acción **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="5f5d2-128">Este son algúns escenarios nos que podería usar un diario:</span><span class="sxs-lookup"><span data-stu-id="5f5d2-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="5f5d2-129">Debe rexistrar os custos reais do material e as vendas nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="5f5d2-130">Debe mover os datos reais de transaccións doutro sistema a PSA.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="5f5d2-131">Debe rexistrar os custos que se produciron noutro sistema, como os custos de adquisición ou subcontratación.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f5d2-132">O uso de diarios de entradas para crear o datos reais debe facelo só un usuario que teña pleno coñecemento do impacto contable que teñen os datos reais no proxecto.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="5f5d2-133">Isto é debido a que a aplicación non valida o tipo de liña de diario ou o prezo relacionado que se introduce na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="5f5d2-134">Debido ao impacto deste tipo de diario, teña a precaución adecuada sobre quen ten acceso a crear diarios de entradas.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="5f5d2-135">Rexistro de datos reais baseados en eventos de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-135">Recording actuals based on project events</span></span>

<span data-ttu-id="5f5d2-136">PSA rexistra as transaccións financeiras que se producen durante un proxecto.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5f5d2-137">Estas transaccións rexístranse como **datos reais**.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="5f5d2-138">As seguintes táboas mostran os diferentes tipos de datos reais que se crean dependendo de se o proxecto é un proxecto de tempo e materiais ou de prezo fixo, de se está en fase de prevenda ou de se é un proxecto interno.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="5f5d2-139">**O recurso pertence á mesma unidade organizativa que a unidade de contratación do proxecto**</span><span class="sxs-lookup"><span data-stu-id="5f5d2-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5f5d2-140">Evento</span><span class="sxs-lookup"><span data-stu-id="5f5d2-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5f5d2-141">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="5f5d2-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5f5d2-142">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="5f5d2-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5f5d2-143">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="5f5d2-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5f5d2-144">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5f5d2-145">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5f5d2-146">Valores reais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-146">Actuals</span></span></th>
<th><span data-ttu-id="5f5d2-147">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="5f5d2-147">Transaction currency</span></span></th>
<th><span data-ttu-id="5f5d2-148">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-148">Fixed price</span></span></th>
<th><span data-ttu-id="5f5d2-149">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="5f5d2-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f5d2-150">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5f5d2-151">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-152">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5f5d2-153">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f5d2-154">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f5d2-155">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-155">Cost actual</span></span></td>
<td><span data-ttu-id="5f5d2-156">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-157">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-158">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5f5d2-159">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-160">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-161">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5f5d2-162">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f5d2-163">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f5d2-164">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-164">Cost actual</span></span></td>
<td><span data-ttu-id="5f5d2-165">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-166">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-167">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-168">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-169">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-170">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="5f5d2-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f5d2-171">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-172">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="5f5d2-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f5d2-173">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f5d2-174">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f5d2-175">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="5f5d2-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f5d2-176">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-177">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="5f5d2-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-178">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-179">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-180">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-181">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="5f5d2-181">Billed sales</span></span></td>
<td><span data-ttu-id="5f5d2-182">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f5d2-183">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f5d2-184">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="5f5d2-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f5d2-185">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-186">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-187">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-188">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-189">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-190">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="5f5d2-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f5d2-191">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-192">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="5f5d2-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f5d2-193">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f5d2-194">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f5d2-195">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="5f5d2-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f5d2-196">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5f5d2-197">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="5f5d2-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5f5d2-198">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="5f5d2-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5f5d2-199">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-200">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-201">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-202">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="5f5d2-202">Billed sales</span></span></td>
<td><span data-ttu-id="5f5d2-203">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f5d2-204">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f5d2-205">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="5f5d2-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f5d2-206">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-207">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="5f5d2-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5f5d2-208">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-209">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="5f5d2-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f5d2-210">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f5d2-211">**O recurso pertence a unha unidade organizativa que é distinta da unidade de contratación do proxecto**</span><span class="sxs-lookup"><span data-stu-id="5f5d2-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5f5d2-212">Evento</span><span class="sxs-lookup"><span data-stu-id="5f5d2-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5f5d2-213">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="5f5d2-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5f5d2-214">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="5f5d2-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5f5d2-215">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="5f5d2-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5f5d2-216">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5f5d2-217">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5f5d2-218">Valores reais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-218">Actuals</span></span></th>
<th><span data-ttu-id="5f5d2-219">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="5f5d2-219">Transaction currency</span></span></th>
<th><span data-ttu-id="5f5d2-220">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-220">Fixed price</span></span></th>
<th><span data-ttu-id="5f5d2-221">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="5f5d2-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f5d2-222">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5f5d2-223">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-224">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5f5d2-225">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="5f5d2-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5f5d2-226">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f5d2-227">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-227">Cost actual</span></span></td>
<td><span data-ttu-id="5f5d2-228">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5f5d2-229">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5f5d2-230">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5f5d2-231">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5f5d2-232">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-233">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5f5d2-234">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-235">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="5f5d2-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5f5d2-236">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="5f5d2-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-237">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="5f5d2-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5f5d2-238">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5f5d2-239">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f5d2-240">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-240">Cost actual</span></span></td>
<td><span data-ttu-id="5f5d2-241">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-242">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-243">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-244">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-245">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="5f5d2-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-246">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="5f5d2-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5f5d2-247">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="5f5d2-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-248">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="5f5d2-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5f5d2-249">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="5f5d2-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-250">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="5f5d2-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f5d2-251">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-252">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="5f5d2-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f5d2-253">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f5d2-254">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f5d2-255">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="5f5d2-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f5d2-256">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-257">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="5f5d2-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-258">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-259">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5f5d2-260">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-261">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="5f5d2-261">Billed sales</span></span></td>
<td><span data-ttu-id="5f5d2-262">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f5d2-263">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f5d2-264">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="5f5d2-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f5d2-265">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-266">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-267">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-268">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f5d2-269">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-270">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="5f5d2-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f5d2-271">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-272">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="5f5d2-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f5d2-273">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f5d2-274">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f5d2-275">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="5f5d2-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f5d2-276">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5f5d2-277">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="5f5d2-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5f5d2-278">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="5f5d2-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5f5d2-279">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-280">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5f5d2-281">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="5f5d2-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-282">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="5f5d2-282">Billed sales</span></span></td>
<td><span data-ttu-id="5f5d2-283">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f5d2-284">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="5f5d2-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f5d2-285">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="5f5d2-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f5d2-286">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-287">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="5f5d2-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5f5d2-288">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f5d2-289">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="5f5d2-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f5d2-290">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="5f5d2-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
