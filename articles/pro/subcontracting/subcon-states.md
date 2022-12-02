---
title: Transicións de estado nun subcontrato
description: Este artigo explica as transicións de estado nun subcontrato en Microsoft Dynamics 365 Project Operations a medida que se crea, executa e pecha o subcontrato.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522931"
---
# <a name="state-transitions-on-a-subcontract"></a>Transicións de estado nun subcontrato 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Este artigo explica as transicións de estado nun subcontrato en Microsoft Dynamics 365 Project Operations. Cada estado represéntase como borrador, confirmado, pechado ou cancelado. A seguinte imaxe representa as transicións de estado.

![Modelo de estado de subcontratación](../media/SubconStates.png)  

A seguinte táboa ofrece unha descrición do que cada estado representa no ciclo de vida dun subcontrato en Project Operations.

| Estado | Descripción | Transicións permitidas |
| --- | --- | --- |
| Esbozo | Isto representa o estado inicial dun subcontrato. As negociacións co fornecedor están en curso. As liñas e os prezos están suxeitos a modificacións. Un subcontrato neste estado pódese utilizar para estimar e empregar os requisitos do proxecto de recursos e materiais. Tamén se pode facer referencia a tempo, gasto e uso de material nun proxecto. Un subcontrato neste estado pódese editar e eliminar. | Confirmado |
| Confirmado | Isto representa a fase dun subcontrato despois de que se completen as negociacións co fornecedor sobre os prezos e os elementos de liña que se compran. Non obstante, a entrega real de materiais e/ou traballos por parte de recursos subcontratados aínda está en curso. Un subcontrato neste estado pódese utilizar para estimar e empregar os requisitos do proxecto de recursos e materiais. Tamén se pode facer referencia a tempo, gasto e uso de material nun proxecto. Un subcontrato neste estado non se pode editar nin eliminar. O botón **Cancelar** permítelle cancelar un subcontrato confirmado. O botón **Volver a abrir** permítelle reabrir o subcontrato para devolvelo ao estado **Borrador**. Use o botón **Pechar** para pechar un subcontrato confirmado. | Pechadas <br> Cancelado <br> Esbozo |
| Pechadas | Isto representa a fase dun subcontrato na que se completa a entrega real de materiais e/ou traballo por parte dos recursos subcontratados. Un subcontrato neste estado xa non se pode utilizar para estimar e empregar os requisitos do proxecto de recursos e materiais. Ademais, xa non se pode facer referencia a tempo, gasto e uso de material nun proxecto. Un subcontrato neste estado non se pode editar nin eliminar. | Nada |
| Cancelado | Isto representa a fase dun subcontrato na que a entrega real de materiais e/ou traballo por parte dos recursos subcontratados xa non é necesaria. Non se pode utilizar un subcontrato neste estado para estimar e dotar de persoal os requisitos do proxecto de recursos e materiais nin se pode facer referencia a tempo, gasto e uso de material nun proxecto. Un subcontrato neste estado non se pode editar nin eliminar. | Nada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
