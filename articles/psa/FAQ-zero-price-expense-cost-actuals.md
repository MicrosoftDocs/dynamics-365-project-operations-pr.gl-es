---
title: Por que o prezo por defecto é cero nos custos de gastos reais?
description: Resolución de problemas de por que o prezo por defecto é 0 nos custos de gastos reais.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992784"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="57aad-103">Por que o prezo por defecto é cero nos datos reais de custos de gastos</span><span class="sxs-lookup"><span data-stu-id="57aad-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="57aad-104">Estas Preguntas máis frecuentes aplícanse a gastos reais onde a clase de transacción está definida a Gastos e o tipo de transacción é Custo.</span><span class="sxs-lookup"><span data-stu-id="57aad-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="57aad-105">Resolución de problemas das taxas de custos no nos custos de gastos reais</span><span class="sxs-lookup"><span data-stu-id="57aad-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="57aad-106">Vaia a entrada de gastos relacionados e asegúrese de que hai unha cantidade no campo de entrada de gastos.</span><span class="sxs-lookup"><span data-stu-id="57aad-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="57aad-107">Se a entrada de gastos orixinal non se ten o campo de importe enchido, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="57aad-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="57aad-108">Para solucionar este problema, cree novamente a entrada de gastos cunha cantidade válida e apróbea.</span><span class="sxs-lookup"><span data-stu-id="57aad-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]