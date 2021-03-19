---
title: Crear unha solución para as dimensións de prezos personalizadas
description: Este tema fornece información sobre como crear solucións para dimensións de prezos personalizadas.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278416"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="9218b-103">Crear unha solución para as dimensións de prezos personalizadas</span><span class="sxs-lookup"><span data-stu-id="9218b-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="9218b-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="9218b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="9218b-105">Todos os cambios de dimensións de prezos personalizadas deberían estar nunha solución separada.</span><span class="sxs-lookup"><span data-stu-id="9218b-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="9218b-106">Esta importante boa práctica permite a flexibilidade para actualizar ou eliminar os cambios segundo sexa necesario, axuda á reutilización do seu traballo e facilita levar estes cambios a outras instancias.</span><span class="sxs-lookup"><span data-stu-id="9218b-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="9218b-107">Despois de facer todos os cambios necesarios, exporte esta solución como unha solución **Xestionada** e logo impórtea a outras instancias para a súa reutilización.</span><span class="sxs-lookup"><span data-stu-id="9218b-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="9218b-108">Crear unha solución para as dimensións de prezos personalizadas</span><span class="sxs-lookup"><span data-stu-id="9218b-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="9218b-109">Seleccione **Configuración** > **Solucións** e logo seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="9218b-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="9218b-110">Poña nome á solución, *Dimensións de prezos de <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="9218b-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="9218b-111">Introduza a información necesaria restante e, a seguir, seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="9218b-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Creación dunha solución de dimensión de prezos personalizada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="9218b-113">Engadir todas as entidades requiridas e os compoñentes relacionados á solución de dimensión de prezos</span><span class="sxs-lookup"><span data-stu-id="9218b-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="9218b-114">Engada as seguintes entidades de Project Service á súa solución de prezos para facer cambios importantes no esquema da solución de prezos.</span><span class="sxs-lookup"><span data-stu-id="9218b-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="9218b-115">Despois de completar este procedemento, as entidades recoñecerán as novas dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="9218b-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="9218b-116">Seleccione **Configuración** > **Solucións** e logo prema dúas veces en **Dimensións de prezos de <*nome da súa organización*>**.</span><span class="sxs-lookup"><span data-stu-id="9218b-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="9218b-117">No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="9218b-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="9218b-118">Na caixa de diálogo **Compoñentes da solución**, seleccione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="9218b-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="9218b-119">**Dato real**</span><span class="sxs-lookup"><span data-stu-id="9218b-119">**Actual**</span></span>
   - <span data-ttu-id="9218b-120">**Recurso reservable**</span><span class="sxs-lookup"><span data-stu-id="9218b-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="9218b-121">**Liña de estimación**</span><span class="sxs-lookup"><span data-stu-id="9218b-121">**Estimate Line**</span></span>
   - <span data-ttu-id="9218b-122">**Tarefa do proxecto**</span><span class="sxs-lookup"><span data-stu-id="9218b-122">**Project Task**</span></span>
   - <span data-ttu-id="9218b-123">**Detalle da liña da factura**</span><span class="sxs-lookup"><span data-stu-id="9218b-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="9218b-124">**Liña de diario**</span><span class="sxs-lookup"><span data-stu-id="9218b-124">**Journal Line**</span></span>
   - <span data-ttu-id="9218b-125">**Detalle da liña de contrato do proxecto**</span><span class="sxs-lookup"><span data-stu-id="9218b-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="9218b-126">**Membro do equipo do proxecto**</span><span class="sxs-lookup"><span data-stu-id="9218b-126">**Project Team Member**</span></span>
   - <span data-ttu-id="9218b-127">**Detalle da liña da oferta**</span><span class="sxs-lookup"><span data-stu-id="9218b-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="9218b-128">**Sobreprezo do prezo da función**</span><span class="sxs-lookup"><span data-stu-id="9218b-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="9218b-129">**Prezo do rol**</span><span class="sxs-lookup"><span data-stu-id="9218b-129">**Role Price**</span></span>
   - <span data-ttu-id="9218b-130">**Entrada de tempo**</span><span class="sxs-lookup"><span data-stu-id="9218b-130">**Time Entry**</span></span>
 
   ![Engadir entidades existentes á solución de dimensións de prezos personalizada](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="9218b-132">Para cada entidade, revise os compoñentes que se engaden e a lista final de activos da entidade para cada entidade.</span><span class="sxs-lookup"><span data-stu-id="9218b-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="9218b-133">Inclúa todos os formularios e vistas para cada unha das entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="9218b-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entidades engadidas](./media/solution-component-selection.png)


5.  <span data-ttu-id="9218b-135">Cando se lle solicite que inclúa entidades dependentes para as entidades seleccionadas, seleccione **Non, non incluír os compoñentes necesarios.**</span><span class="sxs-lookup"><span data-stu-id="9218b-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Inclusión de entidades dependentes](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]