---
title: Revisar os recursos propostos
description: Este artigo ofrece información sobre como propoñer recursos do proxecto.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183972"
---
# <a name="review-proposed-resources"></a>Revisar os recursos propostos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os xestores de recursos poden propoñer un recurso ao xestor de proxectos empregando unha solicitude de recursos.

Para revisar os recursos propostos, siga estes pasos:

1. Na grade **Solicitude** ou na propia solicitude, seleccione **Buscar recursos**.
2. Na páxina **Asistente de programación**, seleccione o recurso e logo confirme que todas as horas propostas están incluídas na reserva proposta.
3. No panel **Crear reserva de recursos**, configure o campo **Estado da reserva** en **Proposta** e, a seguir, seleccione **Reservar**.

    > [!NOTE]
    > Configurar o **Estado da reserva** en **Proposta** non reserva o recurso e non substitúe o recurso xenérico polo membro do equipo nomeado.

    Prodúcense as seguintes actualizacións de estado:

    - Na páxina **Asistente de programación**, os indicadores de estado actualízanse para indicar que a reserva é unha proposta, non unha reserva dura.
    - Na solicitude de recurso, o revisor da solicitude debe cambiar o estado a **Necesita revisión**.
    - No **Equipo** ficha do proxecto, a do membro xenérico do equipo **Estado da solicitude** o valor cámbiase automaticamente a **Necesita revisión**.

O responsable do proxecto pode aceptar ou rexeitar a proposta.

Cando os xestores de recursos procesan solicitudes de recursos, poden empregar calquera dos seguintes enfoques:

- Propoñer múltiples recursos para satisfacer a demanda se non se dispón dun recurso único para cumprir as horas requiridas. As horas propostas divídense entre varios recursos que poden satisfacer as horas requiridas. Neste escenario, as horas non se poden solapar.
- Propoñer menos recursos dos necesarios. Neste escenario, a capacidade do recurso proposta é inferior ás horas requiridas que o solicitante especificou. Cando o solicitante acepta os recursos propostos, créase un requisito de recursos non cumpridos para capturar a demanda restante.
- Reserve múltiples recursos para satisfacer a demanda se non dispón dun recurso único para rematar o traballo.
- Reserve menos recursos dos necesarios. Neste escenario, as horas reservadas son menos que as horas requiridas. O sistema guíalle para que propoña recursos en lugar de reservas para que o solicitante poida verificar e rastrexar da demanda restante.

## <a name="resource-availability"></a>Dispoñibilidade de recursos

Os xestores de recursos deben poder ver a dispoñibilidade de recursos e actualizar as reservas. Nalgúns casos, non hai demanda formal (solicitude de recursos). Non obstante, un xestor de recursos debe responder a unha demanda non planificada que chega a través doutras canles como correos electrónicos, chamadas telefónicas ou mensaxes instantáneas. Os xestores de recursos usan o **Panel de programación** para actualizar recursos e reservas.

As horas laborables do recurso serven como base para calcular a dispoñibilidade dun recurso. As reservas de recursos consumen a capacidade dos recursos.

O **Panel de programación** usa cores e sombreados para amosar reservas, dispoñibilidade e saturacións, e tamén o estado das reservas. Un axuste no **Panel de programación** permite amosar unha lenda.

Se aparece unha frecha apuntando á dereita xunto a un recurso reservable individual no **Panel de programación**, pódese ampliar o recurso para mostrar detalles do traballo no que está reservado o recurso.

Debido a que Dynamics 365 Project Operations usa o motor de Universal Resource Scheduling, se tamén ten Dynamics 365 Field Service instalado, pode ver os detalles das reservas de recursos para proxectos, pedidos de traballo e calquera outra entidade á que estendeu a programación.

Para ver detalles adicionais sobre un recurso individual, prema co botón dereito sobre el para abrir a tarxeta do recurso.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
