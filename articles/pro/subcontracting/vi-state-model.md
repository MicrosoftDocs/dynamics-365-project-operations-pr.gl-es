---
title: Transicións de estado nunha factura de fornecedor
description: Este artigo explica as transicións de estado nunha factura de provedor en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934318"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transicións de estado nunha factura de fornecedor

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo explica as transicións de estado nunha factura de provedor en Microsoft Dynamics 365 Project Operations. Utilízanse os seguintes estados: **Borrador**, **revisión**, **·**, **espera**, e **Cancelado**.

As seguintes ilustracións mostran as transicións de estado.

![Modelo de transición de estados de subcontratación.](../media/VI_State_Model.jpg)

A seguinte táboa explica o que representa cada estado no ciclo de vida dunha factura de provedor en Project Operations.

| Estado | Descripción | Transicións permitidas |
| --- | --- | --- |
| Esbozo | Este estado é o estado inicial dunha factura de provedor. As liñas e os prezos están suxeitos a modificación. Pódese editar e eliminar unha factura de provedor neste estado. | En proceso |
| En revisión | Este estado representa o estado de procesamento dunha factura de provedor. Polo menos unha liña de factura de provedor ten un estado de verificación de **En progreso**. | Confirmado, en espera |
| Confirmado | Este estado representa a fase dunha factura de provedor na que a aplicación creou custos reais para cada liña de factura de provedor. Calquera reais de custo vinculado que se relacionase coas liñas de factura do provedor invertéronse e substituíronse polos reais de custo desas liñas de factura do provedor. Non se pode editar nin eliminar unha factura de provedor neste estado. Podes usar o **Cancelar** botón para cancelar una factura de proveedor confirmada. A acción Cancelar inverte o impacto da acción Confirmar. | Cancelado |
| En espera | <p>Este estado representa unha etapa dunha factura de provedor na que a factura do provedor non se pode mover debido a un problema coa factura ou o estado do provedor. Non se pode confirmar, cancelar, editar nin eliminar unha factura de provedor neste estado.</p><p>Podes usar a acción Volver abrir para mover a factura do provedor ao **Borrador** ou **En revisión** estado. Se polo menos unha liña da factura do provedor ten un estado de verificación de **En progreso** ou **Completa**, a factura do provedor reabrirase no **En revisión** estado. Se todas as liñas da factura do provedor teñen un estado de verificación de **Non comezou**, a factura do provedor reabrirase no **Borrador** estado.</p> | Borrador, En revisión |
| Cancelado | Este estado representa a fase dun subcontrato na que xa non se require a entrega real de materiais e/ou traballo por parte dos recursos subcontratados. Un subcontrato neste estado non se pode utilizar para estimar e empregar os requisitos do proxecto para recursos e materiais, e tampouco se pode facer referencia ao tempo, aos gastos e ao uso do material nun proxecto. Non se pode editar nin eliminar un subcontrato neste estado. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
