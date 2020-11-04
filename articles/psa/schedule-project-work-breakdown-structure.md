---
title: Programar un proxecto coa estrutura de subdivisión do traballo
description: Como programar un proxecto coa estrutura de subdivisión do traballo (Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076314"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="8adc3-103">Programar un proxecto coa estrutura de subdivisión do traballo (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8adc3-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8adc3-104">Unha programación de proxecto communica que traballo é necesario levar a cabo, que recursos van realizar o traballo e o intervalo temporal que se precisa para concluír o traballo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="8adc3-105">A programación de proxecto reflicte todo o traballo asociado coa entrega do proxecto a tempo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="8adc3-106">Un dos primeiros pasos da fase de inicio do proxecto é facer unha programación de proxecto.</span><span class="sxs-lookup"><span data-stu-id="8adc3-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="8adc3-107">Para establecer unha programación de proxecto, ten que crear unha estrutura de subdivisión de traballo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="8adc3-108">Crear unha estrutura de proxecto cunha estrutura de subdivisión de traballo, axuda a:</span><span class="sxs-lookup"><span data-stu-id="8adc3-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="8adc3-109">Dividir o traballo en tarefas manexables</span><span class="sxs-lookup"><span data-stu-id="8adc3-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="8adc3-110">Estimar o tempo necesario para finalizar unha tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="8adc3-111">Definir as dependencias de tarefa e duración de tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="8adc3-112">Determinar os roles necesarios para completar cada tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="8adc3-113">A programación de proxecto na estrutura de subdivisión do traballo ten unha aparencia familiar, así como unha gráfica interactiva de Gantt.</span><span class="sxs-lookup"><span data-stu-id="8adc3-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="8adc3-114">Crear unha estrutura de subdivisión do traballo para un proxecto</span><span class="sxs-lookup"><span data-stu-id="8adc3-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="8adc3-115">Cree unha estrutura de subdivisión do traballo para representar a secuencia de tarefas nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="8adc3-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="8adc3-116">A estrutura de subdivisión do traballo inclúe tarefas, requirimentos para cada tarefa e a información de ingresos e custos.</span><span class="sxs-lookup"><span data-stu-id="8adc3-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="8adc3-117">Na estrutura de subdivisión do traballo, pode engadir:</span><span class="sxs-lookup"><span data-stu-id="8adc3-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="8adc3-118">A secuencia de tarefas nunha xerarquía</span><span class="sxs-lookup"><span data-stu-id="8adc3-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="8adc3-119">Outras tarefas que debe completar para poder iniciar unha tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="8adc3-120">A data inicial, a data final, e a duración dunha tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="8adc3-121">O número de horas necesarias para unha tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="8adc3-122">Os coñecementos e educación necesarios para un traballador</span><span class="sxs-lookup"><span data-stu-id="8adc3-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="8adc3-123">Os traballadores que están atribuídos a unha tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="8adc3-124">Os ingresos e custos estimados</span><span class="sxs-lookup"><span data-stu-id="8adc3-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="8adc3-125">Tipos de tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-125">Task types</span></span>  
<span data-ttu-id="8adc3-126">Usará os seguintes tipos de tarefas ao crear a estrutura de subdivisión do traballo:</span><span class="sxs-lookup"><span data-stu-id="8adc3-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="8adc3-127">**Nó de raíz de proxecto**</span><span class="sxs-lookup"><span data-stu-id="8adc3-127">**Project root node**</span></span> | <span data-ttu-id="8adc3-128">Tarefa de resumo de nivel superior para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="8adc3-128">The top-level summary task for the project.</span></span> <span data-ttu-id="8adc3-129">Todas as outras tarefas de proxecto créanse nela.</span><span class="sxs-lookup"><span data-stu-id="8adc3-129">All other project tasks are created under it.</span></span> <span data-ttu-id="8adc3-130">O nome da tarefa de raíz é o nome de proxecto.</span><span class="sxs-lookup"><span data-stu-id="8adc3-130">The name of the root task is the project name.</span></span> <span data-ttu-id="8adc3-131">O esforzo, as datas e a duración do nó de raíz están baseados nos valores na xerarquía de abaixo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="8adc3-132">Non se poden editar os nós de propiedades ou eliminar o nó de raíz.</span><span class="sxs-lookup"><span data-stu-id="8adc3-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="8adc3-133">**Tarefas de resumo ou contedor**</span><span class="sxs-lookup"><span data-stu-id="8adc3-133">**Summary or container tasks**</span></span> | <span data-ttu-id="8adc3-134">Unha tarefa de resumo é unha tarefa con subtarefas.</span><span class="sxs-lookup"><span data-stu-id="8adc3-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="8adc3-135">Unha tarefa de resumo non ten un esforzo de traballo ou custo propio.</span><span class="sxs-lookup"><span data-stu-id="8adc3-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="8adc3-136">O esforzo de traballo e o custo son un resumo das subtarefas.</span><span class="sxs-lookup"><span data-stu-id="8adc3-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="8adc3-137">Pode modificar o nome dunha tarefa de resumo, mais non pode cambiar o esforzo, as datas ou a duración, porque eses calcúlanse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8adc3-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="8adc3-138">Ao eliminar unha tarefa de resumo elimínase a tarefa e todas as subtarefas.</span><span class="sxs-lookup"><span data-stu-id="8adc3-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="8adc3-139">**Tarefas de nó folla**</span><span class="sxs-lookup"><span data-stu-id="8adc3-139">**Leaf node tasks**</span></span> | <span data-ttu-id="8adc3-140">As tarefas nó follas representan o traballo máis detallado no proxecto.</span><span class="sxs-lookup"><span data-stu-id="8adc3-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="8adc3-141">Ten un esforzo estimado, varios recursos planificados, datas de inicio e fin planificadas e unha duración.</span><span class="sxs-lookup"><span data-stu-id="8adc3-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="8adc3-142">Xerarquía de tarefas</span><span class="sxs-lookup"><span data-stu-id="8adc3-142">Task hierarchy</span></span>  
 <span data-ttu-id="8adc3-143">Ten as seguintes opcións ao crear unha xerarquía de tarefa:</span><span class="sxs-lookup"><span data-stu-id="8adc3-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="8adc3-144">**Engadir tarefa**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-144">**Add task**.</span></span>   <span data-ttu-id="8adc3-145">Pode engadir unha tarefa nunha posición que escolla na xerarquía de tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="8adc3-146">Se non selecciona unha posición, a nova tarefa aparece no fin.</span><span class="sxs-lookup"><span data-stu-id="8adc3-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="8adc3-147">**Aplicar sangría á tarefa**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-147">**Indent task**.</span></span>   <span data-ttu-id="8adc3-148">Aplicar sangría a unha tarefa para torna a que está enriba secundaria.</span><span class="sxs-lookup"><span data-stu-id="8adc3-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="8adc3-149">**Eliminar sangría dunha tarefa**</span><span class="sxs-lookup"><span data-stu-id="8adc3-149">**Outdent task**.</span></span>   <span data-ttu-id="8adc3-150">Elimine a sangría dunha tarefa para facer para que deixe de ser unha subtarefa da súa tarefa primaria orixinal.</span><span class="sxs-lookup"><span data-stu-id="8adc3-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="8adc3-151">**Mover para arriba e mover para abaixo**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-151">**Move up and Move down**.</span></span>   <span data-ttu-id="8adc3-152">Mova tarefas arriba ou abaixo na xerarquía da tarefa primaria.</span><span class="sxs-lookup"><span data-stu-id="8adc3-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="8adc3-153">Mover unha tarefa arriba ou baixo non ten efecto no seu esforzo, custo, datas ou duración.</span><span class="sxs-lookup"><span data-stu-id="8adc3-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="8adc3-154">Atributos de lista</span><span class="sxs-lookup"><span data-stu-id="8adc3-154">Task attributes</span></span>  
 <span data-ttu-id="8adc3-155">O nome dunha tarefa describe o traballo que precisa ser concluído.</span><span class="sxs-lookup"><span data-stu-id="8adc3-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="8adc3-156">Pode utilizar varios atributos de tarefas para describir a programación e os requirimentos de persoal para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="8adc3-157">Programar atributos</span><span class="sxs-lookup"><span data-stu-id="8adc3-157">Schedule attributes</span></span>

 - <span data-ttu-id="8adc3-158">Atribuír valores a **Horas de esforzo** , **Número de recursos** , **Data de Inicio** , **Data de Fin** e **Duración** para determinar a programación para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-158">Assign values to **Effort hours** , **Number of resources** , **Start date** , **End date** , and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="8adc3-159">**Esforzo** é a estimación de horas que leva concluír a tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="8adc3-160">**Número de recursos** é unha estimación que o xestor de proxecto pon na tarefa para axudar a crear a mellor programación posible.</span><span class="sxs-lookup"><span data-stu-id="8adc3-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="8adc3-161">**Duración** (en días) indica o número de días laborables que levará concluír a tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="8adc3-162">Atributos de persoal</span><span class="sxs-lookup"><span data-stu-id="8adc3-162">Staffing attributes</span></span>

 - <span data-ttu-id="8adc3-163">**Rol** , **Unidade da organización de recursos** , **Número de recursos** e **Recursos** describen os requisitos de persoal da tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-163">**Role** , **Resource organizational unit** , **Number of resources** , and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="8adc3-164">**Rol** describe o tipo de recurso necesario para realizar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="8adc3-165">**Unidade de organización de recursos** indica a unidade da organización da que vén o persoal dos recursos para esa tarefa; isto tamén afecta a estiamción de vendas e custo, xa que se ten en conta para determinar o prezo de venda da unidade para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8adc3-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="8adc3-166">**Recursos** mantén un recurso xenérico ou un recurso con nome cando se atopa un.</span><span class="sxs-lookup"><span data-stu-id="8adc3-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="8adc3-167">Dependencias de tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-167">Task dependencies</span></span>  
 <span data-ttu-id="8adc3-168">Pode crear relacións de predecesor entre unha ou varias tarefas na estrutura de subdivisión de traballo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="8adc3-169">Pode definir un ou máis valores para o campo predecesor nas tarefas para indicar as tarefas das que dependerá.</span><span class="sxs-lookup"><span data-stu-id="8adc3-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="8adc3-170">Cando atribúe un valor predecesor a unha tarefa, a tarefa só pode iniciarse cando todas as tarefas predecesoras conclúan.</span><span class="sxs-lookup"><span data-stu-id="8adc3-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="8adc3-171">Definir este dependencia nunha tarefa levará a recalcular a data de inicio planificada da tarefa como o último fin de todos os predecesores.</span><span class="sxs-lookup"><span data-stu-id="8adc3-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="8adc3-172">Os impactos relacionados cos predecesores nunha programación non están limitados polo modo de tarefa definido na tarefa.</span><span class="sxs-lookup"><span data-stu-id="8adc3-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="8adc3-173">Modo de tarefa</span><span class="sxs-lookup"><span data-stu-id="8adc3-173">Task mode</span></span>  
 <span data-ttu-id="8adc3-174">O modo de tarefa é unha dos factores importante que determinan tarefas de nó folla de programación.</span><span class="sxs-lookup"><span data-stu-id="8adc3-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="8adc3-175">Hai dous modos de tarefa para cada tarefa: modo automático e modo de programación manual.</span><span class="sxs-lookup"><span data-stu-id="8adc3-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="8adc3-176">**Programación automática**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-176">**Auto scheduling**.</span></span>   <span data-ttu-id="8adc3-177">Cando establece o modo de tarefa a Programada automaticamente, o motor de programación de tarefas usa as regras de programación nos seguintes atributos de tarefa para determinar a programación para a tarefa:</span><span class="sxs-lookup"><span data-stu-id="8adc3-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="8adc3-178">Predecesores</span><span class="sxs-lookup"><span data-stu-id="8adc3-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="8adc3-179">Esforzo</span><span class="sxs-lookup"><span data-stu-id="8adc3-179">Effort</span></span>  
  
    -   <span data-ttu-id="8adc3-180">Número de recursos</span><span class="sxs-lookup"><span data-stu-id="8adc3-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="8adc3-181">Datas de inicio e de fin</span><span class="sxs-lookup"><span data-stu-id="8adc3-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="8adc3-182">**Regras de programación**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-182">**Scheduling rules**.</span></span>   <span data-ttu-id="8adc3-183">A data de inicio dunha tarefa de nó folla que non teña predecesores ten por defecto a data de inicio da programación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="8adc3-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="8adc3-184">A duración dunha tarefa de nó folla calcúlase sempre como o número de días laborables entre as datas de inicio e fin.</span><span class="sxs-lookup"><span data-stu-id="8adc3-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="8adc3-185">Cando unha tarefa automaticamente está programada, o motor de programación segue as regras seguintes:</span><span class="sxs-lookup"><span data-stu-id="8adc3-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="8adc3-186">As datas de inicio e fin dunha tarefa sempre deben ser días laborables segundo o calendario de programación do proxecto</span><span class="sxs-lookup"><span data-stu-id="8adc3-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="8adc3-187">A data de inicio dunha tarefa que teña predecesores ten por defecto a última data de fin dos seus predecesores</span><span class="sxs-lookup"><span data-stu-id="8adc3-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="8adc3-188">Esforzo = Número de persoas \* Duración \* horas nun día laborable estándar do calendario de proxecto</span><span class="sxs-lookup"><span data-stu-id="8adc3-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="8adc3-189">**Programación manual**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-189">**Manual scheduling**.</span></span>   <span data-ttu-id="8adc3-190">Nalgúns casos, é posible que desexe afastarse destas regras.</span><span class="sxs-lookup"><span data-stu-id="8adc3-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="8adc3-191">Nestes casos, pode definir que o modo de tarefas para a tarefa se programe manualmente.</span><span class="sxs-lookup"><span data-stu-id="8adc3-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="8adc3-192">Isto fai que o motor de programación non calcule os valores para outros atributos de programación.</span><span class="sxs-lookup"><span data-stu-id="8adc3-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="8adc3-193">Configurar os predecesores nas tarefas sempre afecta a data de comezo da tarefa dependente.</span><span class="sxs-lookup"><span data-stu-id="8adc3-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="8adc3-194">Crear unha estrutura de subdivisión do traballo</span><span class="sxs-lookup"><span data-stu-id="8adc3-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="8adc3-195">Vaia a **Project Service > Proxectos**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="8adc3-196">Prema no proxecto no que quere traballar.</span><span class="sxs-lookup"><span data-stu-id="8adc3-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="8adc3-197">Na barra da parte superior da pantalla, seleccione a frecha cara abaixo ao lado do nome do proxecto e, a seguir, prema Estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="8adc3-198">Para engadir unha tarefa, prema **Engadir Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="8adc3-199">Complete os campos para a tarefa e, a seguir, prema en **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="8adc3-200">Continúe a engadir tarefas até que conclúa a estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="8adc3-201">Ao crear a estrutura de subdivisión do traballo, pode realizar o seguinte para organizar as súas tarefas:</span><span class="sxs-lookup"><span data-stu-id="8adc3-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="8adc3-202">Seleccione unha tarefa e prema **Aplicar sangría** para movela a outra tarefa ou prema Eliminar sangría para movela un nivel.</span><span class="sxs-lookup"><span data-stu-id="8adc3-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="8adc3-203">Seleccione unha tarefa e prema **Mover para arriba** ou **Mover para abaixo** para movela cara arriba ou cara a abaixo na lista.</span><span class="sxs-lookup"><span data-stu-id="8adc3-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="8adc3-204">Prema **Ocultar Gantt** para ocultar a gráfica de Gantt e prema **Mostrar Gantt** para mostrala de novo.</span><span class="sxs-lookup"><span data-stu-id="8adc3-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="8adc3-205">Seleccione outro período de tempo para a gráfica de Gantt en **Escala de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="8adc3-206">Para engadir os roles especificados na estrutura de subdivisión do traballo aos membros do equipo do proxecto, prema **Xerar equipo de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="8adc3-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="8adc3-207">Prema **Gardar** na parte inferior dereita da pantalla cando remate as modificacións.</span><span class="sxs-lookup"><span data-stu-id="8adc3-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8adc3-208">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="8adc3-208">See Also</span></span>  
 [<span data-ttu-id="8adc3-209">Guía do xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="8adc3-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
