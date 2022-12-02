---
title: Reserva branda dun recurso
description: Este artigo fornece información sobre como programar provisionalmente ou facer unha reserva branda de membros de equipo.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c666e5c0a83a3d1b440144a62cbd58a58c5db81
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929120"
---
# <a name="soft-book-a-resource"></a>Reserva branda dun recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Provisionalmente, pode programar ou facer unha "reserva blanda" dun recurso nun equipo de proxecto para informar de que ten intención de atribuír o recurso a un proxecto. As reservas brandas non consumen a capacidade dispoñible dun recurso, e pode atribuír membros do equipo con reserva branda a tarefas do proxecto. No entanto, debido a que a reserva branda non consume a capacidade dun recurso, pode facer unha "reserva dura" do recurso para outras tarefas dentro do mesmo período. Non se pode facer reservas brandas dos recursos xenéricos nin unha reserva branda pode satisfacer unha solicitude unha solicitude de recurso xenérico.

Os membros do equipo do proxecto con reserva branda móstranse no separador **Equipo** da páxina **Proxecto**, con as súas horas con reserva branda mostrados na columna **Horas con reserva branda** na visualización **Membros de equipo denominados**. Os membros do equipo con reserva branda tamén aparecen no panel de programación. Posto que teñen reserva branda, o panel de programación non mostra ningún consumo de capacidade para eses recursos. O tempo con reserva branda non aparece no separador **Conciliación**, nin se mostra no campo **Estender reservas** no separador **Conciliación** do panel de programación. 

Hai dúas formas de facer unha reserva branda dun membro do equipo nun proxecto: directamente desde o panel de programación, ou engadindo o membro do equipo no separador **Equipo**. 

## <a name="soft-book-from-the-schedule-board"></a>Reserva branda dende o panel de programación
Complete os seguintes pasos para facer unha reserva branda dun recurso desde o panel de programación. 

1. Abra o panel de programación, e logo no panel **Requisitos de reserva**, seleccione o separador **Proxecto**.
2. Localice o proxecto para o que desexa facer unha reserva branda de recurso. Se hai un gran número de proxectos na lista, seleccione o encabezado de columna **Proxecto** e, a seguir, use o filtro para buscar un ou varios proxectos.
3. Seleccione o proxecto e, a seguir, arrástreo e sólteo na grade de tempo do recurso.
5. No panel **Crear reserva de recurso**, axuste a data de inicio e finalización, estableza o **Estado da reserva** en **Branda** e logo estableza as horas. 
6. Prema **Reservar**. O recurso agora móstrase no separador **Equipo** como recurso para o proxecto. Na visualización **Membros do equipo nomeados** verá as horas con reserva branda na columna **Horas con reserva branda**.

> [!NOTE]
> Agora pode atribuír a reserva branda a tarefas no separador **Programación**. No separador **Conciliación**, o recurso mostra unha falta de reserva relativa a atribución da tarefa, xa que o separador **Conciliación** só ten en conta as reservas duras. Pode utilizar a funcionalidade de **Estender reservas** para facer unha reserva dura dun recurso e eliminar a falta de reservas duras contra as atribucións de recursos. Ten que cancelar manualmente a reserva branda do recurso utilizando **Manter reservas**.

## <a name="soft-book-on-the-team-tab"></a>Reserva branda no separador Equipo

Pode engadir membros do equipo directamente no separador **Equipo** e, a seguir, modifique o se seu estado de reserva de **Dura** a **Branda** con **Manter reservas**. Ao engadir un membro do equipo desta forma, sempre resultará nunha reserva dura a menos que seleccione o método de atribución como **Ningún**.

Para utilizar este método, realice os seguintes pasos.

1. Na páxina **Proxecto**, no separador **Equipo**, prema **Novo**.
2. Seleccione o recurso reservable, o rol, e datas desde e ata.
3. Seleccione un método de atribución que non sexa **Ningún**.
4. Seleccione **Gardar**. Tamén verá o recurso na grade e as súas horas na columna **Horas con reserva dura**.
5. Manter as reservas de recursos seleccionando **Manter reservas**.
6. Cando abre o panel de programación, expanda o recurso para mostrar as súas reservas. Verá a reserva indicada como **Dura**.
7. Prema co botón secundario na reserva, e en **Cambiar estado**, seleccione **Reserva branda** \> **Branda**. O estado da reserva é **Branda**.
8. Despois de pechar o panel de programación, verá que as horas para o recurso movéronse desde a columna **Horas con reserva dura** a **Horas con reserva blanda** na grade do separador **Equipo**, ao visualizar **Membros do equipo nomeados**.

> [!NOTE]
> Cando utiliza **Manter reservas** para cambiar o estado de **Dura** a **Branda**, se fai unha reserva dura dun recurso no equipo e atribúe tarefas ao recurso, retéñense as atribucións de tarefas para o recurso. No entanto, no separador **Conciliación**, o recurso terá unha falta de reserva, xa que só se consideran as reservas duras ao conciliar as reservas fronte as atribucións. Pode utilizar a funcionalidade de **Estender reservas** no separador **Conciliación** para facer unha reserva dura dun recurso e eliminar a falta de reservas duras contra as atribucións de recursos. Ten que cancelar a reserva branda do recurso utilizando **Manter reservas**.

Cando esté listo para modificar un recurso de membro de equipo con reserva branda a membro do equipo con reserva dura, faga o seguinte:

1. No panel de programación, expanda o recurso para mostrar as súas reservas. Verá a reserva marcada como **Branda**.
2. Prema co botón secundario na reserva, en **Cambiar estado**, seleccione **Reserva dura** \> **Dura**. O estado da reserva é agora **Dura**.
3. Despois de pechar o panel de programación, volver ao proxecto e abrir o separador **Equipo**, verá que as horas para o recurso movéronse desde a columna **Horas con reserva branda** á columna **Horas con reserva** dura na grade do separador **Equipo**, ao visualizar **Membros do equipo nomeados**. Se o recurso se atribuíu a tarefas, xa non mostrará unha falta de reserva no separador **Conciliación**, xa que as súas reservas agora son duras.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
