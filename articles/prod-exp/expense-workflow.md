---
title: Fluxo de traballo de xestión de gastos
description: Este tema explica como pode usar o sistema de fluxo de traballo en Microsoft Dynamics 365 Finance, para configurar un proceso de revisión dos informes de gastos na xestión de gastos.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001294"
---
# <a name="expense-management-workflow"></a>Fluxo de traballo de xestión de gastos

Pode usar o sistema de fluxo de traballo para configurar un proceso de revisión dos informes de gastos na xestión de gastos. Pode configurar un fluxo de traballo que use os seguintes criterios para determinar quen aproba os informes de gastos:

- A xerarquía de informes dos empregados e os límites de aprobación predefinidos
- Aprobación multinivel que admite responsables de aprobacións intermedios e un responsable de aprobacións final
- Dimensións financeiras e responsabilidade do proxecto
- Atribución a usuarios ou grupos de usuarios específicos

Pódense crear aprobacións de fluxo de traballo para informes de gastos, solicitudes de viaxes, adiantos de efectivo e recuperación do imposto sobre o valor engadido (IVE).

**Exemplo**

O seguinte proceso é un exemplo do fluxo de traballo de xestión de gastos para un informe de gastos.

1. Un empregado crea e garda un informe de gastos.
2. O empregado envía o informe de gastos para a súa aprobación. O responsable de aprobacións identifícase en función das regras que se definiron cando se configurou o fluxo de traballo.
3. O responsable de aprobacións recibe unha notificación de que un informe de gastos está listo para a súa aprobación. O responsable de aprobacións revisa o informe de gastos e verifica que se cumpren as seguintes condicións:

    - Os gastos non infrinxen ningunha política de gastos. Se un gasto infrinxe unha política, o responsable de aprobacións verifica que o informe de gastos inclúe unha xustificación comercial válida.
    - Os xustificantes electrónicos anéxanse ao informe de gastos.

4. O responsable de aprobacións aproba o informe de gastos.
5. O informe de gastos atribúese ao coordinador de contas pendentes de pago para a súa contabilización.
6. Prodúcese un dos seguintes pasos, dependendo de se está configurada a contabilización automática:

    - Se se configura a contabilización automática, o informe de gastos procesarase para o pagamento e actualizarase o estado do informe de gastos.
    - Se a contabilización automática non está configurada, o coordinador de contas pendentes de pago verifica que se enviaron todos os recibos orixinais e que os recibos están aliñados cos gastos do informe de gastos. Todos os códigos fiscais que se introducen no informe de gastos tamén deben verificarse como correctos.

Despois de verificar estes requisitos, contabilízase o informe de gastos.

Despois de publicar o informe de gastos, autorízase o pagamento do informe de gastos e reembolsaráselle ao empregado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]