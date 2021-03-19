---
title: Crear modelos de previsión para orzamentos de proxecto
description: Este tema describe como crear un modelo de previsión para os orzamentos restantes.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271036"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="948d5-103">Crear modelos de previsión para orzamentos de proxecto</span><span class="sxs-lookup"><span data-stu-id="948d5-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="948d5-104">Este tema describe como crear un modelo de previsión para os orzamentos restantes.</span><span class="sxs-lookup"><span data-stu-id="948d5-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="948d5-105">Un proxecto suxeito a control orzamentario utiliza dous tipos de orzamentos: o orixinal e o restante.</span><span class="sxs-lookup"><span data-stu-id="948d5-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="948d5-106">Cando cree un orzamento do proxecto, debe especificar os modelos de previsión de orzamento orixinais e restantes que se crearon na páxina **Modelos de previsión**.</span><span class="sxs-lookup"><span data-stu-id="948d5-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="948d5-107">Os orzamentos do proxecto baseados nos modelos especificados créanse cando confirma o orzamento do proxecto.</span><span class="sxs-lookup"><span data-stu-id="948d5-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="948d5-108">Un modelo de previsión que se usa para o control do orzamento non pode ter un submodelo nin ser usado como submodelo.</span><span class="sxs-lookup"><span data-stu-id="948d5-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="948d5-109">Seleccione **Xestión e contabilidade de proxectos** > **Configuración** > **Previsións**  > **Modelos de previsión**.</span><span class="sxs-lookup"><span data-stu-id="948d5-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="948d5-110">Seleccione **Novo** para crear un novo modelo de previsión e, a seguir, escriba un número de identificación e un nome de modelo para o novo modelo.</span><span class="sxs-lookup"><span data-stu-id="948d5-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="948d5-111">Configure a opción **Detido** en **Si** para evitar cambios nas liñas de previsión do modelo de previsión.</span><span class="sxs-lookup"><span data-stu-id="948d5-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="948d5-112">Se as liñas de previsión coas que se asocia o modelo deberían xerar previsións de fluxo de efectivo no libro maior, configure **Incluír nas previsións de fluxo de caixa** en **Si.**</span><span class="sxs-lookup"><span data-stu-id="948d5-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="948d5-113">Para usar a data do proxecto como data de factura, configure **Previsión da data da factura** en **Si**.</span><span class="sxs-lookup"><span data-stu-id="948d5-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="948d5-114">No campo **Tipo de orzamento**, seleccione un dos seguintes tipos de modelos:</span><span class="sxs-lookup"><span data-stu-id="948d5-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="948d5-115">**Orzamento orixinal**: Use os importes do orzamento orixinal confirmados cando se crea e aproba o orzamento inicial.</span><span class="sxs-lookup"><span data-stu-id="948d5-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="948d5-116">**Orzamento restante**: Use os importes do orzamento restante durante a vida do proxecto.</span><span class="sxs-lookup"><span data-stu-id="948d5-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="948d5-117">Os saldos deste modelo de previsión redúcense por transaccións reais e aumentan ou diminúen por revisións orzamentarias.</span><span class="sxs-lookup"><span data-stu-id="948d5-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="948d5-118">**Transferir**: Use os importes do orzamento transferidos para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="948d5-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="948d5-119">A transferencia é un proceso opcional que se pode executar para transferir cantidades orzamentarias non utilizadas dun ano fiscal a outro.</span><span class="sxs-lookup"><span data-stu-id="948d5-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="948d5-120">Defina as seguintes opcións segundo sexa necesario:</span><span class="sxs-lookup"><span data-stu-id="948d5-120">Set the following options as required:</span></span>

   - <span data-ttu-id="948d5-121">Active **Previsión de data de factura** para usar a data do proxecto como data da factura.</span><span class="sxs-lookup"><span data-stu-id="948d5-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="948d5-122">Active **Previsión con WIP** para predicir en función do traballo en curso (WIP) e logo seleccionar o tipo de WIP.</span><span class="sxs-lookup"><span data-stu-id="948d5-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="948d5-123">Pode manter o valor predefinido **Tipo de orzamento** como **Ningún** ou introduza un novo tipo.</span><span class="sxs-lookup"><span data-stu-id="948d5-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="948d5-124">O tipo de orzamento non se pode cambiar despois de cambiar un rexistro.</span><span class="sxs-lookup"><span data-stu-id="948d5-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="948d5-125">Se cambia o tipo de orzamento predefinido, as demais opcións non estarán dispoñibles para actualizacións e non pode volver usar este modelo de previsión.</span><span class="sxs-lookup"><span data-stu-id="948d5-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]