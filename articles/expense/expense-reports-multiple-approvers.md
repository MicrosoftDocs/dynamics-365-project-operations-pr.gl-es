---
title: Informes de gastos e múltiples responsables de aprobación
description: Este tema ofrece información sobre os informes de gastos que requiren a aprobación de máis dunha persoa.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276526"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="87295-103">Informes de gastos e múltiples responsables de aprobación</span><span class="sxs-lookup"><span data-stu-id="87295-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="87295-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="87295-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="87295-105">Dependendo das políticas de aprobación de gastos da súa organización, é posible que máis dunha persoa teña que aprobar un informe de gastos enviado.</span><span class="sxs-lookup"><span data-stu-id="87295-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="87295-106">Cando configura o proceso de fluxo de traballo para a aprobación do informe de gastos, pode engadir elementos do fluxo de traballo que inclúan tarefas ou pasos para un ou máis responsables de aprobación de informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="87295-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="87295-107">Por exemplo, pode requirir que todos os informes de gastos sexan aprobados por dúas persoas distintas, o superior do empregado que o presentou e o coordinador de contas pendentes de pago.</span><span class="sxs-lookup"><span data-stu-id="87295-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="87295-108">Se decide requirir varios responsables de aprobación de informes de gastos, pode engadir os elementos do fluxo de traballo dalgún dos seguintes xeitos:</span><span class="sxs-lookup"><span data-stu-id="87295-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="87295-109">Engada un elemento de aprobación que teña un paso.</span><span class="sxs-lookup"><span data-stu-id="87295-109">Add one approval element that has one step.</span></span> <span data-ttu-id="87295-110">Por exemplo, o paso pode requirir que se atribúa un informe de gastos a un grupo de usuarios e que o aprobe o 50 por cento dos membros do grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="87295-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="87295-111">Engada un elemento de aprobación que teña varios pasos.</span><span class="sxs-lookup"><span data-stu-id="87295-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="87295-112">Por exemplo, o elemento de aprobación pode ter os seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="87295-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="87295-113">O superior do empregado que presentou o informe de gastos apróbao.</span><span class="sxs-lookup"><span data-stu-id="87295-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="87295-114">O empregado de contas pendentes de pago verifica os recibos e os elementos do informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="87295-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="87295-115">O responsable do orzamento aproba o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="87295-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="87295-116">Engada varios elementos de aprobación, cada un deles cun paso.</span><span class="sxs-lookup"><span data-stu-id="87295-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="87295-117">Por exemplo, pode engadir un elemento de aprobación separado para cada un dos seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="87295-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="87295-118">O superior do empregado aproba o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="87295-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="87295-119">O responsable do orzamento aproba o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="87295-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]