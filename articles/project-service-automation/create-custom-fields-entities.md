---
title: Crear campos e entidades personalizados
description: Este tema explica como crear conxuntos de opcións e entidades na súa propia solución na plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751451"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="69c29-103">Crear campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="69c29-103">Create custom fields and entities</span></span> 

<span data-ttu-id="69c29-104">Realice os seguintes pasos sempre que queira crear un conxunto de opcións ou unha entidade personalizada na plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="69c29-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="69c29-105">Os procedementos deste tema deberían realizarse mediante a interface web de Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="69c29-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69c29-106">Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada.</span><span class="sxs-lookup"><span data-stu-id="69c29-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="69c29-107">Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia.</span><span class="sxs-lookup"><span data-stu-id="69c29-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="69c29-108">Despois de facer todos os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.</span><span class="sxs-lookup"><span data-stu-id="69c29-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="69c29-109">Crear unha solución personalizada para as dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="69c29-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="69c29-110">En PSA, prema en **Configuración** > **Solucións** e logo prema en **Nova** para crear unha nova solución.</span><span class="sxs-lookup"><span data-stu-id="69c29-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="69c29-111">Poña nome á solución, **\<nome da súa organización> dimensións de prezos**, introduza a información restante necesaria e logo prema en **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="69c29-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Creación dunha solución personalizada para as dimensións de prezos](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="69c29-113">Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="69c29-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="69c29-114">Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade.</span><span class="sxs-lookup"><span data-stu-id="69c29-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="69c29-115">Ambos deben crearse na súa solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="69c29-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="69c29-116">Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="69c29-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="69c29-117">Dimensións baseada en entidade</span><span class="sxs-lookup"><span data-stu-id="69c29-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="69c29-118">En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces en **\<nome da súa organización> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="69c29-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="69c29-119">No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="69c29-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="69c29-120">Prema en **Nova** para crear unha nova entidade chamada **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="69c29-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="69c29-121">Introduza a información necesaria restante e, a seguir, prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="69c29-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definición de entidade de título estándar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="69c29-123">Dimensións baseadas en conxunto de opcións</span><span class="sxs-lookup"><span data-stu-id="69c29-123">Option set-based dimensions</span></span> 
<span data-ttu-id="69c29-124">Pode crear dúas dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="69c29-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="69c29-125">Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo con localización **Casa** e o traballo **No sitio** e utilice **Horas de traballo do recurso** cos valores **Normal** e **Horas extra** para aplicar un aumento cando finalice o traballo.</span><span class="sxs-lookup"><span data-stu-id="69c29-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="69c29-126">En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces en **\<nome da súa organización> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="69c29-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="69c29-127">No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**.</span><span class="sxs-lookup"><span data-stu-id="69c29-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="69c29-128">Prema **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="69c29-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="69c29-129">Dimensión de prezos baseada en conxunto de opcións chamada Localización do traballo do recurso</span><span class="sxs-lookup"><span data-stu-id="69c29-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="69c29-130">Dimensión de prezos baseada en conxunto de opcións chamada Horas de traballo do recurso</span><span class="sxs-lookup"><span data-stu-id="69c29-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="69c29-131">Crear datos para dimensións baseadas en entidade</span><span class="sxs-lookup"><span data-stu-id="69c29-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="69c29-132">Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo.</span><span class="sxs-lookup"><span data-stu-id="69c29-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="69c29-133">Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="69c29-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="69c29-134">Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="69c29-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="69c29-135">En PSA prema **Localización avanzada**.</span><span class="sxs-lookup"><span data-stu-id="69c29-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="69c29-136">Seleccione a entidade **Título estándar** e logo prema **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="69c29-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="69c29-137">Mostraranse todas as filas na entidade **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="69c29-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="69c29-138">Prema **Novo**.</span><span class="sxs-lookup"><span data-stu-id="69c29-138">Click **New**.</span></span> <span data-ttu-id="69c29-139">No campo **Nome** introduza "Enxeñeiro de sistemas" e logo prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="69c29-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="69c29-140">Peche o formulario.</span><span class="sxs-lookup"><span data-stu-id="69c29-140">Close the form.</span></span> 
4. <span data-ttu-id="69c29-141">Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".</span><span class="sxs-lookup"><span data-stu-id="69c29-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="69c29-142">Datos de exemplo para a entidade Título estándar</span><span class="sxs-lookup"><span data-stu-id="69c29-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="69c29-143">Engada todas as entidades PSA requiridas e os compoñentes relacionados á solución de dimensión de prezos</span><span class="sxs-lookup"><span data-stu-id="69c29-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="69c29-144">Terá que engadir as seguintes entidades de Project Service á súa solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="69c29-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="69c29-145">Siga os pasos deste procedemento para facer algúns cambios importantes do esquema na solución de prezos para que as entidades teñan coñecemento das novas dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="69c29-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="69c29-146">En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces en **\<nome da súa organización> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="69c29-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="69c29-147">No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="69c29-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="69c29-148">Na caixa de diálogo **Compoñentes da solución**, seleccione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="69c29-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="69c29-149">Real</span><span class="sxs-lookup"><span data-stu-id="69c29-149">Actual</span></span>
- <span data-ttu-id="69c29-150">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="69c29-150">Bookable Resource</span></span>
- <span data-ttu-id="69c29-151">Liña de estimación</span><span class="sxs-lookup"><span data-stu-id="69c29-151">Estimate Line</span></span>
- <span data-ttu-id="69c29-152">Detalle da liña da factura</span><span class="sxs-lookup"><span data-stu-id="69c29-152">Invoice Line Detail</span></span>
- <span data-ttu-id="69c29-153">Liña de diario</span><span class="sxs-lookup"><span data-stu-id="69c29-153">Journal Line</span></span>
- <span data-ttu-id="69c29-154">Detalle da liña de contrato do proxecto</span><span class="sxs-lookup"><span data-stu-id="69c29-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="69c29-155">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="69c29-155">Project Team Member</span></span>
- <span data-ttu-id="69c29-156">Detalle da liña da oferta</span><span class="sxs-lookup"><span data-stu-id="69c29-156">Quote Line Detail</span></span>
- <span data-ttu-id="69c29-157">Sobreprezo de rol</span><span class="sxs-lookup"><span data-stu-id="69c29-157">Role Price Markup</span></span>
- <span data-ttu-id="69c29-158">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="69c29-158">Role Price</span></span> 
- <span data-ttu-id="69c29-159">Entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="69c29-159">Time Entry</span></span> 

> ![Engadir entidades existentes á solución de dimensións de prezos](media/Existing-entities-to-PD-solution.png)

> ![Seleccionar compoñentes da solución](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="69c29-162">Asegúrese de incluír todos os formularios e vistas para cada unha das entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="69c29-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="69c29-163">Cando se lle solicite incluír calquera entidade dependente para as entidades seleccionadas anteriormente, prema en **Non**.</span><span class="sxs-lookup"><span data-stu-id="69c29-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Non incluír todos os compoñentes relacionados](media/Do-not-include-required.png)


