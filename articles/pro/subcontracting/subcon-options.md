---
title: Opcións de subcontratación dos membros do equipo do proxecto
description: Este artigo explica as opcións de subcontratación dos membros do equipo do proxecto en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261604"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opcións de subcontratación dos membros do equipo do proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Microsoft Dynamics 365 Project Operations, pode avaliar as opcións de subcontratación dispoñibles para un ou máis membros do equipo do proxecto. As opcións de subcontratación dispoñibles permítenche:

- Crear un novo subcontrato e/ou crear novas liñas nun subcontrato existente para os membros do equipo do proxecto seleccionados. 
- Reserva contra unha liña de subcontrato e subcontrato xa existente. 

Podes escoller entre as opcións de subcontratación dispoñibles para os membros xenéricos do equipo do proxecto ou escoller entre os membros do equipo do proxecto que contaron cun recurso nomeado que é un traballador por contrato. 

Non hai opcións de subcontratación dispoñibles para os seguintes:

- Membros do equipo do proxecto que contaron cun empregado. 
- Membros do equipo do proxecto que xa estean asociados a unha liña de subcontrato e subcontrato. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto sen persoal

Para revisar e escoller entre as opcións de subcontratación dispoñibles para un membro do equipo do proxecto xenérico ou sen persoal, siga estes pasos:

1. Seleccione un ou máis rexistros de membros do equipo do proxecto onde o recurso sexa un recurso xenérico.
2. Asegúrese de que ningún dos rexistros dos membros do equipo do proxecto seleccionado xa estea subcontratado. 
3. Seleccione **Opcións de subcontratación** na subreixa dos membros do equipo do proxecto. O **Opcións de subcontratación** ábrese o diálogo. 
4. Se só seleccionou un rexistro de membro do equipo do proxecto no paso 1, estarán dispoñibles as seguintes opcións:
    - Crear novas liñas de subcontratación. 
    - Reserva contra un subcontrato existente Se seleccionaches varios rexistros de membros do equipo do proxecto no paso 1, entón a única opción dispoñible é crear liñas de subcontrato novas.
5. A opción de reservar contra unha liña de subcontrato existente permítelle seleccionar unha liña de subcontrato e de subcontratación coa que desexa reservar. Ao seleccionar unha liña de subcontratación para reservar capacidade, debe asegurarse de que a liña de subcontratación seleccionada é para o tempo e de que a función requirida no membro do equipo do proxecto coincide coa función que se comprou na liña de subcontratación.
6. Cando seleccione crear novas liñas de subcontrato para os membros do equipo do proxecto, o sistema permitiralle seleccionar o subcontrato que desexa crear estas liñas. O subcontrato no que selecciones para crear novas liñas debería estar **Borrador** estado. Con esta opción para crear novas liñas de subcontrato para os membros do equipo do proxecto seleccionados, o sistema creará unha liña de subcontrato por tempo para cada membro do equipo do proxecto. A función, as horas e as datas copiaranse do membro do equipo do proxecto a cada liña de subcontratación que se cree. 
7. Cando un membro xenérico do equipo está asociado a unha liña de subcontrato e subcontrato, o **Tipo de traballador** actualizarase o campo da fila xenérica do membro do equipo **Traballador por Contrato** e o **Vixencia do subcontrato** o valor establecerase en **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto

Do mesmo xeito que os membros do equipo xenérico ou sen persoal, tamén podes ver opcións de subcontratación para un membro do equipo do proxecto dotado de persoal sempre que o membro do equipo sexa un traballador por contrato. Para revisar e escoller entre as opcións de subcontratación dispoñibles para un membro do equipo do proxecto con persoal ou nomeado, siga estes pasos:

1. Seleccione un ou máis rexistros de membros do equipo do proxecto onde o recurso sexa un traballador contratado con nome.
2. Asegúrese de que ningún dos rexistros dos membros do equipo do proxecto seleccionados estea xa subcontratado. 
3. Seleccione **Opcións de subcontratación** na subreixa dos membros do equipo do proxecto. O **Opcións de subcontratación** ábrese o diálogo. 
4. Se só seleccionou un rexistro de membro do equipo do proxecto no paso 1, estarán dispoñibles as seguintes opcións:
      - Crear novas liñas de subcontratación.
      - Reserva contra un subcontrato existente.
  Se seleccionou varios rexistros de membros do equipo do proxecto no paso 1, entón a única opción dispoñible é crear liñas de subcontratación novas.
5. A opción de reservar contra unha liña de subcontrato existente permítelle seleccionar unha liña de subcontrato e de subcontratación coa que desexa reservar. Ao seleccionar unha liña de subcontratación para reservar capacidade, debes asegurarte do seguinte:
      - A liña de subcontratación seleccionada é por tempo. 
      - A función necesaria para o membro do equipo do proxecto coincide coa función adquirida na liña de subcontratación. 
      - O provedor ao que está asociado o traballador contratado é o mesmo que o provedor do subcontrato.
6. Cando seleccione crear novas liñas de subcontrato para os membros do equipo do proxecto, o sistema permitiralle seleccionar o subcontrato que desexa crear estas liñas. Con esta opción, debes asegurarte de que o provedor ao que pertence o traballador contratado é o mesmo que o provedor do subcontrato. 
7. O subcontrato no que selecciones para crear novas liñas debería estar **Borrador** estado. Con esta opción para crear novas liñas de subcontrato para os membros do equipo do proxecto seleccionados, o sistema creará unha liña de subcontrato por tempo para cada membro do equipo do proxecto. A función, as horas e as datas copiaranse do membro do equipo do proxecto a cada liña de subcontratación que se cree.  
8. Cando un membro do equipo nomeado está asociado a unha liña de subcontrato e subcontrato, o **Tipo de traballador** actualizarase o campo da fila do membro do equipo nomeado **Traballador por Contrato** e o **Vixencia do subcontrato** o valor establecerase en **Válido**.

## <a name="re-costing-subcontractor-assignments"></a>Recustar as tarefas de subcontratistas

Cando un membro do equipo do proxecto (xenérico ou con nome) está vinculado a liñas de subcontratación mediante o **Opcións de subcontratación** diálogo, calquera asignación de tarefas que teña o membro do equipo volverá custarse en función da lista de prezos de compra adxunta ao subcontrato. No **Estimacións** ficha na **Detalles do proxecto** páxina, seleccione o **Actualizar prezos** botón para ver os prezos e/ou custos actualizados resultantes da decisión de subcontratar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
