---
title: Configurar fluxos de traballo de xestión de gastos
description: Pode configurar un proceso de fluxo de traballo para revisar e aprobar documentos de viaxes e gastos.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005114"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="90f65-103">Configurar fluxos de traballo de xestión de gastos</span><span class="sxs-lookup"><span data-stu-id="90f65-103">Set up Expense management workflows</span></span>

<span data-ttu-id="90f65-104">Pode configurar un proceso de fluxo de traballo que se empregue para revisar e aprobar documentos de viaxes e gastos.</span><span class="sxs-lookup"><span data-stu-id="90f65-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="90f65-105">Os documentos para os que se poden definir fluxos de traballo inclúen informes de gastos, solicitudes de viaxes e solicitudes de adianto de efectivo.</span><span class="sxs-lookup"><span data-stu-id="90f65-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="90f65-106">Un fluxo de traballo representa un proceso de negocio.</span><span class="sxs-lookup"><span data-stu-id="90f65-106">A workflow represents a business process.</span></span> <span data-ttu-id="90f65-107">Define como un documento flúe a través do sistema e indica quen debe completar unha tarefa ou aproba un documento.</span><span class="sxs-lookup"><span data-stu-id="90f65-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="90f65-108">Hai varios beneficios de usar o sistema de fluxo de traballo na súa organización:</span><span class="sxs-lookup"><span data-stu-id="90f65-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="90f65-109">**Procesos uniformes**: Pode definir o proceso de aprobación de documentos específicos, como solicitudes de compra e informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="90f65-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="90f65-110">O uso do sistema de fluxo de traballo axuda a garantir que os documentos se procesan e aproban de xeito uniforme e eficiente.</span><span class="sxs-lookup"><span data-stu-id="90f65-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="90f65-111">Visibilidade do proceso: Pode rastrexar o estado, o historial e os indicadores de rendemento dunha instancia de fluxo de traballo específica.</span><span class="sxs-lookup"><span data-stu-id="90f65-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="90f65-112">Isto axúdalle a determinar se se deben facer cambios no fluxo de traballo para mellorar a eficiencia.</span><span class="sxs-lookup"><span data-stu-id="90f65-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="90f65-113">Lista de traballo centralizada: Os usuarios poden ver unha lista de traballo centralizada para ver as tarefas e aprobacións do fluxo de traballo que se lles atribuíron.</span><span class="sxs-lookup"><span data-stu-id="90f65-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="90f65-114">**Os tipos de fluxos de traballo que pode crear**</span><span class="sxs-lookup"><span data-stu-id="90f65-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="90f65-115">A seguinte táboa mostra os tipos de fluxos de traballo que pode crear **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="90f65-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="90f65-116"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="90f65-117"><strong>Use este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="90f65-118"><strong>Informe de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="90f65-119">Cree fluxos de traballo de aprobación para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="90f65-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="90f65-120"><strong>Publicación automática de informes de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="90f65-121">Cree fluxos de traballo de publicación automática para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="90f65-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="90f65-122"><strong>Elemento de liña de gasto</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="90f65-123">Cree fluxos de traballo de aprobación para elementos de liña en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="90f65-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="90f65-124"><strong>Publicación automática de elemento de liña de gasto</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="90f65-125">Cree fluxos de traballo de publicación automática para elementos de liña en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="90f65-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="90f65-126"><strong>Requirimento de viaxe</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="90f65-127">Cree fluxos de traballo de aprobación para solicitudes de viaxes.</span><span class="sxs-lookup"><span data-stu-id="90f65-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="90f65-128"><strong>Solicitude de adianto de efectivo</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="90f65-129">Cree fluxos de traballo de aprobación para solicitudes de adianto de efectivo.</span><span class="sxs-lookup"><span data-stu-id="90f65-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="90f65-130"><strong>Recuperación do IVE</strong></span><span class="sxs-lookup"><span data-stu-id="90f65-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="90f65-131">Cree fluxos de traballo de aprobación para a recuperación do imposto sobre o valor engadido (IVE).</span><span class="sxs-lookup"><span data-stu-id="90f65-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]