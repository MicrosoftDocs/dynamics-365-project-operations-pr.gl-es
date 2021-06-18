---
title: Novidades ou cambios na versión 18 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 18 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006644"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="3e716-103">Versión 18 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="3e716-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3e716-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3e716-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3e716-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="3e716-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3e716-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3e716-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3e716-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="3e716-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="3e716-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="3e716-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3e716-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 18 de actualización.</span><span class="sxs-lookup"><span data-stu-id="3e716-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="3e716-110">Esta versión ten un número de compilación de V3.10.8.12 e está xeralmente dispoñible a través dunha actualización automática en abril de 2020.</span><span class="sxs-lookup"><span data-stu-id="3e716-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="3e716-111">Versión 18 de actualización</span><span class="sxs-lookup"><span data-stu-id="3e716-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3e716-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="3e716-112">Bug fixes</span></span>

<span data-ttu-id="3e716-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="3e716-113">**Time and Expense**</span></span>

- <span data-ttu-id="3e716-114">Corrixido: Os fluxos **Recuperar**, **Solicitar** e **Cancelar aprobación** lanzan excepcións con mensaxes de erro pouco claras.</span><span class="sxs-lookup"><span data-stu-id="3e716-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="3e716-115">Corrixido: Cando **Cancelar a aprobación** falla para un gasto, non se lanza un erro de excepción relevante.</span><span class="sxs-lookup"><span data-stu-id="3e716-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="3e716-116">Corrixido: A grade Entrada de tempo xestiona de forma incorrecta os días non laborables en Australia despois do cambio da hora de verán (DST) en outubro.</span><span class="sxs-lookup"><span data-stu-id="3e716-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="3e716-117">Corrixido: A lóxica por defecto incorrecta impide a presentación de gastos.</span><span class="sxs-lookup"><span data-stu-id="3e716-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="3e716-118">Corrixido: Cando falla a aprobación de entrada de tempo, a aprobación permanece en estado de **Pendente**.</span><span class="sxs-lookup"><span data-stu-id="3e716-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="3e716-119">Corrixido: Erros de SQL nas aprobacións en masa (paralización/tempo esgotado).</span><span class="sxs-lookup"><span data-stu-id="3e716-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="3e716-120">Corrixido: Problemas de rendemento importantes na experiencia do usuario causados pola actualización dos membros do equipo mentres aproban as entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="3e716-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="3e716-121">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="3e716-121">**Project Management**</span></span>

- <span data-ttu-id="3e716-122">Corrixido: A notificación do fuso horario mudouse da vista **Conciliación** ao formulario principal **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="3e716-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="3e716-123">Corrixido: O modelo do calendario non está predefinido correctamente cando se abre un novo formulario de proxecto.</span><span class="sxs-lookup"><span data-stu-id="3e716-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="3e716-124">Corrixido: Nos exploradores baseados en chromium, os usuarios non poden seleccionar facilmente as tarefas predecesoras para eliminar.</span><span class="sxs-lookup"><span data-stu-id="3e716-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="3e716-125">Corrixido: Ao crear ou copiar **Proxecto desde modelo baleiro** obtéñense asignacións non relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3e716-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="3e716-126">Corrixido: En casos específicos de edge, a creación dunha nova asignación desde a grade de tarefas ten como resultado a creación de rexistros duplicados.</span><span class="sxs-lookup"><span data-stu-id="3e716-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="3e716-127">Corrixido: En modo manual, os usuarios non poden actualizar as datas de inicio de tarefas como posteriores á data gardada.</span><span class="sxs-lookup"><span data-stu-id="3e716-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="3e716-128">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="3e716-128">**Resource Management**</span></span>

- <span data-ttu-id="3e716-129">Corrixido: A fila de subtotal da vista **Conciliación** calcula incorrectamente a diferenza das reservas despois de ampliar as reservas.</span><span class="sxs-lookup"><span data-stu-id="3e716-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="3e716-130">Corrixido: A vista **Conciliación** mostra incorrectamente as asignacións de recursos cando o recurso reservable ten un calendario que non coincide co calendario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="3e716-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="3e716-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3e716-131">**Sales**</span></span>

- <span data-ttu-id="3e716-132">Corrixido: Cando se aproban de novo as entradas de tempo (**Aprobar > Cancelar >** aprobar de novo), créase un duplicado real non imputable.</span><span class="sxs-lookup"><span data-stu-id="3e716-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]