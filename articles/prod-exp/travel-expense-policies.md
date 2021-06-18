---
title: Configurar políticas de gasto
description: Pode configurar as políticas de gastos que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes en Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005744"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="871cb-103">Configurar políticas de gasto</span><span class="sxs-lookup"><span data-stu-id="871cb-103">Set up expense policies</span></span>

<span data-ttu-id="871cb-104">Pode definir as políticas que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes.</span><span class="sxs-lookup"><span data-stu-id="871cb-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="871cb-105">A aplicación de políticas de gastos pode axudarlle a xestionar os gastos de xeito eficaz.</span><span class="sxs-lookup"><span data-stu-id="871cb-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="871cb-106">Por exemplo, pode establecer unha política de gastos de hotel en Nova York, na que se afirma que o gasto por noite non pode superar os 250 USD.</span><span class="sxs-lookup"><span data-stu-id="871cb-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="871cb-107">Se un traballador presenta un informe de gastos ou unha solicitude de viaxe na que a tarifa da habitación supera esta cantidade, o sistema notificará</span><span class="sxs-lookup"><span data-stu-id="871cb-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="871cb-108">ao traballador que se superou o importe da política para o gasto.</span><span class="sxs-lookup"><span data-stu-id="871cb-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="871cb-109">Pode configurar a mensaxe que recibirá o traballador cando</span><span class="sxs-lookup"><span data-stu-id="871cb-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="871cb-110">defina a política.</span><span class="sxs-lookup"><span data-stu-id="871cb-110">define the policy.</span></span>      
        
<span data-ttu-id="871cb-111">Pode definir tres tipos de políticas:</span><span class="sxs-lookup"><span data-stu-id="871cb-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="871cb-112">Advertencia – Permite ao traballador presentar un informe de gastos ou unha solicitude de viaxe pero o gasto marcarase para todos os responsables de aprobacións</span><span class="sxs-lookup"><span data-stu-id="871cb-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="871cb-113">e para informes posteriores.</span><span class="sxs-lookup"><span data-stu-id="871cb-113">for later reporting.</span></span>        

- <span data-ttu-id="871cb-114">Erro – Esixe ao traballador que revise o gasto para cumprir coa política antes de enviar o informe de gastos ou a solicitude de viaxe.</span><span class="sxs-lookup"><span data-stu-id="871cb-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="871cb-115">Xustificación – Require que o traballador ou un xestor introduza unha xustificación por superar o importe da política antes de enviar o informe de gastos ou a solicitude de viaxe.</span><span class="sxs-lookup"><span data-stu-id="871cb-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="871cb-116">Consellos sobre políticas</span><span class="sxs-lookup"><span data-stu-id="871cb-116">Policy tips</span></span>
<span data-ttu-id="871cb-117">Aquí ten algunhas suxestións que poden axudarlle á hora de crear novas políticas para a xestión de gastos.</span><span class="sxs-lookup"><span data-stu-id="871cb-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="871cb-118">As políticas teñen data de entrada en vigor e non entrarán en vigor se a política se crea cunha data posterior á data na que se produciu o gasto.</span><span class="sxs-lookup"><span data-stu-id="871cb-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="871cb-119">Por exemplo, se está a crear unha nova política hoxe para aplicar un gasto máximo de comida de 50 $, os gastos existentes introducidos ata onte non se compararán con esta política.</span><span class="sxs-lookup"><span data-stu-id="871cb-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="871cb-120">Ao crear unha política para unha categoría de gastos que se poida detallar, considere engadir unha condición para o tipo de liña de gasto.</span><span class="sxs-lookup"><span data-stu-id="871cb-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="871cb-121">É posible que algunhas políticas como esixir un recibo non teñan sentido para as liñas detalladas e só se deben aplicar á liña de cabeceira ou a unha liña non detallada.</span><span class="sxs-lookup"><span data-stu-id="871cb-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="871cb-122">As políticas de xestión de gastos avalíanse por defecto con respecto á entidade de orixe.</span><span class="sxs-lookup"><span data-stu-id="871cb-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="871cb-123">Para os escenarios entre empresas, pode definir a política que se avaliará coa entidade de destino (entidade prestameira).</span><span class="sxs-lookup"><span data-stu-id="871cb-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="871cb-124">Para executar as políticas contra a entidade de destino, active a funcionalidade "Avaliar a política de gastos fronte á entidade legal prestameira" na área de traballo **Xestión de funcionalidades**.</span><span class="sxs-lookup"><span data-stu-id="871cb-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="871cb-125">Cando avaliar as políticas</span><span class="sxs-lookup"><span data-stu-id="871cb-125">When to evaluate policies</span></span>

<span data-ttu-id="871cb-126">Nos parámetros de xestión de gastos, hai unha opción para avaliar as políticas de xestión de gastos cando se garda unha liña ou cando se envía un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="871cb-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="871cb-127">Se elixe avaliar cando se garda unha liña, isto garante que os usuarios terán unha visibilidade previa do que deben facer para completar o seu informe de gastos á vez.</span><span class="sxs-lookup"><span data-stu-id="871cb-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="871cb-128">Se non o fai, pode atrasar a avaliación da política e aforrar tempo se fai que a validación ocorra ao final, durante o envío ao fluxo de traballo.</span><span class="sxs-lookup"><span data-stu-id="871cb-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]