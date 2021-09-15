---
title: Versión de acceso anticipado de subcontratación en outubro de 2021
description: Este tema ofrece unha visión xeral das capacidades de subcontratación en Project Operations que forman parte da versión de acceso anticipado de outubro de 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383693"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Versión de acceso anticipado de subcontratación en outubro de 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este tema ofrece unha visión xeral das capacidades de subcontratación en Dynamics 365 Project Operations que forman parte da versión de acceso anticipado de outubro de 2021. Este conxunto de funcionalidades non está preparado para a produción nin ambientes en directo, polo que estas funcións permanecerán na versión de acceso anticipado ata que se publique o conxunto completo de funcionalidades. Recomendamos encarecidamente que non use o conxunto de funcionalidades de subcontratación para escenarios de produción en directo ata que se elimine a faia de versión preliminar. 

A seguinte lista ofrece un resumo do que está dispoñible actualmente na versión de acceso anticipado de outubro de 2021:

1. O xestor do proxecto crea un subcontrato cun provedor. De xeito predefinido, as listas de prezos que se xuntan ao rexistro do fornecedor úsanse para o subcontrato. A conta do fornecedor ten un tipo de relación de **Fornecedor** ou **Provedor**.

2. O xestor do proxecto pode detallar todas as compras como partidas na subcontrata. As liñas de subcontrato poden ser por tempo, gastos ou produtos. A clase de transacción da liña de subcontrato determina para que serve a liña.

3. O xestor de contas do fornecedor e o xestor de proxectos poden repetir o subcontrato. Os prezos poden axustarse nas listas de prezos de compra que se xuntan ao subcontrato.

4. Neste momento ou máis tarde no proceso, se a liña de subcontrato é por tempo, o xestor de contas do fornecedor asocia contactos de fornecedor con cada liña de subcontrato. Esta asociación proporciona información ao xestor do proxecto que está a traballar no subcontrato. Cando un contacto de fornecedor está asociado a unha liña de subcontrato, o sistema crea automaticamente un recurso reservable a partir do contacto, se aínda non existe un recurso reservable.

5. O método de facturación en cada liña de subcontrato pode ser **Prezo fixo** ou **Tempo e material**. Para as liñas de subcontrato a prezo fixo, configúrase un programa de facturas baseado en fitos.

Os restantes pasos do fluxo do proceso de negocio para subcontratar que se describen na visión xeral non están dispoñibles actualmente. A medida que se engada nova funcionalidade, este tema actualizarase. 

A seguinte ilustración representa a versión de subcontratación de acceso anticipado en contraste co proceso comercial de extremo a extremo.

![Fluxo do proceso de subcontratación](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Versión de acceso anticipado de liñas de subcontrato baseadas en cantidade e baseadas en traballo
Na versión de acceso anticipado de outubro de 2021, só se admiten liñas de subcontrato baseadas en cantidade. Isto significa que unha liña de subcontrato pode usarse para mercar tempo, gastos ou materiais dun fornecedor pero non todo un corpo de traballo. Isto tamén significa que a cantidade que se vai comprar (unidades de tempo, gastos ou cantidade de materiais) nunha liña de subcontrato pode usarse en calquera proxecto do sistema.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
