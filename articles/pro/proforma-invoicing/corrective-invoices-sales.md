---
title: Facturas de proxecto correctivas
description: Este tema ofrece información sobre como crear e confirmar facturas correctivas en Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004079"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="02488-103">Facturas de proxecto correctivas</span><span class="sxs-lookup"><span data-stu-id="02488-103">Corrective project invoices</span></span>

<span data-ttu-id="02488-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="02488-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="02488-105">Pódese corrixir unha factura de proxecto confirmada para procesar cambios ou créditos segundo se negociaron co cliente e o xestor do proxecto.</span><span class="sxs-lookup"><span data-stu-id="02488-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="02488-106">Para editar unha factura confirmada, abra a factura confirmada e seleccione **Corrixir esta factura**.</span><span class="sxs-lookup"><span data-stu-id="02488-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="02488-107">Esta selección non está dispoñible a menos que se confirme unha factura do proxecto.</span><span class="sxs-lookup"><span data-stu-id="02488-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="02488-108">A partir da factura confirmada créase un novo borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="02488-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="02488-109">Todos os detalles da liña de factura da factura confirmada anteriormente copianse no novo borrador.</span><span class="sxs-lookup"><span data-stu-id="02488-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="02488-110">Os seguintes son algúns dos puntos clave para comprender os detalles da liña da nova factura corrixida:</span><span class="sxs-lookup"><span data-stu-id="02488-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="02488-111">Todas as cantidades actualízanse a cero.</span><span class="sxs-lookup"><span data-stu-id="02488-111">All quantities are updated to zero.</span></span> <span data-ttu-id="02488-112">A aplicación asume que todos os elementos facturados están totalmente aboados.</span><span class="sxs-lookup"><span data-stu-id="02488-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="02488-113">Se é necesario, pode actualizar manualmente estas cantidades para reflectir a cantidade que se está a facturar e non a cantidade que se vai aboar.</span><span class="sxs-lookup"><span data-stu-id="02488-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="02488-114">En función da cantidade que introduza, a aplicación calcula a cantidade aboada.</span><span class="sxs-lookup"><span data-stu-id="02488-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="02488-115">Este importe reflíctese nos datos reais que se crean cando se confirma a factura corrixida.</span><span class="sxs-lookup"><span data-stu-id="02488-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="02488-116">Se está a facer cambios no importe do imposto, debe ingresar o importe do imposto correcto e non o importe do imposto que vai aboar.</span><span class="sxs-lookup"><span data-stu-id="02488-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="02488-117">Non se copian as liñas de contrato baseado en produto confirmadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="02488-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="02488-118">Non se admite o procesamento de correccións nunha factura dun proxecto baseado en produto.</span><span class="sxs-lookup"><span data-stu-id="02488-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="02488-119">As correccións de fitos sempre se procesan como abonos completos.</span><span class="sxs-lookup"><span data-stu-id="02488-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="02488-120">Os importes de retencións ou adiantos pódense corrixir se se facturou ao cliente un importe incorrecto.</span><span class="sxs-lookup"><span data-stu-id="02488-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="02488-121">As conciliacións de retencións e adiantos pódense corrixir se se utilizou un importe incorrecto para conciliar os cargos dunha factura confirmada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02488-122">Os detalles da liña de factura que son correccións doutros cargos xa facturados teñen o campo **Corrección** definido como **Si**.</span><span class="sxs-lookup"><span data-stu-id="02488-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="02488-123">As facturas que corrixiron os detalles da liña de factura teñen un campo chamado **Ten correccións** que tamén está establecido en **Si**.</span><span class="sxs-lookup"><span data-stu-id="02488-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="02488-124">Datos reais creados cando se confirma unha factura correctiva</span><span class="sxs-lookup"><span data-stu-id="02488-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="02488-125">A seguinte táboa indica os datos reais que se crean cando se confirma unha factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="02488-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="02488-126">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="02488-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="02488-127">
                    <strong>Datos reais creados na confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="02488-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="02488-128">Confirme a corrección dun adianto ou retención facturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="02488-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-129">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="02488-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="02488-130">Este importe é positivo porque está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.</span><span class="sxs-lookup"><span data-stu-id="02488-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-131">Créase un dato real de reversión das vendas facturadas polo importe da retención ou o adianto para reverter as vendas facturadas orixinais.</span><span class="sxs-lookup"><span data-stu-id="02488-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-132">Créase un novo dato real de vendas facturadas para o importe corrixido da liña de factura corrixida baseada en retención ou adianto.</span><span class="sxs-lookup"><span data-stu-id="02488-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-133">Un dato real de vendas non facturadas dun importe negativo da liña de factura corrixida baseada en retención ou adianto, que se utilizará para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="02488-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="02488-134">Unha confirmación da corrección dunha retención ou un adianto conciliado previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-135">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="02488-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="02488-136">Este importe é positivo e está destinado a cancelar o negativo que se creou cando se produciu a conciliación previa.</span><span class="sxs-lookup"><span data-stu-id="02488-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-137">Un dato real de inversión das vendas facturadas polo importe da factura previa.</span><span class="sxs-lookup"><span data-stu-id="02488-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-138">Créase un novo dato real de vendas facturadas para o importe da retención que se aplica na factura corrixida.</span><span class="sxs-lookup"><span data-stu-id="02488-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-139">Un dato real de vendas non facturadas cun importe negativo da retención ou o adianto sobrante corrixido, que se utilizará para a conciliación de facturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="02488-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02488-140">Facturación do abono total dunha transacción de tempo facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-141">Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="02488-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-142">Un novo dato real de vendas sen facturar por horas e importe no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="02488-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="02488-143">Facturación do abono parcial nunha transacción temporal.</span><span class="sxs-lookup"><span data-stu-id="02488-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-144">Unha reversión de vendas facturadas por horas e importe facturados no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="02488-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-145">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="02488-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-146">Un novo dato real de vendas sen facturar que é imputable para as horas e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="02488-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02488-147">Facturación do abono total dunha transacción de gasto facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-148">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.</span><span class="sxs-lookup"><span data-stu-id="02488-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-149">Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.</span><span class="sxs-lookup"><span data-stu-id="02488-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="02488-150">Facturación do abono parcial dunha transacción de gasto facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-151">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para un gasto.</span><span class="sxs-lookup"><span data-stu-id="02488-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-152">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura corrixida, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="02488-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-153">Un novo dato real de vendas sen facturar que é imputable para a cantidade e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="02488-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02488-154">Facturación do crédito total dunha transacción de material facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-155">Unha reversión das vendas facturadas para a cantidade e o importe no detalle da liña de factura para material.</span><span class="sxs-lookup"><span data-stu-id="02488-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-156">Un novo dato real de vendas sen facturar para a cantidade e o importe no detalle da liña de factura para material.</span><span class="sxs-lookup"><span data-stu-id="02488-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="02488-157">Facturación do crédito parcial dunha transacción de material.</span><span class="sxs-lookup"><span data-stu-id="02488-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-158">Unha reversión das vendas facturadas para a cantidade e o importe facturados no detalle da liña de factura para material.</span><span class="sxs-lookup"><span data-stu-id="02488-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-159">Un novo dato real de vendas sen facturar que é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión desta e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="02488-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-160">Un novo dato real de vendas sen facturar que é imputable para a cantidade e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="02488-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02488-161">Facturación do abono total dunha transacción de taxa facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-162">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="02488-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-163">Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="02488-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02488-164">Facturación do abono parcial dunha transacción de taxa facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-165">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="02488-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-166">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura correctiva editada, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="02488-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="02488-167">Facturación do abono total dunha transacción de fito facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-168">Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para o fito.</span><span class="sxs-lookup"><span data-stu-id="02488-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="02488-169">O estado da factura do fito actualízase desde <b>Factura do cliente contabilizada</b> a <b>Listo para facturar</b>.</span><span class="sxs-lookup"><span data-stu-id="02488-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="02488-170">Facturación do abono parcial dunha transacción de fito facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="02488-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-171">Non compatible</span><span class="sxs-lookup"><span data-stu-id="02488-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="02488-172">Créditos e correccións dunha liña de contrato baseado en produto previamente facturada.</span><span class="sxs-lookup"><span data-stu-id="02488-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02488-173">Non compatible</span><span class="sxs-lookup"><span data-stu-id="02488-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
