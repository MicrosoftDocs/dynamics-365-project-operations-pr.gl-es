---
title: Cancelar unha factura de fornecedor do proxecto
description: Este artigo explica como cancelar unha factura de provedor de proxecto en Microsoft Dynamics 365 Project Operations e o impacto financeiro de cancelar unha factura do provedor do proxecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261088"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancelar unha factura de fornecedor do proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Despois de que se confirma a factura do fornecedor, non se pode editar nin eliminar. Se houbo un erro nunha factura de fornecedor que se confirmou, pode usar a acción Cancelar para reverter o impacto da factura de fornecedor e crear unha nova factura de fornecedor.

Cando seleccione **Cancelar** nunha factura de fornecedor, ocorre o seguinte comportamento:

1. Actualízase o estado da factura do fornecedor a **Cancelada**.
2. A factura do fornecedor cancelada e os seus rexistros relacionados pasan a ser de só lectura e non se poden editar nin eliminar.
3. Todos os custos reais que se crearon en función das liñas de factura do fornecedor como parte da confirmación da factura do fornecedor reverteranse.
4. Se algún dato real de custo estaba ligado ás liñas de factura do fornecedor como parte do proceso de busca de coincidencias, a confirmación orixinal da factura do fornecedor reverteuno. Durante a cancelación da factura do fornecedor, eses datos reais de custos créanse de novo. As orixes apuntan ás entradas de tempo, gasto ou uso de material.
5. Despois de que se cancele a factura do fornecedor, pode volver crear diarios de corrección, procesar os recordatorios de entradas de tempo e cancelar a aprobación dos datos reais de tempo, gasto ou material orixinais.

> [!NOTE]
> Só se poden cancelar as facturas do fornecedor do proxecto confirmadas. Non se poden cancelar as facturas de fornecedor noutros estados.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
