---
title: Como podo atribuír un recurso reservable a unha tarefa na aplicación web
description: Unha visión xeral das formas en que pode asignar recursos reservables.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146571"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Como podo atribuír un recurso reservable a unha tarefa na aplicación web (aplicación Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Hai dúas formas de atribuír un recurso a unha tarefa en Project Service. Pode reservar un recurso como un membro do equipo e, a seguir, atribuílo a unha tarefa. Tamén pode crear un membro do equipo xenérico a través de atribución de rol en tarefas, xerar un equipo e, a seguir, cumplir os requisitos de seguranza cun recurso denominado.

Teña en conta que se se quere atribuír un recurso reservable a unha tarefa, o membro do equipo de recurso reservable debe ter suficientes reservas dispoñibles. O estado da reserva debe ser Tipo de compromiso reserva dura, e Estado comprometido. Se non hai suficiente reservas para o recurso, Project Service elimina a atribución e mostra a mensaxe de erro seguinte:

*Non é posible atribuír recurso á tarefa - Os seguintes recursos non teñen suficientes horas reservadas contra proxecto*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reserve un recurso como un membro do equipo e, a seguir, atribúa o recurso a unha tarefa.

Con este método pode engadir un recurso ao equipo de proxecto e, a seguir, atribuír as tarefas ao recurso na programación do proxecto. Aquí atopará a forma de facelo:
1.  Na grade de membro do equipo, engada un novo membro do equipo seleccionando **Novo**.
2.  Na pantalla Creación rápida de membro do equipo, seleccione o nome do recurso reservable e defina un rol.
3.  Seleccione as datas **Desde** e **Para**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de engadir membro do equipo](media/FAQ-Resources-to-Tasks2-1.png "Captura de pantalla de engadir membro do equipo")
 
4.  Seleccione un dos seguintes métodos de atribución para o reservar o recurso:
    - **Capacidade completa** reserva a capacidade completa do recurso para as datas desde e para especificadas.
    - **Capacidade da porcentaxe** reserva unha porcentaxe da capacidade do recurso para as datas desde e para especificadas.
    - **Por horas: distribuír uniformemente** reserva o recurso para un número de horas especificado, e distribúe o tempo de forma similar por día sobre as datas esde e para especificadas.
    - **Por horas: carga frontal** reserva o recurso para un número de horas especificado, con carga frontal das horas por día sobre as datas desde e para especificadas.

    Non seleccione **Ningún** porque engade o recurso ao equipo, pero non crea ningunha reserva que absorba a capacidade do recurso.
5.  Seleccione **Gardar**.

    Teña en conta que as horas da reserva deben ser suficientes para cubrir as horas de traballo e os intervalos de datas das tarefas que atribúa a este recurso. Se non están aliñadas, non pode atribuír o recurso á tarefa.

6.  Na estrutura de subdivisión do traballo (WBS) da tarefa, prema o despregable da cela de recursos. A seguir: 

    1. Seleccione **Engadir**.
    2. Seleccione o despregable en **Recursos** e seleccione o membro do equipo que engadiu anteriormente.
    3. Seleccione **Aceptar**. Agora, o membro do equipo agora atribuído á tarefa.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de engadir recursos con WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de pantalla de engadir recursos con WBS")
 
Na grade de membro do equipo, verá o total das horas atribuídas do recurso Horas atribuídas. Será igual ou inferior ás horas reservadas para o recurso. 

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla das horas asignadas para un recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de pantalla das horas asignadas para un recurso")
 
Se a tarefa que tenta atribuír ao recurso comeza despóis da data de fin das reservas de recursos, o recurso non aparecerán no despregable.

Teña en conta que pode atribuír un recurso a máis horas das horas reservadas se o recurso ten capacidade restante non atribuída. Neste caso o recurso só se atribuirá parcialmente até as súas reservas. Pode ver as horas de tarefa non atribuídas restantes engadindo a columna Horas sen personal á estrutura de subdivisión do traballo.

Se os recursos están atribuidos ás súas horas reservadas (as súas horas reservadas serán iguais que as súas horas atribuídas), poderá ver a seguinte mensaxe de erro ao tentar atribuírlles máis tarefas:

*Non é posible atribuír recurso á tarefa - Os seguintes recursos non teñen suficientes horas reservadas contra proxecto.*

Alén diso, o membro do equipo xestor de proxecto predefinido engadido ao equipo ao crear o proxecto engádese sen ningunha reserva e non se poden atribuír a ningunha tarefa. Non se mostrará no despregable do recurso para a tarefas.

Se desexa atribuír este recurso, ten que eliminalo do equipo e, a seguir, volver a engadilo cun método de atribución que non sexa Ningún. O motivo de que se engada ao equipo ao crear o proxecto é para que o proxecto teña polo menos un aprobador do proxecto por defecto.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Crear un membro do equipo xenérico a través da atribución de rol de tarefas

Este método garante que os recursos teñan suficientes reservas para as tarefas. En primeiro lugar, ten que crear un marcador de posición ou recurso xenérico que describa as características do recurso denominado coas tarefas nas que desexa traballar xerando un equipo despois de atribuirde roles ás tarefas. Aquí atopará a forma de facelo:

1. Na estrutura de subdivisión do traballo, seleccione unha tarefa.
2. Seleccione a icona despregable **Rol atribuído** na cela do recurso.
3. Seleccione o despregable **Rol** e seleccione o rol para o recurso xenérico.
4. Seleccione **Aceptar**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de usar WBS para engadir un recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de pantalla de usar WBS para engadir un recurso")
 
Despois de concluír a atribución de roles para as tarefas en WBS, seleccione **Xerar equipo de proxecto**. Project Service crea o mínimo número de membros do equipo xenéricos baseado nos roles, as unidades de organización de recursos e o calendario do proxecto agregando as atribucións da tarefa.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de xeración do equipo de proxecto](media/FAQ-Resources-to-Tasks2-5.png "Captura de pantalla de xeración do equipo de proxecto")
 
Na grade Membro do equipo, verá os recursos do tipo Recurso xenérico co nome de rol e posición. Se dous recursos necesitan un rol para concluír o traballo, a funcionalidade de Xerar equipo crea dous membros do equipo e utiliza o nome da posición para separalos.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de engadir dous recursos xenéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de pantalla de engadir dous recursos xenéricos")
 
Pode abrir o requisito de recurso de seguranza para o membro do equipo xenérico seleccionando a ligazón en Requisitos de recurso.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de abrir requisito de recurso de respaldo](media/FAQ-Resources-to-Tasks2-7.png "Captura de pantalla de abrir requisito de recurso de respaldo")

Seleccione **Reservar** para o recurso xenérico e, a seguir, pode utilizar o panel de programación para localizar e reservar un recurso real. Tamén pode enviar o requirimento para conclusión por un xestor de recursos seleccionando **Enviar solicitud**.

Cando o recurso xenérico cumple cun recurso denominado, o recurso xenérico elimínase do equipo e as atribucións de tarefa para o recurso xenérico atribúense ao recurso denominado que cumplíu o requisitos de recurso do recurso xenérico.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]