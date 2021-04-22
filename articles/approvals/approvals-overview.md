---
title: Visión xeral das aprobacións
description: Este tema ofrece información sobre como traballar con aprobacións en Project Operations.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852497"
---
# <a name="approvals-overview"></a><span data-ttu-id="16681-103">Visión xeral das aprobacións</span><span class="sxs-lookup"><span data-stu-id="16681-103">Approvals overview</span></span>

<span data-ttu-id="16681-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="16681-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="16681-105">Os envíos de tempo, gasto e uso de material móvense a través dun fluxo de traballo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="16681-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="16681-106">Despois de que se aproben as entradas, as transaccións rexístranse en datos reais ou o tempo resérvase no programa.</span><span class="sxs-lookup"><span data-stu-id="16681-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="16681-107">Fluxo de traballo de aprobacións</span><span class="sxs-lookup"><span data-stu-id="16681-107">Approvals workflow</span></span>
<span data-ttu-id="16681-108">Cando crea e envía unha entrada de tempo, gasto ou uso de material, créase un rexistro de aprobación.</span><span class="sxs-lookup"><span data-stu-id="16681-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="16681-109">O responsable de aprobación ou o xestor do proxecto revisa e aproba a entrada.</span><span class="sxs-lookup"><span data-stu-id="16681-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="16681-110">Se a entrada está relacionada cun proxecto, os datos reais crearanse cando se aprobe.</span><span class="sxs-lookup"><span data-stu-id="16681-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="16681-111">Isto permite rastrexar o custo e a facturación.</span><span class="sxs-lookup"><span data-stu-id="16681-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="16681-112">Aprobar unha entrada</span><span class="sxs-lookup"><span data-stu-id="16681-112">Approve an entry</span></span>
<span data-ttu-id="16681-113">A páxina **Aprobacións** permite cambiar entre diferentes vistas para que poida ver os diferentes tipos de aprobacións.</span><span class="sxs-lookup"><span data-stu-id="16681-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="16681-114">Vaia á páxina **Aprobacións** e seleccione **Gastos**, **Tempo**, **Uso de material** ou **Retiradas**.</span><span class="sxs-lookup"><span data-stu-id="16681-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="16681-115">Revise cada aprobación e seleccione as que desexa aprobar.</span><span class="sxs-lookup"><span data-stu-id="16681-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="16681-116">Seleccione **Aprobar** para aprobar as entradas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="16681-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="16681-117">O sistema procesa estas entradas e crea datos reais.</span><span class="sxs-lookup"><span data-stu-id="16681-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="16681-118">Rexeitar unha entrada</span><span class="sxs-lookup"><span data-stu-id="16681-118">Reject an entry</span></span>
<span data-ttu-id="16681-119">Como responsable de aprobación do proxecto, é posible que deba devolver unha entrada a un usuario para a súa corrección.</span><span class="sxs-lookup"><span data-stu-id="16681-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="16681-120">Vaia á páxina **Aprobacións** e seleccione a entrada para rexeitar.</span><span class="sxs-lookup"><span data-stu-id="16681-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="16681-121">Seleccione **Rexeitar**.</span><span class="sxs-lookup"><span data-stu-id="16681-121">Select **Reject**.</span></span>
3. <span data-ttu-id="16681-122">Opcionalmente, engada un comentario na caixa de diálogo **Comentarios de rexeitamento** para informar ao usuario por que se rexeita a entrada.</span><span class="sxs-lookup"><span data-stu-id="16681-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="16681-123">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="16681-123">Select **OK**.</span></span> <span data-ttu-id="16681-124">A entrada devolverase ao usuario.</span><span class="sxs-lookup"><span data-stu-id="16681-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="16681-125">Cancelar aprobación</span><span class="sxs-lookup"><span data-stu-id="16681-125">Cancel approval</span></span>
<span data-ttu-id="16681-126">Nalgúns casos, pode que teña que cancelar unha entrada previamente aprobada.</span><span class="sxs-lookup"><span data-stu-id="16681-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="16681-127">A cancelación dunha entrada previamente aprobada terá un impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="16681-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="16681-128">Aprobación de solicitudes de retirada</span><span class="sxs-lookup"><span data-stu-id="16681-128">Approving recall requests</span></span>
<span data-ttu-id="16681-129">Nalgúns casos, un consultor pode ter que retirar unha entrada previamente aprobada.</span><span class="sxs-lookup"><span data-stu-id="16681-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="16681-130">A cancelación dunha entrada previamente aprobada terá un impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="16681-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="16681-131">O responsable de aprobacións do proxecto está obrigado a aprobar a retirada para reverter a transacción en Datos reais.</span><span class="sxs-lookup"><span data-stu-id="16681-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="16681-132">Especificar responsables de aprobación de proxectos</span><span class="sxs-lookup"><span data-stu-id="16681-132">Specify Project approvers</span></span>
<span data-ttu-id="16681-133">Cada proxecto ten un número de membros do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="16681-133">Each project has a number of project team members.</span></span> <span data-ttu-id="16681-134">Pode especificar que membros do equipo tamén son responsables de aprobacións do proxecto.</span><span class="sxs-lookup"><span data-stu-id="16681-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="16681-135">Vaia á páxina **Proxectos** e abra o proxecto da lista.</span><span class="sxs-lookup"><span data-stu-id="16681-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="16681-136">No separador **Equipo**, seleccione o membro do equipo que aprobará o proxecto e seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="16681-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="16681-137">Configure o campo **Responsable de aprobación do proxecto** en **Si**.</span><span class="sxs-lookup"><span data-stu-id="16681-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="16681-138">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="16681-138">Select **Save**.</span></span>
5. <span data-ttu-id="16681-139">Repita os pasos 2 a 4 para engadir responsables de aprobacións do proxecto adicionais.</span><span class="sxs-lookup"><span data-stu-id="16681-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="16681-140">Configurar o xestor do usuario</span><span class="sxs-lookup"><span data-stu-id="16681-140">Configure the user's manager</span></span>

1. <span data-ttu-id="16681-141">Vaia a **Configuración** > **Seguranza** > **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="16681-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="16681-142">Seleccione o usuario ao que está asignando un xestor e na área **Información da organización** seleccione o xestor da lista.</span><span class="sxs-lookup"><span data-stu-id="16681-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="16681-143">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="16681-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
