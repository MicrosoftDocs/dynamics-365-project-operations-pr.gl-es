---
title: Sincronizar estimacións de proxectos directamente desde Project Service Automation a Finance and Operations
description: Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as estimacións de horas do proxecto e as estimacións de gastos do proxecto directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
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
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289457"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="6dbec-103">Sincronizar estimacións de proxectos directamente desde Project Service Automation a Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6dbec-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6dbec-104">Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as estimacións de horas do proxecto e as estimacións de gastos do proxecto directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="6dbec-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="6dbec-105">A integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades está dispoñible na versión 8.0.</span><span class="sxs-lookup"><span data-stu-id="6dbec-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="6dbec-106">A integración dos datos reais está dispoñible a partir da versión 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="6dbec-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="6dbec-107">Fluxo de datos de Project Service Automation a Finanzas</span><span class="sxs-lookup"><span data-stu-id="6dbec-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="6dbec-108">A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="6dbec-109">Os modelos de integración dispoñibles coa funcionalidade de integración de datos permiten o fluxo de datos sobre as estimacións de horas do proxecto e as estimacións de gastos do proxecto de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="6dbec-110">A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="6dbec-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="6dbec-111">[![Fluxo de datos para a integración de Project Service Automation con Finanzas](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="6dbec-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="6dbec-112">Estimacións de horas do proxecto</span><span class="sxs-lookup"><span data-stu-id="6dbec-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="6dbec-113">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="6dbec-113">Template and tasks</span></span>

<span data-ttu-id="6dbec-114">Para acceder aos modelos dispoñibles, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="6dbec-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="6dbec-115">O seguinte modelo e as tarefas subxacentes úsanse para sincronizar as estimacións de horas do proxecto de Project Service Automation a Finanzas:</span><span class="sxs-lookup"><span data-stu-id="6dbec-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="6dbec-116">**Nome do modelo en integración de datos:** Estimacións de horas do proxecto (PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="6dbec-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="6dbec-117">**Nome das tarefas do proxecto:**</span><span class="sxs-lookup"><span data-stu-id="6dbec-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="6dbec-118">Relacións de transacción</span><span class="sxs-lookup"><span data-stu-id="6dbec-118">Transaction relationships</span></span>
    - <span data-ttu-id="6dbec-119">Estimacións de gastos</span><span class="sxs-lookup"><span data-stu-id="6dbec-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="6dbec-120">Conxunto de entidades</span><span class="sxs-lookup"><span data-stu-id="6dbec-120">Entity set</span></span>

| <span data-ttu-id="6dbec-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6dbec-121">Project Service Automation</span></span> | <span data-ttu-id="6dbec-122">Finanzas</span><span class="sxs-lookup"><span data-stu-id="6dbec-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="6dbec-123">Tarefas do proxecto</span><span class="sxs-lookup"><span data-stu-id="6dbec-123">Project tasks</span></span>              | <span data-ttu-id="6dbec-124">Entidade de integración para estimacións de horas do proxecto</span><span class="sxs-lookup"><span data-stu-id="6dbec-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="6dbec-125">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="6dbec-125">Entity flow</span></span>

<span data-ttu-id="6dbec-126">As estimacións de horas do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como previsións de horas do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dbec-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6dbec-127">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6dbec-127">Prerequisites</span></span>

<span data-ttu-id="6dbec-128">Antes de que poida producirse a sincronización das estimacións de horas do proxecto, debe sincronizar proxectos, tarefas do proxecto e categorías de transaccións de gastos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dbec-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="6dbec-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="6dbec-129">Power Query</span></span>

<span data-ttu-id="6dbec-130">No modelo de estimacións de horas do proxecto, debe usar Microsoft Power Query for Excel para completar estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="6dbec-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="6dbec-131">Establecer o ID de modelo de previsión predefinido que se usará cando a integración cree novas previsións de horas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="6dbec-132">Filtrar os rexistros específicos de recursos na tarefa que fallarán na integración nas previsións de horas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="6dbec-133">Filtrar as filas de categoría de transaccións baleiras.</span><span class="sxs-lookup"><span data-stu-id="6dbec-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="6dbec-134">O incumprimento desta tarefa pode provocar previsións de horas incorrectas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="6dbec-135">Establecer o ID de modelo de previsión predeterminado</span><span class="sxs-lookup"><span data-stu-id="6dbec-135">Set the default forecast model ID</span></span>

<span data-ttu-id="6dbec-136">Para actualizar o ID de modelo de previsión predefinido no modelo, prema a frecha de **Asignar** para abrir a asignación.</span><span class="sxs-lookup"><span data-stu-id="6dbec-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="6dbec-137">A seguir, seleccione a ligazón **Consulta e filtrado avanzados**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="6dbec-138">Se está a usar o modelo predefinido de estimacións de horas do proxecto (PSA a Fin e Ops), seleccione a última **Condición inserida** na lista de **Pasos aplicados**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="6dbec-139">Na entrada **Función**, substitúa **O\_forecast** polo nome do ID de modelo de previsión que se debería empregar coa integración.</span><span class="sxs-lookup"><span data-stu-id="6dbec-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="6dbec-140">O modelo predefinido ten un ID de modelo de previsión a partir dos datos de demostración.</span><span class="sxs-lookup"><span data-stu-id="6dbec-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="6dbec-141">Se está a crear un novo modelo, debe engadir esta columna.</span><span class="sxs-lookup"><span data-stu-id="6dbec-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="6dbec-142">En Power Query, seleccione **Engadir columna condicional** e escriba un nome para a nova columna, como **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="6dbec-143">Introduza a condición para a columna, onde, se a tarefa de proxecto non é nula, entón \<enter the forecast model ID\>; senón nulo.</span><span class="sxs-lookup"><span data-stu-id="6dbec-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="6dbec-144">Filtrar rexistros específicos de recursos</span><span class="sxs-lookup"><span data-stu-id="6dbec-144">Filter out resource-specific records</span></span>

<span data-ttu-id="6dbec-145">O modelo de estimacións de horas do proxecto (PSA a Fin e Ops) ten un filtro predeterminado que elimina os rexistros específicos de recursos.</span><span class="sxs-lookup"><span data-stu-id="6dbec-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="6dbec-146">Se crea o seu propio modelo, debe engadir este filtro.</span><span class="sxs-lookup"><span data-stu-id="6dbec-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="6dbec-147">Seleccione a ligazón **Consulta e filtrado avanzados** para filtrar na columna **msdyn\_islinetask** para que só se inclúan os rexistros **False**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="6dbec-148">Filtrar as filas de categoría de transaccións baleiras</span><span class="sxs-lookup"><span data-stu-id="6dbec-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="6dbec-149">Debe engadir un filtro para eliminar as filas que teñan categorías de transaccións baleiras.</span><span class="sxs-lookup"><span data-stu-id="6dbec-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="6dbec-150">Esta tarefa é necesaria, independentemente de se está a usar o modelo predefinido ou se está a crear o seu propio modelo.</span><span class="sxs-lookup"><span data-stu-id="6dbec-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="6dbec-151">Este filtro elimina as filas resumidas de Project Service Automation que poidan causar que as previsións de horas en Finanzas sexan incorrectas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="6dbec-152">Seleccione a ligazón **Consulta e filtrado avanzados** para filtrar rexistros nulos na columna **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6dbec-153">Asignación de modelos na integración de datos</span><span class="sxs-lookup"><span data-stu-id="6dbec-153">Template mapping in Data integration</span></span>

<span data-ttu-id="6dbec-154">A seguinte ilustración mostra un exemplo da asignación de tarefas do modelo en integración de datos.</span><span class="sxs-lookup"><span data-stu-id="6dbec-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="6dbec-155">A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="6dbec-156">[![Asignación de tarefas de modelos na integración de datos](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6dbec-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="6dbec-157">Estimación de gastos do proxecto</span><span class="sxs-lookup"><span data-stu-id="6dbec-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="6dbec-158">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="6dbec-158">Template and tasks</span></span>

<span data-ttu-id="6dbec-159">O seguinte modelo e as tarefas subxacentes úsanse para sincronizar as estimacións de gastos do proxecto de Project Service Automation a Finanzas:</span><span class="sxs-lookup"><span data-stu-id="6dbec-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="6dbec-160">**Nome do modelo en integración de datos:** Estimacións de gastos do proxecto (PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="6dbec-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="6dbec-161">**Nome das tarefas do proxecto:**</span><span class="sxs-lookup"><span data-stu-id="6dbec-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="6dbec-162">Relacións de transacción</span><span class="sxs-lookup"><span data-stu-id="6dbec-162">Transaction relationships</span></span> 
    - <span data-ttu-id="6dbec-163">Estimacións de gastos</span><span class="sxs-lookup"><span data-stu-id="6dbec-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="6dbec-164">Conxunto de entidades</span><span class="sxs-lookup"><span data-stu-id="6dbec-164">Entity set</span></span>

| <span data-ttu-id="6dbec-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6dbec-165">Project Service Automation</span></span> | <span data-ttu-id="6dbec-166">Finanzas</span><span class="sxs-lookup"><span data-stu-id="6dbec-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="6dbec-167">Conexións da transacción</span><span class="sxs-lookup"><span data-stu-id="6dbec-167">Transaction Connections</span></span>    | <span data-ttu-id="6dbec-168">Entidade de integración para as relacións de transaccións do proxecto</span><span class="sxs-lookup"><span data-stu-id="6dbec-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="6dbec-169">Liñas de estimación</span><span class="sxs-lookup"><span data-stu-id="6dbec-169">Estimate Lines</span></span>             | <span data-ttu-id="6dbec-170">Entidade de integración para estimacións de gastos do proxecto</span><span class="sxs-lookup"><span data-stu-id="6dbec-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="6dbec-171">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="6dbec-171">Entity flow</span></span>

<span data-ttu-id="6dbec-172">As estimacións de gastos do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como previsións de gastos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dbec-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6dbec-173">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6dbec-173">Prerequisites</span></span>

<span data-ttu-id="6dbec-174">Antes de que poida producirse a sincronización das estimacións de gastos do proxecto, debe sincronizar proxectos, tarefas do proxecto e categorías de transaccións de gastos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dbec-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="6dbec-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="6dbec-175">Power Query</span></span>

<span data-ttu-id="6dbec-176">No modelo de estimacións de gastos do proxecto, debe usar Power Query para completar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="6dbec-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="6dbec-177">Filtrar para incluír só rexistros de liñas de estimación de gastos.</span><span class="sxs-lookup"><span data-stu-id="6dbec-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="6dbec-178">Establecer o ID de modelo de previsión predefinido que se usará cando a integración cree novas previsións de horas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="6dbec-179">Transformar os tipos de facturación.</span><span class="sxs-lookup"><span data-stu-id="6dbec-179">Transform the billing types.</span></span>
- <span data-ttu-id="6dbec-180">Transformar os tipos de transacción.</span><span class="sxs-lookup"><span data-stu-id="6dbec-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="6dbec-181">Filtrar para incluír só liñas de estimación de gastos</span><span class="sxs-lookup"><span data-stu-id="6dbec-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="6dbec-182">O modelo de estimacións de gastos do proxecto (PSA a Fin e Ops) ten un filtro predefinido que só inclúe liñas de gasto na integración.</span><span class="sxs-lookup"><span data-stu-id="6dbec-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="6dbec-183">Se crea o seu propio modelo, debe engadir este filtro.</span><span class="sxs-lookup"><span data-stu-id="6dbec-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="6dbec-184">Seleccione a tarefa **Relacións de transacción** e prema a frecha **Asignar** para abrir a asignación.</span><span class="sxs-lookup"><span data-stu-id="6dbec-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="6dbec-185">Seleccione a ligazón **Consulta e filtrado avanzados**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="6dbec-186">Filtre a columna **msdyn\_transactiontype1** para que só inclúa **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="6dbec-187">Establecer o ID de modelo de previsión predeterminado</span><span class="sxs-lookup"><span data-stu-id="6dbec-187">Set the default forecast model ID</span></span>

<span data-ttu-id="6dbec-188">Para actualizar o ID de modelo de previsión predefinido no modelo, seleccione a tarefa **Estimacións de gastos** e, a seguir, prema a frecha de **Asignar** para abrir a asignación.</span><span class="sxs-lookup"><span data-stu-id="6dbec-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="6dbec-189">Seleccione a ligazón **Consulta e filtrado avanzados**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="6dbec-190">Se está a usar o modelo predefinido de estimacións de gastos do proxecto (PSA a Fin e Ops), en Power Query, seleccione a primeira **Condición inserida** desde a sección **Pasos aplicados**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="6dbec-191">Na entrada **Función**, substitúa **O\_forecast** polo nome do ID de modelo de previsión que se debería empregar coa integración.</span><span class="sxs-lookup"><span data-stu-id="6dbec-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="6dbec-192">O modelo predefinido ten un ID de modelo de previsión a partir dos datos de demostración.</span><span class="sxs-lookup"><span data-stu-id="6dbec-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="6dbec-193">Se está a crear un novo modelo, debe engadir esta columna.</span><span class="sxs-lookup"><span data-stu-id="6dbec-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="6dbec-194">En Power Query, seleccione **Engadir columna condicional** e escriba un nome para a nova columna, como **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="6dbec-195">Introduza a condición para a columna, onde, se a ID de liña de estimación non é nula, entón \<enter the forecast model ID\>; senón nulo.</span><span class="sxs-lookup"><span data-stu-id="6dbec-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="6dbec-196">Transformar os tipos de facturación</span><span class="sxs-lookup"><span data-stu-id="6dbec-196">Transform the billing types</span></span>

<span data-ttu-id="6dbec-197">O modelo de estimacións de gastos do proxecto (PSA a Fin e Ops) inclúe unha columna condicional que se usa para transformar os tipos de facturación que se reciben de Project Service Automation durante a integración.</span><span class="sxs-lookup"><span data-stu-id="6dbec-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="6dbec-198">Se crea o seu propio modelo, debe engadir esta columna condicional.</span><span class="sxs-lookup"><span data-stu-id="6dbec-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="6dbec-199">Seleccione a ligazón **Consulta e filtrado avanzados** e logo seleccione **Engadir columna condicional**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="6dbec-200">Introduza un nome para a nova columna, como **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="6dbec-201">A seguir, introduza a seguinte condición:</span><span class="sxs-lookup"><span data-stu-id="6dbec-201">Then enter the following condition:</span></span>

<span data-ttu-id="6dbec-202">Se **msdyn\_billingtype** = 192350000, entón **Non imputable**</span><span class="sxs-lookup"><span data-stu-id="6dbec-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="6dbec-203">pero se **msdyn\_billingtype** = 192350001, entón **Imputable**</span><span class="sxs-lookup"><span data-stu-id="6dbec-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="6dbec-204">pero se **msdyn\_billingtype** = 192350002, entón **Gratuíto**</span><span class="sxs-lookup"><span data-stu-id="6dbec-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="6dbec-205">pero **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="6dbec-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="6dbec-206">Transformar os tipos de transacción</span><span class="sxs-lookup"><span data-stu-id="6dbec-206">Transform the transaction types</span></span>

<span data-ttu-id="6dbec-207">O modelo de estimacións de gastos do proxecto (PSA a Fin e Ops) inclúe unha columna condicional que se usa para transformar os tipos de transacción que se reciben de Project Service Automation durante a integración.</span><span class="sxs-lookup"><span data-stu-id="6dbec-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="6dbec-208">Se crea o seu propio modelo, debe engadir esta columna condicional.</span><span class="sxs-lookup"><span data-stu-id="6dbec-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="6dbec-209">Seleccione a ligazón **Consulta e filtrado avanzados** e logo seleccione **Engadir columna condicional**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="6dbec-210">Introduza un nome para a nova columna, como **Tipo de transacción**.</span><span class="sxs-lookup"><span data-stu-id="6dbec-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="6dbec-211">A seguir, introduza a seguinte condición:</span><span class="sxs-lookup"><span data-stu-id="6dbec-211">Then enter the following condition:</span></span>

<span data-ttu-id="6dbec-212">Se **msdyn\_transactiontypecode** = 192350000, entón **Custo**</span><span class="sxs-lookup"><span data-stu-id="6dbec-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="6dbec-213">pero se **msdyn\_transactiontypecode** = 192350005, entón **Vendas**</span><span class="sxs-lookup"><span data-stu-id="6dbec-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="6dbec-214">pero **null**</span><span class="sxs-lookup"><span data-stu-id="6dbec-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6dbec-215">Asignación de modelos na integración de datos</span><span class="sxs-lookup"><span data-stu-id="6dbec-215">Template mapping in Data integration</span></span>

<span data-ttu-id="6dbec-216">As seguintes ilustracións mostran exemplos das asignacións de tarefas do modelo en integración de datos.</span><span class="sxs-lookup"><span data-stu-id="6dbec-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="6dbec-217">A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="6dbec-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="6dbec-218">[![Asignación de modelos de transaccións de estimación de gastos](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6dbec-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="6dbec-219">[![Asignación de modelos de estimacións de gastos](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6dbec-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]