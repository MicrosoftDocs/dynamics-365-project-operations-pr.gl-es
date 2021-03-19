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
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273691"
---
# <a name="cost-product-based-contract-lines---lite"></a>Custo de liñas de contrato baseado en de produto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_


As liñas de contrato baseado en produtos en Dynamics 365 Project Operations inclúen o campo **Prezo de custo**, que almacena o prezo de custo do produto para cálculos de rendibilidade descendentes.

Cando se crea unha liña de contrato baseada en produto para un produto de catálogo, o custo da liña é por defecto o do campo **Custo estándar** do catálogo de produtos. O campo de **Custo estándar** do catálogo de produtos configúrase na moeda base da organización. Cando o custo unitario é predeterminado na liña de contrato, convértese na moeda de venda do contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitario nunha liña de contrato baseado en produto

Ter un custo unitario nunha liña de contrato baseado en produto permite diferentes custos de produto para cada venda dunha unidade. Aínda que non sempre é necesario, hai certos escenarios nos que o fornecedor pode descontar o custo do produto para o cliente. Teña en conta o seguinte escenario:

Fabrikam Robotics está instalando armas robóticas nas liñas de montaxe de Adatum Corporation. Fabrikam ofrece servizos de instalación, pero os brazos robóticos son de Trey Research. Se a instalación de armas robóticas en Adatum Corporation abre un novo sector vertical para Trey Research, poderían ofrecerlle un desconto especial a Fabrikam por este acordo. Neste caso, Fabrikam crea unha liña de contrato baseado en produto para Robotic Arms. Para este contrato introdúcese un custo unitario. O custo é diferente do custo dos brazos robóticos de Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]