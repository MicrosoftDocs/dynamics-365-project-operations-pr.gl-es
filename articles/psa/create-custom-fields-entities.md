---
title: Crear campos e entidades personalizados
description: Este tema explica como crear conxuntos de opcións e entidades na súa propia solución na plataforma Power Apps.
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
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144861"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="a569e-103">Crear campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="a569e-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a569e-104">Realice os seguintes pasos sempre que queira crear un conxunto de opcións ou unha entidade personalizada na plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a569e-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="a569e-105">Os procedementos deste tema deberían realizarse mediante a interface web de Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a569e-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a569e-106">Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada.</span><span class="sxs-lookup"><span data-stu-id="a569e-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="a569e-107">Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia.</span><span class="sxs-lookup"><span data-stu-id="a569e-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="a569e-108">Despois de facer todos os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.</span><span class="sxs-lookup"><span data-stu-id="a569e-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="a569e-109">Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="a569e-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="a569e-110">Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade.</span><span class="sxs-lookup"><span data-stu-id="a569e-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="a569e-111">Ambos deben crearse na súa solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="a569e-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="a569e-112">Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="a569e-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="a569e-113">Dimensións baseada en entidade</span><span class="sxs-lookup"><span data-stu-id="a569e-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="a569e-114">En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="a569e-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="a569e-115">No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="a569e-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="a569e-116">Prema en **Nova** para crear unha nova entidade chamada **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="a569e-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="a569e-117">Introduza a información necesaria restante e, a seguir, prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="a569e-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definición de entidade de título estándar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="a569e-119">Dimensións baseadas en conxunto de opcións</span><span class="sxs-lookup"><span data-stu-id="a569e-119">Option set-based dimensions</span></span> 
<span data-ttu-id="a569e-120">Pode crear dúas dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="a569e-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="a569e-121">Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo con localización **Casa** e o traballo **No sitio** e utilice **Horas de traballo do recurso** cos valores **Normal** e **Horas extra** para aplicar un aumento cando finalice o traballo.</span><span class="sxs-lookup"><span data-stu-id="a569e-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="a569e-122">En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="a569e-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a569e-123">No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**.</span><span class="sxs-lookup"><span data-stu-id="a569e-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="a569e-124">Prema **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="a569e-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="a569e-125">Dimensión de prezos baseada en conxunto de opcións chamada Localización do traballo do recurso</span><span class="sxs-lookup"><span data-stu-id="a569e-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="a569e-126">Dimensión de prezos baseada en conxunto de opcións chamada Horas de traballo do recurso</span><span class="sxs-lookup"><span data-stu-id="a569e-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="a569e-127">Crear datos para dimensións baseadas en entidade</span><span class="sxs-lookup"><span data-stu-id="a569e-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="a569e-128">Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo.</span><span class="sxs-lookup"><span data-stu-id="a569e-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="a569e-129">Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="a569e-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="a569e-130">Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="a569e-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="a569e-131">En PSA prema **Localización avanzada**.</span><span class="sxs-lookup"><span data-stu-id="a569e-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="a569e-132">Seleccione a entidade **Título estándar** e logo prema **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="a569e-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="a569e-133">Mostraranse todas as filas na entidade **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="a569e-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="a569e-134">Prema **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a569e-134">Click **New**.</span></span> <span data-ttu-id="a569e-135">No campo **Nome** introduza "Enxeñeiro de sistemas" e logo prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="a569e-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="a569e-136">Peche o formulario.</span><span class="sxs-lookup"><span data-stu-id="a569e-136">Close the form.</span></span> 
4. <span data-ttu-id="a569e-137">Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".</span><span class="sxs-lookup"><span data-stu-id="a569e-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="a569e-138">Datos de exemplo para a entidade Título estándar</span><span class="sxs-lookup"><span data-stu-id="a569e-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


