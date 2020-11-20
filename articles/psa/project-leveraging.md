---
title: Proxectos e estimacións de vendas
description: Este tema fornece información sobre como aproveitar a programación e as estimacións no proceso de vendas.
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120676"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="25840-103">Proxectos e estimacións de vendas</span><span class="sxs-lookup"><span data-stu-id="25840-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="25840-104">Durante o proceso de vendas, pode crear estimacións de vendas ligando un proxecto a unha oferta de vendas.</span><span class="sxs-lookup"><span data-stu-id="25840-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="25840-105">Deste xeito, pode producirse unha estimación determinista durante o proceso de vendas, para aproveitar as capacidades de programación e estimación de proxectos.</span><span class="sxs-lookup"><span data-stu-id="25840-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="25840-106">Se a venda continúa, pódese empregar a programación que se empregou con fins de estimación de vendas como base para o refinamento adicional do plan do proxecto.</span><span class="sxs-lookup"><span data-stu-id="25840-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="25840-107">Ligar un proxecto a unha liña de oferta</span><span class="sxs-lookup"><span data-stu-id="25840-107">Linking a project to a quote line</span></span>

<span data-ttu-id="25840-108">Cando crea unha liña de oferta baseada en proxectos, pode crear un proxecto novo ou asociar un proxecto existente na páxina **Liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="25840-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulario de liña de oferta](media/project-8.png)
 
<span data-ttu-id="25840-110">Cando crea un novo proxecto a partir dos detalles da liña de oferta, pode aproveitar os modelos de proxecto.</span><span class="sxs-lookup"><span data-stu-id="25840-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="25840-111">Os modelos de proxectos son proxectos modelo que representan plans de proxecto estándar e estimacións financeiras típicas dunha organización.</span><span class="sxs-lookup"><span data-stu-id="25840-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="25840-112">Tamén poden representar copias de plans de proxectos e estimacións de proxectos pasados.</span><span class="sxs-lookup"><span data-stu-id="25840-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalles da liña de oferta](media/project-9.png)
  
<span data-ttu-id="25840-114">Cando cree o proxecto desde unha oferta, o proxecto asóciase automaticamente á liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="25840-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="25840-115">Compoñentes das estimacións nun proxecto</span><span class="sxs-lookup"><span data-stu-id="25840-115">Components of estimates in a project</span></span>

<span data-ttu-id="25840-116">Unha programación permítelle dividir o traballo en tarefas, manter unha xerarquía de tarefas, determinar que recursos son necesarios para completar unha tarefa e atribuír unha estimación do esforzo que se require para completar unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="25840-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="25840-117">Pode definir o esforzo de traballo e programar estimacións mediante os campos do separador **Programación** da páxina **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="25840-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="25840-118">Debido a que unha lista de prezos está asociada ao proxecto, as estimacións financeiras calcúlanse mediante os prezos de custos e vendas definidos na lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="25840-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="25840-119">Importación de estimacións dun proxecto a unha oferta</span><span class="sxs-lookup"><span data-stu-id="25840-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="25840-120">Despois de definir as estimacións do proxecto, pode importalas na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="25840-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="25840-121">Na páxina **Detalles de liña de oferta**, seleccione **Importación das estimacións** na fita para resumir as estimacións do proxecto por tipo de transacción, rol ou nivel de tarefa.</span><span class="sxs-lookup"><span data-stu-id="25840-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
