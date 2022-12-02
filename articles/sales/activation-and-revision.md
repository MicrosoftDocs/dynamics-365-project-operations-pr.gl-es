---
title: Activar e revisar unha oferta de proxecto
description: Este artigo ofrece información sobre como activar e revisar ofertas en Microsoft Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Activar e revisar unha oferta de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As capacidades de activación e revisión axúdanlle a realizar un seguimento das versións das ofertas baseadas en proxectos durante as fases de estimación e negociación. Cando se activa un borrador dunha oferta, pasa a ser de só lectura.

As capacidades de activación e revisión permítenlle realizar as seguintes tarefas:

- Gañar ou perder ofertas só despois da activación.
- Revisar unha oferta para facer cambios na oferta existente ou crear unha nova versión.

> [!NOTE]
> Despois de activar a funcionalidade de activación e revisión de ofertas, non se pode desactivar.

Para activar a capacidade de activar e revisar ofertas baseadas en proxectos, siga estes pasos.

1. Vaia a **Configuración** \> **Parámetros**.
1. Abra o rexistro **Parámetros**.
1. No panel de Acción, no separador **Control de funcionalidades**, seleccione **Activar a activación e revisión de ofertas**.
1. Na caixa de diálogo de confirmación, seleccione **Aceptar**.
1. Despois duns momentos, actualice o navegador. Agora deberían estar dispoñibles as capacidades de activación e revisión. Saberá que estas capacidades foron habilitadas se o botón **Activa a activación e a revisión de ofertas** xa non aparece no panel Acción.

## <a name="activating-a-quote"></a>Activación dunha oferta

Despois de activar a funcionalidade de activación e revisión de ofertas, os botóns **Pechar oferta como gañada** e **Pechar oferta como perdida** do panel de Acción non están dispoñibles para os borradores de ofertas do proxecto. Só están dispoñibles despois de que se active unha oferta.

A activación representa a etapa do proceso de cotización na que se queren evitar máis cambios na oferta. Nesta fase, a oferta envíase para revisión interna ou ao cliente.

Os botóns **Pechar oferta como gañada** e **Pechar oferta como perdida** do panel de Acción están dispoñibles para as ofertas activadas. Dependendo do resultado da revisión interna ou do cliente, pode usar un destes botóns para pechar unha oferta activada. Pode facer negociacións e cambios nas ofertas activadas seleccionando **Revisar oferta**.

## <a name="revising-a-quote"></a>Revisión dunha oferta

Se debe facer cambios nunha oferta activada, seleccione **Revisar oferta**. A oferta está pechada, e utilízase o código de motivo **revisado**. A seguir, créase unha nova oferta que ten o mesmo ID e un número de revisión incrementado. Todos os detalles da oferta orixinal cópianse na nova oferta. A nova oferta está en estado de borrador e pódese editar segundo sexa necesario.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
