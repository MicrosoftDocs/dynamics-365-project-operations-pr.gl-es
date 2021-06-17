---
title: Xestionar fusos horarios
description: Cando se crea un proxecto, o seu fuso horario baséase no fuso horario definido no modelo de hora de traballo aplicado.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997734"
---
# <a name="manage-time-zones"></a><span data-ttu-id="19d2a-103">Xestionar fusos horarios</span><span class="sxs-lookup"><span data-stu-id="19d2a-103">Manage time zones</span></span>

<span data-ttu-id="19d2a-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="19d2a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="19d2a-105">Proxectos</span><span class="sxs-lookup"><span data-stu-id="19d2a-105">Projects</span></span>

<span data-ttu-id="19d2a-106">Cando se crea un proxecto, o fuso horario baséase no fuso horario definido no modelo de hora de traballo aplicado.</span><span class="sxs-lookup"><span data-stu-id="19d2a-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="19d2a-107">En **Proxecto**, as datas son sempre relativas ao fuso horario do usuario que iniciou sesión en cada separador, agás o separador **Tarefa**. Cando vexa a estrutura de subdivisión do traballo, as datas sempre se amosarán no fuso horario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="19d2a-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="19d2a-108">Tarefas</span><span class="sxs-lookup"><span data-stu-id="19d2a-108">Tasks</span></span>

<span data-ttu-id="19d2a-109">Cando se crea unha tarefa, a hora de inicio, a hora de finalización e as horas/día están controladas polas horas de traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="19d2a-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="19d2a-110">Por exemplo, se se crea unha tarefa cun proxecto cuxo fuso horario é -8 PST e ten o seguinte horario de traballo: de 9:00 a 17:00 de luns a venres, calquera tarefa creada sen unha atribución respectará a hora de inicio e hora de finalización do calendario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="19d2a-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="19d2a-111">Xestionar recursos con fusos horarios</span><span class="sxs-lookup"><span data-stu-id="19d2a-111">Manage resources with time zones</span></span>

<span data-ttu-id="19d2a-112">Para obter resultados precisos e predicibles ao usar **Ampliar reserva**, hai dous requisitos previos clave que deben cumprirse:</span><span class="sxs-lookup"><span data-stu-id="19d2a-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="19d2a-113">O usuario debe configurar o fuso horario do seu dispositivo para que coincida co fuso horario definido no sistema **Configuración de personalización**.</span><span class="sxs-lookup"><span data-stu-id="19d2a-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Configuración do fuso horario en Windows 10](media/reconcile-assignments-03.png)

  ![Configuración do fuso horario na configuración de personalización](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="19d2a-116">O recurso reservable debe ter polo menos un minuto de tempo de traballo que se superpón cos contornos que se empregan para definir a extensión solicitada.</span><span class="sxs-lookup"><span data-stu-id="19d2a-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="19d2a-117">Por exemplo, os seguintes recursos con horario de traballo comprendido entre as 9:00 e as 19:00.</span><span class="sxs-lookup"><span data-stu-id="19d2a-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparación de contornos de recursos](media/reconcile-assignments-05.png)

<span data-ttu-id="19d2a-119">A seguinte táboa mostra:</span><span class="sxs-lookup"><span data-stu-id="19d2a-119">The following table shows:</span></span>

- <span data-ttu-id="19d2a-120">Un modelo de calendario do proxecto</span><span class="sxs-lookup"><span data-stu-id="19d2a-120">A project calendar template</span></span>
- <span data-ttu-id="19d2a-121">Recurso A: Este recurso ten o mesmo calendario e está no mesmo fuso horario que o proxecto.</span><span class="sxs-lookup"><span data-stu-id="19d2a-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="19d2a-122">A hora de inicios das reservas será ás 9:00.</span><span class="sxs-lookup"><span data-stu-id="19d2a-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="19d2a-123">Recurso B: Este recurso está situado nun fuso horario diferente do proxecto e comeza ás 7:00 AM no seu fuso horario.</span><span class="sxs-lookup"><span data-stu-id="19d2a-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="19d2a-124">Non obstante, as reservas comezarán ás 9:00 xa que esa é a hora de inicio máis temperá do contorno da tarefa.</span><span class="sxs-lookup"><span data-stu-id="19d2a-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="19d2a-125">Recursos C e D: Os recursos localízanse en diferentes fusos horarios, ambos diferentes entre si e do proxecto, e as súas reservas non comezan antes das respectivas horas de inicio dispoñibles.</span><span class="sxs-lookup"><span data-stu-id="19d2a-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="19d2a-126">Entidade</span><span class="sxs-lookup"><span data-stu-id="19d2a-126">Entity</span></span>  |<span data-ttu-id="19d2a-127">Calendario</span><span class="sxs-lookup"><span data-stu-id="19d2a-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="19d2a-128">Modelo de calendario do proxecto</span><span class="sxs-lookup"><span data-stu-id="19d2a-128">Project calendar template</span></span>   | ![calendario do proxecto](media/reconcile-assignments-06.png) |
|<span data-ttu-id="19d2a-130">Recurso A</span><span class="sxs-lookup"><span data-stu-id="19d2a-130">Resource A</span></span>  | ![Calendario do recurso A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="19d2a-132">Recurso B</span><span class="sxs-lookup"><span data-stu-id="19d2a-132">Resource B</span></span>  |  ![Calendario do recurso B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="19d2a-134">Recurso C</span><span class="sxs-lookup"><span data-stu-id="19d2a-134">Resource C</span></span>  |  ![Calendario do recurso C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="19d2a-136">Recurso D</span><span class="sxs-lookup"><span data-stu-id="19d2a-136">Resource D</span></span>  | ![Calendario do recurso D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="19d2a-138">Cando navegue á vista **Conciliación**, móstranse as atribucións de recursos e as carencias de reservas asociadas.</span><span class="sxs-lookup"><span data-stu-id="19d2a-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Vista de conciliación antes da extensión](media/reconcile-assignments-10.png)

<span data-ttu-id="19d2a-140">Despois de que se empregou a funcionalidade de ampliación de reservas para cada recurso, as reservas amplíanse con éxito para cada recurso porque as horas de traballo de cada recurso superpuxéronse aos contornos da escaseza.</span><span class="sxs-lookup"><span data-stu-id="19d2a-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Vista de conciliación despois da extensión da reserva](media/reconcile-assignments-11.png) 

<span data-ttu-id="19d2a-142">Teña en conta que unha ollada máis atenta aos detalles das reservas mostra diferenzas na hora de inicio das reservas.</span><span class="sxs-lookup"><span data-stu-id="19d2a-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="19d2a-143">As reservas comezan non antes da hora de inicio do contorno da atribución nin antes da hora de inicio dispoñible do recurso.</span><span class="sxs-lookup"><span data-stu-id="19d2a-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Novas reservas dos recursos no panel de programación](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]