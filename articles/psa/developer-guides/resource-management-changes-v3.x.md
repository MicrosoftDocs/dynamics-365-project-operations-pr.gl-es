---
title: Cambios de xestión de recursos (Project Service Automation 3.x)
description: Este tema ofrece información sobre os cambios na área de xestión de recursos.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e888d55b93c40e08e51bd4480853fec37f2b6333
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007814"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Cambios de xestión de recursos (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

As seccións deste tema proporcionan información sobre os cambios realizados na área de xestión de recursos de Dynamics 365 Project Service Automation versión 3.x.

## <a name="project-estimates"></a>Estimacións do proxecto

En vez de basearse na entidade **msdyn\_projecttask** (**Tarefa do proxecto**), as estimacións do proxecto baséanse na entidade **msdyn\_resourceassignement** (**Atribución de recursos**). As atribucións de recursos convertéronse na "fonte de verdade" para a programación de tarefas e os prezos.

## <a name="line-tasks"></a>Tarefas de liña

En PSA 3.x, as tarefas de liña están obsoletas (desfasadas). As atribucións apuntan a toda a tarefa en lugar das tarefas de liña.

O seguinte exemplo mostra como unha tarefa denominada "tarefa de proba" está atribuída aos membros do equipo A e B en versións anteriores de PSA e en PSA 3.x.

- **Antes de PSA 3.x:**

    - Tarefa de proba

        - Tarefa de proba – tarefa de liña 1

            - Atribución a A

        - Tarefa de proba – tarefa de liña 2

            - Atribución a B

- **PSA 3.x:**

    - Tarefa de proba

        - Atribución a A
        - Atribución a B

## <a name="unassigned-assignment"></a>Atribución non atribuída

En PSA 3.x, unha atribución non atribuída é unha tarefa que se atribúe a un membro do equipo **NULO** e un recurso **NULO**. As atribucións sen atribuír poden ocorrer nun par de escenarios:

- Se se creou unha tarefa, pero aínda non foi atribuída a ningún membro do equipo, sempre se crea unha atribución sen atribuír. 
- Se se eliminan todos os atribuídos nunha tarefa, créase unha tarefa non atribuída para esa tarefa.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Campos de programación na entidade Tarefa de proxecto

Os campos da entidade **msdyn\_projecttask** quedaron desfasados ou movéronse á entidade **msdyn\_resourceassignment**, ou agora faise referencia a eles dende a entidade **msdyn \_projectteam** (**Membro do equipo de proxecto**).

| Campo desfasado en en msdyn\_projecttask (Tarefa de proxecto) | Novo campo en msdyn\_resourceassignment (Asignación de recursos) | Comentario |
|---|---|---|
| msdyn\_assignedresources | Ningún | |
| msdyn\_assignedteammembers | Ningún | |
| msdyn\_numberofresources | Ningún | |
| msdyn\_scheduledhours | Ningún | |
| msdyn\_effortcontour | msdyn\_plannedwork | Cambiouse o formato da estrutura de datos de JavaScript Object Notation (JSON) que se garda no campo. |

## <a name="schedule-contour"></a>Contorno de programación

O contorno de programación almacénase no campo **Traballo previsto** (**msdyn\_plannedwork**) de cada entidade **Atribución de recursos** (**msdyn \_resourceassignment**).

### <a name="structure"></a>Estrutura

A nova estrutura do contorno de programación consta de franxas de tempo flexibles que se definen para cada día da programación. Cada porción de tempo ten as seguintes propiedades:

- **Inicio** - O inicio do horario laboral do día, segundo o calendario do proxecto.
- **Final** - O final do horario laboral do día, segundo o calendario do proxecto.
- **Horas** - O número de horas asignadas no día.

**Exemplo**

Este exemplo usa un calendario de proxecto onde a xornada laboral é de 9:00 a 17:00 na zona horaria UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Programación automática e programación manual

Se unha tarefa está programada de xeito automático, as horas son de carga frontal e pode que a duración da tarefa se reduza.

**Exemplo**

A seguinte tarefa está programada de xeito automático durante 18 horas ao longo de tres días (do 3 de decembro de 2018 ao 5 de decembro de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Se unha tarefa está programada manualmente, as horas distribúense uniformemente en todas as datas.

**Exemplo**

A seguinte tarefa está programada manualmente durante 18 horas ao longo de tres días (do 3 de decembro de 2018 ao 5 de decembro de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unidade de atribución

A unidade de atribución quedou desfasada en PSA 3.x. As horas de esforzo da tarefa están hoxe igualmente divididas, por día, entre todos os recursos atribuídos.

**Exemplo**

Neste exemplo, a tarefa está asignada a dous recursos e está programada automaticamente durante 36 horas ao longo de tres días (do 3 de decembro de 2018 ao 5 de decembro de 2018).

- Atribución 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Atribución 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensións de prezos

En PSA 3.x, os campos de dimensión de prezos específicos dos recursos (como **Rol** e **Unidade organizativa**) elimináronse da entidade **msdyn \_projecttask**. Estes campos pódense recuperar dende o membro do equipo de proxecto correspondente (**msdyn \_projectteam**) da asignación de recursos (**msdyn \_resourceassignment**) cando se xeran estimacións do proxecto. Un novo campo, **msdyn\_organizationalunit**, engadiuse á entidade **msdyn\_projectteam**.

| Campo desfasado en en msdyn\_projecttask (Tarefa de proxecto) | Campo de msdyn\_projectteam (membro do equipo de proxecto) que se utiliza no seu lugar |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Contornos

Os campos de contorno de prezos e estimacións quedaron desfasadas na entidade **msdyn\_projecttask**. Trasladáronse á entidade **msdyn\_resourceassignment**.

| Campo desfasado en en msdyn\_projecttask (Tarefa de proxecto) | Novo campo en msdyn\_resourceassignment (Asignación de recursos) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Engadíronse os seguintes campos á entidade **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Non se modifican os seguintes campos para o custo e as vendas planificadas, reais e restantes na entidade **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]