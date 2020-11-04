---
title: Como podo facer unha "reserva branda" de recursos na versión da apl. 2.x?
description: Este artigo describe como facer unha reserva branda de membros de proxecto con Project Service.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9e5d1c91f8ea98117583996552c2f2834be9c537
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076155"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Como podo facer unha "reserva branda" de recursos na aplicación web (aplicación Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Provisionalmente, pode programar ou facer unha "reserva blanda" dun recurso nun equipo de proxecto para informar de que ten intención de atribuír o recurso a un proxecto. As reservas brandas non consumen a capacidade dispoñible dun recurso. Non se poden atribuír os membros do equipo cunha reserva branda para tarefas de proxecto. Só os recursos co estado Reserva dura e tipo de compromiso Comprometido poden ser atribuídos a tarefas (sempre que teñan suficientes horas de reserva dura para cubrir o esforzo da atribución).

Os membros do equipo de proxecto con reserva branda aparecen na grade Membro do equipo con as súas horas de reserva branda mostradas na columna Reserva branda. Tamén se mostran no panel de programación. De novo, non indican calquer consumo de capacidade, xa que a reserva branda non consume a capacidade dun recurso.

Existen tres maneiras de facer unha reserva branda dun membro do equipo nun proxecto coa versión de Project Service 2.x. Pode facer unha reserva branda co panel de programación, utilizar a funcionalidade Manter reservas ou crear un recurso xenérico. Estes métodos se describen debaixo.

## <a name="soft-book-with-the-schedule-board"></a>Reserva branda co panel de programación

Siga este procedemento para facer unha reserva branda co panel de programación: 
1. Abrir o panel de programación.
2. Seleccionar o separador Proxecto na parte inferior do panel Requisitos de reserva do panel de programación.
3. Localice o proxecto no que desexa facer unha reserva branda. Se ten moitos proxectos, prema no título da columna Proxecto e, a seguir, utilice o filtro para encontrar o proxecto.
4. Prema no proxecto, a seguir, arrástreo e sólteo na grade de hora do recurso.
5. Isto abre o panel de Crear unha reserva de recurso á dereita. Axuste a data de inicio e fin, seleccione o Estado de reserva como brando e defina as horas. 
6. Prema Reservar.
7. No proxecto, o recurso agora aparecerá como membro do equipo coas horas con reserva branda na columna Reserva branda.

Teña en conta que non pode atribuírlle a tarefas na estrutura de subdivisión do traballo (WBS) xa que os recursos deben ter unha reserva dura no equipo para ser atribuídos.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Reserva branda utilizando a funcionalidade Manter reservas

Siga este procedemento para facer unha reserva branda con Manter reservas:
1. Na grade de membro do equipo, prema Novo.
2. Seleccione o recurso reservable, rol, desde/para.
3. Seleccione un método de atribución que non sexa Ningún:
- Capacidade completa
- Capacidade da porcentaxe
- Por horas: distribuír uniformemente
- Por horas: carga frontal
4. Prema Gardar. Tamén verá o recurso na grade do equipo e as súas horas indicadas como Dura.
5. Manter as reservas de recursos premendo Manter reservas.
6. Cando abre o panel de programación, expanda o recurso para mostrar as súas reservas. Verá a reserva indicada como Dura.
7. Prema co botón secundario na reserva, en Cambiar estado, seleccione Reserva branda e, a seguir, Branda. O estado da reserva é Brando.
8. Despois de pechar o panel de programación, verá que as horas do recurso cambiaron de Dura a Branda na grade de membro do equipo.
Teña en conta que se fai unha reservar dura dun recurso no equipo e, a seguir, atribúe as tarefas en WBS, ao utilizar Manter reservas para modificar o estado de Duro a Brando, eliminará a atribucións das tarefas para ese recurso, xa que só os recursos con reserva dura poden ser atribuídos a tarefas.

## <a name="soft-book-by-creating-a-generic-resource"></a>Reserva branda creando un recurso xenérico

Pode crear unha reserva branda xerando un membro do equipo de recurso xenérico, cumplindo co panel de programación ou Solicitar recursos e cambiando o tipo durante a reserva.
Para facelo, utilice o seguinte procedemento:

1. No WBS do proxecto, atribúa roles para as tarefas nas que desexa xerar membros do equipo xenéricos.
2. Prema Xerar equipo de proxecto.
3. Na grade de membro de equipo de proxecto, seleccione o recurso xenérico e prema Reservar.
4. No panel de programación, seleccione o recurso que desexa reservar.
5. No panel Crear reserva de recurso do panel de programación, cambie o Estado de reserva a Brando.
6. Prema Reservar ou Reservar e saír.

Despois de pechar o panel de programación, verá o recurso seleccionado engadido ao equipo con horas de reserva brand, así como as horas atribuídas. Tamén verá que o recurso xenérico continúa no equipo como un indicador de que as tarefas están atribuídas a un membro do equipo con reserva branda.

Cando esté listo para modificar un recurso de membro de equipo con reserva branda a membro do equipo con reservado dura para poder atribuílo a tarefas, faga o seguinte:

1. Seleccione o recurso e prema Manter reservas.
2. Cando abre o panel de programación, expanda o recurso para mostrar as súas reservas. Verá a reserva marcada como Branda.
3. Prema co botón secundario na reserva, en Cambiar estado, seleccione Reserva dura e, a seguir, Dura. O estado da reserva é Duro.
4. Despois de pechar o panel de programación, verá que as horas do recurso cambiaron de Branda a Dura na grade de membro do equipo. Agora pode atribuir o recurso a tarefas (sempre que haxa aliñación entre as horas con reserva dura e as horas de esforzo da tarefa de atribución). Teña en conta que se seguiron os pasos de realización de recurso xenérico no punto #3 anterior, cando se modifica o estado do recurso reservado con reserva branda a dura, o membro do equipo xenérico é eliminado do equipo.
