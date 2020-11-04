---
title: Por que o prezo por defecto é cero nos custos de tempo reais?
description: Resolución de problemas de por que o prezo por defecto é 0 nos custos por tempo reais.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076151"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="94932-103">Por que o prezo por defecto é cero nos custos de tempo reais?</span><span class="sxs-lookup"><span data-stu-id="94932-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="94932-104">Estas Preguntas máis frecuentes aplícanse a valores reais onde a clase de transacción está definida a Tempo e o tipo de transacción é Custo.</span><span class="sxs-lookup"><span data-stu-id="94932-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="94932-105">As tres seguintes comprobacións axudaranlle a solucionar por que o prezo son por defecto 0 nos valores reais de custos por tempo.</span><span class="sxs-lookup"><span data-stu-id="94932-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="94932-106">Verificación 1: Identificar a lista de prezos de custos para o proxecto</span><span class="sxs-lookup"><span data-stu-id="94932-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="94932-107">Busque o proxecto no campo de proxectos do valor real e vaia á páxina de proxecto.</span><span class="sxs-lookup"><span data-stu-id="94932-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="94932-108">Prema a ligazón de unidade de contrato no campo.</span><span class="sxs-lookup"><span data-stu-id="94932-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="94932-109">Na páxina Unidade de contrato, comprobe se a unidade de contrato ten unha lista de prezos na grade de Listas de prezos de custo.</span><span class="sxs-lookup"><span data-stu-id="94932-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="94932-110">Se hai máis dunha lista de prezos, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="94932-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="94932-111">Project Service só admite unha lista de prezos por unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="94932-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="94932-112">Elimina todas as listas de prezos desta entidade até que haxa só unha lista de prezos anexada a grade de Listas de prezos de custo da unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="94932-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="94932-113">Se non hai ningunha lista de prezos anexada á unidade organizativa, anote a moeda da unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="94932-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="94932-114">Vaia a Project Service e, a seguir, Parámetros e abra o separador Listas de prezos. Comprobe se hai algunha lista de prezos con contexto definido como Custo e a moeda que coincide coa moeda da unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="94932-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="94932-115">Se non hai ningunha lista de prezos que se correspondan con esos criterios, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="94932-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="94932-116">Asegúrese de ter polo menos unha lista de prezos cun contexto definido en Custo e cunha moeda que coincida coa moeda da unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="94932-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="94932-117">Se hai máis dunha lista de prezos que se correspondan con esos criterios, siga lendo este documento para facer máis comprobacións.</span><span class="sxs-lookup"><span data-stu-id="94932-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="94932-118">Verificación 2: Algunha das listas de prezos identificadas enriba é válida para a data específica no valor real de vendas por custo?</span><span class="sxs-lookup"><span data-stu-id="94932-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="94932-119">Para que Project Service considere unha lista de prezos como prezo por defecto, esa lista de prezos debe ser aplicable para a data no valor real de vendas por custo.</span><span class="sxs-lookup"><span data-stu-id="94932-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="94932-120">Comprobe o seguinte para ver se as listas de prezos identificados enriba son aplicables:</span><span class="sxs-lookup"><span data-stu-id="94932-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="94932-121">Comprobe se as datas de inicio e fin no separador xeral para as listas de prezos anexada non están baleiras.</span><span class="sxs-lookup"><span data-stu-id="94932-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="94932-122">Se as datas de inicio e fin nas listas de prezos identificadas enriba está baleiras, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="94932-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="94932-123">Anote o campo de data de inicio no seu valor real de vendas por custo e comprobe se algunha das listas de prezos identificadas é aplicable para esa data.</span><span class="sxs-lookup"><span data-stu-id="94932-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="94932-124">Por exemplo, a data do valor real de vendas por custo debería estar entre a data de inicio e a data de fin na lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="94932-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="94932-125">Se non hai ningunha lista de prezos que cubra esa data no valor real de vendas por custo, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="94932-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="94932-126">Modificar as datas de inicio e fin da lista de prezos para asegurar que a lista de prezos cubra a data do valor real de vendas por custo.</span><span class="sxs-lookup"><span data-stu-id="94932-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="94932-127">Se hai máis dunha lista de prezos que cubra a data no valor real de vendas por custo, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="94932-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="94932-128">Pode corrixir isto editando as datas de inicio e fin das listas de prezos, de forma que haxa só unha lista de prezos que cubra a data do valor real de vendas por custo.</span><span class="sxs-lookup"><span data-stu-id="94932-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="94932-129">Se só hai unha lista de prezos que cubra esa data do valor real de custo de tempo, vaia á seguinte verificación no documento.</span><span class="sxs-lookup"><span data-stu-id="94932-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="94932-130">Cando faga as correccións necesarias, cree novamente unha entrada de tempo, apróbea e verifique que o valor real de vendas por custo mostra un prezo válido.</span><span class="sxs-lookup"><span data-stu-id="94932-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="94932-131">Verificación 3: Hai un prezo na lista de prezos para as dimensions de prezos no valor real de vendas por custo?</span><span class="sxs-lookup"><span data-stu-id="94932-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="94932-132">Se concluíu correctamente as Verificacións 1 e 2, agora debe ter só unha lista de prezos é aplicable para a data do valor real de vendas por custo.</span><span class="sxs-lookup"><span data-stu-id="94932-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="94932-133">Abra esta Lista de prezos do proxecto e vaia ao separador Prezos de rol. Asegúrese de que hai unha liña na grade para as dimensións de tempo no valor real de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="94932-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="94932-134">Se non hai ningunha fila na grade de prezos de rol para as dimensións de prezos no valor real de vendas por custo, xa identificou o problema.</span><span class="sxs-lookup"><span data-stu-id="94932-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="94932-135">Cree unha liña na grade de prezos de Rol para as dimensións de prezos no valor real de vendas por custo.</span><span class="sxs-lookup"><span data-stu-id="94932-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="94932-136">Cando termine, cree novamente unha entrada de tempo, apróbea e verifique que o valor real de vendas por custo mostra un prezo válido.</span><span class="sxs-lookup"><span data-stu-id="94932-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="94932-137">Se aínda non ve un prezo válido no valor real de vendas por custo despois de realizar as tres comprobacións anteriores, rexistre o tícket de asistencia.</span><span class="sxs-lookup"><span data-stu-id="94932-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



