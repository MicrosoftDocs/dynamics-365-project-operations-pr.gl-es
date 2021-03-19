---
title: Entrada de gasto (lite)
description: Este tema ofrece información sobre como traballar coa entrada de gastos nun despregamento lite.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276751"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="80763-103">Entrada de gasto (lite)</span><span class="sxs-lookup"><span data-stu-id="80763-103">Expense entry (lite)</span></span>

<span data-ttu-id="80763-104">_**Aplícase a:** Despregamento de Lite - acordo para facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="80763-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="80763-105">A xestión básica ou lite de gastos é a capacidade de rexistrar gastos simples.</span><span class="sxs-lookup"><span data-stu-id="80763-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="80763-106">Pode rexistrar os gastos contra un proxecto e logo o responsable de aprobacións do proxecto revisaraos e aprobaraos.</span><span class="sxs-lookup"><span data-stu-id="80763-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="80763-107">Para obter máis información sobre as capacidades de gasto en Dynamics 365 Project Operations, consulte [Visión xeral dos gastos](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="80763-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="80763-108">Capta un gasto básico</span><span class="sxs-lookup"><span data-stu-id="80763-108">Capture a basic expense</span></span>

<span data-ttu-id="80763-109">Pode capturar os seus gastos para poder envialos ao responsables de aprobacións.</span><span class="sxs-lookup"><span data-stu-id="80763-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="80763-110">Vaia a **Gastos** e seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="80763-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="80763-111">Na páxina **Novo gasto**, introduza a información do gasto requirida e seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="80763-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="80763-112">Enviar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="80763-112">Submit a basic expense</span></span>

<span data-ttu-id="80763-113">Despois de rematar de capturar todos os seus gastos e cando estea listo para facer que os aproben, debe envialos.</span><span class="sxs-lookup"><span data-stu-id="80763-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="80763-114">Vaia a **Gastos** e seleccione un gasto.</span><span class="sxs-lookup"><span data-stu-id="80763-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="80763-115">Ou seleccione todos os gastos empregando a caixa de verificación da cabeceira.</span><span class="sxs-lookup"><span data-stu-id="80763-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="80763-116">Seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="80763-116">Select **Submit**.</span></span> <span data-ttu-id="80763-117">O sistema procesa as entradas seleccionadas e logo crea solicitudes de aprobación de gastos.</span><span class="sxs-lookup"><span data-stu-id="80763-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="80763-118">Engadir un anexo</span><span class="sxs-lookup"><span data-stu-id="80763-118">Add an attachment</span></span>

<span data-ttu-id="80763-119">É posible que deba proporcionar ao responsable de aprobación documentación adicional sobre o seu gasto.</span><span class="sxs-lookup"><span data-stu-id="80763-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="80763-120">Pode anexar un recibo na liña de tempo da entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="80763-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="80763-121">Seleccione **Editar** e na sección **Liña de tempo** seleccione a icona de clip para anexar o recibo.</span><span class="sxs-lookup"><span data-stu-id="80763-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="80763-122">Recuperar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="80763-122">Recall a basic expense</span></span>

<span data-ttu-id="80763-123">Cando envíe un gasto por erro, pode recuperalo.</span><span class="sxs-lookup"><span data-stu-id="80763-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="80763-124">O tempo necesario para recuperar unha entrada de gasto depende da súa fase de aprobación.</span><span class="sxs-lookup"><span data-stu-id="80763-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="80763-125">Se o responsable de aprobacións aínda non aprobou a entrada, a recuperación pode producirse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="80763-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="80763-126">Non obstante, se a entrada xa foi aprobada, solicítaselle ao responsable de aprobacións que aprobe a recuperación e reverta as transaccións.</span><span class="sxs-lookup"><span data-stu-id="80763-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="80763-127">Vaia a **Gastos** e, a seguir, na lista de gastos, seleccione o gasto que desexa recuperar.</span><span class="sxs-lookup"><span data-stu-id="80763-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="80763-128">Seleccione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="80763-128">Select **Recall**.</span></span> <span data-ttu-id="80763-129">Se aínda non se aprobou a entrada de gasto, o sistema o recupera inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="80763-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="80763-130">Se a entrada de gasto xa se aprobou, créase unha solicitude de recuperación para notificar ao responsable de aprobacións de que desexa reverter o gasto.</span><span class="sxs-lookup"><span data-stu-id="80763-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="80763-131">A seguir, o responsable de aprobacións confirmará que se pode facer a reversión e devolverase a entrada.</span><span class="sxs-lookup"><span data-stu-id="80763-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="80763-132">Eliminar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="80763-132">Delete a basic expense</span></span>

<span data-ttu-id="80763-133">Pódense eliminar os gastos que aínda non se enviaron.</span><span class="sxs-lookup"><span data-stu-id="80763-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="80763-134">Para eliminar un gasto xa enviado, primeiro debe recuperalo.</span><span class="sxs-lookup"><span data-stu-id="80763-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="80763-135">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="80763-135">See also</span></span>

- [<span data-ttu-id="80763-136">Visión xeral das aprobacións</span><span class="sxs-lookup"><span data-stu-id="80763-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]