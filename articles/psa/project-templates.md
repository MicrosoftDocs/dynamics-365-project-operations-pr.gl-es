---
title: Modelos de proxecto
description: Este tema fornece información sobre como usar modelos de proxecto para a configuración rápida do proxecto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148056"
---
# <a name="project-templates"></a><span data-ttu-id="2e93e-103">Modelos de proxecto</span><span class="sxs-lookup"><span data-stu-id="2e93e-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2e93e-104">Un modelo de proxecto é un marco predefinido que axuda a iniciar con rapidez e facilidade un proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="2e93e-105">Pode usar un modelo predefinido para crear un novo proxecto cun só clic.</span><span class="sxs-lookup"><span data-stu-id="2e93e-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="2e93e-106">En canto aos proxectos, debe definir os requisitos previos para os modelos de proxectos.</span><span class="sxs-lookup"><span data-stu-id="2e93e-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="2e93e-107">Debe definir un calendario de proxecto para cada modelo de proxecto, e os roles e listas de prezos deben ser predefinidos na organización, de xeito que os compoñentes do modelo teñan datos útiles.</span><span class="sxs-lookup"><span data-stu-id="2e93e-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="2e93e-108">Un modelo de proxecto consta de tres compoñentes: un calendario, estimacións do proxecto e membros do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="2e93e-109">Programar</span><span class="sxs-lookup"><span data-stu-id="2e93e-109">Schedule</span></span>

<span data-ttu-id="2e93e-110">Unha programación nun modelo de proxecto ten o mesmo conxunto de elementos que unha programación nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="2e93e-111">Pode crear unha xerarquía de tarefas, asociar roles a tarefas, definir atributos de programación e definir dependencias.</span><span class="sxs-lookup"><span data-stu-id="2e93e-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="2e93e-112">Unha programación nun modelo de proxecto tamén admite modos de tarefas para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="2e93e-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="2e93e-113">Polo tanto, admite o motor de programación.</span><span class="sxs-lookup"><span data-stu-id="2e93e-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="2e93e-114">Debe asociar un calendario de proxecto ao proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="2e93e-115">Ao crear unha programación de traballo, non hai ningunha diferenza entre un modelo de proxecto e un proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="2e93e-116">Estimacións do proxecto</span><span class="sxs-lookup"><span data-stu-id="2e93e-116">Project estimates</span></span>

<span data-ttu-id="2e93e-117">As estimacións dun proxecto nun modelo de proxecto funcionan da mesma forma que as estimacións dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="2e93e-118">Non obstante, os custos e os prezos de venda extráense das listas de prezos e custos por defecto que se definen nos parámetros.</span><span class="sxs-lookup"><span data-stu-id="2e93e-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="2e93e-119">Creación dun proxecto a partir dun modelo</span><span class="sxs-lookup"><span data-stu-id="2e93e-119">Creating a project from a template</span></span>
 
<span data-ttu-id="2e93e-120">Hai varios xeitos de crear un proxecto a partir dun modelo de proxecto:</span><span class="sxs-lookup"><span data-stu-id="2e93e-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="2e93e-121">Ao crear un proxecto desde unha oferta, pode seleccionar un modelo de proxecto na caixa de diálogo **Creación rápida: Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="2e93e-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Caixa de diálogo Creación rápida: Proxecto](media/project-11.png)

- <span data-ttu-id="2e93e-123">Cando cree un proxecto seleccionando **Novo proxecto**, a páxina **Proxecto** aparece antes de gardar o rexistro.</span><span class="sxs-lookup"><span data-stu-id="2e93e-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="2e93e-124">No campo **Escoller un modelo**, seleccione un dos modelos de proxecto predefinidos na organización.</span><span class="sxs-lookup"><span data-stu-id="2e93e-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="2e93e-125">Use **Crear proxecto a partir dun modelo** na páxina **Entidade de modelo**.</span><span class="sxs-lookup"><span data-stu-id="2e93e-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="2e93e-126">Copiar compoñentes do modelo a un proxecto</span><span class="sxs-lookup"><span data-stu-id="2e93e-126">Copying components of template to project</span></span>

<span data-ttu-id="2e93e-127">Cando copia os compoñentes dun modelo de proxecto nun proxecto, poden ocorrer algunhas anulacións, dependendo da configuración do proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="2e93e-128">Copiar a programación</span><span class="sxs-lookup"><span data-stu-id="2e93e-128">Copying the schedule</span></span>

<span data-ttu-id="2e93e-129">Ao copiar a programación a partir dun modelo de proxecto, se o proxecto ten un calendario de proxecto diferente ao do modelo, as horas de traballo do calendario do proxecto aplicaranse á programación de tarefas.</span><span class="sxs-lookup"><span data-stu-id="2e93e-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="2e93e-130">Deste xeito, a programación axústase segundo o calendario de respaldo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="2e93e-131">De forma similar, a primeira tarefa na programación colle a data de inicio do proxecto, e a programación do resto da xerarquía actualízase segundo a duración e as dependencias especificadas no modelo.</span><span class="sxs-lookup"><span data-stu-id="2e93e-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="2e93e-132">Copiar estimacións do proxecto</span><span class="sxs-lookup"><span data-stu-id="2e93e-132">Copying project estimates</span></span> 

<span data-ttu-id="2e93e-133">Cando copia entre liñas de estimación do proxecto, as listas de prezos actualízanse.</span><span class="sxs-lookup"><span data-stu-id="2e93e-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="2e93e-134">Para a lista de prezos de custos, estas actualizacións baséanse na unidade propietaria do proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="2e93e-135">Para a lista de prezos de vendas, baséanse no cliente.</span><span class="sxs-lookup"><span data-stu-id="2e93e-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="2e93e-136">Para proxectos que están asociados a unha entidade de vendas, o custo unitario e os prezos de vendas determínanse segundo estas listas de prezos.</span><span class="sxs-lookup"><span data-stu-id="2e93e-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="2e93e-137">Copiar un equipo de proxecto</span><span class="sxs-lookup"><span data-stu-id="2e93e-137">Copying a project team</span></span>

<span data-ttu-id="2e93e-138">Ao copiar o equipo de proxecto a partir do modelo de proxecto, os recursos xenéricos está tamén se copian, xunto cos coñecementos e habilidades definidos no modelo.</span><span class="sxs-lookup"><span data-stu-id="2e93e-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="2e93e-139">As atribucións de recursos xenéricas tamén se manteñen igual que no modelo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="2e93e-140">Os recursos nomeados non son compatibles cos modelos de proxecto.</span><span class="sxs-lookup"><span data-stu-id="2e93e-140">Named resources aren't supported in project templates.</span></span>
