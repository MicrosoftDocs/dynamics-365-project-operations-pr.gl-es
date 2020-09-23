---
title: Dotación de recursos de proxectos
description: Neste tema se proporciona información sobre a dotación de recursos de proxectos.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751322"
---
# <a name="project-resourcing"></a>Dotación de recursos de proxectos

[!include [banner](../includes/banner.md)]

Neste tema se proporciona información sobre a dotación de recursos de proxectos.

Un desafío para os xestores de proxectos e xestores de recursos durante a fase de planificación do proxecto é a asignación de recursos, na que deben determinar e reservar o recurso correcto para traballar nun proxecto. En Dynamics 365 Finance, as capacidades de dotación de recursos para proxectos permítenlle definir funcións que se tratan como recursos temporais que se poden reservar para un compromiso específico ou parte dun compromiso. Este tipo de recursos permiten aos xestores de proxectos e xestores de recursos realizar as seguintes tarefas:

- Definir un rol que teña as competencias requiridas, para que sexa fácil atopar recursos.
- Usar os roles para definir un programa de compromiso inicial baseado en recursos reservados.
- Estimar custos e determinar un orzamento inicial, segundo os roles e recursos asignados a un proxecto.
- Usar os roles para estimar o número de reservas de recursos necesarias para cada compromiso.
- Estimar o número de recursos necesarios para todo o ciclo de vida dun proxecto.
- Elaborar unha estrutura de subdivisión do traballo (WBS) empregando as atribucións de recursos iniciais.

[![Ciclo de vida do proxecto](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

A medida que avanza a planificación do proxecto, os recursos planificados pódense substituír por recursos con persoal. O xestor do proxecto tamén pode volver atrás e actualizar as reservas de recursos durante calquera fase do proxecto.

## <a name="set-up-project-resources"></a>Configurar recursos de proxectos
Debe configurar un calendario e asocialo a un empregado ou a un traballador. O calendario úsase para programar o proxecto e o tempo de traballo dos recursos reservados para o proxecto. Durante a configuración do calendario, os xestores de proxectos poden realizar a nivelación de recursos como parte da optimización de recursos. En función do programa do calendario, pódense aplicar restricións aos recursos. Pode configurar un calendario na páxina **Calendarios**.

Cando configura un traballador como recurso do proxecto, pode seleccionar entre os traballadores que traballan na empresa para a que configura recursos. Como alternativa, pode seleccionar traballadores doutras empresas da súa organización. Estes traballadores son coñecidos como recursos entre empresas.

Os seguintes procedementos explican como configurar un traballador como recurso de proxecto na súa empresa e como configurar un recurso de proxecto entre empresas.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurar un traballador como recurso do proxecto

1. Na páxina **Traballadores**, na lista **Traballadores**, seleccione o traballador que está a engadir como recurso do proxecto e abra o rexistro de traballador.
2. No panel de acción, seleccione **Proxecto** &gt; **Configurar** &gt; **Configuración do proxecto**.
3. Seleccione un calendario e logo peche a páxina.

Tamén pode especificar proxectos predefinidos para un recurso como un tipo de atribución previa. As atribucións previas pódense empregar cando o xestor de recursos ou o xestor de proxectos saiban en que proxectos traballará o recurso con antelación. As asignacións previas tamén poden basearse na solicitude dun patrocinador ou cliente do proxecto. Para atribuír previamente un proxecto, na páxina **Atribuír proxectos**, no separador **Proxectos**, na lista **Proxectos restantes**, seleccione o proxecto axeitado.

### <a name="set-up-an-intercompany-resource"></a>Configurar un recurso entre empresas

Cando configura un traballador como recurso entre empresas, debe completar a configuración tanto na empresa prestamista como na empresa prestameira.

**Na empresa prestamista**

1. En Finanzas, verifique que a empresa prestamista está seleccionada e logo complete o procedemento da sección anterior, "Configurar un traballador como recurso do proxecto".
2. Na páxina **Contabilidade entre empresas**, seleccione **Nova**.
3. No campo **ID da persoa xurídica**, seleccione a empresa prestamista. Encha os campos como corresponda e, a seguir, seleccione **Gardar**.
4. Na páxina **Prezo de transferencia**, seleccione **Novo**.
5. No campo **Persoa xurídica prestameira**, seleccione a empresa apropiada.
6. Para prestar á empresa prestameira só o recurso que creou ao comezo desta sección, no campo **Recurso**, seleccione o nome do recurso que creou. Para poñer todos os recursos da empresa prestamista a disposición da empresa prestameira, deixe o campo **Recurso** en branco.
7. Na páxina **Parámetros de xestión de proxectos e contabilidade**, no separador **Entre empresas**, configure a opción **Activar a programación de recursos e follas de control horario entre empresas** en **Si**.

**Na empresa prestameira**

- Na páxina **Lista de recursos**, no filtro de busca, introduza o nome do recurso que creou para a empresa prestamista, para comprobar que o nome está incluído na lista de recursos para a empresa prestameira.

## <a name="manage-resource-competencies"></a>Xestionar competencias de recursos
As competencias de recursos son unha parte esencial da xestión de recursos. As competencias pódense usar como base para determinar os recursos que teñan o equilibrio de habilidades, educación, certificación e experiencia no proxecto correctos. Debería configurar esta información para cada recurso e actualizala regularmente. Deste xeito, pode maximizar as capacidades cando se combinan competencias específicas de recursos durante a atribución de recursos do proxecto.

[![Exemplos de habilidades, certificacións, educación e experiencia no proxecto](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Os seguintes procedementos explican como configurar algunhas das competencias para un recurso.

Para configurar as competencias dun traballador, pode empregar a páxina de lista **Traballadores** en Recursos humanos ou a páxina de lista **Recursos** en Xestión de proxectos e contabilidade. Para os seguintes procedementos, utilízase a páxina de lista **Traballadores** en Recursos humanos.

### <a name="set-up-competencies-certificates"></a>Configurar competencias: certificados

1. Na páxina de lista **Traballadores**, seleccione a liña para que o traballador engada a información do certificado.
2. No panel Acción, no separador **Traballador**, no grupo **Competencias**, seleccione **Certificados**.
3. Seleccione **Novo** e, a seguir, no campo **Tipo de certificado**, seleccione **PMP**.
4. No campo **Data de inicio**, seleccione **01/10/2015** e seleccione **Gardar**.

### <a name="set-up-competencies-skills"></a>Configurar competencias: habilidades

1. Na páxina de lista **Traballadores**, asegúrese de que o traballador que utilizou no procedemento anterior aínda está seleccionado. A seguir, no panel Acción, no separador **Traballador**, no grupo **Competencias**, seleccione **Habilidades**.
2. Seleccione **Nova**.
3. No campo **Habilidade**, seleccione **Xestión de proxectos**.
4. No campo **Nivel**, seleccione **5 Experto**.
5. No campo **Data de nivel**, seleccione **1-/14/2014**.
6. No campo **Anos de experiencia**, introduza **10**.
7. Seleccione **Gardar** e logo peche a páxina.

## <a name="create-a-new-project"></a>Crear un novo proxecto
1. Na páxina **Xestión de proxectos**, seleccione **Novo proxecto** e introduza os seguintes valores:

    - **Tipo de proxecto:** Tempo e material
    - **Nome do proxecto:** Fase 2 de actualización de XYZ
    - **Grupo de proxectos:** TM\_WIP
    - **ID do contrato do proxecto:** 00000002

2. Seleccione **Crear proxecto**.

### <a name="assign-a-resource-to-a-project"></a>Atribuír un recurso a un proxecto

1. Na páxina **Traballadores**, na lista **Traballadores**, seleccione o rexistro do traballador para o que configurou competencias previamente e abra o rexistro de traballador.
2. No panel Acción, no separador **Proxecto**, no grupo **Configurar**, seleccione **Atribuír proxectos**.
3. Na páxina **Atribucións de proxectos de validación de recursos**, no separador **Proxectos**, no campo **Engadir o proxecto aos proxectos seleccionados**, filtre no proxecto **Fase 2 de actualización de XYZ**.
4. No panel **Proxectos restantes**, seleccione un proxecto e seleccione o botón de frecha para engadilo ao panel **Proxectos seleccionados**.

Tamén pode atribuír categorías a un recurso segundo o precise. O tipo de categoría é **Custo** ou **Ingresos**. O tipo de categoría está determinado pola súa organización. Se non se atribúen categorías a un recurso, Finanzas busca a categoría predefinida en prezos de hora para custo e ingresos.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurar as características do recurso e do rol do proxecto

Un xestor de proxectos pode usar a funcionalidade de dotación de recursos para crear os roles necesarios para o proxecto. Pódense usar roles se aínda se descoñecen os recursos confirmados cando se reservan os recursos. Os roles pódense reservar temporalmente como recursos planificados, para que poida continuar as fases de planificación do proxecto.

[![Exemplo de rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Escenario:** Contoso foi contratada para completar un proxecto de tempo e material que ten unha carta de proxecto aprobada. O xestor de proxectos subalterno aínda está completando o alcance do proxecto. O xestor de recursos está a identificar actualmente recursos específicos que se reservarán para traballar no novo proxecto. Debido á natureza crítica do proxecto, o patrocinador do proxecto solicitou ao xestor de proxectos principal como un dos roles. O xestor de recursos debe adquirir o novo recurso e definir o rol no sistema no caso de que o xestor de proxectos subalterno precise a información do recurso durante a planificación do proxecto.

Os seguintes pasos mostran como o xestor de recursos pode configurar a función de xestor de proxectos principal e asociar as características dos recursos a el. Máis tarde, o rol pódese empregar para buscar recursos dispoñibles que coincidan coas competencias requiridas.

1. Na páxina **Configurar roles**, seleccione **Novo** e introduza os seguintes valores:

    - **ID de rol:** Xestor de proxectos principal
    - **Descrición:** Xestor de proxectos principal

2. Seleccione **Crear**.
3. Seleccione o rol **Xestor de proxectos principal** e seleccione **Configurar características**.
4. No campo **Tipo de características**, seleccione **Habilidade**.
5. No campo **Características dispoñibles**, introduza a habilidade para buscar.
6. No campo **Tipo de característica**, seleccione **Certificado**.
7. No campo **Características dispoñibles**, introduza o tipo de certificado para buscar.

### <a name="assign-a-project-resource-to-a-project"></a>Atribuír un recurso de proxecto a un proxecto

1. Na páxina **Todos os proxectos**, seleccione o proxecto **Fase 2 de actualización de XYZ**.
2. No separador **Equipo do proxecto e programación**, seleccione **Engadir**.
3. No campo **Rol**, seleccione **Membro do equipo**.
4. Seleccione **Reservar desde calendario**.
5. Na páxina **Dispoñibilidade de recursos**, seleccione **Ver configuración**.
6. Na páxina **Axustar configuración de visualización**, introduza os seguintes valores:

    - **Formato para a visualización do intervalo de datas:** Día
    - **Mostrar descricións de dispoñibilidade:** Si
    - **Mostrar capacidade restante:** Si

7. Na lista de recursos, seleccione un recurso.
8. Seleccione **Reserva dura** e **Capacidade total**.


### <a name="assign-a-resource-to-a-default-role"></a>Atribuír un recurso a un rol predefinido

Para axudar aos xestores de proxectos ou recursos, pode profundizar nos recursos que se poden reservar para un proxecto. Pode asociar un rol predefinido a un recurso existente ou a un recurso adquirido recentemente. Por exemplo, cando se contratou a Daniel, tiña a experiencia e as habilidades para ocupar o rol de analista empresarial. O xestor de recursos asignou este rol como o rol predefinido de Daniel. Polo tanto, o xestor de recursos engadiu a Daniel a un grupo de analistas empresariais dispoñibles para traballar en proxectos.

Durante a reserva de recursos, os xestores de proxectos poden filtrar os recursos de rol dispoñibles para traballar en proxectos. Poden utilizar esta información como un criterio cando realizan análises de decisións con múltiples criterios durante o cumprimento dos recursos. Tamén poden engadir outras características de recurso ao filtro para buscar recursos que teñan habilidades, educación e experiencia específicas para un determinado proxecto.

**Escenario:** Comezou un proxecto aprobado e reservouse a función de xestor de proxectos principal como recurso planificado durante a fase de planificación do proxecto. O xestor de recursos agora adquiriu un recurso para cubrir o rol de xestor de proxectos principal.

1. Na páxina **Lista de recursos**, seleccione **Daniel Goldschmidt**.
2. Na páxina **Rol de recurso**, seleccione **Novo** e introduza os seguintes valores:

    - **Efectivo:** Introduza a data actual.
    - **Caducidade:** Introduce **Nunca**.
    - **Rol:** Introduza **Xestor de proxectos principal**.

3. Seleccione **Gardar** e logo peche a páxina.
4. No separador **Competencias**, engada a habilidade **ProjectMgmt** e o certificado **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurar prezos baseados en roles
Pódense configurar todos os custos, vendas e prezos de transferencia para roles.

1. Na páxina **Prezo de venda (hora)**, seleccione **Novo** e introduza unha data de entrada en vigor.
2. Na columna **Rol**, seleccione un rol.
3. Na columna **Prezos**, introduza un prezo para o rol de recurso seleccionado.

## <a name="form-a-project-team"></a>Formar un equipo de proxecto
Para usar os roles que se configuraron previamente nun proxecto, un xestor de proxectos debe asociar os roles ao proxecto. Pódense asignar varios roles para un proxecto. Para evitar confusións, estas funcións etiquétanse automaticamente durante a reserva. Por exemplo, se o xestor de proxectos require tres enxeñeiros de software, tres roles de enxeñeiro de software que teñen **enxeñeiro de software 1**, **enxeñeiro de software 2** e **enxeñeiro de software 3** como etiquetas que se xeran automaticamente. Se previamente se definiron as características do rol, aplícanse como filtro durante as buscas dun recurso. Pódense engadir características adicionais segundo sexa necesario para mellorar a busca.

A configuración da visualización tamén se pode personalizar para visualizar mellor a dispoñibilidade de recursos. Hai opcións para amosar a dispoñibilidade horaria, diaria, semanal, mensual, trimestral e anual. Tamén hai unha opción para amosar a capacidade dispoñible e restante de recursos. Esta opción é útil para a xestión do tempo cando estima o tempo dispoñible para actividades ou a dispoñibilidade de recursos.

O xestor de proxectos pode seleccionar un rol na páxina e despois, se hai un recurso dispoñible que se axuste ao requisito, seleccionar reservar un recurso para cubrir o rol. Teña en conta que non ten que reservar os recursos neste momento da fase de planificación. Cando crea unha WBS, pode substituír roles por recursos de persoal para o proxecto. Se as funcións substitúense por recursos con persoal na WBS, a configuración de recursos actualiza automaticamente a listaxe e a programación do equipo do proxecto.

[![Listaxe do equipo do proxecto que inclúe roles e recursos reais](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

O xestor do proxecto ten varias opcións para reservar un recurso para un proxecto, como **Capacidade restante**, **Capacidade total**, **Porcentaxe de capacidade** e **Especificar horas**. Estas opcións de reserva pódense cancelar en calquera momento se cambian as atribucións de recursos. Admítense dous tipos de reserva:

- **Reserva dura** - Aprobouse e confirmouse a reserva de recursos para traballar no compromiso durante o tempo especificado.
- **Reserva branda** - A reserva de recursos estableceuse provisionalmente para traballar no compromiso durante o tempo especificado.

O seguinte procedemento explica como crear un equipo de proxecto:

### <a name="create-a-project-team"></a>Crear un equipo de proxecto

1. Na páxina de lista **Todos os proxectos**, seleccione un proxecto e logo seleccione **Editar**.
2. No separador **Equipo do proxecto e programación**, no campo **Data de finalización da programación**, introduza a data de inicio da programación máis un mes. Por exemplo, se a data de inicio da programación é o 24 de xuño de 2017 (24/06/2017), introduza **24/07/2017**.
3. Seleccione **Engadir**.
4. No panel **Engadir roles ao proxecto**, no campo **Rol**, seleccione **Xestor de proxectos principal**.
5. Seleccione **Competencias requiridas**.
6. Na páxina **Elixir características**, as características que configurou previamente para o rol de xestor de proxectos principal se seleccionan de xeito predefinido. Seleccione **Aceptar**.
7. Na páxina **Engadir funcións ao proxecto**, no campo **Número de recursos**, introduza **1**.
8. No campo **Recurso**, a busca mostra todos os recursos que teñen as competencias requiridas. Seleccione **Daniel Goldschmidt** e, a seguir, seleccione **Crear**.
9. Na páxina **Proxecto**, seleccione **Engadir**.
10. No panel **Engadir roles ao proxecto**, no campo **Rol**, seleccione **Membro do equipo**. No campo **Número de recursos**, introduza **5**.
11. Seleccione **Crear**.
12. Na páxina **Proxectos**, seleccione **Encher recurso**.

## <a name="resource-capacity-synchronization"></a>Sincronización da capacidade dos recursos
Os procesos de sincronización de recursos axudan a garantir que a información do calendario e do calendario base chega á programación de recursos do proxecto. Se se cambia o calendario, os procesos realizan as actualizacións necesarias para a programación dos recursos do proxecto. Os procesos tamén axudan a mellorar o rendemento, porque a información dos recursos do calendario está sincronizada con antelación. Polo tanto, as actualizacións da información de programación de recursos prodúcense con maior rapidez. Recomendámoslle que programe os procesos como un lote en vez de un á vez. En caso contrario, existe o risco de que alguén esqueza as datas incluídas na última sincronización da información. Se non se utilizan datas inclusivas, poden producirse lagoas durante a sincronización de datas.

![Sincronización do calendario](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar agrupamentos de capacidade de recursos

O proceso de sincronización está deseñado para sincronizar toda a información do calendario de recursos. Esta información inclúe información do calendario base sobre calquera cambio na táboa de capacidade do calendario dos recursos do proxecto. Se se engaden novos recursos no proxecto, a sincronización axuda a garantir que a información actualizada do calendario está dispoñible. Esta sincronización pódese facer en calquera momento.

Recomendámoslle que use un lote. As opcións están dispoñibles durante a sincronización das reservas de capacidade.

1. Seleccione **Xestión de proxectos e contabilidade** &gt; **Periódico** &gt; **Sincronización de capacidade** &gt; **Sincronizar agrupamentos de capacidade de recursos**.
2. Configure as opcións na táboa seguinte.

    | Opción      | Descripción |
    |-------------|-------------|
    | Código do período | Opcionalmente, seleccione o código do intervalo de datas do libro maior para establecer as datas de inicio e finalización do proceso de sincronización para os agrupamentos de capacidade de recursos. |
    | Data de inicio  | Introduza a data de inicio do proceso de sincronización para os agrupamentos de capacidade de recursos. |
    | Data de finalización    | Introduza a data de finalización do proceso de sincronización para os agrupamentos de capacidade de recursos. |

[![Proceso de sincronización](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurar roles nos modelos de WBS
Os xestores de proxectos poden configurar modelos de WBS que poden aplicar cando crean unha WBS para novos proxectos. Os xestores de proxectos poden engadir roles cando crean un modelo. Utilice o seguinte procedemento para atribuír un rol a un modelo de WBS.

1. Seleccione **Xestión de proxectos e contabilidade** &gt; **Configurar** &gt; **Proxectos** &gt; **Modelos de estruturas de subdivisión do traballo**.
2. Seleccione **Detalles** para ver un modelo de WBS seleccionado.
3. Seleccione unha tarefa na lista e, a seguir, no campo **Rol**, seleccione un rol para atribuír á tarefa.

### <a name="work-with-a-wbs"></a>Traballar cunha formularios

Pode crear unha nova WBS ou copiar unha WBS dun modelo de WBS existente. Un xestor de proxectos pode xestionar facilmente os recursos atribuíndo funcións a novas tarefas na WBS. Os roles pódense substituír despois de que se adquira un recurso ou despois de identificar un recurso confirmado para traballar na tarefa. Esta flexibilidade permitirá aos xestores de proxectos realizar as seguintes tarefas:

- Identificar o número de recursos necesarios para os paquetes de traballo de WBS.
- Estimar custos de proxectos.
- Determinar un orzamento preliminar.
- Estimar a duración da actividade, baseada en roles e recursos.
- Desenvolver algúns plans de xestión de proxectos, baseados na información do proxecto dispoñible.

Engadíronse opcións adicionais na WBS para utilizar mellor a funcionalidade de dotación de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Asignacións de recursos</td>
<td>Visualizar os recursos, as datas, o número de horas e o tipo de reserva asignados para tarefas na WBS.</td>
</tr>
<tr class="even">
<td>Xerar equipo automaticamente</td>
<td>Engadir automaticamente os recursos planificados usando roles asociados a unha tarefa. Finanzas suxiren automaticamente os recursos planificados mediante a análise de decisións con múltiples criterios baseada en roles. Despois de definir as funcións e o esforzo (horas) para as tarefas nunha WBS e despois de liberar a estrutura, seleccione <strong>Xerar equipo automaticamente</strong>. O número necesario de recursos planificados engádese á WBS e ao separador <strong>Programación de proxectos e equipos</strong>.</td>
</tr>
<tr class="odd">
<td>Recurso (lista despregable)</td>
<td>Na páxina <strong>Iniciar a atribución de recursos</strong>, pode seleccionar recursos para reserva dura ou reserva branda, en función da duración especificada. Pode axustar a configuración da visualización para ver e establecer a duración das actividades de recursos. Pode seleccionar e atribuír recursos a nivel de paquete de traballo empregando as seguintes opcións:
<ul>
<li><strong>Aceptar</strong> - Confirmar os cambios no recurso atribuído a unha tarefa.</li>
<li><strong>Cancelar</strong> - Cancelar os cambios no recurso atribuído a unha tarefa.</li>
<li><strong>Atribuir automaticamente</strong> - Seleccionase automaticamente un recurso dispoñible con persoal que teña un papel coincidente e atribuído á tarefa seleccionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na páxina **Todos os proxectos**, seleccione o proxecto **Fase 2 de actualización de XYZ**.
2. Seleccione **Planificar** &gt; **Actividades** &gt; **Estrutura de subdivisión do traballo**.
3. Seleccione **Nova** para engadir as seguintes actividades de primeiro nivel á WBS:

    - Inicio
    - Planificación
    - Executando
    - Supervisión e control
    - Pechar

4. Estableza as datas e o esforzo (horas), como se mostra na seguinte ilustración.

    [![Establecemento de datas e esforzo](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleccione a liña da tarefa **Inicio** e, a seguir, no campo **Rol**, seleccione **Xestor de proxectos principal**.
6. Seleccione **Publicar**.
7. Na mesma liña, no campo **Recurso**, seleccione **Daniel Goldschmidt** e, a seguir, seleccione **Aceptar**.
8. Seleccione a liña da tarefa **Planificación** e, a seguir, no campo **Rol**, seleccione **Analista empresarial**.
9. Seleccione **Publicar** e, a seguir, seleccione **Xerar equipo automaticamente**.
10. Na caixa de mensaxe que aparece, seleccione **Si**.
11. No campo **Recurso** verifique que o valor é **Analista empresarial 1**.
12. Para o recurso **Analista empresarial 1**, abra a busca e seleccione **Iniciar asignacións de recursos**. A seguir, seleccione un traballador para a tarefa.
13. Seleccione **Atribución branda** &gt; **Capacidade total**.

    > [!NOTE] 
    > Non recibe un aviso de que o recurso especificado é agora 2, porque o número de recursos segue a ser 1.

14. Na páxina **Estrutura de subdivisión do traballo**, valide a asignación de recursos na WBS e logo seleccione **Gardar**.

## <a name="resource-fulfillment-for-planned-resources"></a>Cumprimento de recursos para os recursos planificados
Un xestor de proxectos pode planificar os roles de recursos necesarios para un proxecto. O xestor de recursos verá estes recursos planificados como solicitudes na páxina **Cumprimento de recursos** e pode atribuír recursos reais.

1. Na páxina **Todos os proxectos**, seleccione o proxecto **Fase 2 de actualización de XYZ**.
2. Seleccione **Proxecto** e, a seguir, seleccione **Editar**.
3. No separador **Equipo do proxecto e programación**, seleccione **Engadir**.
4. Na caixa de diálogo **Engadir roles**, seleccione o rol **Programador de software**.
5. Seleccione **Crear** e logo peche a páxina do proxecto.
6. Na páxina **Cumprimento de recursos**, seleccione **Programador de software 1** para o proxecto **Fase 2 de actualización de XYZ**.
7. Seleccione un traballador e, a seguir, seleccione **Atribuír**.
8. Verifique que a liña para **Programador de software 1** se eliminou para o proxecto **Fase 2 de actualización de XYZ**.
9. No separador **Equipo do proxecto e programación**, para o proxecto **Fase 2 de actualización de XYZ**, verifique que o traballador que seleccionou no paso anterior se engadiu como **Programador de software**.

## <a name="requests-for-project-resources"></a>Solicitudes de recursos do proxecto
A funcionalidade para a programación de recursos do proxecto só permite aos xestores de recursos distribuír recursos con persoal en compromisos ou proxectos. Para activar esta funcionalidade, complete as seguintes tarefas ou verifique que se completaron:

- Configurar as secuencias numéricas.
- Configurar fluxos de traballo de xestión de proxectos e contabilidade.
- Activar fluxos de traballo de solicitude de recursos.

Despois de completar as tarefas anteriores, pode completar as seguintes tarefas se o precisa:

- Crear unha solicitude de recurso a partir dun recurso con persoal con reserva branda.
- Supervisar solicitudes de recursos.
- Cumprir de solicitudes de recursos.
- Solicitar un recurso con persoal dunha WBS.
- Reservar recursos para un proxecto sen ter unha solicitude dun recurso con persoal.

## <a name="monitor-project-teams"></a>Supervisar os equipos do proxecto
1. Na páxina **Todos os proxectos**, seleccione a ligazón **ID de proxecto** para o proxecto **Fase 2 de actualización de XYZ**.
2. No separador rápido **Equipo do proxecto e programación**, verifique que os recursos do proxecto que aparecen na lista son correctos.
