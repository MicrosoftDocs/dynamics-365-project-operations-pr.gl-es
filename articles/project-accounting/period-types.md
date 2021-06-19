---
title: Tipos de período
description: Este tema ofrece información sobre como configurar os tipos de período para a estimación de ingresos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013484"
---
# <a name="period-types"></a><span data-ttu-id="9736e-103">Tipos de período</span><span class="sxs-lookup"><span data-stu-id="9736e-103">Period types</span></span>

<span data-ttu-id="9736e-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="9736e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9736e-105">Un tipo de período define a frecuencia coa que se calculan os ingresos dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="9736e-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="9736e-106">Este tema ofrece información sobre como configurar os tipos de período para a estimación de ingresos.</span><span class="sxs-lookup"><span data-stu-id="9736e-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="9736e-107">Crear tipos de período e traballar con eles</span><span class="sxs-lookup"><span data-stu-id="9736e-107">Create and work with period types</span></span>
<span data-ttu-id="9736e-108">Para crear e traballar con tipos de período, complete os seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="9736e-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="9736e-109">No seu ambiente de Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Configuración** > **Estimacións** > **Tipos de período**.</span><span class="sxs-lookup"><span data-stu-id="9736e-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="9736e-110">Seleccione **Novo** para crear o novo tipo de período.</span><span class="sxs-lookup"><span data-stu-id="9736e-110">Select **New** to create new period type.</span></span> <span data-ttu-id="9736e-111">Introduza un nome e unha descrición.</span><span class="sxs-lookup"><span data-stu-id="9736e-111">Enter a name and description.</span></span>
3. <span data-ttu-id="9736e-112">No campo **Frecuencia**, seleccione un valor:</span><span class="sxs-lookup"><span data-stu-id="9736e-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="9736e-113">Se selecciona **Semana**, **Quincenal**, **Semestral**, **Mes**, **Día**, **Trimestre**, ou **Ano**, o calendario usarase para xerar os períodos.</span><span class="sxs-lookup"><span data-stu-id="9736e-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="9736e-114">Se selecciona **Período de libro maiore**, os períodos de libro maior da configuración do libro xeral utilizaranse para xerar períodos.</span><span class="sxs-lookup"><span data-stu-id="9736e-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="9736e-115">Se selecciona **Ilimitado**, pode especificar períodos personalizados.</span><span class="sxs-lookup"><span data-stu-id="9736e-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="9736e-116">Seleccione o rexistro do tipo de período e logo seleccione **Xerar períodos** para crear períodos para o tipo de período.</span><span class="sxs-lookup"><span data-stu-id="9736e-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="9736e-117">En función da frecuencia do período que seleccionou, pode que teña a opción de especificar unha data de inicio ou o número de períodos a xerar.</span><span class="sxs-lookup"><span data-stu-id="9736e-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="9736e-118">Seleccione **Períodos** para revisar os períodos xerados.</span><span class="sxs-lookup"><span data-stu-id="9736e-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]