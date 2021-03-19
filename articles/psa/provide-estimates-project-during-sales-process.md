---
title: Fornecer estimacións de traballo para un proxecto durante o proceso de vendas
description: Como fornecer estimacións de traballo para un proxecto durante o proceso de vendas en Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283546"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="b0616-103">Fornecer estimacións de traballo para un proxecto durante o proceso de vendas (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b0616-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b0616-104">Durante o proceso de vendas, pode calcular estimacións de vendas desde o principio con liñas de oferta.</span><span class="sxs-lookup"><span data-stu-id="b0616-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="b0616-105">As capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] proporcionan unha forma máis científica e coherente de calcular estimacións de vendas desagregando elementos de traballo e asociando os atributos relevantes que contribúen ás estimacións para o proxecto na estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="b0616-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="b0616-106">Unha vez gañada a venda, pode utilizar a estrutura de subdivisión do traballo asociada no seu plan de proxecto, precisándoa segundo sexa necesario para a conclusión correcta do seu proxecto.</span><span class="sxs-lookup"><span data-stu-id="b0616-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="b0616-107">Ligar un proxecto a unha liña de oferta</span><span class="sxs-lookup"><span data-stu-id="b0616-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="b0616-108">Ao crear unha liña de oferta baseada en proxecto, pode crear un novo proxecto desde a liña da oferta.</span><span class="sxs-lookup"><span data-stu-id="b0616-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="b0616-109">Despois pode utilizar modelos de proxecto, que poden ser estimacións financeiras e plans de proxecto predefinido estándar configurados previamente comúns para a súa organización, ou unha copia dunha estimación ou un plan de proxecto dun proxecto anterior.</span><span class="sxs-lookup"><span data-stu-id="b0616-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="b0616-110">Ao crear un proxecto, escoller un modelo de proxecto fornece a base para refinar os requirimentos do plan, a estimación e o rol do proxecto.</span><span class="sxs-lookup"><span data-stu-id="b0616-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="b0616-111">Ao crear o proxecto desde unha oferta, o proxecto asóciase automaticamente á liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="b0616-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="b0616-112">Compoñentes de estimate de proxecto</span><span class="sxs-lookup"><span data-stu-id="b0616-112">Project estimate components</span></span>  
 <span data-ttu-id="b0616-113">A estrutura de subdivisión do traballo nun proxecto proporciona unha forma de dividir o traballo en tarefas, manter unha xerarquía de tarefas e atribuír unha estimación de esforzo necesaria para completar as tarefas.</span><span class="sxs-lookup"><span data-stu-id="b0616-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="b0616-114">Tamén pode asociar os roles a unha tarefa para indicar unha estimación do tipo de recurso necesario para finalizar unha tarefa e unha programación.</span><span class="sxs-lookup"><span data-stu-id="b0616-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="b0616-115">A estrutura de subdivisión do traballo axuda a determinar o esforzo de traballo e as estimacións de programación.</span><span class="sxs-lookup"><span data-stu-id="b0616-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="b0616-116">Por defecto, o proxecto utiliza listas de prezos predefinidas que definiu anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b0616-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="b0616-117">Os prezos de custos e vendas definidos nas listas de prezos axudan a determinar estimacións financeiras para a subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="b0616-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="b0616-118">Se o seu proxecto está asociado a unha oferta, e a oferta ten unha lista de prezos diferente da predefinida, a lista de prezos da oferta úsase para estimacións de actividades financeiras.</span><span class="sxs-lookup"><span data-stu-id="b0616-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="b0616-119">Estimacións de importación dun proxecto a unha oferta</span><span class="sxs-lookup"><span data-stu-id="b0616-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="b0616-120">Unha vez teña estimacións de proxecto nun proxecto, pode importar estas estimacións na liña da oferta:</span><span class="sxs-lookup"><span data-stu-id="b0616-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="b0616-121">En **Detalles da liña de oferta**, prema en **Importar de estimacións**.</span><span class="sxs-lookup"><span data-stu-id="b0616-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="b0616-122">Seleccione se desexa importar estimacións de proxecto resumidas por tipo de transacción, rol ou nivel de nó da estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="b0616-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b0616-123">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="b0616-123">See Also</span></span>  
 [<span data-ttu-id="b0616-124">Guía do xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="b0616-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]