---
title: Novidades ou cambios na versión 32 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 32 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129664"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="eede0-103">Novidades ou cambios na versión 32 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="eede0-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="eede0-104">Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="eede0-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="eede0-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="eede0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eede0-106">É compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="eede0-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eede0-107">Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización.</span><span class="sxs-lookup"><span data-stu-id="eede0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="eede0-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="eede0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eede0-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 32 de actualización.</span><span class="sxs-lookup"><span data-stu-id="eede0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="eede0-110">Esta versión ten un número de compilación de V3.10.53.108 e normalmente está dispoñible a través dunha actualización automática en xuño de 2021.</span><span class="sxs-lookup"><span data-stu-id="eede0-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="eede0-111">Versión 32 de actualización</span><span class="sxs-lookup"><span data-stu-id="eede0-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eede0-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="eede0-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="eede0-113">Xeral</span><span class="sxs-lookup"><span data-stu-id="eede0-113">General</span></span>

- <span data-ttu-id="eede0-114">Cando falla unha actualización importante, só se deben bloquear os puntos de entrada da aplicación principal para garantir que as entidades compartidas sexan aínda accesibles.</span><span class="sxs-lookup"><span data-stu-id="eede0-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="eede0-115">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="eede0-115">Time and Expense</span></span>

<span data-ttu-id="eede0-116">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="eede0-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="eede0-117">**TimeEntriesImportFromResourceAssignment** non mantén os tempos de inicio e fin da porción de contorno de atribución de recursos.</span><span class="sxs-lookup"><span data-stu-id="eede0-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="eede0-118">Cando selecciona **Abrir entrada** na grade **Entrada de tempo**, é posible que se lle impida seleccionar outros formularios.</span><span class="sxs-lookup"><span data-stu-id="eede0-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="eede0-119">Mentres importa tarefas a entradas de tempo, a consulta de código de cliente pode xerar un URL longo que falla na consulta.</span><span class="sxs-lookup"><span data-stu-id="eede0-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="eede0-120">Na grade **Entrada de tempo**, despois de que se elimine un valor dunha cela, o foco non permanece na grade.</span><span class="sxs-lookup"><span data-stu-id="eede0-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="eede0-121">O botón **Rexeitar** eliminouse da vista **Aprobacións de procesamento** para aprobacións modernas.</span><span class="sxs-lookup"><span data-stu-id="eede0-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="eede0-122">A estabilidade e o rendemento da aprobación masiva de entradas de tempo vense afectados por bloqueos e un fallo no tratamento adecuado das personalizacións relacionadas coa entidade **Entrada de tempo**.</span><span class="sxs-lookup"><span data-stu-id="eede0-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="eede0-123">Planificación de proxectos</span><span class="sxs-lookup"><span data-stu-id="eede0-123">Project Planning</span></span>

- <span data-ttu-id="eede0-124">Xérase unha excepción de referencia nula cando se actualiza un proxecto que ten un valor nulo no campo **Unidade de contratación**.</span><span class="sxs-lookup"><span data-stu-id="eede0-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="eede0-125">**Actualizar os totais do proxecto** calcula incorrectamente o custo restante e as vendas restantes nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="eede0-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="eede0-126">Os cálculos de prezos redundantes afectan ao rendemento relacionado coas actualizacións dos contornos de atribución de recursos.</span><span class="sxs-lookup"><span data-stu-id="eede0-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="eede0-127">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="eede0-127">Resource Management</span></span>

<span data-ttu-id="eede0-128">Corrixiuse o seguinte problema:</span><span class="sxs-lookup"><span data-stu-id="eede0-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="eede0-129">Cando a capacidade do calendario dun recurso reservable é superior a 1, Project Service Automation recoñece incorrectamente a capacidade como 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="eede0-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="eede0-130">Polo tanto, prodúcese un bucle infinito na vista de programación.</span><span class="sxs-lookup"><span data-stu-id="eede0-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="eede0-131">Vendas</span><span class="sxs-lookup"><span data-stu-id="eede0-131">Sales</span></span>

<span data-ttu-id="eede0-132">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="eede0-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="eede0-133">Cando se crea unha liña de diario que ten un tipo de transacción personalizado, prodúcese a seguinte excepción de referencia nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="eede0-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="eede0-134">Os roles e categorías que están inactivos antes de copiar un orzamento non se deben engadir aos roles e categorías imputables da novo orzamento copiado.</span><span class="sxs-lookup"><span data-stu-id="eede0-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="eede0-135">A data do documento e a data de contabilidade non están aliñadas coa data de inicio que se proporciona nun detalle da liña de factura que se crea directamente nun borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="eede0-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="eede0-136">As excepcións de referencia nulas xéranse en escenarios relacionados coa inactivación de roles e categorías antes de copiar un orzamento.</span><span class="sxs-lookup"><span data-stu-id="eede0-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="eede0-137">A acción **Actualizar prezos** na páxina **Proxectos** non actualiza as estimacións de gastos e de material.</span><span class="sxs-lookup"><span data-stu-id="eede0-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
