---
title: Configurar os custos estándar de man de obra e gastos
description: Este tema explica como configurar os custos estándar de man de obra e gastos para un proxecto.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751477"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="1670c-103">Configurar os custos estándar de man de obra e gastos</span><span class="sxs-lookup"><span data-stu-id="1670c-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1670c-104">Este tema explica como configurar os custos estándar de man de obra e gastos para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="1670c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="1670c-105">Esta tarefa utiliza o conxunto de datos USSI.</span><span class="sxs-lookup"><span data-stu-id="1670c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1670c-106">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de custo (hora)**.</span><span class="sxs-lookup"><span data-stu-id="1670c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="1670c-107">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="1670c-107">Select **New**.</span></span>
3. <span data-ttu-id="1670c-108">No campo **Data de entrada en vigor**, introduza unha data.</span><span class="sxs-lookup"><span data-stu-id="1670c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="1670c-109">No campo **Prezo de custo**, introduza un número.</span><span class="sxs-lookup"><span data-stu-id="1670c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="1670c-110">Pode configurar un prezo de custo estándar para a categoría de proxecto ou pode configurar un prezo de custo por número de traballador, número de proxecto, categoría, data ou calquera combinación destes.</span><span class="sxs-lookup"><span data-stu-id="1670c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="1670c-111">O prezo de custo que se aplica é o prezo de custo co maior nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="1670c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="1670c-112">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="1670c-112">Select **Save**.</span></span>
6. <span data-ttu-id="1670c-113">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de venda (hora)**.</span><span class="sxs-lookup"><span data-stu-id="1670c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="1670c-114">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="1670c-114">Select **New**.</span></span>
8. <span data-ttu-id="1670c-115">No campo **Data de entrada en vigor**, introduza unha data.</span><span class="sxs-lookup"><span data-stu-id="1670c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="1670c-116">No campo **Válido para**, seleccione unha opción.</span><span class="sxs-lookup"><span data-stu-id="1670c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="1670c-117">No campo **Prezos**, introduza un número.</span><span class="sxs-lookup"><span data-stu-id="1670c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="1670c-118">Pode configurar un prezo de venda estándar para transaccións por horas ou para unha categoría de proxecto.</span><span class="sxs-lookup"><span data-stu-id="1670c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="1670c-119">Tamén pode configurar os prezos de venda por número de traballador, número de proxecto, categoría, data de transacción ou calquera combinación destes.</span><span class="sxs-lookup"><span data-stu-id="1670c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="1670c-120">O prezo de venda real, que se aplica cando un traballador realiza unha transacción no diario de horas, é o prezo de venda co maior nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="1670c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="1670c-121">Por exemplo, se se establecen tanto un prezo de venda xeral como un prezo de venda específico para o traballador, úsase o prezo de venda específico para o traballador.</span><span class="sxs-lookup"><span data-stu-id="1670c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="1670c-122">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="1670c-122">Select **Save**.</span></span>
12. <span data-ttu-id="1670c-123">Peche a páxina.</span><span class="sxs-lookup"><span data-stu-id="1670c-123">Close the page.</span></span>
13. <span data-ttu-id="1670c-124">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de custo (gasto)**.</span><span class="sxs-lookup"><span data-stu-id="1670c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="1670c-125">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="1670c-125">Select **New**.</span></span>
15. <span data-ttu-id="1670c-126">No campo **Data de entrada en vigor**, introduza unha data.</span><span class="sxs-lookup"><span data-stu-id="1670c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="1670c-127">No campo **Prezo de custo**, introduza un número.</span><span class="sxs-lookup"><span data-stu-id="1670c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="1670c-128">Pódense encher varios campos, pero este é o mínimo necesario para gardar o rexistro.</span><span class="sxs-lookup"><span data-stu-id="1670c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="1670c-129">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="1670c-129">Select **Save**.</span></span>
18. <span data-ttu-id="1670c-130">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de venda (gasto)**.</span><span class="sxs-lookup"><span data-stu-id="1670c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="1670c-131">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="1670c-131">Select **New**.</span></span>
20. <span data-ttu-id="1670c-132">No campo **Data de entrada en vigor**, introduza unha data.</span><span class="sxs-lookup"><span data-stu-id="1670c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="1670c-133">No campo **Válido para**, seleccione unha opción.</span><span class="sxs-lookup"><span data-stu-id="1670c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="1670c-134">No campo **Prezos**, introduza un número.</span><span class="sxs-lookup"><span data-stu-id="1670c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="1670c-135">O prezo de venda real, que se aplica cando un traballador introduce trasaccións no diario de gastos, é o prezo de venda co maior nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="1670c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="1670c-136">Por exemplo, se se establecen tanto un prezo de venda xeral como un prezo de venda específico para o traballador, úsase o prezo de venda específico para o traballador.</span><span class="sxs-lookup"><span data-stu-id="1670c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="1670c-137">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="1670c-137">Select **Save**.</span></span>

