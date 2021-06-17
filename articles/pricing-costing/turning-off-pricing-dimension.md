---
title: Desactivar unha dimensión de prezos
description: Este tema fornece información sobre como desactivar dimensións de prezos.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004529"
---
# <a name="turning-off-a-pricing-dimension"></a>Desactivar unha dimensión de prezos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pode que necesite revisar e actualizar a súa estratexia de prezos cada poucos anos. Todas as actualizacións que faga pode requirir que desactive unha dimensión de prezos existente e cree unha nova. Por exemplo, pode ter un prezo anterior por **Rol**, pero agora decidiu establecer os prezos por **Experiencia laboral**. Isto pode requirir que desactive **Rol** como dimensión de prezos e cree **Experiencia laboral** como unha nova dimensión de prezos. 

Para desactivar unha dimensión de prezos, independentemente de se é lista para usar ou personalizada, pode configurar os campos **Aplicable ao custo** e **Aplicable ás vendas** da dimensión de prezos en **Non**.

Non obstante, cando fai isto, pode que reciba a mensaxe de erro, **A dimensión de prezos non se pode actualizar nin eliminar se hai rexistros de prezos asociados.**

![Erro de proceso de negocio ao desactivar unha dimensión de prezos](media/Business-Process-Error.png)

Esta mensaxe de erro indica que hai rexistros de prezos previamente configurados para a dimensión que se vai desactivar. Todos os rexistros de **Prezo de rol** e **Sobreprezo de rol** que fan referencia a unha dimensión deben ser eliminados antes de que se poida establecer a aplicabilidade da dimensión en **Non**. Esta regra aplícase tanto ás dimensións de prezos listas para usar como ás dimensións de prezos personalizadas que creou. O motivo desta validación é que cada rexistro de **Prezo de rol** debe ter unha combinación única de dimensións. Por exemplo, nunha lista de prezos chamada **Taxas de custos de EUA 2018**, ten as seguinte filas de **Prezo de rol**. 

| Título estándar         | Unidade organizativa    |Unidade   |Prezo  |Moeda  |
| -----------------------|-------------|-------|-------|----------|
| Enxeñeiro de sistemas|Contoso EUA|Hora| 100|USD|
| Enxeñeiro de sistemas sénior|Contoso EUA|Hora| 150| USD|


Cando desactive **Título estándar** como dimensión de prezos e o motor de prezos busque un prezo, só empregará o valor **Unidade organizativa** do contexto de entrada. Se a **Unidade organizativa** do contexto de entrada é "Contoso Estados Unidos", o resultado non será determinista porque coincidirán as dúas filas. Para evitar este escenario, cando cree rexistros de **Prezo de rol**, o sistema valida que a combinación de dimensións é única. Se a dimensión está desactivada despois da creación de rexistros de **Prezo de rol**, pódese violar esta restrición. Polo tanto, é necesario que antes de desactivar unha dimensión, elimine todas as filas de **Prezo de rol** e **Sobreprezo de rol** que encheu ese valor de dimensión.


[!INCLUDE[footer-include](../includes/footer-banner.md)]