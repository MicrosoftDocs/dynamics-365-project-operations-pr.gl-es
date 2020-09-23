---
title: Visión xeral de estruturas de subdivisión do traballo
description: Unha estrutura de subdivisión do traballo (WBS) é unha descrición do traballo que se realizará para un proxecto. É unha xerarquía de tarefas que representa a comprensión do equipo do proxecto sobre a composición do traballo e sobre o tamaño, custo e duración de cada compoñente ou tarefa.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 954965ee947cbce9d1ae686d281a5fed25a78245
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751397"
---
# <a name="work-breakdown-structures-overview"></a>Visión xeral de estruturas de subdivisión do traballo

[!include [banner](../includes/banner.md)]

Unha estrutura de subdivisión do traballo (WBS) é unha descrición do traballo que se realizará para un proxecto. É unha xerarquía de tarefas que representa a comprensión do equipo do proxecto sobre a composición do traballo e sobre o tamaño, custo e duración de cada compoñente ou tarefa. Unha WBS ten tres finalidades principais:

-   Describir a subdivisión ou composición do traballo en tarefas.
-   Programar o traballo do proxecto
-   Estimar o custo de cada tarefa.

O grao de detalle dunha WBS depende do nivel de precisión que se require nas estimacións e do nivel de seguimento que se require con respecto a esas estimacións. Os proxectos que teñan unha tolerancia moi baixa ás desviacións no programa ou no custo normalmente requiren unha WBS máis detallada e un seguimento dilixente do progreso do traballo e o custo con respecto á WBS. Este tipo de proxectos son frecuentes nos sectores de construción e enxeñaría. 

Pola contra, os proxectos en sectores como medios de comunicación e publicidade, software e infraestruturas de TI adoitan ser únicos e a produtividade está relacionada coa experiencia e competencia da persoa que realiza a tarefa. Polo tanto, estes sectores utilizan unha WBS para obter unha aproximación do tamaño dun proxecto, non para rastrexar o progreso dese proxecto en detalle. 

Construír unha WBS é un proceso intensivo que se realiza normalmente durante un longo período e que require colaboración e información dunha gran variedade de persoas. Este tema describe como pode usar as melloras da WBS para cumprir os seus requisitos de estimacións e rastrexo.

## <a name="prerequisites-for-creating-a-wbs"></a>Requisitos previos para a creación dunha WBS
Para crear unha WBS, ten que ser capaz de crear un programa de traballo e estimar o custo do traballo.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Requisitos previos para a creación dun programa de traballo

Para utilizar as capacidades de programación completas das funcionalidades de WBS, complete a seguinte configuración:

1.  Configure un calendario predefinido e un calendario do proxecto:
    1.  Prema **Xestión de proxectos e contabilidade** &gt; **Configuración** &gt; **Parámetros de xestión de proxectos e contabilidade** &gt; **Programación**. No campo **Calendario de traballo predefinido**, especifique un calendario predefinido. Este será o calendario de traballo predefinido para calquera proxecto novo que se cree.
    2.  Pode cambiar o calendario predefinido para un proxecto específico. Prema na páxina de detalles do proxecto e, a seguir, no separador rápido **Equipo do proxecto e programación**, actualice o campo **Calendario de programación** seleccionando outro calendario.

2.  Configure os días e horas de traballo estándar. O calendario que estableza como calendario de traballo para o seu proxecto utilizarase na WBS para determinar a seguinte información:

-   Días laborables e festivos
-   O número de horas de traballo nun día

Para configurar os días e horas de traballo dun calendario ou crear un novo calendario, prema **Administración da organización** &gt; **Común** &gt; **Calendarios**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Requisitos previos para estimar o custo do traballo

Para empregar as capacidades completas de estimación de custos da WBS, debe configurar os custos e prezos de venda dos traballadores, categorías de man de obra, gastos e tarifas e artigos.

-   Para configurar o custo e o prezo de venda das categorías de man de obra, gastos e tarifas, prema **Xestión de proxectos e contabilidade** &gt; **Configurar** &gt; **Prezos**.
-   Para configurar o custo e o prezo de venda dos artigos, use a páxina **Acordos comerciais** para cada artigo da páxina de lista **Produtos lanzados** en xestión de información de produtos.

## <a name="creating-a-wbs"></a>Creación dunha WBS
A creación dunha WBS implica tres actividades:

1.  **Descomposición do traballo** - Crear unha subdivisión do traballo en anacos ou tarefas manexables.
2.  **Programa de traballo** - Estimar o tempo necesario para completar unha tarefa, establecer interdependencias de tarefas e seleccionar as datas de inicio e finalización das tarefas.
3.  **Estimación de custos** - Estimar os custos de cada tarefa.

As seguintes seccións analizan como as capacidades de WBS poden axudar con cada unha destas actividades.

### <a name="work-decomposition"></a>Descomposición do traballo

A creación dunha descomposición ou subdivisión do traballo adoita ser o primeiro paso no proceso de creación dunha WBS. A funcionalidade de WBS admite as seguintes construcións básicas para a descomposición ou subdivisión do traballo. 

**Tarefa raíz do proxecto** A tarefa raíz do proxecto é a tarefa resumo de nivel superior dun proxecto. Todas as outras tarefas de proxecto créanse por debaixo dela. O nome da tarefa raíz é sempre o nome do proxecto. O esforzo, as datas e a duración do nó raíz resumen os valores das tarefas debaixo da tarefa raíz. Non se poden modificar as propiedades do nó raíz nin eliminalo.

**Resumo ou tarefas de contedores** Unha tarefa resumo é unha tarefa que ten subtarefas ou tarefas dependentes debaixo dela. Unha tarefa de resumo non ten un esforzo de traballo ou custo propio. Pola contra, o esforzo de traballo e o custo dunha tarefa resumo son a suma do esforzo de traballo e o custo das súas tarefas dependentes. A primeira data de inicio das tarefas dependentes utilízase como data de inicio da tarefa resumo e a última data de finalización las tarefas dependentes utilízase como a data final. Pode modificar o nome dunha tarefa resumo, pero non pode modificar as propiedades de programación de esforzo, datas e duración. Se elimina unha tarefa resumo, tamén eliminará as súa tarefas dependentes. 

**Tarefas nó folla** Unha tarefa nó folla representa o paquete de traballo máis granular do proxecto. Un nó folla ten un esforzo estimado, varios recursos planificados, unha data de inicio e unha data de fin planificadas e unha duración. 

Pode completar as seguintes operacións de xerarquía para permitir a creación dunha xerarquía de traballo ou descomposición para un proxecto. 

**Nova tarefa** Calquera nova tarefa que cree engádese automaticamente baixo o nó raíz e un número de WBS asignase automaticamente á tarefa. O número de WBS representa o nivel da tarefa na xerarquía. Para tarefas do primeiro nivel baixo a tarefa raíz do proxecto, úsase un esquema de numeración de 1, 2, 3, etc. Para as tarefas que están baixo o primeiro nivel, úsase un esquema de numeración de 1.1, 1.2, 1.3, etc. Para cada nivel engadido baixo un nivel anterior, engádese unha nova serie de números con puntos. 

Actualmente, non se pode personalizar a numeración de WBS. 

**Tarefa de sangría** Cando se aplica unha sangría a unha tarefa, convértese en dependente da tarefa que a precede. O número de WBS da nova tarefa secundaria calcúlase de novo automaticamente en función do número WBS da súa nova tarefa principal. A tarefa principal agora é unha tarefa resumo ou contedor e, polo tanto, convértese nun resumo das súas tarefas dependentes. 

> [!NOTE] 
> Cando aplica unha sangría ás tarefas baixo unha tarefa que era un nó folla antes da operación de aplicación de sangría, a tarefa resumo recentemente creada perde as súas propias datas, esforzo e número de recursos. Agora usa un resumo dos valores das súas novas tarefas dependentes. 

**Eliminar sangría de tarefa** Cando se elimina a sangría dunha tarefa, xa non é unha tarefa dependente da súa tarefa principal. O número WBS desta tarefa recálculase automaticamente para reflectir o novo nivel da tarefa na xerarquía. O esforzo, custo e datas da tarefa principal anterior da tarefa calcúlanse de novo para excluír esa tarefa. 

**Mover cara arriba e abaixo** Ao premer **Mover cara arriba** e **Mover cara abaixo**, cambia a posición dunha tarefa dentro da xerarquía das súas tarefas principais. A posición dunha tarefa non afecta ao esforzo, o custo, as datas ou a duración da tarefa. Non obstante, o número WBS da tarefa recálculase automaticamente para reflectir a nova posición da tarefa.

### <a name="schedule-estimation"></a>Estimación de programación

A estimación da programación adoita ser o segundo paso para crear unha WBS. Como mellor práctica, debería completar a estimación da programación despois de crear as tarefas. A páxina **Estrutura de subdivisión do traballo** en Finanzas ten dúas seccións. O panel superior está destinado á estimación de programación e o panel inferior inclúe un separador de **Custos e ingresos estimados** que pode empregar para a estimación de custos. 
**Dependencias de tarefas** Nunha WBS, pode crear unha relación predecesora entre tarefas. Cando atribúe tarefas predecesoras a unha tarefa, esa tarefa só pode iniciarse despois de que conclúan todas as súas tarefas predecesoras. A data de inicio planificada da tarefa establécese automaticamente na data máis recente de todas as súas predecesoras. 

**Programación de tarefas** Os seguintes factores determinan a programación das tarefas do nó folla:

-   Predecesores
-   Esforzo
-   O número de recursos
-   Datas de inicio e de fin

A data de inicio dunha tarefa de nó folla que non teña predecesores é automaticamente a data de inicio da programación do proxecto. A duración dunha tarefa de nó folla calcúlase sempre como o número de días laborables entre as datas de inicio e fin. 

*<strong><em>Normas de programación</em></strong>* Cando a asistencia de programación automática está activada, as seguintes regras aplícanse á programación de tarefas para tarefas de nó folla:

-   As datas de inicio e fin dunha tarefa sempre deben ser días laborables segundo o calendario de programación do proxecto.
-   A data de inicio dunha tarefa que teña predecesores é automaticamente a última data de fin das súas predecesoras.
-   O esforzo para unha tarefa calcúlase automaticamente do seguinte xeito:

Número de persoas × Duración × Número de horas nun día laborable estándar do calendario de proxecto. 

Nalgúns casos, é posible que desexe afastarse destas regras. Pode desactivar a programación automática para evitar que Finanzas configure ou corrixa automaticamente calquera propiedade das tarefas nó folla. Cando introduce información para unha tarefa que causa unha violación de calquera regra de programación, móstrase unha icona de erro de programación para a tarefa. Se non desexa que se mostren erros de programación, prema **Amósanse os erros de programación** para desactivar a función. 

> [!NOTE] 
> Os valores dunha tarefa resumo ou contedor seguen calculándose como a suma dos valores das tarefas dependentes, independentemente de que a asistencia de programación automática estea activada ou desactivada. 

**Corrección de erros de programación** Cando a asistencia de programación automática está activada, é probable que non se produzan erros de programación. Non obstante, se desactiva a asistencia de programación automática e volve a activala máis tarde, poden aparecer iconas de erro de programación na WBS. 

**Corrección de erros de programación por tarefa** Cando fai dobre clic na icona de erro de programación para unha tarefa específica, unha caixa de diálogo amosa todos os erros de programación desa tarefa. Pode decidir que erros de programación corrixir para a tarefa. 

**Corrección de todos os erros de programación** Se desexa que Finanzas corrixa todos os erros de programación na WBS, no panel de acción, prema **Corrixir todas as discrepancias de programación**. 

> [!NOTE] 
> Esta funcionalidade pode causar modificacións significativas na WBS. Os erros corríxense na seguinte orde:

1.  Modifícase o esforzo estimado en todas as tarefas para que sexa igual á capacidade definida no calendario do proxecto.
2.  A data de inicio de cada tarefa modifícase para que a tarefa comece despois de completadas todas as tarefas predecesoras.
3.  A data de inicio de cada tarefa modifícase para eliminar as lagoas nas datas de inicio das tarefas predecesoras.

### <a name="cost-estimation"></a>Estimación de custos

Como se mencionou anteriormente neste documento, vostede introduce a estimación de custos para cada tarefa nó folla usando o separador **Custos e ingresos estimados** no panel inferior da páxina **Estrutura de subdivisión do traballo**. 

> [!NOTE] 
> Non pode modificar a estimación de custos para unha tarefa resumo ou contedor. A estimación de custos para unha tarefa resumo é igual á suma da estimación de custos das súas tarefas nó folla. O custo total estimado para cada tarefa calcúlase como a suma dos custos estimados para os seguintes tipos de transacción:

-   Traballo
-   Artigo ou material
-   Gastos

O tipo de transacción **Tarifa** úsase para estimar os ingresos baseados en tarifas. Este tipo de transacción non ten un compoñente de custo e, polo tanto, non se considera cando se estiman os custos. 

O tipo de transacción **En conta** úsase para rexistrar o valor de venda contratado nun tipo de proxecto de valor fixo. Este tipo de transacción tampouco se ten en conta cando se estiman os custos. 

Cando estima os custos de man de obra, material e gastos para cada tarefa, debe asignar unha categoría de proxecto ao custo estimado. 

**Estimación dos custos laborais** Para cada tarefa nó folla, vostede atribúe un esforzo e traballo en horas e unha categoría predefinida. Polo tanto, cando configura un programa para unha tarefa, a estimación do custo laboral para esa tarefa engádese automaticamente na categoría predefinida para man de obra. Esta estimación de custos móstrase no separador **Custos e ingresos estimados** na grade **Detalles da liña** para esa tarefa. Se precisa máis estimacións de custo laboral, pode engadilas neste separador. Se aumenta ou diminúe as horas na estimación do custo laboral, o calendario da tarefa calcúlase de novo automaticamente. 

**Estimación de gastos e custos de material** O separador **Custos e ingresos estimados** tamén permite calcular os gastos e os materiais dunha tarefa, se precisa estimacións. 

O custo e o prezo de venda para cada liña de estimación de man de obra ou gasto baséanse na configuración que se define para cada categoría nas táboas de prezos de **Xestión de proxectos e contabilidade** &gt; **Configurar** &gt; **Prezos**. Para os artigos, o custo e o prezo de venda engádense por defecto desde o artigo ou os acordos comerciais para cada artigo da páxina de lista **Produtos lanzados** en xestión de información de produtos.

## <a name="tracking-progress-on-the-wbs"></a>Rastrexo do progreso na WBS
Algúns sectores rastrexan o progreso dun proxecto respecto a unha WBS a un nivel moi granular, mentres que outros seguen o progreso a un nivel máis alto da WBS. Esta sección describe como pode usar o rastrexo de WBS para os requisitos do seu proxecto. 

Finanzas ten tres vistas para a WBS dun proxecto: a vista de planificación, a vista de rastrexo do esforzo e a vista de rastrexo de custos.

### <a name="planning-view"></a>Vista de planificación

A vista de planificación mostra a estimación planificada ou de base da información sobre programación e custos. Aínda que non hai funcionalidades para rastrexar a versión e a liña de base da WBS dun proxecto, os valores desta vista están pensados para representar a versión de liña de base. As seccións de estimación de programación e estimación de custos deste tema describen esta vista e como se usa para crear unha WBS.

### <a name="effort-tracking-view"></a>Visualización de rastrexamento do esforzo

A vista de rastrexo do esforzo mostra o rastrexo do progreso das tarefas na WBS. Compara as horas de esforzo reais acumuladas para unha tarefa coas horas de esforzo planificadas. As seguintes fórmulas proporcionan os valores na vista de rastrexo do esforzo:

-   Porcentaxe de progreso = Esforzo real ata a data ÷ Esforzo planificado para a tarefa
-   Esforzo restante (tamén coñecido como estimación para completar \[ETC\]) = Esforzo planificado - esforzo real ata a data
-   Estimación ao completar (EAC) = Esforzo restante + Esforzo real ata a data
-   Varianza de esforzo proxectado = Esforzo planificado - EAC

A vista de rastrexo do esforzo mostra unha proxección da variación do esforzo para a tarefa, en función de se EAC é máis ou menos que o esforzo planificado:

-   Se a EAC supón un esforzo superior ao previsto, proxéctase que a tarefa levará máis tempo do que estaba previsto inicialmente e está atrasada.
-   Se a EAC supón un esforzo inferior ao previsto, proxéctase que a tarefa levará menos tempo do que estaba previsto inicialmente e está adiantada.

**Reproxección do esforzo do xestor de proxectos** En ocasións, o xestor do proxecto ou outra persoa que estea a rastrexar o progreso dun proxecto terá que revisar as estimacións orixinais dunha tarefa. A tarefa podería moverse máis rápido ou máis lento do que se prevía orixinalmente por varias razóns. Por exemplo, o alcance reduciuse ou os traballadores teñen menos experiencia da que se planificaba orixinalmente. As proxeccións son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto. En xeral, non debe cambiar os números da liña base porque a liña base do proxecto representa un documento ben publicado para a estimación de custo e programación do proxecto que todos os implicados no proxecto acordaron. 

Hai dous xeitos de que os xestores de proxectos poidan modificar o esforzo das tarefas:

-   Modificar o esforzo restante que se define automaticamente para actualizar o esforzo restante real na tarefa.
-   Modificar a porcentaxe de progreso que se define automaticamente para actualizar o progreso real na tarefa.

Ambos enfoques provocan un novo cálculo do ETC, EAC e a porcentaxe de progreso da tarefa, e a variación do esforzo proxectado nunha tarefa. Tamén se calculan de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e actualízase a súa variación do esforzo proxectada. 

**Esforzo modificado en tarefas resumo** Pode modificar o esforzo en tarefas resumo ou contedor. Independentemente de que vostede modifique estes valores empregando o esforzo restante ou a porcentaxe de progreso nas tarefas resumo, os cálculos realízanse automaticamente na seguinte orde:

1.  Calcúlanse o EAC, ETC e a porcentaxe progreso da tarefa.
2.  A nova EAC distribúese ás tarefas dependentes na mesma proporción que a cantidade do EAC orixinal.
3.  Calcúlase o novo EAC en cada tarefa nó folla.
4.  A porcentaxe de esforzo e progreso restante calcúlanse de novo para todas as tarefas dependentes afectadas, en función do novo valor de EAC. Tamén se calcula de novo a variación do esforzo das tarefas.
5.  A EAC das tarefas resumo tamén se calcula de novo a partir dos nós folla.

Prema **Ampliar ao nivel** na vista de rastrexo do esforzo para establecer o nivel no que se realiza un rastrexo e manter a súa WBS. A WBS amplíase automaticamente ata ese nivel na vista de rastrexo de esforzo cada vez que a abre.

### <a name="cost-tracking-view"></a>Vista de rastrexo de custo

A vista de rastrexo de custos mostra o rastrexo do consumo de custos para unha tarefa. Nesta vista, o custo real que se gastou nunha tarefa ata a data compárase co custo previsto para a tarefa. As seguintes fórmulas proporcionan os valores na vista de rastrexo do custo:

-   Porcentaxe do custo consumido = Custo real ata a data ÷ Custo planificado para a tarefa
-   Custo para completar (CTC) = Custo planificado - Custo real ata a data
-   Estimación ao completar (EAC) = CTC + custo real ata a data
-   Varianza do custo proxectado = Custo planificado - EAC

A vista de rastrexo do custo mostra unha proxección da variación do custo para a tarefa, en función de se EAC é máis ou menos que o custo planificado:

-   Se a EAC supón un custo superior ao previsto, proxéctase que a tarefa usará máis diñeiro do que estaba previsto inicialmente e supera o orzamento.
-   Se a EAC supón un custo inferior ao previsto, proxéctase que a tarefa usará menos diñeiro do que estaba previsto inicialmente e non supera o orzamento.

**Reproxección do custo do xestor de proxectos** Os xestores de proxectos deben usar CTC para revisar a estimación de custo orixinal nunha tarefa. O xestor do proxecto pode modificar o valor de CTC ao custo necesario para completar a tarefa. Se modifica o valor de CTC, calcularanse de novo o CTC, a EAC e a porcentaxe do custo consumido da tarefa e a variación de custo proxectada nunha tarefa. Tamén se calculan de novo EAC, ETC e a porcentaxe de custo consumido nas tarefas resumo, e actualízase a súa variación do custo proxectada. 

> [!NOTE] 
> Cando revisa o esforzo para unha tarefa da WBS na vista de rastrexo do esforzo, o CTC da tarefa, a EAC, a porcentaxe do custo consumido e a variación de custo proxectada calcúlanse de novo na vista de rastrexo de custo. Non obstante, as revisións de custos non afectan os valores da vista de rastrexo do esforzo, porque o custo por tipo de transacción (man de obra, material ou gasto) ou categoría de proxecto non se revisa. 

**Revisión de proxección de custos en tarefas resumo** Podes revisar os custos das tarefas resumidas e os cálculos prodúcense automaticamente na seguinte orde:

1.  A EAC, o CTC e a porcentaxe do custo consumido na tarefa calcúlanse de novo.
2.  A nova EAC distribúese nas tarefas dependentes na mesma proporción que o EAC orixinal estaba nas tarefas.
3.  Calcúlase a nova EAC para cada tarefa.
4.  O CTS e a porcentaxe do custo consumido calcúlanse de novo para as tarefas dependentes afectadas, en función do valor de EAC. Tamén se calcula de novo a variación do custo das tarefas.
5.  A EAC para todas as tarefas resumo calcúlase de novo en función deste cambio.

Prema **Ampliar ao nivel** na vista de rastrexo do custo para establecer o nivel no que se realiza un rastrexo e manter a súa WBS. A WBS amplíase ata ese nivel na vista de rastrexo de custo cada vez que a abre.

### <a name="earned-value-management"></a>Xestión do valor gañado

Podes usar o método de valor gañado (EVM) para rastrexar o progreso dun proxecto. Pode ver os indicadores de valor gañado no centro de roles do xestor de proxectos. O compoñente do gráfico de valor gañado mostra os valores por fases temporais do valor planificado e do custo real. O valor gañado a partir da data actual móstrase como un punto. Os datos de fases temporais do valor obtido non están dispoñibles actualmente. 

A fase temporal no gráfico de valor gañado móstrase por semana ou por mes. Esta sección describe os tres piares do EVM: valor planificado, valor gañado e custo real. 

**Valor planificado** A teoría de EVM afirma que a gráfica de valor planificado representa a velocidade coa que o equipo do proxecto tiña previsto gañar valor no proxecto. 

Finanzas usa a regra de ganancia 0:100 cando representa graficamente o valor planificado. Segundo esta regra, o valor da tarefa contabilízase na tarefa a partir da súa data de finalización. Non se contabiliza ningún valor ata completar a tarefa ao 100 por cento. 

En Xestión de proxectos e contabilidade, introduza a data de finalización dos nós folla e o custo previsto para iso. Cando se mostra o gráfico do valor planificado por semana, o valor planificado resúmese por semana para todas as tarefas nó folla durante todo o proxecto. 

**Valor gañado** A teoría de EVM afirma que a gráfica de valor gañado representa a velocidade coa que o equipo do proxecto está a gañar valor realmente no proxecto. 

Finanzas usa a regra de ganancia 0:100 cando representa graficamente o valor gañado. Segundo esta regra, o valor da tarefa contabilízase na tarefa a partir da súa data de finalización. Non se contabiliza ningún valor ata completar a tarefa ao 100 por cento. 

Cando se calcula o valor gañado, considérase a porcentaxe de progreso de cada tarefa. Segundo a regra de ganancia 0:100, só se consideran as tarefas que se realizan nun período determinado para o cálculo do valor obtido a partir do final dese período. O valor gañado no proxecto calcúlase para todas as tarefas que se completaron cando se crea o gráfico. 

> [!NOTE] 
> Actualmente, o sistema de rastrexo de WBS non ten estruturas de datos para almacenar porcentaxes de progreso histórico en cada tarefa. Polo tanto, o valor obtido só se pode informar no momento en que se procesa o cubo. Procese o cubo regularmente para actualizar os datos do valor obtido que se amosan no centro de roles. 

**Custo real** A teoría de EVM afirma que a representación gráfica do custo real representa a velocidade coa que se gasta o diñeiro no proxecto. 

As transaccións que se contabilizan nun proxecto úsanse para rastrexar a liña de custos reais. Os custos resúmense por data. Estes datos úsanse para representar os custos reais por semana ou por mes no gráfico de valores gañados.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Como usar os conceptos de valor planificado, valor gañado e custo real

**Variación do programa** Durante a planificación, vostede crea unha previsión para o traballo nunha liña de tempo. Polo tanto, o valor previsto é a velocidade coa que os planificadores de proxectos pensaron que se completaría o traballo no proxecto. Despois de que un proxecto estea en curso, o traballo rematou e o proxecto gaña valor. Comparando o valor planificado co valor gañado, pode ver como avanza o traballo nun proxecto. O resultado desta comparación chámase variación do programa. 

Se o valor previsto para un período é superior ao valor gañado, a cantidade de traballo realizado nun proxecto é inferior ao previsto. Polo tanto, o proxecto está atrasado. Debido a que o valor planificado e o valor gañado se expresan en termos monetarios, o tempo de atraso no proxecto tamén recibe un valor monetario. 

Se o valor previsto para un período é inferior ao valor gañado, a cantidade de traballo realizado nun proxecto é superior ao previsto. Polo tanto, o proxecto está adiantado. Este tempo de entrega tamén ten un valor monetario.

**Variación de custos** Debido a que o valor gañado utiliza o prezo de custo como multiplicador, o valor gañado indica o custo do traballo que se realiza nun proxecto. A medida que avanza un proxecto, o rexistro de transaccións proporciona un rexistro do diñeiro que realmente se gasta nese proxecto. Ao comparar o valor gañado co custo real, pode ver a cantidade de diñeiro que se gasta fronte ao valor que se gaña. O resultado desta comparación chámase variación do custo. 

Se o custo real que se gasta durante un período é superior ao valor gañado, gastouse máis diñeiro do que se gañou. Polo tanto, o proxecto superou o orzamento. 

Se o custo real que se gasta durante un período é inferior ao valor gañado, gañouse máis diñeiro do que se gastou. Polo tanto, o proxecto non superou o orzamento.

## <a name="wbs-templates"></a>Modelos de WBS
Podes usar a funcionalidade de modelos de WBS para crear modelos estándar para proxectos. Se os proxectos que ofrece a súa empresa implican moito traballo repetible, debería considerar a creación dun modelo de WBS. 

Podes crear un modelo de WBS a partir da WBS dun proxecto existente, de xeito que o coñecemento e as boas prácticas que reuniu durante a planificación dese proxecto se poidan reutilizar en proxectos similares no futuro. Non obstante, ás veces, pode que non teña sentido gardar toda a WBS como modelo. Polo tanto, tamén pode crear modelos a partir de partes da WBS para un proxecto.

### <a name="saving-a-projects-wbs-as-a-template"></a>Gardar a WBS dun proxecto como modelo

Despois de crear un modelo, pode importalo na WBS dun novo proxecto baixo o nó raíz ou en calquera tarefa da WBS do proxecto.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importación dun modelo de WBS á WBS dun proxecto

Cando importa tarefas, as tarefas do modelo organízanse en función da data de inicio da tarefa na que se importan. Durante a importación, as relacións predecesoras nas tarefas do modelo úsanse para calcular as datas de inicio das tarefas importadas. O calendario de traballo estándar do proxecto de destino aplícase para calcular as datas de finalización das tarefas importadas, de xeito que se conserven os días de traballo e o horario de traballo estándar definidos no calendario de traballo do proxecto actual. 

Os importes dos custos e os prezos de venda nas liñas de estimación aplícanse para garantir que os prezos específicos do proxecto ou contrato do proxecto teñen datas válidas.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Diferenzas entre a WBS dun proxecto e un modelo de WBS

-   As tarefas dos modelos de WBS non teñen datas de inicio e fin.

Os días laborables e non laborables non están definidos para os modelos de WBS.

-   Os modelos de WBS sempre usan o calendario de programación configurado como calendario predefinido para todos os proxectos.

O calendario de programación predefinido úsase só para coñecer as horas nun día de traballo estándar.

-   As relacións predecesoras non se copian nun modelo de WBS.

Debido a que os modelos de WBS non teñen datas, non é necesaria a lóxica de data de inicio baseada na data de finalización do predecesor.

-   Unha liña de estimación de custos de traballo créase automaticamente cando se crea unha tarefa nun modelo de WBS. O prezo de venda e o importe do custo copíanse do traballador seleccionado.

Os custos dos gastos e dos artigos pódense crear manualmente, do mesmo xeito que na WBS dun proxecto.

-   Os erros de programación móstranse cando hai desviacións da seguinte fórmula:

Esforzo = Número de recursos × Duración × Número de horas nun día de traballo estándar 

Podes corrixir todos os erros de programación ao mesmo tempo premendo **Corrixir todos os erros de programación**. 

Como alternativa, pode corrixir os erros de programación individualmente premendo na icona de aviso de cada tarefa.



