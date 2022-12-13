---
title: Custos de liñas de oferta baseadas en produto
description: Este artigo fornece información sobre aplicar un prezo de custo a unha liña de oferta baseada en produtos.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825609"
---
# <a name="costing-product-based-quote-lines"></a>Custos de liñas de oferta baseadas en produto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_


As liñas de oferta baseada en produto en Dynamics 365 Project Operations tamén teñen un campo **Prezo de custo**. Este campo úsase para rastrexar o prezo de custo do produto na liña de oferta e para cálculos de rendibilidade descendentes.

Cando se crea unha liña de oferta baseada en produto para un produto de catálogo, o custo da liña de oferta baseada en produto é por defecto o do campo **Custo estándar** do catálogo de produtos. O campo de custo estándar do catálogo de produtos configúrase na moeda base da organización. O custo unitario predefinido da liña de oferta baseada en produto convértese na moeda de vendas da oferta.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Custo unitario nunha liña de oferta baseada en produto

A finalidade de ter un custo unitario nunha liña de oferta baseada en produto é permitir diferentes custos dun produto para cada venda. Esta non é unha situación típica, pero ás veces o fornecedor pode descontar o custo do produto dependendo do cliente da venda final.

Por exemplo:

Fabrikam Robotics está instalando armas robóticas nas liñas de montaxe de A Datum Corporation. Fabrikam presta servizos de instalación, pero os brazos robóticos son adquiridos a Trey robotics. Se a instalación de armas robóticas en A Datum Corporation abre un novo sector vertical para as armas robóticas de Trey, Trey podería facerlle un desconto especial a Fabrikam por este acordo.

Neste caso, Fabrikam creará unha liña de oferta baseada en produto para Robotic Arms e introducirá un custo especial por unidade para esta oferta. Este custo é diferente do custo estándar de Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
