---
title: Custos de liñas de contrato baseadas en produto
description: Neste tema se proporciona información sobre a creación de
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "4076363"
---
# <a name="costing-product-based-contract-lines"></a>Custos de liñas de contrato baseadas en produto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_


As liñas de contrato baseado en produto en Dynamics 365 Project Operations inclúen o campo **Prezo de custo** , que almacena o prezo de custo do produto para cálculos de rendibilidade descendentes.

Cando se crea unha liña de contrato baseado en produto para un produto de catálogo, o custo da liña de contrato baseado en produto é por defecto o do campo **Custo estándar** do catálogo de produtos. O campo de **Custo estándar** do catálogo de produtos configúrase na moeda base da organización. Cando o custo unitario é predeterminado na liña de contrato, convértese na moeda de venda do contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitario nunha liña de contrato baseado en produto

Ter un custo unitario nunha liña de contrato baseado en produto permite diferentes custos de produto para cada venda dunha unidade. Aínda que non sempre é necesario, hai certos escenarios nos que o fornecedor pode descontar o custo do produto para o cliente. Teña en conta o seguinte escenario:

Fabrikam Robotics está instalando armas robóticas nas liñas de montaxe de Adatum Corporation. Fabrikam presta servizos de instalación, pero os brazos robóticos son adquiridos a Trey Research. Se a instalación de armas robóticas en Adatum Corporation abre un novo sector vertical para Trey Research, poderían ofrecerlle un desconto especial a Fabrikam por este acordo. Neste caso, Fabrikam crea unha liña de contrato baseado en produto para Robotic Arms e introduce un custo unitario para este contrato que é diferente do custo estándar dos brazos robóticos de Trey Research.
