---
title: Enviar unha solicitude de recurso
description: Este tema fornece información sobre o envío dunha solicitude dun recurso de proxecto.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 8976ca2360be8676350178059615c59995544a71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282241"
---
# <a name="submitting-a-resource-request"></a>Enviar unha solicitude de recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode enviar un requisito de recurso xerado como solicitude de recurso. A solicitude envíase a un xestor de recursos para o seu cumprimento.

1. En Project Service Automation (PSA), na páxina **Proxectos** prema no separador **Equipo** para ver unha lista de recursos reservables. 
2. Seleccione o recurso xenérico que ten un requisito de recurso da lista e, a seguir, prema en **Enviar solicitude**.

![Enviar unha solicitude de recurso](media/RM-how-to-18.png)

O estado da solicitude de membro xenérico do equipo cambiará a **Enviado**.

Despois de que o xestor de recursos cumpra a solicitude, o recurso xenérico substituirase por un recurso nomeado se o xestor de recursos cumpre a solicitude coa reserva dun recurso nomeado. Se non, o recurso xenérico permanecerá no equipo e o estado da solicitude cambiará a **Necesita revisión**, se o xestor de recursos propuxo un recurso nomeado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]