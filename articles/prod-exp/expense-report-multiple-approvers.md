---
title: Varios responsables de aprobación nun informe de gastos
description: Este tema ofrece información sobre os informes de gastos que requiren a aprobación de varias persoas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271711"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="39a92-103">Varios responsables de aprobación nun informe de gastos</span><span class="sxs-lookup"><span data-stu-id="39a92-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="39a92-104">Dependendo das políticas de aprobación de gastos da súa organización, é posible que máis dunha persoa teña que aprobar un informe de gastos que enviou un empregado.</span><span class="sxs-lookup"><span data-stu-id="39a92-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="39a92-105">Cando configura o proceso de fluxo de traballo para a aprobación do informe de gastos, pode engadir elementos do fluxo de traballo que inclúan tarefas ou pasos para un ou máis responsables de aprobación de informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="39a92-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="39a92-106">Por exemplo, pode requirir que todos os informes de gastos sexan aprobados primeiro polo superior do empregado que o presentou e logo polo coordinador de contas pendentes de pago.</span><span class="sxs-lookup"><span data-stu-id="39a92-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="39a92-107">Se decide requirir varios responsables de aprobación de informes de gastos, pode engadir os elementos do fluxo de traballo dalgún dos seguintes xeitos:</span><span class="sxs-lookup"><span data-stu-id="39a92-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="39a92-108">Engada un elemento de aprobación que teña un paso.</span><span class="sxs-lookup"><span data-stu-id="39a92-108">Add one approval element that has one step.</span></span> <span data-ttu-id="39a92-109">Por exemplo, o paso pode requirir que se atribúa un informe de gastos a un grupo de usuarios e que o aprobe o 50 por cento dos membros do grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="39a92-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="39a92-110">Engada un elemento de aprobación que teña varios pasos.</span><span class="sxs-lookup"><span data-stu-id="39a92-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="39a92-111">Por exemplo, o elemento de aprobación pode ter os seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="39a92-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="39a92-112">O superior do empregado que presentou o informe de gastos apróbao.</span><span class="sxs-lookup"><span data-stu-id="39a92-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="39a92-113">O empregado de contas pendentes de pago verifica os recibos e os elementos do informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="39a92-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="39a92-114">O responsable do orzamento aproba o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="39a92-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="39a92-115">Engada varios elementos de aprobación, cada un deles cun paso.</span><span class="sxs-lookup"><span data-stu-id="39a92-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="39a92-116">Por exemplo, pode engadir un elemento de aprobación separado para cada un dos seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="39a92-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="39a92-117">O superior do empregado aproba o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="39a92-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="39a92-118">O responsable do orzamento aproba o informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="39a92-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]