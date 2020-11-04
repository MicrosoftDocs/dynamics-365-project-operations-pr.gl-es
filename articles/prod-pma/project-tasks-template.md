---
title: Sincronizar tarefas de proxectos directamente desde Project Service Automation a Finance and Operations
description: Este tema describe o modelo e a tarefa subxacente que se usan para sincronizar as tarefas do proxecto directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076114"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="97be8-103">Sincronizar tarefas de proxectos directamente desde Project Service Automation a Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97be8-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="97be8-104">Este tema describe o modelo e a tarefa subxacente que se usan para sincronizar as tarefas do proxecto directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="97be8-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="97be8-105">A integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades están dispoñibles na versión 8.0.</span><span class="sxs-lookup"><span data-stu-id="97be8-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="97be8-106">Se está a usar Enterprise edition 7.3.0, despois de instalar KB 4132657 e KB 4132660, poderá usar os modelos para integrar tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e datos reais e para configurar o bloqueo de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="97be8-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="97be8-107">Se debe restablecer as distribucións contables, recomendámoslle que instale tamén KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="97be8-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="97be8-108">A integración dos datos reais está dispoñible a partir da versión 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="97be8-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="97be8-109">Fluxo de datos de Project Service Automation a Finanzas</span><span class="sxs-lookup"><span data-stu-id="97be8-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="97be8-110">A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas.</span><span class="sxs-lookup"><span data-stu-id="97be8-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="97be8-111">O modelo de integración dispoñible coa funcionalidade de integración de datos permite o fluxo de datos sobre as tarefas do proxecto de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="97be8-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="97be8-112">A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="97be8-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="97be8-113">[![Fluxo de datos para a integración de Project Service Automation con Finanzas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="97be8-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="97be8-114">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="97be8-114">Template and task</span></span>

<span data-ttu-id="97be8-115">Para acceder ao modelo, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="97be8-115">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="97be8-116">O seguinte modelo e a tarefa subxacente úsanse para sincronizar as tarefas do proxecto de Project Service Automation a Finanzas:</span><span class="sxs-lookup"><span data-stu-id="97be8-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="97be8-117">**Nome do modelo en integración de datos:** Tarefas do proxecto (PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="97be8-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="97be8-118">**Nome da tarefa do proxecto:** Tarefas do proxecto</span><span class="sxs-lookup"><span data-stu-id="97be8-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="97be8-119">Antes de que poida producirse a sincronización de tarefas de proxectos e proxectos, debe sincronizar os contratos do proxecto e os proxectos.</span><span class="sxs-lookup"><span data-stu-id="97be8-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="97be8-120">Conxunto de entidades</span><span class="sxs-lookup"><span data-stu-id="97be8-120">Entity set</span></span>

| <span data-ttu-id="97be8-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="97be8-121">Project Service Automation</span></span> | <span data-ttu-id="97be8-122">Finanzas</span><span class="sxs-lookup"><span data-stu-id="97be8-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="97be8-123">Tarefas do proxecto</span><span class="sxs-lookup"><span data-stu-id="97be8-123">Project Tasks</span></span>              | <span data-ttu-id="97be8-124">Entidade de integración para a tarefa do proxecto</span><span class="sxs-lookup"><span data-stu-id="97be8-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="97be8-125">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="97be8-125">Entity flow</span></span>

<span data-ttu-id="97be8-126">As tarefas do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como tarefas de proxecto.</span><span class="sxs-lookup"><span data-stu-id="97be8-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="97be8-127">Requisitos previos e configuración de asignación</span><span class="sxs-lookup"><span data-stu-id="97be8-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="97be8-128">Antes de que poida producirse a sincronización de tarefas de proxectos e proxectos, debe sincronizar os contratos do proxecto e os proxectos.</span><span class="sxs-lookup"><span data-stu-id="97be8-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="97be8-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="97be8-129">Power Query</span></span>

<span data-ttu-id="97be8-130">Debe usar Microsoft Power Query for Excel para filtrar os datos se se cumpre esta condición:</span><span class="sxs-lookup"><span data-stu-id="97be8-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="97be8-131">Ten rexistros específicos de recursos nunha tarefa do proxecto.</span><span class="sxs-lookup"><span data-stu-id="97be8-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="97be8-132">Se debe usar Power Query, siga esta pauta:</span><span class="sxs-lookup"><span data-stu-id="97be8-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="97be8-133">O modelo de tarefas do proxecto (PSA a Fin e Ops) ten un filtro predefinido que exclúe os rexistros específicos do recurso dunha tarefa do proxecto configurando o filtro en **IsLineTask** a **False**.</span><span class="sxs-lookup"><span data-stu-id="97be8-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="97be8-134">Se crea o seu propio modelo, debe engadir este filtro.</span><span class="sxs-lookup"><span data-stu-id="97be8-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="97be8-135">Asignación de modelos na integración de datos</span><span class="sxs-lookup"><span data-stu-id="97be8-135">Template mapping in Data integration</span></span>

<span data-ttu-id="97be8-136">A seguinte ilustración mostra un exemplo das asignacións de tarefas do modelo en integración de datos.</span><span class="sxs-lookup"><span data-stu-id="97be8-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="97be8-137">A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="97be8-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="97be8-138">[![Asignación de modelos](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="97be8-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
