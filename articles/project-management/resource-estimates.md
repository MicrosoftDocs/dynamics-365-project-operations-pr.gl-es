---
title: Estimacións de recursos
description: Este tema ofrece información sobre como se calculan as estimacións de recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076052"
---
# <a name="resource-estimates"></a>Estimacións de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As estimacións de recursos proceden dun esforzo de fases de tempo que se define na estrutura de subdivisión do traballo xunto coas dimensións de prezos aplicables. Normalmente, o cálculo é **taxa/hora para cada rol x horas.** O esforzo de fases de tempo para cada recurso almacénase no rexistro de atribución de recursos. Os prezos almacénanse nunha lista de prezos predefinida. A conversión de unidades aplícase en función da lista de prezos aplicable.

![Estimacións de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prezo de custo e moeda de custos por defecto

Os prezos de custo son por defecto os da unidade organizativa.

## <a name="default-bill-rate-and-sales-currency"></a>Taxa de facturación de gastos e moeda de vendas por defecto

Os prezos de vendas aplícanse unha vez por acordo. A xerarquía da lista de prezos de venda predefinida é a seguinte:

1. Organización
2. Cliente
3. Oferta/contrato
