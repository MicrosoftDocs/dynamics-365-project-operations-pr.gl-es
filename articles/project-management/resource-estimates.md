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


[!INCLUDE[footer-include](../includes/footer-banner.md)]