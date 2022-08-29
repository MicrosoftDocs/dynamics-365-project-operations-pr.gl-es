---
title: Confirmar unha factura fornecedor do proxecto
description: Este artigo explica como confirmar unha factura do provedor do proxecto en Microsoft Dynamics 365 Project Operations e o impacto financeiro de confirmar unha factura do provedor do proxecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261509"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmar unha factura fornecedor do proxecto

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
