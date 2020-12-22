---
title: Métodos de custo para completar
description: Este tema ofrece información sobre os métodos empregados para calcular o custo para completar un proxecto.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531424"
---
# <a name="cost-to-complete-methods"></a>Métodos de custo para completar

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema ofrece información sobre os métodos empregados para calcular o custo para completar un proxecto. Hai varios métodos que pode usar para calcular o custo para completar un proxecto. 

Cando crea unha estimación para un proxecto, na páxina **Crear estimación**, no campo **Método de custo para completar**, pode seleccionar un dos seguintes métodos de custo para completar.

| Método de custo para completar    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Custo total-real            | Introduza os custos de estimación manualmente nos campos **Custo total** ou **Cantidade total** usando o botón **Estimación de custos** na páxina **Estimación**. O sistema resta os custos reais dos totais que introduciu. O total é o custo para completar o proxecto. Este método non usa as estimacións de gastos e as atribucións de recursos introducidos en Project Operations integrado en Microsoft Dataverse. O custo total ou a cantidade total pódense actualizar manualmente segundo sexa necesario.  |
| Previsión total-real        | As atribucións de recursos e as estimacións de gastos úsanse para determinar o importe total previsto do proxecto. Os custos reais compáranse con esta previsión para calcular o custo para completar.                                                                                                                                                                                                                                                                          |
| Como estimación anterior         | Aquí utilízanse os mesmos métodos de estimación que se empregaron no período anterior. Este método require un modelo de previsión se o período anterior requiría un modelo de previsión.                                                                                                                                                                                                                                                                                                                           |
| Establecer o custo para completar en cero | Normalmente utilizado antes de que se elimine o proxecto de estimación, este método coincide coas estimacións totais coas transaccións reais rexistradas e borra a columna **Custo para completar**. Cando se completa, o resultado sempre é do 100 por cento. Para cada liña de custo que cree, a caixa de verificación **Previsión** se desmarca e se copia a estimación total da estimación de custo anterior. O consumo real para o período estimado dedúcese do custo para completar o proxecto.              |
| A partir do modelo de custo           | O método de custo para completar que se configura no modelo de custo asociado ao proxecto de estimación seleccionado.                                                                                                                                                                                                                                                                                                                                                                          |
