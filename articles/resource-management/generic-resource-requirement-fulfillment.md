---
title: Cumprimento dos requisitos de recursos xenéricos
description: Este tema proporciona información sobre como reservar recursos nomeados para un requisito de recursos xenérico.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130306"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="44aee-103">Cumprimento dos requisitos de recursos xenéricos</span><span class="sxs-lookup"><span data-stu-id="44aee-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="44aee-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="44aee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44aee-105">Pode reservar un recurso nomeado para substituír un recurso xenérico que teña un requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="44aee-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="44aee-106">Na páxina **Proxectos**, seleccione o separador **Equipo**.</span><span class="sxs-lookup"><span data-stu-id="44aee-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="44aee-107">Seleccione o recurso xenérico que ten un requisito de recursos da lista e logo seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="44aee-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="44aee-108">Ou abra o requisito de recursos e logo seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="44aee-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="44aee-109">Na páxina **Asistente de programación**, seleccione un recurso nomeado para reservar no seu equipo de proxecto e logo seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="44aee-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="44aee-110">Cando a reserva está completa e cumprida por un recurso nomeado, o recurso xenérico substitúese polo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="44aee-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="44aee-111">As asignacións do programa actualízanse co recurso nomeado tamén.</span><span class="sxs-lookup"><span data-stu-id="44aee-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="44aee-112">Cumprir un recurso xenérico con varios recursos nomeados</span><span class="sxs-lookup"><span data-stu-id="44aee-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="44aee-113">Cumprir un requisito para un recurso xenérico con varios recursos nomeados é similar a asignar un único recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="44aee-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="44aee-114">Por exemplo, hai unha tarefa cunha duración de cinco días e 120 horas de esforzo.</span><span class="sxs-lookup"><span data-stu-id="44aee-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="44aee-115">Esta tarefa non se pode completar cun recurso que traballa un día típico de oito horas durante unha semana de cinco días.</span><span class="sxs-lookup"><span data-stu-id="44aee-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="44aee-116">O requisito é de 120 horas de enxeñería robótica durante cinco días, é dicir, 24 horas ao día.</span><span class="sxs-lookup"><span data-stu-id="44aee-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="44aee-117">Este é un exemplo de cando se necesitan varios recursos nomeados para cumprir unha solicitude de recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="44aee-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="44aee-118">Deberá reservar varios recursos para cumprir o requisito.</span><span class="sxs-lookup"><span data-stu-id="44aee-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="44aee-119">A principal diferenza neste escenario é que o recurso xenérico permanece no equipo asignado á tarefa e os membros do equipo de recursos nomeados reservados non se asignan como parte do posto.</span><span class="sxs-lookup"><span data-stu-id="44aee-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="44aee-120">O xestor do proxecto pode atribuír o traballo segundo corresponda aos recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="44aee-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="44aee-121">A vista **Reconciliación** pode axudar a un xestor de proxectos a dividir as reservas entre varios recursos para a asignación de tarefas.</span><span class="sxs-lookup"><span data-stu-id="44aee-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="44aee-122">Isto non se fai de xeito automático porque en calquera escenario máis complicado que o simple exemplo anterior, como cando hai un paquete de tarefas que conforman o requisito ou a intención de como o xestor de proxectos quere atribuír debe ser asumida polo sistema.</span><span class="sxs-lookup"><span data-stu-id="44aee-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="44aee-123">Debido a que o sistema non pode entender a intención, é probable que as suposicións sexan diferentes do previsto e se produza un resultado incorrecto ou imprevisible.</span><span class="sxs-lookup"><span data-stu-id="44aee-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="44aee-124">O resultado previsible é que o recurso xenérico permaneza asignado ata que o responsable do proxecto cree asignacións deliberadamente, coa asistencia da vista **Reconciliación**.</span><span class="sxs-lookup"><span data-stu-id="44aee-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


