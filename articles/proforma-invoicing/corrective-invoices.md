---
title: Facturas baseadas en proxecto correctivas
description: Este tema ofrece información sobre como crear e confirmar facturas baseadas en proxecto correctivas en Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867039"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="203d7-103">Facturas baseadas en proxecto correctivas</span><span class="sxs-lookup"><span data-stu-id="203d7-103">Corrective project-based invoices</span></span>

<span data-ttu-id="203d7-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="203d7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="203d7-105">Pódese corrixir unha factura de proxecto confirmada para procesar cambios ou créditos segundo se negociaron co cliente e o xestor do proxecto.</span><span class="sxs-lookup"><span data-stu-id="203d7-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="203d7-106">Para editar unha factura confirmada, abra a factura confirmada e seleccione **Corrixir esta factura**.</span><span class="sxs-lookup"><span data-stu-id="203d7-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="203d7-107">Esta selección non está dispoñible a menos que se confirme unha factura do proxecto ou a factura baseada en proxecto conteña adiantos ou retencións ou conciliacións de adiantos ou retencións.</span><span class="sxs-lookup"><span data-stu-id="203d7-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="203d7-108">A partir da factura confirmada créase un novo borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="203d7-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="203d7-109">Todos os detalles da liña de factura da factura confirmada anteriormente copianse no novo borrador.</span><span class="sxs-lookup"><span data-stu-id="203d7-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="203d7-110">Os seguintes son algúns dos puntos clave para comprender os detalles da liña da nova factura corrixida:</span><span class="sxs-lookup"><span data-stu-id="203d7-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="203d7-111">Todas as cantidades actualízanse a cero.</span><span class="sxs-lookup"><span data-stu-id="203d7-111">All quantities are updated to zero.</span></span> <span data-ttu-id="203d7-112">Dynamics 365 Project Operations supón que todos os elementos facturados están totalmente abonados.</span><span class="sxs-lookup"><span data-stu-id="203d7-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="203d7-113">Se é necesario, pode actualizar manualmente estas cantidades para reflectir a cantidade que se está a facturar e non a cantidade que se vai aboar.</span><span class="sxs-lookup"><span data-stu-id="203d7-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="203d7-114">En función da cantidade que introduza, a aplicación calcula a cantidade aboada.</span><span class="sxs-lookup"><span data-stu-id="203d7-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="203d7-115">Este importe reflíctese nos datos reais que se crean cando se confirma a factura corrixida.</span><span class="sxs-lookup"><span data-stu-id="203d7-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="203d7-116">Se está a facer cambios no importe do imposto, debe ingresar o importe do imposto correcto e non o importe do imposto que vai aboar.</span><span class="sxs-lookup"><span data-stu-id="203d7-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="203d7-117">As correccións de fitos sempre se procesan como abonos completos.</span><span class="sxs-lookup"><span data-stu-id="203d7-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="203d7-118">Para os detalles da liña de factura que son correccións doutros cargos xa facturados, o campo **Corrección** está definido como **Si**.</span><span class="sxs-lookup"><span data-stu-id="203d7-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="203d7-119">Para facturas que teñen os detalles da liña de factura corrixidos, o campo **Ten correccións** está definido como **Si**.</span><span class="sxs-lookup"><span data-stu-id="203d7-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="203d7-120">Datos reais creados cando se confirma unha factura correctiva</span><span class="sxs-lookup"><span data-stu-id="203d7-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="203d7-121">A seguinte táboa indica os datos reais que se crean cando se confirma unha factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="203d7-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="203d7-122">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="203d7-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="203d7-123">
                    <strong>Datos reais creados na confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="203d7-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="203d7-124">Facturación do abono total dunha transacción de tempo facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-125">Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="203d7-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-126">Un novo dato real de vendas sen facturar por horas e importe no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="203d7-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="203d7-127">Facturación do abono parcial nunha transacción temporal.</span><span class="sxs-lookup"><span data-stu-id="203d7-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-128">Unha reversión de vendas facturadas por horas e importe facturados no detalle da liña de factura orixinal para tempo.</span><span class="sxs-lookup"><span data-stu-id="203d7-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-129">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="203d7-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-130">Un novo dato real de vendas sen facturar que é imputable para as horas e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="203d7-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="203d7-131">Facturación do abono total dunha transacción de gasto facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-132">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.</span><span class="sxs-lookup"><span data-stu-id="203d7-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-133">Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.</span><span class="sxs-lookup"><span data-stu-id="203d7-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="203d7-134">Facturación do abono parcial dunha transacción de gasto facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-135">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para un gasto.</span><span class="sxs-lookup"><span data-stu-id="203d7-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-136">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura corrixida, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="203d7-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-137">Un novo dato real de vendas sen facturar que é imputable para a cantidade e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="203d7-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="203d7-138">Facturación do crédito total dunha transacción de material facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-139">Unha reversión das vendas facturadas para a cantidade e o importe no detalle da liña de factura para material.</span><span class="sxs-lookup"><span data-stu-id="203d7-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-140">Un novo dato real de vendas sen facturar para a cantidade e o importe no detalle da liña de factura para material.</span><span class="sxs-lookup"><span data-stu-id="203d7-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="203d7-141">Facturación do crédito parcial dunha transacción de material.</span><span class="sxs-lookup"><span data-stu-id="203d7-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-142">Unha reversión das vendas facturadas para a cantidade e o importe facturados no detalle da liña de factura para material.</span><span class="sxs-lookup"><span data-stu-id="203d7-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-143">Un novo dato real de vendas sen facturar que é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión desta e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="203d7-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-144">Un novo dato real de vendas sen facturar que é imputable para a cantidade e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="203d7-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="203d7-145">Facturación do abono total dunha transacción de taxa facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-146">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="203d7-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-147">Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="203d7-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="203d7-148">Facturación do abono parcial dunha transacción de taxa facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-149">Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.</span><span class="sxs-lookup"><span data-stu-id="203d7-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-150">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura correctiva editada, unha reversión disto e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="203d7-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="203d7-151">Facturación do abono total dunha transacción de fito facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-152">Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para o fito.</span><span class="sxs-lookup"><span data-stu-id="203d7-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="203d7-153">O estado da factura do fito actualízase desde <b>Factura do cliente contabilizada</b> a <b>Listo para facturar</b>.</span><span class="sxs-lookup"><span data-stu-id="203d7-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="203d7-154">Facturación do abono parcial dunha transacción de fito facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="203d7-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="203d7-155">Non se admite este escenario.</span><span class="sxs-lookup"><span data-stu-id="203d7-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
