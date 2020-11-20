---
title: Confirmar unha factura proforma - lite
description: Este tema ofrece información sobre a confirmación de facturas proforma en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176519"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="411b4-103">Confirmar unha factura proforma - lite</span><span class="sxs-lookup"><span data-stu-id="411b4-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="411b4-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="411b4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="411b4-105">Despois de confirmarse unha factura proforma, o estado da factura do proxecto actualízase a **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="411b4-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="411b4-106">Cando se confirma unha factura, convértese en de só lectura.</span><span class="sxs-lookup"><span data-stu-id="411b4-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="411b4-107">No futuro, a factura só se poderá corrixir se hai correccións ou créditos iniciados polo cliente ou se a factura está marcada como pagada.</span><span class="sxs-lookup"><span data-stu-id="411b4-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="411b4-108">A seguinte táboa mostra os datos reais creados polo sistema.</span><span class="sxs-lookup"><span data-stu-id="411b4-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="411b4-109">Estes datos actuais créanse cando se realizan determinadas operacións no borrador da factura do proxecto antes de que se confirme.</span><span class="sxs-lookup"><span data-stu-id="411b4-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="411b4-110">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="411b4-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="411b4-111">
                    <strong>Datos reais creados na confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="411b4-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="411b4-112">Facturación dunha retención ou un adianto</span><span class="sxs-lookup"><span data-stu-id="411b4-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-113">Un dato real de vendas facturadas de tipo <strong>Retención</strong> créase polo importe do adianto ou da retención.</span><span class="sxs-lookup"><span data-stu-id="411b4-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-114">Un dato real de vendas non facturadas dun importe negativo da retención ou do adianto que se utilizará para a conciliación</span><span class="sxs-lookup"><span data-stu-id="411b4-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="411b4-115">Despois de conciliar completamente unha retención ou un adianto nunha factura.</span><span class="sxs-lookup"><span data-stu-id="411b4-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-116">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="411b4-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="411b4-117">Este importe é positivo xa que está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.</span><span class="sxs-lookup"><span data-stu-id="411b4-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-118">Un dato real das vendas facturadas polo importe desta factura.</span><span class="sxs-lookup"><span data-stu-id="411b4-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="411b4-119">Despois de conciliar parcialmente unha retención ou un adianto nunha factura.</span><span class="sxs-lookup"><span data-stu-id="411b4-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-120">Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación.</span><span class="sxs-lookup"><span data-stu-id="411b4-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="411b4-121">Este importe é positivo xa que está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.</span><span class="sxs-lookup"><span data-stu-id="411b4-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-122">Un dato real das vendas facturadas polo importe desta factura.</span><span class="sxs-lookup"><span data-stu-id="411b4-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-123">Un dato real de vendas non facturadas negativo do importe restante da retención ou do adianto que se utilizará para a conciliación en futuras facturas.</span><span class="sxs-lookup"><span data-stu-id="411b4-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="411b4-124">Facturación dunha transacción de tempo sen modificacións no borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="411b4-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-125">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-126">Un dato real de vendas facturadas por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="411b4-127">Facturación dunha transacción temporal editada para reducir a cantidade.</span><span class="sxs-lookup"><span data-stu-id="411b4-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-128">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-129">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="411b4-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-130">Un novo dato real de vendas sen facturar que non é imputable polas horas e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="411b4-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="411b4-131">Facturación dunha transacción temporal editada para aumentar a cantidade.</span><span class="sxs-lookup"><span data-stu-id="411b4-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-132">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-133">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="411b4-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="411b4-134">Facturación dunha transacción de gasto sen modificacións no borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="411b4-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-135">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-136">Un dato real de vendas facturadas pola cantidade e o importe na aprobación de gasto orixinal</span><span class="sxs-lookup"><span data-stu-id="411b4-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="411b4-137">Facturación dunha transacción de gasto que foi editada para reducir a cantidade.</span><span class="sxs-lookup"><span data-stu-id="411b4-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-138">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-139">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="411b4-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-140">Un novo dato real de vendas sen facturar que non é imputable pola cantidade e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="411b4-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="411b4-141">Facturación dunha transacción de gasto que foi editada para aumentar a cantidade.</span><span class="sxs-lookup"><span data-stu-id="411b4-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-142">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-143">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="411b4-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="411b4-144">Facturación dunha taxa.</span><span class="sxs-lookup"><span data-stu-id="411b4-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-145">Unha reversión de vendas sen facturar polo importe da taxa na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="411b4-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-146">Un dato real de vendas facturadas pola cantidade e o importe na liña de diario da taxa orixinal.</span><span class="sxs-lookup"><span data-stu-id="411b4-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="411b4-147">Facturación dun fito.</span><span class="sxs-lookup"><span data-stu-id="411b4-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-148">Un dato real de vendas facturadas polo importe do fito no fito orixinal da liña de contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="411b4-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="411b4-149">Facturación dunha liña de contrato baseado en produto.</span><span class="sxs-lookup"><span data-stu-id="411b4-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="411b4-150">Un dato real de vendas facturadas para a liña de produto coa cantidade e importe procedentes da liña de contrato baseado en produto.</span><span class="sxs-lookup"><span data-stu-id="411b4-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
