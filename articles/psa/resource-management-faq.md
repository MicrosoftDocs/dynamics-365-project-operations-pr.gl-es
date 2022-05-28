---
title: Preguntas frecuentes sobre xestión de recursos.
description: Este tema ofrece respostas a preguntas frecuentes sobre xestión de recursos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8ce1edf7d7c535271fa8076befd26f092fbd495
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587492"
---
# <a name="resource-management-faq"></a>Preguntas frecuentes sobre xestión de recursos.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Cal é a diferenza entre un membro do equipo e un requisito de recurso?

Un membro do equipo do proxecto pode ser atribuído a tarefas, reservado ou saturado e establecido como responsable de aprobación. Pode existir un requisito de recurso sen membro do equipo do proxecto, como nota de demanda. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Cal é a diferenza entre o has horas propostas e as horas de reserva branda?

As horas propostas e as horas de reserva branda difiren en visibilidade. As horas propostas só son visibles para os xestores de recursos e o xestor de proxectos que iniciaron a demanda mediante unha solicitude de recurso. As horas de reserva branda son visibles para todos os que teñan acceso ao panel de programación.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Como podo ver as horas de reserva branda para os recursos dun equipo?

As reservas brandas se poden facer ao reservar un requisito de recurso. Os recursos que teñen reservas brandas nun equipo do proxecto aparecen como membros do equipo que teñen horas de reserva branda. Tamén se aparecen no panel de programación.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Como cambio as horas necesarias e as datas de inicio e finalización dun recurso (xenérico ou nomeado) que reservei?

Despois de reservar os recursos, seleccione **Manter reservas** para facer os cambios que se precisen.

## <a name="what-resources-types-does-project-service-automation-support"></a>Que tipos de recursos admite Project Service Automation?

**Usuario** e **Contacto** son os únicos tipos de recursos que admite Dynamics 365 Project Service Automation. Aínda que pode crear outro tipo de recursos (por exemplo, **Equipamento** e **Grupo**), non se admite ningún caso de uso global.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Que diferenza hai entre unha atribución e unha reserva?

As atribucións son a atribución de recursos ás tarefas do proxecto na programación do proxecto. Os recursos poden ser recursos reais ou xenéricos. As reservas son a atribución branda o dura de recursos a un proxecto. As reservas duras consumen a capacidade dun recurso. O ideal sería que, para os recursos reais, as reservas e as atribucións coincidisen, porque non difiren. Non obstante, PSA non fai cumprir este acordo. A vista Conciliación mostra a un xestor de proxectos lugares onde as reservas e atribucións dun recurso non coinciden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
