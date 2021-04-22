---
title: Confirmar unha factura proforma de proxecto
description: Este tema ofrece información sobre a confirmación das facturas proforma do proxecto en Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867084"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="2c45b-103">Confirmar unha factura proforma de proxecto</span><span class="sxs-lookup"><span data-stu-id="2c45b-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="2c45b-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="2c45b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2c45b-105">Despois de confirmarse unha factura proforma, o estado da factura do proxecto actualízase a **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="2c45b-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="2c45b-106">Cando se confirma unha factura, convértese en de só lectura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="2c45b-107">No futuro, a factura só se poderá corrixir se hai correccións iniciadas polo cliente ou créditos.</span><span class="sxs-lookup"><span data-stu-id="2c45b-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="2c45b-108">A seguinte táboa mostra os datos reais creados polo sistema.</span><span class="sxs-lookup"><span data-stu-id="2c45b-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="2c45b-109">Estes datos actuais créanse cando se realizan determinadas operacións no borrador da factura do proxecto antes de que se confirme.</span><span class="sxs-lookup"><span data-stu-id="2c45b-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="2c45b-110">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2c45b-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="2c45b-111">
                    <strong>Datos reais creados na confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2c45b-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-112">Facturación dunha retención ou un adianto</span><span class="sxs-lookup"><span data-stu-id="2c45b-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-113">Un dato real de vendas facturadas de tipo <strong>Retención</strong> créase polo importe do adianto ou da retención.</span><span class="sxs-lookup"><span data-stu-id="2c45b-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-114">Un dato real de vendas non facturadas dun importe negativo da retención ou do adianto que se utilizará para a conciliación</span><span class="sxs-lookup"><span data-stu-id="2c45b-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-115">Despois de conciliar completamente unha retención ou un adianto nunha factura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-116">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="2c45b-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2c45b-117">Este importe é positivo xa que está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.</span><span class="sxs-lookup"><span data-stu-id="2c45b-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-118">Un dato real das vendas facturadas polo importe desta factura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2c45b-119">Despois de conciliar parcialmente unha retención ou un adianto nunha factura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-120">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="2c45b-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2c45b-121">Este importe é positivo xa que está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.</span><span class="sxs-lookup"><span data-stu-id="2c45b-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-122">Un dato real das vendas facturadas polo importe desta factura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-123">Un dato real de vendas non facturadas negativo do importe restante da retención ou do adianto que se utilizará para a conciliación en futuras facturas.</span><span class="sxs-lookup"><span data-stu-id="2c45b-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-124">Facturación dunha transacción de tempo sen modificacións no borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-125">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-126">Un dato real de vendas facturadas por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2c45b-127">Facturación dunha transacción temporal editada para reducir a cantidade.</span><span class="sxs-lookup"><span data-stu-id="2c45b-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-128">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-129">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-130">Un novo dato real de vendas sen facturar que non é imputable polas horas e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-131">Facturación dunha transacción temporal editada para aumentar a cantidade.</span><span class="sxs-lookup"><span data-stu-id="2c45b-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-132">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-133">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-134">Facturación dunha transacción de gasto sen modificacións no borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-135">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-136">Un dato real de vendas facturadas pola cantidade e o importe na aprobación de gasto orixinal</span><span class="sxs-lookup"><span data-stu-id="2c45b-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2c45b-137">Facturación dunha transacción de gasto que foi editada para reducir a cantidade.</span><span class="sxs-lookup"><span data-stu-id="2c45b-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-138">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-139">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-140">Un novo dato real de vendas sen facturar que non é imputable pola cantidade e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-141">Facturación dunha transacción de gasto que foi editada para aumentar a cantidade.</span><span class="sxs-lookup"><span data-stu-id="2c45b-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-142">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-143">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-144">Facturación dunha transacción de material sen modificacións no borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="2c45b-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-145">Unha reversión das vendas sen facturar para a cantidade e o importe na aprobación de uso de material orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-146">Un dato real das vendas facturadas para a cantidade e o importe na aprobación de uso de material orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2c45b-147">Facturación dunha transacción de material que se editou para reducir a cantidade.</span><span class="sxs-lookup"><span data-stu-id="2c45b-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-148">Unha reversión das vendas sen facturar para a cantidade e o importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-149">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-150">Un novo dato real de vendas sen facturar que non é imputable pola cantidade e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-151">Facturación dunha transacción de material que se editou para aumentar a cantidade.</span><span class="sxs-lookup"><span data-stu-id="2c45b-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-152">Unha reversión das vendas sen facturar para a cantidade e o importe na aprobación de uso de material orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-153">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="2c45b-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c45b-154">Facturación dunha taxa.</span><span class="sxs-lookup"><span data-stu-id="2c45b-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-155">Unha reversión de vendas sen facturar polo importe da taxa na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="2c45b-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-156">Un dato real de vendas facturadas pola cantidade e o importe na liña de diario da taxa orixinal.</span><span class="sxs-lookup"><span data-stu-id="2c45b-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2c45b-157">Facturación dun fito.</span><span class="sxs-lookup"><span data-stu-id="2c45b-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-158">Un dato real de vendas facturadas polo importe do fito no fito orixinal da liña de contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="2c45b-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2c45b-159">Facturación dunha liña de contrato baseado en produto.</span><span class="sxs-lookup"><span data-stu-id="2c45b-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c45b-160">Un dato real de vendas facturadas para a liña de produto coa cantidade e importe procedentes da liña de contrato baseado en produto.</span><span class="sxs-lookup"><span data-stu-id="2c45b-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
