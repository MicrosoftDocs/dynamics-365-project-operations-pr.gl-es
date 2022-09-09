---
title: Activar e revisar unha cotización de proxecto
description: Este artigo ofrece información sobre como activar e revisar presupostos en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410365"
---
# <a name="activate-and-revise-a-project-quote"></a>Activar e revisar unha cotización de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As capacidades de activación e revisión axúdanche a realizar un seguimento das versións das cotizacións baseadas en proxectos durante as fases de estimación e negociación. Cando se activa un borrador dunha cita, pasa a ser de só lectura.

As capacidades de activación e revisión permítenche realizar as seguintes tarefas:

- Gaña ou perda presupostos só despois da activación.
- Revisa unha cotización para facer cambios na cotización existente ou crear unha nova versión.

> [!NOTE]
> Despois de activar a función de activación e revisión de comiñas, non se pode desactivar.

Para activar a capacidade de activar e revisar presupostos baseados en proxectos, siga estes pasos.

1. Ir a **Configuración** \> **Parámetros**.
1. Abre o **Parámetros** rexistro.
1. No panel de accións, no **Control de funcións** ficha, seleccione **Activa a activación e revisión de comiñas**.
1. Na caixa de diálogo de confirmación, seleccione **Aceptar**.
1. Despois duns momentos, actualice o navegador. Agora deberían estar dispoñibles as capacidades de activación e revisión. Sabrá que estas capacidades foron habilitadas se o **Activa a activación e a revisión das cotizacións** o botón xa non aparece no Panel de accións.

## <a name="activating-a-quote"></a>Activando unha cotización

Despois de activar a función de activación e revisión de comiñas, o **Pechar cita como gañada** e **Pechar cita como perdida** os botóns do Panel de accións non están dispoñibles para os borradores do proxecto. Só están dispoñibles despois de que se active unha cotización.

A activación representa a etapa do proceso de cotización na que se quere evitar máis cambios na cotización. Nesta fase, a cotización envíase para revisión interna ou ao cliente.

O **Pechar cita como gañada** e **Pechar cita como perdida** os botóns do Panel de accións están dispoñibles para as cotizacións activadas. Dependendo do resultado da revisión interna ou do cliente, pode usar un destes botóns para pechar unha cotización activada. Podes facer negociacións e cambios nas cotizacións activadas seleccionando **Revisar cotización**.

## <a name="revising-a-quote"></a>Revisando unha cotización

Se debes facer cambios nunha cotización activada, selecciona **Revisar cotización**. A cita está pechada, e o **revisado** úsase o código motivo. A continuación, créase unha nova cotización que teña o mesmo ID e un número de revisión incrementado. Todos os detalles da cita orixinal cópiase na nova cita. A nova cotización está en estado de borrador e pódese editar segundo sexa necesario.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
