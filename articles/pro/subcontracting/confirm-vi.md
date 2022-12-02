---
title: Confirmar unha factura fornecedor do proxecto
description: Este artigo explica como confirmar unha factura de fornecedor de proxecto en Microsoft Dynamics 365 Project Operations e o impacto financeiro de confirmar unha factura do fornecedor do proxecto.
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

Despois de verificar todas as liñas dunha factura de fornecedor en Microsoft Dynamics 365 Project Operations , pode usar a acción de Confirmar para confirmar a factura do fornecedor.

Cando seleccione **Confirmar** nunha factura de fornecedor, ocorre o seguinte comportamento:

1. Actualízase o estado da factura do fornecedor a **Confirmada**.
2. A factura do fornecedor confirmada e os seus rexistros relacionados pasan a ser de só lectura e non se poden editar nin eliminar.
3. Se algún dato real de custo fai referencia á liña de factura do fornecedor como parte do proceso de busca de coincidencias, todos os datos reais de custo que están asociados á liña de factura do fornecedor de referencia reverteranse.
4. Os novos datos reais de custo créanse utilizando a información da liña de factura do fornecedor.
5. Despois de que se confirme a factura do fornecedor, xa non pode crear diarios de corrección, procesar os recordatorios de entradas de tempo ou cancelar a aprobación dos datos reais de tempo, gasto ou material orixinais que se reverteron.

> [!NOTE]
> Se algunha liña dunha factura de fornecedor ten un estado de verificación distinto de **Completa**, a factura do fornecedor non se pode confirmar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
