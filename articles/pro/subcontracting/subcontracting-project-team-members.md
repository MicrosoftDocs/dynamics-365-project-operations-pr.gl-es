---
title: Subcontratación dos membros do equipo do proxecto
description: Este artigo explica como subcontratar membros do equipo do proxecto en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 649687cb9ac66e684069434a353b63155103aefb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916884"
---
# <a name="subcontracting-project-team-members"></a>Subcontratación dos membros do equipo do proxecto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Microsoft Dynamics 365 Project Operations, pode optar por subcontratar membros do equipo do proxecto sen persoal ou con persoal.

- Os membros do equipo do proxecto sen persoal teñen asignado un recurso xenérico.
- Os membros do equipo de persoal teñen asignado un recurso nomeado.

Cando vinculas un membro do equipo do proxecto a unha liña de subcontrato, todas as asignacións ás tarefas que teña o membro do equipo serán revalorizadas en función da lista de prezos de compra adxunta ao subcontrato.  No **Estimacións** ficha na **Detalles do proxecto** páxina, seleccione o **Actualizar prezos** botón para ver os prezos e/ou custos actualizados resultantes da decisión de subcontratar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto sen persoal
O **Detalles dos membros do equipo** A páxina ten campos de subcontrato e liña de subcontrato que permiten a un xestor de proxecto expresar como lle gustaría obter a capacidade necesaria dun subcontrato. Para subcontratar un membro do equipo do proxecto como recurso xenérico, siga estes pasos:

1.  Escolle un subcontrato no **Detalle do membro do equipo** páxina.

2.  Só pode seleccionar subcontratos con **Borrador** ou **Confirmado** estado. **Pechado** ou **Cancelado** non se poden seleccionar subcontratos. 

3.  O **Liña de subcontratación** o campo faise visible despois de seleccionar un subcontrato.

4.  No **Liña de subcontratación** campo, só pode seleccionar liñas de subcontratación que sexan por tempo. Non pode seleccionar liñas de subcontratación para gastos ou material.

5.  A función do rexistro do membro do equipo do proxecto debe coincidir coa función da liña de subcontrato. Isto garante que o tempo para o papel que se está a estimar no proxecto sexa o mesmo que se adquire na liña de subcontratación. 

Cando un membro xenérico do equipo está asociado a unha liña de subcontrato e subcontrato, o **Tipo de traballador** actualizarase o campo da fila xenérica do membro do equipo **Traballador por Contrato** e **Vixencia do subcontrato** establecerase en **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto
Do mesmo xeito que os membros do equipo xenérico ou sen persoal, a capacidade dos membros do equipo necesario para un proxecto tamén se pode vincular a un subcontrato. Para subcontratar un membro do equipo do proxecto, siga estes pasos:

1.  Asegúrese de que o recurso nomeado está configurado como un tipo de recurso reservable de traballador contratado. Ademais, asegúrese de que o **Vendedor** o campo do recurso reservable coincide co provedor do subcontrato que está seleccionando. 

2.  Só pode seleccionar subcontratos en **Borrador** ou **Confirmado** estado. **Pechado** ou **Cancelado** non se poden seleccionar subcontratos. 

3.  O **Liña de subcontratación** o campo faise visible despois de seleccionar un subcontrato.

4.  No **Liña de subcontratación** campo, só pode seleccionar liñas de subcontratación que sexan por tempo. Non pode seleccionar liñas de subcontratación para gastos ou material.

5.  A función do rexistro do membro do equipo do proxecto debe coincidir coa función da liña de subcontrato. Isto garante que o tempo para o papel que se está a estimar no proxecto sexa o mesmo que se adquire na liña de subcontratación. 

Nomeados membros do equipo do proxecto que están configurados como un tipo de traballador contratado **Recurso reservable** mostrarase cun estado de validez de subcontrato de **Non válido** se non están vinculados a un subcontrato. Cando un membro do equipo do proxecto nomeado está asociado cunha liña de subcontrato e subcontrato, o **Tipo de traballador** campo da fila de membro do equipo actualizarase a **Traballador por Contrato** e **Vixencia do subcontrato** establecerase en **Válido**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
