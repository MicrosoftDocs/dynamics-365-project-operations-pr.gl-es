---
title: Ver a utilización imputable de recursos
description: Este tema fornece información sobre a vista de utilización de recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122161"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="c79f1-103">Ver a utilización imputable de recursos</span><span class="sxs-lookup"><span data-stu-id="c79f1-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="c79f1-104">A **Vista de utilización** na páxina **Utilización de recursos de Project Service** a páxina mostra a utilización imputable por cada recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="c79f1-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="c79f1-105">Porque a vista está baseada no panel de programación, de forma que atopará moitas das mesmas funcións.</span><span class="sxs-lookup"><span data-stu-id="c79f1-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Captura da visualización de utilización](media/FAQ-utilization-1.png)
 

<span data-ttu-id="c79f1-107">O cálculo da utilización imputable funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c79f1-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="c79f1-108">Utilización imputable = (Horas reais imputables) / (capacidade do recurso).</span><span class="sxs-lookup"><span data-stu-id="c79f1-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="c79f1-109">O celas representan a utilización imputable calculada para o período seleccionado (días, semanas ou meses).</span><span class="sxs-lookup"><span data-stu-id="c79f1-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="c79f1-110">As cores en cada cela mostrar a utilización imputable para un recurso comparada coa utilización imputable de destino.</span><span class="sxs-lookup"><span data-stu-id="c79f1-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="c79f1-111">A utilization de destino pódese definir no rol predefinido do recurso ou no recurso individual.</span><span class="sxs-lookup"><span data-stu-id="c79f1-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="c79f1-112">O cálculo busca no individual o destino en primeiro lugar e, a seguir, no rol predefinido do recurso.</span><span class="sxs-lookup"><span data-stu-id="c79f1-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="c79f1-113">Establecer o destino nun recurso</span><span class="sxs-lookup"><span data-stu-id="c79f1-113">Set target on a resource</span></span>

1. <span data-ttu-id="c79f1-114">Vaia a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c79f1-115">Seleccione un recurso para abrir o rexistro.</span><span class="sxs-lookup"><span data-stu-id="c79f1-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="c79f1-116">No separador **Project Service**, pode definir a utilización obxectivo do recurso.</span><span class="sxs-lookup"><span data-stu-id="c79f1-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Captura de utilizar o separador Project Service para definir a utilización de destino](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="c79f1-118">Estableza a utilización obxectivo nun rol</span><span class="sxs-lookup"><span data-stu-id="c79f1-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="c79f1-119">Vaia a **Recursos** \> **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c79f1-120">Seleccione un rol e abra o rexistro.</span><span class="sxs-lookup"><span data-stu-id="c79f1-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="c79f1-121">Defina a utilización de destino para o rol.</span><span class="sxs-lookup"><span data-stu-id="c79f1-121">Set the target utilization for the role.</span></span>

> ![Captura de utilizar os roles de recursos para definir a utilización de destino](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="c79f1-123">Calcular a utilización imputable dun recurso</span><span class="sxs-lookup"><span data-stu-id="c79f1-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="c79f1-124">Para calcular a utilización imputable para un recurso, terá que cumprir algúns requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="c79f1-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="c79f1-125">Estableza o rol por defecto para cada recurso individual</span><span class="sxs-lookup"><span data-stu-id="c79f1-125">Set default role for individual resource</span></span>

<span data-ttu-id="c79f1-126">En primeiro lugar, a utilización obxectivo debe definirse no recurso individual ou nos roles do recurso.</span><span class="sxs-lookup"><span data-stu-id="c79f1-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="c79f1-127">Se está a usar roles de recursos para destinos, cada recurso individual debe ter un rol predefinido.</span><span class="sxs-lookup"><span data-stu-id="c79f1-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="c79f1-128">Para definir isto, vaia a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c79f1-129">Seleccione un recurso, abra o rexistro e logo seleccione o separador **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="c79f1-130">Na grade **Rol do recurso**, comprobe que hai un rol para o recurso e que **É predefinido** está configurado en **Si**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="c79f1-131">Cambiar tipo de facturación deste rol do recurso</span><span class="sxs-lookup"><span data-stu-id="c79f1-131">Change billing type for resource role</span></span>

<span data-ttu-id="c79f1-132">Os roles de recurso deben definirse para ter un tipo de facturación **Imputable**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="c79f1-133">Vaia a **Recursos** \> **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c79f1-134">Abra o rexistro que quere actualizar e, a seguir, defina o tipo de facturación predefinido en **Imputable**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="c79f1-135">Definir as horas laborables para o rol de recurso</span><span class="sxs-lookup"><span data-stu-id="c79f1-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="c79f1-136">O recurso debe ter horas de traballo para o cálculo de capacidade.</span><span class="sxs-lookup"><span data-stu-id="c79f1-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="c79f1-137">Vaia a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c79f1-138">Seleccione un recurso para abrir o rexistro e, a seguir, seleccione **Mostrar horas laborables**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="c79f1-139">Pode actualizar en masa a lista de recursos aplicándolles un **Modelo de horas de traballo** desde a visualización de **Lista de recursos**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="c79f1-140">Resolución de problemas de horas reais imputables</span><span class="sxs-lookup"><span data-stu-id="c79f1-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="c79f1-141">As horas reais imputables orixínanse da entidade **Valores reais**.</span><span class="sxs-lookup"><span data-stu-id="c79f1-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="c79f1-142">Os valores reais co tipo de facturación **Imputable** están incluídos no cálculo e, por este motivo, debe ter proxectos onde os valores reais son imputables.</span><span class="sxs-lookup"><span data-stu-id="c79f1-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="c79f1-143">Se non está a ver a utilización imputable, ofrecémoslle algunhas cousas pode comprobar:</span><span class="sxs-lookup"><span data-stu-id="c79f1-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="c79f1-144">O recurso ten horas laborables definidas para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="c79f1-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="c79f1-145">O recurso ten en un destino de utilización individualmente definido ou ten un rol predefinido atribuído.</span><span class="sxs-lookup"><span data-stu-id="c79f1-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="c79f1-146">O rol ten un destino de utilización definido.</span><span class="sxs-lookup"><span data-stu-id="c79f1-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="c79f1-147">Os valores reais teñen un tipo de facturación **Imputable** para o período do que espera un cálculo de utilización.</span><span class="sxs-lookup"><span data-stu-id="c79f1-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="c79f1-148">Comprobe o seguinte se está a ver os valores reais con tipos de facturación que non sexan imputables:</span><span class="sxs-lookup"><span data-stu-id="c79f1-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="c79f1-149">O rol utilizado no valor real ten un tipo de facturación predefinido que non é imputable.</span><span class="sxs-lookup"><span data-stu-id="c79f1-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="c79f1-150">O rol na liña de contrato do proxecto que fai de copia de seguranza do proxecto está definido en non imputable.</span><span class="sxs-lookup"><span data-stu-id="c79f1-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="c79f1-151">O proxecto non ten unha liña de contrato asociada.</span><span class="sxs-lookup"><span data-stu-id="c79f1-151">The project does not have an associated contract line.</span></span>

