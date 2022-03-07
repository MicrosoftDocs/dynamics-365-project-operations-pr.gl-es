---
title: Estimacións financeiras dos gastos en proxectos
description: Este tema ofrece información sobre a definición ou estimación de gastos baseados en proxectos.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f4d42724af61aa241671e8dacacbe2be5a7d531f55c2025a89ff777ac41e9b67
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987839"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimacións financeiras dos gastos en proxectos
_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations permite aos xestores de proxectos definir gastos baseados en proxectos para cada proxecto ou tarefa. Cada elemento de gasto pode asociarse a unha tarefa específica do proxecto. Os gastos clasifícanse en diferentes categorías de gasto, que se definen a nivel organizativo. O prezo e o custo de cada categoría de gasto defínense na lista de prezos. 

Complete os seguintes pasos para ver, engadir ou eliminar un gasto do proxecto.

1. Vaia a **Proxectos** e seleccione o proxecto no que desexa traballar.
2. Seleccione o separador **Estimacións do proxecto** e vexa a lista de gastos do proxecto.
3. Seleccione **Novo gasto** para engadir un gasto. Ou seleccione un gasto para eliminar e despois seleccione **Eliminar gasto**.

A seguinte táboa ofrece información sobre os campos da **Liña de estimación de gastos** nun proxecto. 

| **Campo** | **Descrición** | **Impacto descendente** |
| --- | --- | --- |
| Tarefa | A lista de tarefas do proxecto. Isto inclúe tarefas de resumo e nó folla. | A selección dunha tarefa para unha liña de estimación do gasto afectará ao custo estimado do gasto e as vendas estimadas dos gastos dunha tarefa. Se se deixa este campo baleiro, a estimación do gasto rastréxase e resúmese só a nivel do proxecto. |
| Categoría | Unha lista de categorías de transaccións que ligaron categorías de gastos na aplicación. | A selección dunha categoría fai que o prezo e o custo se calculen na liña de estimación de gastos. |
| Data de inicio | A data prevista na que se producirá o gasto. | Non hai ningún impacto descendente para este campo. |
| Grupo de unidades | O valor predefinido neste campo provén do grupo de unidades configurado como predefinido na categoría seleccionada. Pode actualizar este campo para seleccionar outro grupo de unidades. | Non hai ningún impacto descendente para este campo. |
| Unidade | O valor deste campo é a unidade predefinida da categoría seleccionada. Pode actualizar este campo para seleccionar outra unidade. | Cambiar a unidade dá lugar a nun prezo unitario e un custo predefinidos diferentes. |
| Importe | A cantidade do gasto estimado no que incorrerá. | Non hai ningún impacto descendente para este campo. |
| Custo da unidade | O custo da categoría seleccionada e a combinación de unidades establecidas na lista de prezos de custo aplicable | O custo unitario móstrase sempre na moeda de custo do proxecto. |
| Prezo por unidade | O prezo da categoría seleccionada e a combinación de unidades establecidas na lista de prezos de venda aplicable | O prezo unitario móstrase sempre na moeda de vendas do proxecto. |
| Custo total | O importe do custo que se calcula como cantidade de \* custo unitario.| O importe do custo móstrase sempre na moeda de custo do proxecto. |
| Total de vendas | O importe de vendas que se calcula como cantidade de \* prezo unitario. | O importe de vendas móstrase sempre na moeda de vendas do proxecto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
