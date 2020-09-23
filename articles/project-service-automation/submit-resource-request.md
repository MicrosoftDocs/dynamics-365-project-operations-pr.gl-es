---
title: Enviar unha solicitude de recurso
description: Este tema fornece información sobre o envío dunha solicitude dun recurso de proxecto.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751431"
---
# <a name="submit-a-resource-request"></a>Enviar unha solicitude de recurso

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode enviar un requisito de recurso xerado como solicitude de recurso. A solicitude envíase a un xestor de recursos para o seu cumprimento.

1. En Project Service Automation (PSA), na páxina **Proxectos** prema no separador **Equipo** para ver unha lista de recursos reservables. 
2. Seleccione o recurso xenérico que ten un requisito de recurso da lista e, a seguir, prema en **Enviar solicitude**.

![Enviar unha solicitude de recurso](media/RM-how-to-18.png)

O estado da solicitude de membro xenérico do equipo cambiará a **Enviado**.

Despois de que o xestor de recursos cumpra a solicitude, o recurso xenérico substituirase por un recurso nomeado se o xestor de recursos cumpre a solicitude coa reserva dun recurso nomeado. Se non, o recurso xenérico permanecerá no equipo e o estado da solicitude cambiará a **Necesita revisión**, se o xestor de recursos propuxo un recurso nomeado.
