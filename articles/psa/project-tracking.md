---
title: Progreso do proxecto e consumo de custos
description: Este tema ofrece información sobre o rastrexo do progreso do proxecto e o consumo de custos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283636"
---
# <a name="project-progress-and-cost-consumption"></a>Progreso do proxecto e consumo de custos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A necesidade de rastrexar o progreso cunha programación varía segundo o sector. Algúns sectores rastrexan a un nivel granular, mentres que outros sectores rastrexan a un nivel máis alto. Este tema mostra como programar para cumprir os requisitos da súa organización.

## <a name="effort-tracking-view"></a>Visualización de rastrexamento do esforzo

A vista **Rastrexo do esforzo** rastrexa o progreso das tarefas na programación. Compara as horas de esforzo real dedicadas a unha tarefa coas horas de esforzo planificadas da tarefa. Project Service Automation usa as seguintes fórmulas para calcular as métricas de seguimento:

Inicialmente na creación da tarefa: O custo planificado establecerase segundo o custo estimado ao finalizar. Unha vez rexistrados os datos reais na tarefa, o seguinte será o cálculo na vista de rastrexo do esforzo

- Porcentaxe de progreso = Esforzo real realizado ata a data ÷ Estimación ao completar (EAC) 
- Estimación para completar (ETC) = Estimación ao completar (EAC) – Esforzo real realizado ata a data 
- EAC = Esforzo restante + Esforzo real realizado ata a data 
- Varianza de esforzo proxectado = Esforzo planificado - EAC

Project Service Automation mostra unha proxección da varianza de esforzo na tarefa. Se a EAC supón un esforzo superior ao previsto, proxéctase que a tarefa levará máis tempo do que estaba previsto inicialmente. Polo tanto, está atrasada. Se a EAC supón un esforzo inferior ao previsto, proxéctase que a tarefa levará menos tempo do que estaba previsto inicialmente. Polo tanto, está adiantada.

## <a name="reprojecting-effort"></a>Proxectar de novo o esforzo

É frecuente que un xestor de proxectos revise as estimacións orixinais dunha tarefa. As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto. Non obstante, non recomendamos que os xestores de proxectos modifiquen os números da liña base, porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.

Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:

- Anular o ETC predefinido cunha nova estimación do esforzo restante real da tarefa. 
- Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.

Cada un destes enfoques provoca un novo cálculo do ETC, EAC e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa. Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nova proxección do esforzo en tarefas resumo

Pódese proxectar de novo o esforzo en tarefas resumo ou en tarefas contedor. Independentemente de que o usuario volva proxectar empregando o esforzo restante ou a porcentaxe de progreso nas tarefas resumo, comeza o seguinte conxunto de cálculos:

- Calcúlanse o EAC, ETC e a porcentaxe progreso da tarefa.
- O nova EAC distribúese nas tarefas dependentes na mesma proporción que o EAC orixinal estaba na tarefa.
- Calcúlase o novo EAC en cada unha das tarefas individuais ata as tarefas do nó folla. 
- As tarefas dependentes afectadas ata os nós folla teñen a súa ETC e a porcentaxe de progreso calculada de novo en función do valor de EAC. Isto da lugar a unha nova proxección para a varianza de esforzo da tarefa. 
- Calcúlanse de novo os EAC das tarefas resumo ata o nó raíz.

### <a name="cost-tracking-view"></a>Vista de rastrexo de custo 

A vista **Seguimento de custos** compara o custo real que se gastou nunha tarefa co custo planificado. 

> [!NOTE]
> Esta vista mostra só os custos laborais e non inclúe os custos das estimacións de gastos. 

Project Service Automation usa as seguintes fórmulas para calcular as métricas de seguimento:

Cando se crea unha tarefa, o custo previsto é igual ao custo estimado ao completar. Despois de rexistrar os datos reais na tarefa, o seguinte calcúlase na vista de **Rastrexo** do custo:

 - Porcentaxe do custo consumido = Custo real gastado ata a data ÷ Custo estimado ao completar para a tarefa
 - Custo para completar (CTC) = Custo estimado ao completar - Custo real gastado ata a data
 - Custo estimado ao completar = CTC + Custo real gastado ata a data
 - Variación do custo proxectado = Custo planificado – Custo estimado ao completar

A proxección da varianza de custo móstrase na tarefa. Se o custo estimado para completar supón un esforzo superior ao custo previsto, proxéctase que a tarefa custará máis do que estaba previsto inicialmente. Polo tanto, tende a superar o orzamento. Se o custo estimado ao completar é inferior ao custo previsto, proxéctase que a tarefa custará menos do que estaba previsto inicialmente.

## <a name="project-managers-reprojection-of-cost"></a>Nova proxección de custos do xestor de proxectos

Cando se proxecta de novo o esforzo, todos os CTC, custo estimado ao completar, porcentaxe de custo consumido e varianza de custo proxectado calcúlanse de novo na vista **Rastrexo de custos**.

## <a name="project-status-summary"></a>Resumo do estado do proxecto

Os datos de rastrexo nas vistas **Rastrexo do esforzo** e **Rastrexo de custos** mostran o progreso e o consumo de custos aos niveis de nó raíz do proxecto, tarefas de resumo e tarefas de nó folla. A sección **Estado** de páxina **Entidade do proxecto** mostra un resumo do estado a nivel de proxecto.

## <a name="status-summary-fields"></a>Campos resumo do estado

O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto. Emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente. O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado. O campo **Estado actualizado o** non se pode editar e o valor é unha marca de tempo que indica cando se actualizou o estado por última vez.

Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da data de rastrexo. Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, pode axustar estes campos a **Adiantado**. Cando o calendario e a varianza de custos para o nó raíz son negativos, pode configuralos en **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]