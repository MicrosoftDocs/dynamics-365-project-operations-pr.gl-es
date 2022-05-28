---
title: Fluxo de traballo de xestión de gastos
description: Este tema explica como pode usar o sistema de fluxo de traballo en Microsoft Dynamics 365 Finanzas, para establecer un proceso de revisión de informes de gastos en Xestión de gastos.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eb4d57194ce2dd7f80d75c2c765f1cfa48b0348
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684272"
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