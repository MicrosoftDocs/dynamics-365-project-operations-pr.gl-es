---
title: Requisitos da reserva branda
description: Este tema fornece información sobre como cumprir requisitos de reserva branda.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751463"
---
# <a name="soft-book-requirements"></a>Requisitos da reserva branda

Pódese facer unha reserva dura dun requisito de recursos. Unha reserva dura crea unha proposta que consume a capacidade dun recurso. A proposta é remitida ao solicitante para a súa aprobación. Unha reserva branda engade provisionalmente un recurso a un equipo de proxecto e ten un estado diferente no panel de programación, pero non consume a capacidade do recurso. Para facer unha reserva branda dun recurso, configure o campo **Estado da reserva** en **Branda**.

![O estado da reserva establecido en Branda](media/Resource-Management-image77.png)

Cando o separador **Equipo** está na vista **Membros nomeados do equipo**, o recurso aparece alí. As horas con reserva branda aparecen na columna **Horas con reserva branda**.

![Horas con reserva branda na vista de membros nomeados do equipo](media/Resource-Management-image78.png)

Non se poden atribuír os membros do equipo cunha reserva branda a tarefas.

![Membro do equipo cunha reserva branda atribuído a una tarefa.](media/Resource-Management-image79.png)

No separador **Conciliación**, non se amosan reservas para un recurso con reserva branda, porque o separador **Conciliación** considera só as reservas duras.

![Recurso con reserva branda sen reservas no separador Conciliación](media/Resource-Management-image80.png)

> [!NOTE]
> Non pode facer unha reserva branda dun recurso desde un requisito xerado cun membro xenérico do equipo.

No panel de programación, úsase unha cor diferente para reservas brandas para un recurso.

![Reservas brandas no panel de programación](media/Resource-Management-image81.png)

Para converter unha reserva branda en unha reserva dura, no panel de programación, prema co botón dereito do rato sobre a reserva branda e logo seleccione **Cambiar estado** \> **Reserva dura** \> **Dura**.

![Cambio do estado da reserva a dura](media/Resource-Management-image82.png)

A reserva cambia e o estado cámbiase no panel de programación. Como o estado da reserva é agora **Dura**, o recurso móstrase como reservado e axústase a súa capacidade e dispoñibilidade.

Pode usar o mesmo método para cancelar unha reserva dura ou unha reserva branda no panel de programación.

Para converter un recurso con reserva branda en reserva dura no separador **Equipo** do proxecto, seleccione o recurso e logo seleccione **Confirmar**.

![Comando Confirmar](media/Resource-Management-image83.png)
