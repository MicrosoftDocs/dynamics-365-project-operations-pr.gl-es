---
title: Reserva a un proxecto
description: Este tema fornece información sobre como reservar un recurso para un proxecto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908129"
---
# <a name="book-to-a-project"></a><span data-ttu-id="a5ac1-103">Reserva a un proxecto</span><span class="sxs-lookup"><span data-stu-id="a5ac1-103">Book to a project</span></span>

<span data-ttu-id="a5ac1-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="a5ac1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a5ac1-105">Hai ocasións nas que un xestor de proxectos ou un xestor de recursos necesitará asignar un recurso a un proxecto sen que un membro do equipo xenérico defina un requisito específico.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="a5ac1-106">Isto pódese conseguir de tres formas.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="a5ac1-107">Reservar desde a grade de membro do equipo</span><span class="sxs-lookup"><span data-stu-id="a5ac1-107">Book from the team member grid</span></span>
- <span data-ttu-id="a5ac1-108">Reservar desde o panel de programación</span><span class="sxs-lookup"><span data-stu-id="a5ac1-108">Book from the schedule board</span></span>
- <span data-ttu-id="a5ac1-109">Reservar desde o formulario **Project**</span><span class="sxs-lookup"><span data-stu-id="a5ac1-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="a5ac1-110">Reservar desde a grade de membro do equipo</span><span class="sxs-lookup"><span data-stu-id="a5ac1-110">Book from the team member grid</span></span>

<span data-ttu-id="a5ac1-111">Se a súa organización opera en modo híbrido de asignación de recursos, o xestor de proxectos pode reservar un recurso directamente no proxecto completando os seguintes pasos.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="a5ac1-112">No proxecto, vai á grade dos membros do equipo e seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="a5ac1-113">Definir o nome do posto e o rol do recurso.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="a5ac1-114">Seleccione o recurso reservable na busca dispoñible.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="a5ac1-115">Despois de seleccionar o recurso, defina a información dos seguintes campos para reservar o recurso:</span><span class="sxs-lookup"><span data-stu-id="a5ac1-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="a5ac1-116">Data de inicio</span><span class="sxs-lookup"><span data-stu-id="a5ac1-116">Start date</span></span>
    - <span data-ttu-id="a5ac1-117">Data de finalización</span><span class="sxs-lookup"><span data-stu-id="a5ac1-117">Finish date</span></span>
    - <span data-ttu-id="a5ac1-118">Método de atribución</span><span class="sxs-lookup"><span data-stu-id="a5ac1-118">Allocation method</span></span>
    - <span data-ttu-id="a5ac1-119">Horas, se procede</span><span class="sxs-lookup"><span data-stu-id="a5ac1-119">Hours, if applicable</span></span>
    - <span data-ttu-id="a5ac1-120">Responsable da aprobación do proxecto</span><span class="sxs-lookup"><span data-stu-id="a5ac1-120">Project approver</span></span>

6. <span data-ttu-id="a5ac1-121">Seleccione **Gardar e pechar**</span><span class="sxs-lookup"><span data-stu-id="a5ac1-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="a5ac1-122">Reservar desde o panel de programación</span><span class="sxs-lookup"><span data-stu-id="a5ac1-122">Book from the schedule board</span></span>

<span data-ttu-id="a5ac1-123">Cando un xestor de recursos necesita reservar un recurso directamente nun proxecto, pode usar o cadro de programación e o requisito do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="a5ac1-124">O requisito do proxecto é un requisito de recursos que sempre está dispoñible para ser reservado.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="a5ac1-125">Complete os seguintes pasos para facer unha reserva directamente a un proxecto desde o panel de programación.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="a5ac1-126">Desprácese ata o panel de programación e, na páxina esquerda, filtre os recursos que está considerando para o requisito.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="a5ac1-127">No panel inferior, seleccione o separador **Proxecto** para ver unha lista dos requisitos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="a5ac1-128">Arrastre o requisito a un recurso e defina a seguinte información:</span><span class="sxs-lookup"><span data-stu-id="a5ac1-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="a5ac1-129">Data de inicio</span><span class="sxs-lookup"><span data-stu-id="a5ac1-129">Start date</span></span>
    - <span data-ttu-id="a5ac1-130">Data de finalización</span><span class="sxs-lookup"><span data-stu-id="a5ac1-130">Finish date</span></span>
    - <span data-ttu-id="a5ac1-131">Estado da reserva</span><span class="sxs-lookup"><span data-stu-id="a5ac1-131">Booking status</span></span>
    - <span data-ttu-id="a5ac1-132">Método de reserva</span><span class="sxs-lookup"><span data-stu-id="a5ac1-132">Booking method</span></span>
    - <span data-ttu-id="a5ac1-133">Duración</span><span class="sxs-lookup"><span data-stu-id="a5ac1-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="a5ac1-134">Reservar desde o formulario Proxecto</span><span class="sxs-lookup"><span data-stu-id="a5ac1-134">Book from the Project form</span></span>

<span data-ttu-id="a5ac1-135">Como xestor de proxectos, é posible que necesite reservar un recurso para un proxecto, pero só coñece os criterios e non o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="a5ac1-136">Complete os seguintes pasos para usar o asistente de programación para atopar un recurso baseado en calquera atributo dispoñible do recurso.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="a5ac1-137">Desprácese ata o proxecto e seleccione **Reservar** para abrir o asistente de programación.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="a5ac1-138">Usando os filtros da parte esquerda do asistente de programación, restrinxa os criterios e seleccione **Buscar.**</span><span class="sxs-lookup"><span data-stu-id="a5ac1-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="a5ac1-139">En función dos recursos devoltos nos resultados, pode reservar un recurso.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="a5ac1-140">Este método non crea ningunha reserva para o recurso.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="a5ac1-141">No seu lugar, engade o recurso ao equipo.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="a5ac1-142">Despois de engadir o membro do equipo ao proxecto, o xestor do proxectos pode usar manter as reservas ou ampliar as reservas para engadir as reservas requiridas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="a5ac1-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
