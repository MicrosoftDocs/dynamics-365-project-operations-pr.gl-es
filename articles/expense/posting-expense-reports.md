---
title: Publicar informes de gastos
description: Este artigo explica como publicar informes de gastos.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524867"
---
# <a name="post-expense-reports"></a>Publicar informes de gastos

Unha vez aprobado un informe de gastos e transferido ao diario xeral, pódese contabilizar. Ao contabilizar un informe de gastos, identifícanse os gastos que son elixibles para a recuperación do imposto sobre o valor engadido (IVE). A tarefa de verificación e recuperación dos pagos do IVE atribúese ao empregado responsable da verificación do informe de gastos.

Se os gastos derivados dun informe de gastos se impoñen a unha empresa distinta da empresa á que pertence empregado, deberá verificar tanto a empresa á que eses gastos se deben como a empresa os debe. Por exemplo, o empregado que presentou un informe de gastos traballa para a empresa DAT pero cobrou un gasto á empresa DIR. Neste caso, DAT é a empresa á que se debe o gasto e DIR é a empresa que debe o gasto. Despois de verificar estas liñas de diario, pode contabilizar as liñas de gasto no libro maior.

Para contabilizar un informe de gastos, na páxina **Informes de gastos aprobados**, seleccione o informe de gastos e, a seguir, no panel de acción, seleccione **Contabilizar**.

Tamén pode contabilizar todos os informes de gastos da lista ao mesmo tempo. Seleccione todos os informes de gastos e logo seleccione **Contabilizar**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Activa a función Capacidade de contabilizar a responsabilidade dos gastos na moeda do provedor para o método de pago en efectivo

O **Capacidade de contabilizar a responsabilidade dos gastos na moeda do provedor para o método de pago en efectivo** A función permite que os informes de gastos se publiquen nunha moeda do provedor para o método de pago en efectivo.

Actualmente, cando envía gastos en efectivo, os informes de gastos publícanse na moeda contable. Debido á conversión de cantidades entre a moeda da transacción, a moeda contable e a moeda do provedor, págase un importe incorrecto aos provedores se a data de transacción do gasto e a data de pago real teñen tipos de cambio diferentes.

Esta función garantirá que o saldo do provedor estea rexistrado na moeda do provedor cando se publique o informe de gastos.

1. Vaia a **Áreas de traballo** \> **Xestión de funcionalidades**.
2. Na lista, busque e seleccione **Capacidade de contabilizar a responsabilidade dos gastos na moeda do provedor para o método de pago en efectivo** e, a continuación, seleccione **Habilita agora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
