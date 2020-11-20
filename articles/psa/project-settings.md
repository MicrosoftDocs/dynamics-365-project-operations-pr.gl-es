---
title: Configuración de proxecto
description: Neste tema se proporciona información sobre a configuración de xestión de proxectos.
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123106"
---
# <a name="project-settings"></a><span data-ttu-id="7125b-103">Configuración de proxecto</span><span class="sxs-lookup"><span data-stu-id="7125b-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7125b-104">Use os seguintes axustes para acceder ás funcións de planificación de proxectos.</span><span class="sxs-lookup"><span data-stu-id="7125b-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="7125b-105">Modelo de traballo</span><span class="sxs-lookup"><span data-stu-id="7125b-105">Work template</span></span>

<span data-ttu-id="7125b-106">Para crear unha programación de proxecto, créase un modelo de calendario de proxecto que define o número de horas de traballo para adaptar por día na programación e os peches de empresa.</span><span class="sxs-lookup"><span data-stu-id="7125b-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="7125b-107">Para crear un modelo de calendario de proxecto, asocie un modelo de traballo ao campo **Modelo de calendario** para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="7125b-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="7125b-108">Siga estes pasos para crear un modelo de traballo.</span><span class="sxs-lookup"><span data-stu-id="7125b-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="7125b-109">En PSA, no panel de navegación esquerdo, prema **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="7125b-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="7125b-110">Na páxina de lista **Recursos**, abra un rexistro de usuario e, a seguir, seleccione **Mostrar horas laborables**.</span><span class="sxs-lookup"><span data-stu-id="7125b-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7125b-111">Asegúrese de permitir ventás emerxentes na páxina do navegador.</span><span class="sxs-lookup"><span data-stu-id="7125b-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="7125b-112">Isto permítelle ver as horas laborables establecidas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="7125b-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="7125b-113">No separador **Vista mensual**, prema **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="7125b-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="7125b-114">Aparece unha lista de tres opcións:</span><span class="sxs-lookup"><span data-stu-id="7125b-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="7125b-115">Nova programación semanal</span><span class="sxs-lookup"><span data-stu-id="7125b-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="7125b-116">Programación de traballo para un día</span><span class="sxs-lookup"><span data-stu-id="7125b-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="7125b-117">Tempo libre</span><span class="sxs-lookup"><span data-stu-id="7125b-117">Time Off</span></span>

> ![Configurar opcións](media/project-13.png)

4. <span data-ttu-id="7125b-119">Seleccione **Nova programación semanal** e logo configure as opcións para esta programación de recursos.</span><span class="sxs-lookup"><span data-stu-id="7125b-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="7125b-120">Pode definir unha programación semanal recorrente, parámetros horarios diarios, peches de negocio e moito máis.</span><span class="sxs-lookup"><span data-stu-id="7125b-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="7125b-121">Estableza o intervalo de datas, seleccione **Gardar** e, a seguir, prema **Pechar**.</span><span class="sxs-lookup"><span data-stu-id="7125b-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="7125b-122">Volva á páxina de lista **Recursos** e seleccione o recurso para o que estableceu as horas laborables.</span><span class="sxs-lookup"><span data-stu-id="7125b-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="7125b-123">Seleccione **Establecer calendario como** para configurar o modelo de traballo.</span><span class="sxs-lookup"><span data-stu-id="7125b-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="7125b-124">Na caixa de diálogo **Modelo de traballo**, introduza un nome para o modelo de traballo e, a seguir, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="7125b-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="7125b-125">Agora pode asociar o modelo de traballo a un modelo de calendario de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7125b-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="7125b-126">Roles do recurso</span><span class="sxs-lookup"><span data-stu-id="7125b-126">Resource roles</span></span>

<span data-ttu-id="7125b-127">O termo *rol de recurso* refírese a un conxunto de habilidades, competencias e certificacións que unha persoa debe ter para realizar un conxunto específico de tarefas nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="7125b-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="7125b-128">PSA permítelle determinar o custo e facturar o tempo dun recurso en función do rol ao que estea asociado o recurso.</span><span class="sxs-lookup"><span data-stu-id="7125b-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="7125b-129">Cada organización debe configurar estes roles empregando a navegación á esquerda no menú de **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="7125b-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="7125b-130">Cada organización debe configurar estes roles na páxina **Categorías de recurso activas**.</span><span class="sxs-lookup"><span data-stu-id="7125b-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="7125b-131">Para abrir esta páxina, no panel de navegación da esquerda, seleccione **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="7125b-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="7125b-132">Listas de prezos</span><span class="sxs-lookup"><span data-stu-id="7125b-132">Price lists</span></span>

<span data-ttu-id="7125b-133">As listas de prezos permítenlle establecer o custo e os prezos de vendas para roles de recursos, categorías de gasto, produtos e outros elementos dunha organización.</span><span class="sxs-lookup"><span data-stu-id="7125b-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="7125b-134">Antes de establecer estimacións financeiras para o traballo que se deben entregar para un proxecto, debería crear unha lista de custos e prezos de vendas de seguridade.</span><span class="sxs-lookup"><span data-stu-id="7125b-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="7125b-135">Na sección de parámetros, tamén debe configurar unha lista de custos e prezos de vendas predefinida que se aplica a todos os proxectos creados na organización.</span><span class="sxs-lookup"><span data-stu-id="7125b-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="7125b-136">Na páxina **Parámetros do proxecto activos**, asegúrese de configurar unha lista de prezos de vendas e custos predefinida.</span><span class="sxs-lookup"><span data-stu-id="7125b-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
