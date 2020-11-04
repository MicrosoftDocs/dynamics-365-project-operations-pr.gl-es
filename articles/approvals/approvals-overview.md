---
title: Visión xeral das aprobacións
description: Este tema ofrece información sobre como traballar con aprobacións en Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075992"
---
# <a name="approvals-overview"></a><span data-ttu-id="903ed-103">Visión xeral das aprobacións</span><span class="sxs-lookup"><span data-stu-id="903ed-103">Approvals overview</span></span>

<span data-ttu-id="903ed-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="903ed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="903ed-105">Os envíos de tempo e gasto pasan por un fluxo de traballo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="903ed-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="903ed-106">Despois de que se aproben as entradas, as transaccións rexístranse en datos reais ou o tempo resérvase no programa.</span><span class="sxs-lookup"><span data-stu-id="903ed-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="903ed-107">Fluxo de traballo de aprobacións</span><span class="sxs-lookup"><span data-stu-id="903ed-107">Approvals workflow</span></span>
<span data-ttu-id="903ed-108">Cando crea e envía unha entrada de tempo ou gasto, créase unha entrada de aprobación.</span><span class="sxs-lookup"><span data-stu-id="903ed-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="903ed-109">O responsable de aprobación do proxecto ou o seu xestor revisa e aproba a súa entrada.</span><span class="sxs-lookup"><span data-stu-id="903ed-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="903ed-110">Se a entrada está relacionada cun proxecto, cando se aprobe, crearanse os datos reais.</span><span class="sxs-lookup"><span data-stu-id="903ed-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="903ed-111">Isto permite rastrexar o custo e a facturación.</span><span class="sxs-lookup"><span data-stu-id="903ed-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="903ed-112">Aprobar unha entrada</span><span class="sxs-lookup"><span data-stu-id="903ed-112">Approve an entry</span></span>
<span data-ttu-id="903ed-113">O formulario **Aprobacións** permítelle cambiar entre diferentes vistas para que poida ver os diferentes tipos de aprobacións.</span><span class="sxs-lookup"><span data-stu-id="903ed-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="903ed-114">Vaia ao formulario **Aprobacións** e seleccione **Gastos** , **Tempo** ou **Recuperacións**.</span><span class="sxs-lookup"><span data-stu-id="903ed-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="903ed-115">Revise cada aprobación e seleccione as que desexa aprobar.</span><span class="sxs-lookup"><span data-stu-id="903ed-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="903ed-116">Seleccione **Aprobar** para aprobar as entradas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="903ed-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="903ed-117">O sistema procesará estas entradas e creará datos reais ou unha reserva.</span><span class="sxs-lookup"><span data-stu-id="903ed-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="903ed-118">Rexeitar unha entrada</span><span class="sxs-lookup"><span data-stu-id="903ed-118">Reject an entry</span></span>
<span data-ttu-id="903ed-119">Como responsable de aprobación do proxecto, é posible que deba devolver unha entrada a un usuario para a súa corrección.</span><span class="sxs-lookup"><span data-stu-id="903ed-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="903ed-120">Vaia ao formulario **Aprobacións** e seleccione a entrada para rexeitar.</span><span class="sxs-lookup"><span data-stu-id="903ed-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="903ed-121">Seleccione **Rexeitar**.</span><span class="sxs-lookup"><span data-stu-id="903ed-121">Select **Reject**.</span></span>
3. <span data-ttu-id="903ed-122">Opcional - Engada un comentario no diálogo **Comentarios de rexeitamento** para informar ao usuario de por que se rexeita a entrada.</span><span class="sxs-lookup"><span data-stu-id="903ed-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="903ed-123">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="903ed-123">Select **OK**.</span></span> <span data-ttu-id="903ed-124">A entrada devolverase ao usuario.</span><span class="sxs-lookup"><span data-stu-id="903ed-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="903ed-125">Recuperar entradas</span><span class="sxs-lookup"><span data-stu-id="903ed-125">Recall entries</span></span>
<span data-ttu-id="903ed-126">Nalgún momento, é posible que teña que recuperar unha entrada enviada.</span><span class="sxs-lookup"><span data-stu-id="903ed-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="903ed-127">Se a entrada non foi aprobada, devolverase inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="903ed-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="903ed-128">Non obstante, unha entrada aprobada pode ter un impacto substancial.</span><span class="sxs-lookup"><span data-stu-id="903ed-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="903ed-129">O responsable de aprobacións do proxecto está obrigado a aprobar a recuperación para reverter a transacción en Datos reais.</span><span class="sxs-lookup"><span data-stu-id="903ed-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="903ed-130">Especificar responsables de aprobación de proxectos</span><span class="sxs-lookup"><span data-stu-id="903ed-130">Specify Project approvers</span></span>
<span data-ttu-id="903ed-131">Cada proxecto ten un número de membros do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="903ed-131">Each project has a number of project team members.</span></span> <span data-ttu-id="903ed-132">Pode especificar que membros do equipo tamén son responsables de aprobacións do proxecto.</span><span class="sxs-lookup"><span data-stu-id="903ed-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="903ed-133">Vaia ao formulario **Proxectos** e abra o proxecto desde a lista.</span><span class="sxs-lookup"><span data-stu-id="903ed-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="903ed-134">No separador **Equipo** , seleccione o membro do equipo que aprobará o proxecto e seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="903ed-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="903ed-135">Configure o campo **Responsable de aprobación do proxecto** en **Si**.</span><span class="sxs-lookup"><span data-stu-id="903ed-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="903ed-136">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="903ed-136">Select **Save**.</span></span>
5. <span data-ttu-id="903ed-137">Repita os pasos 2 a 4 para engadir responsables de aprobacións do proxecto adicionais.</span><span class="sxs-lookup"><span data-stu-id="903ed-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="903ed-138">Configurar o xestor do usuario</span><span class="sxs-lookup"><span data-stu-id="903ed-138">Configure the user's manager</span></span>

1. <span data-ttu-id="903ed-139">Vaia a **Configuración** > **Seguranza** > **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="903ed-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="903ed-140">Seleccione o usuario ao que está asignando un xestor e na área **Información da organización** seleccione o xestor da lista.</span><span class="sxs-lookup"><span data-stu-id="903ed-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="903ed-141">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="903ed-141">Select **Save**.</span></span>


