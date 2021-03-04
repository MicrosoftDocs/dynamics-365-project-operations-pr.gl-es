---
title: Recuperar entradas de tempo ou gasto aprobadas previamente
description: Este tema fornece información sobre como recuperar unha transacción de tempo e gasto de proxecto aprobada previamente.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147832"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="091c0-103">Recuperar entradas de tempo ou gasto aprobadas previamente</span><span class="sxs-lookup"><span data-stu-id="091c0-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="091c0-104">Un membro do equipo do proxecto ou outra persoa que envíe unha entrada de tempo ou gasto pode lembrar esa entrada de tempo ou gasto despois de que foi aprobada.</span><span class="sxs-lookup"><span data-stu-id="091c0-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="091c0-105">O proceso para recuperar unha entrada de tempo ou gasto aprobada ten dous pasos:</span><span class="sxs-lookup"><span data-stu-id="091c0-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="091c0-106">Un solicitante solicita unha recuperación.</span><span class="sxs-lookup"><span data-stu-id="091c0-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="091c0-107">Un responsable de aprobación aproba a recuperación.</span><span class="sxs-lookup"><span data-stu-id="091c0-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="091c0-108">Solicitar unha recuperación</span><span class="sxs-lookup"><span data-stu-id="091c0-108">Request a recall</span></span>

<span data-ttu-id="091c0-109">Siga estes pasos para solicitar unha recuperación dunha entrada de tempo ou gasto que aprobada.</span><span class="sxs-lookup"><span data-stu-id="091c0-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="091c0-110">Para as entradas de tempo, vaia a **Proxectos** \> **O meu traballo** \> **Entrada de tempo**.</span><span class="sxs-lookup"><span data-stu-id="091c0-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="091c0-111">–ou–</span><span class="sxs-lookup"><span data-stu-id="091c0-111">–or–</span></span>

    <span data-ttu-id="091c0-112">Para as entradas de gasto, vaia a **Proxectos** \> **O meu traballo** \> **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="091c0-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="091c0-113">Para as entradas de tempo, seleccione todas as entradas de tempo para unha combinación específica dun proxecto e unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="091c0-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="091c0-114">Alternativamente, na grade, seleccione as celas individuais para tempo nunha data concreta para un proxecto específico.</span><span class="sxs-lookup"><span data-stu-id="091c0-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="091c0-115">–ou–</span><span class="sxs-lookup"><span data-stu-id="091c0-115">–or–</span></span>

    <span data-ttu-id="091c0-116">Para as entradas de gasto, seleccione a fila da entrada de gasto para recuperar.</span><span class="sxs-lookup"><span data-stu-id="091c0-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="091c0-117">Seleccione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="091c0-117">Select **Recall**.</span></span> <span data-ttu-id="091c0-118">Aparecerá unha caixa de diálogo de confirmación.</span><span class="sxs-lookup"><span data-stu-id="091c0-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="091c0-119">Se as entradas de tempo e gasto seleccionadas xa foron aprobadas, solicitaráselle que introduza un motivo para a recuperación.</span><span class="sxs-lookup"><span data-stu-id="091c0-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="091c0-120">Insira un motivo para a recuperación e seleccione **Aceptar** para confirmar a operación.</span><span class="sxs-lookup"><span data-stu-id="091c0-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="091c0-121">O sistema envía á persoa que aprobou as entradas unha solicitude para aprobar a recuperación.</span><span class="sxs-lookup"><span data-stu-id="091c0-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="091c0-122">Aínda que se poden recuperar as entradas de tempo e gasto aprobadas, se xa se facturou ao cliente un tempo ou gasto aprobado, non se pode crear unha solicitude de recuperación.</span><span class="sxs-lookup"><span data-stu-id="091c0-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="091c0-123">Un usuario que intente crear unha solicitude de recuperación recibirá unha mensaxe que afirma que non se pode recuperar o tempo nin o gasto porque xa foi facturado.</span><span class="sxs-lookup"><span data-stu-id="091c0-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="091c0-124">Aprobar ou rexeitar unha solicitude de recuperación</span><span class="sxs-lookup"><span data-stu-id="091c0-124">Approve or reject a recall request</span></span>

<span data-ttu-id="091c0-125">Siga estes pasos para aprobar ou rexeitar unha solicitude de recuperación.</span><span class="sxs-lookup"><span data-stu-id="091c0-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="091c0-126">Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.</span><span class="sxs-lookup"><span data-stu-id="091c0-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="091c0-127">Na páxina de lista **Aprobacións**, cambie a vista a **Solicitudes de recuperación para aprobación**.</span><span class="sxs-lookup"><span data-stu-id="091c0-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="091c0-128">Móstrase unha lista de solicitudes de recuperación enviadas.</span><span class="sxs-lookup"><span data-stu-id="091c0-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="091c0-129">Seleccione unha ou máis entradas e logo seleccione **Aprobar** ou **Rexeitar**.</span><span class="sxs-lookup"><span data-stu-id="091c0-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="091c0-130">Se seleccionou **Aprobar**, recibirá unha mensaxe de aviso que explica o impacto da aprobación.</span><span class="sxs-lookup"><span data-stu-id="091c0-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="091c0-131">Seleccione **Aceptar** para confirmar a operación.</span><span class="sxs-lookup"><span data-stu-id="091c0-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="091c0-132">Apróbase a solicitude de recuperación.</span><span class="sxs-lookup"><span data-stu-id="091c0-132">The recall request is approved.</span></span>

    <span data-ttu-id="091c0-133">–ou–</span><span class="sxs-lookup"><span data-stu-id="091c0-133">–or–</span></span>

    <span data-ttu-id="091c0-134">Se seleccionou **Rexeitar**, a solicitude de recuperación é rexeitada.</span><span class="sxs-lookup"><span data-stu-id="091c0-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="091c0-135">Como cando se solicita unha recuperación, cando se aproba unha recuperación, o sistema verifica calquera actividade de facturación nas entradas de tempo ou gasto.</span><span class="sxs-lookup"><span data-stu-id="091c0-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="091c0-136">Se unha entrada xa foi facturada ou se está nun borrador de factura, o responsable de aprobacións recibirá unha mensaxe de erro que afirma que o tempo ou gasto non se poden aprobar para a súa recuperación porque xa foi facturado.</span><span class="sxs-lookup"><span data-stu-id="091c0-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="091c0-137">Impacto dunha solicitude de recuperación</span><span class="sxs-lookup"><span data-stu-id="091c0-137">Impact of a recall request</span></span>

<span data-ttu-id="091c0-138">Cando se recupera unha aprobación, hai un impacto operativo e financeiro.</span><span class="sxs-lookup"><span data-stu-id="091c0-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="091c0-139">Impacto operativo</span><span class="sxs-lookup"><span data-stu-id="091c0-139">Operational impact</span></span>

<span data-ttu-id="091c0-140">Se se aproba unha solicitude de recuperación, o rexistro de aprobación está marcado como **Rexeitado**.</span><span class="sxs-lookup"><span data-stu-id="091c0-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="091c0-141">O estado da entrada cambia a **Devolto** ou **Rexeitado**, segundo sexa unha entrada de tempo ou unha entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="091c0-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="091c0-142">O membro do equipo do proxecto pode ver as entradas, editar e volver enviar as entradas ou borrar por completo as entradas.</span><span class="sxs-lookup"><span data-stu-id="091c0-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="091c0-143">Se se rexeita unha solicitude de recuperación, o estado da entrada permanece en **Aprobado** e a entrada non pode ser editada polo membro do equipo do proxecto nin polo responsable de aprobacións do proxecto.</span><span class="sxs-lookup"><span data-stu-id="091c0-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="091c0-144">Impacto financeiro</span><span class="sxs-lookup"><span data-stu-id="091c0-144">Financial impact</span></span>

<span data-ttu-id="091c0-145">Se unha solicitude de recuperación é aprobada, os datos reais correspondentes de custo e vendas actualízanse do seguinte xeito:</span><span class="sxs-lookup"><span data-stu-id="091c0-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="091c0-146">O campo **Estado de axuste** actualízase a **Axustado**.</span><span class="sxs-lookup"><span data-stu-id="091c0-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="091c0-147">O campo **Estado de facturación** actualízase a **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="091c0-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="091c0-148">A continuación, créanse entradas de reversión na táboa de Datos reais.</span><span class="sxs-lookup"><span data-stu-id="091c0-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="091c0-149">Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais.</span><span class="sxs-lookup"><span data-stu-id="091c0-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="091c0-150">Os únicos valores que non se copian son os valores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="091c0-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="091c0-151">Estes valores revértense.</span><span class="sxs-lookup"><span data-stu-id="091c0-151">These values are reversed instead.</span></span> <span data-ttu-id="091c0-152">Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**.</span><span class="sxs-lookup"><span data-stu-id="091c0-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="091c0-153">O campo **Estado de axuste** nos datos reais invertidos establecese en **Inaxustable**, e o campo **Estado de facturación** establécese en **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="091c0-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="091c0-154">Debido a estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto xa non contabilizarán as cantidades que representan estes datos reais.</span><span class="sxs-lookup"><span data-stu-id="091c0-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="091c0-155">Se se rexeita a solicitude de recuperación, non hai impacto financeiro no proxecto.</span><span class="sxs-lookup"><span data-stu-id="091c0-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="091c0-156">Cambios nos rexistros de entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="091c0-156">Changes to time entry records</span></span>

<span data-ttu-id="091c0-157">A seguinte ilustración mostra os cambios que se producen para as entradas de tempo aprobadas cando se recuperan.</span><span class="sxs-lookup"><span data-stu-id="091c0-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Transicións de estado de entradas de tempo](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="091c0-159">Cambios nos rexistros de entrada de gasto</span><span class="sxs-lookup"><span data-stu-id="091c0-159">Changes to expense entry records</span></span>

<span data-ttu-id="091c0-160">A seguinte ilustración mostra os cambios que se producen para as entradas de gasto aprobadas cando se recuperan.</span><span class="sxs-lookup"><span data-stu-id="091c0-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Transicións de estado de entradas de gasto](media/ExpenseEntryStateTransitions.png)
