---
title: Estimacións de recursos
description: Este tema ofrece información sobre como se calculan as estimacións de recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286516"
---
# <a name="resource-estimates"></a><span data-ttu-id="8be53-103">Estimacións de recursos</span><span class="sxs-lookup"><span data-stu-id="8be53-103">Resource estimates</span></span>

<span data-ttu-id="8be53-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="8be53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8be53-105">As estimacións de recursos proceden dun esforzo de fases de tempo que se define na estrutura de subdivisión do traballo xunto coas dimensións de prezos aplicables.</span><span class="sxs-lookup"><span data-stu-id="8be53-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="8be53-106">Normalmente, o cálculo é **taxa/hora para cada rol x horas.**</span><span class="sxs-lookup"><span data-stu-id="8be53-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="8be53-107">O esforzo de fases de tempo para cada recurso almacénase no rexistro de atribución de recursos.</span><span class="sxs-lookup"><span data-stu-id="8be53-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="8be53-108">Os prezos almacénanse nunha lista de prezos predefinida.</span><span class="sxs-lookup"><span data-stu-id="8be53-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="8be53-109">A conversión de unidades aplícase en función da lista de prezos aplicable.</span><span class="sxs-lookup"><span data-stu-id="8be53-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimacións de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="8be53-111">Prezo de custo e moeda de custos por defecto</span><span class="sxs-lookup"><span data-stu-id="8be53-111">Default cost price and cost currency</span></span>

<span data-ttu-id="8be53-112">Os prezos de custo son por defecto os da unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="8be53-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="8be53-113">Taxa de facturación de gastos e moeda de vendas por defecto</span><span class="sxs-lookup"><span data-stu-id="8be53-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="8be53-114">Os prezos de vendas aplícanse unha vez por acordo.</span><span class="sxs-lookup"><span data-stu-id="8be53-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="8be53-115">A xerarquía da lista de prezos de venda predefinida é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="8be53-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="8be53-116">Organización</span><span class="sxs-lookup"><span data-stu-id="8be53-116">Organization</span></span>
2. <span data-ttu-id="8be53-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="8be53-117">Customer</span></span>
3. <span data-ttu-id="8be53-118">Oferta/contrato</span><span class="sxs-lookup"><span data-stu-id="8be53-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]