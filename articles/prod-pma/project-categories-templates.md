---
title: Sincronizar as categorías de gastos do proxecto entre Finance and Operations e Project Service Automation
description: Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as categorías de gastos do proxecto entre Microsoft Dynamics 365 Finance e Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289637"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="588ea-103">Sincronizar as categorías de gastos do proxecto entre Finance and Operations e Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="588ea-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="588ea-104">Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as categorías de gastos do proxecto entre Dynamics 365 Finance e Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="588ea-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="588ea-105">A integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades están dispoñibles na versión 8.0.</span><span class="sxs-lookup"><span data-stu-id="588ea-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="588ea-106">A integración dos datos reais está dispoñible a partir da versión 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="588ea-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="588ea-107">Se está a usar Enterprise edition 7.3.0, despois de instalar KB 4132657 e KB 4132660, poderá usar os modelos para integrar tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e datos reais e para configurar o bloqueo de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="588ea-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="588ea-108">Se debe restablecer as distribucións contables, recomendámoslle que instale tamén KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="588ea-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="588ea-109">Fluxo de datos para Project Service Automation e Finanzas</span><span class="sxs-lookup"><span data-stu-id="588ea-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="588ea-110">A solución de integración de Project Service Automation e Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas.</span><span class="sxs-lookup"><span data-stu-id="588ea-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="588ea-111">Os modelos de integración dispoñibles coa funcionalidade de integración de datos permiten o fluxo de datos sobre as categorías de transaccións de gastos do proxecto entre Finanzas e Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="588ea-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="588ea-112">Se as categorías de gastos do proxecto se controlan en Finanzas, o fluxo de integración é primeiro de Finanzas a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="588ea-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="588ea-113">A seguir, actualízanse os ID de integración das categorías de gastos do proxecto mediante a sincronización de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="588ea-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="588ea-114">Se as categorías de gastos do proxecto se controlan en Project Service Automation, o fluxo de integración é primeiro de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="588ea-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="588ea-115">As categorías do proxecto xa deben estar configuradas en Finanzas antes da sincronización desde Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="588ea-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="588ea-116">A seguir, sincronice de novo de Finanzas a Project Service Automation e logo de Project Service Automation a Finanzas de novo.</span><span class="sxs-lookup"><span data-stu-id="588ea-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="588ea-117">Deste xeito, axudará a garantir que as categorías están vinculadas e que non se crean duplicados.</span><span class="sxs-lookup"><span data-stu-id="588ea-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="588ea-118">Normalmente, as categorías de gastos do proxecto contrólanse en Finanzas.</span><span class="sxs-lookup"><span data-stu-id="588ea-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="588ea-119">Non obstante, se non e así ou se xa se crearon categorías de gastos en Project Service Automation, primeiro debe sincronizar empregando o modelo de categorías de transaccións de gastos de proxecto (PSA a Fin e Ops).</span><span class="sxs-lookup"><span data-stu-id="588ea-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="588ea-120">A seguir, sincronízase usando o modelo de categorías de transaccións de gastos do proxecto (Fin e Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="588ea-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="588ea-121">A seguir, debería executar a sincronización de Project Service Automation a Finanzas unha vez máis.</span><span class="sxs-lookup"><span data-stu-id="588ea-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="588ea-122">Se sincroniza primeiro desde Project Service Automation, antes de executar a sincronización deben cumprirse os seguintes requisitos en Finanzas:</span><span class="sxs-lookup"><span data-stu-id="588ea-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="588ea-123">A categoría compartida que coincida coa categoría de proxecto configurada en Project Service Automation debe existir e debe estar activada para **Proxecto** e **Gasto**.</span><span class="sxs-lookup"><span data-stu-id="588ea-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="588ea-124">Para cada persoa xurídica de Finanzas coa que se debe integrar, deben existir as seguintes categorías de proxectos:</span><span class="sxs-lookup"><span data-stu-id="588ea-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="588ea-125">**A categoría do proxecto** existe.</span><span class="sxs-lookup"><span data-stu-id="588ea-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="588ea-126">**Usar en Gasto** está activada.</span><span class="sxs-lookup"><span data-stu-id="588ea-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="588ea-127">**Activar en diario** está activada.</span><span class="sxs-lookup"><span data-stu-id="588ea-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="588ea-128">**Tipo de transacción** está establecido en **Gasto**.</span><span class="sxs-lookup"><span data-stu-id="588ea-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="588ea-129">A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="588ea-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="588ea-130">[![Fluxo de datos para a integración de Project Service Automation con Finanzas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="588ea-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="588ea-131">Sincronización da categoría de gastos do proxecto de Finanzas a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="588ea-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="588ea-132">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="588ea-132">Template and task</span></span>

<span data-ttu-id="588ea-133">Para acceder ao modelo, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="588ea-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="588ea-134">O seguinte modelo e a tarefa subxacente úsanse para sincronizar as categorías de gastos do proxecto desde Finanzas ata Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="588ea-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="588ea-135">**Nome do modelo en integración de datos:** Categorías de transaccións de gastos do proxecto (Fin e Ops a PSA)</span><span class="sxs-lookup"><span data-stu-id="588ea-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="588ea-136">**Nome da tarefa do proxecto:** Sincronizar categorías con PSA</span><span class="sxs-lookup"><span data-stu-id="588ea-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="588ea-137">Conxunto de entidades</span><span class="sxs-lookup"><span data-stu-id="588ea-137">Entity set</span></span>

| <span data-ttu-id="588ea-138">Finanzas</span><span class="sxs-lookup"><span data-stu-id="588ea-138">Finance</span></span>                           | <span data-ttu-id="588ea-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="588ea-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="588ea-140">Entidade de integración para categorías</span><span class="sxs-lookup"><span data-stu-id="588ea-140">Integration entity for categories</span></span> | <span data-ttu-id="588ea-141">Categorías de transaccións</span><span class="sxs-lookup"><span data-stu-id="588ea-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="588ea-142">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="588ea-142">Entity flow</span></span>

<span data-ttu-id="588ea-143">As categorías de gastos do proxecto xestiónanse en Finanzas e se sincronizan con Project Service Automation como categorías de transaccións.</span><span class="sxs-lookup"><span data-stu-id="588ea-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="588ea-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="588ea-144">Power Query</span></span>

<span data-ttu-id="588ea-145">Cando se sincronice con Project Service Automation, debe empregar Microsoft Power Query for Excel para establecer o tipo de facturación na categoría de transaccións.</span><span class="sxs-lookup"><span data-stu-id="588ea-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="588ea-146">O modelo de categorías de transaccións de gastos do proxecto (Fin e Ops a PSA) ofrece unha columna predefinida e asignación.</span><span class="sxs-lookup"><span data-stu-id="588ea-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="588ea-147">Se crea o seu propio modelo, debe engadir unha columna condicional en Power Query.</span><span class="sxs-lookup"><span data-stu-id="588ea-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="588ea-148">Siga estes pasos.</span><span class="sxs-lookup"><span data-stu-id="588ea-148">Follow these steps.</span></span>

1. <span data-ttu-id="588ea-149">Prema na frecha para abrir a asignación da tarefa de categorías de gastos do proxecto no modelo de categorías de transaccións de gastos de proxecto (Fin e Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="588ea-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="588ea-150">Prema a ligazón **Consulta e filtrado avanzados** para abrir Power Query.</span><span class="sxs-lookup"><span data-stu-id="588ea-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="588ea-151">Seleccione **Engadir columna condicional**.</span><span class="sxs-lookup"><span data-stu-id="588ea-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="588ea-152">Introduza un nome para a nova columna, como **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="588ea-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="588ea-153">Introduza a seguinte condición: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="588ea-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="588ea-154">Prema **Aceptar** na columna.</span><span class="sxs-lookup"><span data-stu-id="588ea-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="588ea-155">Asegúrese de asignar esta nova columna na páxina de asignación.</span><span class="sxs-lookup"><span data-stu-id="588ea-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="588ea-156">A seguinte ilustración mostra un exemplo da asignación de tarefas do modelo en integración de datos.</span><span class="sxs-lookup"><span data-stu-id="588ea-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="588ea-157">A asignación mostra a información de campo que se sincronizará de Finanzas a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="588ea-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="588ea-158">[![Asignación de modelos de categoría de gastos do proxecto a Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="588ea-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="588ea-159">Sincronización da categoría de gastos do proxecto de Project Service Automation a Finanzas</span><span class="sxs-lookup"><span data-stu-id="588ea-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="588ea-160">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="588ea-160">Template and task</span></span>

<span data-ttu-id="588ea-161">O seguinte modelo e a tarefa subxacente úsanse para sincronizar as categorías de gastos do proxecto de Project Service Automation a Finanzas:</span><span class="sxs-lookup"><span data-stu-id="588ea-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="588ea-162">**Nome do modelo en integración de datos:** Categorías de transaccións de gastos do proxecto (PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="588ea-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="588ea-163">**Nome da tarefa do proxecto:** Sincronizar categorías con Fin Ops</span><span class="sxs-lookup"><span data-stu-id="588ea-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="588ea-164">Conxunto de entidades</span><span class="sxs-lookup"><span data-stu-id="588ea-164">Entity set</span></span>

| <span data-ttu-id="588ea-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="588ea-165">Project Service Automation</span></span> | <span data-ttu-id="588ea-166">Finanzas</span><span class="sxs-lookup"><span data-stu-id="588ea-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="588ea-167">Categorías de transaccións</span><span class="sxs-lookup"><span data-stu-id="588ea-167">Transaction categories</span></span>     | <span data-ttu-id="588ea-168">Entidade de integración para categorías</span><span class="sxs-lookup"><span data-stu-id="588ea-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="588ea-169">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="588ea-169">Entity flow</span></span>

<span data-ttu-id="588ea-170">As categorías de gastos do proxecto xestiónanse en Finanzas e se sincronizan con Project Service Automation como categorías de transaccións.</span><span class="sxs-lookup"><span data-stu-id="588ea-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="588ea-171">A sincronización de novo con Finanzas actualiza a categoría do proxecto en Finanzas co ID de integración desde Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="588ea-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="588ea-172">Asignación de modelos na integración de datos</span><span class="sxs-lookup"><span data-stu-id="588ea-172">Template mapping in Data integration</span></span>

<span data-ttu-id="588ea-173">A seguinte ilustración mostra un exemplo da asignación de tarefas do modelo en integración de datos.</span><span class="sxs-lookup"><span data-stu-id="588ea-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="588ea-174">A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.</span><span class="sxs-lookup"><span data-stu-id="588ea-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="588ea-175">[![Asignación de modelos de Project Service Automation a Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="588ea-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]