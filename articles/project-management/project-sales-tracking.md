---
title: Rastrexo de vendas do proxecto
description: Este tema ofrece información sobre como as Project Operations rastrexa o progreso fronte aos ingresos laborais nun proxecto.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711045"
---
# <a name="project-sales-tracking"></a>Rastrexo de vendas do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations rastrexa as estimacións de man de obra e dos ingresos coa granularidade máis baixa requirida no plan do proxecto. A estimación financeira dos ingresos laborais baséase no esforzo planificado e nos recursos xenéricos ou nomeados que se atribúen a cada tarefa de nó folla no plan do proxecto. Cando comeza o proxecto e o persoal comeza a informar do tempo das distintas tarefas do proxecto, resúmese os ingresos reais en man de obra, o que inicia un cálculo das proxeccións.

## <a name="labor-revenue-tracking-view"></a>Vista de rastrexo de ingresos laborais

Na páxina **Proxectos**, no separador **Rastrexo**, pode seleccionar **Rastrexo** > **Custo** para abrir a vista **Rastrexo de custos**. Ou pode seleccionar **Uso** > **Taxa de facturación** para abrir a vista **Rastrexo de ingresos**, que mostra o progreso dos ingresos laborais en cada tarefa no plan do proxecto. Esta vista tamén compara os ingresos laborais reais gastado nunha tarefa cos ingresos laborais planificados da tarefa. Project Operations utiliza as seguintes fórmulas para calcular as métricas dos ingresos laborais:

- **Ingresos previstos**: Valores estimados de vendas de todas as atribucións de recursos en cada tarefa de nó folla
- **Ingresos reais**: Suma de todas as vendas sen facturar polo tempo rexistrado na tarefa
- **% se ingresos facturables**: Ingresos reais ÷ Estimación de ingresos ao finalizar
- **Ingresos restante**: Estimación de ingresos ao finalizar – Ingresos reais
- **Ingresos estimados ao finalizar**: Ingresos restantes + Ingresos reais
- **Variación de ingresos**: Ingresos planificados – Ingresos estimados ao finalizar


> [!NOTE]
> Project Operations só mostra ingresos laborais na páxina **Proxecto** no separador **Rastrexo**. Aínda que os materiais e gastos poden ser estimados e rastrexados para o consumo, estes ingresos non están incluídos nos ingresos mostrados no separador **Rastrexo**. Este separador está deseñado para funcionar só para reproxectar ingresos laborais mediante a reproxección de esforzos.  
> Todos os importes de ingresos mostrados convértense á moeda de custo do proxecto. A moeda de custo do proxecto é a moeda da unidade contratante do proxecto. Para proxectos de prezo fixo, os números de ingresos na vista **Rastrexo dos ingresos laborais** non é relevante porque os datos reais de vendas non facturadas non se rexistran coa aprobación do tempo.
> Os valores de vendas estimados para o tempo que se amosan no separador **Estimación** do proxecto pode non sumar o valor de ingresos previsto no separador **Rastrexo**. A orixe desta discrepancia débese a dúas posibles razóns:
><ol>
   ><li> O separador <b>Estimacións</b> mostra os ingresos estimados na moeda de vendas, mentres que o separador <b>Rastre</b> mostra os ingresos planificados convertidos á moeda de custo. </li>
   ><li> Cando as vendas estimadas se converten á moeda do contrato como se mostra no separador <b>Estimacións</b>, a conversión implica pasos que poden provocar certa perda de precisión: </li>
><ol>
><li> O importe das vendas estimado na moeda do contrato convértese primeiro na moeda base do proxecto (conversión 1).</li>
><li> O importe das vendas estimado na moeda base convértese na moeda de custo do proxecto (conversión 2). </li>
></ol>
></ol>
> A precisión da moeda aplícase nos dous pasos, o que resulta nunha desviación dos ingresos previstos na moeda do proxecto a partir das vendas planificadas na moeda do contrato.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Reproxección de ingresos en tarefas de nó folla

Os ingresos laborais nunha tarefa de nó folla non se poden reproxectar directamente no separador **Rastrexo** na páxina **Proxecto**. Non obstante, pode usar a vista **Rastrexo do esforzo** para proxectar o esforzo restante nunha tarefa. Isto provoca un novo cálculo dos ingresos restantes na tarefa. A continuación descríbese como funciona isto.

1. Un xestor de proxectos pode reproxectar esforzos nas tarefas actualizando o valor predefinido no campo **Esforzo restante** cunha nova estimación do esforzo restante na tarefa. A reproxección provoca un novo cálculo da estimación do esforzo da tarefa ao finalizar (EAC), a porcentaxe de progreso e a variación do esforzo proxectada nunha tarefa. Tamén se calculan de novo o EAC, a estimación para finalizar e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.
2. Baseándose no novo valor do esforzo restante na tarefa, o sistema calcula os ingresos restantes na vista **Rastrexo de ingresos**. Para calcular os ingresos restante en función do esforzo restante, o sistema primeiro calcula os ingresos medios dunha hora de esforzo na tarefa resumo como ingresos planificados ou esforzo planificado. Os ingresos planificados é a suma dos ingresos de todas as atribucións de recursos na tarefa. Os ingresos medios por hora úsanse para calcular os ingresos restantes do esforzo restante proxectado na tarefa.
3. Os ingresos restantes ao finalizar e a porcentaxe de consumo de ingresos na tarefa de nó folla calcúlanse de novo.
4. O valor dos ingresos ao finalizar das tarefas resumo ata o nó raíz calcúlase de novo.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Reproxección de ingresos en tarefas resumo

Pode reproxectar ingresos laborais en tarefas resumo ou tarefas contedor. Non obstante, non pode reproxectar directamente os ingresos laborais nunha tarefa resumo do proxecto no separador **Rastrexo** na páxina **Proxecto**. De modo semellante ás tarefas de nó folla, o resumo de reproxección e as tarefas do contedor pódense facer usando a vista **Rastrexo do esforzo**. Nesta vista, pode reproxectar o esforzo restante nunha tarefa resumo provocando un novo cálculo dos ingresos restantes na tarefa resumo. A continuación descríbese como funciona isto.

1. Un xestor de proxectos pode reproxectar esforzos nas tarefas actualizando o valor predefinido no campo **Esforzo restante** cunha nova estimación do **Esforzo restante** na tarefa. A reproxección provoca un novo cálculo da estimación da tarefa ao finalizar (EAC), a porcentaxe de progreso e a variación do esforzo proxectada nunha tarefa. Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.
2. Baseándose no novo valor do campo **Esforzo restante** na tarefa, o sistema calcula os ingresos restantes na vista **Rastrexo de ingresos**. Para calcular os ingresos restante en función do esforzo restante, o sistema primeiro calcula os ingresos medios dunha hora de esforzo na tarefa resumo como ingresos planificados ou esforzo planificado. Os ingresos planificados é a suma dos ingresos de todas as atribucións de recursos na tarefa. Os ingresos medios por hora úsanse para calcular os ingresos do esforzo restante proxectado na tarefa.
3. Os ingresos restantes ao finalizar e as porcentaxes de consumo de ingresos na tarefa resumo calcúlanse de novo.
4. O novo valor dos ingresos estimados ao finalizar distribúese nas tarefas dependentes na mesma proporción que os ingresos planificados orixinais estaba na tarefa.
5. Calcúlanse os novos ingresos estimados ao finalizar en cada unha das tarefas individuais ata as tarefas do nó folla. En base a este valor, calcularanse os ingresos restantes e a porcentaxe de consumo de ingresos de novo das tarefas secundarias afectadas ata os nós folla en función do valor dos ingresos ao finalizar. Isto da lugar a unha nova proxección para a varianza de ingresos da tarefa. 
6. O valor dos ingresos ao finalizar das tarefas resumo ata o nó raíz calcúlase de novo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

