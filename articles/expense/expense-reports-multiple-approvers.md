---
title: Informes de gastos e múltiples responsables de aprobación
description: Este tema ofrece información sobre os informes de gastos que requiren a aprobación de máis dunha persoa.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076135"
---
# <a name="expense-reports-and-multiple-approvers"></a>Informes de gastos e múltiples responsables de aprobación

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dependendo das políticas de aprobación de gastos da súa organización, é posible que máis dunha persoa teña que aprobar un informe de gastos enviado. Cando configura o proceso de fluxo de traballo para a aprobación do informe de gastos, pode engadir elementos do fluxo de traballo que inclúan tarefas ou pasos para un ou máis responsables de aprobación de informes de gastos. Por exemplo, pode requirir que todos os informes de gastos sexan aprobados por dúas persoas distintas, o superior do empregado que o presentou e o coordinador de contas pendentes de pago.

Se decide requirir varios responsables de aprobación de informes de gastos, pode engadir os elementos do fluxo de traballo dalgún dos seguintes xeitos:

- Engada un elemento de aprobación que teña un paso. Por exemplo, o paso pode requirir que se atribúa un informe de gastos a un grupo de usuarios e que o aprobe o 50 por cento dos membros do grupo de usuarios.
- Engada un elemento de aprobación que teña varios pasos. Por exemplo, o elemento de aprobación pode ter os seguintes pasos:

    1. O superior do empregado que presentou o informe de gastos apróbao.
    2. O empregado de contas pendentes de pago verifica os recibos e os elementos do informe de gastos.
    3. O responsable do orzamento aproba o informe de gastos.

- Engada varios elementos de aprobación, cada un deles cun paso. Por exemplo, pode engadir un elemento de aprobación separado para cada un dos seguintes pasos:

    1. O superior do empregado aproba o informe de gastos.
    2. O responsable do orzamento aproba o informe de gastos.
