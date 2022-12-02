---
title: Opcións de subcontratación dos membros do equipo do proxecto
description: Este artigo explica as opcións de subcontratación dos membros do equipo do proxecto en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522276"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opcións de subcontratación dos membros do equipo do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

En Microsoft Dynamics 365 Project Operations, pode avaliar as opcións de subcontratación dispoñibles para un ou máis membros do equipo do proxecto. As opcións de subcontratación dispoñibles permítenlle o seguinte:

- Crear un novo subcontrato e/ou crear novas liñas nun subcontrato existente para os membros do equipo do proxecto seleccionados. 
- Reserve contra unha subcontratación e liña de subcontratación xa existente. 

Podes escoller entre as opcións de subcontratación dispoñibles para os membros xenéricos do equipo do proxecto ou escoller entre os membros do equipo do proxecto que contaron cun recurso nomeado que é un traballador por contrato. 

Non hai opcións de subcontratación dispoñibles para o seguinte:

- Membros do equipo do proxecto que se dotaron cun empregado. 
- Membros do equipo do proxecto que xa están asociados a unha subcontratación ou liña de subcontratación. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto sen persoal

Para revisar e escoller entre as opcións de subcontratación dispoñibles para un membro do equipo do proxecto xenérico ou sen persoal, siga estes pasos:

1. Seleccione un ou máis rexistros de membros do equipo do proxecto cando o recurso sexa un recurso xenérico.
2. Asegúrese de que ningún dos rexistros dos membros do equipo do proxecto seleccionado xa estea subcontratado. 
3. Seleccione **Opcións de subcontratación** na subgrade dos membros do equipo do proxecto. Ábrese a caixa de diálogo **Opcións de subcontratación**. 
4. Se só seleccionou un rexistro de membro do equipo do proxecto no paso 1, estarán dispoñibles as seguintes opcións:
    - Crear novas liñas de subcontratación. 
    - Reserve contra un subcontrato existente. Se seleccionou varios rexistros de membros do equipo do proxecto no paso 1, entón a única opción dispoñible é crear liñas de subcontratación novas.
5. A opción de reservar contra unha liña de subcontratación existente permítelle seleccionar unha subcontratación e unha liña de subcontratación coa que desexa reservar. Ao seleccionar unha liña de subcontratación para reservar capacidade, debe asegurarse de que a liña de subcontratación seleccionada é para o tempo e de que a función requirida para o membro do equipo do proxecto coincide coa función que se comprou na liña de subcontratación.
6. Cando seleccione crear novas liñas de subcontratación para os membros do equipo do proxecto, o sistema permitiralle seleccionar a subcontratación para a que desexa crear estas liñas. O subcontrato que seleccione para crear novas liñas nel debería estar no estado de **Borrador**. Con esta opción para crear novas liñas de subcontratación para os membros do equipo do proxecto seleccionados, o sistema creará unha liña de subcontratación para tempo para cada membro do equipo do proxecto. O rol, as horas e as datas copiaranse do membro do equipo do proxecto a cada liña de subcontratación que se cree. 
7. Cando un membro xenérico do equipo está asociado a unha subcontratación e liña de subcontratación, o campo **Tipo de traballador** na fila do membro xenérico do equipo actualizarase a **Traballador por Contrato** e o valor **Validez do subcontrato** establecerase en **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto con persoal

Do mesmo xeito que os membros do equipo xenéricos ou sen persoal, tamén pode ver opcións de subcontratación para un membro do equipo do proxecto con persoal sempre que o membro do equipo sexa un traballador por contrato. Para revisar e escoller entre as opcións de subcontratación dispoñibles para un membro do equipo do proxecto con persoal ou nomeado, siga estes pasos:

1. Seleccione un ou máis rexistros de membros do equipo do proxecto cando o recurso sexa un traballador por contrato nomeado.
2. Asegúrese de que ningún dos rexistros dos membros do equipo do proxecto seleccionado xa estea subcontratado. 
3. Seleccione **Opcións de subcontratación** na subgrade dos membros do equipo do proxecto. Ábrese a caixa de diálogo **Opcións de subcontratación**. 
4. Se só seleccionou un rexistro de membro do equipo do proxecto no paso 1, estarán dispoñibles as seguintes opcións:
      - Crear novas liñas de subcontratación.
      - Reserve contra un subcontrato existente.
  Se seleccionou varios rexistros de membros do equipo do proxecto no paso 1, entón a única opción dispoñible é crear liñas de subcontratación novas.
5. A opción de reservar contra unha liña de subcontratación existente permítelle seleccionar unha subcontratación e unha liña de subcontratación coa que desexa reservar. Ao seleccionar unha liña de subcontratación para reservar capacidade, debe asegurarse do seguinte:
      - A liña de subcontratación seleccionada é para tempo. 
      - O rol necesario para o membro do equipo do proxecto coincide co rol adquirido na liña de subcontratación. 
      - O fornecedor ao que está asociado o traballador contratado é o mesmo que o fornecedor do subcontrato.
6. Cando seleccione crear novas liñas de subcontratación para os membros do equipo do proxecto, o sistema permitiralle seleccionar a subcontratación para a que desexa crear estas liñas. Con esta opción, debe asegurarse de que o fornecedor ao que pertence o traballador por contrato é o mesmo que o fornecedor do subcontrato. 
7. O subcontrato que seleccione para crear novas liñas nel debería estar no estado de **Borrador**. Con esta opción para crear novas liñas de subcontratación para os membros do equipo do proxecto seleccionados, o sistema creará unha liña de subcontratación para tempo para cada membro do equipo do proxecto. O rol, as horas e as datas copiaranse do membro do equipo do proxecto a cada liña de subcontratación que se cree.  
8. Cando un membro nomeado do equipo está asociado a unha subcontratación e liña de subcontratación, o campo **Tipo de traballador** na fila do membro nomeado do equipo actualizarase a **Traballador por Contrato** e o valor **Validez do subcontrato** establecerase en **Válido**.

## <a name="re-costing-subcontractor-assignments"></a>Volver determinar os custos das atribucións de subcontratistas

Cando un membro do equipo do proxecto (xenérico ou nomeado) está vinculado a liñas de subcontratación mediante o diálogo **Opcións de subcontratación**, calquera atribución de tarefas que teña o membro do equipo volverá a calcularse en función da lista de prezos de compra anexa ao subcontrato. No separador **Estimacións** da páxina **Detalles do proxecto**, seleccione o botón **Actualizar prezos** para ver os prezos e/ou custos actualizados resultantes da decisión de subcontratar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
