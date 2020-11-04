---
title: Configurar roles nos modelos de estrutura de subdivisión do traballo
description: Este tema ofrece información sobre como configurar información de roles en modelos de estrutura de subdivisión do traballo.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
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
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076112"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Configurar roles nos modelos de estrutura de subdivisión do traballo

[!include [banner](../includes/banner.md)]

Os xestores de proxectos poden configurar modelos de estrutura de subdivisión do traballo (WBS) que poden aplicar cando crean unha WBS para novos proxectos. Os xestores de proxectos poden engadir roles cando crean un modelo. Utilice o seguinte procedemento para atribuír un rol a un modelo de WBS.

1. Seleccione **Xestión e contabilidade de proxectos** > **Configurar** > **Proxectos** > **Modelos de estruturas de subdivisión do traballo**.
2. Seleccione **Detalles** para ver un modelo de WBS seleccionado.
3. Seleccione unha tarefa na lista e, a seguir, no campo **Rol** , seleccione un rol para atribuír á tarefa.

## <a name="work-with-a-wbs"></a>Traballar cunha formularios

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

1. Na páxina **Todos os proxectos** , seleccione o proxecto **Fase 2 de actualización de XYZ**.
2. Seleccione **Planificar** > **Actividades** > **Estrutura de subdivisión do traballo**.
3. Seleccione **Nova** para engadir as seguintes actividades de primeiro nivel á WBS:

    - Inicio
    - Planificación
    - Executando
    - Supervisión e control
    - Pechar

4. Estableza as datas e o esforzo (horas), como se mostra na seguinte ilustración.

    [![Establecemento de datas e esforzo](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleccione a liña da tarefa **Inicio** e, a seguir, no campo **Rol** , seleccione **Xestor de proxectos principal**.
6. Seleccione **Publicar**.
7. Na mesma liña, no campo **Recurso** , seleccione **Daniel Goldschmidt** e, a seguir, seleccione **Aceptar**.
8. Seleccione a liña da tarefa **Planificación** e, a seguir, no campo **Rol** , seleccione **Analista empresarial**.
9. Seleccione **Publicar** e, a seguir, seleccione **Xerar equipo automaticamente**.
10. Na caixa de mensaxe que aparece, seleccione **Si**.
11. No campo **Recurso** verifique que o valor é **Analista empresarial 1**.
12. Para o recurso **Analista empresarial 1** , abra a busca e seleccione **Iniciar asignacións de recursos**. A seguir, seleccione un traballador para a tarefa.
13. Seleccione **Atribución branda** &gt; **Capacidade total**.

    > [!NOTE] 
    > Non recibe un aviso de que o recurso especificado é agora 2, porque o número de recursos segue a ser 1.

14. Na páxina **Estrutura de subdivisión do traballo** , valide a asignación de recursos na WBS e logo seleccione **Gardar**.
