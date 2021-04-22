---
title: Listas de prezos de produtos
description: Este tema ofrece información sobre as listas de prezos nos prezos do catálogo empregados para ofertas e contratos de proxectos.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877488"
---
# <a name="product-price-lists"></a><span data-ttu-id="62096-103">Listas de prezos de produtos</span><span class="sxs-lookup"><span data-stu-id="62096-103">Product price lists</span></span>

<span data-ttu-id="62096-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="62096-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="62096-105">En Project Operations, **Listas de prezos dos produtos** e as entidades relacionadas cos elementos da lista de prezos admiten a funcionalidade para fixar o prezo dos produtos en liñas de oferta e contrato baseadas en produtos.</span><span class="sxs-lookup"><span data-stu-id="62096-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="62096-106">Para os produtos utilizados en proxectos, úsanse os rexistros de elementos da lista de prezos para as listas de prezos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="62096-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="62096-107">Os produtos deben configurarse de xeito que teñan listas de custos e prezos por defecto no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="62096-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="62096-108">Use o prezo da lista, o custo estándar e o custo actual para configurar o custo predeterminado e os prezos da lista.</span><span class="sxs-lookup"><span data-stu-id="62096-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="62096-109">Os prezos da lista por defecto úsanse nunha liña de presupostos ou nunha liña de contratos de proxecto só cando o sistema non atopa unha liña de prezos para ese produto na lista de prezos do produto para a oferta ou contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="62096-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="62096-110">O prezo de custo das liñas de catálogo de produtos pódese cambiar entre ofertas.</span><span class="sxs-lookup"><span data-stu-id="62096-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="62096-111">Esta capacidade é importante, porque se non rastrexa con precisión os custos, non pode determinar os beneficios operativos nas compromisos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="62096-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="62096-112">Por defecto, o custo estándar do produto utilízase como prezo de custo</span><span class="sxs-lookup"><span data-stu-id="62096-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="62096-113">Non obstante, o prezo de custo por defecto pódese actualizar na liña de oferta se hai un prezo de custo diferente para esa oferta.</span><span class="sxs-lookup"><span data-stu-id="62096-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="62096-114">Elementos da lista de prezos</span><span class="sxs-lookup"><span data-stu-id="62096-114">Price list items</span></span>

<span data-ttu-id="62096-115">Pode engadir produtos dun catálogo de produtos a diferentes listas de prezos.</span><span class="sxs-lookup"><span data-stu-id="62096-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="62096-116">As liñas de lista prezos dos produtos fan referencia sempre a unha unidade específica.</span><span class="sxs-lookup"><span data-stu-id="62096-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="62096-117">Os prezos dun produto dos elementos da lista de prezos pódense configurar como cantidade de moeda.</span><span class="sxs-lookup"><span data-stu-id="62096-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="62096-118">Alternativamente, pódese configurar en función do prezo da lista, do custo actual ou do custo estándar.</span><span class="sxs-lookup"><span data-stu-id="62096-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="62096-119">A funcionalidade de fixación de prezos admite varias opcións de redondeo cando os prezos dos produtos están configurados en función do prezo de lista, do custo estándar ou do custo actual.</span><span class="sxs-lookup"><span data-stu-id="62096-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="62096-120">Ademais de aproveitar múltiples métodos de prezos e opcións de redondeo, pode asociar listas de descontos con elementos da lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="62096-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="62096-121">Lista de prezos de produtos predefinida</span><span class="sxs-lookup"><span data-stu-id="62096-121">Default product price list</span></span>
<span data-ttu-id="62096-122">Cada rexistro de clientes ten un campo **Lista de prezos por defecto**, onde pode especificar unha lista de prezos que coincida coa moeda do cliente.</span><span class="sxs-lookup"><span data-stu-id="62096-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="62096-123">Un valor por defecto non se introduce automaticamente neste campo.</span><span class="sxs-lookup"><span data-stu-id="62096-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="62096-124">Cando existe un acordo de prezos personalizado cun cliente específico, pode usar este campo para asociar unha lista de prezos a ese cliente.</span><span class="sxs-lookup"><span data-stu-id="62096-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="62096-125">As entidades Oportunidade, Oferta e Contrato de proxecto usan a seguinte orde para introducir listas de prezos de produtos por defecto.</span><span class="sxs-lookup"><span data-stu-id="62096-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="62096-126">A mesma orde úsase para listas de prezos de proxecto.</span><span class="sxs-lookup"><span data-stu-id="62096-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="62096-127">Oferta</span><span class="sxs-lookup"><span data-stu-id="62096-127">Quote</span></span>
2.  <span data-ttu-id="62096-128">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="62096-128">Opportunity</span></span>
3.  <span data-ttu-id="62096-129">Cliente</span><span class="sxs-lookup"><span data-stu-id="62096-129">Customer</span></span>
4.  <span data-ttu-id="62096-130">Configuración global</span><span class="sxs-lookup"><span data-stu-id="62096-130">Global settings</span></span> 

<span data-ttu-id="62096-131">Por defecto, o campo **Produto** da liña de oferta indica todos os produtos activos na lista de prezos do produto.</span><span class="sxs-lookup"><span data-stu-id="62096-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="62096-132">Se un produto foi inactivado ou se é un produto borrador, non aparece na lista, aínda que estea na lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="62096-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="62096-133">As liñas de catálogo de produtos engádense como liñas de factura na primeira factura que se crea para un contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="62096-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="62096-134">Nun borrador de factura, pódense eliminar esas liñas de factura.</span><span class="sxs-lookup"><span data-stu-id="62096-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="62096-135">Nese caso, as liñas aparecerán nunha factura posterior ata a facturación ou ata que a factura se envíe ao cliente.</span><span class="sxs-lookup"><span data-stu-id="62096-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="62096-136">Non pode facturar unha cantidade parcial dunha liña de factura de produto.</span><span class="sxs-lookup"><span data-stu-id="62096-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="62096-137">Cando se facturan as liñas de produto do contrato do proxecto, créanse datos reais.</span><span class="sxs-lookup"><span data-stu-id="62096-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="62096-138">Non obstante, eses datos reais non están ligados á entidade de proxecto relacionada.</span><span class="sxs-lookup"><span data-stu-id="62096-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="62096-139">Noutras palabras, as liñas de contrato de proxecto baseadas en produtos son independentes de calquera uso baseado en proxectos.</span><span class="sxs-lookup"><span data-stu-id="62096-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
