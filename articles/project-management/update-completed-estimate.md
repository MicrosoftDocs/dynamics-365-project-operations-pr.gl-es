---
title: Actualizar estimación ao finalizar
description: Este tema ofrece información sobre a actualización da proxección do esforzo nun proxecto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286426"
---
# <a name="update-estimate-at-completion"></a>Actualizar estimación ao finalizar

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

É frecuente que un xestor de proxectos revise as estimacións orixinais dunha tarefa. As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto. Non obstante, non recomendamos que os xestores de proxectos modifiquen os números da liña base, porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.

Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:

- Anular o tempo estimado para finalizar (ETC) predefinido cunha nova estimación do esforzo restante real da tarefa. 
- Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.

Cada un destes enfoques provoca un novo cálculo do ETC, a estimación ao completar (EAC) e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa. Calcúlanse de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]