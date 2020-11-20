---
title: Propoñer recursos do proxecto
description: Este tema fornece información sobre propoñer recursos de proxecto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120181"
---
# <a name="propose-project-resources"></a><span data-ttu-id="8cb06-103">Propoñer recursos do proxecto</span><span class="sxs-lookup"><span data-stu-id="8cb06-103">Propose project resources</span></span>

<span data-ttu-id="8cb06-104">Os xestores de recursos poden propoñer un recurso ao xestor de proxectos empregando unha solicitude de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cb06-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="8cb06-105">Na grade de solicitudes ou na propia solicitude, seleccione **Buscar recursos**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="8cb06-106">Na páxina **Asistente de programación**, seleccione o recurso e, a seguir, no panel **Crear reserva de recursos**, no campo **Estado da reserva**, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Recurso proposto seleccionado](media/Resource-Management-image62.png)

<span data-ttu-id="8cb06-108">Prodúcense as seguintes actualizacións de estado:</span><span class="sxs-lookup"><span data-stu-id="8cb06-108">The following status updates occur:</span></span>

- <span data-ttu-id="8cb06-109">Na páxina **Asistente de programación**, os indicadores de estado actualízanse para indicar que a reserva é unha proposta, non unha reserva dura.</span><span class="sxs-lookup"><span data-stu-id="8cb06-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indicadores de estado para a reserva proposta na páxina de Asistente de programación](media/Resource-Management-image63.png)

- <span data-ttu-id="8cb06-111">Na solicitude do recurso, o estado cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Estado de solicitude de recurso cambiado a Necesita revisión.](media/Resource-Management-image64.png)

- <span data-ttu-id="8cb06-113">No separador **Equipo** do proxecto, o valor **Estado da solicitude** do membro xenérico do equipo, o valor cambiase a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Estado da solicitude de membro xenérico de equipo cambiado a Necesita revisión no separador Equipo](media/Resource-Management-image48.png)

<span data-ttu-id="8cb06-115">O responsable do proxecto pode aceptar ou rexeitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="8cb06-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="8cb06-116">Cando os xestores de recursos procesan solicitudes de recursos, poden empregar calquera dos seguintes enfoques:</span><span class="sxs-lookup"><span data-stu-id="8cb06-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="8cb06-117">Propoñer múltiples recursos para satisfacer a demanda se non se dispón dun recurso único para cumprir as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="8cb06-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="8cb06-118">As horas propostas divídense entre varios recursos que poden satisfacer as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="8cb06-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="8cb06-119">Neste escenario, as horas non se poden solapar.</span><span class="sxs-lookup"><span data-stu-id="8cb06-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="8cb06-120">Propoñer menos recursos dos necesarios.</span><span class="sxs-lookup"><span data-stu-id="8cb06-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="8cb06-121">Neste escenario, a capacidade do recurso proposta é inferior ás horas requiridas que o solicitante especificou.</span><span class="sxs-lookup"><span data-stu-id="8cb06-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="8cb06-122">Polo tanto, cando o solicitante acepta os recursos propostos, créase un requisito de recursos non cumpridos para capturar a demanda restante.</span><span class="sxs-lookup"><span data-stu-id="8cb06-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="8cb06-123">Reserve múltiples recursos para satisfacer a demanda se non dispón dun recurso único para rematar o traballo.</span><span class="sxs-lookup"><span data-stu-id="8cb06-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="8cb06-124">Reserve menos recursos dos necesarios.</span><span class="sxs-lookup"><span data-stu-id="8cb06-124">Book fewer resources than are required.</span></span> <span data-ttu-id="8cb06-125">Neste escenario, as horas reservadas son menos que as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="8cb06-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="8cb06-126">O sistema guíalle para que propoña recursos en lugar de reservas para que o solicitante poida verificar e rastrexar da demanda restante.</span><span class="sxs-lookup"><span data-stu-id="8cb06-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="8cb06-127">Utilización facturable</span><span class="sxs-lookup"><span data-stu-id="8cb06-127">Billable utilization</span></span>

<span data-ttu-id="8cb06-128">Os recursos poden ter unha utilización facturable obxectivo.</span><span class="sxs-lookup"><span data-stu-id="8cb06-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="8cb06-129">Esta utilización obxectivo defínese como un atributo no rol predefinido dun recurso ou establécese no rexistro do recurso reservable individual.</span><span class="sxs-lookup"><span data-stu-id="8cb06-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="8cb06-130">Os cálculos de utilización baséanse nas horas reais que os recursos comunicaron mediante entradas de tempo aprobadas.</span><span class="sxs-lookup"><span data-stu-id="8cb06-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="8cb06-131">Para o cálculo da utilización úsanse as seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="8cb06-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="8cb06-132">Utilización facturable = (Horas reais imputables) ÷ (Capacidade do recurso).</span><span class="sxs-lookup"><span data-stu-id="8cb06-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="8cb06-133">Utilización non facturable = Tempo real con ID de tipo de facturación = Non imputable, Gratuíto ou Non dispoñible ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8cb06-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="8cb06-134">Interno = Tempo real sen contrato de vendas ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8cb06-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="8cb06-135">Capacidade do recurso = Horas laborables do recurso - Fóra de oficina - Días non laborables</span><span class="sxs-lookup"><span data-stu-id="8cb06-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="8cb06-136">Podes atopar a vista **Utilización de recursos** no panel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Visualización da utilización de recursos](media/Resource-Management-image65.png)

<span data-ttu-id="8cb06-138">Cada cela da grade representa a porcentaxe de utilización facturable do recurso nun período, como un día, unha semana ou un mes.</span><span class="sxs-lookup"><span data-stu-id="8cb06-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="8cb06-139">Para o color das celas úsanse as seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="8cb06-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="8cb06-140">**Verde:** Utilización facturable \>= Utilización obxectivo de recursos</span><span class="sxs-lookup"><span data-stu-id="8cb06-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="8cb06-141">**Amarelo:** Utilización de recursos – 20 \<= Utilización facturable \< Utilización objectivo</span><span class="sxs-lookup"><span data-stu-id="8cb06-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="8cb06-142">**Vermello:** Utilización facturable \< Utilización obxectivo – 20</span><span class="sxs-lookup"><span data-stu-id="8cb06-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="8cb06-143">Debido a que a vista **Utilización de recursos** está baseada no panel de programación, pode empregar as capacidades de filtrado do panel de programación para filtrar os seus resultados.</span><span class="sxs-lookup"><span data-stu-id="8cb06-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="8cb06-144">A grade require que estableza unha utilización obxectivo no rol ou o recurso individual.</span><span class="sxs-lookup"><span data-stu-id="8cb06-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="8cb06-145">Para configurar isto, vaia a **Recursos** \> **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="8cb06-146">Ademais, debe atribuírse un rol predefinido a cada recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="8cb06-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="8cb06-147">Vaia a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="8cb06-148">No separador **Project Service**, verifique se está definido un rol de recurso e que o campo **É predefinido** para el está configurado en **Si**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="8cb06-149">Pode engadir roles adicionais cando **É predefinido = Non**.</span><span class="sxs-lookup"><span data-stu-id="8cb06-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="8cb06-150">O rol cando **É predefinido = Si** úsase para avaliar a utilización do recurso fronte ao obxectivo para ese rol.</span><span class="sxs-lookup"><span data-stu-id="8cb06-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Rol predefinido establecido](media/Resource-Management-image67.png)

<span data-ttu-id="8cb06-152">No separador **Project Service**, tamén pode configurar unha utilización obxectivo individual para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8cb06-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="8cb06-153">A seguir, o cálculo de utilización usa esa utilización obxectivo para avaliar o obxectivo do recurso no canto do obxectivo do rol predefinido do recurso.</span><span class="sxs-lookup"><span data-stu-id="8cb06-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="8cb06-154">A utilización móstrase para un recurso só se ese recurso ten un tempo imputable acordado durante o período que se amosa na grade.</span><span class="sxs-lookup"><span data-stu-id="8cb06-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="8cb06-155">Dispoñibilidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8cb06-155">Resource availability</span></span>

<span data-ttu-id="8cb06-156">É fundamental que os xestores de recursos poidan ver a dispoñibilidade de recursos e actualizar as reservas.</span><span class="sxs-lookup"><span data-stu-id="8cb06-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="8cb06-157">Nalgúns casos, non hai unha demanda formal (solicitude de recursos), pero un xestor de recursos debe responder a unha demanda non planificada que chega por canles como un correo electrónico, chamada telefónica ou mensaxe instantánea.</span><span class="sxs-lookup"><span data-stu-id="8cb06-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="8cb06-158">Os xestores de recursos usan o panel de programación para actualizar recursos e reservas.</span><span class="sxs-lookup"><span data-stu-id="8cb06-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="8cb06-159">As horas laborables do recurso serven como base para calcular a dispoñibilidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="8cb06-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="8cb06-160">As reservas de recursos consumen a capacidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="8cb06-160">Resource bookings consume the capacity of the resources.</span></span>

![Panel de programación](media/Resource-Management-image68.png)

<span data-ttu-id="8cb06-162">O panel de programación usa cores e sombreados para amosar reservas, dispoñibilidade e saturacións, e tamén o estado das reservas.</span><span class="sxs-lookup"><span data-stu-id="8cb06-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="8cb06-163">Un axuste da configuración do panel de programación permítelle mostrar unha lenda.</span><span class="sxs-lookup"><span data-stu-id="8cb06-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="8cb06-164">Se aparece unha frecha apuntando á dereita xunto a un recurso reservable individual no panel de programación, pódese ampliar o recurso para mostrar detalles do traballo no que está reservado o recurso.</span><span class="sxs-lookup"><span data-stu-id="8cb06-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Engadir o recurso reservable expandido no panel de programación](media/Resource-Management-image69.png)

<span data-ttu-id="8cb06-166">Debido a que Dynamics 365 Project Service Automation usa o motor de Universal Resource Scheduling, se tamén ten Dynamics 365 Field Service instalado, pode ver os detalles das reservas de recursos para proxectos, pedidos de traballo e calquera outra entidade á que estendeu a programación.</span><span class="sxs-lookup"><span data-stu-id="8cb06-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detalles de reservas de recursos para proxectos e pedidos de traballo](media/Resource-Management-image70.png)

<span data-ttu-id="8cb06-168">Para ver máis detalles sobre un recurso individual, prema co botón dereito sobre el para abrir a tarxeta do recurso.</span><span class="sxs-lookup"><span data-stu-id="8cb06-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Tarxeta de recurso](media/Resource-Management-image71.png)
