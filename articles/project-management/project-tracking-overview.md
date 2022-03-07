---
title: Visión xeral do rastrexo de proxectos
description: Este tema ofrece información sobre como rastrexar o progreso do proxecto e o consumo de custos.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075983"
---
# <a name="project-tracking-overview"></a>Visión xeral do rastrexo de proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A necesidade de rastrexar o progreso cunha programación varía segundo o sector. Algúns sectores rastrexan a un nivel granular, mentres que outros sectores rastrexan a un nivel máis alto. Este tema mostra como programar para cumprir os requisitos da súa organización.

## <a name="effort-tracking-view"></a>Visualización de rastrexamento do esforzo

A vista **Rastrexo do esforzo** rastrexa o progreso das tarefas de programación comparando as horas de esforzo real dedicadas a unha tarefa coas horas de esforzo planificadas da tarefa. Dynamics 365 Project Operations usa as seguintes fórmulas para calcular as métricas de rastrexo:

- **Porcentaxe de progreso**: Esforzo real realizado ata a data ÷ Estimación ao completar (EAC) 
- **Estimación para completar (ETC)**: Esforzo previsto - Esforzo real realizado ata a data 
- **EAC**: Esforzo restante + Esforzo real realizado ata a data 
- **Varianza de esforzo proxectado**: Esforzo planificado - EAC

Project Operations mostra unha proxección da varianza de esforzo na tarefa. Se a EAC supón un esforzo superior ao previsto, proxéctase que a tarefa levará máis tempo do que estaba previsto inicialmente e está atrasada. Se a EAC supón un esforzo inferior ao previsto, proxéctase que a tarefa levará menos tempo do que estaba previsto inicialmente e está adiantada.

## <a name="reprojecting-effort"></a>Proxectar de novo o esforzo

Os xestores de proxectos revisan con frecuencia as estimacións orixinais dunha tarefa. As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto. Non obstante, non recomendamos que os xestores de proxectos cambien os números da liña base. Isto é porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.

Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:

- Anular o ETC predefinido cunha nova estimación do esforzo restante real da tarefa. 
- Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.

Cada enfoque provoca un novo cálculo do ETC, EAC e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa. Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nova proxección do esforzo en tarefas resumo

Pódese proxectar de novo o esforzo en tarefas resumo ou en tarefas contedor. Independentemente de que o usuario volva proxectar empregando o esforzo restante ou a porcentaxe de progreso nas tarefas resumo, comeza o seguinte conxunto de cálculos:

- Calcúlanse o EAC, ETC e a porcentaxe progreso da tarefa.
- O nova EAC distribúese nas tarefas dependentes na mesma proporción que o EAC orixinal estaba na tarefa.
- Calcúlase o novo EAC en cada unha das tarefas individuais ata as tarefas do nó folla. 
- As tarefas dependentes afectadas ata os nós folla teñen a súa ETC e a porcentaxe de progreso calculada de novo en función do valor de EAC. Isto da lugar a unha nova proxección para a varianza de esforzo da tarefa. 
- Calcúlanse de novo os EAC das tarefas resumo ata o nó raíz.

### <a name="cost-tracking-view"></a>Vista de rastrexo de custo 

A vista **Seguimento de custos** compara o custo real que se gastou nunha tarefa co custo planificado dunha tarefa. 

> [!NOTE]
> Esta vista mostra só os custos laborais e non inclúe os custos das estimacións de gastos. Project Operations usa as seguintes fórmulas para calcular as métricas de rastrexo:

- **Porcentaxe do custo consumido**: Custo real gastado ata a data ÷ Custo estimado ao completar
- **Custo para completar (CTC)**: Custo planificado - Custo real gastado ata a data
- **EAC**: custo restante + custo real gastado ata a data
- **Varianza do custo proxectado**: Custo planificado - EAC

A proxección da varianza de custo móstrase na tarefa. Se o EAC supón un esforzo superior ao custo previsto, proxéctase que a tarefa custará máis do que estaba previsto inicialmente. Polo tanto, tende a superar o orzamento. Se o EAC supón un esforzo inferior ao custo previsto, proxéctase que a tarefa custará menos do que estaba previsto inicialmente. Polo tanto, tende a estar por debaixo do orzamento.

## <a name="project-managers-reprojection-of-cost"></a>Nova proxección de custos do xestor de proxectos

Cando se proxecta de novo o esforzo, todos os CTC, EAC, porcentaxe de custo consumido e varianza de custo proxectado calcúlanse de novo na vista **Rastrexo de custos**.

## <a name="project-status-summary"></a>Resumo do estado do proxecto

Os datos de rastrexo nas vistas **Rastrexo do esforzo** e **Rastrexo de custos** mostran o progreso e o consumo de custos aos niveis de nó raíz do proxecto, tarefas de resumo e tarefas de nó folla. A sección **Estado** de páxina **Entidade do proxecto** mostra un resumo do estado a nivel de proxecto.

## <a name="status-summary-fields"></a>Campos resumo do estado

O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto. Emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente. O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado. O campo **Estado actualizado o** non se pode editar e o valor é unha marca de tempo que indica cando se actualizou o estado por última vez.

Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da data de rastrexo. Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, pode axustar estes campos a **Adiantado**. Cando o calendario e a varianza de custos para o nó raíz son negativos, pode configuralos en **Atrasado**.
