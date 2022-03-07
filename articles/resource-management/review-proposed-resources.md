---
title: Revisar os recursos propostos
description: Este tema fornece información sobre como propoñer recursos de proxecto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279271"
---
# <a name="review-proposed-resources"></a>Revisar os recursos propostos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os xestores de recursos poden propoñer un recurso ao xestor de proxectos empregando unha solicitude de recursos.

1. Na grade de solicitudes ou na propia solicitude, seleccione **Buscar recursos**.
2. Na páxina **Asistente de programación**, seleccione o recurso e, a seguir, no panel **Crear reserva de recursos**, no campo **Estado da reserva**, seleccione **Reservar**.

Prodúcense as seguintes actualizacións de estado:

- Na páxina **Asistente de programación**, os indicadores de estado actualízanse para indicar que a reserva é unha proposta, non unha reserva dura.
- Na solicitude do recurso, o estado cambia a **Necesita revisión**.
- No separador **Equipo** do proxecto, o valor **Estado da solicitude** do membro xenérico do equipo, o valor cambiase a **Necesita revisión**.

O responsable do proxecto pode aceptar ou rexeitar a proposta.

Cando os xestores de recursos procesan solicitudes de recursos, poden empregar calquera dos seguintes enfoques:

- Propoñer múltiples recursos para satisfacer a demanda se non se dispón dun recurso único para cumprir as horas requiridas. As horas propostas divídense entre varios recursos que poden satisfacer as horas requiridas. Neste escenario, as horas non se poden solapar.
- Propoñer menos recursos dos necesarios. Neste escenario, a capacidade do recurso proposta é inferior ás horas requiridas que o solicitante especificou. Polo tanto, cando o solicitante acepta os recursos propostos, créase un requisito de recursos non cumpridos para capturar a demanda restante.
- Reserve múltiples recursos para satisfacer a demanda se non dispón dun recurso único para rematar o traballo.
- Reserve menos recursos dos necesarios. Neste escenario, as horas reservadas son menos que as horas requiridas. O sistema guíalle para que propoña recursos en lugar de reservas para que o solicitante poida verificar e rastrexar da demanda restante.

## <a name="resource-availability"></a>Dispoñibilidade de recursos

É fundamental que os xestores de recursos poidan ver a dispoñibilidade de recursos e actualizar as reservas. Nalgúns casos, non hai unha demanda formal (solicitude de recursos), pero un xestor de recursos debe responder a unha demanda non planificada que chega por canles como un correo electrónico, chamada telefónica ou mensaxe instantánea. Os xestores de recursos usan o panel de programación para actualizar recursos e reservas.

As horas laborables do recurso serven como base para calcular a dispoñibilidade dun recurso. As reservas de recursos consumen a capacidade dos recursos.

O panel de programación usa cores e sombreados para amosar reservas, dispoñibilidade e saturacións, e tamén o estado das reservas. Un axuste da configuración do panel de programación permítelle mostrar unha lenda.

Se aparece unha frecha apuntando á dereita xunto a un recurso reservable individual no panel de programación, pódese ampliar o recurso para mostrar detalles do traballo no que está reservado o recurso.

Debido a que Dynamics 365 Project Operations usa o motor de Universal Resource Scheduling, se tamén ten Dynamics 365 Field Service instalado, pode ver os detalles das reservas de recursos para proxectos, pedidos de traballo e calquera outra entidade á que estendeu a programación.

Para ver máis detalles sobre un recurso individual, prema co botón dereito sobre el para abrir a tarxeta do recurso.



[!INCLUDE[footer-include](../includes/footer-banner.md)]