---
title: Varios responsables de aprobación nun informe de gastos
description: Este tema ofrece información sobre os informes de gastos que requiren a aprobación de varias persoas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076288"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Varios responsables de aprobación nun informe de gastos

[!include [banner](../includes/banner.md)]

Dependendo das políticas de aprobación de gastos da súa organización, é posible que máis dunha persoa teña que aprobar un informe de gastos que enviou un empregado. Cando configura o proceso de fluxo de traballo para a aprobación do informe de gastos, pode engadir elementos do fluxo de traballo que inclúan tarefas ou pasos para un ou máis responsables de aprobación de informes de gastos. Por exemplo, pode requirir que todos os informes de gastos sexan aprobados primeiro polo superior do empregado que o presentou e logo polo coordinador de contas pendentes de pago.

Se decide requirir varios responsables de aprobación de informes de gastos, pode engadir os elementos do fluxo de traballo dalgún dos seguintes xeitos:

- Engada un elemento de aprobación que teña un paso. Por exemplo, o paso pode requirir que se atribúa un informe de gastos a un grupo de usuarios e que o aprobe o 50 por cento dos membros do grupo de usuarios.
- Engada un elemento de aprobación que teña varios pasos. Por exemplo, o elemento de aprobación pode ter os seguintes pasos:

    1. O superior do empregado que presentou o informe de gastos apróbao.
    2. O empregado de contas pendentes de pago verifica os recibos e os elementos do informe de gastos.
    3. O responsable do orzamento aproba o informe de gastos.

- Engada varios elementos de aprobación, cada un deles cun paso. Por exemplo, pode engadir un elemento de aprobación separado para cada un dos seguintes pasos:

    1. O superior do empregado aproba o informe de gastos.
    2. O responsable do orzamento aproba o informe de gastos.
