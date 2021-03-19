---
title: Desactivar unha dimensión de prezos
description: Este tema fornece información sobre como desactivar dimensións de prezos.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274726"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="ea169-103">Desactivar unha dimensión de prezos</span><span class="sxs-lookup"><span data-stu-id="ea169-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="ea169-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="ea169-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea169-105">Pode que necesite revisar e actualizar a súa estratexia de prezos cada poucos anos.</span><span class="sxs-lookup"><span data-stu-id="ea169-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="ea169-106">Todas as actualizacións que faga pode requirir que desactive unha dimensión de prezos existente e cree unha nova.</span><span class="sxs-lookup"><span data-stu-id="ea169-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="ea169-107">Por exemplo, pode ter un prezo anterior por **Rol**, pero agora decidiu establecer os prezos por **Experiencia laboral**.</span><span class="sxs-lookup"><span data-stu-id="ea169-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="ea169-108">Isto pode requirir que desactive **Rol** como dimensión de prezos e cree **Experiencia laboral** como unha nova dimensión de prezos.</span><span class="sxs-lookup"><span data-stu-id="ea169-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="ea169-109">Para desactivar unha dimensión de prezos, independentemente de se é lista para usar ou personalizada, pode configurar os campos **Aplicable ao custo** e **Aplicable ás vendas** da dimensión de prezos en **Non**.</span><span class="sxs-lookup"><span data-stu-id="ea169-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="ea169-110">Non obstante, cando fai isto, pode que reciba a mensaxe de erro, **A dimensión de prezos non se pode actualizar nin eliminar se hai rexistros de prezos asociados.**</span><span class="sxs-lookup"><span data-stu-id="ea169-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Erro de proceso de negocio ao desactivar unha dimensión de prezos](media/Business-Process-Error.png)

<span data-ttu-id="ea169-112">Esta mensaxe de erro indica que hai rexistros de prezos previamente configurados para a dimensión que se vai desactivar.</span><span class="sxs-lookup"><span data-stu-id="ea169-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="ea169-113">Todos os rexistros de **Prezo de rol** e **Sobreprezo de rol** que fan referencia a unha dimensión deben ser eliminados antes de que se poida establecer a aplicabilidade da dimensión en **Non**.</span><span class="sxs-lookup"><span data-stu-id="ea169-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="ea169-114">Esta regra aplícase tanto ás dimensións de prezos listas para usar como ás dimensións de prezos personalizadas que creou.</span><span class="sxs-lookup"><span data-stu-id="ea169-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="ea169-115">O motivo desta validación é que cada rexistro de **Prezo de rol** debe ter unha combinación única de dimensións.</span><span class="sxs-lookup"><span data-stu-id="ea169-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="ea169-116">Por exemplo, nunha lista de prezos chamada **Taxas de custos de EUA 2018**, ten as seguinte filas de **Prezo de rol**.</span><span class="sxs-lookup"><span data-stu-id="ea169-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="ea169-117">Título estándar</span><span class="sxs-lookup"><span data-stu-id="ea169-117">Standard Title</span></span>         | <span data-ttu-id="ea169-118">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="ea169-118">Org Unit</span></span>    |<span data-ttu-id="ea169-119">Unidade</span><span class="sxs-lookup"><span data-stu-id="ea169-119">Unit</span></span>   |<span data-ttu-id="ea169-120">Prezo</span><span class="sxs-lookup"><span data-stu-id="ea169-120">Price</span></span>  |<span data-ttu-id="ea169-121">Moeda</span><span class="sxs-lookup"><span data-stu-id="ea169-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="ea169-122">Enxeñeiro de sistemas</span><span class="sxs-lookup"><span data-stu-id="ea169-122">Systems Engineer</span></span>|<span data-ttu-id="ea169-123">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="ea169-123">Contoso US</span></span>|<span data-ttu-id="ea169-124">Hour</span><span class="sxs-lookup"><span data-stu-id="ea169-124">Hour</span></span>| <span data-ttu-id="ea169-125">100</span><span class="sxs-lookup"><span data-stu-id="ea169-125">100</span></span>|<span data-ttu-id="ea169-126">USD</span><span class="sxs-lookup"><span data-stu-id="ea169-126">USD</span></span>|
| <span data-ttu-id="ea169-127">Enxeñeiro de sistemas sénior</span><span class="sxs-lookup"><span data-stu-id="ea169-127">Senior Systems Engineer</span></span>|<span data-ttu-id="ea169-128">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="ea169-128">Contoso US</span></span>|<span data-ttu-id="ea169-129">Hour</span><span class="sxs-lookup"><span data-stu-id="ea169-129">Hour</span></span>| <span data-ttu-id="ea169-130">150</span><span class="sxs-lookup"><span data-stu-id="ea169-130">150</span></span>| <span data-ttu-id="ea169-131">USD</span><span class="sxs-lookup"><span data-stu-id="ea169-131">USD</span></span>|


<span data-ttu-id="ea169-132">Cando desactive **Título estándar** como dimensión de prezos e o motor de prezos busque un prezo, só empregará o valor **Unidade organizativa** do contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea169-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="ea169-133">Se a **Unidade organizativa** do contexto de entrada é "Contoso EUA", o resultado non será determinista porque coincidirán as dúas filas.</span><span class="sxs-lookup"><span data-stu-id="ea169-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="ea169-134">Para evitar este escenario, cando cree rexistros de **Prezo de rol**, o sistema valida que a combinación de dimensións é única.</span><span class="sxs-lookup"><span data-stu-id="ea169-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="ea169-135">Se a dimensión está desactivada despois da creación de rexistros de **Prezo de rol**, pódese violar esta restrición.</span><span class="sxs-lookup"><span data-stu-id="ea169-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="ea169-136">Polo tanto, é necesario que antes de desactivar unha dimensión, elimine todas as filas de **Prezo de rol** e **Sobreprezo de rol** que encheu ese valor de dimensión.</span><span class="sxs-lookup"><span data-stu-id="ea169-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]