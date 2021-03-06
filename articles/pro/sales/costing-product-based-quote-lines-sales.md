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
# <a name="costing-product-based-quote-lines"></a>Custos de liñas de oferta baseadas en produto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


As liñas de oferta baseada en produto en Dynamics 365 Project Operations tamén teñen un campo **Prezo de custo**. Este campo úsase para rastrexar o prezo de custo do produto na liña de oferta e para cálculos de rendibilidade descendentes.

Cando se crea unha liña de oferta baseada en produto para un produto de catálogo, o custo da liña de oferta baseada en produto é por defecto o do campo **Custo estándar** do catálogo de produtos. O campo de custo estándar do catálogo de produtos configúrase na moeda base da organización. O custo unitario predefinido da liña de oferta baseada en produto convértese na moeda de vendas da oferta.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Custo unitario nunha liña de oferta baseada en produto

A finalidade de ter un custo unitario nunha liña de oferta baseada en produto é permitir diferentes custos dun produto para cada venda. Esta non é unha situación típica, pero ás veces o fornecedor pode descontar o custo do produto dependendo do cliente da venda final.

Por exemplo:

Fabrikam Robotics está instalando armas robóticas nas liñas de montaxe de A Datum Corporation. Fabrikam presta servizos de instalación, pero os brazos robóticos son adquiridos a Trey robotics. Se a instalación de armas robóticas en A Datum Corporation abre un novo sector vertical para as armas robóticas de Trey, Trey podería facerlle un desconto especial a Fabrikam por este acordo.

Neste caso, Fabrikam creará unha liña de oferta baseada en produto para Robotic Arms e introducirá un custo especial por unidade para esta oferta. Este custo é diferente do custo estándar de Trey Robotic Arms.
