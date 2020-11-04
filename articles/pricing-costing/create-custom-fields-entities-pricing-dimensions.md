---
title: Crear campos e entidades personalizados como dimensións de prezos
description: Este tema ofrece información sobre como crear conxuntos de opcións ou entidades personalizados.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076170"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="cb1f1-103">Crear campos e entidades personalizados como dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="cb1f1-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="cb1f1-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="cb1f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb1f1-105">Realice os seguintes pasos sempre que queira crear un conxunto de opcións ou unha entidade personalizados.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb1f1-106">Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="cb1f1-107">Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="cb1f1-108">Despois de facer todos os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="cb1f1-109">Crear unha solución personalizada para as dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="cb1f1-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="cb1f1-110">Vaia a **Configuración** > **Solucións** e logo seleccione en **Nova** para crear unha nova solución.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="cb1f1-111">Poña nome á solución, **\<your organization name> dimensións de prezos** , introduza a información restante necesaria e logo seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="cb1f1-112">Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="cb1f1-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="cb1f1-113">Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="cb1f1-114">Ambos deben crearse na súa solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="cb1f1-115">Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="cb1f1-116">Dimensións baseada en entidade</span><span class="sxs-lookup"><span data-stu-id="cb1f1-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="cb1f1-117">Vaia a **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="cb1f1-118">No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="cb1f1-119">Seleccione **Nova** para crear unha nova entidade chamada **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="cb1f1-120">Introduza a información necesaria restante e, a seguir, seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="cb1f1-121">Dimensións baseadas en conxunto de opcións</span><span class="sxs-lookup"><span data-stu-id="cb1f1-121">Option set-based dimensions</span></span> 
<span data-ttu-id="cb1f1-122">Pode crear dúas dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="cb1f1-123">Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo con localización **Casa** e o traballo **No sitio** e utilice **Horas de traballo do recurso** cos valores **Normal** e **Horas extra** para aplicar un aumento cando finalice o traballo.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="cb1f1-124">Vaia a **Configuración** > **Solucións** e prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="cb1f1-125">No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="cb1f1-126">Seleccione **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="cb1f1-127">Crear datos para dimensións baseadas en entidade</span><span class="sxs-lookup"><span data-stu-id="cb1f1-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="cb1f1-128">Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="cb1f1-129">Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="cb1f1-130">Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="cb1f1-131">Seleccione **Busca avanzada** , seleccione a entidade **Título estándar** e, a seguir, seleccione **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="cb1f1-132">Mostraranse todas as filas na entidade **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="cb1f1-133">Seleccione **Novo** e no campo **Nome** introduza "Enxeñeiro de sistemas" e logo seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="cb1f1-134">Peche o formulario.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-134">Close the form.</span></span> 
4. <span data-ttu-id="cb1f1-135">Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".</span><span class="sxs-lookup"><span data-stu-id="cb1f1-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="cb1f1-136">Engada todas as entidades requiridas e os compoñentes relacionados á solución de dimensión de prezos</span><span class="sxs-lookup"><span data-stu-id="cb1f1-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="cb1f1-137">Terá que engadir as seguintes entidades á súa solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="cb1f1-138">Siga os pasos deste procedemento para facer algúns cambios importantes do esquema na solución de prezos para que as entidades teñan coñecemento das novas dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="cb1f1-139">Seleccione **Configuración** > **Solucións** e prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="cb1f1-140">No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="cb1f1-141">Na caixa de diálogo **Compoñentes da solución** , seleccione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="cb1f1-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="cb1f1-142">Real</span><span class="sxs-lookup"><span data-stu-id="cb1f1-142">Actual</span></span>
  - <span data-ttu-id="cb1f1-143">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="cb1f1-143">Bookable Resource</span></span>
  - <span data-ttu-id="cb1f1-144">Liña de estimación</span><span class="sxs-lookup"><span data-stu-id="cb1f1-144">Estimate Line</span></span>
  - <span data-ttu-id="cb1f1-145">Detalle da liña da factura</span><span class="sxs-lookup"><span data-stu-id="cb1f1-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="cb1f1-146">Liña de diario</span><span class="sxs-lookup"><span data-stu-id="cb1f1-146">Journal Line</span></span>
  - <span data-ttu-id="cb1f1-147">Detalle da liña de contrato do proxecto</span><span class="sxs-lookup"><span data-stu-id="cb1f1-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="cb1f1-148">Membro do equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="cb1f1-148">Project Team Member</span></span>
  - <span data-ttu-id="cb1f1-149">Detalle da liña da oferta</span><span class="sxs-lookup"><span data-stu-id="cb1f1-149">Quote Line Detail</span></span>
  - <span data-ttu-id="cb1f1-150">Sobreprezo do prezo da función</span><span class="sxs-lookup"><span data-stu-id="cb1f1-150">Role Price Markup</span></span>
  - <span data-ttu-id="cb1f1-151">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="cb1f1-151">Role Price</span></span> 
  - <span data-ttu-id="cb1f1-152">Entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="cb1f1-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="cb1f1-153">Asegúrese de incluír todos os formularios e vistas para cada unha das entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="cb1f1-154">Cando se lle solicite incluír calquera entidade dependente para as entidades seleccionadas anteriormente, seleccione **Non**.</span><span class="sxs-lookup"><span data-stu-id="cb1f1-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

