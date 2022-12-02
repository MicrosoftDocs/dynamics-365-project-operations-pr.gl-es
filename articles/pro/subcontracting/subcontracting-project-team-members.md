---
title: Subcontratación dos membros do equipo do proxecto
description: Este artigo explica como subcontratar membros do equipo do proxecto en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522793"
---
# <a name="subcontracting-project-team-members"></a>Subcontratación dos membros do equipo do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

En Microsoft Dynamics 365 Project Operations, pode optar por subcontratar membros do equipo do proxecto sen persoal ou con persoal.

- Os membros do equipo do proxecto sen persoal teñen asignado un recurso xenérico.
- Os membros do equipo de persoal teñen asignado un recurso nomeado.

Cando vincula un membro do equipo do proxecto a unha liña de subcontratación, as asignacións ás tarefas que teña o membro do equipo calcularanse en función da lista de prezos de compra anexa ao subcontrato.  No separador **Estimacións** da páxina **Detalles do proxecto**, seleccione o botón **Actualizar prezos** para ver os prezos e/ou custos actualizados resultantes da decisión de subcontratar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto sen persoal
A páxina **Detalles dos membros do equipo** ten campos de subcontratación e liña de subcontratación que permiten a un xestor de proxecto expresar como lle gustaría obter a capacidade necesaria dun subcontrato. Para subcontratar un membro do equipo do proxecto como recurso xenérico, siga estes pasos:

1.  Escolla un subcontrato na páxina **Detalle do membro do equipo**.

2.  Só pode seleccionar subcontratos cun estado de **Borrador** ou **Confirmado**. Os subcontrato con estado **Pechado** ou **Cancelado** non se poden seleccionar. 

3.  O campo **Liña de subcontratación** faise visible despois de seleccionar un subcontrato.

4.  No campo **Liña de subcontratación**, só pode seleccionar liñas de subcontratación que sexan para tempo. Non pode seleccionar liñas de subcontratación para gastos ou material.

5.  O rol do rexistro do membro do equipo do proxecto debe coincidir co rol da liña de subcontratatación. Isto garante que o tempo para o rol que se está a estimar no proxecto sexa o mesmo que se adquire na liña de subcontratación. 

Cando un membro xenérico do equipo está asociado a unha subcontratación e liña de subcontratación, o campo **Tipo de traballador** na fila do membro xenérico do equipo actualizarase a **Traballador por Contrato** e **Validez do subcontrato** establecerase en **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratación dun membro do equipo do proxecto con persoal
Do mesmo xeito que os membros do equipo xenéricos ou sen persoal, a capacidade dos membros do equipo necesaria para un proxecto tamén se pode vincular a un subcontrato. Para subcontratar un membro do equipo do proxecto nomeado, siga estes pasos:

1.  Asegúrese de que o recurso nomeado está configurado como un tipo de recurso reservable de traballador contratado. Ademais, asegúrese de que o campo **Fornecedor** do recurso reservable coincide co fornecedor do subcontrato que está seleccionando. 

2.  Só pode seleccionar subcontratos en estado de **Borrador** ou **Confirmado**. Os subcontrato con estado **Pechado** ou **Cancelado** non se poden seleccionar. 

3.  O campo **Liña de subcontratación** faise visible despois de seleccionar un subcontrato.

4.  No campo **Liña de subcontratación**, só pode seleccionar liñas de subcontratación que sexan para tempo. Non pode seleccionar liñas de subcontratación para gastos ou material.

5.  O rol do rexistro do membro do equipo do proxecto debe coincidir co rol da liña de subcontratatación. Isto garante que o tempo para o rol que se está a estimar no proxecto sexa o mesmo que se adquire na liña de subcontratación. 

Os membros do equipo do proxecto nomeados que están configurados como un tipo de traballador contratado **Recurso reservable** mostrarase cun estado de validez de subcontrato de **Non válido** se non están vinculados a un subcontrato. Cando un membro do equipo do proxecto nomeado está asociado a unha subcontratación e liña de subcontratación, o campo **Tipo de traballador** na fila do membro xenérico do equipo actualizarase a **Traballador por Contrato** e **Validez do subcontrato** establecerase en **Válido**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
