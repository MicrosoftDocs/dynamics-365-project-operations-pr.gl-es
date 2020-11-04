---
title: Revisar os recursos propostos
description: Este tema fornece información sobre como propoñer recursos de proxecto.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076099"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="5cc5b-103">Revisar os recursos propostos</span><span class="sxs-lookup"><span data-stu-id="5cc5b-103">Review proposed resources</span></span>

<span data-ttu-id="5cc5b-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="5cc5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5cc5b-105">Os xestores de recursos poden propoñer un recurso ao xestor de proxectos empregando unha solicitude de recursos.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="5cc5b-106">Na grade de solicitudes ou na propia solicitude, seleccione **Buscar recursos**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="5cc5b-107">Na páxina **Asistente de programación** , seleccione o recurso e, a seguir, no panel **Crear reserva de recursos** , no campo **Estado da reserva** , seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="5cc5b-108">Prodúcense as seguintes actualizacións de estado:</span><span class="sxs-lookup"><span data-stu-id="5cc5b-108">The following status updates occur:</span></span>

- <span data-ttu-id="5cc5b-109">Na páxina **Asistente de programación** , os indicadores de estado actualízanse para indicar que a reserva é unha proposta, non unha reserva dura.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="5cc5b-110">Na solicitude do recurso, o estado cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="5cc5b-111">No separador **Equipo** do proxecto, o valor **Estado da solicitude** do membro xenérico do equipo, o valor cambiase a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="5cc5b-112">O responsable do proxecto pode aceptar ou rexeitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="5cc5b-113">Cando os xestores de recursos procesan solicitudes de recursos, poden empregar calquera dos seguintes enfoques:</span><span class="sxs-lookup"><span data-stu-id="5cc5b-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="5cc5b-114">Propoñer múltiples recursos para satisfacer a demanda se non se dispón dun recurso único para cumprir as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="5cc5b-115">As horas propostas divídense entre varios recursos que poden satisfacer as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="5cc5b-116">Neste escenario, as horas non se poden solapar.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="5cc5b-117">Propoñer menos recursos dos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="5cc5b-118">Neste escenario, a capacidade do recurso proposta é inferior ás horas requiridas que o solicitante especificou.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="5cc5b-119">Polo tanto, cando o solicitante acepta os recursos propostos, créase un requisito de recursos non cumpridos para capturar a demanda restante.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="5cc5b-120">Reserve múltiples recursos para satisfacer a demanda se non dispón dun recurso único para rematar o traballo.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="5cc5b-121">Reserve menos recursos dos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-121">Book fewer resources than are required.</span></span> <span data-ttu-id="5cc5b-122">Neste escenario, as horas reservadas son menos que as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="5cc5b-123">O sistema guíalle para que propoña recursos en lugar de reservas para que o solicitante poida verificar e rastrexar da demanda restante.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="5cc5b-124">Utilización facturable</span><span class="sxs-lookup"><span data-stu-id="5cc5b-124">Billable utilization</span></span>

<span data-ttu-id="5cc5b-125">Os recursos poden ter unha utilización facturable obxectivo.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="5cc5b-126">Esta utilización obxectivo defínese como un atributo no rol predefinido dun recurso ou establécese no rexistro do recurso reservable individual.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="5cc5b-127">Os cálculos de utilización baséanse nas horas reais que os recursos comunicaron mediante entradas de tempo aprobadas.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="5cc5b-128">Para o cálculo da utilización úsanse as seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="5cc5b-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="5cc5b-129">Utilización facturable = (Horas reais imputables) ÷ (Capacidade do recurso).</span><span class="sxs-lookup"><span data-stu-id="5cc5b-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="5cc5b-130">Utilización non facturable = Tempo real con ID de tipo de facturación = Non imputable, Gratuíto ou Non dispoñible ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5cc5b-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="5cc5b-131">Interno = Tempo real sen contrato de vendas ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5cc5b-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="5cc5b-132">Capacidade do recurso = Horas laborables do recurso - Fóra de oficina - Días non laborables</span><span class="sxs-lookup"><span data-stu-id="5cc5b-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="5cc5b-133">Podes atopar a vista **Utilización de recursos** no panel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="5cc5b-134">Cada cela da grade representa a porcentaxe de utilización facturable do recurso nun período, como un día, unha semana ou un mes.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="5cc5b-135">Para o color das celas úsanse as seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="5cc5b-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="5cc5b-136">**Verde:** Utilización facturable \>= Utilización obxectivo de recursos</span><span class="sxs-lookup"><span data-stu-id="5cc5b-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="5cc5b-137">**Amarelo:** Utilización de recursos – 20 \<= Utilización facturable \< Utilización objectivo</span><span class="sxs-lookup"><span data-stu-id="5cc5b-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="5cc5b-138">**Vermello:** Utilización facturable \< Utilización obxectivo – 20</span><span class="sxs-lookup"><span data-stu-id="5cc5b-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="5cc5b-139">Debido a que a vista **Utilización de recursos** está baseada no panel de programación, pode empregar as capacidades de filtrado do panel de programación para filtrar os seus resultados.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="5cc5b-140">A grade require que estableza unha utilización obxectivo no rol ou o recurso individual.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="5cc5b-141">Para configurar isto, vaia a **Recursos** \> **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="5cc5b-142">Ademais, debe atribuírse un rol predefinido a cada recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="5cc5b-143">Vaia a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="5cc5b-144">No separador **Project Service** , verifique se está definido un rol de recurso e que o campo **É predefinido** para el está configurado en **Si**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="5cc5b-145">Pode engadir roles adicionais cando **É predefinido = Non**.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="5cc5b-146">O rol cando **É predefinido = Si** úsase para avaliar a utilización do recurso fronte ao obxectivo para ese rol.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="5cc5b-147">No separador **Project Service** , tamén pode configurar unha utilización obxectivo individual para o recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="5cc5b-148">A seguir, o cálculo de utilización usa esa utilización obxectivo para avaliar o obxectivo do recurso no canto do obxectivo do rol predefinido do recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="5cc5b-149">A utilización móstrase para un recurso só se ese recurso ten un tempo imputable acordado durante o período que se amosa na grade.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="5cc5b-150">Dispoñibilidade de recursos</span><span class="sxs-lookup"><span data-stu-id="5cc5b-150">Resource availability</span></span>

<span data-ttu-id="5cc5b-151">É fundamental que os xestores de recursos poidan ver a dispoñibilidade de recursos e actualizar as reservas.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="5cc5b-152">Nalgúns casos, non hai unha demanda formal (solicitude de recursos), pero un xestor de recursos debe responder a unha demanda non planificada que chega por canles como un correo electrónico, chamada telefónica ou mensaxe instantánea.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="5cc5b-153">Os xestores de recursos usan o panel de programación para actualizar recursos e reservas.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="5cc5b-154">As horas laborables do recurso serven como base para calcular a dispoñibilidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="5cc5b-155">As reservas de recursos consumen a capacidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="5cc5b-156">O panel de programación usa cores e sombreados para amosar reservas, dispoñibilidade e saturacións, e tamén o estado das reservas.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="5cc5b-157">Un axuste da configuración do panel de programación permítelle mostrar unha lenda.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="5cc5b-158">Se aparece unha frecha apuntando á dereita xunto a un recurso reservable individual no panel de programación, pódese ampliar o recurso para mostrar detalles do traballo no que está reservado o recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="5cc5b-159">Debido a que Dynamics 365 Project Operations usa o motor de Universal Resource Scheduling, se tamén ten Dynamics 365 Field Service instalado, pode ver os detalles das reservas de recursos para proxectos, pedidos de traballo e calquera outra entidade á que estendeu a programación.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="5cc5b-160">Para ver máis detalles sobre un recurso individual, prema co botón dereito sobre el para abrir a tarxeta do recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc5b-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

