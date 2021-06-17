---
title: Estimacións financeiras dos materiais en proxectos
description: Este tema ofrece información sobre a definición ou estimación de materiais baseados en proxectos.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 768da6adb83b4593a227f60182179b3036f4c040
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002684"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimacións financeiras dos materiais en proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations permite aos xestores de proxectos definir custos de material baseados en proxectos para cada proxecto ou tarefa. Cada estimación de material pode asociarse a unha tarefa específica do proxecto. Os gastos clasifícanse en diferentes categorías de gasto, que se definen a nivel organizativo. O prezo e o custo de cada categoría de gasto defínense na lista de prezos. 

Complete os seguintes pasos para ver, engadir ou eliminar unha estimación do material do proxecto.

1. Vaia a **Proxectos** e seleccione o proxecto que desexa actualizar.
2. No separador **Estimacións de materiais**, vexa a lista de estimacións de material do proxecto.
3. Seleccione **Nova estimación de material** para crear unha nova estimación de material. Ou seleccione unha estimación de material para eliminar e logo seleccione **Eliminar estimación de material**.

A seguinte táboa ofrece información sobre os campos da **Liña de estimación de material** nun proxecto. 

| **Campo** | **Descrición** | **Impacto descendente** |
| --- | --- | --- |
| Tarefa | A lista de tarefas do proxecto. Isto inclúe tarefas de resumo e nó folla. | Cando selecciona unha tarefa para unha liña de estimación de material, o custo estimado do material e as vendas de material estimadas para unha tarefa vense afectados. Se este campo está baleiro, a estimación do material rastréxase e resúmese só a nivel do proxecto. |
| Seleccionar produto |  Pode especificar se a liña de estimación é para un produto existente (catálogo) ou un produto fóra de catálogo. | Este campo determina se selecciona un produto do catálogo ou un produto fóra de catálogo. |
| Produto | O ID do produto do catálogo de produtos. Cando selecciona un ID de produto, o valor do campo **Seleccionar produto** actualízase automaticamente a **Produto existente**. O ID úsase para recuperar os prezos de custo e venda da lista de prezos. | Non hai ningún impacto descendente para este campo. |
| Descrición do produto fóra de catálogo | Un campo de texto para escribir o nome do produto. Este campo debería usarse só cando seleccione **Fóra de catálogo** no campo **Seleccionar produto**.| Non hai ningún impacto descendente para este campo. |
| Data de inicio | A data prevista na que se prevé empregar o material. | Non hai ningún impacto descendente para este campo. |
| Grupo de unidades | O valor predefinido deste campo provén do grupo de unidades predefinido do produto de catálogo. Pode actualizar este campo para seleccionar outro grupo de unidades. | Non hai ningún impacto descendente para este campo. |
| Unidade | O valor deste campo procede da unidade predefinida do produto seleccionado. Pode actualizar este campo para seleccionar outra unidade. | Cambiar a unidade dá lugar a nun prezo unitario e un custo predefinidos diferentes. |
| Importe | A cantidade estimada do produto que se utilizará no proxecto. | Non hai ningún impacto descendente para este campo. |
| Custo da unidade | O custo unitario do produto seleccionado e a combinación de unidades establecidas na lista de prezos de custo aplicable | O custo unitario móstrase sempre na moeda de custo do proxecto. Se non hai unha configuración do custo unitario para a combinación do produto e a configuración unitaria na lista de prezos, o custo unitario será por defecto 0,00. |
| Prezo por unidade | O prezo do produto seleccionado e a combinación de unidades establecidas na lista de prezos de venda aplicable | O prezo unitario móstrase sempre na moeda de vendas do proxecto. Se non hai unha configuración do prezo unitario para a combinación do produto e a configuración unitaria na lista de prezos, o prezo unitario será por defecto 0,00.|
| Custo total | O importe do custo que se calcula como cantidade de \* custo unitario.| O importe do custo móstrase sempre na moeda de custo do proxecto. |
| Total de vendas | O importe de vendas que se calcula como cantidade de \* prezo unitario. | O importe de vendas móstrase sempre na moeda de vendas do proxecto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
