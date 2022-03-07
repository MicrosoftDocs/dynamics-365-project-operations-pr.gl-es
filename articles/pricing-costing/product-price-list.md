---
title: Listas de prezos de produtos
description: Este tema ofrece información sobre as listas de prezos nos prezos do catálogo empregados para ofertas e contratos de proxectos.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8bfd4eaa6f4bcbbdf398683a25a3b0079cfedd535ef32d383993883607f7ef5a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999224"
---
# <a name="product-price-lists"></a>Listas de prezos de produtos

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

 En Project Operations, **Listas de prezos dos produtos** e as entidades relacionadas cos elementos da lista de prezos admiten a funcionalidade para fixar o prezo dos produtos en liñas de oferta e contrato baseadas en produtos. Para os produtos utilizados en proxectos, úsanse os rexistros de elementos da lista de prezos para as listas de prezos do proxecto. 

Os produtos deben configurarse de xeito que teñan listas de custos e prezos por defecto no catálogo de produtos. Use o prezo da lista, o custo estándar e o custo actual para configurar o custo predeterminado e os prezos da lista. Os prezos da lista por defecto úsanse nunha liña de presupostos ou nunha liña de contratos de proxecto só cando o sistema non atopa unha liña de prezos para ese produto na lista de prezos do produto para a oferta ou contrato de proxecto.

O prezo de custo das liñas de catálogo de produtos pódese cambiar entre ofertas. Esta capacidade é importante, porque se non rastrexa con precisión os custos, non pode determinar os beneficios operativos nas compromisos do proxecto. Por defecto, o custo estándar do produto utilízase como prezo de custo Non obstante, o prezo de custo por defecto pódese actualizar na liña de oferta se hai un prezo de custo diferente para esa oferta.

## <a name="price-list-items"></a>Elementos da lista de prezos

Pode engadir produtos dun catálogo de produtos a diferentes listas de prezos. As liñas de lista prezos dos produtos fan referencia sempre a unha unidade específica. Os prezos dun produto dos elementos da lista de prezos pódense configurar como cantidade de moeda. Alternativamente, pódese configurar en función do prezo da lista, do custo actual ou do custo estándar.

A funcionalidade de fixación de prezos admite varias opcións de redondeo cando os prezos dos produtos están configurados en función do prezo de lista, do custo estándar ou do custo actual. Ademais de aproveitar múltiples métodos de prezos e opcións de redondeo, pode asociar listas de descontos con elementos da lista de prezos. 

 
## <a name="default-product-price-list"></a>Lista de prezos de produtos predefinida
Cada rexistro de clientes ten un campo **Lista de prezos por defecto**, onde pode especificar unha lista de prezos que coincida coa moeda do cliente. Un valor por defecto non se introduce automaticamente neste campo. Cando existe un acordo de prezos personalizado cun cliente específico, pode usar este campo para asociar unha lista de prezos a ese cliente.

As entidades Oportunidade, Oferta e Contrato de proxecto usan a seguinte orde para introducir listas de prezos de produtos por defecto. A mesma orde úsase para listas de prezos de proxecto.

1.  Oferta
2.  Oportunidade
3.  Cliente
4.  Configuración global 

Por defecto, o campo **Produto** da liña de oferta indica todos os produtos activos na lista de prezos do produto. Se un produto foi inactivado ou se é un produto borrador, non aparece na lista, aínda que estea na lista de prezos. 

As liñas de catálogo de produtos engádense como liñas de factura na primeira factura que se crea para un contrato de proxecto. Nun borrador de factura, pódense eliminar esas liñas de factura. Nese caso, as liñas aparecerán nunha factura posterior ata a facturación ou ata que a factura se envíe ao cliente. Non pode facturar unha cantidade parcial dunha liña de factura de produto. Cando se facturan as liñas de produto do contrato do proxecto, créanse datos reais. Non obstante, eses datos reais non están ligados á entidade de proxecto relacionada. Noutras palabras, as liñas de contrato de proxecto baseadas en produtos son independentes de calquera uso baseado en proxectos. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
