---
title: Rastrexo de custos de proxecto
description: Este tema ofrece información sobre como as Project Operations rastrexa o progreso fronte ao custo laboral e ao gasto nun proxecto.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cb76987cf15a14639f34cd3b67c1296a020b2e3e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996519"
---
# <a name="labor-cost-tracking-on-projects"></a>Rastrexo do custo laboral en proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations rastrexa as estimacións de man de obra e do gasto coa granularidade máis baixa requirida no plan do proxecto. A estimación financeira do custo laboral baséase no esforzo planificado e nos recursos xenéricos ou nomeados que se atribúen a cada tarefa de nó folla no plan do proxecto. Cando comeza o proxecto e o persoal comeza a informar do tempo das distintas tarefas do proxecto, resúmese o gasto real en man de obra, o que inicia un cálculo das proxeccións.

## <a name="labor-cost-tracking-view"></a>Vista de rastrexo de custo laboral

Na páxina **Proxectos**, no separador **Rastrexo**, pode seleccionar **Rastrexo** > **Custo** para abrir a vista **Rastrexo de custos** e ver o progreso do gasto laboral en cada tarefa no plan do proxecto. Esta vista tamén compara o custo laboral real gastado nunha tarefa co custo laboral planificado da tarefa. Project Operations utiliza as seguintes fórmulas para calcular as métricas do custo laboral:

- **Custo previsto**: Custo estimado de todas as atribucións de recursos en cada tarefa de nó folla
- **Custo real**: Suma de todos os datos reais de custo polo tempo rexistrado na tarefa
- **Porcentaxe de consumo de custos**: Custo real ÷ Estimación do custo ao finalizar
- **Custo restante**: Estimación do custo ao finalizar – Custo real
- **Custo ao finalizar**: Custo restante + Custo real
- **Variación de custo**: Custo planificado – Estimación de custo ao finalizar

Cada tarefa mostra unha proxección da variación de custo na tarefa. Se a estimación de custo ao finalizar é superior ao custo previsto, proxéctase que a tarefa superará o orzamento. Se a estimación de custo ao finalizar é inferior ao custo previsto, proxéctase que a tarefa finalizará por debaixo do orzamento.

>[!NOTE]
> Project Operations só mostra custos laborais na páxina **Proxecto** no separador **Rastrexo**. Aínda que os materiais e gastos poden ser estimados e rastrexados para o consumo, estes custos non están incluídos nos custos mostrados no separador **Rastrexo**. Este separador está deseñado para funcionar só para reproxectar custos laborais mediante a reproxección de esforzos.
Todos os importes de custos mostrados convértense na moeda de custo do proxecto a partir da moeda de custo do proxecto utilizada para determinar a taxa de custo. A moeda de custo do proxecto é a moeda da unidade contratante do proxecto. Os valores de custo estimados para o tempo que se amosan no separador **Estimacións** na páxina **Proxecto** pode non sumar o custo planificado no separador **Rastrexo**. O motivo desta discrepancia so as diferenzas na forma en que se resume o custo estimado na grade **Estimacións** e como se calcula o custo planificado na grade **Rastrexo**. 
>
> - O separador **Estimacións** calcula o custo estimado empregando a mesma moeda da taxa de custo da lista de prezos. A seguir, o custo estimado na moeda da lista de prezos convértese no custo estimado na moeda de custos do proxecto. O custo estimado na moeda do proxecto móstrase redondeada a 2 decimais. Non se aplica en ningún momento desta conversión a precisión de moeda. 
> - No separador **Rastrexo**, o cálculo do custo previsto segue unha orde de cálculo lixeiramente diferente que implica a precisión da moeda en dúas etapas: 
   ><ol>
   ><li>O importe do custo estimado na moeda da lista de prezos convértese na moeda base (conversión 1).</li>
   ><li>O importe do custo estimado na moeda base convértese na moeda de custo do proxecto (conversión 2). </li>
   ></ol>
   >A precisión da moeda aplícase nos dous pasos para obter un custo planificado (no separador **Rastrexo**) que se desvía lixeiramente do custo estimado (na vista **Tempo - fases** no separador **Estimacións**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Reproxección de custos en tarefas de nó folla

Os custos laborais nunha tarefa de nó folla non se poden reproxectar directamente no separador **Rastrexo** na **Páxina do proxecto**. Non obstante, pode usar a vista **Rastrexo do esforzo** para proxectar o esforzo restante nunha tarefa. Isto provoca un novo cálculo do custo restante na tarefa. A continuación descríbese como funciona isto.

1. Un xestor de proxectos pode reproxectar esforzos nas tarefas actualizando o valor predefinido no campo **Esforzo restante** cunha nova estimación do esforzo restante na tarefa. A reproxección provoca un novo cálculo da estimación do esforzo da tarefa ao finalizar (EAC), a porcentaxe de progreso e a variación do esforzo proxectada nunha tarefa. Tamén se calculan de novo o EAC, a estimación para finalizar e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.
2. Baseándose no novo valor do esforzo restante na tarefa, o sistema calcula o custo restante na vista **Rastrexo de custos**. Para calcular o custo restante en función do esforzo restante, o sistema primeiro calcula o custo medio dunha hora de esforzo na tarefa como custo planificado ou esforzo planificado. O custo planificado é a suma do custo de todas as atribucións de recursos na tarefa. O custo medio por hora úsase para calcular o custo restante do esforzo restante proxectado na tarefa.
3. O custo ao finalizar e a porcentaxe de consumo de custos na tarefa de nó folla calcúlanse de novo.
4. O valor de custo ao finalizar das tarefas resumo ata o nó raíz calcúlase de novo.

## <a name="reprojecting-costs-on-summary-tasks"></a>Reproxección de custos en tarefas resumo

Pode reproxectar custos laborais en tarefas resumo ou tarefas contedor. Non obstante, non pode reproxectar directamente o custo laboral nunha tarefa resumo do proxecto no separador **Rastrexo** na páxina **Proxecto**. De modo semellante ás tarefas de nó folla, o resumo de reproxección e as tarefas do contedor pódense facer usando a vista **Rastrexo do esforzo**. Nesta vista, pode reproxectar o esforzo restante nunha tarefa resumo provocando un novo cálculo do custo restante na tarefa resumo. A continuación descríbese como funciona isto.

1. Un xestor de proxectos pode reproxectar o esforzo nas tarefas resumo actualizando o valor predefinido do esforzo restante cunha nova estimación na tarefa. Esta actualización provoca un novo cálculo da estimación da tarefa resumo ao finalizar (EAC), a porcentaxe de progreso e a variación do esforzo proxectada nunha tarefa. Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.
2. Baseándose no novo valor do esforzo restante na tarefa resumo, o sistema calcula o custo restante na vista **Rastrexo de custos**. Para calcular o custo restante en función do esforzo restante, o sistema primeiro calcula o custo medio dunha hora de esforzo na tarefa resumo como custo planificado ou esforzo planificado. O custo medio por hora úsase para calcular o custo do esforzo restante proxectado de novo na tarefa resumo.
3. O custo ao finalizar e a porcentaxe de consumo de custos na tarefa resumo calcúlanse de novo.
4. O novo custo ao finalizar distribúese nas tarefas dependentes na mesma proporción que o custo planificado orixinal estaba na tarefa.
5. Calcúlase o novo valor de custo ao finalizar en cada unha das tarefas individuais ata as tarefas do nó folla. En base a este valor, calcularanse o custo restante e a porcentaxe de consumo de custos de novo das tarefas secundarias afectadas ata os nós folla en función do valor de custo ao finalizar. Este valor da lugar a unha nova proxección para a varianza de custo da tarefa. 


O campo **Rendemento do custo** campo pódese establecer a partir dos datos de rastrexo. Cando a variación de custo para o nodo raíz na vista **Rastrexo de custos** é negativa, pode establecer este campo en **Inferior ao orzamento**. Cando a varianza de custo para o nó raíz é positiva, pode establecer o valor en **Superior ao orzamento**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
