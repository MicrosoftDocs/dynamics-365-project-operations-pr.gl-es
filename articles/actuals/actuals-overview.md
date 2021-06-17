---
title: Datos reais
description: Este tema ofrece información sobre como traballar con datos reais en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996609"
---
# <a name="actuals"></a><span data-ttu-id="ee5cc-103">Datos reais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-103">Actuals</span></span> 

<span data-ttu-id="ee5cc-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="ee5cc-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee5cc-105">Os datos reais representan o progreso financeiro e programado revisado e aprobado nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="ee5cc-106">Créanse como resultado da aprobación das entradas de tempo, gasto e uso de material e as entradas do diario e facturas.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="ee5cc-107">Liñas de diario e envío de tempo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-107">Journal lines and time submission</span></span>

<span data-ttu-id="ee5cc-108">Para obter máis información sobre a entrada de tempo, consulte [Visión xeral da entrada de tempo](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee5cc-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ee5cc-109">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-109">Time and materials</span></span>

<span data-ttu-id="ee5cc-110">Cando unha entrada de tempo que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ee5cc-111">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-111">Fixed price</span></span>

<span data-ttu-id="ee5cc-112">Cando unha entrada de tempo que se envía está ligada a un proxecto que está asignado a unha liña de contrato de prezo fixo, o sistema crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ee5cc-113">Prezos predefinidos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-113">Default pricing</span></span>

<span data-ttu-id="ee5cc-114">A lóxica para crear prezos predefinidos reside na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="ee5cc-115">Os valores de campo da entrada de tempo cópianse á liña de diario.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="ee5cc-116">Estes valores inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="ee5cc-117">Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade de recursos**, utilízanse para determinar o prezo adecuado por defecto na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ee5cc-118">Pode engadir un campo personalizado na entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="ee5cc-119">Se desexa que o valor do campo se propague aos datos reais, cree o campo nas táboas **Datos reais** e **Liña de diario**.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ee5cc-120">Use código personalizado para propagar o valor do campo seleccionado desde a entrada de tempo ata os datos reais a través da liña do diario empregando as orixes das transaccións.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ee5cc-121">Para obter máis información sobre as orixes e conexións das transaccións, consulte [Ligar datos reais cos rexistros orixinais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="ee5cc-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="ee5cc-122">Liñas de diario e envío de gastos básicos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="ee5cc-123">Para obter máis información sobre a entrada de gasto, consulte [Visión xeral do gasto](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee5cc-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ee5cc-124">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-124">Time and materials</span></span>

<span data-ttu-id="ee5cc-125">Cando unha entrada de gasto básico que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ee5cc-126">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-126">Fixed price</span></span>

<span data-ttu-id="ee5cc-127">Cando se liga unha entrada de gasto básica enviada a un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ee5cc-128">Prezos predefinidos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-128">Default pricing</span></span>

<span data-ttu-id="ee5cc-129">A lóxica para introducir os prezos por defecto dos gastos baséase na categoría de gasto.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="ee5cc-130">A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ee5cc-131">Os campos que afectan aos prezos predefinidos, por exemplo, **Categoría de transacción** e **Unidade**, utilízanse para determinar o prezo adecuado por defecto na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ee5cc-132">Non obstante, isto só funciona cando o método de fixación de prezos na lista de prezos é **Prezo por unidade**.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="ee5cc-133">Se o método de fixación de prezos é **Ao custo** ou **Sobreprezo sobre o custo**, o prezo introducido cando se crea a entrada de gasto úsase para o custo e o prezo da liña do diario de vendas calcúlase en función do método de fixación de prezos.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="ee5cc-134">Pode engadir un campo personalizado na entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="ee5cc-135">Se desexa que o valor do campo se propague aos datos reais, cree o campo nas táboas **Datos reais** e **Liña de diario**.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ee5cc-136">Use código personalizado para propagar o valor do campo seleccionado desde a entrada de tempo ata os datos reais a través da liña do diario empregando as orixes das transaccións.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ee5cc-137">Para obter máis información sobre as orixes e conexións das transaccións, consulte [Ligar datos reais cos rexistros orixinais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="ee5cc-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="ee5cc-138">Presentación de rexistro de liñas de diario e uso de material</span><span class="sxs-lookup"><span data-stu-id="ee5cc-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="ee5cc-139">Para obter máis información sobre a entrada de gasto, consulte [Rexistro do uso de material](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="ee5cc-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ee5cc-140">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-140">Time and materials</span></span>

<span data-ttu-id="ee5cc-141">Cando unha entrada de rexistro do uso de material enviada está ligada a un proxecto que está asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ee5cc-142">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-142">Fixed price</span></span>

<span data-ttu-id="ee5cc-143">Cando se liga unha entrada de rexistro do uso de material básica enviada a un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ee5cc-144">Prezos predefinidos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-144">Default pricing</span></span>

<span data-ttu-id="ee5cc-145">A lóxica para introducir os prezos predefinidos do material baséase na combinación de produtos e unidades.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="ee5cc-146">A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ee5cc-147">Os campos que afectan aos prezos predefinidos, por exemplo, **ID de produto** e **Unidade de recursos**, utilízanse para determinar o prezo adecuado por defecto na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ee5cc-148">Non obstante, isto só funciona para produtos de catálogo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-148">However, this only works for catalog products.</span></span> <span data-ttu-id="ee5cc-149">Para os produtos fóra de catálogo, o prezo introducido cando se crea a entrada do rexistro do uso de material utilízase para o custo e o prezo de venda nas liñas do diario.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="ee5cc-150">Pode engadir un campo personalizado na entrada de **Rexistro do uso de material**.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="ee5cc-151">Se desexa que o valor do campo se propague aos datos reais, cree o campo nas táboas **Datos reais** e **Liña de diario**.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ee5cc-152">Use código personalizado para propagar o valor do campo seleccionado desde a entrada de tempo ata os datos reais a través da liña do diario empregando as orixes das transaccións.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ee5cc-153">Para obter máis información sobre as orixes e conexións das transaccións, consulte [Ligar datos reais cos rexistros orixinais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="ee5cc-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="ee5cc-154">Utilizar diarios de entradas para rexistrar custos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-154">Use entry journals to record costs</span></span>

<span data-ttu-id="ee5cc-155">Pode usar diarios de entradas para rexistrar os custos ou ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ee5cc-156">Os diarios pódense usar para os seguintes fins:</span><span class="sxs-lookup"><span data-stu-id="ee5cc-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="ee5cc-157">Mova os datos reais de transaccións doutro sistema a Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="ee5cc-158">Rexistrar os custos que se produciron noutro sistema.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="ee5cc-159">Estes custos poden incluír gastos de adquisición ou subcontratación.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee5cc-160">A aplicación non valida o tipo de liña de diario nin o prezo relacionado que se introduce na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ee5cc-161">Polo tanto, só un usuario que coñeza perfectamente o impacto contable que teñen os datos reais no proxecto debería usar os diarios de entradas para crear datos reais.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="ee5cc-162">Debido ao impacto deste tipo de diario, debe escoller con atención quen ten acceso para crear diarios de entradas.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="ee5cc-163">Rexistrar datos reais baseados en eventos de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-163">Record actuals based on project events</span></span>

<span data-ttu-id="ee5cc-164">Project Operations rexistra as transaccións financeiras que se producen durante un proxecto.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ee5cc-165">Estas transaccións rexístranse como datos reais.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="ee5cc-166">As seguintes táboas mostran os diferentes tipos de datos reais que se crean dependendo de se o proxecto é un proxecto de tempo e materiais ou de prezo fixo, de se está en fase de prevenda ou de se é un proxecto interno.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="ee5cc-167">O recurso pertence á mesma unidade organizativa que a unidade de contratación do proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ee5cc-168">Evento</span><span class="sxs-lookup"><span data-stu-id="ee5cc-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ee5cc-169">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="ee5cc-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ee5cc-170">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="ee5cc-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ee5cc-171">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="ee5cc-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ee5cc-172">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ee5cc-173">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ee5cc-174">Valores reais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-174">Actuals</span></span></th>
<th><span data-ttu-id="ee5cc-175">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="ee5cc-175">Transaction currency</span></span></th>
<th><span data-ttu-id="ee5cc-176">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-176">Fixed price</span></span></th>
<th><span data-ttu-id="ee5cc-177">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="ee5cc-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee5cc-178">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ee5cc-179">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-180">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ee5cc-181">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee5cc-182">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee5cc-183">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-183">Cost actual</span></span></td>
<td><span data-ttu-id="ee5cc-184">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-185">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-186">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ee5cc-187">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-188">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-189">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ee5cc-190">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee5cc-191">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee5cc-192">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-192">Cost actual</span></span></td>
<td><span data-ttu-id="ee5cc-193">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-194">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-195">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-196">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-197">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-198">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="ee5cc-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee5cc-199">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-200">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="ee5cc-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee5cc-201">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee5cc-202">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee5cc-203">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="ee5cc-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee5cc-204">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-205">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="ee5cc-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-206">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-207">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-208">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-209">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="ee5cc-209">Billed sales</span></span></td>
<td><span data-ttu-id="ee5cc-210">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee5cc-211">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee5cc-212">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="ee5cc-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee5cc-213">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-214">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-215">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-216">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-217">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-218">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="ee5cc-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee5cc-219">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-220">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="ee5cc-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee5cc-221">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee5cc-222">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee5cc-223">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="ee5cc-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee5cc-224">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ee5cc-225">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="ee5cc-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ee5cc-226">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="ee5cc-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ee5cc-227">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-228">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-229">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-230">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="ee5cc-230">Billed sales</span></span></td>
<td><span data-ttu-id="ee5cc-231">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee5cc-232">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee5cc-233">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="ee5cc-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee5cc-234">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-235">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="ee5cc-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ee5cc-236">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-237">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="ee5cc-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee5cc-238">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="ee5cc-239">O recurso pertence a unha unidade organizativa que é distinta da unidade de contratación do proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ee5cc-240">Evento</span><span class="sxs-lookup"><span data-stu-id="ee5cc-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ee5cc-241">Proxecto facturable ou vendido</span><span class="sxs-lookup"><span data-stu-id="ee5cc-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ee5cc-242">Proxecto na fase de prevendas</span><span class="sxs-lookup"><span data-stu-id="ee5cc-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ee5cc-243">Proxecto interno</span><span class="sxs-lookup"><span data-stu-id="ee5cc-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ee5cc-244">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ee5cc-245">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ee5cc-246">Valores reais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-246">Actuals</span></span></th>
<th><span data-ttu-id="ee5cc-247">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="ee5cc-247">Transaction currency</span></span></th>
<th><span data-ttu-id="ee5cc-248">Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-248">Fixed price</span></span></th>
<th><span data-ttu-id="ee5cc-249">Moeda da transacción</span><span class="sxs-lookup"><span data-stu-id="ee5cc-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee5cc-250">Créase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ee5cc-251">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-252">Envíase unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ee5cc-253">Non hai actividade na entidade Datos reais</span><span class="sxs-lookup"><span data-stu-id="ee5cc-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ee5cc-254">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee5cc-255">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-255">Cost actual</span></span></td>
<td><span data-ttu-id="ee5cc-256">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ee5cc-257">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ee5cc-258">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ee5cc-259">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ee5cc-260">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-261">Dato real de vendas sen facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ee5cc-262">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-263">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ee5cc-264">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-265">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="ee5cc-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ee5cc-266">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ee5cc-267">O tempo se aproba e diminúen as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee5cc-268">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-268">Cost actual</span></span></td>
<td><span data-ttu-id="ee5cc-269">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-270">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-271">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-272">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-273">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="ee5cc-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-274">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ee5cc-275">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ee5cc-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-276">Vendas entre organizacións</span><span class="sxs-lookup"><span data-stu-id="ee5cc-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ee5cc-277">Moeda da unidade de contratación</span><span class="sxs-lookup"><span data-stu-id="ee5cc-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-278">Dato real de vendas sen facturar: imputable para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="ee5cc-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee5cc-279">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-280">Dato real de vendas sen facturar: non imputable para a diferencia</span><span class="sxs-lookup"><span data-stu-id="ee5cc-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee5cc-281">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee5cc-282">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee5cc-283">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="ee5cc-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee5cc-284">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-285">Vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="ee5cc-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-286">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-287">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ee5cc-288">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-289">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="ee5cc-289">Billed sales</span></span></td>
<td><span data-ttu-id="ee5cc-290">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee5cc-291">Confírmase unha factura e prodúcese unha diminución das horas facturables.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee5cc-292">Inversión de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="ee5cc-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee5cc-293">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-294">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-295">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-296">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee5cc-297">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-298">Vendas facturadas: imputables para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="ee5cc-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee5cc-299">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-300">Vendas facturadas: non imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="ee5cc-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee5cc-301">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee5cc-302">Corríxese unha factura para aumentar a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee5cc-303">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="ee5cc-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee5cc-304">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ee5cc-305">Inversión de vendas facturadas para fito</span><span class="sxs-lookup"><span data-stu-id="ee5cc-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ee5cc-306">Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></span><span class="sxs-lookup"><span data-stu-id="ee5cc-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ee5cc-307">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-308">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ee5cc-309">Non aplicable</span><span class="sxs-lookup"><span data-stu-id="ee5cc-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-310">Vendas facturadas</span><span class="sxs-lookup"><span data-stu-id="ee5cc-310">Billed sales</span></span></td>
<td><span data-ttu-id="ee5cc-311">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee5cc-312">Corríxese unha factura para diminuír a cantidade imputable.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee5cc-313">Vendas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="ee5cc-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee5cc-314">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-315">Vendas facturadas para a nova cantidade</span><span class="sxs-lookup"><span data-stu-id="ee5cc-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ee5cc-316">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee5cc-317">Vendas sen facturar: imputables para a diferencia</span><span class="sxs-lookup"><span data-stu-id="ee5cc-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee5cc-318">Moeda de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ee5cc-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
