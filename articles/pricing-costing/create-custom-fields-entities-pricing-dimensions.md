---
title: Crear campos e entidades personalizados como dimensións de prezos
description: Este tema ofrece información sobre como crear conxuntos de opcións ou entidades personalizados.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000524"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="5cd27-103">Crear campos e entidades personalizados como dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="5cd27-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="5cd27-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="5cd27-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5cd27-105">Realice os seguintes pasos cando queira crear un conxunto de opcións ou unha entidade personalizada para usala como dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="5cd27-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="5cd27-106">Para obter máis información, consulte [Visión xeral das dimensións de prezos](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5cd27-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="5cd27-107">Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada.</span><span class="sxs-lookup"><span data-stu-id="5cd27-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="5cd27-108">Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios cando sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="5cd27-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="5cd27-109">Isto tamén axudará á reutilización do seu traballo e facilitará o traslado destes cambios a outra instancia. Despois de facer todos os cambios necesarios, exporte esta solución como **Solución administrada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.</span><span class="sxs-lookup"><span data-stu-id="5cd27-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="5cd27-110">Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="5cd27-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="5cd27-111">Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade.</span><span class="sxs-lookup"><span data-stu-id="5cd27-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="5cd27-112">Ambos deben crearse na súa solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="5cd27-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="5cd27-113">Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="5cd27-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="5cd27-114">Dimensións baseada en entidade</span><span class="sxs-lookup"><span data-stu-id="5cd27-114">Entity-based dimensions</span></span>
<span data-ttu-id="5cd27-115">Para crear dimensións baseadas en entidade, siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="5cd27-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="5cd27-116">Vaia a **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="5cd27-117">No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="5cd27-118">Seleccione **Nova** para crear unha nova entidade chamada **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="5cd27-119">Introduza a información necesaria restante e, a seguir, seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definición de entidade de título estándar](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="5cd27-121">Dimensións baseadas en conxunto de opcións</span><span class="sxs-lookup"><span data-stu-id="5cd27-121">Option set-based dimensions</span></span> 
<span data-ttu-id="5cd27-122">Pode crear dúas dimensións baseadas en conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="5cd27-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="5cd27-123">Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo na localización **Casa** e o traballo **No sitio**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="5cd27-124">Utilice **Horas de traballo do recurso** con valores **Normal** e **Horas extra** para aplicar un sobreprezo cando remate o traballo.</span><span class="sxs-lookup"><span data-stu-id="5cd27-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="5cd27-125">O seguinte gráfico ofrece unha vista da dimensión **Localización do traballo do recurso**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensión de prezos baseada en conxunto de opcións chamada Localización do traballo do recurso](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="5cd27-127">O seguinte gráfico ofrece unha vista da dimensión **Horas de traballo do recurso**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensión de prezos baseada en conxunto de opcións chamada Horas de traballo do recurso](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="5cd27-129">Vaia a **Configuración** > **Solucións** e prema dúas veces **\<your organization name> dimensións de prezos**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="5cd27-130">No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="5cd27-131">Seleccione **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="5cd27-132">Crear datos para dimensións baseadas en entidade</span><span class="sxs-lookup"><span data-stu-id="5cd27-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="5cd27-133">Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo.</span><span class="sxs-lookup"><span data-stu-id="5cd27-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="5cd27-134">Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="5cd27-135">Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="5cd27-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="5cd27-136">Seleccione **Busca avanzada**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="5cd27-137">Seleccione a entidade **Título estándar** e logo seleccione **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="5cd27-138">Mostraranse todas as filas na entidade **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="5cd27-139">Seleccione **Novo** e no campo **Nome** introduza "Enxeñeiro de sistemas" e logo seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="5cd27-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="5cd27-140">Peche a páxina.</span><span class="sxs-lookup"><span data-stu-id="5cd27-140">Close the page.</span></span> 
5. <span data-ttu-id="5cd27-141">Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".</span><span class="sxs-lookup"><span data-stu-id="5cd27-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Datos de exemplo para a entidade Título estándar](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]