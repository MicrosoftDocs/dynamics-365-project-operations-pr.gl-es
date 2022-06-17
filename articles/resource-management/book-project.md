---
title: Reserva a un proxecto
description: Este artigo ofrece información sobre como reservar un recurso para un proxecto.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928522"
---
# <a name="book-to-a-project"></a>Reserva a un proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Hai ocasións nas que un xestor de proxectos ou un xestor de recursos necesitará asignar un recurso a un proxecto sen que un membro do equipo xenérico defina un requisito específico. Isto pódese conseguir de tres formas.

- Reservar desde a grade de membro do equipo
- Reservar desde o panel de programación
- Reservar desde o formulario **Project**

## <a name="book-from-the-team-member-grid"></a>Reservar desde a grade de membro do equipo

Se a súa organización opera en modo híbrido de asignación de recursos, o xestor de proxectos pode reservar un recurso directamente no proxecto completando os seguintes pasos.

1. No proxecto, vai á grade dos membros do equipo e seleccione **Novo**.
2. Definir o nome do posto e o rol do recurso.
3. Seleccione o recurso reservable na busca dispoñible.
4. Despois de seleccionar o recurso, defina a información dos seguintes campos para reservar o recurso:

    - Data de inicio
    - Data de finalización
    - Método de atribución
    - Horas, se procede
    - Responsable da aprobación do proxecto

6. Seleccione **Gardar e pechar**

## <a name="book-from-the-schedule-board"></a>Reservar desde o panel de programación

Cando un xestor de recursos necesita reservar un recurso directamente nun proxecto, pode usar o cadro de programación e o requisito do proxecto. O requisito do proxecto é un requisito de recursos que sempre está dispoñible para ser reservado. Complete os seguintes pasos para facer unha reserva directamente a un proxecto desde o panel de programación.

1. Desprácese ata o panel de programación e, na páxina esquerda, filtre os recursos que está considerando para o requisito.
2. No panel inferior, seleccione o separador **Proxecto** para ver unha lista dos requisitos do proxecto.
3. Arrastre o requisito a un recurso e defina a seguinte información:

    - Data de inicio
    - Data de finalización
    - Estado da reserva
    - Método de reserva
    - Duración
   
   > [!NOTE]
   > Actualmente,Dynamics 365 Project Operations non admite o taboleiro de programación.   

## <a name="book-from-the-project-form"></a>Reservar desde o formulario Proxecto

Como xestor de proxectos, é posible que necesite reservar un recurso para un proxecto, pero só coñece os criterios e non o nome do recurso. Complete os seguintes pasos para usar o asistente de programación para atopar un recurso baseado en calquera atributo dispoñible do recurso. 

1. Desprácese ata o proxecto e seleccione **Reservar** para abrir o asistente de programación.
2. Usando os filtros da parte esquerda do asistente de programación, restrinxa os criterios e seleccione **Buscar.**
3. En función dos recursos devoltos nos resultados, pode reservar un recurso.

> [!NOTE]
> Este método non crea ningunha reserva para o recurso. No seu lugar, engade o recurso ao equipo. Despois de engadir o membro do equipo ao proxecto, o xestor do proxectos pode usar manter as reservas ou ampliar as reservas para engadir as reservas requiridas ao recurso.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
