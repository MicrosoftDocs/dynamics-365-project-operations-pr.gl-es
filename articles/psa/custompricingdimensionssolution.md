---
title: Crear solucións personalizadas para as dimensións de prezos
description: Este tema explica como crear unha solución personalizada ao crear dimensións de prezos personalizadas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076141"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="83dc6-103">Crear solucións personalizadas para as dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="83dc6-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83dc6-104">Todos os cambios de dimensións de prezos personalizadas deberían estar nunha solución separada.</span><span class="sxs-lookup"><span data-stu-id="83dc6-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="83dc6-105">Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia.</span><span class="sxs-lookup"><span data-stu-id="83dc6-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="83dc6-106">Despois de facer os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.</span><span class="sxs-lookup"><span data-stu-id="83dc6-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="83dc6-107">Seleccione **Configuración** > **Solucións** e logo seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="83dc6-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="83dc6-108">Poña nome á solución, **\<your organization name> dimensións de prezos** , introduza a información restante necesaria e logo seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="83dc6-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Creación dunha solución personalizada para as dimensións de prezos](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="83dc6-110">Engadir todas as entidades requiridas e os compoñentes relacionados á solución de dimensión de prezos</span><span class="sxs-lookup"><span data-stu-id="83dc6-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="83dc6-111">Terá que engadir as seguintes entidades de Project Service á súa solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="83dc6-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="83dc6-112">Complete os pasos deste procedemento para facer algúns cambios importantes do esquema na solución de prezos para que as entidades teñan coñecemento das novas dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="83dc6-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="83dc6-113">Seleccione **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="83dc6-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="83dc6-114">No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="83dc6-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="83dc6-115">Na caixa de diálogo **Compoñentes da solución** , seleccione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="83dc6-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="83dc6-116">Dato real</span><span class="sxs-lookup"><span data-stu-id="83dc6-116">Actual</span></span>
- <span data-ttu-id="83dc6-117">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="83dc6-117">Bookable Resource</span></span>
- <span data-ttu-id="83dc6-118">Liña de estimación</span><span class="sxs-lookup"><span data-stu-id="83dc6-118">Estimate Line</span></span>
- <span data-ttu-id="83dc6-119">Tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="83dc6-119">Project Task</span></span>
- <span data-ttu-id="83dc6-120">Detalle da liña da factura</span><span class="sxs-lookup"><span data-stu-id="83dc6-120">Invoice Line Detail</span></span>
- <span data-ttu-id="83dc6-121">Liña de diario</span><span class="sxs-lookup"><span data-stu-id="83dc6-121">Journal Line</span></span>
- <span data-ttu-id="83dc6-122">Detalle da liña de contrato do proxecto</span><span class="sxs-lookup"><span data-stu-id="83dc6-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="83dc6-123">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="83dc6-123">Project Team Member</span></span>
- <span data-ttu-id="83dc6-124">Detalle da liña da oferta</span><span class="sxs-lookup"><span data-stu-id="83dc6-124">Quote Line Detail</span></span>
- <span data-ttu-id="83dc6-125">Sobreprezo de rol</span><span class="sxs-lookup"><span data-stu-id="83dc6-125">Role Price Markup</span></span>
- <span data-ttu-id="83dc6-126">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="83dc6-126">Role Price</span></span> 
- <span data-ttu-id="83dc6-127">Entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="83dc6-127">Time Entry</span></span> 

> ![Engadir entidades existentes á solución de dimensións de prezos](media/Existing-entities-to-PD-solution.png)

> ![Seleccionar compoñentes da solución](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="83dc6-130">Asegúrese de incluír todos os formularios e vistas para cada unha das entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="83dc6-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="83dc6-131">Cando se lle solicite incluír calquera entidade dependente para as entidades seleccionadas, seleccione **Non**.</span><span class="sxs-lookup"><span data-stu-id="83dc6-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Non incluír todos os compoñentes relacionados](media/Do-not-include-required.png)


