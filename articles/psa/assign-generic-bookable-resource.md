---
title: Atribuír recursos reservables xenéricos a unha tarefa e un equipo de proxectos
description: Este tema fornece información sobre a reserva de recursos xenéricos a tarefas e equipos de proxectos.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076147"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="916a2-103">Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="916a2-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="916a2-104">Ademais de reservar e atribuír recursos nomeados ou reais ao seu proxecto, pode atribuír recursos xenéricos ás tarefas do proxecto.</span><span class="sxs-lookup"><span data-stu-id="916a2-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="916a2-105">Estes recursos poden servir como marcadores de posición para os recursos nomeados ata que estea listo para dotar de persoal ao seu proxecto con recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="916a2-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="916a2-106">En Project Service Automation (PSA), abra a páxina **Proxecto** e no separador **Programa** escolla o nome do posto do recurso xenérico na cela **Recurso** do programa.</span><span class="sxs-lookup"><span data-stu-id="916a2-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="916a2-107">Ou prema a icona **Recurso** na cela para abrir o selector de recursos e logo introduza o nome do recurso xenérico que desexa crear.</span><span class="sxs-lookup"><span data-stu-id="916a2-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Creación e asignación dun membro xenérico do equipo](media/RM-how-to-9.png)

<span data-ttu-id="916a2-109">Isto abrirá o panel **Creación rápida: Membro do equipo do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="916a2-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="916a2-110">Introduza a función e a unidade de organización do membro do equipo de recursos xenéricos e logo prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="916a2-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Creación rápida de membro xenérico do equipo](media/RM-how-to-10.png)

3. <span data-ttu-id="916a2-112">Despois de crear o novo membro do equipo de recursos xenéricos, atribuirase á tarefa.</span><span class="sxs-lookup"><span data-stu-id="916a2-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="916a2-113">Pode continuar atribuíndo ese recurso xenérico a outras tarefas da programación de tarefas.</span><span class="sxs-lookup"><span data-stu-id="916a2-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Asignación de membro xenérico de equipo existente a tarefas](media/RM-how-to-11.png)

4. <span data-ttu-id="916a2-115">Despois de atribuír o recurso xenérico, pode xerar un requisito de recurso e cumprilo reservando directamente ou enviando unha solicitude de recurso a un xestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="916a2-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Xeración dun requisito para un membro xenérico do equipo](media/RM-how-to-12.png)

<span data-ttu-id="916a2-117">Na grade do membro do equipo, ademais de poder empregar o selector de recursos como se mencionou anteriormente, pode engadir recursos xenéricos directamente.</span><span class="sxs-lookup"><span data-stu-id="916a2-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="916a2-118">Os recursos engádense cun requisito de recurso baseado nas datas de comezo/final e método de atribución especificados no panel **Creación rápida: Membro do equipo do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="916a2-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="916a2-119">Pode ver unha diferenza se engade directamente o membro do equipo xenérico e despois atribúe máis tarefas ao recurso xenérico das que solicitaron horas para cubrir.</span><span class="sxs-lookup"><span data-stu-id="916a2-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="916a2-120">Prema **Xerar requisito** para rexenerar o requisito para equilibrar as horas solicitadas coas atribucións.</span><span class="sxs-lookup"><span data-stu-id="916a2-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="916a2-121">Tamén pode premer a ligazón **Requisito do recurso** na grade do equipo para abrir o requisito e engadir habilidades, recursos preferidos, etc.</span><span class="sxs-lookup"><span data-stu-id="916a2-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Requisito do recurso](media/RM-how-to-13.png)

