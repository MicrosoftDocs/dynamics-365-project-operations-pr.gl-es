---
title: Liñas de oferta baseadas en produtos
description: Este tema fornece información sobre liñas de oferta baseadas en produtos.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751366"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="29214-103">Liñas de oferta baseadas en produtos</span><span class="sxs-lookup"><span data-stu-id="29214-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="29214-104">Pode crear liñas de oferta baseadas en produtos Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="29214-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="29214-105">As liñas de oferta baseadas en produtos poden ser liñas "fóra de catálogo" ou poden ser elementos do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="29214-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="29214-106">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="29214-106">Product catalog</span></span>

<span data-ttu-id="29214-107">Os produtos dun catálogo de produtos de Dynamics 365 teñen unha unidade por defecto e un grupo de unidades.</span><span class="sxs-lookup"><span data-stu-id="29214-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="29214-108">Se varios produtos comparten o mesmo conxunto de atributos, pode crear unha familia de produtos que tamén teña eses atributos.</span><span class="sxs-lookup"><span data-stu-id="29214-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="29214-109">Todos os produtos dunha familia de produtos herdan o mesmo conxunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="29214-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="29214-110">Por exemplo, unha empresa vende licenzas de subscrición para unha variedade de software.</span><span class="sxs-lookup"><span data-stu-id="29214-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="29214-111">Todo o software de subscrición ten os dous atributos seguintes:</span><span class="sxs-lookup"><span data-stu-id="29214-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="29214-112">Número de usuarios</span><span class="sxs-lookup"><span data-stu-id="29214-112">Number of users</span></span> 
- <span data-ttu-id="29214-113">Duración da subscrición (en meses)</span><span class="sxs-lookup"><span data-stu-id="29214-113">Subscription duration (in months)</span></span>

<span data-ttu-id="29214-114">Un bo xeito de manter este tipo de catálogo é crear unha familia de produtos que leva o nome **Software de subscrición**, e iso ten **Número de usuarios** e **Duración da subscrición** como atributos.</span><span class="sxs-lookup"><span data-stu-id="29214-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="29214-115">Pode engadir produtos individuais, como **Dynamics 365 Sales** ou **Dynamics 365 Field Service** á familia de produtos **Software de subscrición**.</span><span class="sxs-lookup"><span data-stu-id="29214-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="29214-116">Engadir elementos do catálogo de produtos a unha oferta de proxecto</span><span class="sxs-lookup"><span data-stu-id="29214-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="29214-117">As páxinas de oferta de proxecto e contrato de proxecto teñen seccións para dous tipos de liñas: liñas baseadas en proxectos e liñas baseadas en produtos.</span><span class="sxs-lookup"><span data-stu-id="29214-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="29214-118">Para liñas baseadas en produtos, Dynamics 365 úsase para engadir elementos dun catálogo de produtos a unha oferta.</span><span class="sxs-lookup"><span data-stu-id="29214-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="29214-119">A lista despregable na liña de oferta ou liña de contrato de proxecto inclúe todos os produtos e unidades da lista de prezos de produtos que se anexa á oferta ou contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="29214-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="29214-120">Tamén pode engadir produtos que non forman parte da lista de prezos da oferta.</span><span class="sxs-lookup"><span data-stu-id="29214-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="29214-121">Ademais, pode seleccionar produtos doutras listas de prezos ou pode seleccionar os produtos directamente do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="29214-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="29214-122">Cando selecciona produtos directamente dun catálogo de produtos, utilízase a lista de prezos por defecto dese produto para obter o prezo de venda do produto.</span><span class="sxs-lookup"><span data-stu-id="29214-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="29214-123">Se non se establece unha lista de prezos por defecto, o prezo será de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="29214-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="29214-124">Se unha liña de oferta está baseada nun catálogo de produtos, pode anular o prezo de venda directamente na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="29214-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="29214-125">Teña en conta que unha liña de oferta en Dynamics 365 ten un campo **Prezos**.</span><span class="sxs-lookup"><span data-stu-id="29214-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="29214-126">Hai dous valores dispoñibles:</span><span class="sxs-lookup"><span data-stu-id="29214-126">Two values are available:</span></span>

- <span data-ttu-id="29214-127">Anular prezos</span><span class="sxs-lookup"><span data-stu-id="29214-127">Override pricing</span></span>  
- <span data-ttu-id="29214-128">Usar predefinido</span><span class="sxs-lookup"><span data-stu-id="29214-128">Use default</span></span>

<span data-ttu-id="29214-129">Se definiu este campo en **Anular prezos**, Dynamics 365 non establece un prezo por defecto.</span><span class="sxs-lookup"><span data-stu-id="29214-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="29214-130">Debe introducir un prezo para o produto na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="29214-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="29214-131">Se definiu este campo como **Usar predefinido**, Dynamics 365 usa o prezo de venda predefinido e bloquea o campo para evitar a edición.</span><span class="sxs-lookup"><span data-stu-id="29214-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="29214-132">Despois de instalar PSA, os prezos de venda por defecto introdúcense nas liñas baseadas en produtos nunha oferta.</span><span class="sxs-lookup"><span data-stu-id="29214-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="29214-133">O campo **Prezos** defínese como **Anular prezos** para que poida editar o prezo por defecto nas liñas de oferta.</span><span class="sxs-lookup"><span data-stu-id="29214-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Establecer anular prezos](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="29214-135">Factores de cantidade para produtos</span><span class="sxs-lookup"><span data-stu-id="29214-135">Quantity factors for products</span></span>

<span data-ttu-id="29214-136">PSA usa factores de cantidade para apoiar a venda de produtos baseados en subscrición.</span><span class="sxs-lookup"><span data-stu-id="29214-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="29214-137">Para os produtos baseados en subscrición, a cantidade na liña de oferta ou contrato de proxecto exprésase como o número de meses de usuario.</span><span class="sxs-lookup"><span data-stu-id="29214-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="29214-138">Normalmente, o prezo do software de subscrición almacénase no catálogo como o prezo por usuario ao mes.</span><span class="sxs-lookup"><span data-stu-id="29214-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="29214-139">Non obstante, pode usar outras descricións de tempo no seu lugar.</span><span class="sxs-lookup"><span data-stu-id="29214-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="29214-140">Durante o proceso de vendas, o prezo na liña de oferta adoita ser o prezo por usuario, por mes que foi negociado e descontado polo axente de vendas de TI.</span><span class="sxs-lookup"><span data-stu-id="29214-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="29214-141">Cada acordo ten un número diferente de usuarios e un número diferente de meses de subscrición.</span><span class="sxs-lookup"><span data-stu-id="29214-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="29214-142">A cantidade que se utiliza para calcular a cantidade da liña de oferta é un produto do número de usuarios e do número de meses de subscrición.</span><span class="sxs-lookup"><span data-stu-id="29214-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="29214-143">Para apoiar este tipo de venda, PSA introduciu o concepto de factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="29214-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="29214-144">Os factores de cantidade dependen dos atributos do produto en Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="29214-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="29214-145">Ao configurar propiedades específicas para un produto, PSA permítelle marcar un subconxunto destas propiedades ou de todas as propiedades como factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="29214-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="29214-146">PSA valida que só as propiedades numéricas ou propiedades de produto que teñen un tipo de datos numéricos estean marcadas como factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="29214-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="29214-147">Cando un produto para o que se configuran os factores de cantidade se engade a unha liña de presupostos, o campo **Cantidade** na liña de oferta convértese nun campo de só lectura.</span><span class="sxs-lookup"><span data-stu-id="29214-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="29214-148">Despois de introducir valores para as propiedades do produto que son factores de cantidade, PSA calcula a cantidade da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="29214-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="29214-149">Por exemplo, Dynamics 365 pode ter as seguintes propiedades:</span><span class="sxs-lookup"><span data-stu-id="29214-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="29214-150">**N.º de usuarios** - O número de usuarios</span><span class="sxs-lookup"><span data-stu-id="29214-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="29214-151">**Nº de meses** - O número de meses de subscrición</span><span class="sxs-lookup"><span data-stu-id="29214-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="29214-152">**SKU de produto**</span><span class="sxs-lookup"><span data-stu-id="29214-152">**Product SKU**</span></span> 

<span data-ttu-id="29214-153">As propiedades **N.º de Usuarios** e **N.º de meses** pódense marcar como factores de cantidade editando as propiedades da liña de produtos.</span><span class="sxs-lookup"><span data-stu-id="29214-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Marcado de n.º de usuarios e n.º de meses como factores de calidade](media/basic-guide-11.png)
 
