---
title: Progreso do proxecto e consumo de custos
description: Este tema ofrece información sobre como rastrexar o progreso do proxecto e o consumo de custos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751444"
---
# <a name="project-progress-and-cost-consumption"></a>Progreso do proxecto e consumo de custos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A necesidade de rastrexar o progreso cunha programación varía segundo o sector. Algúns sectores rastrexan a un nivel granular, mentres que outros sectores rastrexan a un nivel máis alto. Este tema mostra como programar para cumprir os requisitos da súa organización.

## <a name="effort-tracking-view"></a>Visualización de rastrexamento do esforzo

A vista **Rastrexo do esforzo** rastrexa o progreso das tarefas na programación. Compara as horas de esforzo real dedicadas a unha tarefa coas horas de esforzo planificadas para esa tarefa. PSA usa as seguintes fórmulas para calcular as métricas de seguimento:

- Porcentaxe de progreso = Esforzo real realizado ata a data ÷ Esforzo planificado para a tarefa 
- Estimación para completar (ETC) = Esforzo previsto - Esforzo real realizado ata a data 
- Estimación ao completar (EAC) = Esforzo restante - Esforzo real realizado ata a data 
- Varianza de esforzo proxectado = Esforzo planificado - EAC

PSA mostra unha proxección da varianza de esforzo na tarefa. Se a EAC supón un esforzo superior ao previsto, proxéctase que a tarefa levará máis tempo do que estaba previsto inicialmente. Polo tanto, está atrasada. Se a EAC supón un esforzo inferior ao previsto, proxéctase que a tarefa levará menos tempo do que estaba previsto inicialmente. Polo tanto, está adiantada.

## <a name="re-projecting-effort"></a>Proxectar de novo o esforzo

É frecuente que un xestor de proxectos revise as estimacións orixinais dunha tarefa. As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto. Non obstante, non recomendamos que os xestores de proxectos modifiquen os números da liña base, porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.

Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:

- Anular o ETC predefinido cunha nova estimación do esforzo restante real da tarefa. 
- Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.

Cada un destes enfoques provoca un novo cálculo do ETC, EAC e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa. Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Nova proxección do esforzo en tarefas resumo

Pódese proxectar de novo o esforzo en tarefas resumo ou en tarefas contedor. Independentemente de que o usuario volva proxectar empregando o esforzo restante ou a porcentaxe de progreso nas tarefas resumo, comeza o seguinte conxunto de cálculos:

- Calcúlanse o EAC, ETC e a porcentaxe progreso da tarefa.
- O nova EAC distribúese nas tarefas dependentes na mesma proporción que o EAC orixinal estaba na tarefa.
- Calcúlase o novo EAC en cada unha das tarefas individuais ata as tarefas do nó folla. 
- As tarefas dependentes afectadas ata os nós folla teñen a súa ETC e a porcentaxe de progreso calculada de novo en función do valor de EAC. Isto da lugar a unha nova proxección para a varianza de esforzo da tarefa. 
- Calcúlanse de novo os EAC das tarefas resumo ata o nó raíz.

### <a name="cost-tracking-view"></a>Vista de rastrexo de custo 

A vista **Seguimento de custos** compara o custo real que se gastou nunha tarefa co custo planificado dunha tarefa. 

> [!NOTE]
> Esta vista mostra só os custos laborais e non inclúe os custos das estimacións de gastos. 

PSA usa as seguintes fórmulas para calcular as métricas de seguimento:

- Porcentaxe do custo consumido = Custo real gastado ata a data ÷ Custo planificado para a tarefa
- Custo para completar (CTC) = Custo planificado - Custo real gastado ata a data
- EAC = CTC + Custo real gastado ata a data
- Varianza do custo proxectado = Custo planificado - EAC

A proxección da varianza de custo móstrase na tarefa. Se o EAC supón un esforzo superior ao custo previsto, proxéctase que a tarefa custará máis do que estaba previsto inicialmente. Polo tanto, tende a superar o orzamento. Se o EAC supón un esforzo inferior ao custo previsto, proxéctase que a tarefa custará menos do que estaba previsto inicialmente. Polo tanto, tende a estar por debaixo do orzamento.

## <a name="project-managers-re-projection-of-cost"></a>Nova proxección de custos do xestor de proxectos

Cando se proxecta de novo o esforzo, todos os CTC, EAC, porcentaxe de custo consumido e varianza de custo proxectado calcúlanse de novo na vista **Rastrexo de custos**.

## <a name="project-status-summary"></a>Resumo do estado do proxecto

Os datos de rastrexo nas vistas **Rastrexo do esforzo** e **Rastrexo de custos** mostran o progreso e o consumo de custos aos niveis de nó raíz do proxecto, tarefas de resumo e tarefas de nó folla. A sección **Estado** de páxina **Entidade do proxecto** mostra un resumo do estado a nivel de proxecto.

## <a name="status-summary-fields"></a>Campos resumo do estado

O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto. Emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente. O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado. O campo **Estado actualizado o** non se pode editar e o valor é unha marca de tempo que indica cando se actualizou o estado por última vez.

Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da data de rastrexo. Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, pode axustar estes campos a **Adiantado**. Cando o calendario e a varianza de custos para o nó raíz son negativos, pode configuralos en **Atrasado**.
