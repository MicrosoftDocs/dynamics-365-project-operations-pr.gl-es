---
title: Novidades ou cambios na versión 29 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 29 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948628"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="6fa24-103">Novidades ou cambios na versión 29 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="6fa24-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6fa24-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6fa24-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6fa24-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="6fa24-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6fa24-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6fa24-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6fa24-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="6fa24-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6fa24-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="6fa24-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6fa24-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 29 de actualización.</span><span class="sxs-lookup"><span data-stu-id="6fa24-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="6fa24-110">Esta versión ten un número de compilación de V3.10.47.7 e está dispoñible xeralmente a través dunha actualización automática en febreiro de 2021.</span><span class="sxs-lookup"><span data-stu-id="6fa24-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="6fa24-111">Versión 29 de actualización</span><span class="sxs-lookup"><span data-stu-id="6fa24-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6fa24-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="6fa24-112">Bug fixes</span></span>

<span data-ttu-id="6fa24-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="6fa24-113">**Time and Expense**</span></span>

<span data-ttu-id="6fa24-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6fa24-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6fa24-115">Os usuarios non poden ver as horas de traballo rexistradas en días non laborables na grade de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="6fa24-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="6fa24-116">As entradas de gastos aprobadas pódense editar na grade.</span><span class="sxs-lookup"><span data-stu-id="6fa24-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="6fa24-117">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="6fa24-117">**Project Management**</span></span>

<span data-ttu-id="6fa24-118">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6fa24-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="6fa24-119">Falta a lóxica de validación para garantir que as horas de esforzo de atribución de recursos non poidan ser negativas.</span><span class="sxs-lookup"><span data-stu-id="6fa24-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="6fa24-120">A acción personalizada **AssignResourcesForTask** actualiza todos os campos en vez de só os campos modificados.</span><span class="sxs-lookup"><span data-stu-id="6fa24-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="6fa24-121">Ao copiar un proxecto nun ambiente con complementos ou fluxos de traballo rexistrados no evento **CreateProject**, o atributo **msdyn_bulkgenerationstatus** non se actualiza se falla **CopyWBSToProject**.</span><span class="sxs-lookup"><span data-stu-id="6fa24-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="6fa24-122">Ao ampliar o calendario do proxecto, os días hábiles non se ordenan en orde ascendente e provocan o fallo dalgunhas actualizacións das tarefas do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6fa24-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="6fa24-123">Cambiar o xestor de proxectos nun proxecto existente desencadea a lóxica predefinida da unidade organizativa.</span><span class="sxs-lookup"><span data-stu-id="6fa24-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="6fa24-124">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="6fa24-124">**Sales**</span></span>

<span data-ttu-id="6fa24-125">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6fa24-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="6fa24-126">O separador **Execución do contrato** na páxina **Contrato** falla en silencio durante o inicio cando non hai liñas de contrato.</span><span class="sxs-lookup"><span data-stu-id="6fa24-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>