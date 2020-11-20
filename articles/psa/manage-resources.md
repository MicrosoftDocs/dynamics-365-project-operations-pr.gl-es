---
title: Xestionar recursos
description: Este tema fornece información sobre como pode xestionar recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132331"
---
# <a name="manage-resources"></a><span data-ttu-id="f0844-103">Xestionar recursos</span><span class="sxs-lookup"><span data-stu-id="f0844-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f0844-104">Dynamics 365 Project Service Automation inclúe un panel de xestor de recursos que ofrece unha visión xeral da demanda e utilización de recursos en toda a organización.</span><span class="sxs-lookup"><span data-stu-id="f0844-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="f0844-105">Podes usar os gráficos deste panel para visualizar a seguinte información:</span><span class="sxs-lookup"><span data-stu-id="f0844-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="f0844-106">**Demanda de recursos** - O gráfico **Solicitude de recursos activos** mostra os recursos enviados.</span><span class="sxs-lookup"><span data-stu-id="f0844-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="f0844-107">Os recursos agrúpanse por rol ou proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="f0844-108">**Demanda de recursos non enviados** - O ggráfico **Demanda de recursos non enviados** mostra todos os requisitos de recursos que non se enviaron.</span><span class="sxs-lookup"><span data-stu-id="f0844-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="f0844-109">Axuda aos xestores de recursos a ver a demanda que non é firme e pode enviarse mediante unha solicitude de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0844-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="f0844-110">**Utilización facturable a semana pasada** - O gráfico **Utilización por rol** mostra a porcentaxe da utilización facturable real da organización por rol fronte á súa utilización facturable obxectivo por rol.</span><span class="sxs-lookup"><span data-stu-id="f0844-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0844-111">Para facer que o gráfico **Utilización por rol** estea dispoñible, cree un traballo que execute o fluxo de traballo UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="f0844-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="f0844-112">Este traballo recorrente execútase cada sete días para calcular a utilización facturable dos sete días anteriores.</span><span class="sxs-lookup"><span data-stu-id="f0844-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="f0844-113">Os resultados agrúpanse por rol.</span><span class="sxs-lookup"><span data-stu-id="f0844-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="f0844-114">Xestionar membros do equipo de proxecto</span><span class="sxs-lookup"><span data-stu-id="f0844-114">Manage project team members</span></span>

<span data-ttu-id="f0844-115">Os xestores de proxectos poden usar o panel de xestor de recursos para xestionar os recursos dos proxectos.</span><span class="sxs-lookup"><span data-stu-id="f0844-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="f0844-116">Por exemplo, poden engadir un membro do equipo directamente a un proxecto e reservar un membro do equipo para cumprir os requisitos de recursos capturados por un recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="f0844-117">Engadir un membro do equipo directamente a un proxecto</span><span class="sxs-lookup"><span data-stu-id="f0844-117">Add a team member directly to a project</span></span>

<span data-ttu-id="f0844-118">Para engadir un membro do equipo directamente a un proxecto, na páxina **Proxectos**, no separador **Equipo**, seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="f0844-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="f0844-119">Aparecerá a caixa de diálogo **Creación rápida: Membro de equipo de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="f0844-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="f0844-120">Nesta caixa de diálogo, pode realizar estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="f0844-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="f0844-121">**Reservar un recurso nomeado** - No campo **Recurso reservable**, seleccione o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="f0844-122">A seguir, seleccione o rol, estableza o período e seleccione un método de asignación.</span><span class="sxs-lookup"><span data-stu-id="f0844-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="f0844-123">O recurso nomeado que seleccionou engádese ao proxecto mediante o método de asignación seleccionado e o calendario de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0844-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="f0844-124">**Engadir un recurso xenérico** - Deixe o campo **Recurso reservable** en branco e, a seguir, seleccione o rol, estableza o período e seleccione o método de asignación preferido.</span><span class="sxs-lookup"><span data-stu-id="f0844-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="f0844-125">Un recurso xenérico engádese ao equipo como marcador de posición para manter o padrón de demanda empregado para reservar recursos nomeados no equipo.</span><span class="sxs-lookup"><span data-stu-id="f0844-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="f0844-126">O requisito faise segundo o calendario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="f0844-127">**Engadir un recurso nomeado ao equipo sen consumir capacidade do recurso** - No capo **Recurso reservable**, seleccione un recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="f0844-128">A seguir, seleccione o período e seleccione **Ningún** como método de asignación.</span><span class="sxs-lookup"><span data-stu-id="f0844-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="f0844-129">O recurso engádese ao equipo, pero a capacidade do recurso non se consume a través dunha reserva.</span><span class="sxs-lookup"><span data-stu-id="f0844-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="f0844-130">Reservar un membro do equipo para cumprir os requisitos dun recurso xenérico</span><span class="sxs-lookup"><span data-stu-id="f0844-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="f0844-131">En PSA, pode reservar un recurso xenérico nun equipo de proxecto e pode especificar o rol, a capacidade requirida e como se distribúe esa capacidade.</span><span class="sxs-lookup"><span data-stu-id="f0844-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="f0844-132">No requisito de recurso, pode especificar os atributos asociados ao recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="f0844-133">Estes atributos inclúen habilidades requiridas, a unidade organizativa preferida e recursos preferentes.</span><span class="sxs-lookup"><span data-stu-id="f0844-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="f0844-134">Siga estes pasos para especificar as habilidades necesarias nun recurso xenérico para un programador.</span><span class="sxs-lookup"><span data-stu-id="f0844-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="f0844-135">Na páxina **Proxectos**, no separador **Equipo**, seleccione **Novo** para reservar un recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Recurso xenérico reservado no equipo](media/Resource-Management-image9.png)

2. <span data-ttu-id="f0844-137">Na vista **Todos os membros do equipo**, na columna **Requisito de recurso**, seleccione a ligazón para engadir as habilidades necesarias para o recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Ligazón de requisito](media/Resource-Management-image10.png)

3. <span data-ttu-id="f0844-139">Na páxina **Requisito de recurso** que aparece, na grade **Habilidades**, seleccione os puntos suspensivos (**...**) e, a seguir, seleccione **Engadir unha nova característica de requisito** para engadir as habilidades necesarias para o seu programador.</span><span class="sxs-lookup"><span data-stu-id="f0844-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Engadir comando de nova característica de requisito](media/Resource-Management-image11.png)

4. <span data-ttu-id="f0844-141">Na caixa de diálogo **Creación rápida: característica de requisito** que aparece no campo **Característica**, seleccione a habilidade requirida.</span><span class="sxs-lookup"><span data-stu-id="f0844-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="f0844-142">Despois, no campo **Valor de clasificación**, seleccione o nivel de competencia para esa habilidade.</span><span class="sxs-lookup"><span data-stu-id="f0844-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="f0844-143">Finalmente, no campo **Requisito de recurso**, estableza o requisito para obter recursos orixe de unidades organizativas ou incluso recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="f0844-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="f0844-144">Ao concluír, seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="f0844-144">When you've finished, select **Save**.</span></span>

    ![Caixa de diáñogo Creación rápida: Característica de requisito](media/Resource-Management-image12.png)

5. <span data-ttu-id="f0844-146">Na páxina **Requisito de recurso**, seleccione **Reservar** para cumprir o requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Botón de reserva na páxina Requisito de recurso](media/Resource-Management-image13.png)

    <span data-ttu-id="f0844-148">Tamén pode seleccionar o recurso xenérico na grade **Todos os membros do equipo** e, a seguir, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="f0844-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Botón de reserva enriba da grade Todos os membros do equipo](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="f0844-150">Neste exemplo, hai 40 horas requiridas pero non hai horas reservadas reais, porque os recursos xenéricos non teñen reservas.</span><span class="sxs-lookup"><span data-stu-id="f0844-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="f0844-151">Ademais, non hai horas atribuídas, porque o recurso xenérico se engadiu directamente ao equipo.</span><span class="sxs-lookup"><span data-stu-id="f0844-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="f0844-152">Non se engadiu mediante a atribución de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f0844-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="f0844-153">Na páxina **Asistente de programación** pode filtrar os recursos dispoñibles segundo os requisitos que se especifican no requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="f0844-154">Os recursos clasifícanse segundo os parámetros de ordenación que se especifican no panel de programación.</span><span class="sxs-lookup"><span data-stu-id="f0844-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Páxina Asistente de programación](media/Resource-Management-image15.png)

    <span data-ttu-id="f0844-156">Aquí ten algúns filtros que se usan con frecuencia:</span><span class="sxs-lookup"><span data-stu-id="f0844-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="f0844-157">**Características xunto cunha clasificación** - Filtrar por habilidades, certificacións e outras calidades de recursos, ademais das clasificacións de competencia.</span><span class="sxs-lookup"><span data-stu-id="f0844-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="f0844-158">**Roles** – Filtrar por roles predefinidos que se atribúen aos recursos reservables.</span><span class="sxs-lookup"><span data-stu-id="f0844-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="f0844-159">**Unidades organizativas** - Filtrar os recursos reservables polas unidades organizativas ás que están atribuídos.</span><span class="sxs-lookup"><span data-stu-id="f0844-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="f0844-160">Se non está satisfeito cos resultados da busca de requisitos iniciais, pode cambiar os criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="f0844-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="f0844-161">Expanda o panel **Vista de filtro** á esquerda e, a seguir, seleccione **Buscar** para buscar recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="f0844-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Panel Vista de filtro](media/Resource-Management-image16.png)

7. <span data-ttu-id="f0844-163">Para cambiar como se clasifican os resultados, seleccione **Ordenar**.</span><span class="sxs-lookup"><span data-stu-id="f0844-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Comando Ordenar](media/Resource-Management-image17.png)

8. <span data-ttu-id="f0844-165">Seleccione recursos segundo a demanda que se especifica no requisito, como se indica na parte superior da grade.</span><span class="sxs-lookup"><span data-stu-id="f0844-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="f0844-166">Pode limpar a selección de celas da grade e deixar aberta esa capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="f0844-167">Só un recurso á vez pode seleccionarse como reservado.</span><span class="sxs-lookup"><span data-stu-id="f0844-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="f0844-168">Seleccione **Reservar** para reservar o recurso seleccionado e deixar aberto o panel de programación para que poida seleccionar recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="f0844-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="f0844-169">Alternativamente, seleccione **Reservar e saír** para reservar o recurso seleccionado e pechar o panel de programación.</span><span class="sxs-lookup"><span data-stu-id="f0844-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Recurso para reservar](media/Resource-Management-image19.png)

    <span data-ttu-id="f0844-171">Recibe unha notificación sobre horas reservadas.</span><span class="sxs-lookup"><span data-stu-id="f0844-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="f0844-172">Os indicadores de demanda amosan canto se satisfai o requisito de reserva e canto queda.</span><span class="sxs-lookup"><span data-stu-id="f0844-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="f0844-173">Tamén pode ver canto se consume da capacidade do recurso seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f0844-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="f0844-174">Seleccione **Expandir** para ver máis detalles sobre as reservas de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0844-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="f0844-175">Volva á vista **Todos os membros do equipo**.</span><span class="sxs-lookup"><span data-stu-id="f0844-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="f0844-176">Na grade, observe que o recurso xenérico foi substituído polo recurso nomeado, e que figuran 40 horas como reservadas para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Grade Todos os membros do equipo actualizada](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="f0844-178">Non se amosan horas atribuídas porque se reservaron directamente no equipo.</span><span class="sxs-lookup"><span data-stu-id="f0844-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="f0844-179">Non foron reservados mediante a atribución de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f0844-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="f0844-180">Atribuír recursos xenéricos a tarefas e xerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="f0844-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="f0844-181">En PSA, pode crear tarefas e despois asignarlles recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="f0844-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="f0844-182">Deste xeito, a demanda de recursos pode ser representada polos marcadores de posición mentres estima a súa programación e cifras financeiras.</span><span class="sxs-lookup"><span data-stu-id="f0844-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="f0844-183">Pode xerar requisitos de recursos para os recursos xenéricos e cumprilos.</span><span class="sxs-lookup"><span data-stu-id="f0844-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="f0844-184">Na páxina **Proxectos**, no separador **Programación**, seleccione **Engadir** para crear unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="f0844-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Nova tarefa creada](media/Resource-Management-image21.png)

2. <span data-ttu-id="f0844-186">No campo **Recursos**, seleccione o símbolo de **Selector de recursos**.</span><span class="sxs-lookup"><span data-stu-id="f0844-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="f0844-187">O Selector de recursos aparece e amosa aos membros do equipo existentes para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Selector de recursos](media/Resource-Management-image22.png)

3. <span data-ttu-id="f0844-189">Introduza o nome do novo recurso xenérico e logo seleccione **Crear**.</span><span class="sxs-lookup"><span data-stu-id="f0844-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Nomee o novo recurso xenérico introducido](media/Resource-Management-image23.png)

4. <span data-ttu-id="f0844-191">Na caixa de diálogo **Creación rápida: membro do equipo de proxecto** que aparece, no campo **Rol**, seleccione o recurso requirido.</span><span class="sxs-lookup"><span data-stu-id="f0844-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="f0844-192">No campo **Unidade de recursos**, seleccione a unidade organizativa para o recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="f0844-193">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="f0844-193">Then select **Save**.</span></span>

    ![Caixa de diálogo Creación rápida: membro de equipo de proxecto.](media/Resource-Management-image24.png)

    <span data-ttu-id="f0844-195">Agora o membro do equipo xenérico atribúese á tarefa.</span><span class="sxs-lookup"><span data-stu-id="f0844-195">The generic team member is now assigned to the task.</span></span>

    ![Membro do equipo xenérico atribuído á tarefa](media/Resource-Management-image25.png)

    <span data-ttu-id="f0844-197">No separador **Equipo**, verá o novo membro xenérico do equipo.</span><span class="sxs-lookup"><span data-stu-id="f0844-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="f0844-198">Teña en conta que só ten atribuídas horas.</span><span class="sxs-lookup"><span data-stu-id="f0844-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="f0844-199">Estas horas son a suma de todas as tarefas atribuídas ao membro do equipo xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="f0844-200">O membro do equipo xenérico aínda non necesita horas ou un requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Membro xenérico do equipo no separador Equipo](media/Resource-Management-image26.png)

5. <span data-ttu-id="f0844-202">Agora pode atribuír o membro do equipo xenérico a outras tarefas mediante o Selector de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0844-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Membro do equipo xenérico no Selector de recursos](media/Resource-Management-image27.png)

    <span data-ttu-id="f0844-204">Cando termine de atribuír o recurso xenérico a tarefas, pode xerar un requisito de recurso para o recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="f0844-205">No separador **Equipo**, seleccione o recurso xenérico e, a seguir, seleccione **Xerar requisito**.</span><span class="sxs-lookup"><span data-stu-id="f0844-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Comando Xerar requisito](media/Resource-Management-image28.png)

    <span data-ttu-id="f0844-207">Cando se xera o requisito, o membro do equipo xenérico terá horas e unha ligazón para o requisito do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Ligazón de requisito de recurso](media/Resource-Management-image29.png)

    <span data-ttu-id="f0844-209">Despois de reservar un recurso nomeado, o recurso xenérico elimínase do equipo e substitúese polo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="f0844-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Recurso xenérico substituído polo recurso nomeado](media/Resource-Management-image30.png)

    <span data-ttu-id="f0844-211">No separador **Programación**, elimínanse as atribucións do recurso xenérico e substitúense polo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="f0844-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Atribucións do recurso xenérico substituídas polo recurso nomeado no separador de programación](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="f0844-213">Este comportamento só se produce cando un recurso nomeado está totalmente reservado para o requisito de recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="f0844-214">Cando un recurso nomeado substitúe parcialmente o requisito de recurso xenérico ou varios recursos nomeados substitúen o requisito de recurso xenérico, o recurso xenérico permanece atribuído á tarefa.</span><span class="sxs-lookup"><span data-stu-id="f0844-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="f0844-215">Na seguinte ilustración, planificouse unha tarefa de 80 horas cunha duración de cinco días (16 horas ao día durante cinco días) e atribuíuse ao recurso xenérico que leva o nome **Funcional**.</span><span class="sxs-lookup"><span data-stu-id="f0844-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Tarefa de oitenta horas e cinco días atribuída ao recurso xenérico funcional](media/Resource-Management-image32.png)

    <span data-ttu-id="f0844-217">Cando xera o requisito, é de 80 horas ao longo de cinco días.</span><span class="sxs-lookup"><span data-stu-id="f0844-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Requisito xerado para 80 horas durante cinco días](media/Resource-Management-image33.png)

    <span data-ttu-id="f0844-219">Debido a que os recursos dispoñibles traballan só oito horas ao día, necesítanse dous recursos para cumprir o requisito.</span><span class="sxs-lookup"><span data-stu-id="f0844-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Segundo recurso](media/Resource-Management-image35.png)

    <span data-ttu-id="f0844-221">No separador **Equipo**, agora pode ver que o recurso xenérico non ten horas requiridas, pero as horas atribuídas aínda aparecen xunto cos dous recursos nomeados encargados do cumprimento.</span><span class="sxs-lookup"><span data-stu-id="f0844-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dous recursos nomeados no separador Equipo](media/Resource-Management-image36.png)

    <span data-ttu-id="f0844-223">No separador **Programación**, o recurso xenérico permanece asignado á tarefa.</span><span class="sxs-lookup"><span data-stu-id="f0844-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Recursos xenéricos no separador Programación](media/Resource-Management-image37.png)

<span data-ttu-id="f0844-225">PSA non atribúe ambos recursos á tarefa, porque ese comportamento produciría unha programación menos previsible.</span><span class="sxs-lookup"><span data-stu-id="f0844-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="f0844-226">Neste sinxelo exemplo, é fácil dividir as horas por igual entre dous recursos.</span><span class="sxs-lookup"><span data-stu-id="f0844-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="f0844-227">Non obstante, en escenarios máis complexos que impliquen múltiples tarefas e múltiples recursos, PSA tería que facer suposicións sobre como debería asignar as reservas que se reciben para varios recursos en varias tarefas.</span><span class="sxs-lookup"><span data-stu-id="f0844-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="f0844-228">Por iso, nestes escenarios, o responsable do proxecto é o responsable de analizar as múltiples reservas e atribuílas segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="f0844-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="f0844-229">Para asignar as reservas, o xestor de proxectos atribúe as tarefas dos recursos xenéricos aos recursos nomeados e logo usa a vista **Conciliación** para asegurarse de que a asignación funciona coas reservas.</span><span class="sxs-lookup"><span data-stu-id="f0844-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="f0844-230">Editar un requisito de recurso</span><span class="sxs-lookup"><span data-stu-id="f0844-230">Edit a resource requirement</span></span>

<span data-ttu-id="f0844-231">Despois de que se crease un requisito de recurso, un xestor de proxectos ou xestor de recursos pode querer editar os detalles para refinar os criterios de busca cando se emprega o panel de programación.</span><span class="sxs-lookup"><span data-stu-id="f0844-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="f0844-232">Para editar o requisito de recurso, siga estes pasos.</span><span class="sxs-lookup"><span data-stu-id="f0844-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="f0844-233">Na páxina **Proxectos**, no separador **Equipo**, seleccione a ligazón a calquera requisito nun recurso xenérico.</span><span class="sxs-lookup"><span data-stu-id="f0844-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="f0844-234">Na páxina **Requisito de recurso** que aparece, pode actualizar varios atributos.</span><span class="sxs-lookup"><span data-stu-id="f0844-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="f0844-235">Aquí van algúns exemplos:</span><span class="sxs-lookup"><span data-stu-id="f0844-235">Here are some examples:</span></span>

    - <span data-ttu-id="f0844-236">Nome</span><span class="sxs-lookup"><span data-stu-id="f0844-236">Name</span></span>
    - <span data-ttu-id="f0844-237">Data de inicio</span><span class="sxs-lookup"><span data-stu-id="f0844-237">From Date</span></span>
    - <span data-ttu-id="f0844-238">Data final</span><span class="sxs-lookup"><span data-stu-id="f0844-238">To Date</span></span>
    - <span data-ttu-id="f0844-239">Duración</span><span class="sxs-lookup"><span data-stu-id="f0844-239">Duration</span></span>
    - <span data-ttu-id="f0844-240">Tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="f0844-240">Resource Type</span></span>

<span data-ttu-id="f0844-241">Na páxina **Requisito de recursos**, o xestor de proxectos ou o xestor de recursos tamén pode definir a seguinte información:</span><span class="sxs-lookup"><span data-stu-id="f0844-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="f0844-242">Habilidades</span><span class="sxs-lookup"><span data-stu-id="f0844-242">Skills</span></span>
- <span data-ttu-id="f0844-243">Roles</span><span class="sxs-lookup"><span data-stu-id="f0844-243">Roles</span></span>
- <span data-ttu-id="f0844-244">Preferencias de recurso</span><span class="sxs-lookup"><span data-stu-id="f0844-244">Resource preferences</span></span>
- <span data-ttu-id="f0844-245">Unidade organizativa preferida</span><span class="sxs-lookup"><span data-stu-id="f0844-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="f0844-246">Actualizar as reservas de recursos despois de que sexan reservadas nun proxecto</span><span class="sxs-lookup"><span data-stu-id="f0844-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="f0844-247">Despois de engadir un recurso xenérico ou nomeado a un equipo de proxecto, pode cambiar as reservas do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="f0844-248">Na páxina **Proxecto**, no separador **Equipo**, seleccione un membro do equipo e, a seguir, seleccione **Manter reservas**.</span><span class="sxs-lookup"><span data-stu-id="f0844-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Panel de programación aberto para o membro do equipo seleccionado](media/Resource-Management-image40.png)

    <span data-ttu-id="f0844-250">O panel de programación aparece e mostra as reservas do membro do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="f0844-251">Expanda o rexistro do membro do equipo para ver as horas reservadas con este proxecto e outros proxectos que estean consumindo a capacidade do membro do equipo.</span><span class="sxs-lookup"><span data-stu-id="f0844-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="f0844-252">Seleccione e arrastre a reserva para estendela ou acurtala.</span><span class="sxs-lookup"><span data-stu-id="f0844-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="f0844-253">Aparece a caixa de diálogo **Crear reserva de recurso** que permite axustar a reserva.</span><span class="sxs-lookup"><span data-stu-id="f0844-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Caixa de diálogo Crear reserva de recurso](media/Resource-Management-image41.png)

3. <span data-ttu-id="f0844-255">Prema botón dereito na reserva.</span><span class="sxs-lookup"><span data-stu-id="f0844-255">Right-click the booking.</span></span> <span data-ttu-id="f0844-256">Pode empregar o menú de atallo para realizar as seguintes accións:</span><span class="sxs-lookup"><span data-stu-id="f0844-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="f0844-257">Cambiar o estado da reserva.</span><span class="sxs-lookup"><span data-stu-id="f0844-257">Change the booking status.</span></span>
    - <span data-ttu-id="f0844-258">Editar a reserva.</span><span class="sxs-lookup"><span data-stu-id="f0844-258">Edit the booking.</span></span>
    - <span data-ttu-id="f0844-259">Substituír un recurso no equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="f0844-260">Cambiar o estado da reserva</span><span class="sxs-lookup"><span data-stu-id="f0844-260">Change the booking status</span></span>

<span data-ttu-id="f0844-261">Pode cambiar calquera estado de reserva predefinido ou personalizado.</span><span class="sxs-lookup"><span data-stu-id="f0844-261">You can change any default or custom booking status.</span></span>

![Comando Cambiar estado](media/Resource-Management-image42.png)

<span data-ttu-id="f0844-263">Os seguintes estados están incluídos en PSA:</span><span class="sxs-lookup"><span data-stu-id="f0844-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="f0844-264">**Cancelado** - Este estado cancela a reserva dun recurso e libera a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="f0844-265">**Reserva dura** - Este estado consume a capacidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="f0844-266">Unha reserva normalmente ten este estado cando se abre **Manter reservas** dende a grade **Todos os membros do equipo** na páxina **Proxectos**.</span><span class="sxs-lookup"><span data-stu-id="f0844-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="f0844-267">**Reserva branda** - Este estado engade un recurso a un equipo pero non consume a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="f0844-268">Indica que o recurso reservouse para traballos potenciais, pero aínda ten capacidade se é necesario noutros traballos.</span><span class="sxs-lookup"><span data-stu-id="f0844-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="f0844-269">Na vista de dispoñibilidade global dos recursos, as reservas brandas teñen un estado diferente das reservas duras.</span><span class="sxs-lookup"><span data-stu-id="f0844-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="f0844-270">**Proposto** - Este estado representa a proposta dun xestor de recursos ou xestor de proxectos para un recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="f0844-271">As propostas non consumen a capacidade dun recurso e o recurso non se engade ao equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="f0844-272">Para facer unha reserva dura dun recurso no equipo, o xestor de proxectos debe aceptar a proposta.</span><span class="sxs-lookup"><span data-stu-id="f0844-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="f0844-273">Enviar solicitudes de recursos</span><span class="sxs-lookup"><span data-stu-id="f0844-273">Submit resource requests</span></span>

<span data-ttu-id="f0844-274">As solicitudes de recursos úsanse para cubrir a demanda (requisito de recursos) que debe cumprir un xestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0844-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="f0844-275">Para un recurso xenérico que xa está no equipo, pode enviar unha solicitude de recurso directamente.</span><span class="sxs-lookup"><span data-stu-id="f0844-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="f0844-276">Pódese realizar unha solicitude de recursos de dous xeitos:</span><span class="sxs-lookup"><span data-stu-id="f0844-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="f0844-277">O xestor de recursos cumpre directamente a solicitude.</span><span class="sxs-lookup"><span data-stu-id="f0844-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="f0844-278">Neste caso, o recurso xenérico substitúese por unha reserva dura que ten un recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="f0844-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="f0844-279">O xestor de recursos propón un recurso ao xestor de proxectos e o responsable do proxecto aproba ou rexeita o recurso proposto.</span><span class="sxs-lookup"><span data-stu-id="f0844-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="f0844-280">Cumprimento directo das solicitudes de recursos</span><span class="sxs-lookup"><span data-stu-id="f0844-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="f0844-281">Cando se xera un requisito de recurso, o xestor de proxectos pode enviar unha solicitude de recurso para un recurso xenérico seleccionando o recurso e, a seguir, seleccionando **Enviar solicitude**.</span><span class="sxs-lookup"><span data-stu-id="f0844-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Botón Enviar solicitude](media/Resource-Management-image45.png)

<span data-ttu-id="f0844-283">Os comentarios sobre o recurso pódense proporcionar ao xestor de recursos que cumpra a solicitude.</span><span class="sxs-lookup"><span data-stu-id="f0844-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="f0844-284">Despois de enviar a solicitude, o campo **Estado** para o membro do equipo cambiase a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="f0844-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Introdución de comentarios opcionais](media/Resource-Management-image46.png)

<span data-ttu-id="f0844-286">Cando o xestor de recursos cumpre a solicitude, o membro do equipo xenérico substitúese polo recurso nomeado na grade **Todos os membros do equipo**.</span><span class="sxs-lookup"><span data-stu-id="f0844-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Membro do equipo xenérico substituído polo recurso nomeado na grade Todos os membros do equipo](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="f0844-288">Usar unha proposta de recurso para solicitudes de recursos</span><span class="sxs-lookup"><span data-stu-id="f0844-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="f0844-289">En lugar de reservar directamente un recurso nunha solicitude de recurso, un xestor de recursos pode propor un recurso ao xestor de proxectos.</span><span class="sxs-lookup"><span data-stu-id="f0844-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="f0844-290">Un xestor de recursos pode usar esta opción cando non se dispón dunha coincidencia exacta para os requisitos.</span><span class="sxs-lookup"><span data-stu-id="f0844-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="f0844-291">Cando un xestor de recursos propón un recurso, o xestor de proxectos ve que o campo **Estado** para o membro do equipo xenérico cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="f0844-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![O estado do membro do equipo xenérico cambiou a Necesita revisión](media/Resource-Management-image48.png)

<span data-ttu-id="f0844-293">Para ver o recurso proposto xunto cunha visualización do efecto da reserva da proposta, prema dúas veces no membro do equipo que ten un estado de **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="f0844-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="f0844-294">A seguir, seleccione o separador **Recursos propostos**.</span><span class="sxs-lookup"><span data-stu-id="f0844-294">Then select the **Proposed Resources** tab.</span></span>

![Separador Recursos propostos](media/Resource-Management-image49.png)

<span data-ttu-id="f0844-296">Seleccione **Aceptar todas as propostas** para aceptar todos os recursos propostos ou **Rexeitar todas as propostas** para rexeitalos.</span><span class="sxs-lookup"><span data-stu-id="f0844-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="f0844-297">Se acepta os recursos propostos, farase unha reserva dura no proxecto como membros do equipo e substitúen aos recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="f0844-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="f0844-298">Debe aceptar ou rexeitar todos os recursos propostos.</span><span class="sxs-lookup"><span data-stu-id="f0844-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="f0844-299">Non pode aceptalos ou rexeitalos parcialmente.</span><span class="sxs-lookup"><span data-stu-id="f0844-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="f0844-300">Substituír un recurso no equipo do proxecto</span><span class="sxs-lookup"><span data-stu-id="f0844-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="f0844-301">Ás veces, un xestor de proxectos debe substituír un membro reservado dun equipo nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="f0844-302">Na páxina **Proxectos**, no separador **Equipo**, seleccione un recurso que necesita un substituto e, a seguir, seleccione **Manter reservas**.</span><span class="sxs-lookup"><span data-stu-id="f0844-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="f0844-303">Expanda o recurso para ver os proxectos aos que está asignado.</span><span class="sxs-lookup"><span data-stu-id="f0844-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Recurso expandido para mostrar os proxectos asignados](media/Resource-Management-image50.png)

3. <span data-ttu-id="f0844-305">Co botón secundario, prema o proxecto e, a seguir, seleccione **Substituír recurso**.</span><span class="sxs-lookup"><span data-stu-id="f0844-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="f0844-306">Se coñece o recurso que desexa que substitúa ao recurso actual, seleccione ou escriba o nome e, a seguir, seleccione **Volver atribuír**.</span><span class="sxs-lookup"><span data-stu-id="f0844-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Especificación dun recurso substituto](media/Resource-Management-image51.png)

    <span data-ttu-id="f0844-308">Alternativamente, siga estes pasos para buscar un recurso:</span><span class="sxs-lookup"><span data-stu-id="f0844-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="f0844-309">Seleccione **Buscar substitución**.</span><span class="sxs-lookup"><span data-stu-id="f0844-309">Select **Find Substitution**.</span></span>

        ![Busca dun recurso substituto](media/Resource-Management-image52.png)

        <span data-ttu-id="f0844-311">O Asistente de programación devolve unha lista de substitutos dispoñibles.</span><span class="sxs-lookup"><span data-stu-id="f0844-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="f0844-312">No Asistente de programación, pode filtrar os recursos dispoñibles para atopar un substituto adecuado.</span><span class="sxs-lookup"><span data-stu-id="f0844-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Lista de substitutos dispoñibles](media/Resource-Management-image53.png)

    2. <span data-ttu-id="f0844-314">Para substituír o recurso, seleccione o recurso que desexe e, a seguir, seleccione **Substituír**.</span><span class="sxs-lookup"><span data-stu-id="f0844-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Substituír recurso seleccionado](media/Resource-Management-image54.png)

    <span data-ttu-id="f0844-316">As reservas e atribucións substitúense co novo recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![As reservas e atribucións substituídas co novo recurso](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="f0844-318">Conciliar reservas de membros de equipo e atribucións</span><span class="sxs-lookup"><span data-stu-id="f0844-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="f0844-319">Para os membros do equipo, as reservas e atribucións están emparelladas libremente.</span><span class="sxs-lookup"><span data-stu-id="f0844-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="f0844-320">Noutras palabras, os recursos poden ter atribucións pero sen reservas ou poden ter reservas pero sen atribucións.</span><span class="sxs-lookup"><span data-stu-id="f0844-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="f0844-321">O ideal sería que as reservas e atribucións estivesen aliñadas, de xeito que os recursos teñan capacidade comprometida para realizar as atribucións de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f0844-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="f0844-322">Non obstante, as reservas poden estar baseadas na dispoñibilidade e os calendarios de tarefas poderían cambiar a medida que o proxecto continúe.</span><span class="sxs-lookup"><span data-stu-id="f0844-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="f0844-323">Polo tanto, o emparellamento libre de reservas e atribucións proporciona flexibilidade.</span><span class="sxs-lookup"><span data-stu-id="f0844-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="f0844-324">PSA ten unha grade **Conciliación** que permite aos xestores de proxectos concilien as reservas dos membros do equipo e as súas atribucións para os equipos de proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Separador Conciliación](media/Resource-Management-image56.png)

<span data-ttu-id="f0844-326">O separador **Conciliación** mostra reservas e atribucións ata o nivel da tarefa individual para cada membro do equipo.</span><span class="sxs-lookup"><span data-stu-id="f0844-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="f0844-327">Amosa horas en celas que representan períodos de tempo desde meses ata días.</span><span class="sxs-lookup"><span data-stu-id="f0844-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="f0844-328">O separador tamén mostra un total neto global do proxecto, xunto cunha columna total.</span><span class="sxs-lookup"><span data-stu-id="f0844-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="f0844-329">Para cada recurso, o separador calcula a diferenza entre as reservas do membro do equipo e un resumo das atribucións do membro do equipo.</span><span class="sxs-lookup"><span data-stu-id="f0844-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="f0844-330">O ideal sería que esta diferenza fose 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="f0844-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="f0844-331">Noutras palabras, non debería haber ningunha diferenza entre reservas e atribucións.</span><span class="sxs-lookup"><span data-stu-id="f0844-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="f0844-332">As diferenzas están coloreadas e sombreadas para chamar a atención sobre dúas condicións:</span><span class="sxs-lookup"><span data-stu-id="f0844-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="f0844-333">**Escaseza de reservas** - A escaseza de reservas prodúcese cando un recurso ten máis atribucións que reservas.</span><span class="sxs-lookup"><span data-stu-id="f0844-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="f0844-334">Debido a que non se reservou esta capacidade, un xestor de proxectos podería querer corrixir esta condición ampliando as reservas do recurso para cubrir o déficit.</span><span class="sxs-lookup"><span data-stu-id="f0844-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="f0844-335">**Exceso de reservas** - O exceso de reservas prodúcese cando se reservou un recurso para o proxecto pero non foi asignado a tarefas.</span><span class="sxs-lookup"><span data-stu-id="f0844-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="f0844-336">Esta condición pode ser aceptable nos casos en que o recurso foi reservado para o proxecto antes de que se producise a atribución de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f0844-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="f0844-337">Non obstante, noutros casos, non está previsto atribuír tarefas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="f0844-338">Nestes casos, o xestor do proxecto debería considerar a cancelación das reservas do recurso, de xeito que a capacidade poida utilizarse para outro proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0844-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="f0844-339">Nalgúns casos, cando ve o tempo a un nivel superior ao nivel de día (por exemplo, a nivel de mes), pode que vexa unha diferenza neta de cero para un recurso (noutras palabras, reservas = atribucións).</span><span class="sxs-lookup"><span data-stu-id="f0844-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="f0844-340">Non obstante, se ve o tempo a nivel de semana, é posible que vexa que hai atribucións de cero horas e reservas de 40 horas na primeira semana, pero atribucións de 40 horas e reservas de cero horas na segunda semana.</span><span class="sxs-lookup"><span data-stu-id="f0844-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="f0844-341">En xeral, as reservas e atribucións conciliaranse, pero difiren dunha semana a outra.</span><span class="sxs-lookup"><span data-stu-id="f0844-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="f0844-342">Cando vexa o tempo a niveis máis altos, as celas do separador **Conciliación** ten un indicador para informar de que hai diferenzas a niveis máis baixos.</span><span class="sxs-lookup"><span data-stu-id="f0844-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="f0844-343">Ao premer dúas veces nunha cela, pode facer zoom para ver a diferenza.</span><span class="sxs-lookup"><span data-stu-id="f0844-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="f0844-344">A seguir, pode premer co botón dereito para facer zoom. Ao seleccionar un recurso e despois usar o control **Seguinte diferenza** na barra de ferramentas da rede, pode ir á seguinte diferenza entre reservas e atribucións para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="f0844-345">Pode entón usar o control **Diferencia anterior** para volver.</span><span class="sxs-lookup"><span data-stu-id="f0844-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="f0844-346">Tamén pode desactivar o indicador de diferenzas e o comportamento de navegación en **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="f0844-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Indicador de diferenzas](media/Resource-Management-image57.png)

<span data-ttu-id="f0844-348">Se ten atribucións de tarefas para un recurso pero non ten reservas, na páxina **Proxectos**, no separador **Conciliación**, seleccione a escaseza de reservas e logo seleccione **Estender a reserva**.</span><span class="sxs-lookup"><span data-stu-id="f0844-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="f0844-349">Aparece a caixa de diálogo **Estender reserva** e mostra a reserva que é necesaria para resolver a escaseza do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0844-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="f0844-350">Tamén amosa as reservas existentes do recurso en todos os proxectos ou outras entidades programables.</span><span class="sxs-lookup"><span data-stu-id="f0844-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="f0844-351">Se selecciona **Aceptar** para crear a reserva para o recurso, independentemente da dispoñibilidade dese recurso, pode causar un exceso de reservas.</span><span class="sxs-lookup"><span data-stu-id="f0844-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Caixa de diálogo de Estender reserva](media/Resource-Management-image58.png)

<span data-ttu-id="f0844-353">O xestor de proxectos ou xestor de recursos pode utilizar o panel de programación para xestionar calquera situación na que un recurso estea sobrecargado fóra da súa capacidade.</span><span class="sxs-lookup"><span data-stu-id="f0844-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
