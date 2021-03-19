---
title: Configurar taxas de custo e vendas para produtos de catálogo - lite
description: Este tema ofrece información sobre como configurar as taxas de custo e vendas de elementos dun catálogo de produtos.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274456"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="1e618-103">Configurar taxas de custo e vendas para produtos de catálogo - lite</span><span class="sxs-lookup"><span data-stu-id="1e618-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="1e618-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1e618-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1e618-105">A configuración de prezos para elementos do catálogo de produtos en Dynamics 365 Project Operations é igual que en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="1e618-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="1e618-106">En Project Operations, os produtos non se poden estimar nin usar en proxectos, polo que non é preciso fixar os prezos do catálogo de produtos nas listas de prezos do proxecto para ofertas e contratos.</span><span class="sxs-lookup"><span data-stu-id="1e618-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="1e618-107">Use o campo **Prezo do produto** dunha oferta, contrato ou conta para configurar os prezos do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="1e618-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="1e618-108">Non configure os prezos do catálogo de produtos nas listas de prezos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1e618-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="1e618-109">As listas de prezos do proxecto son exclusivas de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1e618-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="1e618-110">A lóxica empresarial específica da aplicación copia as listas de prezos dunha oferta a un contrato.</span><span class="sxs-lookup"><span data-stu-id="1e618-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="1e618-111">O resultado é unha lista de prezos específica para o contrato.</span><span class="sxs-lookup"><span data-stu-id="1e618-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="1e618-112">A operación de copia pode retrasar o proceso de gañar a oferta se a lista de prezos do proxecto da oferta é demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="1e618-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="1e618-113">As listas de prezos de produtos non se copian para crear listas de prezos personalizadas nos contratos.</span><span class="sxs-lookup"><span data-stu-id="1e618-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="1e618-114">Debido a que non hai copia, o rendemento do proceso da oferta non se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="1e618-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]