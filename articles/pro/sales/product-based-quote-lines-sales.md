---
title: Visión xeral de liñas de oferta baseada en produto - lite
description: Este tema ofrece información sobre o traballo con liñas de oferta baseada en produto.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178186"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="cf5fb-103">Visión xeral de liñas de oferta baseada en produto - lite</span><span class="sxs-lookup"><span data-stu-id="cf5fb-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="cf5fb-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="cf5fb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf5fb-105">Pode crear liñas de oferta baseadas en produtos en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="cf5fb-106">As liñas de oferta baseadas en produtos poden engadirse manualmente ou poden ser elementos do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="cf5fb-107">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="cf5fb-107">Product catalog</span></span>

<span data-ttu-id="cf5fb-108">Cada produto do catálogo de produtos ten unha unidade e un grupo de unidades por defecto.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="cf5fb-109">Se varios produtos comparten o mesmo conxunto de atributos, pode crear unha familia de produtos que comparta eses atributos.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="cf5fb-110">Por exemplo, unha empresa vende licenzas de subscrición para diferentes tipos de software.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="cf5fb-111">Todo o software de subscrición ten os dous atributos seguintes:</span><span class="sxs-lookup"><span data-stu-id="cf5fb-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="cf5fb-112">Número de usuarios</span><span class="sxs-lookup"><span data-stu-id="cf5fb-112">Number of users</span></span>
- <span data-ttu-id="cf5fb-113">Unha duración da subscrición medida en meses</span><span class="sxs-lookup"><span data-stu-id="cf5fb-113">A subscription duration measured in months</span></span>

<span data-ttu-id="cf5fb-114">Para manter este tipo de catálogo, cree unha familia de produtos que leva o nome **Software de subscrición** e engada o número de usuarios e a duración da subscrición como atributos.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="cf5fb-115">A seguir, pode engadir produtos individuais á familia de produtos de **Software de subscrición**.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="cf5fb-116">Engadir elementos do catálogo de produtos a unha oferta de proxecto</span><span class="sxs-lookup"><span data-stu-id="cf5fb-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="cf5fb-117">As páxinas **Oferta de proxecto** e **Contrato de proxecto** teñen seccións para liñas baseadas en proxecto e liñas baseadas en produto.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="cf5fb-118">Para liñas baseadas en produto, a lista despregable na liña de oferta ou liña de contrato de proxecto inclúe todos os produtos e unidades da lista de prezos de produtos.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="cf5fb-119">Tamén pode engadir produtos que non forman parte da lista de prezos de produtos.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="cf5fb-120">Ademais, pode seleccionar produtos doutras listas de prezos ou directamente do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="cf5fb-121">Cando selecciona produtos directamente dun catálogo de produtos, utilízase a lista de prezos por defecto dese produto para obter o prezo de venda do produto.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="cf5fb-122">Se non se establece unha lista de prezos por defecto, o prezo será de cero (0).</span><span class="sxs-lookup"><span data-stu-id="cf5fb-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="cf5fb-123">Cando unha liña de oferta está baseada nun catálogo de produtos, pode anular o prezo de venda directamente na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="cf5fb-124">Unha liña de oferta no campo **Prezos** con dous valores dispoñibles:</span><span class="sxs-lookup"><span data-stu-id="cf5fb-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="cf5fb-125">**Anular prezos**</span><span class="sxs-lookup"><span data-stu-id="cf5fb-125">**Override Pricing**</span></span>
- <span data-ttu-id="cf5fb-126">**Utilizar predefinido**</span><span class="sxs-lookup"><span data-stu-id="cf5fb-126">**Use Default**</span></span>

<span data-ttu-id="cf5fb-127">Se selecciona **Anular prezos**, o prezo por defecto non está definido.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="cf5fb-128">En lugar diso, debe introducir un prezo para o produto na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="cf5fb-129">Se selecciona **Usar predefinido**, úsase o prezo de venda por defecto e o campo está bloqueado para a súa edición.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="cf5fb-130">Os prezos de venda por defecto introdúcense nas liñas baseadas en produtos dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="cf5fb-131">O campo **Prezos** defínese como **Anular prezos** para que poida editar o prezo por defecto nas liñas de oferta.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="cf5fb-132">Trátase dunha anulación específica de Project Operations do comportamento das liñas baseadas en produto en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="cf5fb-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
