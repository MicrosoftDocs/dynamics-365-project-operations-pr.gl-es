---
title: Crear un novo proxecto
description: Este tema fornece información sobre como crear un novo proxecto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270721"
---
# <a name="create-a-new-project"></a><span data-ttu-id="5e94a-103">Crear un novo proxecto</span><span class="sxs-lookup"><span data-stu-id="5e94a-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e94a-104">Complete os seguintes pasos para crear un novo proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="5e94a-105">Na páxina **Xestión de proxectos**, seleccione **Novo proxecto** e introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5e94a-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="5e94a-106">**Tipo de proxecto:** Tempo e material</span><span class="sxs-lookup"><span data-stu-id="5e94a-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="5e94a-107">**Nome do proxecto:** Fase 2 de actualización de XYZ</span><span class="sxs-lookup"><span data-stu-id="5e94a-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="5e94a-108">**Grupo de proxectos:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="5e94a-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="5e94a-109">**ID do contrato do proxecto:** 00000002</span><span class="sxs-lookup"><span data-stu-id="5e94a-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="5e94a-110">Seleccione **Crear proxecto**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="5e94a-111">Atribuír un recurso a un proxecto</span><span class="sxs-lookup"><span data-stu-id="5e94a-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="5e94a-112">Na páxina **Traballadores**, na lista **Traballadores**, seleccione o rexistro do traballador para o que configurou competencias previamente e abra o rexistro de traballador.</span><span class="sxs-lookup"><span data-stu-id="5e94a-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="5e94a-113">No panel Acción, no separador **Proxecto**, no grupo **Configurar**, seleccione **Atribuír proxectos**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="5e94a-114">Na páxina **Atribucións de proxectos de validación de recursos**, no separador **Proxectos**, no campo **Engadir o proxecto aos proxectos seleccionados**, filtre no proxecto **Fase 2 de actualización de XYZ**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="5e94a-115">No panel **Proxectos restantes**, seleccione un proxecto e seleccione o botón de frecha para engadilo ao panel **Proxectos seleccionados**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="5e94a-116">Tamén pode atribuír categorías a un recurso segundo o precise.</span><span class="sxs-lookup"><span data-stu-id="5e94a-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="5e94a-117">O tipo de categoría é **Custo** ou **Ingresos**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="5e94a-118">O tipo de categoría está determinado pola súa organización.</span><span class="sxs-lookup"><span data-stu-id="5e94a-118">The category type is determined by your organization.</span></span> <span data-ttu-id="5e94a-119">Se non se atribúen categorías a un recurso, Finanzas busca a categoría predefinida en prezos de hora para custo e ingresos.</span><span class="sxs-lookup"><span data-stu-id="5e94a-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="5e94a-120">Configurar as características do recurso e do rol do proxecto</span><span class="sxs-lookup"><span data-stu-id="5e94a-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="5e94a-121">Un xestor de proxectos pode usar a funcionalidade de dotación de recursos para crear os roles necesarios para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="5e94a-122">Pódense usar roles se aínda se descoñecen os recursos confirmados cando se reservan os recursos.</span><span class="sxs-lookup"><span data-stu-id="5e94a-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="5e94a-123">Os roles pódense reservar temporalmente como recursos planificados, para que poida continuar as fases de planificación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="5e94a-124">[![Exemplo de rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="5e94a-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="5e94a-125">**Escenario:** Contoso foi contratada para completar un proxecto de tempo e material que ten unha carta de proxecto aprobada.</span><span class="sxs-lookup"><span data-stu-id="5e94a-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="5e94a-126">O xestor de proxectos subalterno aínda está completando o alcance do proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="5e94a-127">O xestor de recursos está a identificar actualmente recursos específicos que se reservarán para traballar no novo proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="5e94a-128">Debido á natureza crítica do proxecto, o patrocinador do proxecto solicitou ao xestor de proxectos principal como un dos roles.</span><span class="sxs-lookup"><span data-stu-id="5e94a-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="5e94a-129">O xestor de recursos debe adquirir o novo recurso e definir o rol no sistema no caso de que o xestor de proxectos subalterno precise a información do recurso durante a planificación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="5e94a-130">Os seguintes pasos mostran como o xestor de recursos pode configurar a función de xestor de proxectos principal e asociar as características dos recursos a el.</span><span class="sxs-lookup"><span data-stu-id="5e94a-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="5e94a-131">Máis tarde, o rol pódese empregar para buscar recursos dispoñibles que coincidan coas competencias requiridas.</span><span class="sxs-lookup"><span data-stu-id="5e94a-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="5e94a-132">Na páxina **Configurar roles**, seleccione **Novo** e introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5e94a-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="5e94a-133">**ID de rol:** Xestor de proxectos principal</span><span class="sxs-lookup"><span data-stu-id="5e94a-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="5e94a-134">**Descrición:** Xestor de proxectos principal</span><span class="sxs-lookup"><span data-stu-id="5e94a-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="5e94a-135">Seleccione **Crear**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-135">Select **Create**.</span></span>
3. <span data-ttu-id="5e94a-136">Seleccione o rol **Xestor de proxectos principal** e seleccione **Configurar características**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="5e94a-137">No campo **Tipo de características**, seleccione **Habilidade**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="5e94a-138">No campo **Características dispoñibles**, introduza a habilidade para buscar.</span><span class="sxs-lookup"><span data-stu-id="5e94a-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="5e94a-139">No campo **Tipo de característica**, seleccione **Certificado**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="5e94a-140">No campo **Características dispoñibles**, introduza o tipo de certificado para buscar.</span><span class="sxs-lookup"><span data-stu-id="5e94a-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="5e94a-141">Atribuír un recurso de proxecto a un proxecto</span><span class="sxs-lookup"><span data-stu-id="5e94a-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="5e94a-142">Na páxina **Todos os proxectos**, seleccione o proxecto **Fase 2 de actualización de XYZ**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="5e94a-143">No separador **Equipo do proxecto e programación**, seleccione **Engadir**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="5e94a-144">No campo **Rol**, seleccione **Membro do equipo**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="5e94a-145">Seleccione **Reservar desde calendario**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="5e94a-146">Na páxina **Dispoñibilidade de recursos**, seleccione **Ver configuración**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="5e94a-147">Na páxina **Axustar configuración de visualización**, introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5e94a-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="5e94a-148">**Formato para a visualización do intervalo de datas:** Día</span><span class="sxs-lookup"><span data-stu-id="5e94a-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="5e94a-149">**Mostrar descricións de dispoñibilidade:** Si</span><span class="sxs-lookup"><span data-stu-id="5e94a-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="5e94a-150">**Mostrar capacidade restante:** Si</span><span class="sxs-lookup"><span data-stu-id="5e94a-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="5e94a-151">Na lista de recursos, seleccione un recurso.</span><span class="sxs-lookup"><span data-stu-id="5e94a-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="5e94a-152">Seleccione **Reserva dura** e **Capacidade total**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="5e94a-153">Atribuír un recurso a un rol predefinido</span><span class="sxs-lookup"><span data-stu-id="5e94a-153">Assign a resource to a default role</span></span>

<span data-ttu-id="5e94a-154">Para axudar aos xestores de proxectos ou recursos, pode profundizar nos recursos que se poden reservar para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="5e94a-155">Pode asociar un rol predefinido a un recurso existente ou a un recurso adquirido recentemente.</span><span class="sxs-lookup"><span data-stu-id="5e94a-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="5e94a-156">Por exemplo, cando se contratou a Daniel, tiña a experiencia e as habilidades para ocupar o rol de analista empresarial.</span><span class="sxs-lookup"><span data-stu-id="5e94a-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="5e94a-157">O xestor de recursos asignou este rol como o rol predefinido de Daniel.</span><span class="sxs-lookup"><span data-stu-id="5e94a-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="5e94a-158">Polo tanto, o xestor de recursos engadiu a Daniel a un grupo de analistas empresariais dispoñibles para traballar en proxectos.</span><span class="sxs-lookup"><span data-stu-id="5e94a-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="5e94a-159">Durante a reserva de recursos, os xestores de proxectos poden filtrar os recursos de rol dispoñibles para traballar en proxectos.</span><span class="sxs-lookup"><span data-stu-id="5e94a-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="5e94a-160">Poden utilizar esta información como un criterio cando realizan análises de decisións con múltiples criterios durante o cumprimento dos recursos.</span><span class="sxs-lookup"><span data-stu-id="5e94a-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="5e94a-161">Tamén poden engadir outras características de recurso ao filtro para buscar recursos que teñan habilidades, educación e experiencia específicas para un determinado proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="5e94a-162">**Escenario:** Comezou un proxecto aprobado e reservouse a función de xestor de proxectos principal como recurso planificado durante a fase de planificación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e94a-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="5e94a-163">O xestor de recursos agora adquiriu un recurso para cubrir o rol de xestor de proxectos principal.</span><span class="sxs-lookup"><span data-stu-id="5e94a-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="5e94a-164">Na páxina **Lista de recursos**, seleccione **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="5e94a-165">Na páxina **Rol de recurso**, seleccione **Novo** e introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5e94a-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="5e94a-166">**Efectivo:** Introduza a data actual.</span><span class="sxs-lookup"><span data-stu-id="5e94a-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="5e94a-167">**Caducidade:** Introduce **Nunca**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="5e94a-168">**Rol:** Introduza **Xestor de proxectos principal**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="5e94a-169">Seleccione **Gardar** e logo peche a páxina.</span><span class="sxs-lookup"><span data-stu-id="5e94a-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="5e94a-170">No separador **Competencias**, engada a habilidade **ProjectMgmt** e o certificado **PMP**.</span><span class="sxs-lookup"><span data-stu-id="5e94a-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]