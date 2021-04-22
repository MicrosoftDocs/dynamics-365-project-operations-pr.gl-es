---
title: Crear facturas baseadas en proxecto correctivas
description: Este tema ofrece información sobre as facturas correctivas en Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788854"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="2d07f-103">Crear facturas baseadas en proxecto correctivas</span><span class="sxs-lookup"><span data-stu-id="2d07f-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="2d07f-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="2d07f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2d07f-105">Pódese corrixir unha factura de proxecto confirmada para procesar cambios ou créditos segundo se negociaron co cliente e o xestor do proxecto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="2d07f-106">Para editar unha factura confirmada, abra a factura confirmada e seleccione **Corrixir esta factura**.</span><span class="sxs-lookup"><span data-stu-id="2d07f-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2d07f-107">Esta selección non está dispoñible a menos que se confirme unha factura do proxecto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="2d07f-108">A partir da factura confirmada créase un novo borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="2d07f-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="2d07f-109">Todos os detalles da liña de factura da factura confirmada anteriormente copianse no novo borrador.</span><span class="sxs-lookup"><span data-stu-id="2d07f-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="2d07f-110">Os seguintes son algúns puntos clave para axudar a comprender mellor os detalles da liña na nova factura corrixida:</span><span class="sxs-lookup"><span data-stu-id="2d07f-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="2d07f-111">Todas as cantidades actualízanse a cero.</span><span class="sxs-lookup"><span data-stu-id="2d07f-111">All quantities are updated to zero.</span></span> <span data-ttu-id="2d07f-112">Isto supón que todos os elementos facturados están totalmente abonados.</span><span class="sxs-lookup"><span data-stu-id="2d07f-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="2d07f-113">Se é necesario, pode actualizar manualmente estas cantidades para reflectir a cantidade que se está a facturar e non a cantidade que se vai aboar.</span><span class="sxs-lookup"><span data-stu-id="2d07f-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="2d07f-114">En función da cantidade que introduza, a aplicación calcula a cantidade aboada.</span><span class="sxs-lookup"><span data-stu-id="2d07f-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="2d07f-115">Este importe reflíctese nos datos reais que se crean cando se confirma a factura corrixida.</span><span class="sxs-lookup"><span data-stu-id="2d07f-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="2d07f-116">Se está a facer cambios no importe do imposto, debe ingresar o importe do imposto correcto e non o importe do imposto que vai aboar.</span><span class="sxs-lookup"><span data-stu-id="2d07f-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="2d07f-117">As correccións de fitos sempre se procesan como abonos completos.</span><span class="sxs-lookup"><span data-stu-id="2d07f-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="2d07f-118">Os importes de retencións ou adiantos pódense corrixir se se facturou ao cliente un importe incorrecto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="2d07f-119">As conciliacións de retencións e adiantos pódense corrixir se se utilizou un importe incorrecto para conciliar os cargos dunha factura confirmada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d07f-120">Os detalles da liña de factura que son correccións doutros cargos xa facturados teñen o campo **Corrección** campo definido como **Si**.</span><span class="sxs-lookup"><span data-stu-id="2d07f-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="2d07f-121">As facturas que corrixiron os detalles da liña de factura teñen un campo chamado **Ten correccións** que tamén está establecido en **Si**.</span><span class="sxs-lookup"><span data-stu-id="2d07f-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="2d07f-122">Datos reais creados na confirmación dunha factura correctiva</span><span class="sxs-lookup"><span data-stu-id="2d07f-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="2d07f-123">A seguinte táboa indica os datos reais que se crean cando se confirma unha factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="2d07f-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="2d07f-124">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d07f-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="2d07f-125">
                    <strong>Datos reais creados na confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d07f-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2d07f-126">Confirme a corrección dun adianto ou retención facturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d07f-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-127">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="2d07f-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2d07f-128">Este importe é positivo porque está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-129">Créase un dato real de reversión das vendas facturadas polo importe da retención ou o adianto para reverter as vendas facturadas orixinais.</span><span class="sxs-lookup"><span data-stu-id="2d07f-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-130">Créase un novo dato real de vendas facturadas para o importe corrixido da liña de factura corrixida baseada en retención ou adianto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-131">Un dato real de vendas non facturadas dun importe negativo da liña de factura corrixida baseada en retención ou adianto, que se utilizará para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="2d07f-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2d07f-132">Unha confirmación da corrección dunha retención ou un adianto conciliado previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-133">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="2d07f-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2d07f-134">Este importe é positivo e está destinado a cancelar o negativo que se creou cando se produciu a conciliación previa.</span><span class="sxs-lookup"><span data-stu-id="2d07f-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-135">Un dato real de inversión das vendas facturadas polo importe da factura previa.</span><span class="sxs-lookup"><span data-stu-id="2d07f-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-136">Créase un novo dato real de vendas facturadas para o importe da retención que se aplica na factura corrixida.</span><span class="sxs-lookup"><span data-stu-id="2d07f-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-137">Un dato real de vendas non facturadas cun importe negativo da retención ou o adianto sobrante corrixido, que se utilizará para a conciliación de facturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="2d07f-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d07f-138">Facturación do abono total dunha transacción de tempo facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-139">Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="2d07f-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-140">Un novo dato real de vendas sen facturar por horas e importe no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="2d07f-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2d07f-141">Facturación do abono parcial nunha transacción temporal.</span><span class="sxs-lookup"><span data-stu-id="2d07f-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-142">Unha reversión de vendas facturadas por horas e importe facturados no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="2d07f-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-143">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-144">Un novo dato real de vendas sen facturar que é imputable para as horas e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="2d07f-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d07f-145">Facturación do abono total dunha transacción de gasto facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-146">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-147">Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2d07f-148">Facturación do abono parcial dunha transacción de gasto facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-149">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para un gasto.</span><span class="sxs-lookup"><span data-stu-id="2d07f-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-150">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura corrixida, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-151">Un novo dato real de vendas sen facturar que é imputable para a cantidade e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="2d07f-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d07f-152">Facturación do abono total dunha transacción de taxa facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-153">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="2d07f-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-154">Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="2d07f-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d07f-155">Facturación do abono parcial dunha transacción de taxa facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-156">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="2d07f-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-157">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura correctiva editada, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2d07f-158">Facturación do abono total dunha transacción de fito facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-159">Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para o fito.</span><span class="sxs-lookup"><span data-stu-id="2d07f-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="2d07f-160">O estado da factura no fito actualízase de <b>Factura do cliente contabilizada</b> a <b>Listo para facturar</b>.</span><span class="sxs-lookup"><span data-stu-id="2d07f-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2d07f-161">Facturación do abono parcial dunha transacción de fito facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d07f-162">Non compatible</span><span class="sxs-lookup"><span data-stu-id="2d07f-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
