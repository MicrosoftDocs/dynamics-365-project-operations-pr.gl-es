---
title: Fluxo de traballo de xestión de gastos
description: Este tema explica como pode usar o sistema de fluxo de traballo en Microsoft Dynamics 365 Finance, para configurar un proceso de revisión dos informes de gastos na xestión de gastos.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271666"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="07030-103">Fluxo de traballo de xestión de gastos</span><span class="sxs-lookup"><span data-stu-id="07030-103">Expense management workflow</span></span>

<span data-ttu-id="07030-104">Pode usar o sistema de fluxo de traballo para configurar un proceso de revisión dos informes de gastos na xestión de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="07030-105">Pode configurar un fluxo de traballo que use os seguintes criterios para determinar quen aproba os informes de gastos:</span><span class="sxs-lookup"><span data-stu-id="07030-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="07030-106">A xerarquía de informes dos empregados e os límites de aprobación predefinidos</span><span class="sxs-lookup"><span data-stu-id="07030-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="07030-107">Aprobación multinivel que admite responsables de aprobacións intermedios e un responsable de aprobacións final</span><span class="sxs-lookup"><span data-stu-id="07030-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="07030-108">Dimensións financeiras e responsabilidade do proxecto</span><span class="sxs-lookup"><span data-stu-id="07030-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="07030-109">Atribución a usuarios ou grupos de usuarios específicos</span><span class="sxs-lookup"><span data-stu-id="07030-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="07030-110">Pódense crear aprobacións de fluxo de traballo para informes de gastos, solicitudes de viaxes, adiantos de efectivo e recuperación do imposto sobre o valor engadido (IVE).</span><span class="sxs-lookup"><span data-stu-id="07030-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="07030-111">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="07030-111">**Example**</span></span>

<span data-ttu-id="07030-112">O seguinte proceso é un exemplo do fluxo de traballo de xestión de gastos para un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="07030-113">Un empregado crea e garda un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="07030-114">O empregado envía o informe de gastos para a súa aprobación.</span><span class="sxs-lookup"><span data-stu-id="07030-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="07030-115">O responsable de aprobacións identifícase en función das regras que se definiron cando se configurou o fluxo de traballo.</span><span class="sxs-lookup"><span data-stu-id="07030-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="07030-116">O responsable de aprobacións recibe unha notificación de que un informe de gastos está listo para a súa aprobación.</span><span class="sxs-lookup"><span data-stu-id="07030-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="07030-117">O responsable de aprobacións revisa o informe de gastos e verifica que se cumpren as seguintes condicións:</span><span class="sxs-lookup"><span data-stu-id="07030-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="07030-118">Os gastos non infrinxen ningunha política de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="07030-119">Se un gasto infrinxe unha política, o responsable de aprobacións verifica que o informe de gastos inclúe unha xustificación comercial válida.</span><span class="sxs-lookup"><span data-stu-id="07030-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="07030-120">Os xustificantes electrónicos anéxanse ao informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="07030-121">O responsable de aprobacións aproba o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="07030-122">O informe de gastos atribúese ao coordinador de contas pendentes de pago para a súa contabilización.</span><span class="sxs-lookup"><span data-stu-id="07030-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="07030-123">Prodúcese un dos seguintes pasos, dependendo de se está configurada a contabilización automática:</span><span class="sxs-lookup"><span data-stu-id="07030-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="07030-124">Se se configura a contabilización automática, o informe de gastos procesarase para o pagamento e actualizarase o estado do informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="07030-125">Se a contabilización automática non está configurada, o coordinador de contas pendentes de pago verifica que se enviaron todos os recibos orixinais e que os recibos están aliñados cos gastos do informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="07030-126">Todos os códigos fiscais que se introducen no informe de gastos tamén deben verificarse como correctos.</span><span class="sxs-lookup"><span data-stu-id="07030-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="07030-127">Despois de verificar estes requisitos, contabilízase o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="07030-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="07030-128">Despois de publicar o informe de gastos, autorízase o pagamento do informe de gastos e reembolsaráselle ao empregado.</span><span class="sxs-lookup"><span data-stu-id="07030-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]