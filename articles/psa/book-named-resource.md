---
title: Reservar recursos nomeados a partir de requisitos de recursos
description: Este tema proporciona información sobre a reserva de recursos nomeados para un requisito de recursos xenérico.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145088"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="c9bbf-103">Reservar recursos nomeados a partir de requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="c9bbf-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c9bbf-104">Pode reservar un recurso nomeado para substituír un recurso xenérico que teña un requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c9bbf-105">En Project Service Automation (PSA), na páxina **Proxectos** prema no separador **Equipo**.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="c9bbf-106">Seleccione o recurso xenérico que ten un requisito de recursos da lista e logo prema en **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="c9bbf-107">Ou abra o requisito de recursos e logo prema en **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-107">Or, open the resource requirement and then click **Book**.</span></span>


![Reserva dun membro xenérico do equipo](media/RM-how-to-14.png)


3. <span data-ttu-id="c9bbf-109">Na páxina **Asistente de programación**, seleccione un recurso nomeado para reservar no seu equipo de proxecto e logo prema en **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Reserva dun membro xenérico do equipo usando o asistente de programación](media/RM-how-to-15.png)

<span data-ttu-id="c9bbf-111">Cando a reserva está completa e cumprida por un recurso nomeado, o recurso xenérico substitúese polo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![O membro nomeado do equipo substitúe a un membro xenérico do equipo](media/RM-how-to-16.png)

<span data-ttu-id="c9bbf-113">As asignacións do programa actualízanse co recurso nomeado tamén.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Membro do equipo nomeado asignado ás tarefas do proxecto](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c9bbf-115">Cumprir un recurso xenérico con varios recursos nomeados</span><span class="sxs-lookup"><span data-stu-id="c9bbf-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c9bbf-116">Cumprir un requisito para un recurso xenérico con varios recursos nomeados é similar a asignar un único recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c9bbf-117">Por exemplo, hai unha tarefa cunha duración de cinco días e 120 horas de esforzo.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c9bbf-118">Esta tarefa non se pode completar cun recurso que traballa un día típico de oito horas durante unha semana de cinco días.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Unha tarefa que necesita 120 horas de esforzo ao longo de cinco días](media/RM-how-to-21.png)

<span data-ttu-id="c9bbf-120">O requisito é de 120 horas de enxeñería robótica durante cinco días, é dicir, 24 horas ao día.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Requisito por día](media/RM-how-to-22.png)

<span data-ttu-id="c9bbf-122">Este é un exemplo de cando se necesitan varios recursos nomeados para cumprir unha solicitude de recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c9bbf-123">Deberá reservar varios recursos para cumprir o requisito.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Reservar varios recursos para cumprir o requisito](media/RM-how-to-23.png)

<span data-ttu-id="c9bbf-125">A principal diferenza neste escenario é que o recurso xenérico permanece no equipo asignado á tarefa e os membros do equipo de recursos nomeados reservados non se asignan como parte do posto.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c9bbf-126">O xestor do proxecto pode atribuír o traballo segundo corresponda aos recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c9bbf-127">A vista **Reconciliación** pode axudar a un xestor de proxectos a dividir as reservas entre varios recursos para a asignación de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c9bbf-128">Isto non se fai de xeito automático porque en calquera escenario máis complicado que o simple exemplo anterior, como cando hai un paquete de tarefas que conforman o requisito, a intención de como o xestor de proxectos quere atribuír debe ser asumida polo sistema.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c9bbf-129">Debido a que o sistema non pode entender a intención, é probable que as suposicións sexan diferentes do previsto e se produza un resultado incorrecto ou imprevisible.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="c9bbf-130">O resultado previsible é que o recurso xenérico permaneza asignado ata que o responsable do proxecto cree asignacións deliberadamente, coa asistencia da vista **Reconciliación**.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


