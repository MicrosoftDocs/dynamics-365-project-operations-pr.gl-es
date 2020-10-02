---
title: Configurar fluxos de traballo para a xestión de gastos
description: Pode configurar un proceso de fluxo de traballo que se empregue para revisar e aprobar documentos de viaxes e gastos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896549"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="3af4e-103">Configurar fluxos de traballo para a xestión de gastos</span><span class="sxs-lookup"><span data-stu-id="3af4e-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="3af4e-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="3af4e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3af4e-105">Pode configurar un proceso de fluxo de traballo para revisar e aprobar documentos de viaxes e gastos.</span><span class="sxs-lookup"><span data-stu-id="3af4e-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="3af4e-106">Pode definir fluxos de traballo para informes de gastos, solicitudes de viaxes e solicitudes de adianto de efectivo.</span><span class="sxs-lookup"><span data-stu-id="3af4e-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="3af4e-107">Un fluxo de traballo representa un proceso de negocio e define como un documento flúe a través do sistema.</span><span class="sxs-lookup"><span data-stu-id="3af4e-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="3af4e-108">O fluxo de traballo tamén indica quen debe completar unha tarefa ou aprobar un documento.</span><span class="sxs-lookup"><span data-stu-id="3af4e-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="3af4e-109">Hai varios beneficios de usar o sistema de fluxo de traballo na súa organización:</span><span class="sxs-lookup"><span data-stu-id="3af4e-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="3af4e-110">**Procesos uniformes**: Pode definir o proceso de aprobación de documentos específicos, como solicitudes de compra e informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="3af4e-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="3af4e-111">O uso do sistema de fluxo de traballo axuda a garantir que os documentos se procesan e aproban de xeito uniforme e eficiente.</span><span class="sxs-lookup"><span data-stu-id="3af4e-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="3af4e-112">**Visibilidade do proceso**: Pode rastrexar o estado, o historial e os indicadores de rendemento dunha instancia de fluxo de traballo específica.</span><span class="sxs-lookup"><span data-stu-id="3af4e-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="3af4e-113">Isto axúdalle a determinar se se deben facer cambios no fluxo de traballo para mellorar a eficiencia.</span><span class="sxs-lookup"><span data-stu-id="3af4e-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="3af4e-114">**Lista de traballo centralizada**: Os usuarios poden ver unha lista de traballo centralizada para ver as tarefas e aprobacións do fluxo de traballo que se lles atribuíron.</span><span class="sxs-lookup"><span data-stu-id="3af4e-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="3af4e-115">Tipos de fluxo de traballo</span><span class="sxs-lookup"><span data-stu-id="3af4e-115">Workflow types</span></span>

<span data-ttu-id="3af4e-116">A seguinte táboa mostra os tipos de fluxos de traballo que pode crear **Xestión de gastos**.</span><span class="sxs-lookup"><span data-stu-id="3af4e-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="3af4e-117"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="3af4e-118"><strong>Use este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="3af4e-119"><strong>Aprobación automática de informes de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="3af4e-120">Cree fluxos de traballo de aprobación para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="3af4e-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="3af4e-121"><strong>Publicación automática de informes de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="3af4e-122">Cree fluxos de traballo de publicación automática para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="3af4e-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="3af4e-123"><strong>Elemento de liña de gasto</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="3af4e-124">Cree fluxos de traballo de aprobación para elementos de liña en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="3af4e-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="3af4e-125"><strong>Publicación automática de elemento de liña de gasto</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="3af4e-126">Cree fluxos de traballo de publicación automática para elementos de liña en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="3af4e-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="3af4e-127"><strong>Requirimento de viaxe</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="3af4e-128">Cree fluxos de traballo de aprobación para solicitudes de viaxes.</span><span class="sxs-lookup"><span data-stu-id="3af4e-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="3af4e-129"><strong>Solicitude de adianto de efectivo</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="3af4e-130">Cree fluxos de traballo de aprobación para solicitudes de adianto de efectivo.</span><span class="sxs-lookup"><span data-stu-id="3af4e-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="3af4e-131"><strong>Recuperación do IVE</strong></span><span class="sxs-lookup"><span data-stu-id="3af4e-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="3af4e-132">Cree fluxos de traballo de aprobación para a recuperación do imposto sobre o valor engadido (IVE).</span><span class="sxs-lookup"><span data-stu-id="3af4e-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
