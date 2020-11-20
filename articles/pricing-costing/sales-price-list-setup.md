---
title: Configurar unha lista de prezos de vendas
description: Este tema ofrece información sobre listas de prezos de vendas para a fixación de prezos de proxectos.
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
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176249"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="3006f-103">Configurar unha lista de prezos de vendas</span><span class="sxs-lookup"><span data-stu-id="3006f-103">Set up a sales price list</span></span>

<span data-ttu-id="3006f-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="3006f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3006f-105">Para as ofertas e contratos de proxectos, a lista de prezos dun proxecto ten un padrón de anulación de prezos diferente do que ten unha lista de prezos de produtos.</span><span class="sxs-lookup"><span data-stu-id="3006f-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="3006f-106">Nunha liña de oferta baseada en catálogo de produtos, pode anular o prezo aos roles e categorías directamente na liña de oferta, porque cada liña de oferta apunta exactamente a un elemento do catálogo.</span><span class="sxs-lookup"><span data-stu-id="3006f-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="3006f-107">Non obstante, nunha liña de oferta baseada en proxectos, non pode anular o prezo aos roles e categorías directamente na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="3006f-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="3006f-108">Pode usar a lista de prezos de proxectos para traballar cos dous padróns de anulación distintos.</span><span class="sxs-lookup"><span data-stu-id="3006f-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="3006f-109">Recomendamos que teña unha lista de prezos independente para os recursos do proxecto e os elementos do seu catálogo, debido ás diferenzas de comportamento entre ambas cando anula os prezos.</span><span class="sxs-lookup"><span data-stu-id="3006f-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="3006f-110">Cada unha das seguintes entidades pode ter unha ou varias listas de prezos de vendas asociadas para os prezos de proxectos:</span><span class="sxs-lookup"><span data-stu-id="3006f-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="3006f-111">Cliente (conta)</span><span class="sxs-lookup"><span data-stu-id="3006f-111">Customer (account)</span></span> 
- <span data-ttu-id="3006f-112">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="3006f-112">Opportunity</span></span> 
- <span data-ttu-id="3006f-113">Oferta</span><span class="sxs-lookup"><span data-stu-id="3006f-113">Quote</span></span> 
- <span data-ttu-id="3006f-114">Contrato do proxecto</span><span class="sxs-lookup"><span data-stu-id="3006f-114">Project Contract</span></span>

<span data-ttu-id="3006f-115">A asociación destas entidades cunha lista de prezos está indicada polas listas de prezos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="3006f-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="3006f-116">Pode asociar unha ou varias listas de prezos ás entidades de vendas Cliente, Oportunidade, Oferta e Contrato de Proxecto.</span><span class="sxs-lookup"><span data-stu-id="3006f-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="3006f-117">Non se introduce automaticamente unha lista de prezos do proxecto predefinida nun rexistro de clientes.</span><span class="sxs-lookup"><span data-stu-id="3006f-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="3006f-118">Non obstante, pode anexar manualmente unha lista de prezos do proxecto ao rexistro de clientes.</span><span class="sxs-lookup"><span data-stu-id="3006f-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="3006f-119">Non obstante, debe anexar manualmente unha lista de prezos do proxecto só cando teña un acordo de prezos personalizado co cliente.</span><span class="sxs-lookup"><span data-stu-id="3006f-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="3006f-120">Cando unha lista de prezos do proxecto está anexada a unha entidade de vendas, valídase a seguinte información:</span><span class="sxs-lookup"><span data-stu-id="3006f-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="3006f-121">A lista de prezos ten un contexto de **Vendas**</span><span class="sxs-lookup"><span data-stu-id="3006f-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="3006f-122">A moeda da lista de prezos coincide coa moeda do cliente.</span><span class="sxs-lookup"><span data-stu-id="3006f-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="3006f-123">No contrato do proxecto, a seguinte orde de precedencia utilízase para establecer automaticamente as listas de prezos de proxecto relacionadas:</span><span class="sxs-lookup"><span data-stu-id="3006f-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="3006f-124">Oferta</span><span class="sxs-lookup"><span data-stu-id="3006f-124">Quote</span></span>
2. <span data-ttu-id="3006f-125">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="3006f-125">Opportunity</span></span>
3. <span data-ttu-id="3006f-126">Cliente</span><span class="sxs-lookup"><span data-stu-id="3006f-126">Customer</span></span> 
4. <span data-ttu-id="3006f-127">Configuración global</span><span class="sxs-lookup"><span data-stu-id="3006f-127">Global settings</span></span> 

<span data-ttu-id="3006f-128">Cando se introduce de xeito predeterminado unha lista de prezos do proxecto, o sistema valida que a moeda coincide coa moeda do cliente e que as listas de prezos por defecto que se introduciron teñen un contexto de **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="3006f-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="3006f-129">Pode asociar varias listas de prezos ás entidades de vendas Cliente, Oportunidade, Oferta e Contrato de Proxecto.</span><span class="sxs-lookup"><span data-stu-id="3006f-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="3006f-130">Esta capacidade admite prezos predefinidos específicos da data para un contrato de proxecto de longa duración, onde pode requirir máis dunha lista de prezos para dar conta das actualizacións de prezos que se producen por mor da inflación.</span><span class="sxs-lookup"><span data-stu-id="3006f-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="3006f-131">Non obstante, se as listas de prezos que asocie á entidade Cliente, Oportunidade, Oferta ou Contrato de proxecto teñen efectividade de datas superpostas, os prezos por defecto poderían ser incorrectos.</span><span class="sxs-lookup"><span data-stu-id="3006f-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="3006f-132">Polo tanto, ten que asegurarse de que as listas de prezos do proxecto que teñan data de superposición non estean asociadas a esas entidades.</span><span class="sxs-lookup"><span data-stu-id="3006f-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
