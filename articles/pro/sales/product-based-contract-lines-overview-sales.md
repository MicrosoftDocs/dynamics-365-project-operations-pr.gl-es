---
title: Visión xeral de liñas de contrato baseado en produto - lite
description: Este tema fornece información sobre liñas de contrato baseado en produtos.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177869"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="16d75-103">Visión xeral de liñas de contrato baseado en produto - lite</span><span class="sxs-lookup"><span data-stu-id="16d75-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="16d75-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="16d75-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="16d75-105">Pode crear liñas de contrato baseado en produto en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="16d75-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="16d75-106">As liñas de contrato baseado en produtos poden ser liñas creadas manualmente ou poden ser elementos do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="16d75-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="16d75-107">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="16d75-107">Product catalog</span></span>

<span data-ttu-id="16d75-108">Os produtos do catálogo de produtos teñen unha unidade por defecto e un grupo de unidades.</span><span class="sxs-lookup"><span data-stu-id="16d75-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="16d75-109">Se varios produtos comparten o mesmo conxunto de atributos, pode crear unha familia de produtos que tamén teña eses atributos.</span><span class="sxs-lookup"><span data-stu-id="16d75-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="16d75-110">Todos os produtos dunha familia de produtos herdan o mesmo conxunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="16d75-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="16d75-111">Por exemplo, unha empresa vende licenzas de subscrición para diferentes tipos de software.</span><span class="sxs-lookup"><span data-stu-id="16d75-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="16d75-112">Todo o software de subscrición ten os dous atributos seguintes:</span><span class="sxs-lookup"><span data-stu-id="16d75-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="16d75-113">Número de usuarios</span><span class="sxs-lookup"><span data-stu-id="16d75-113">Number of users</span></span>
- <span data-ttu-id="16d75-114">Duración da subscrición (en meses)</span><span class="sxs-lookup"><span data-stu-id="16d75-114">Subscription duration (in months)</span></span>

<span data-ttu-id="16d75-115">Para manter este tipo de catálogo, cree unha familia de produtos con nome **Software de subscrición**.</span><span class="sxs-lookup"><span data-stu-id="16d75-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="16d75-116">Engada os atributos **Número de usuarios** e **Duración da subscrición** á familia de produtos.</span><span class="sxs-lookup"><span data-stu-id="16d75-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="16d75-117">A seguir, engada produtos individuais á familia de produtos **Software de subscrición**.</span><span class="sxs-lookup"><span data-stu-id="16d75-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="16d75-118">Engadir elementos do catálogo de produtos a un contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="16d75-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="16d75-119">Os contratos de proxecto e contrato de proxecto teñen seccións para dous tipos de liñas: liñas baseadas en proxectos e liñas baseadas en produtos.</span><span class="sxs-lookup"><span data-stu-id="16d75-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="16d75-120">As liñas baseadas en produtos inclúen todos os produtos e unidades da lista de prezos do contrato.</span><span class="sxs-lookup"><span data-stu-id="16d75-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="16d75-121">Poden engadirse produtos que non forman parte da lista de prezos de produtos do contrato.</span><span class="sxs-lookup"><span data-stu-id="16d75-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="16d75-122">Pode seleccionar produtos doutras listas de prezos ou directamente do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="16d75-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="16d75-123">Cando selecciona produtos directamente dun catálogo de produtos, utilízase a lista de prezos por defecto dese produto para o prezo de venda do produto.</span><span class="sxs-lookup"><span data-stu-id="16d75-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="16d75-124">Se non se establece unha lista de prezos por defecto, o prezo será de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="16d75-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="16d75-125">Se unha liña de contrato está baseada nun catálogo de produtos, pode anular o prezo de venda directamente na liña.</span><span class="sxs-lookup"><span data-stu-id="16d75-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="16d75-126">Unha liña de contrato ten o campo **Prezos** cos dous valores:</span><span class="sxs-lookup"><span data-stu-id="16d75-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="16d75-127">**Anular prezos**</span><span class="sxs-lookup"><span data-stu-id="16d75-127">**Override pricing**</span></span>
- <span data-ttu-id="16d75-128">**Usar predefinido**</span><span class="sxs-lookup"><span data-stu-id="16d75-128">**Use default**</span></span>

<span data-ttu-id="16d75-129">Se definiu o campo **Prezos** en **Anular prezos**, non se establece un prezo por defecto.</span><span class="sxs-lookup"><span data-stu-id="16d75-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="16d75-130">Introduza un prezo do produto da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="16d75-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="16d75-131">Se configura o campo en **Usar predefinido**, úsase o prezo de venda predefinido e o campo non se pode editar.</span><span class="sxs-lookup"><span data-stu-id="16d75-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="16d75-132">Despois de instalar Project Operations, os prezos de venda por defecto introdúcense nas liñas baseadas en produtos nun contrato.</span><span class="sxs-lookup"><span data-stu-id="16d75-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="16d75-133">O campo **Prezos** defínese como **Anular prezos** para que poida editar o prezo por defecto nas liñas de contrato.</span><span class="sxs-lookup"><span data-stu-id="16d75-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="16d75-134">Trátase dunha anulación específica de Project Operations para o comportamento das liñas baseadas en produto en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="16d75-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
