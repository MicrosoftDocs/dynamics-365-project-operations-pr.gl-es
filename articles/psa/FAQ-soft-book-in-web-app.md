---
title: Como podo facer unha "reserva branda" de recursos na versión da apl. 2.x?
description: Este artigo describe como facer unha reserva branda de membros de proxecto con Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 413783d2386cccd98cfe216a7c7300a5b7f771ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992893"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="9657d-103">Como podo facer unha "reserva branda" de recursos na aplicación web (aplicación Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="9657d-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9657d-104">Provisionalmente, pode programar ou facer unha "reserva blanda" dun recurso nun equipo de proxecto para informar de que ten intención de atribuír o recurso a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="9657d-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="9657d-105">As reservas brandas non consumen a capacidade dispoñible dun recurso.</span><span class="sxs-lookup"><span data-stu-id="9657d-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="9657d-106">Non se poden atribuír os membros do equipo cunha reserva branda para tarefas de proxecto.</span><span class="sxs-lookup"><span data-stu-id="9657d-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="9657d-107">Só os recursos co estado Reserva dura e tipo de compromiso Comprometido poden ser atribuídos a tarefas (sempre que teñan suficientes horas de reserva dura para cubrir o esforzo da atribución).</span><span class="sxs-lookup"><span data-stu-id="9657d-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="9657d-108">Os membros do equipo de proxecto con reserva branda aparecen na grade Membro do equipo con as súas horas de reserva branda mostradas na columna Reserva branda.</span><span class="sxs-lookup"><span data-stu-id="9657d-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="9657d-109">Tamén se mostran no panel de programación.</span><span class="sxs-lookup"><span data-stu-id="9657d-109">They also show up on the schedule board.</span></span> <span data-ttu-id="9657d-110">De novo, non indican calquer consumo de capacidade, xa que a reserva branda non consume a capacidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="9657d-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="9657d-111">Existen tres maneiras de facer unha reserva branda dun membro do equipo nun proxecto coa versión de Project Service 2.x.</span><span class="sxs-lookup"><span data-stu-id="9657d-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="9657d-112">Pode facer unha reserva branda co panel de programación, utilizar a funcionalidade Manter reservas ou crear un recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="9657d-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="9657d-113">Estes métodos se describen debaixo.</span><span class="sxs-lookup"><span data-stu-id="9657d-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="9657d-114">Reserva branda co panel de programación</span><span class="sxs-lookup"><span data-stu-id="9657d-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="9657d-115">Siga este procedemento para facer unha reserva branda co panel de programación:</span><span class="sxs-lookup"><span data-stu-id="9657d-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="9657d-116">Abrir o panel de programación.</span><span class="sxs-lookup"><span data-stu-id="9657d-116">Open the schedule board.</span></span>
2. <span data-ttu-id="9657d-117">Seleccionar o separador Proxecto na parte inferior do panel Requisitos de reserva do panel de programación.</span><span class="sxs-lookup"><span data-stu-id="9657d-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="9657d-118">Localice o proxecto no que desexa facer unha reserva branda.</span><span class="sxs-lookup"><span data-stu-id="9657d-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="9657d-119">Se ten moitos proxectos, prema no título da columna Proxecto e, a seguir, utilice o filtro para encontrar o proxecto.</span><span class="sxs-lookup"><span data-stu-id="9657d-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="9657d-120">Prema no proxecto, a seguir, arrástreo e sólteo na grade de hora do recurso.</span><span class="sxs-lookup"><span data-stu-id="9657d-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="9657d-121">Isto abre o panel de Crear unha reserva de recurso á dereita.</span><span class="sxs-lookup"><span data-stu-id="9657d-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="9657d-122">Axuste a data de inicio e fin, seleccione o Estado de reserva como brando e defina as horas.</span><span class="sxs-lookup"><span data-stu-id="9657d-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="9657d-123">Prema Reservar.</span><span class="sxs-lookup"><span data-stu-id="9657d-123">Click Book.</span></span>
7. <span data-ttu-id="9657d-124">No proxecto, o recurso agora aparecerá como membro do equipo coas horas con reserva branda na columna Reserva branda.</span><span class="sxs-lookup"><span data-stu-id="9657d-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="9657d-125">Teña en conta que non pode atribuírlle a tarefas na estrutura de subdivisión do traballo (WBS) xa que os recursos deben ter unha reserva dura no equipo para ser atribuídos.</span><span class="sxs-lookup"><span data-stu-id="9657d-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="9657d-126">Reserva branda utilizando a funcionalidade Manter reservas</span><span class="sxs-lookup"><span data-stu-id="9657d-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="9657d-127">Siga este procedemento para facer unha reserva branda con Manter reservas:</span><span class="sxs-lookup"><span data-stu-id="9657d-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="9657d-128">Na grade de membro do equipo, prema Novo.</span><span class="sxs-lookup"><span data-stu-id="9657d-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="9657d-129">Seleccione o recurso reservable, rol, desde/para.</span><span class="sxs-lookup"><span data-stu-id="9657d-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="9657d-130">Seleccione un método de atribución que non sexa Ningún:</span><span class="sxs-lookup"><span data-stu-id="9657d-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="9657d-131">Capacidade completa</span><span class="sxs-lookup"><span data-stu-id="9657d-131">Full Capacity</span></span>
- <span data-ttu-id="9657d-132">Capacidade da porcentaxe</span><span class="sxs-lookup"><span data-stu-id="9657d-132">Percentage Capacity</span></span>
- <span data-ttu-id="9657d-133">Por horas: distribuír uniformemente</span><span class="sxs-lookup"><span data-stu-id="9657d-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="9657d-134">Por horas: carga frontal</span><span class="sxs-lookup"><span data-stu-id="9657d-134">By Hours Front Load</span></span>
4. <span data-ttu-id="9657d-135">Prema Gardar.</span><span class="sxs-lookup"><span data-stu-id="9657d-135">Click Save.</span></span> <span data-ttu-id="9657d-136">Tamén verá o recurso na grade do equipo e as súas horas indicadas como Dura.</span><span class="sxs-lookup"><span data-stu-id="9657d-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="9657d-137">Manter as reservas de recursos premendo Manter reservas.</span><span class="sxs-lookup"><span data-stu-id="9657d-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="9657d-138">Cando abre o panel de programación, expanda o recurso para mostrar as súas reservas.</span><span class="sxs-lookup"><span data-stu-id="9657d-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="9657d-139">Verá a reserva indicada como Dura.</span><span class="sxs-lookup"><span data-stu-id="9657d-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="9657d-140">Prema co botón secundario na reserva, en Cambiar estado, seleccione Reserva branda e, a seguir, Branda.</span><span class="sxs-lookup"><span data-stu-id="9657d-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="9657d-141">O estado da reserva é Brando.</span><span class="sxs-lookup"><span data-stu-id="9657d-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="9657d-142">Despois de pechar o panel de programación, verá que as horas do recurso cambiaron de Dura a Branda na grade de membro do equipo.</span><span class="sxs-lookup"><span data-stu-id="9657d-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="9657d-143">Teña en conta que se fai unha reservar dura dun recurso no equipo e, a seguir, atribúe as tarefas en WBS, ao utilizar Manter reservas para modificar o estado de Duro a Brando, eliminará a atribucións das tarefas para ese recurso, xa que só os recursos con reserva dura poden ser atribuídos a tarefas.</span><span class="sxs-lookup"><span data-stu-id="9657d-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="9657d-144">Reserva branda creando un recurso xenérico</span><span class="sxs-lookup"><span data-stu-id="9657d-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="9657d-145">Pode crear unha reserva branda xerando un membro do equipo de recurso xenérico, cumplindo co panel de programación ou Solicitar recursos e cambiando o tipo durante a reserva.</span><span class="sxs-lookup"><span data-stu-id="9657d-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="9657d-146">Para facelo, utilice o seguinte procedemento:</span><span class="sxs-lookup"><span data-stu-id="9657d-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="9657d-147">No WBS do proxecto, atribúa roles para as tarefas nas que desexa xerar membros do equipo xenéricos.</span><span class="sxs-lookup"><span data-stu-id="9657d-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="9657d-148">Prema Xerar equipo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="9657d-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="9657d-149">Na grade de membro de equipo de proxecto, seleccione o recurso xenérico e prema Reservar.</span><span class="sxs-lookup"><span data-stu-id="9657d-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="9657d-150">No panel de programación, seleccione o recurso que desexa reservar.</span><span class="sxs-lookup"><span data-stu-id="9657d-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="9657d-151">No panel Crear reserva de recurso do panel de programación, cambie o Estado de reserva a Brando.</span><span class="sxs-lookup"><span data-stu-id="9657d-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="9657d-152">Prema Reservar ou Reservar e saír.</span><span class="sxs-lookup"><span data-stu-id="9657d-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="9657d-153">Despois de pechar o panel de programación, verá o recurso seleccionado engadido ao equipo con horas de reserva brand, así como as horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="9657d-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="9657d-154">Tamén verá que o recurso xenérico continúa no equipo como un indicador de que as tarefas están atribuídas a un membro do equipo con reserva branda.</span><span class="sxs-lookup"><span data-stu-id="9657d-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="9657d-155">Cando esté listo para modificar un recurso de membro de equipo con reserva branda a membro do equipo con reservado dura para poder atribuílo a tarefas, faga o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9657d-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="9657d-156">Seleccione o recurso e prema Manter reservas.</span><span class="sxs-lookup"><span data-stu-id="9657d-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="9657d-157">Cando abre o panel de programación, expanda o recurso para mostrar as súas reservas.</span><span class="sxs-lookup"><span data-stu-id="9657d-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="9657d-158">Verá a reserva marcada como Branda.</span><span class="sxs-lookup"><span data-stu-id="9657d-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="9657d-159">Prema co botón secundario na reserva, en Cambiar estado, seleccione Reserva dura e, a seguir, Dura.</span><span class="sxs-lookup"><span data-stu-id="9657d-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="9657d-160">O estado da reserva é Duro.</span><span class="sxs-lookup"><span data-stu-id="9657d-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="9657d-161">Despois de pechar o panel de programación, verá que as horas do recurso cambiaron de Branda a Dura na grade de membro do equipo.</span><span class="sxs-lookup"><span data-stu-id="9657d-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="9657d-162">Agora pode atribuir o recurso a tarefas (sempre que haxa aliñación entre as horas con reserva dura e as horas de esforzo da tarefa de atribución).</span><span class="sxs-lookup"><span data-stu-id="9657d-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="9657d-163">Teña en conta que se seguiron os pasos de realización de recurso xenérico no punto #3 anterior, cando se modifica o estado do recurso reservado con reserva branda a dura, o membro do equipo xenérico é eliminado do equipo.</span><span class="sxs-lookup"><span data-stu-id="9657d-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]