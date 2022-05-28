---
title: Cancelar unha factura de provedor do proxecto
description: Este tema explica como cancelar unha factura de provedor de proxecto en Microsoft Dynamics 365 Project Operations e o impacto financeiro de cancelar unha factura do provedor do proxecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580638"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancelar unha factura de provedor do proxecto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Despois de confirmar unha factura de provedor, non se pode editar nin eliminar. Se houbo un erro nunha factura de provedor que se confirmou, pode usar a acción Cancelar para revertir o impacto da factura de provedor e crear unha nova factura de provedor.

Cando selecciones **Cancelar** nunha factura de provedor, ocorre o seguinte comportamento:

1. Actualízase o estado da factura do provedor **Cancelado**.
2. A factura do provedor cancelada e os seus rexistros relacionados pasan a ser de só lectura e non se poden editar nin eliminar.
3. Todos os custos reais que se crearon en función das liñas de factura do provedor como parte da confirmación da factura do provedor invírtense.
4. Se algún custo reais estaba ligado ás liñas de factura do provedor como parte do proceso de coincidencia, a confirmación orixinal da factura do provedor invertíao. Durante a cancelación da factura do provedor, eses custos reais recréanse de novo. As orixes apuntan ás entradas de tempo, gasto ou uso de material.
5. Despois de cancelar a factura do provedor, pode volver crear diarios de corrección, procesar os recordatorios de entradas de tempo e cancelar a aprobación do tempo orixinal, dos gastos ou dos datos reais do material.

> [!NOTE]
> Só se poden cancelar as facturas de provedores do proxecto confirmadas. Non se poden cancelar as facturas de provedores doutros estados.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
