---
title: Análise de ofertas de proxecto
description: Este tema fornece información sobre a análise de ofertas de proxecto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291257"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="89cb5-103">Análise de ofertas de proxecto</span><span class="sxs-lookup"><span data-stu-id="89cb5-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="89cb5-104">Dynamics 365 Project Service Automation analiza as ofertas de proxectos para estimar a rendibilidade.</span><span class="sxs-lookup"><span data-stu-id="89cb5-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="89cb5-105">Tamén analiza o axuste da oferta ás expectativas dos clientes sobre a data de entrega ou a data de finalización e sobre o orzamento.</span><span class="sxs-lookup"><span data-stu-id="89cb5-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="89cb5-106">Análise da rendibilidade</span><span class="sxs-lookup"><span data-stu-id="89cb5-106">Profitability analysis</span></span>

<span data-ttu-id="89cb5-107">Project Service Automation analiza a rendibilidade empregando a marxe bruta e a marxe bruta axustada.</span><span class="sxs-lookup"><span data-stu-id="89cb5-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="89cb5-108">A marxe bruta calcúlase mediante a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="89cb5-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="89cb5-109">A marxe bruta axustada calcúlase mediante a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="89cb5-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="89cb5-110">Se os valores da marxe bruta e da marxe bruta axustada difiren por unha ampla marxe, gran parte do traballo da oferta clasifícase como non impoñible.</span><span class="sxs-lookup"><span data-stu-id="89cb5-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="89cb5-111">Análise das expectativas do cliente</span><span class="sxs-lookup"><span data-stu-id="89cb5-111">Analysis of customer expectations</span></span>

<span data-ttu-id="89cb5-112">Pode analizar ofertas e xerar gráficos para as expectativas dos clientes sobre a programación e o orzamento se introduce valores para os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="89cb5-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="89cb5-113">O campo **Data de entrega solicitada** no encabezado da oferta.</span><span class="sxs-lookup"><span data-stu-id="89cb5-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="89cb5-114">O campo **Orzamento do cliente** para cada liña da oferta (para liñas baseadas en proxectos e liñas baseadas en produtos).</span><span class="sxs-lookup"><span data-stu-id="89cb5-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="89cb5-115">A análise das expectativas dos clientes sobre a programación realízase comparando a última data final do detalle da liña de oferta coa data de entrega solicitada en todas as liñas de oferta da oferta.</span><span class="sxs-lookup"><span data-stu-id="89cb5-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="89cb5-116">A análise das expectativas dos clientes sobre o orzamento realízase comparando a suma do orzamento total do cliente co importe ofertado en todas as liñas da oferta.</span><span class="sxs-lookup"><span data-stu-id="89cb5-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]