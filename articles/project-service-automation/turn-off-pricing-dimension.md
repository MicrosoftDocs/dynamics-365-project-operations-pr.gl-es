---
title: Desactivar unha dimensión de prezos
description: Este tema mostra como configurar as dimensións de prezos na solución Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751424"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="6d548-103">Desactivar unha dimensión de prezos</span><span class="sxs-lookup"><span data-stu-id="6d548-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="6d548-104">Pode que necesite revisar e actualizar a súa estratexia de prezos cada poucos anos.</span><span class="sxs-lookup"><span data-stu-id="6d548-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="6d548-105">Todas as actualizacións que faga pode requirir que desactive unha dimensión de prezos existente e cree unha nova.</span><span class="sxs-lookup"><span data-stu-id="6d548-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="6d548-106">Por exemplo, pode ter un prezo anterior por **Rol**, pero agora decidiu establecer os prezos por **Experiencia laboral**.</span><span class="sxs-lookup"><span data-stu-id="6d548-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="6d548-107">Isto pode requirir que desactive **Rol** como dimensión de prezos e cree **Experiencia laboral** como unha nova dimensión de prezos.</span><span class="sxs-lookup"><span data-stu-id="6d548-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="6d548-108">Para desactivar unha dimensión de prezos, independentemente de se é lista para usar ou personalizada, pode configurar os campos **Aplicable ao custo** e **Aplicable ás vendas** da dimensión de prezos en **Non**.</span><span class="sxs-lookup"><span data-stu-id="6d548-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="6d548-109">Non obstante, cando faga isto, pode que reciba a seguinte mensaxe de erro.</span><span class="sxs-lookup"><span data-stu-id="6d548-109">However, when you do this, you might receive the following error message.</span></span>

![Erro de proceso de negocio ao desactivar unha dimensión de prezos](media/Business-Process-Error.png)


<span data-ttu-id="6d548-111">Esta mensaxe de erro indica que hai rexistros de prezos previamente configurados para a dimensión que se vai desactivar.</span><span class="sxs-lookup"><span data-stu-id="6d548-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="6d548-112">Todos os rexistros de **Prezo de rol** e **Sobreprezo de rol** que fan referencia a unha dimensión deben ser eliminados antes de que se poida establecer a aplicabilidade da dimensión en **Non**.</span><span class="sxs-lookup"><span data-stu-id="6d548-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="6d548-113">Esta regra aplícase tanto ás dimensións de prezos listas para usar como ás dimensións de prezos personalizadas que creou.</span><span class="sxs-lookup"><span data-stu-id="6d548-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="6d548-114">O motivo desta validación é porque Project Service ten unha restrición de que cada rexistro de **Prezo de rol** debe ter unha combinación única de dimensións.</span><span class="sxs-lookup"><span data-stu-id="6d548-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="6d548-115">Por exemplo, nunha lista de prezos chamada **Taxas de custos de EUA 2018**, ten as seguinte filas de **Prezo de rol**.</span><span class="sxs-lookup"><span data-stu-id="6d548-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="6d548-116">Título estándar</span><span class="sxs-lookup"><span data-stu-id="6d548-116">Standard Title</span></span>         | <span data-ttu-id="6d548-117">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="6d548-117">Org Unit</span></span>    |<span data-ttu-id="6d548-118">Unidade</span><span class="sxs-lookup"><span data-stu-id="6d548-118">Unit</span></span>   |<span data-ttu-id="6d548-119">Prezo</span><span class="sxs-lookup"><span data-stu-id="6d548-119">Price</span></span>  |<span data-ttu-id="6d548-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="6d548-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="6d548-121">Enxeñeiro de sistemas</span><span class="sxs-lookup"><span data-stu-id="6d548-121">Systems Engineer</span></span>|<span data-ttu-id="6d548-122">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="6d548-122">Contoso US</span></span>|<span data-ttu-id="6d548-123">Hour</span><span class="sxs-lookup"><span data-stu-id="6d548-123">Hour</span></span>| <span data-ttu-id="6d548-124">100</span><span class="sxs-lookup"><span data-stu-id="6d548-124">100</span></span>|<span data-ttu-id="6d548-125">USD</span><span class="sxs-lookup"><span data-stu-id="6d548-125">USD</span></span>|
| <span data-ttu-id="6d548-126">Enxeñeiro de sistemas sénior</span><span class="sxs-lookup"><span data-stu-id="6d548-126">Senior Systems Engineer</span></span>|<span data-ttu-id="6d548-127">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="6d548-127">Contoso US</span></span>|<span data-ttu-id="6d548-128">Hour</span><span class="sxs-lookup"><span data-stu-id="6d548-128">Hour</span></span>| <span data-ttu-id="6d548-129">150</span><span class="sxs-lookup"><span data-stu-id="6d548-129">150</span></span>| <span data-ttu-id="6d548-130">USD</span><span class="sxs-lookup"><span data-stu-id="6d548-130">USD</span></span>|


<span data-ttu-id="6d548-131">Cando desactive **Título estándar** como dimensión de prezos e o motor de prezos de Project Service busque un prezo, só empregará o valor **Unidade organizativa** do contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="6d548-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="6d548-132">Se a **Unidade organizativa** do contexto de entrada é "Contoso EUA", o resultado non será determinista porque coincidirán as dúas filas.</span><span class="sxs-lookup"><span data-stu-id="6d548-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="6d548-133">Para evitar este escenario, cando cree rexistros de **Prezo de rol**, Project Service valida que a combinación de dimensións é única.</span><span class="sxs-lookup"><span data-stu-id="6d548-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="6d548-134">Se a dimensión está desactivada despois da creación de rexistros de **Prezo de rol**, pódese violar esta restrición.</span><span class="sxs-lookup"><span data-stu-id="6d548-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="6d548-135">Polo tanto, é necesario que antes de desactivar unha dimensión, elimine todas as filas de **Prezo de rol** e **Sobreprezo de rol** que encheu ese valor de dimensión.</span><span class="sxs-lookup"><span data-stu-id="6d548-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

