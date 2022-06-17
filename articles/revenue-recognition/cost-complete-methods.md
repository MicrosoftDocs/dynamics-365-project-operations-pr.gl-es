---
title: Métodos de custo para completar
description: Este artigo ofrece información sobre os métodos utilizados para calcular o custo para completar un proxecto.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920288"
---
# <a name="cost-to-complete-methods"></a>Métodos de custo para completar

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo ofrece información sobre os métodos utilizados para calcular o custo para completar un proxecto. Hai varios métodos que pode usar para calcular o custo para completar un proxecto. 

Cando crea unha estimación para un proxecto, na páxina **Crear estimación**, no campo **Método de custo para completar**, pode seleccionar un dos seguintes métodos de custo para completar.

| Método de custo para completar    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Custo total-real            | Introduza os custos de estimación manualmente nos campos **Custo total** ou **Cantidade total** usando o botón **Estimación de custos** na páxina **Estimación**. O sistema resta os custos reais dos totais que introduciu. O total é o custo para completar o proxecto. Este método non usa as estimacións de gastos e as atribucións de recursos introducidos en Project Operations integrado en Microsoft Dataverse. O custo total ou a cantidade total pódense actualizar manualmente segundo sexa necesario.  |
| Previsión total-real        | As atribucións de recursos e as estimacións de gastos úsanse para determinar o importe total previsto do proxecto. Os custos reais compáranse con esta previsión para calcular o custo para completar.                                                                                                                                                                                                                                                                          |
| Como estimación anterior         | Aquí utilízanse os mesmos métodos de estimación que se empregaron no período anterior. Este método require un modelo de previsión se o período anterior requiría un modelo de previsión.                                                                                                                                                                                                                                                                                                                           |
| Establecer o custo para completar en cero | Normalmente utilizado antes de que se elimine o proxecto de estimación, este método coincide coas estimacións totais coas transaccións reais rexistradas e borra a columna **Custo para completar**. Cando se completa, o resultado sempre é do 100 por cento. Para cada liña de custo que cree, a caixa de verificación **Previsión** se desmarca e se copia a estimación total da estimación de custo anterior. O consumo real para o período estimado dedúcese do custo para completar o proxecto.              |
| A partir do modelo de custo           | O método de custo para completar que se configura no modelo de custo asociado ao proxecto de estimación seleccionado.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]