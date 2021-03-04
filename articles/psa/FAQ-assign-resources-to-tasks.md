---
title: Atribuír un recurso a unha tarefa
description: Este tema fornece información sobre como atribuír recursos a tarefas.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149991"
---
# <a name="assign-a-resource-to-a-task"></a>Atribuír un recurso a unha tarefa

[!include [banner](../includes/psa-now-project-operations.md)]

Hai tres formas de atribuír un recurso a unha tarefa en Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservar un recurso como un membro do equipo e, a seguir, atribuír o recurso a unha tarefa

Pode engadir un recurso ao equipo de proxecto e, a seguir, atribuír o recurso ás tarefas na programación do proxecto.

1. No separador **Membro do equipo**, engada un novo membro do equipo seleccionando **Novo**. 

2. Iso abre o panel **Creación rápida de membro do equipo**, onde pode seleccionar o nome do recurso reservable e defina un rol. 

    Seleccione un dos seguintes métodos de atribución para a reserva do recurso:

    - **Capacidade completa** reserva a capacidade completa do recurso para as datas desde e para especificadas.
    - **Capacidade da porcentaxe** reserva unha porcentaxe da capacidade do recurso para as datas desde e para especificadas.
    - **Distribuír uniformemente por horas** reserva o recurso para un número de horas especificado, e distribúe o tempo de forma similar por día sobre as datas desde e ata especificadas.
    - **Por horas: carga frontal** reserva o recurso para un número de horas especificado, con carga frontal das horas por día sobre as datas desde e para especificadas.
    - **Ningún** engade o recurso ao equipo, pero non crea ningunha reserva que absorba a capacidade do recurso.

3. Na grade de **Programación** para unha tarefa, seleccione a icona de **Recurso** na cela de recursos e, a seguir, baixo **Membros do equipo**, seleccione o membro do equipo que acaba de engadir. 

> [!NOTE]
> Nos separadores **Membro do equipo** e **Conciliación**, o recurso mostra as horas reservadas e as horas atribuídas. As horas deberían ser as mesmas, pero non é necesario, xa que as reservas e as atribucións non están totalmente emparelladas. O separador **Conciliación** ofrece detalles cando son diferentes, como por exemplo se atribúe a un recurso máis horas de traballo das que ten reservadas. Se é necesario, pode corrixir a información, ben estendendo as reservas do recurso ou modificando a atribución.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un membro do equipo xenérico a través da atribución de tarefas

Cando cree un membro de equipo xenérico a través da atribución de tarefas, ten que crear un marcador de posición ou recurso xenérico que describa as características do recurso denominado coas tarefas nas que vostede desexa que traballe. A seguir, pode xerar un requisito (ou enviar unha solicitude utilizando o requisito) que se utiliza para buscar e reservar o recurso denominado.

1. Na grade **Programación** para unha tarefa, seleccione a icona de **Recurso** na cela do recurso.

2. Escriba un nome que sirva como nome do recurso marcador de posición. Por exemplo, Xestor de programa.

3. Seleccione **Crear** e, no campo **Creación rápida de membro do equipo** de proxecto á dereita, defina o rol para o recurso xenérico.

4. Pode seguir atribuíndo tarefas a este recurso de marcador de posición seleccionando o recurso no **Selector de recursos** para a tarefa. Aparecen en **Membros do equipo**.

5. Cando termine a atribución do recurso xenérico, seleccione o recurso xenérico no separador **Equipo** e, a seguir, seleccione **Xerar requisito** para crear un requisito de recurso para o recurso xenérico.

6. Seleccione **Reservar** para o recurso xenérico. Despois pode usar o panel de programación para buscar e reservar un recurso real. Tamén pode enviar o requisito para conclusión por un xestor de recursos.

7. Cando o recurso xenérico cumple cun recurso denominado, o recurso xenérico elimínase do equipo e as atribucións de tarefa para o recurso xenérico atribúense ao recurso denominado que cumplíu o requisitos de recurso do recurso xenérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuír un recurso denominado da lista de todos os recursos que se poden reservar.

Pode utilizar a caixa de busca no **Selector de recursos** para buscar todos os recursos que se poden reservar en Project Service e atribuílos a unha tarefa.

Os recursos atribuídos deste xeito engádense ao equipo sen reservas. Isto é similar a engadir un membro do equipo e seleccionar Ningún como método de asignación. O recurso móstrase nos separadores **Equipo** e **Conciliación** como recursos co só atribucións e sen reserva. Reservaos se desexas utilizar a súa dispoñibilidade.

1. Na grade **Programación** para unha tarefa, seleccione a icona de **Recurso** na cela do recurso.

2. Comece a escribir un nome. Os resultados de busca para o nome móstranse no **Selector de recursos** en **Outros recursos**.

3. Seleccione o recurso que desexa atribuír á tarefa.

