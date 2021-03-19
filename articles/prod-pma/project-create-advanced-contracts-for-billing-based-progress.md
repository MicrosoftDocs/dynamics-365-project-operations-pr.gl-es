---
title: Crear contratos avanzados para a facturación baseada no progreso
description: Este tema explica como crear contratos de proxectos para que poida xerar facturas para os clientes, en función dunha porcentaxe do traballo rematado.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289502"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="59bb5-103">Crear contratos avanzados para a facturación baseada no progreso</span><span class="sxs-lookup"><span data-stu-id="59bb5-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="59bb5-104">Este tema explica como crear contratos de proxectos para que poida crear facturas para os clientes, en función dunha porcentaxe do traballo rematado.</span><span class="sxs-lookup"><span data-stu-id="59bb5-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="59bb5-105">Os importes da factura calcúlanse automaticamente para as categorías orzamentarias de traballo que configurou para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="59bb5-106">O prazo de facturación establécese cando negocia o contrato do proxecto co cliente.</span><span class="sxs-lookup"><span data-stu-id="59bb5-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="59bb5-107">Utilice os procedementos deste tema para configurar un contrato, un proxecto asociado e as regras de facturación que calculan os importes da factura para as categorías de traballo orzamentarias que configurou para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="59bb5-108">Despois de crear o contrato e o proxecto, pode configurar os detalles do proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="59bb5-109">Por exemplo, pode definir actividades e atribuír traballadores ao proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="59bb5-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="59bb5-110">Example</span></span>

<span data-ttu-id="59bb5-111">A súa organización é unha empresa de desenvolvemento de software.</span><span class="sxs-lookup"><span data-stu-id="59bb5-111">Your organization is a software development firm.</span></span> <span data-ttu-id="59bb5-112">Acepta desenvolver un paquete de contabilidade da nóminas para un cliente por unha taxa total de 20 000 dólares estadounidenses (USD).</span><span class="sxs-lookup"><span data-stu-id="59bb5-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="59bb5-113">A súa organización acepta facturar ao cliente a medida que completa porcentaxes específicas do proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="59bb5-114">Vostede configura as seguintes categorías de proxectos para o traballo para que poida usalas no proceso de facturación:</span><span class="sxs-lookup"><span data-stu-id="59bb5-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="59bb5-115">Consultoría</span><span class="sxs-lookup"><span data-stu-id="59bb5-115">Consulting</span></span>
- <span data-ttu-id="59bb5-116">Deseñar</span><span class="sxs-lookup"><span data-stu-id="59bb5-116">Design</span></span>
- <span data-ttu-id="59bb5-117">Instalación</span><span class="sxs-lookup"><span data-stu-id="59bb5-117">Installation</span></span>

<span data-ttu-id="59bb5-118">Vostede tamén configura regras de facturación que calculan automaticamente os importes da factura para a porcentaxe de traballo do proxecto que se completa para cada categoría.</span><span class="sxs-lookup"><span data-stu-id="59bb5-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="59bb5-119">O xestor do orzamento crea un orzamento para as categorías do proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="59bb5-120">A cantidade de traballo completado calcúlase automaticamente como unha porcentaxe do traballo real en comparación cos importes orzados.</span><span class="sxs-lookup"><span data-stu-id="59bb5-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59bb5-121">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59bb5-121">Prerequisites</span></span>

<span data-ttu-id="59bb5-122">Antes de crear un proxecto que use regras de facturación, debe configurar as secuencias numéricas para as regras de facturación e un diario de tarifas que se empregue para contabilizar as facturas de progreso.</span><span class="sxs-lookup"><span data-stu-id="59bb5-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="59bb5-123">Vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Parámetros de Xestión e contabilidade de proxectos**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="59bb5-124">Na páxina **Parámetros de Xestión e contabilidade de proxectos**, no separador **Secuencias numéricas**, configure a secuencia numérica que desexa empregar cando se crean as regras de facturación.</span><span class="sxs-lookup"><span data-stu-id="59bb5-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="59bb5-125">Vaia a **Xestión e contabilidade de proxectos** \> **Diarios** \> **Tarifa**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="59bb5-126">Na páxina **Diario de tarifas**, seleccione **Novo** e introduza o nome do diario.</span><span class="sxs-lookup"><span data-stu-id="59bb5-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="59bb5-127">Crear un contrato para a facturación de progreso</span><span class="sxs-lookup"><span data-stu-id="59bb5-127">Create a contract for progress billings</span></span>

<span data-ttu-id="59bb5-128">Utilice este procedemento para crear un contrato de proxecto para un proxecto de prezo fixo.</span><span class="sxs-lookup"><span data-stu-id="59bb5-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="59bb5-129">Vostede crea unha factura do proxecto cando o traballo rematado no proxecto alcanza unha porcentaxe especificada.</span><span class="sxs-lookup"><span data-stu-id="59bb5-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="59bb5-130">Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Contratos de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="59bb5-131">Na páxina **Contratos de proxecto**, seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="59bb5-132">Na caixa de diálogo **Novo contrato de proxecto**, configure os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="59bb5-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="59bb5-133">**Nome**</span><span class="sxs-lookup"><span data-stu-id="59bb5-133">**Name**</span></span>
    - <span data-ttu-id="59bb5-134">**Tipo de financiamento**</span><span class="sxs-lookup"><span data-stu-id="59bb5-134">**Funding type**</span></span>
    - <span data-ttu-id="59bb5-135">**Fonte de financiamento**</span><span class="sxs-lookup"><span data-stu-id="59bb5-135">**Funding source**</span></span>
    - <span data-ttu-id="59bb5-136">**Moeda de vendas** - Por defecto, esta moeda úsase para as facturas dos clientes asociadas ao contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="59bb5-137">Non obstante, pode cambiar a moeda de vendas nunha factura específica do cliente.</span><span class="sxs-lookup"><span data-stu-id="59bb5-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="59bb5-138">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-138">Select **OK**.</span></span> <span data-ttu-id="59bb5-139">A información copiase na cabeceira da páxina **Contratos de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="59bb5-140">Na páxina **Contratos de proxecto**, encha o resto da información requirida para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="59bb5-141">Crear un proxecto para a facturación de progreso</span><span class="sxs-lookup"><span data-stu-id="59bb5-141">Create a project for progress billings</span></span>

<span data-ttu-id="59bb5-142">Siga estes pasos para crear un proxecto e calquera subproxecto asociado a un contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="59bb5-143">Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="59bb5-144">Na páxina **Todos os proxectos**, seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="59bb5-145">Na caixa de diálogo **Novo proxecto**, no campo **Tipo de proxecto**, seleccione **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="59bb5-146">Seleccionar un grupo de proxectos.</span><span class="sxs-lookup"><span data-stu-id="59bb5-146">Select a project group.</span></span> <span data-ttu-id="59bb5-147">Un grupo de proxectos define a información de contabilización dos proxectos asignados ao grupo.</span><span class="sxs-lookup"><span data-stu-id="59bb5-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="59bb5-148">Seleccione **Crear proxecto**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-148">Select **Create project**.</span></span>
6. <span data-ttu-id="59bb5-149">Despois de crear o proxecto, configure a fase do proxecto en **En proceso**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="59bb5-150">Crear un orzamento para un proxecto</span><span class="sxs-lookup"><span data-stu-id="59bb5-150">Create a budget for a project</span></span>

<span data-ttu-id="59bb5-151">As categorías de orzamento utilízanse para calcular automaticamente os importes da factura para a porcentaxe de traballo que se completa para cada categoría.</span><span class="sxs-lookup"><span data-stu-id="59bb5-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="59bb5-152">Siga estes pasos para crear categorías de orzamento para os custos estimados.</span><span class="sxs-lookup"><span data-stu-id="59bb5-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="59bb5-153">Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="59bb5-154">Na páxina **Todos os proxectos**, seleccione e abra o proxecto que desexe.</span><span class="sxs-lookup"><span data-stu-id="59bb5-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="59bb5-155">Na páxina **Proxectos**, no Panel de acción, no separador **Plan**, no grupo **Orzamento**, seleccione **Orzamento do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="59bb5-156">Na páxina **Orzamento do proxecto**, introduza un custo estimado para cada categoría do proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="59bb5-157">Crear regras de facturación para a facturación de progreso</span><span class="sxs-lookup"><span data-stu-id="59bb5-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="59bb5-158">Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Contratos de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="59bb5-159">Na páxina de lista **Contratos de proxecto**, seleccione e abra un contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="59bb5-160">Na páxina do contrato do proxecto, no separador rápido **Regras de facturación**, seleccione **Engadir**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="59bb5-161">Na páxina **Regra de facturación**, no campo **Tipo de liña**, seleccione **Progreso**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="59bb5-162">No separador rápido **Detalles da liña de regra de facturación**, no campo **Valor do contrato**, introduza o valor total do contrato.</span><span class="sxs-lookup"><span data-stu-id="59bb5-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="59bb5-163">No campo **Categoría**, seleccione a categoría para contabilizar a transacción da tarifa.</span><span class="sxs-lookup"><span data-stu-id="59bb5-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="59bb5-164">No campo **Proxecto**, seleccione o proxecto que usa esta regra de facturación.</span><span class="sxs-lookup"><span data-stu-id="59bb5-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="59bb5-165">Opcional: Atribúa a regra de facturación a proxectos adicionais.</span><span class="sxs-lookup"><span data-stu-id="59bb5-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="59bb5-166">No separador rápido **Proxecto**, na sección **Proxectos dispoñibles**, seleccione un proxecto e, a seguir, seleccione o botón de frecha dereita para engadir o proxecto á sección **Proxectos seleccionados**.</span><span class="sxs-lookup"><span data-stu-id="59bb5-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="59bb5-167">Opcional: Calcule a cantidade porcentual que o cliente retén dos pagamentos dunha factura.</span><span class="sxs-lookup"><span data-stu-id="59bb5-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="59bb5-168">No separador rápido **Termos de retención do pagamento**, seleccione a fonte de financiamento e, a seguir, no campo **Porcentaxe de retención**, introduza a porcentaxe de retención.</span><span class="sxs-lookup"><span data-stu-id="59bb5-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="59bb5-169">Repita estes pasos para crear regras de facturación adicionais para o contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="59bb5-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]