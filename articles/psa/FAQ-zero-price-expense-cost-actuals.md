---
title: Por que o prezo por defecto é cero nos custos de gastos reais?
description: Resolución de problemas de por que o prezo por defecto é 0 nos custos de gastos reais.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122116"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="33310-103">Por que o prezo por defecto é cero nos custos de gastos reais?</span><span class="sxs-lookup"><span data-stu-id="33310-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="33310-104">Estas Preguntas máis frecuentes aplícanse a gastos reais onde a clase de transacción está definida a Gastos e o tipo de transacción é Custo.</span><span class="sxs-lookup"><span data-stu-id="33310-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="33310-105">Resolución de problemas das taxas de custos no nos custos de gastos reais</span><span class="sxs-lookup"><span data-stu-id="33310-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="33310-106">Vaia a entrada de gastos relacionados e asegúrese de que hai unha cantidade no campo de entrada de gastos.</span><span class="sxs-lookup"><span data-stu-id="33310-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="33310-107">Se a entrada de gastos orixinal non se ten o campo de importe enchido, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="33310-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="33310-108">Para solucionar este problema, cree novamente a entrada de gastos cunha cantidade válida e apróbea.</span><span class="sxs-lookup"><span data-stu-id="33310-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
