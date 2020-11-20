---
title: Dietas
description: Este tema ofrece información sobre as regras das dietas que se usan na xestión de gastos.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128506"
---
# <a name="per-diems"></a><span data-ttu-id="4cd19-103">Dietas</span><span class="sxs-lookup"><span data-stu-id="4cd19-103">Per diems</span></span>

<span data-ttu-id="4cd19-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="4cd19-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="4cd19-105">A dieta é un subsidio que se paga a un traballador que viaxa por traballo.</span><span class="sxs-lookup"><span data-stu-id="4cd19-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="4cd19-106">En xestión de gastos, pode crear regras de dietas para varias situacións de viaxe.</span><span class="sxs-lookup"><span data-stu-id="4cd19-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="4cd19-107">As taxas das dietas poden basearse na época do ano, na localización da viaxe ou en ambas.</span><span class="sxs-lookup"><span data-stu-id="4cd19-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="4cd19-108">Cando crea unha regra de dietas, pode especificar que se reterá unha porcentaxe da taxa de dietas se un traballador recibe comidas ou servizos de cortesía.</span><span class="sxs-lookup"><span data-stu-id="4cd19-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="4cd19-109">Tamén pode establecer un número mínimo e máximo de horas que a taxa de dietas se pode aplicar ás viaxes dun traballador.</span><span class="sxs-lookup"><span data-stu-id="4cd19-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="4cd19-110">Configuración</span><span class="sxs-lookup"><span data-stu-id="4cd19-110">Configuration</span></span> 

1. <span data-ttu-id="4cd19-111">Para engadir localizacións de dietas, vaia a **Configuración** > **Cálculos e códigos** > **Localizacións de dietas**.</span><span class="sxs-lookup"><span data-stu-id="4cd19-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="4cd19-112">Para cada unha das localizacións engadidas anteriormente, seleccione unha taxa de dietas e a moeda que sexa válida entre unha data específica de inicio e fin para hotel, comidas e outros gastos.</span><span class="sxs-lookup"><span data-stu-id="4cd19-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="4cd19-113">Os tipos e as moedas diarios configúranse en **Configuración** > **Cálculos e códigos** > **Dietas**.</span><span class="sxs-lookup"><span data-stu-id="4cd19-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="4cd19-114">Na páxina **Localizacións de dietas**, configure os niveis de taxa de dietas.</span><span class="sxs-lookup"><span data-stu-id="4cd19-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="4cd19-115">Os niveis de taxa de dietas permítenlle definir a porcentaxe de división dun subsidio diario para gastos de hotel, comida e outros.</span><span class="sxs-lookup"><span data-stu-id="4cd19-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="4cd19-116">Para especificar a redución da porcentaxe das comidas para o almorzo, o xantar ou a cea, actualice os campos da páxina **Parámetros de xestión de gastos** no separador **Dietas**.</span><span class="sxs-lookup"><span data-stu-id="4cd19-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="4cd19-117">Enviar os gastos usando as dietas</span><span class="sxs-lookup"><span data-stu-id="4cd19-117">Submit expenses using per diem</span></span>
<span data-ttu-id="4cd19-118">Para enviar gastos utilizando dietas, use a categoría de gasto **Dietas** cando cree un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="4cd19-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="4cd19-119">Introduza a **Dietas desde a data**, **Dietas ata a data** e **Localización de dietas**.</span><span class="sxs-lookup"><span data-stu-id="4cd19-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="4cd19-120">A cantidade calcularase en función das taxas de dietas para a localización seleccionada e a redución de comidas calcularase en función dos niveis de taxas de dietas.</span><span class="sxs-lookup"><span data-stu-id="4cd19-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
