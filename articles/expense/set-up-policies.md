---
title: Definir políticas de gastos
description: Pode definir as políticas de gastos que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076202"
---
# <a name="define-expense-policies"></a><span data-ttu-id="cec0c-103">Definir políticas de gastos</span><span class="sxs-lookup"><span data-stu-id="cec0c-103">Define expense policies</span></span>

<span data-ttu-id="cec0c-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="cec0c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cec0c-105">Pode definir as políticas que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes.</span><span class="sxs-lookup"><span data-stu-id="cec0c-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="cec0c-106">A aplicación de políticas de gastos pode axudarlle a xestionar os gastos de xeito eficaz.</span><span class="sxs-lookup"><span data-stu-id="cec0c-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="cec0c-107">Por exemplo, pode establecer unha política de gastos de hotel en Nova York, na que se afirma que o gasto por noite non pode superar os 250 USD.</span><span class="sxs-lookup"><span data-stu-id="cec0c-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="cec0c-108">Se un traballador presenta un informe de gastos ou unha solicitude de viaxe na que a tarifa da habitación supera esta cantidade, o sistema notificará</span><span class="sxs-lookup"><span data-stu-id="cec0c-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="cec0c-109">ao traballador que se superou o importe da política para o gasto.</span><span class="sxs-lookup"><span data-stu-id="cec0c-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="cec0c-110">Pode configurar a mensaxe que recibirá o traballador cando</span><span class="sxs-lookup"><span data-stu-id="cec0c-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="cec0c-111">defina a política.</span><span class="sxs-lookup"><span data-stu-id="cec0c-111">define the policy.</span></span>      
        
<span data-ttu-id="cec0c-112">Pode definir tres tipos de políticas:</span><span class="sxs-lookup"><span data-stu-id="cec0c-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="cec0c-113">**Advertencia** : Permite ao traballador presentar un informe de gastos ou unha solicitude de viaxe pero o gasto marcarase para todos os responsables de aprobacións</span><span class="sxs-lookup"><span data-stu-id="cec0c-113">**Warning** : Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="cec0c-114">e para informes posteriores.</span><span class="sxs-lookup"><span data-stu-id="cec0c-114">for later reporting.</span></span>        

- <span data-ttu-id="cec0c-115">**Erro** : Esixe ao traballador que revise o gasto para cumprir coa política antes de enviar o informe de gastos ou a solicitude de viaxe.</span><span class="sxs-lookup"><span data-stu-id="cec0c-115">**Error** : Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="cec0c-116">**Xustificación** : Require que o traballador ou un xestor introduza unha xustificación por superar o importe da política antes de enviar o informe de gastos ou a solicitude de viaxe.</span><span class="sxs-lookup"><span data-stu-id="cec0c-116">**Justification** : Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="cec0c-117">Consellos sobre políticas</span><span class="sxs-lookup"><span data-stu-id="cec0c-117">Policy tips</span></span>
<span data-ttu-id="cec0c-118">Aquí ten algunhas suxestións que poden axudarlle á hora de crear novas políticas para a xestión de gastos:</span><span class="sxs-lookup"><span data-stu-id="cec0c-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="cec0c-119">As políticas teñen data de entrada en vigor, o que significa que unha política non entrará en vigor se se crea cunha data posterior á data na que se produciu o gasto.</span><span class="sxs-lookup"><span data-stu-id="cec0c-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="cec0c-120">Por exemplo, vostede crea unha nova política hoxe para aplicar un gasto máximo de comida de 50 $.</span><span class="sxs-lookup"><span data-stu-id="cec0c-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="cec0c-121">Os gastos existentes introducidos ata onte non se comprobarán con esta política.</span><span class="sxs-lookup"><span data-stu-id="cec0c-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="cec0c-122">Ao crear unha política para unha categoría de gastos que se poida detallar, considere engadir unha condición para o tipo de liña de gasto.</span><span class="sxs-lookup"><span data-stu-id="cec0c-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="cec0c-123">Algunhas políticas, como esixir un recibo, poden non ter sentido para as liñas detalladas.</span><span class="sxs-lookup"><span data-stu-id="cec0c-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="cec0c-124">Nesta situación, a política só se aplica á liña de cabeceira ou a unha liña non detallada.</span><span class="sxs-lookup"><span data-stu-id="cec0c-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="cec0c-125">As políticas de xestión de gastos avalíanse por defecto con respecto á entidade de orixe.</span><span class="sxs-lookup"><span data-stu-id="cec0c-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="cec0c-126">Para os escenarios entre empresas, pode definir a política que se avaliará coa entidade de destino (entidade prestameira).</span><span class="sxs-lookup"><span data-stu-id="cec0c-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="cec0c-127">Para executar as políticas contra a entidade de destino, active a funcionalidade **Avaliar a política de gastos fronte á persoa xurídica prestameira** na área de traballo **Xestión de funcionalidades**.</span><span class="sxs-lookup"><span data-stu-id="cec0c-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="cec0c-128">Cando avaliar as políticas</span><span class="sxs-lookup"><span data-stu-id="cec0c-128">When to evaluate policies</span></span>

<span data-ttu-id="cec0c-129">Nos parámetros de xestión de gastos, pode seleccionar avaliar as políticas de xestión de gastos cando se garda unha liña ou cando se envía un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="cec0c-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="cec0c-130">Se elixe avaliar cando se garda unha liña, os usuarios terán unha visibilidade previa do que deben facer para completar o seu informe de gastos á vez.</span><span class="sxs-lookup"><span data-stu-id="cec0c-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="cec0c-131">Se non o fai, pode atrasar a avaliación da política e aforrar tempo validándoa ao final, durante o envío ao fluxo de traballo.</span><span class="sxs-lookup"><span data-stu-id="cec0c-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
