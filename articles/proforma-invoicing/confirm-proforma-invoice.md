---
title: Confirmar unha factura proforma
description: Este tema ofrece información sobre a confirmación dunha factura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128101"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="bc163-103">Confirmar unha factura proforma</span><span class="sxs-lookup"><span data-stu-id="bc163-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="bc163-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="bc163-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bc163-105">Despois de confirmarse unha factura proforma, o estado da factura do proxecto actualízase a **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="bc163-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="bc163-106">Cando se confirma unha factura, convértese en de só lectura.</span><span class="sxs-lookup"><span data-stu-id="bc163-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="bc163-107">No futuro, a factura só se poderá corrixir se hai correccións ou créditos iniciados polo cliente ou cando se marca como pagada.</span><span class="sxs-lookup"><span data-stu-id="bc163-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="bc163-108">A seguinte táboa mostra os datos reais creados polo sistema.</span><span class="sxs-lookup"><span data-stu-id="bc163-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="bc163-109">Estes datos actuais créanse cando se realizan determinadas operacións no borrador da factura do proxecto antes de que se confirme.</span><span class="sxs-lookup"><span data-stu-id="bc163-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="bc163-110">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc163-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="bc163-111">
                    <strong>Datos reais creados na confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc163-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bc163-112">Facturación dunha transacción de tempo sen modificacións no borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="bc163-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-113">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-114">Un dato real de vendas facturadas por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bc163-115">Facturación dunha transacción temporal editada para reducir a cantidade.</span><span class="sxs-lookup"><span data-stu-id="bc163-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-116">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-117">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="bc163-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-118">Un novo dato real de vendas sen facturar que non é imputable polas horas e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="bc163-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bc163-119">Facturación dunha transacción temporal editada para aumentar a cantidade.</span><span class="sxs-lookup"><span data-stu-id="bc163-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-120">Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-121">Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="bc163-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bc163-122">Facturación dunha transacción de gasto sen modificacións no borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="bc163-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-123">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-124">Un dato real de vendas facturadas pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bc163-125">Facturación dunha transacción de gasto que foi editada para reducir a cantidade.</span><span class="sxs-lookup"><span data-stu-id="bc163-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-126">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-127">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="bc163-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-128">Un novo dato real de vendas sen facturar que non é imputable pola cantidade e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="bc163-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bc163-129">Facturación dunha transacción de gasto que foi editada para aumentar a cantidade.</span><span class="sxs-lookup"><span data-stu-id="bc163-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-130">Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-131">Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="bc163-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bc163-132">Facturación dunha taxa.</span><span class="sxs-lookup"><span data-stu-id="bc163-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-133">Unha reversión de vendas sen facturar polo importe da taxa na liña de diario.</span><span class="sxs-lookup"><span data-stu-id="bc163-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-134">Un dato real de vendas facturadas pola cantidade e o importe na liña de diario da taxa orixinal.</span><span class="sxs-lookup"><span data-stu-id="bc163-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="bc163-135">Facturación dun fito.</span><span class="sxs-lookup"><span data-stu-id="bc163-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bc163-136">Un dato real de vendas facturadas polo importe do fito no fito orixinal da liña de contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="bc163-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
