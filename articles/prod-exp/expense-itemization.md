---
title: Detalle de gastos
description: Este artigo explica como detallar os gastos usando a área de traballo de Gasto reinventada.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920932"
---
# <a name="expense-itemization"></a>Detalle de gastos

[!include [banner](../includes/banner.md)]

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

As organizacións adoitan esixir aos empregados que proporcionen un desglose detallado dos gastos realizados durante a viaxe. Por exemplo, un folio de hotel pode conter varias liñas detalladas sobre a tarifa da habitación, os impostos, o aparcamento e outros gastos diversos ocasionados cada día durante a estancia. Ou un gasto de comida pode requirir que proporcione un desglose máis granular para o almorzo, o xantar ou a cea. Sexa cal sexan as necesidades da organización, cada categoría de gasto pódese configurar para reflectir as subcategorías ou as partidas que compoñen un gasto. Aínda que o detallado sempre foi compatible na área de traballo **Xestión de gastos**, ou **Gasto reinventado**, permite un detallado máis eficiente cando a función **Capacidade de detallar os gastos recorrentes rapidamente** está activada.  

## <a name="enable-quick-itemization"></a>Activar detallado rápido 

Pode usar a funcionalidade **Capacidade de detallar os gastos recorrentes rapidamente** para detallar os gastos recorrentes rapidamente evitando a necesidade de introducir os gastos diarios cada vez durante a estancia. Complete os seguintes pasos para activar o detallado rápido.

1. Vaia á área de traballo **Xestión de funcionalidades** e na lista de funcionalidades, localice e seleccione **Informes de gastos reinventados**. 
2. Seleccione **Activar agora**. 
3. Na lista de funcionalidades, localice e seleccione **Capacidade de detallar os gastos recorrentes rapidamente**.
4. Seleccione **Activar agora**. 

## <a name="itemization-grid"></a>Grade de detallado 

Se unha categoría de gasto ten subcategorías ou compoñentes diferentes que compoñen ese gasto, pódese detallar. Para detallar un gasto, seleccione a liña de gasto no informe de gastos e no panel **Detalles do gasto**, seleccione **Accións** > **Detallar**. A barra de desprazamento **Detallado** revela unha grade con campos. A seguinte táboa ofrece un exemplo de cada campo da grade e como se representa o campo no informe de gastos. 

|     Campo          |     Descripción                                                                                  |     Exemplo              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subcategoría    |     A lista de subcategorías configuradas baixo o tipo de categoría de gasto **Hotel**.             |     Tarifa diaria da habitación      |
|     Data de inicio     |     A data na que se incorreu por primeira vez na partida de gasto.                                           |     09/13/2021           |
|     Tarifa diaria     |     O importe incorrido pola partida de gasto.                                                    |     200                  |
|     Cantidade       |     O número de veces que se repite o cargo nun período continuo.                       |     3                    |

![Detalle o gasto.](media/Itemization%20screen%201.png)

Cando garde un detallado, verá unha liña detallada individual para a cantidade especificada na grade de detallado. Cada liña comeza na data especificada na grade.

![Informe detallado.](media/Itemization%20screen%202.png)

