---
title: Novidades ou cambios na versión 19 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 19 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949137"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="ef957-103">Versión 19 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="ef957-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ef957-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ef957-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ef957-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="ef957-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ef957-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ef957-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ef957-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="ef957-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ef957-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="ef957-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ef957-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 19 de actualización.</span><span class="sxs-lookup"><span data-stu-id="ef957-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="ef957-110">Esta versión ten un número de compilación de V3.10.30.41 e está xeralmente dispoñible a través dunha actualización automática en maio de 2020.</span><span class="sxs-lookup"><span data-stu-id="ef957-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="ef957-111">Versión 19 de actualización</span><span class="sxs-lookup"><span data-stu-id="ef957-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ef957-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="ef957-112">Bug fixes</span></span>

<span data-ttu-id="ef957-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="ef957-113">**Time and Expense**</span></span>

<span data-ttu-id="ef957-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="ef957-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="ef957-115">Os erros derivados das importacións de entradas de tempo non aparecen correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef957-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="ef957-116">A grade de entrada de tempo non admite o comportamento de campo **Só data**.</span><span class="sxs-lookup"><span data-stu-id="ef957-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="ef957-117">Os recursos do proxecto non son capaces de crear un gasto cun proxecto.</span><span class="sxs-lookup"><span data-stu-id="ef957-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="ef957-118">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="ef957-118">**Project Management**</span></span>

<span data-ttu-id="ef957-119">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="ef957-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="ef957-120">A tarefa seguinte á secundaria causa unha estimación de esforzo incorrecta durante o cálculo de finalización (EAC).</span><span class="sxs-lookup"><span data-stu-id="ef957-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="ef957-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ef957-121">**Sales**</span></span>

<span data-ttu-id="ef957-122">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="ef957-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="ef957-123">A acción **Calcular de novo** non funciona cos detalles da liña do contrato de gasto ou cos detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="ef957-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="ef957-124">**Actualizar prezos** falta para as estimacións de gastos.</span><span class="sxs-lookup"><span data-stu-id="ef957-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="ef957-125">Os clientes non poden seleccionar os motivos para o estado do contrato na páxina **Contrato de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="ef957-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="ef957-126">Os clientes experimentan un rendemento degradado ao crear unha lista de prezos personalizada a partir dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="ef957-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="ef957-127">Os clientes experimentan incoherencia cos valores predeterminados de **unidade** nas páxinas **Detalles da liña de oferta** e **Detalles da liña de contrato**.</span><span class="sxs-lookup"><span data-stu-id="ef957-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="ef957-128">Se engade elementos da categoría de transacción non imputable a unha liña de contrato imputable, non se respectará o tipo de facturación **Non imputable** da categoría de transacción.</span><span class="sxs-lookup"><span data-stu-id="ef957-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="ef957-129">Os clientes non poden usar os roles e a categoría engadidos recentemente nos contratos creados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ef957-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="ef957-130">Os clientes experimentan un rendemento degradado. Recuperación innecesaria en PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="ef957-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="ef957-131">Os roles configurados como non imputables na lista **Categorías de recursos** deberían engadirse ao separador **Roles imputables** como **Non imputable** na liña de contrato dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="ef957-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="ef957-132">Os clientes poden experimentar un rendemento degradado ao crear un proxecto porque **GetBookableResourceIdFromUser** recupera todas as columnas de recursos reservables en vez de só o ID principal.</span><span class="sxs-lookup"><span data-stu-id="ef957-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="ef957-133">Na entidade **Tipo de transacción** falta o complemento de actualización de validación previa para evitar que os usuarios introduzan **Unidades** e **Grupos de unidades** que non sexan válidos para os tipos de transacción.</span><span class="sxs-lookup"><span data-stu-id="ef957-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="ef957-134">O paso **Eliminar** non funciona para a importación de entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="ef957-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]