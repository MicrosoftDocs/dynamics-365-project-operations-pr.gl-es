---
title: Transicións de estado nun subcontrato
description: Este tema explica as transicións de estado nun subcontrato en Microsoft Dynamics 365 Project Operations a medida que se crea, executa e pecha o subcontrato.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c9533d046398c708c55467e6b1a25acf6abade3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579166"
---
# <a name="state-transitions-on-a-subcontract"></a>Transicións de estado nun subcontrato 

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este tema explica as transicións de estado nun subcontrato en Microsoft Dynamics 365 Project Operations. Cada estado represéntase como borrador, confirmado, pechado ou cancelado. A seguinte imaxe representa as transicións de estado.

![Modelo de estado de subcontratación](../media/SubconStates.png)  

A seguinte táboa ofrece unha descrición do que cada estado representa no ciclo de vida dun subcontrato en Operacións do Proxecto.

| Estado | Descripción | Transicións permitidas |
| --- | --- | --- |
| Esbozo | Isto representa o estado inicial dun subcontrato. As negociacións co vendedor están en curso. As liñas e os prezos están suxeitos a modificacións. Un subcontrato neste estado pódese utilizar para estimar e empregar os requisitos do proxecto de recursos e materiais. Tamén se pode facer referencia ao tempo, aos gastos e ao uso do material nun proxecto. Un subcontrato neste estado pódese editar e eliminar. | Confirmado |
| Confirmado | Isto representa a fase dun subcontrato despois de que se completen as negociacións co provedor sobre os prezos e as liñas que se compran. Non obstante, a entrega real de materiais e/ou traballos por parte de recursos subcontratados aínda está en curso. Un subcontrato neste estado pódese utilizar para estimar e empregar os requisitos do proxecto de recursos e materiais. Tamén se pode facer referencia ao tempo, aos gastos e ao uso do material nun proxecto. Non se pode editar nin eliminar un subcontrato neste estado. O **Cancelar** botón permítelle cancelar un subcontrato confirmado. O **Volver a abrir** botón permítelle reabrir o subcontrato para devolvelo **Borrador** estado. Usa o **Pechar** botón para pechar un subcontrato confirmado. | Pechadas <br> Cancelado <br> Esbozo |
| Pechadas | Isto representa a fase dun subcontrato na que se completa a entrega real de materiais e/ou traballo por parte dos recursos subcontratados. Un subcontrato neste estado xa non se pode utilizar para estimar e dotar de recursos e materiais do proxecto. Ademais, xa non se pode facer referencia a tempo, gasto e uso de material nun proxecto. Non se pode editar nin eliminar un subcontrato neste estado. | Nada |
| Cancelado | Isto representa a fase dun subcontrato na que xa non é necesaria a entrega real de materiais e/ou traballo por parte dos recursos subcontratados. Non se pode utilizar un subcontrato neste estado para estimar e empregar os requisitos do proxecto de recursos e materiais nin se pode facer referencia a tempo, gasto e uso de material nun proxecto. Non se pode editar nin eliminar un subcontrato neste estado. | Nada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
