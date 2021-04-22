---
title: Rastrexo de esforzo de proxectos
description: Este tema ofrece información sobre como rastrexar o esforzo do proxecto e o progreso do traballo.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710938"
---
# <a name="project-effort-tracking"></a>Rastrexo de esforzo de proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A necesidade de rastrexar o progreso cunha programación varía segundo o sector. Algúns sectores rastrexan a un nivel granular, mentres que outros sectores rastrexan a un nivel máis alto. Este tema mostra como programar para cumprir os requisitos da súa organización.

## <a name="effort-tracking-view"></a>Visualización de rastrexamento do esforzo

A vista **Rastrexo do esforzo** rastrexa o progreso das tarefas de programación comparando as horas de esforzo real dedicadas a unha tarefa coas horas de esforzo planificadas da tarefa. Dynamics 365 Project Operations usa as seguintes fórmulas para calcular as métricas de seguimento:

- **Porcentaxe de progreso**: Esforzo real realizado ata a data ÷ Estimación ao completar (EAC) 
- **Esforzo restante**: Esforzo estimado ao finalizar – Esforzo real realizado ata a data 
- **EAC**: Esforzo restante + Esforzo real realizado ata a data 
- **Varianza de esforzo proxectado**: Esforzo planificado - EAC

Project Operations mostra unha proxección da varianza de esforzo na tarefa. Se a EAC supón un esforzo superior ao previsto, proxéctase que a tarefa levará máis tempo do que estaba previsto inicialmente e está atrasada. Se a EAC supón un esforzo inferior ao previsto, proxéctase que a tarefa levará menos tempo do que estaba previsto inicialmente e está adiantada.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Reproxección de esforzo en tarefas de nó folla

Os xestores de proxectos revisan con frecuencia as estimacións orixinais dunha tarefa. As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto. Non obstante, non recomendamos que os xestores de proxectos cambien os números de esforzo planificados. Isto débese a que o esforzo planificado do proxecto representa a orixe da verdade establecida para o programa do proxecto e a estimación de custos, e todos os interesados do proxecto estiveron de acordo.

Un xestor de proxectos pode reproxectar o esforzo nas tarefas actualizando o valor predefinido do **Esforzo restante** cunha nova estimación na tarefa. Esta actualización provoca un novo cálculo da estimación da tarefa ao finalizar (EAC), a porcentaxe de progreso e a variación do esforzo proxectada nunha tarefa. Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nova proxección do esforzo en tarefas resumo

Pódese proxectar de novo o esforzo en tarefas resumo ou en tarefas contedor. Os xestores de proxectos poden actualizar o esforzo restante nas tarefas resumo. A actualización do esforzo restante desencadea o seguinte conxunto de cálculos na aplicación:

- Calcúlanse o EAC e a porcentaxe progreso da tarefa.
- O nova EAC distribúese nas tarefas dependentes na mesma proporción que o EAC orixinal estaba na tarefa.
- Calcúlase o novo EAC en cada unha das tarefas individuais ata as tarefas do nó folla. 
- As tarefas dependentes afectadas ata os nós folla teñen o seu esforzo restante e a porcentaxe de progreso calculada de novo en función do valor de EAC. Isto da lugar a unha nova proxección para a varianza de esforzo da tarefa. 
- Calcúlanse de novo os EAC das tarefas resumo ata o nó raíz.


## <a name="project-status-summary"></a>Resumo do estado do proxecto

Os datos de rastrexo nas vistas **Rastrexo do esforzo** e **Rastrexo de custos** mostran o progreso e o consumo de custos aos niveis de nó raíz do proxecto, tarefas de resumo e tarefas de nó folla. A sección **Estado** de páxina **Entidade do proxecto** mostra un resumo do estado a nivel de proxecto.

## <a name="status-summary-fields"></a>Campos resumo do estado

O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto. Emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente. O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado. O campo **Estado actualizado o** non se pode editar e o valor é unha marca de tempo que indica cando se actualizou o estado por última vez.

Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da data de rastrexo. Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, pode axustar estes campos a **Adiantado**. Cando o calendario e a varianza de custos para o nó raíz son negativos, pode configuralos en **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
