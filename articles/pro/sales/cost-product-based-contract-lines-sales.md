---
title: Custo de liñas de contrato baseado en de produto - lite
description: Neste tema se proporciona información sobre a creación de
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177239"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="37e40-103">Custo de liñas de contrato baseado en de produto - lite</span><span class="sxs-lookup"><span data-stu-id="37e40-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="37e40-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="37e40-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="37e40-105">As liñas de contrato baseado en produto en Dynamics 365 Project Operations inclúen o campo **Prezo de custo**, que almacena o prezo de custo do produto para cálculos de rendibilidade descendentes.</span><span class="sxs-lookup"><span data-stu-id="37e40-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="37e40-106">Cando se crea unha liña de contrato baseado en produto para un produto de catálogo, o custo da liña de contrato baseado en produto é por defecto o do campo **Custo estándar** do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="37e40-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="37e40-107">O campo de **Custo estándar** do catálogo de produtos configúrase na moeda base da organización.</span><span class="sxs-lookup"><span data-stu-id="37e40-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="37e40-108">Cando o custo unitario é predeterminado na liña de contrato, convértese na moeda de venda do contrato.</span><span class="sxs-lookup"><span data-stu-id="37e40-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="37e40-109">Custo unitario nunha liña de contrato baseado en produto</span><span class="sxs-lookup"><span data-stu-id="37e40-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="37e40-110">Ter un custo unitario nunha liña de contrato baseado en produto permite diferentes custos de produto para cada venda dunha unidade.</span><span class="sxs-lookup"><span data-stu-id="37e40-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="37e40-111">Aínda que non sempre é necesario, hai certos escenarios nos que o fornecedor pode descontar o custo do produto para o cliente.</span><span class="sxs-lookup"><span data-stu-id="37e40-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="37e40-112">Teña en conta o seguinte escenario:</span><span class="sxs-lookup"><span data-stu-id="37e40-112">Consider the following scenario:</span></span>

<span data-ttu-id="37e40-113">Fabrikam Robotics está instalando armas robóticas nas liñas de montaxe de Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="37e40-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="37e40-114">Fabrikam presta servizos de instalación, pero os brazos robóticos son adquiridos a Trey Research.</span><span class="sxs-lookup"><span data-stu-id="37e40-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="37e40-115">Se a instalación de armas robóticas en Adatum Corporation abre un novo sector vertical para Trey Research, poderían ofrecerlle un desconto especial a Fabrikam por este acordo.</span><span class="sxs-lookup"><span data-stu-id="37e40-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="37e40-116">Neste caso, Fabrikam crea unha liña de contrato baseado en produto para Robotic Arms e introduce un custo unitario para este contrato que é diferente do custo estándar dos brazos robóticos de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="37e40-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
