---
title: Configurar recursos de proxectos
description: Este tema fornece información sobre a configuración ou solicitude de recursos de proxecto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076304"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="cd8d9-103">Configurar recursos de proxectos</span><span class="sxs-lookup"><span data-stu-id="cd8d9-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd8d9-104">Debe configurar un calendario e asocialo a un empregado ou a un traballador.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="cd8d9-105">O calendario úsase para programar o proxecto e o tempo de traballo dos recursos reservados para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="cd8d9-106">Durante a configuración do calendario, os xestores de proxectos poden realizar a nivelación de recursos como parte da optimización de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="cd8d9-107">En función do programa do calendario, pódense aplicar restricións aos recursos.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="cd8d9-108">Pode configurar un calendario na páxina **Calendarios**.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="cd8d9-109">Cando configura un traballador como recurso do proxecto, pode seleccionar entre os traballadores que traballan na empresa para a que configura recursos.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="cd8d9-110">Como alternativa, pode seleccionar traballadores doutras empresas da súa organización.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="cd8d9-111">Estes traballadores son coñecidos como recursos entre empresas.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="cd8d9-112">Os seguintes procedementos explican como configurar un traballador como recurso de proxecto na súa empresa e como configurar un recurso de proxecto entre empresas.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="cd8d9-113">Configurar un traballador como recurso do proxecto</span><span class="sxs-lookup"><span data-stu-id="cd8d9-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="cd8d9-114">Na páxina **Traballadores** , na lista **Traballadores** , seleccione o traballador que está a engadir como recurso do proxecto e abra o rexistro de traballador.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="cd8d9-115">No panel de acción, seleccione **Proxecto** &gt; **Configurar** &gt; **Configuración do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="cd8d9-116">Seleccione un calendario e logo peche a páxina.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="cd8d9-117">Tamén pode especificar proxectos predefinidos para un recurso como un tipo de atribución previa.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="cd8d9-118">As atribucións previas pódense empregar cando o xestor de recursos ou o xestor de proxectos saiban en que proxectos traballará o recurso con antelación.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="cd8d9-119">As asignacións previas tamén poden basearse na solicitude dun patrocinador ou cliente do proxecto.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="cd8d9-120">Para atribuír previamente un proxecto, na páxina **Atribuír proxectos** , no separador **Proxectos** , na lista **Proxectos restantes** , seleccione o proxecto axeitado.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="cd8d9-121">Configurar un recurso entre empresas</span><span class="sxs-lookup"><span data-stu-id="cd8d9-121">Set up an intercompany resource</span></span>

<span data-ttu-id="cd8d9-122">Cando configura un traballador como recurso entre empresas, debe completar a configuración tanto na empresa prestamista como na empresa prestameira.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="cd8d9-123">Na empresa prestamista</span><span class="sxs-lookup"><span data-stu-id="cd8d9-123">In the lending company</span></span>

1. <span data-ttu-id="cd8d9-124">En Finanzas, verifique que a empresa prestamista está seleccionada e logo complete o procedemento da sección anterior, "Configurar un traballador como recurso do proxecto".</span><span class="sxs-lookup"><span data-stu-id="cd8d9-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="cd8d9-125">Na páxina **Contabilidade entre empresas** , seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="cd8d9-126">No campo **ID da persoa xurídica** , seleccione a empresa prestamista.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="cd8d9-127">Encha os campos como corresponda e, a seguir, seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="cd8d9-128">Na páxina **Prezo de transferencia** , seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="cd8d9-129">No campo **Persoa xurídica prestameira** , seleccione a empresa apropiada.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="cd8d9-130">Para prestar á empresa prestameira só o recurso que creou ao comezo desta sección, no campo **Recurso** , seleccione o nome do recurso que creou.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="cd8d9-131">Para poñer todos os recursos da empresa prestamista a disposición da empresa prestameira, deixe o campo **Recurso** en branco.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="cd8d9-132">Na páxina **Parámetros de xestión de proxectos e contabilidade** , no separador **Entre empresas** , configure a opción **Activar a programación de recursos e follas de control horario entre empresas** en **Si**.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="cd8d9-133">Na empresa prestameira</span><span class="sxs-lookup"><span data-stu-id="cd8d9-133">In the borrowing company</span></span>

- <span data-ttu-id="cd8d9-134">Na páxina **Lista de recursos** , no filtro de busca, introduza o nome do recurso que creou para a empresa prestamista, para comprobar que o nome está incluído na lista de recursos para a empresa prestameira.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="cd8d9-135">Solicitar recursos de proxecto</span><span class="sxs-lookup"><span data-stu-id="cd8d9-135">Request project resources</span></span>
<span data-ttu-id="cd8d9-136">A funcionalidade para a programación de recursos do proxecto só permite aos xestores de recursos distribuír recursos con persoal en compromisos ou proxectos.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="cd8d9-137">Para activar esta funcionalidade, complete as seguintes tarefas ou verifique que se completaron:</span><span class="sxs-lookup"><span data-stu-id="cd8d9-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="cd8d9-138">Configurar as secuencias numéricas.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-138">Set up number sequences.</span></span>
- <span data-ttu-id="cd8d9-139">Configurar fluxos de traballo de xestión de proxectos e contabilidade.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="cd8d9-140">Activar fluxos de traballo de solicitude de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-140">Enable resource request workflows.</span></span>

<span data-ttu-id="cd8d9-141">Despois de completar as tarefas anteriores, pode completar as seguintes tarefas se o precisa:</span><span class="sxs-lookup"><span data-stu-id="cd8d9-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="cd8d9-142">Crear unha solicitude de recurso a partir dun recurso con persoal con reserva branda.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="cd8d9-143">Supervisar solicitudes de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-143">Monitor resource requests.</span></span>
- <span data-ttu-id="cd8d9-144">Cumprir de solicitudes de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="cd8d9-145">Solicitar un recurso con persoal dunha WBS.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="cd8d9-146">Reservar recursos para un proxecto sen ter unha solicitude dun recurso con persoal.</span><span class="sxs-lookup"><span data-stu-id="cd8d9-146">Book resources to a project without having a request for a staffed resource.</span></span>
