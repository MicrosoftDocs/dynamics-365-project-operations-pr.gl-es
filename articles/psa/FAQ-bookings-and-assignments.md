---
title: Reservas de recursos e como se relacionan coas atribucións de tarefas
description: Este tema proporciona información sobre como xestionar os recursos nomeados, as reservas de recursos e as atribucións de tarefas e como se relacionan entre si.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 03285d324e855ecf933b155559e5a4826420ab25
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076319"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Reservas de recursos e como se relacionan coas atribucións de tarefas


Hai dous xeitos de reservar recursos denominados a un equipo de proxecto e tarefas de proxecto atribuídas:

- O recurso pode ser directamente reservado nunha proxecto e, a seguir, atribuído a tarefas de proxecto.
- As tarefas poden atribuírse a un recurso xenérico, que, a seguir, utilízase para localizar e substituír o xenérico por un recurso denominado. 

En ambos casos, a acción de reserva do recurso reserva a capacidade do recurso.

O xestor de proxecto que planifica o proxecto é o propietario do plan e a programación do proxecto. Ao utilizar o recurso xenérico para a atribución e, a seguir, xerar unha solicitude de recurso desde el, o xestor de proxecto pode reservar recursos no proxecto con contornos especificados no plan do proxecto. Poden reservar recursos nun proxecto e, a seguir, atribuírlles a tarefas. Non obstante, non hai ningunha forma de aliñar os contornos de rexistro con contornos das tarefas. As reservas non afectan á programación do proxecto.

Pense nun proxecto complexo con varias tarefas superpostas onde varios recursos do mesmo tipo teñen que traballar ao mesmo tempo. Se a un recurso atribúese un contorno que difire do agregado das súas atribucións, é difícil para modificar as tarefas necesarias para que encaixen co contorno de reservas para as súas tarefas discretas e os seus contornos orixinais.

No exemplo a continuación, o esforzo total necesario para o mesmo recurso dun conxunto de catro tarefas é 62 horas durante un período de dúas semanas e hai un contorno específico. Se o recurso Bob reservouse para 62 horas durante as mismas dúas semanas pero cun contorno diferente, o requisito e as reservas están en aliñación.

| **Contornos de tarefa**    | **Total de horas** | Lu 6/4 | Mar 6/5 | Mér 6/6 | Xov 6/7 | Ven 6/8 | S 6/9 | D 6/10 | Lu 6/11 | Mar 6/12 | Mér 6/13 | Xov 6/14 | Ven 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tarefa 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tarefa 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tarefa 3               | 1,0              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tarefa 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totais**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Dispoñibilidade de Bob
| **Reserva de recurso** | **Total de horas** | Lu 6/4 | Mar 6/5 | Mér 6/6 | Xov 6/7 | Ven 6/8 | S 6/9 | D 6/10 | Lu 6/11 | Mar 6/12 | Mér 6/13 | Xov 6/14 | Ven 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

No entanto, non hai ningunha forma sistemática de atribuír o contorno de horas reservadas para tarefas nunha base diaria. Se o xestor de proxecto quere modificar a programación de proxecto para satisfacer a dispoñibilidade do recurso, a seguir, terá que eliminar a atribución e revisar todas as tarefas para que coincidan cos contornos da reserva.

No caso dunha organización á que se lle atribuira a tarefa de planificación proxecto tanto a un xestor de proxecto e a un xestor de recurso, o xestor de proxecto define a programación, que inclúe o contorno do traballo necesario. O xestor de recurso non debería poder afectar á programación sen coñecemento do xestor de proxecto modificando contornos de esforzo ao reservar recursos reais. Se o xestor de recursos realiza algo diferente do que o xestor de proxecto solicitou, ten que chegar a un acordo sobre os cambios necesarios na programación do proxecto.

Posto que as reservas e atribucións non están totalmente emparelladas, é posible reservar contornos diferentes dos contornos da tarefa ou modificar as atribucións para provocar circunstancias onde as reservas e atribucións están fóra da aliñación.

A **Vista de conciliación** permite ao xestor de proxecto ver as reservas e atribucións de cada membro do equipo de proxecto. A vista utiliza cores e sombras para mostrar donde hai unha falta de coincidencia entre as reservas e atribucións dun membro do equipo. Segundo esta información, o xestor de proxecto pode tomar accións correctivas para ben estender as reservas de recursos para casos nos que hai atribucións e non hai reservas, ou cancelar reservas onde hai recursos reservados pero non hai atribucións.

> [!NOTE]
> Se move unha tarefa que contornou vostede mesmo, estes contornos non se manteñen. O contornos rexenéranse segundo o calendario de proxecto para dar conta das modificacións en horas de traballo e vacacións. Isto é por deseño porque o sistema non coñece a intención do contorno orixinal e non pode determinar se ten sentido manter ese contorno nun período de tempo novo. Posto que as reservas e as atribucións está desconectadas, as reservas conservan os contornos da reserva orixinal. Neste caso, deberá cancelar e volver a reservar no contorno da nova atribución.

