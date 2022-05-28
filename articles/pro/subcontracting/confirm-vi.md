---
title: Confirme unha factura do provedor do proxecto
description: Este tema explica como confirmar unha factura de provedor do proxecto en Microsoft Dynamics 365 Project Operations e o impacto financeiro de confirmar unha factura do provedor do proxecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595726"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirme unha factura do provedor do proxecto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Despois de verificar todas as liñas dunha factura de provedor en Microsoft Dynamics 365 Project Operations, pode usar a acción Confirmar para confirmar a factura do provedor.

Cando selecciones **Confirmar** nunha factura de provedor, ocorre o seguinte comportamento:

1. Actualízase o estado da factura do provedor **Confirmado**.
2. A factura do provedor confirmada e os seus rexistros relacionados pasan a ser de só lectura e non se poden editar nin eliminar.
3. Se algún custo real fai referencia á liña de factura do provedor como parte do proceso de coincidencia, todos os custos reais que están asociados á liña de factura do provedor referenciado invertéranse.
4. Os novos custos reais créanse utilizando a información da liña de factura do provedor.
5. Despois de que se confirme a factura do provedor, xa non pode crear diarios de corrección, procesar recordatorios de entradas de tempo ou cancelar a aprobación do tempo orixinal, o gasto ou os datos reais do material que se reverteron.

> [!NOTE]
> Se algunha liña dunha factura de provedor ten un estado de verificación distinto de **Completa**, a factura do provedor non se pode confirmar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
