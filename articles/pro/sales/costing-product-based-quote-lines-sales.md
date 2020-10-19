---
title: Custos de liñas de oferta baseadas en produto
description: Este tema fornece información sobre aplicar un prezo de custo a unha liña de oferta baseada en produtos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906158"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="c700f-103">Custos de liñas de oferta baseadas en produto</span><span class="sxs-lookup"><span data-stu-id="c700f-103">Costing product-based quote lines</span></span>

<span data-ttu-id="c700f-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="c700f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c700f-105">As liñas de oferta baseada en produto en Dynamics 365 Project Operations tamén teñen un campo **Prezo de custo**.</span><span class="sxs-lookup"><span data-stu-id="c700f-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="c700f-106">Este campo úsase para rastrexar o prezo de custo do produto na liña de oferta e para cálculos de rendibilidade descendentes.</span><span class="sxs-lookup"><span data-stu-id="c700f-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="c700f-107">Cando se crea unha liña de oferta baseada en produto para un produto de catálogo, o custo da liña de oferta baseada en produto é por defecto o do campo **Custo estándar** do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="c700f-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="c700f-108">O campo de custo estándar do catálogo de produtos configúrase na moeda base da organización.</span><span class="sxs-lookup"><span data-stu-id="c700f-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="c700f-109">O custo unitario predefinido da liña de oferta baseada en produto convértese na moeda de vendas da oferta.</span><span class="sxs-lookup"><span data-stu-id="c700f-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="c700f-110">Custo unitario nunha liña de oferta baseada en produto</span><span class="sxs-lookup"><span data-stu-id="c700f-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="c700f-111">A finalidade de ter un custo unitario nunha liña de oferta baseada en produto é permitir diferentes custos dun produto para cada venda.</span><span class="sxs-lookup"><span data-stu-id="c700f-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="c700f-112">Esta non é unha situación típica, pero ás veces o fornecedor pode descontar o custo do produto dependendo do cliente da venda final.</span><span class="sxs-lookup"><span data-stu-id="c700f-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="c700f-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c700f-113">For example:</span></span>

<span data-ttu-id="c700f-114">Fabrikam Robotics está instalando armas robóticas nas liñas de montaxe de A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="c700f-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="c700f-115">Fabrikam presta servizos de instalación, pero os brazos robóticos son adquiridos a Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="c700f-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="c700f-116">Se a instalación de armas robóticas en A Datum Corporation abre un novo sector vertical para as armas robóticas de Trey, Trey podería facerlle un desconto especial a Fabrikam por este acordo.</span><span class="sxs-lookup"><span data-stu-id="c700f-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="c700f-117">Neste caso, Fabrikam creará unha liña de oferta baseada en produto para Robotic Arms e introducirá un custo especial por unidade para esta oferta.</span><span class="sxs-lookup"><span data-stu-id="c700f-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="c700f-118">Este custo é diferente do custo estándar de Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="c700f-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
