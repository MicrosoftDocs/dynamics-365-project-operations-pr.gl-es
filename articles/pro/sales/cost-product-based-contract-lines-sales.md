---
title: Custo de liñas de contrato baseado en de produto - lite
description: Neste tema se proporciona información sobre a creación de
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764457"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="82979-103">Custo de liñas de contrato baseado en de produto - lite</span><span class="sxs-lookup"><span data-stu-id="82979-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="82979-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="82979-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="82979-105">As liñas de contrato baseado en produtos en Dynamics 365 Project Operations inclúen o campo **Prezo de custo**, que almacena o prezo de custo do produto para cálculos de rendibilidade descendentes.</span><span class="sxs-lookup"><span data-stu-id="82979-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="82979-106">Cando se crea unha liña de contrato baseada en produto para un produto de catálogo, o custo da liña é por defecto o do campo **Custo estándar** do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="82979-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="82979-107">O campo de **Custo estándar** do catálogo de produtos configúrase na moeda base da organización.</span><span class="sxs-lookup"><span data-stu-id="82979-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="82979-108">Cando o custo unitario é predeterminado na liña de contrato, convértese na moeda de venda do contrato.</span><span class="sxs-lookup"><span data-stu-id="82979-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="82979-109">Custo unitario nunha liña de contrato baseado en produto</span><span class="sxs-lookup"><span data-stu-id="82979-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="82979-110">Ter un custo unitario nunha liña de contrato baseado en produto permite diferentes custos de produto para cada venda dunha unidade.</span><span class="sxs-lookup"><span data-stu-id="82979-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="82979-111">Aínda que non sempre é necesario, hai certos escenarios nos que o fornecedor pode descontar o custo do produto para o cliente.</span><span class="sxs-lookup"><span data-stu-id="82979-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="82979-112">Teña en conta o seguinte escenario:</span><span class="sxs-lookup"><span data-stu-id="82979-112">Consider the following scenario:</span></span>

<span data-ttu-id="82979-113">Fabrikam Robotics está instalando armas robóticas nas liñas de montaxe de Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="82979-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="82979-114">Fabrikam ofrece servizos de instalación, pero os brazos robóticos son de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="82979-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="82979-115">Se a instalación de armas robóticas en Adatum Corporation abre un novo sector vertical para Trey Research, poderían ofrecerlle un desconto especial a Fabrikam por este acordo.</span><span class="sxs-lookup"><span data-stu-id="82979-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="82979-116">Neste caso, Fabrikam crea unha liña de contrato baseado en produto para Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="82979-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="82979-117">Para este contrato introdúcese un custo unitario.</span><span class="sxs-lookup"><span data-stu-id="82979-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="82979-118">O custo é diferente do custo dos brazos robóticos de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="82979-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
