---
title: Visión xeral de Project Service Automation
description: Este tema ofrece información sobre a solución de integración Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751408"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="b3e78-103">Visión xeral de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b3e78-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b3e78-104">A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Dynamics 365 Finance e Dynamics 365 Project Service Automation a través de Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b3e78-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="b3e78-105">A integración de modelos dispoñible coa funcionalidade de integración de datos permite o fluxo de proxectos, contratos de proxectos, liñas de contratos de proxectos, fitos da liña de contratos de proxectos, tarefas de proxectos, categorías de transaccións de datos, estimacións de horas e estimacións de gastos de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="b3e78-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="b3e78-106">Se está a usar a versión 7.3.0, debe instalar KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="b3e78-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="b3e78-107">Despois poderá integrar proxectos de prezo fixo.</span><span class="sxs-lookup"><span data-stu-id="b3e78-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="b3e78-108">Se está a usar a versión 7.3.0 e trae transaccións de tarifas desde Project Service Automation, debe instalar KB 4345320 para poder incluír esas tarifas na factura do proxecto.</span><span class="sxs-lookup"><span data-stu-id="b3e78-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="b3e78-109">Se está a usar a versión 8.0, poderá usar a integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="b3e78-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="b3e78-110">Se está a usar a versión 8.0.1 ou posterior, poderá sincronizar os datos reais.</span><span class="sxs-lookup"><span data-stu-id="b3e78-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="b3e78-111">Antes de poder integrar Project Service Automation Finance, debe configurar os parámetros de integración de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b3e78-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="b3e78-112">Para obter máis información, consulte [Parámetros de integración de Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b3e78-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="b3e78-113">Esta solución de integración permite a sincronización directa nos seguintes escenarios:</span><span class="sxs-lookup"><span data-stu-id="b3e78-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="b3e78-114">Manter contratos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b3e78-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b3e78-115">Crear proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b3e78-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b3e78-116">Manter liñas de contratos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b3e78-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b3e78-117">Manter fitos de liñas de contratos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b3e78-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b3e78-118">Manter tarefas de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b3e78-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b3e78-119">Manter contratos de categorías de transaccións de gastos en Finanzas e sincronizalos directamente desde Finanzas a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b3e78-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="b3e78-120">Crear estimacións de horas de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b3e78-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b3e78-121">Crear estimacións de gastos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b3e78-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b3e78-122">Crear datos reais de tempo, gastos e tarifas de proxectos en Project Service Automation e cree transaccións de proxectos no diario de integración de Project Service Automation para que poidan contabilizarse en Finanzas.</span><span class="sxs-lookup"><span data-stu-id="b3e78-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="b3e78-123">Sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="b3e78-123">Data synchronization</span></span>

<span data-ttu-id="b3e78-124">A seguinte ilustración mostra como se sincronizan os datos como parte da integración entre Project Service Automation e Finanzas.</span><span class="sxs-lookup"><span data-stu-id="b3e78-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="b3e78-125">Non están dispoñibles todos os modelos actualmente.</span><span class="sxs-lookup"><span data-stu-id="b3e78-125">Not all templates are currently available.</span></span> <span data-ttu-id="b3e78-126">Os modelos publicaranse a medida que se completen.</span><span class="sxs-lookup"><span data-stu-id="b3e78-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="b3e78-127">[![Integración de Project Service Automation con Finanzas](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="b3e78-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="b3e78-128">Requisitos do sistema para Finanzas</span><span class="sxs-lookup"><span data-stu-id="b3e78-128">System requirements for Finance</span></span>

<span data-ttu-id="b3e78-129">Para usar a solución de integración de Project Service Automation a Finanzas, debe instalar Enterprise edition 7.3 coa plataforma 12 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b3e78-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="b3e78-130">Requisitos do sistema para Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b3e78-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="b3e78-131">Para usar a solución de integración de Project Service Automation a Finanzas, debe instalar os seguintes compoñentes:</span><span class="sxs-lookup"><span data-stu-id="b3e78-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="b3e78-132">Dynamics 365 Project Service Automation versión 9.0.0.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b3e78-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="b3e78-133">Solución de posible a interesado a efectivo para Dynamics 365 Sales, versión 1.14.0.0 (v14) ou posterior</span><span class="sxs-lookup"><span data-stu-id="b3e78-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="b3e78-134">Solución de Project Service Automation a Finanzas para Dynamics 365 Project Service Automation versión 1.0.0.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b3e78-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="b3e78-135">Instalar a solución de integración de Project Service Automation a Finanzas na súa instancia de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b3e78-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="b3e78-136">Descargue a solución de integración de Project Service Automation a Finanzas del [Centro de descargas de Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) e siga as instrucións que se inclúen coa solución.</span><span class="sxs-lookup"><span data-stu-id="b3e78-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
