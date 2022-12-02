---
title: Transicións de estado nunha factura de fornecedor
description: Este artigo explica as transicións de estado nunha factura de fornecedor en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261014"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transicións de estado nunha factura de fornecedor

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo explica as transicións de estado nunha factura de fornecedor en Microsoft Dynamics 365 Project Operations. Utilízanse os seguintes estados: **Borrador**, **En revisión**, **Confirmado**, **En espera** e **Cancelado**.

As seguintes ilustracións representan as transicións de estado.

![Modelo de transición de estado de subcontrato,](../media/VI_State_Model.jpg)

A seguinte táboa explica o que cada estado representa no ciclo de vida dunha factura de fornecedor en Project Operations.

| Estado | Descripción | Transicións permitidas |
| --- | --- | --- |
| Esbozo | Este estado é o estado inicial dunha factura de fornecedor. As liñas e os prezos están suxeitos a modificación. Unha factura de fornecedor neste estado se pode editar e eliminar. | En proceso |
| En revisión | Este estado representa o estado de procesamento dunha factura de fornecedor. Polo menos unha liña de factura de fornecedor ten un estado de verificación de **En progreso**. | Confirmada, en espera |
| Confirmado | Este estado representa a fase dunha factura de provedor na que a aplicación creou datos reais de custos para cada liña de factura de fornecedor. Calquera dato real de custo que estivese vinculado ás liñas de factura do fornecedor inverteuse e substituíuse polos datos reais de custo desas liñas de factura do fornecedor. A factura de fornecedor neste estado non se pode editar nin eliminar. Pode usar o botón **Cancelar** para cancelar una factura de fornecedor confirmada. A acción Cancelar inverte o impacto da acción Confirmar. | Cancelado |
| En espera | <p>Este estado representa unha etapa dunha factura de fornecedor na que a factura do fornecedor non se pode mover debido a un problema coa factura ou o estado do fornecedor. A factura de fornecedor neste estado non se pode editar, cancelar, editar nin eliminar.</p><p>Podes usar a acción Volver abrir para mover a factura do fornecedor ao estado **Borrador** ou **En revisión**. Se polo menos unha liña da factura do fornecedor ten un estado de verificación de **En progreso** ou **Completa**, a factura do fornecedor reabrirase no estado **En revisión**. Se todas as liñas da factura do fornecedor teñen un estado de verificación de **Non iniciada**, a factura do fornecedor reabrirase no estado **Borrador**.</p> | Borrador, en revisión |
| Cancelado | Este estado representa a fase dun subcontrato na que a entrega real de materiais e/ou traballo por parte dos recursos subcontratados xa non é necesaria. Non se pode utilizar un subcontrato neste estado para estimar e dotar de persoal os requisitos do proxecto de recursos e materiais nin se pode facer referencia a tempo, gasto e uso de material nun proxecto. Un subcontrato neste estado non se pode editar nin eliminar. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
