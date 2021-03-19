---
title: Novidades ou cambios na versión 23 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 23 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 379379ff643baa10417333b4be5e56d56eb5bc26
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280531"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="d17c9-103">Versión 23 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="d17c9-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d17c9-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d17c9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d17c9-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="d17c9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d17c9-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d17c9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d17c9-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="d17c9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d17c9-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="d17c9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d17c9-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 23 de actualización.</span><span class="sxs-lookup"><span data-stu-id="d17c9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="d17c9-110">Esta versión ten un número de compilación de V 3.10.34.30 e está dispoñible xeralmente a través dunha autoactualización desde agosto de 2020.</span><span class="sxs-lookup"><span data-stu-id="d17c9-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="d17c9-111">Versión 23 de actualización</span><span class="sxs-lookup"><span data-stu-id="d17c9-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d17c9-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="d17c9-112">Bug fixes</span></span>

<span data-ttu-id="d17c9-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="d17c9-113">**Time and Expense**</span></span>

<span data-ttu-id="d17c9-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="d17c9-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="d17c9-115">Manexar a caixa de edge en **Eliminar membro do equipo do proxecto** para proporcionar unha excepción significativa.</span><span class="sxs-lookup"><span data-stu-id="d17c9-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="d17c9-116">A importación de atribucións ten como resultado unha pantalla de eliminación en branco.</span><span class="sxs-lookup"><span data-stu-id="d17c9-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="d17c9-117">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="d17c9-117">**Resource Management**</span></span>

<span data-ttu-id="d17c9-118">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="d17c9-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="d17c9-119">O **Cartón de recursos da grade de utilización de recursos** mostra datos incorrectos cando a escala de tempo é superior a cinco días.</span><span class="sxs-lookup"><span data-stu-id="d17c9-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="d17c9-120">Cando os clientes crean un recurso reservable, o complemento intermitentemente non engade automaticamente o recurso a un grupo de Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="d17c9-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="d17c9-121">A vista **Conciliación** mostra incorrectamente os contornos manuais na vista **Semana** ou **Mes**.</span><span class="sxs-lookup"><span data-stu-id="d17c9-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="d17c9-122">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="d17c9-122">**Project Management**</span></span>

<span data-ttu-id="d17c9-123">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="d17c9-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="d17c9-124">Un número excesivo de entidades **RetrieveMultiple for usersettings** están causando un rendemento degradado para as aprobacións de proxectos e outras operacións.</span><span class="sxs-lookup"><span data-stu-id="d17c9-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="d17c9-125">A busca de recursos da grade **Planificación de tarefas** está limitada a só amosar ata cinco membros do equipo do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="d17c9-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="d17c9-126">A busca de recursos da grade **Planificación de tarefas** non filtra os recursos inactivos.</span><span class="sxs-lookup"><span data-stu-id="d17c9-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="d17c9-127">O modo manual non funciona como se esperaba na estrutura de subdivisión do traballo da planificación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="d17c9-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="d17c9-128">A grade **Planificación de tarefas** mostra **Categorías de transaccións inactivas**.</span><span class="sxs-lookup"><span data-stu-id="d17c9-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="d17c9-129">A grade **Atribución de recursos** redondea incorrectamente cando unha tarefa ten varias atribucións.</span><span class="sxs-lookup"><span data-stu-id="d17c9-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="d17c9-130">Os valores de redondeo son diferentes entre o custo planificado e o custo real para unha soa tarefa.</span><span class="sxs-lookup"><span data-stu-id="d17c9-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="d17c9-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d17c9-131">**Sales**</span></span>

<span data-ttu-id="d17c9-132">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="d17c9-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="d17c9-133">Ao premer dúas veces **Obter todas as categorías de transaccións** créanse varias liñas.</span><span class="sxs-lookup"><span data-stu-id="d17c9-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]