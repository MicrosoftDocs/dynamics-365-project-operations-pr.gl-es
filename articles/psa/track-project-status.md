---
title: Rastrexar o estado dun proxecto
description: Como rastrexar o estado dun proxecto en Project Service
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076218"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="4d62d-103">Rastrexar o estado dun proxecto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4d62d-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4d62d-104">Utilice a [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para rastrexar o progreso do proxecto dun cliente.</span><span class="sxs-lookup"><span data-stu-id="4d62d-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="4d62d-105">A medida que o compromiso progresa, as fases do proxecto actualízanse para reflectir a fase do compromiso:</span><span class="sxs-lookup"><span data-stu-id="4d62d-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="4d62d-106">**Novo**</span><span class="sxs-lookup"><span data-stu-id="4d62d-106">**New**</span></span>    | <span data-ttu-id="4d62d-107">Ao crear un proxecto, a fase está definida en **Nova**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="4d62d-108">Se creou o proxecto a partir dun modelo, nesta fase o proxecto pode ter unha programación, estimacións e datos de equipo.</span><span class="sxs-lookup"><span data-stu-id="4d62d-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="4d62d-109">En caso contrario, será o esquema do proxecto e terá que introducir o resto dos compoñentes do proxecto manualmente.</span><span class="sxs-lookup"><span data-stu-id="4d62d-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="4d62d-110">**Oferta**</span><span class="sxs-lookup"><span data-stu-id="4d62d-110">**Quote**</span></span>   |      <span data-ttu-id="4d62d-111">Cando asocia un proxecto a unha oferta ou crea un proxecto a partir dunha oferta, a fase de proxecto está definida en **Oferta** , e as datas de inicio e fin estimadas tamén se actualizan.</span><span class="sxs-lookup"><span data-stu-id="4d62d-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="4d62d-112">Cando o proxecto está en fase de oferta, móstranse detalles da oferta no separador **Sales** na páxina **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="4d62d-113">**Planificar**</span><span class="sxs-lookup"><span data-stu-id="4d62d-113">**Plan**</span></span>   |                                     <span data-ttu-id="4d62d-114">Cando gaña unha oferta asociada a un proxecto, e cando o compromiso progresa á fase de contrato, a fase de proxecto actualízase a **Planificar**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="4d62d-115">A información do contrato aparece no separador **Sales** na páxina **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="4d62d-116">**Completada**</span><span class="sxs-lookup"><span data-stu-id="4d62d-116">**Complete**</span></span> |                    <span data-ttu-id="4d62d-117">Cando conclúa o traballo de proxecto, pode cambiar a fase a **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="4d62d-118">Cando a fase de proxecto está definida en concluído, enténdese que o traballo está o 100% concluído pero o proxecto queda aberto para entradas de tempo ou gastos pendentes de ser rexistradas.</span><span class="sxs-lookup"><span data-stu-id="4d62d-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="4d62d-119">**Pechar**</span><span class="sxs-lookup"><span data-stu-id="4d62d-119">**Close**</span></span>   |           <span data-ttu-id="4d62d-120">Cando todas as transaccións están rexistradas no proxecto e non espera máis, pode manualmente configurar a fase a **Pechar**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="4d62d-121">Cando o proxecto está definido como **Pechar** , non pode rexistrar máis transaccións no proxecto e o proxecto será só de lectura.</span><span class="sxs-lookup"><span data-stu-id="4d62d-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="4d62d-122">Para rastrexar o estado dun proxecto</span><span class="sxs-lookup"><span data-stu-id="4d62d-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="4d62d-123">Vaia a **Project Service > Proxectos**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="4d62d-124">Prema no proxecto no que quere traballar.</span><span class="sxs-lookup"><span data-stu-id="4d62d-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="4d62d-125">Na barra da parte superior da pantalla, seleccione a frecha cara abaixo ao lado do nome do proxecto e, a seguir, prema **Rastrexar proxecto**.</span><span class="sxs-lookup"><span data-stu-id="4d62d-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="4d62d-126">Seleccione **Rastrexo de esforzo** ou **Rastrexo de custo** na lista despregable enriba da lista de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4d62d-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="4d62d-127">Prema dúas veces nunha tarefa para editala.</span><span class="sxs-lookup"><span data-stu-id="4d62d-127">Double-click any task to edit it.</span></span> <span data-ttu-id="4d62d-128">Tamén pode mover ou redimensionar as barras na gráfica Gantt para modificar a hora e o progreso dunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="4d62d-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="4d62d-129">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="4d62d-129">See Also</span></span>  
 [<span data-ttu-id="4d62d-130">Guía do xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="4d62d-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
