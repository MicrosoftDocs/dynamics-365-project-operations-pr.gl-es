---
title: Crear unha reserva de proxecto desde o panel de programación
description: Este tema fornece información sobre como crear unha reserva de proxecto desde o panel de programación.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146526"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Crear unha reserva de proxecto desde o panel de programación

[!include [banner](../includes/psa-now-project-operations.md)]

Pode reservar un recurso nun proxecto directamente no separador de **Equipo** do proxecto ou xerando un requisito de recursos desde unha atribución de membro de equipo xenérico e, a seguir, cumprir os requisitos xerados cun membro do equipo de proxecto.

Tamén pode reservar un recurso nun proxecto directamente desde o panel de programación. Hai tres xeitos de facer isto:

- **Reservar desde un requirimento de recurso xerado:** Pode xerar un requisito de recurso despois de crear un recurso xenérico e asignar tarefas dentro dun proxecto.

- **Reservar desde o requisito principal:** Os requisitos principais aparecen no panel de programación do separador **Proxecto**. 

- **Reservar desde un novo requisito de recurso:** Pode crear un requisito de recurso dende cero e asocialo a un proxecto. No panel de programación, o requisito de recurso aparece no separador **Requisitos abertos**.

## <a name="book-from-a-generated-resource-requirement"></a>Reservar desde un requisito de recurso xerado.

Pode crear un recurso xenérico e atribuílo a unha ou máis tarefas dentro dun proxecto. A seguir, pode xerar un requisito de recurso desde o membro do equipo xenérico. 

1.  No panel de programación, este recurso aparecerá no separador **Requisitos abertos**. É posible que necesite utilizar filtros de columnas na grade se ten moitos requisitos abertos. 

    ![Abrir o separador Requisitos no panel Programación](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura da táboa de reservas e atribucións")

2. Seleccione o requisito. O separador **Buscar dispoñibilidade** aparecerá na parte superior da fila seleccionada.
 
3. Cando selecciona o separador, ábrese o modo Asistente de programación do panel de programación e filtra os recursos dispoñibles que cumpren o requisito do recurso. Despois diso, pode reservar un recurso.

4. Tamén pode arrastrar e soltar a fila seleccionada na parte inferior do panel de programación a unha cela de recurso na grade de arriba. Cando o solte, isto are o panel **Crear reserva de recurso** á dereita.

    Seleccionar **Reserva** reserva o recurso no equipo de proxecto.

![Panel Crear reserva de recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Reservar desde o requisito principal

Crear un proxecto en Project Service crea automaticamente un requisito de recurso denominado Requisito principal. Isto é un requisito baleiro utilizado para reservar rapidamente un recurso co panel de programación sen xerar un requisito nin crear un desde cero. Debido a que o requisito está baleiro, ten que especificar as datas, así como o método de atribución e as horas, se corresponde. 

1. Para reservar un recurso con Requisito principal no panel de programación, seleccione o separador **Proxecto**. Se ten moitos proxectos, é posible que teña que utilizar o filtro de columna na columna **Proxecto**.

   ![Filtros de columna no panel Programación](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura da táboa de reservas e atribucións")

2. Seleccione o requisito que só se ten o nome de proxecto como o seu nome e ten unha duración de cero (0).

3. Seleccione o separador **Buscar dispoñibilidade** que aparece na fila. Isto pon o panel de programación no modo de Asistente de programación e mostra os recursos dispoñibles que se poden reservar no proxecto.

4. Debido a que o **Requisito principal** é un requisito baleiro con duración cero (0), deberá definir a duración no panel **Crear reserva de recurso** cando seleccione e reserve un recurso.

5. Tamén pode seleccionar o **Requisito principal do proxecto** da parte inferior do panel de programación e arrastralo e soltalo nun recurso para reservalo.
 
    Debido a que o **Requisito principal** é un requisito baleiro con duración cero (0), deberá definir a duración no panel **Crear reserva de recurso** cando seleccione e reserve un recurso.
 
    Cando reserva un recurso a través do **Requisito principal** no panel de programación, engadeo ao equipo de proxecto sen ningunha atribución.
 
## <a name="book-from-a-new-resource-requirement"></a>Reservar desde un novo requisito de recurso.
Complete os seguintes pasos para reservar a partir dun novo requisito de recursos. 

1. Vaia á **Requisitos de recursos** e, a seguir, seleccione **Novo** para crear un novo requisito de recurso.

2. No separador **Proxecto**, seleccione un proxecto para asociar o requisito ao proxecto.
 
    No panel de programación, este novo requisito creado recentemente móstrase como **Requisito aberto** que pode realizar.

3. Reserve o recurso para engadilo ao equipo de proxecto.

4. Agora que o recurso está reservado, debe atribuír tarefas manualmente.

