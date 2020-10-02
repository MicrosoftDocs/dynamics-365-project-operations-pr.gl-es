---
title: Actualizar estimación ao finalizar
description: Este tema ofrece información sobre a actualización da proxección do esforzo nun proxecto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897764"
---
# <a name="update-estimate-at-completion"></a>Actualizar estimación ao finalizar

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

É frecuente que un xestor de proxectos revise as estimacións orixinais dunha tarefa. As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto. Non obstante, non recomendamos que os xestores de proxectos modifiquen os números da liña base, porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.

Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:

- Anular o tempo estimado para finalizar (ETC) predefinido cunha nova estimación do esforzo restante real da tarefa. 
- Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.

Cada un destes enfoques provoca un novo cálculo do ETC, a estimación ao completar (EAC) e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa. Calcúlanse de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.
