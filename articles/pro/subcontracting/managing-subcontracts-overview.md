---
title: Xestión de subcontratos en Project Operations
description: Este tema ofrece unha visión xeral do proceso de xestión de subcontratos de extremo a extremo en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994229"
---
# <a name="subcontract-management-in-project-operations"></a>Xestión de subcontratos en Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

A subcontratación en Microsoft Dynamics 365 Project Operations admite o seguinte fluxo do proceso de negocio.

![Fluxo do proceso de subcontratación](../media/SubcontractingProcessFlow.png)

Aquí ten unha descrición paso a paso do proceso de subcontratación.

1. O xestor do proxecto crea un subcontrato cun provedor. De xeito predefinido, as listas de prezos que se xuntan ao rexistro do fornecedor úsanse para o subcontrato. A conta do fornecedor ten un tipo de relación de **Fornecedor** ou **Provedor**.
2. O xestor do proxecto pode detallar todas as compras como partidas na subcontrata. As liñas de subcontrato poden ser por tempo, gastos ou produtos. A clase de transacción que se selecciona en cada liña de subcontrato determina para que serve a liña.
3. O xestor de contas do fornecedor e o xestor de proxectos poden repetir o subcontrato. Os prezos poden axustarse nas listas de prezos de compra que se xuntan ao subcontrato.
4. Neste momento ou máis tarde no proceso, se a liña de subcontrato é por tempo, o xestor de contas do fornecedor asocia contactos con cada liña de subcontrato. Esta asociación proporciona información ao xestor do proxecto que está a traballar no subcontrato. Cando un contacto está asociado a unha liña de subcontrato, o sistema crea automaticamente un recurso reservable a partir do contacto, se aínda non existe un recurso reservable.
5. O método de facturación en cada liña de subcontrato pode ser **Prezo fixo** ou **Tempo e material**. Para as liñas de subcontrato a prezo fixo, pode configurar un programa de facturas baseado en fitos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
