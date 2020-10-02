---
title: Configurar unha creación automática de facturas
description: Este tema ofrece información sobre como configurar o sistema para xerar facturas automaticamente.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898124"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="1d2e0-103">Configurar unha creación automática de facturas</span><span class="sxs-lookup"><span data-stu-id="1d2e0-103">Configure automated invoice creation</span></span>

<span data-ttu-id="1d2e0-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1d2e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d2e0-105">Complete os seguintes pasos para configurar unha factura automatizada executada en Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="1d2e0-106">Vaia a **Configuración** \> **Traballos en lote**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="1d2e0-107">Cree un traballo en lotes noméelo **Crear facturas de Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="1d2e0-108">O nome do traballo por lotes debe incluír o termo "crear facturas".</span><span class="sxs-lookup"><span data-stu-id="1d2e0-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="1d2e0-109">No campo **Tipo de traballo**, seleccione **Ningún**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="1d2e0-110">Por defecto, as opcións **Frecuencia diaria** e **Está activo** están definidas en **Si**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="1d2e0-111">Seleccione **Executar fluxo de traballo**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-111">Select **Run Workflow**.</span></span> <span data-ttu-id="1d2e0-112">Na caixa de diálogo **Buscar rexistro**, verá tres fluxos de traballo:</span><span class="sxs-lookup"><span data-stu-id="1d2e0-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="1d2e0-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="1d2e0-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="1d2e0-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="1d2e0-114">ProcessRunner</span></span>
    - <span data-ttu-id="1d2e0-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="1d2e0-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="1d2e0-116">Seleccione **ProcessRunCaller** e, a seguir, seleccione **Engadir**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="1d2e0-117">Na caixa de diálogo seguinte, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="1d2e0-118">Un fluxo de traballo **Suspensión** vai seguido por fluxo de traballo **Proceso**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="1d2e0-119">Tamén pode seleccionar **ProcessRunner** no paso 5.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="1d2e0-120">Entón, cando seleccione **Aceptar**, o fluxo de traballo **Proceso** vai seguido por un fluxo de traballo **Suspensión**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="1d2e0-121">Os fluxos de traballo **ProcessRunCaller** e **ProcessRunner** crean facturas.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="1d2e0-122">**ProcessRunCaller** chama a **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="1d2e0-123">**ProcessRunner** é o fluxo de traballo que realmente crea as facturas.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="1d2e0-124">Percorre todas as liñas de contrato nas que deben crearse as facturas e crea facturas para esas liñas.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="1d2e0-125">Para determinar as liñas de contrato para as que deben crearse as facturas, o traballo analiza as datas de execución de facturas para as liñas de contrato.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="1d2e0-126">Se as liñas de contrato que pertencen a un contrato teñen a mesma data de execución de facturas, as transaccións combínanse nunha factura que ten dúas liñas de factura.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="1d2e0-127">Se non hai transaccións para as que crear facturas, o traballo omite a creación de facturas.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="1d2e0-128">Despois de que **ProcessRunner** remate a execución, chama a **ProcessRunCaller**, fornece a hora de finalización e péchase.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="1d2e0-129">A seguir, **ProcessRunCaller** inicia un temporizador que se executa durante 24 horas desde a hora de finalización especificada.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="1d2e0-130">Ao final do temporizador, **ProcessRunCaller** péchase.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="1d2e0-131">O traballo de proceso por lotes para crear facturas é un traballo recorrente.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="1d2e0-132">Se este proceso de lotes se executa moitas veces, créanse varias instancias do traballo e causan erros.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="1d2e0-133">Polo tanto, debe iniciar o proceso por lotes unha soa vez e só debe reinicialo se deixa de executarse.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="1d2e0-134">A facturación por lotes só se executa para as liñas de contrato do proxecto que están configuradas por programacións de facturas.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="1d2e0-135">Unha liña de contrato cun método de facturación de prezos fixos debe ter configurados os fitos.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="1d2e0-136">Unha liña de contrato de proxecto cun método de facturación de tempo e material necesitará unha programación de facturas baseado na data configurada.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="1d2e0-137">O mesmo se aplica a unha liña de contrato baseada nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="1d2e0-137">The same applies to a project-based contract line.</span></span>     
