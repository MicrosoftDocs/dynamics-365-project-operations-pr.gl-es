---
title: Entrada de gasto (lite)
description: Este tema ofrece información sobre como traballar coa entrada de gastos nun despregamento lite.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121081"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="40531-103">Entrada de gasto (lite)</span><span class="sxs-lookup"><span data-stu-id="40531-103">Expense entry (lite)</span></span>

<span data-ttu-id="40531-104">_**Aplícase a:** Despregamento de Lite - acordo para facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="40531-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="40531-105">A xestión básica ou lite de gastos é a capacidade de rexistrar gastos simples.</span><span class="sxs-lookup"><span data-stu-id="40531-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="40531-106">Pode rexistrar os gastos contra un proxecto e logo o responsable de aprobacións do proxecto revisaraos e aprobaraos.</span><span class="sxs-lookup"><span data-stu-id="40531-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="40531-107">Para obter máis información sobre as capacidades de gasto en Dynamics 365 Project Operations, consulte [Visión xeral dos gastos](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="40531-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="40531-108">Capta un gasto básico</span><span class="sxs-lookup"><span data-stu-id="40531-108">Capture a basic expense</span></span>

<span data-ttu-id="40531-109">Pode capturar os seus gastos para poder envialos ao responsables de aprobacións.</span><span class="sxs-lookup"><span data-stu-id="40531-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="40531-110">Vaia a **Gastos** e seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="40531-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="40531-111">Na páxina **Novo gasto**, introduza a información do gasto requirida e seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="40531-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="40531-112">Enviar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="40531-112">Submit a basic expense</span></span>

<span data-ttu-id="40531-113">Despois de rematar de capturar todos os seus gastos e cando estea listo para facer que os aproben, debe envialos.</span><span class="sxs-lookup"><span data-stu-id="40531-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="40531-114">Vaia a **Gastos** e seleccione un gasto.</span><span class="sxs-lookup"><span data-stu-id="40531-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="40531-115">Ou seleccione todos os gastos empregando a caixa de verificación da cabeceira.</span><span class="sxs-lookup"><span data-stu-id="40531-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="40531-116">Seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="40531-116">Select **Submit**.</span></span> <span data-ttu-id="40531-117">O sistema procesa as entradas seleccionadas e logo crea solicitudes de aprobación de gastos.</span><span class="sxs-lookup"><span data-stu-id="40531-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="40531-118">Recuperar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="40531-118">Recall a basic expense</span></span>

<span data-ttu-id="40531-119">Cando envíe un gasto por erro, pode recuperalo.</span><span class="sxs-lookup"><span data-stu-id="40531-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="40531-120">O tempo necesario para recuperar unha entrada de gasto depende da súa fase de aprobación.</span><span class="sxs-lookup"><span data-stu-id="40531-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="40531-121">Se o responsable de aprobacións aínda non aprobou a entrada, a recuperación pode producirse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="40531-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="40531-122">Non obstante, se a entrada xa foi aprobada, solicítaselle ao responsable de aprobacións que aprobe a recuperación e reverta as transaccións.</span><span class="sxs-lookup"><span data-stu-id="40531-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="40531-123">Vaia a **Gastos** e, a seguir, na lista de gastos, seleccione o gasto que desexa recuperar.</span><span class="sxs-lookup"><span data-stu-id="40531-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="40531-124">Seleccione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="40531-124">Select **Recall**.</span></span> <span data-ttu-id="40531-125">Se aínda non se aprobou a entrada de gasto, o sistema o recupera inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="40531-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="40531-126">Se a entrada de gasto xa se aprobou, créase unha solicitude de recuperación para notificar ao responsable de aprobacións de que desexa reverter o gasto.</span><span class="sxs-lookup"><span data-stu-id="40531-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="40531-127">A seguir, o responsable de aprobacións confirmará que se pode facer a reversión e devolverase a entrada.</span><span class="sxs-lookup"><span data-stu-id="40531-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="40531-128">Eliminar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="40531-128">Delete a basic expense</span></span>

<span data-ttu-id="40531-129">Pódense eliminar os gastos que aínda non se enviaron.</span><span class="sxs-lookup"><span data-stu-id="40531-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="40531-130">Para eliminar un gasto xa enviado, primeiro debe recuperalo.</span><span class="sxs-lookup"><span data-stu-id="40531-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="40531-131">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="40531-131">See also</span></span>

- [<span data-ttu-id="40531-132">Visión xeral das aprobacións</span><span class="sxs-lookup"><span data-stu-id="40531-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
