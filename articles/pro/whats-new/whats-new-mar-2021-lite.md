---
title: Novidades marzo 2021 - Despregamento de Project Operations lite
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de marzo de 2021 do despregamento de Project Operations lite.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993864"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="4ec66-103">Novidades marzo 2021 - Despregamento de Project Operations lite</span><span class="sxs-lookup"><span data-stu-id="4ec66-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="4ec66-104">_Aplícase a: Despregamento de Lite - acordo para facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="4ec66-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4ec66-105">Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4ec66-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="4ec66-106">Project Operations en ambiente de Dataverse versión 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="4ec66-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="4ec66-107">Actualizacións de calidade</span><span class="sxs-lookup"><span data-stu-id="4ec66-107">Quality updates</span></span>

| <span data-ttu-id="4ec66-108">**Área de funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="4ec66-108">**Feature area**</span></span> | <span data-ttu-id="4ec66-109">**Número de referencia**</span><span class="sxs-lookup"><span data-stu-id="4ec66-109">**Reference number**</span></span> | <span data-ttu-id="4ec66-110">**Actualización de calidade**</span><span class="sxs-lookup"><span data-stu-id="4ec66-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4ec66-111">Facturación e prezos</span><span class="sxs-lookup"><span data-stu-id="4ec66-111">Billing and pricing</span></span> | <span data-ttu-id="4ec66-112">2133873</span><span class="sxs-lookup"><span data-stu-id="4ec66-112">2133873</span></span> | <span data-ttu-id="4ec66-113">Corrixiuse a visualización do símbolo de moeda de **Prezo de venda unitario** na grade **Estimacións de gastos**.</span><span class="sxs-lookup"><span data-stu-id="4ec66-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="4ec66-114">Facturación e prezos</span><span class="sxs-lookup"><span data-stu-id="4ec66-114">Billing and pricing</span></span> | <span data-ttu-id="4ec66-115">2174616</span><span class="sxs-lookup"><span data-stu-id="4ec66-115">2174616</span></span> | <span data-ttu-id="4ec66-116">Cando se gaña unha oferta, faise referencia á lista de prezos personalizada do contrato nos detalles da liña do contrato que se copian da oferta.</span><span class="sxs-lookup"><span data-stu-id="4ec66-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="4ec66-117">Xestión de oportunidades</span><span class="sxs-lookup"><span data-stu-id="4ec66-117">Opportunity Management</span></span> | <span data-ttu-id="4ec66-118">2167475</span><span class="sxs-lookup"><span data-stu-id="4ec66-118">2167475</span></span> | <span data-ttu-id="4ec66-119">Importe fixo do imposto na factura de corrección que orixinou unha entrada real non facturada.</span><span class="sxs-lookup"><span data-stu-id="4ec66-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="4ec66-120">Xestión de oportunidades</span><span class="sxs-lookup"><span data-stu-id="4ec66-120">Opportunity Management</span></span> | <span data-ttu-id="4ec66-121">2176285</span><span class="sxs-lookup"><span data-stu-id="4ec66-121">2176285</span></span> | <span data-ttu-id="4ec66-122">Non se debe copiar o importe do imposto desde os detalles da liña de contrato de vendas/oferta ata os detalles da liña de contrato/oferta.</span><span class="sxs-lookup"><span data-stu-id="4ec66-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="4ec66-123">Xestión de oportunidades</span><span class="sxs-lookup"><span data-stu-id="4ec66-123">Opportunity Management</span></span> | <span data-ttu-id="4ec66-124">2188079</span><span class="sxs-lookup"><span data-stu-id="4ec66-124">2188079</span></span> | <span data-ttu-id="4ec66-125">Non se debe crear a regra de facturación dividida para contratos que non estean baseados en traballo.</span><span class="sxs-lookup"><span data-stu-id="4ec66-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="4ec66-126">Planificación e rastrexo</span><span class="sxs-lookup"><span data-stu-id="4ec66-126">Planning and Tracking</span></span> | <span data-ttu-id="4ec66-127">2138853</span><span class="sxs-lookup"><span data-stu-id="4ec66-127">2138853</span></span> | <span data-ttu-id="4ec66-128">Actualizouse a función de copia do proxecto para garantir que as liñas de estimación de gastos que fan referencia ás tarefas se copian no proxecto de destino.</span><span class="sxs-lookup"><span data-stu-id="4ec66-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="4ec66-129">Planificación e rastrexo</span><span class="sxs-lookup"><span data-stu-id="4ec66-129">Planning and Tracking</span></span> | <span data-ttu-id="4ec66-130">2173259</span><span class="sxs-lookup"><span data-stu-id="4ec66-130">2173259</span></span> | <span data-ttu-id="4ec66-131">Actualizouse a función de copia do proxecto para asegurarse de que non amosa a mensaxe de erro **Copiando WBS** en determinadas situacións.</span><span class="sxs-lookup"><span data-stu-id="4ec66-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="4ec66-132">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="4ec66-132">Time and Expense</span></span> | <span data-ttu-id="4ec66-133">2148910</span><span class="sxs-lookup"><span data-stu-id="4ec66-133">2148910</span></span> | <span data-ttu-id="4ec66-134">Solucionouse un problema de visualización coa páxina **Editar entrada** na grade **Entrada de tempo**.</span><span class="sxs-lookup"><span data-stu-id="4ec66-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="4ec66-135">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="4ec66-135">Time and Expense</span></span> | <span data-ttu-id="4ec66-136">2159798</span><span class="sxs-lookup"><span data-stu-id="4ec66-136">2159798</span></span> | <span data-ttu-id="4ec66-137">Reforzáronse os controis para garantir que non se poidan editar as entradas de gastos aprobadas.</span><span class="sxs-lookup"><span data-stu-id="4ec66-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


