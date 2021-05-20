---
title: Novidades ou cambios na versión 12 de actualización de Project Service Automation, V3
description: Este tema fornece información sobre as novidades e as modificacións na versión 12 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 58a12ded135712d8194499ce4a9ba9e4e2aa99bd
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949497"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="6c9cf-103">Versión 12 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="6c9cf-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6c9cf-104">Comprácenos anunciar a última actualización para a aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="6c9cf-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6c9cf-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6c9cf-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6c9cf-107">Para actualizar a esta versión, visite o Centro de administración para Dynamics 365 en liña e vaia á páxina de solucións para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6c9cf-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="6c9cf-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6c9cf-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 12 de actualización.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="6c9cf-110">Esta versión ten un número de compilación de V3.10.2.34 e está dispoñible xeralmente a través dunha autoactualización desde outubro de 2019.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="6c9cf-111">Versión 12 de actualización</span><span class="sxs-lookup"><span data-stu-id="6c9cf-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6c9cf-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="6c9cf-112">Bug fixes</span></span>

- <span data-ttu-id="6c9cf-113">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="6c9cf-113">Time and Expense</span></span>

    - <span data-ttu-id="6c9cf-114">Corrixido: As mensaxes de erro de entrada de tempo actualizáronse cun contexto máis relevante.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="6c9cf-115">Corrixido: A grade de entrada de tempo e a programación mostran correctamente a barra de desprazamento vertical cando é necesario.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="6c9cf-116">Corrixido: As entradas de gasto e tempo enviadas poden aprobarse.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="6c9cf-117">Corrixido: Corrixiuse a mensaxe de diálogo de Cancelar confirmación de aprobación para reflectir o estado da aprobación cando se cambia de **Aprobado** a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="6c9cf-118">Corrixido: Os campos **Prezo**, **Unidade** e **Cantidade** campos agora están bloqueados no rexistro Gasto despois de que se aprobaron.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="6c9cf-119">Xestión de proxectos</span><span class="sxs-lookup"><span data-stu-id="6c9cf-119">Project Management</span></span>

    - <span data-ttu-id="6c9cf-120">Fixado: A acción **Novo** no formulario principal de **Membro do equipo** eliminouse.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="6c9cf-121">Corrixido: As atribucións de recursos actualizáronse para dar conta de erros de redondeo inexacto, que provocan un cambio na data de finalización dunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="6c9cf-122">Corrixido: Na grade de tarefas, mostraranse ao usuario os erros relevantes do servidor.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="6c9cf-123">Corrixido: O nome do membro do equipo móstrase agora no selector de tarefas en vez do nome do posto.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="6c9cf-124">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="6c9cf-124">Resource Management</span></span>

    - <span data-ttu-id="6c9cf-125">Corrixido: Os detalles do requisito do recurso para os proxectos creados a partir dun modelo agora usan o calendario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="6c9cf-126">Corrixido: As habilidades e as competencias agora se definen segundo os datos mestres do rol no requisito de recurso creado para ese rol.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="6c9cf-127">Sales</span><span class="sxs-lookup"><span data-stu-id="6c9cf-127">Sales</span></span>

    - <span data-ttu-id="6c9cf-128">Corrixido: Os ID de obxecto duplicados atopados no formulario **Principal do contrato**.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="6c9cf-129">Corrixido: A lóxica actualizouse para facer que o separador **Análise de ofertas** sexa visible e mostre a configuración de metadatos do separador.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="6c9cf-130">Corrixido: A data de contabilidade do rexistro real agora procede da data da entrada de tempo/gasto e non da data de aprobación.</span><span class="sxs-lookup"><span data-stu-id="6c9cf-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]