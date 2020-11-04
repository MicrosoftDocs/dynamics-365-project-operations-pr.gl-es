---
title: Configurar taxas de custo e vendas para produtos de catálogo
description: Este tema ofrece información sobre como configurar as taxas de custo e vendas de elementos dun catálogo de produtos.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076199"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="9510a-103">Configurar taxas de custo e vendas para produtos de catálogo</span><span class="sxs-lookup"><span data-stu-id="9510a-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="9510a-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="9510a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9510a-105">A configuración dos prezos dos elementos do catálogo de produtos en Dynamics 365 Project Operations é a mesma que en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9510a-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="9510a-106">Debido a que os produtos non se poden estimar nin usar en proxectos en Project Operations, non é necesario establecer prezos do catálogo de produtos nas listas de prezos do proxecto para ofertas e contratos.</span><span class="sxs-lookup"><span data-stu-id="9510a-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="9510a-107">Os prezos do catálogo de produtos deben establecerse no campo **Prezo do produto** dunha oferta, contrato ou conta.</span><span class="sxs-lookup"><span data-stu-id="9510a-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="9510a-108">Non configure os prezos do catálogo de produtos nas listas de prezos do proxecto para estas entidades.</span><span class="sxs-lookup"><span data-stu-id="9510a-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="9510a-109">As listas de prezos do proxecto son exclusivas de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9510a-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="9510a-110">Existe unha lóxica de negocio específica da aplicación que copia as listas de prezos dunha oferta a un contrato.</span><span class="sxs-lookup"><span data-stu-id="9510a-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="9510a-111">O resultado é unha lista de prezos específica para o contrato.</span><span class="sxs-lookup"><span data-stu-id="9510a-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="9510a-112">A operación de copia pode retrasar o proceso de gañar a oferta se a lista de prezos do proxecto da oferta é demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="9510a-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="9510a-113">As listas de prezos de produtos non se copian para crear listas de prezos personalizadas nos contratos.</span><span class="sxs-lookup"><span data-stu-id="9510a-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="9510a-114">Isto significa que as listas de prezos de produtos non afectan ao rendemento do proceso de gañar a oferta.</span><span class="sxs-lookup"><span data-stu-id="9510a-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
