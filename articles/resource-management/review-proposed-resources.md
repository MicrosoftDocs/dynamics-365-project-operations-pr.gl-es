---
title: Revisar os recursos propostos
description: Este tema fornece información sobre como propoñer recursos de proxecto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401171"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="0d466-103">Revisar os recursos propostos</span><span class="sxs-lookup"><span data-stu-id="0d466-103">Review proposed resources</span></span>

<span data-ttu-id="0d466-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="0d466-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d466-105">Os xestores de recursos poden propoñer un recurso ao xestor de proxectos empregando unha solicitude de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d466-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="0d466-106">Na grade de solicitudes ou na propia solicitude, seleccione **Buscar recursos**.</span><span class="sxs-lookup"><span data-stu-id="0d466-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="0d466-107">Na páxina **Asistente de programación**, seleccione o recurso e, a seguir, no panel **Crear reserva de recursos**, no campo **Estado da reserva**, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="0d466-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="0d466-108">Prodúcense as seguintes actualizacións de estado:</span><span class="sxs-lookup"><span data-stu-id="0d466-108">The following status updates occur:</span></span>

- <span data-ttu-id="0d466-109">Na páxina **Asistente de programación**, os indicadores de estado actualízanse para indicar que a reserva é unha proposta, non unha reserva dura.</span><span class="sxs-lookup"><span data-stu-id="0d466-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="0d466-110">Na solicitude do recurso, o estado cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="0d466-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="0d466-111">No separador **Equipo** do proxecto, o valor **Estado da solicitude** do membro xenérico do equipo, o valor cambiase a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="0d466-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="0d466-112">O responsable do proxecto pode aceptar ou rexeitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="0d466-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="0d466-113">Cando os xestores de recursos procesan solicitudes de recursos, poden empregar calquera dos seguintes enfoques:</span><span class="sxs-lookup"><span data-stu-id="0d466-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="0d466-114">Propoñer múltiples recursos para satisfacer a demanda se non se dispón dun recurso único para cumprir as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="0d466-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="0d466-115">As horas propostas divídense entre varios recursos que poden satisfacer as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="0d466-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="0d466-116">Neste escenario, as horas non se poden solapar.</span><span class="sxs-lookup"><span data-stu-id="0d466-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="0d466-117">Propoñer menos recursos dos necesarios.</span><span class="sxs-lookup"><span data-stu-id="0d466-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="0d466-118">Neste escenario, a capacidade do recurso proposta é inferior ás horas requiridas que o solicitante especificou.</span><span class="sxs-lookup"><span data-stu-id="0d466-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="0d466-119">Polo tanto, cando o solicitante acepta os recursos propostos, créase un requisito de recursos non cumpridos para capturar a demanda restante.</span><span class="sxs-lookup"><span data-stu-id="0d466-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="0d466-120">Reserve múltiples recursos para satisfacer a demanda se non dispón dun recurso único para rematar o traballo.</span><span class="sxs-lookup"><span data-stu-id="0d466-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="0d466-121">Reserve menos recursos dos necesarios.</span><span class="sxs-lookup"><span data-stu-id="0d466-121">Book fewer resources than are required.</span></span> <span data-ttu-id="0d466-122">Neste escenario, as horas reservadas son menos que as horas requiridas.</span><span class="sxs-lookup"><span data-stu-id="0d466-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="0d466-123">O sistema guíalle para que propoña recursos en lugar de reservas para que o solicitante poida verificar e rastrexar da demanda restante.</span><span class="sxs-lookup"><span data-stu-id="0d466-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="0d466-124">Dispoñibilidade de recursos</span><span class="sxs-lookup"><span data-stu-id="0d466-124">Resource availability</span></span>

<span data-ttu-id="0d466-125">É fundamental que os xestores de recursos poidan ver a dispoñibilidade de recursos e actualizar as reservas.</span><span class="sxs-lookup"><span data-stu-id="0d466-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="0d466-126">Nalgúns casos, non hai unha demanda formal (solicitude de recursos), pero un xestor de recursos debe responder a unha demanda non planificada que chega por canles como un correo electrónico, chamada telefónica ou mensaxe instantánea.</span><span class="sxs-lookup"><span data-stu-id="0d466-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="0d466-127">Os xestores de recursos usan o panel de programación para actualizar recursos e reservas.</span><span class="sxs-lookup"><span data-stu-id="0d466-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="0d466-128">As horas laborables do recurso serven como base para calcular a dispoñibilidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="0d466-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="0d466-129">As reservas de recursos consumen a capacidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="0d466-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="0d466-130">O panel de programación usa cores e sombreados para amosar reservas, dispoñibilidade e saturacións, e tamén o estado das reservas.</span><span class="sxs-lookup"><span data-stu-id="0d466-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="0d466-131">Un axuste da configuración do panel de programación permítelle mostrar unha lenda.</span><span class="sxs-lookup"><span data-stu-id="0d466-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="0d466-132">Se aparece unha frecha apuntando á dereita xunto a un recurso reservable individual no panel de programación, pódese ampliar o recurso para mostrar detalles do traballo no que está reservado o recurso.</span><span class="sxs-lookup"><span data-stu-id="0d466-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="0d466-133">Debido a que Dynamics 365 Project Operations usa o motor de Universal Resource Scheduling, se tamén ten Dynamics 365 Field Service instalado, pode ver os detalles das reservas de recursos para proxectos, pedidos de traballo e calquera outra entidade á que estendeu a programación.</span><span class="sxs-lookup"><span data-stu-id="0d466-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="0d466-134">Para ver máis detalles sobre un recurso individual, prema co botón dereito sobre el para abrir a tarxeta do recurso.</span><span class="sxs-lookup"><span data-stu-id="0d466-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

