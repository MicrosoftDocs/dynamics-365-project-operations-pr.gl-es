---
title: Crear un modelo de proxecto
description: Como crear un modelo de proxecto en Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751345"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="20f2f-103">Crear un modelo de proxecto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="20f2f-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="20f2f-104">Os modelos de proxecto afórranlle tempo se a súa empresa realiaza ofertas con regularidade en tipos de proxectos similares.</span><span class="sxs-lookup"><span data-stu-id="20f2f-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="20f2f-105">Fornecen un conxunto de roles estándar e horas de traballo estimadas para un tipo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="20f2f-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="20f2f-106">Os xestores de contas e os xestores de proxectos poden crear proxectos baseados nun modelo de proxecto, ou poden copiar o modelo e facer un propio.</span><span class="sxs-lookup"><span data-stu-id="20f2f-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="20f2f-107">Compoñentes do modelo de proxecto</span><span class="sxs-lookup"><span data-stu-id="20f2f-107">Components of project template</span></span>
 <span data-ttu-id="20f2f-108">Un modelo de proxecto consta de tres compoñentes:</span><span class="sxs-lookup"><span data-stu-id="20f2f-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="20f2f-109">**Estrutura de subdivisión do traballo**: unha estrutura de subdivisión do traballo nun modelo de proxecto ten o mesmo conxunto de elementos que os do proxecto.</span><span class="sxs-lookup"><span data-stu-id="20f2f-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="20f2f-110">Pode crear unha xerarquía de tarefas, asociar roles a tarefas, definir atributos de programación, definir dependencias e ver todos os datos no Gantt.</span><span class="sxs-lookup"><span data-stu-id="20f2f-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="20f2f-111">A estrutura de subdivisión do traballo en modelos de proxecto tamén é compatible cos modos de tarefa para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="20f2f-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="20f2f-112">Non hai ningunha diferenza entre un modelo de proxecto e un proxecto ao crear a programación de traballo.</span><span class="sxs-lookup"><span data-stu-id="20f2f-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="20f2f-113">**Estimacións de proxecto**: as estimacións de proxecto en modelos funcionan da mesma maneira que nos proxectos, excepto que as listas de prezos listas para definir o valor predefinido dos prezos de ventas e custo son sempre as listas de prezos e custo definidas nos parámetros de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="20f2f-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="20f2f-114">O resto das funcionalidades é o mesmo que nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="20f2f-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="20f2f-115">**Formación do equipo de proxecto**: ao formar un equipo de proxecto para un modelo de proxecto, non se pode reservar un recurso nomeado nun modelo.</span><span class="sxs-lookup"><span data-stu-id="20f2f-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="20f2f-116">Pode utilizar **Xerar equipo de proxecto** na estrutura de subdivisión do traballo para xerar un conxunto de recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="20f2f-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="20f2f-117">Tamén pode especificar os coñecementos e habilidades necesarios para os recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="20f2f-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="20f2f-118">Non se pode cambiar un recurso xenérico cun recurso reservable en modelos de proxecto.</span><span class="sxs-lookup"><span data-stu-id="20f2f-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="20f2f-119">Crear un proxecto a partir dun modelo</span><span class="sxs-lookup"><span data-stu-id="20f2f-119">Create a project from a template</span></span>  
 <span data-ttu-id="20f2f-120">Pode crear un proxecto a partir dun modelo destas maneiras:</span><span class="sxs-lookup"><span data-stu-id="20f2f-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="20f2f-121">Ao crear un proxecto desde a oferta, pode escoller un modelo de proxecto no formulario de creación rápida de proxectos.</span><span class="sxs-lookup"><span data-stu-id="20f2f-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="20f2f-122">Ao crear un proxecto premendo **Novo Proxecto**, o formulario de proxectos móstrase antes de gardar o rexistro.</span><span class="sxs-lookup"><span data-stu-id="20f2f-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="20f2f-123">Desde aquí, pode premer o campo **Escoller un modelo** para escoller un valor da lista de modelos de proxecto predefinidos da súa organización.</span><span class="sxs-lookup"><span data-stu-id="20f2f-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="20f2f-124">Prema **Crear proxecto a partir dun modelo** na páxina **Modelo de proxecto** para crear un proxecto a partir do modelo.</span><span class="sxs-lookup"><span data-stu-id="20f2f-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="20f2f-125">Copiar compoñentes dun modelo a un proxecto</span><span class="sxs-lookup"><span data-stu-id="20f2f-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="20f2f-126">Se copia compoñentes dun modelo a un proxecto, debe saber algunhas cousas.</span><span class="sxs-lookup"><span data-stu-id="20f2f-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="20f2f-127">**Copiar unha estrutura de subdivisión do traballo**: ao copiar a estrutura de subdivisión do traballo a partir dun modelo de proxecto, se o proxecto ten un calendario de proxecto diferente ao do modelo, as horas de traballo do calendario do proxecto aplicaranse á programación de tarefas.</span><span class="sxs-lookup"><span data-stu-id="20f2f-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="20f2f-128">Isto axusta a programación no calendario de respaldo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="20f2f-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="20f2f-129">De forma similar, a primeira tarefa na estrutura de subdivisión do traballo colle a data de inicio do proxecto, de xeito que o resto da programación da xerarquía de tarefas actualízase segundo a duración e as dependencias especificadas na estrutura de subdivisión do traballo no modelo.</span><span class="sxs-lookup"><span data-stu-id="20f2f-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="20f2f-130">**Copiar estimacións do proxecto**: cando copia en liñas de estimación do proxecto, as listas de prezos actualízanse segundo a unidade propietaria do proxecto para a lista de prezos de custo e cliente para a lista de prezos de vendas.</span><span class="sxs-lookup"><span data-stu-id="20f2f-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="20f2f-131">O custo unitario e os prezos de vendas determínanse desde estas listas de prezo en proxectos que están asociados a unha entidade de vendas.</span><span class="sxs-lookup"><span data-stu-id="20f2f-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="20f2f-132">**Copiar un equipo de proxecto**: ao copiar o equipo de proxecto a partir do modelo para un proxecto, os recursos xenéricos está tamén se copian, xunto cos coñecementos e habilidades definidos no modelo.</span><span class="sxs-lookup"><span data-stu-id="20f2f-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="20f2f-133">As atribucións de recursos xenéricas tamén se manteñen iguais no modelo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="20f2f-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="20f2f-134">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="20f2f-134">See Also</span></span>  
 [<span data-ttu-id="20f2f-135">Guía do xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="20f2f-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
