---
title: Consideracións de actualización da estrutura de subdivisión do traballo
description: Este tema fornece información sobre a actualización da estrutura de subdivisión do traballo de Project Service Automation 2.x a 3.x.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076214"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Consideracións de actualización da estrutura de subdivisión do traballo
Este tema fornece información sobre a actualización da estrutura de subdivisión do traballo de Project Service Automation 2.x a 3.x. Este tema define o estado saudable dun proxecto en Project Service Automation (PSA) que é necesario para unha actualización con éxito. Tamén hai información sobre as condicións de bloqueo frecuentes que farán que a actualización falle. Para obter máis información sobre a definición das tarefas do proxecto e as súas funcións dentro dunha programación do proxecto, consulte [Programacións de proxecto](project-creating.md).

## <a name="key-entities"></a>Entidades clave
Para unha estrutura de subdivisión do traballo precisa que xa está cargada con recursos, son necesarias as seguintes entidades:

- [Proxecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Equipo do proxecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Tarefa do proxecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Atribucións de recursos](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dependencia da tarefa do proxecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Recursos reservables](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Para definir unha estrutura de subdivisión do traballo cargada con recursos, debe realizar os seguintes pasos:

1. Cree un novo proxecto. Para obter máis información sobre como crear un novo proxecto, consulte [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Cree unha ou varias tarefas. Para obter máis información sobre como crear unha tarefa, consulte [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Defina as dependencias de tarefas. Para obter máis información, consulte [Dependencia da tarefa do proxecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Atribuír membros do equipo do proxecto ao proxecto. Para obter máis información, consulte [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Atribuír membros do equipo do proxecto ás tarefas. Para obter máis información, consulte [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relacións do equipo do proxecto

Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:
- Todos os membros do equipo do proxecto deben estar asociados a un recurso reservable.
- Todos os membros do equipo do proxecto deben estar asociados ao mesmo proxecto. 

## <a name="project-task-relationships"></a>Relacións de tarefas do proxecto
Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:

- Todas as tarefas relacionadas deben estar asociadas ao mesmo proxecto.
- Cada tarefa de liña debe ter unha tarefa matriz.
- Cada tarefa de liña debe ter un proxecto matriz.

### <a name="valid-conditions"></a>Condicións válidas

- Todas as duracións das tarefas deben ser maiores ou iguais a (> =) unha hora e menos de 1.800.000 minutos (1250 días).*
- Todas as tarefas deben ter unha data de inicio que non sexa anterior a 2000/01/01. *
- Todas as tarefas deben ter unha data de inicio como máximo 17 anos desde a actualidade.*
- Todas as tarefas deben ter unha data de inicio anterior ou igual á data de finalización.
- Todos os tipos de transaccións en clasificacións (gasto, material, imposto e tempo) deben ter valores para **Unidade por defecto** e **Grupo de unidades**.
- Deben evitarse os formatos de datas con letras.

### <a name="potential-mitigation-steps"></a>Posibles pasos de mitigación
- Use Localización avanzada para identificar tarefas de proxecto que non conteñen un ID de proxecto.
- Use Localización avanzada para identificar as tarefas do proxecto onde a duración programada é maior que > 1 800 000.
- Antes de facer calquera cambio de datos, debe investigar as personalizacións asociadas á entidade que puideron dar lugar a obter os datos en mal estado. Estas personalizacións deben abordarse antes de continuar con actualizacións relacionadas cos datos.
- Para as tarefas identificadas que quedaron orfas, considere eliminar estas tarefas se non son necesarias ou se deben asociarse ao proxecto principal correcto.
- Para calquera tarefa onde a duración sexa superior a 1250 días, considere a posibilidade de engadir varias tarefas para representar a duración total, se é viable.

> [!NOTE]
> Os elementos sinalados cun asterisco (\*) teñen límites debido a que a xestión de relacións cos clientes (CRM) só admite 7320 expansións de recorrencia. Debe manterse por debaixo deste límite.

## <a name="resource-assignment-relationships"></a>Relacións de atribución de recursos
Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:

- Todas as atribucións de recursos nunha estrutura de subdivisión do traballo deben estar relacionadas co mesmo proxecto.
- Todas as atribucións de recursos nunha estrutura de subdivisión do traballo deben estar asociadas a membros do equipo de proxecto no mesmo proxecto.

### <a name="potential-mitigation-steps"></a>Posibles pasos de mitigación
- Identifique todas as tarefas que quedan fóra das condicións descritas anteriormente.  
- Deberanse eliminar todas as atribucións de recursos que xa non sexan válidas.

## <a name="project-task-dependency-relationships"></a>Relacións de dependencia de tarefas do proxecto
Para garantir unha actualización correcta, deben manterse correctamente as seguintes relacións:

- Todas as dependencias das tarefas do proxecto deben estar relacionadas co mesmo proxecto.
- Unha tarefa non pode facer referencia á mesma dependencia máis dunha vez.
