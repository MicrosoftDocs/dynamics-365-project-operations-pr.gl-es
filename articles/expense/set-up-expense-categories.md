---
title: Configurar categorías de gasto
description: Este tema ofrece información sobre como configurar categorías de gastos e categorías compartidas para os informes de gastos.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076022"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="a54ab-103">Configurar categorías de gasto</span><span class="sxs-lookup"><span data-stu-id="a54ab-103">Set up expense categories</span></span>

<span data-ttu-id="a54ab-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="a54ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a54ab-105">Cando os empregados crean informes de gastos, cada gasto que rexistran debe asociarse a unha categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="a54ab-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="a54ab-106">As categorías de gastos derivan de categorías compartidas que se poden compartir entre as entidades legais da súa organización.</span><span class="sxs-lookup"><span data-stu-id="a54ab-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="a54ab-107">Dependendo de como se defina a súa organización, estas categorías de gastos tamén se poden compartir noutras áreas.</span><span class="sxs-lookup"><span data-stu-id="a54ab-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="a54ab-108">En función da definición da súa organización e das orientacións do equipo de implementación, debe determinar se as categorías que se usan na xestión de gastos só se usarán na xestión de gastos ou se deben compartir noutras áreas.</span><span class="sxs-lookup"><span data-stu-id="a54ab-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="a54ab-109">Estas categorías pódense compartir entre xestión e contabilidade de proxectos e xestión de gastos ou entre xestión e contabilidade de proxectos e produción.</span><span class="sxs-lookup"><span data-stu-id="a54ab-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="a54ab-110">Non obstante, non se poden compartir entre xestión de gastos e produción.</span><span class="sxs-lookup"><span data-stu-id="a54ab-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="a54ab-111">Antes de comezar o proceso de configuración, deben tomarse as seguintes decisións para cada categoría de gastos:</span><span class="sxs-lookup"><span data-stu-id="a54ab-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="a54ab-112">Que é a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-112">What is the expense category?</span></span> <span data-ttu-id="a54ab-113">Entre os exemplos inclúense as categorías de voos, hotel ou quilometraxe.</span><span class="sxs-lookup"><span data-stu-id="a54ab-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="a54ab-114">A categoría de gasto tamén se pode usar na xestión e contabilidade de proxectos?</span><span class="sxs-lookup"><span data-stu-id="a54ab-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="a54ab-115">Se pode usarse, tamén debe tomar as seguintes decisións:</span><span class="sxs-lookup"><span data-stu-id="a54ab-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="a54ab-116">Que contas de custos se utilizarán para os seguintes gastos?</span><span class="sxs-lookup"><span data-stu-id="a54ab-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="a54ab-117">Custo</span><span class="sxs-lookup"><span data-stu-id="a54ab-117">Cost</span></span>
        - <span data-ttu-id="a54ab-118">Asignación de nóminas</span><span class="sxs-lookup"><span data-stu-id="a54ab-118">Payroll allocation</span></span>
        - <span data-ttu-id="a54ab-119">WIP-valor de custo</span><span class="sxs-lookup"><span data-stu-id="a54ab-119">WIP-cost value</span></span>
        - <span data-ttu-id="a54ab-120">Elemento de custo</span><span class="sxs-lookup"><span data-stu-id="a54ab-120">Cost-item</span></span>
        - <span data-ttu-id="a54ab-121">WIP-elemento de valor de custo</span><span class="sxs-lookup"><span data-stu-id="a54ab-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="a54ab-122">Perda acumulada</span><span class="sxs-lookup"><span data-stu-id="a54ab-122">Accrued loss</span></span>
        - <span data-ttu-id="a54ab-123">WIP-perda acumulada</span><span class="sxs-lookup"><span data-stu-id="a54ab-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="a54ab-124">Que contas de ingresos se utilizarán para as seguintes fontes de ingresos?</span><span class="sxs-lookup"><span data-stu-id="a54ab-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="a54ab-125">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="a54ab-125">Invoiced revenue</span></span>
        - <span data-ttu-id="a54ab-126">Ingresos acumulados-valor de vendas</span><span class="sxs-lookup"><span data-stu-id="a54ab-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="a54ab-127">WIP-valor de vendas</span><span class="sxs-lookup"><span data-stu-id="a54ab-127">WIP-sales value</span></span>
        - <span data-ttu-id="a54ab-128">Ingresos acumulados-produción</span><span class="sxs-lookup"><span data-stu-id="a54ab-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="a54ab-129">WIP-produción</span><span class="sxs-lookup"><span data-stu-id="a54ab-129">WIP-production</span></span>
        - <span data-ttu-id="a54ab-130">Ingresos acumulados-beneficio</span><span class="sxs-lookup"><span data-stu-id="a54ab-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="a54ab-131">WIP-beneficio</span><span class="sxs-lookup"><span data-stu-id="a54ab-131">WIP-profit</span></span>
        - <span data-ttu-id="a54ab-132">Ingresos acumulados-subscrición</span><span class="sxs-lookup"><span data-stu-id="a54ab-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="a54ab-133">WIP-subscrición</span><span class="sxs-lookup"><span data-stu-id="a54ab-133">WIP-subscription</span></span>

- <span data-ttu-id="a54ab-134">Que é o tipo de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-134">What is the expense type?</span></span>
- <span data-ttu-id="a54ab-135">Cal é o método de pagamento predefinido para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="a54ab-136">Hai que detallar os gastos da categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="a54ab-137">Cal é a principal conta predefinida para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="a54ab-138">Cal é o grupo predeterminado do imposto sobre as vendas para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="a54ab-139">Permítense métodos adicionais de pagamento para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="a54ab-140">Se é así, cales son?</span><span class="sxs-lookup"><span data-stu-id="a54ab-140">If so, what are they?</span></span>
- <span data-ttu-id="a54ab-141">Hai subcategorías nesta categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a54ab-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="a54ab-142">Se hai subcategorías, tamén debe tomar as seguintes decisións:</span><span class="sxs-lookup"><span data-stu-id="a54ab-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="a54ab-143">Está excluída algunha das subcategorías da recuperación de impostos?</span><span class="sxs-lookup"><span data-stu-id="a54ab-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="a54ab-144">Cal é o grupo do imposto sobre as vendas das subcategorías?</span><span class="sxs-lookup"><span data-stu-id="a54ab-144">What is the item sales tax group of the subcategories?</span></span>
