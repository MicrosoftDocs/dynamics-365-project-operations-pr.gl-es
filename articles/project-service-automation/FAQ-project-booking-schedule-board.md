---
title: Crear unha reserva de proxecto desde o panel de programación
description: Este tema fornece información sobre como crear unha reserva de proxecto desde o panel de programación.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751445"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="7c3ae-103">Crear unha reserva de proxecto desde o panel de programación</span><span class="sxs-lookup"><span data-stu-id="7c3ae-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="7c3ae-104">Pode reservar un recurso nun proxecto directamente no separador de **Equipo** do proxecto ou xerando un requisito de recursos desde unha atribución de membro de equipo xenérico e, a seguir, cumprir os requisitos xerados cun membro do equipo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="7c3ae-105">Tamén pode reservar un recurso nun proxecto directamente desde o panel de programación.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="7c3ae-106">Hai tres xeitos de facer isto:</span><span class="sxs-lookup"><span data-stu-id="7c3ae-106">There are three ways to do this:</span></span>

- <span data-ttu-id="7c3ae-107">**Reservar desde un requirimento de recurso xerado:** Pode xerar un requisito de recurso despois de crear un recurso xenérico e asignar tarefas dentro dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="7c3ae-108">**Reservar desde o requisito principal:** Os requisitos principais aparecen no panel de programación do separador **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="7c3ae-109">**Reservar desde un novo requisito de recurso:** Pode crear un requisito de recurso dende cero e asocialo a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="7c3ae-110">No panel de programación, o requisito de recurso aparece no separador **Requisitos abertos**.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="7c3ae-111">Reservar desde un requisito de recurso xerado.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="7c3ae-112">Pode crear un recurso xenérico e atribuílo a unha ou máis tarefas dentro dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="7c3ae-113">A seguir, pode xerar un requisito de recurso desde o membro do equipo xenérico.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="7c3ae-114">No panel de programación, este recurso aparecerá no separador **Requisitos abertos**. É posible que necesite utilizar filtros de columnas na grade se ten moitos requisitos abertos.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="7c3ae-115">![Abrir o separador Requisitos no panel Programación](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura da táboa de reservas e atribucións")</span><span class="sxs-lookup"><span data-stu-id="7c3ae-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="7c3ae-116">Seleccione o requisito.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-116">Select the requirement.</span></span> <span data-ttu-id="7c3ae-117">O separador **Buscar dispoñibilidade** aparecerá na parte superior da fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="7c3ae-118">Cando selecciona o separador, ábrese o modo Asistente de programación do panel de programación e filtra os recursos dispoñibles que cumpren o requisito do recurso.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="7c3ae-119">Despois diso, pode reservar un recurso.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="7c3ae-120">Tamén pode arrastrar e soltar a fila seleccionada na parte inferior do panel de programación a unha cela de recurso na grade de arriba.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="7c3ae-121">Cando o solte, isto are o panel **Crear reserva de recurso** á dereita.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="7c3ae-122">Seleccionar **Reserva** reserva o recurso no equipo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-122">Selecting **Book** books the resource onto the project team.</span></span>

![Panel Crear reserva de recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="7c3ae-124">Reservar desde o requisito principal</span><span class="sxs-lookup"><span data-stu-id="7c3ae-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="7c3ae-125">Crear un proxecto en Project Service crea automaticamente un requisito de recurso denominado Requisito principal.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="7c3ae-126">Isto é un requisito baleiro utilizado para reservar rapidamente un recurso co panel de programación sen xerar un requisito nin crear un desde cero.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="7c3ae-127">Debido a que o requisito está baleiro, ten que especificar as datas, así como o método de atribución e as horas, se corresponde.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="7c3ae-128">Para reservar un recurso con Requisito principal no panel de programación, seleccione o separador **Proxecto**. Se ten moitos proxectos, é posible que teña que utilizar o filtro de columna na columna **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="7c3ae-129">![Filtros de columna no panel Programación](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura da táboa de reservas e atribucións")</span><span class="sxs-lookup"><span data-stu-id="7c3ae-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="7c3ae-130">Seleccione o requisito que só se ten o nome de proxecto como o seu nome e ten unha duración de cero (0).</span><span class="sxs-lookup"><span data-stu-id="7c3ae-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="7c3ae-131">Seleccione o separador **Buscar dispoñibilidade** que aparece na fila.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="7c3ae-132">Isto pon o panel de programación no modo de Asistente de programación e mostra os recursos dispoñibles que se poden reservar no proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="7c3ae-133">Debido a que o **Requisito principal** é un requisito baleiro con duración cero (0), deberá definir a duración no panel **Crear reserva de recurso** cando seleccione e reserve un recurso.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="7c3ae-134">Tamén pode seleccionar o **Requisito principal do proxecto** da parte inferior do panel de programación e arrastralo e soltalo nun recurso para reservalo.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="7c3ae-135">Debido a que o **Requisito principal** é un requisito baleiro con duración cero (0), deberá definir a duración no panel **Crear reserva de recurso** cando seleccione e reserve un recurso.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="7c3ae-136">Cando reserva un recurso a través do **Requisito principal** no panel de programación, engadeo ao equipo de proxecto sen ningunha atribución.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="7c3ae-137">Reservar desde un novo requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-137">Book from a new resource requirement</span></span>
<span data-ttu-id="7c3ae-138">Complete os seguintes pasos para reservar a partir dun novo requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="7c3ae-139">Vaia á **Requisitos de recursos** e, a seguir, seleccione **Novo** para crear un novo requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="7c3ae-140">No separador **Proxecto**, seleccione un proxecto para asociar o requisito ao proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="7c3ae-141">No panel de programación, este novo requisito creado recentemente móstrase como **Requisito aberto** que pode realizar.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="7c3ae-142">Reserve o recurso para engadilo ao equipo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="7c3ae-143">Agora que o recurso está reservado, debe atribuír tarefas manualmente.</span><span class="sxs-lookup"><span data-stu-id="7c3ae-143">Now that the resource is booked, you must assign tasks manually.</span></span>

