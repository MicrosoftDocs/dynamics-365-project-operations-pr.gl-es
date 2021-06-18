---
title: Novidades ou cambios na versión 15 de actualización de Project Service Automation, V3
description: Este tema fornece información sobre as novidades e as modificacións na versión 15 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 86aadca637939120d0ccd839e7c425e9e8d38aec
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006824"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="f0342-103">Versión 15 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="f0342-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f0342-104">Comprácenos anunciar a última actualización para a aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="f0342-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="f0342-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="f0342-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f0342-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f0342-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f0342-107">Para actualizar a esta versión, visite o Centro de administración para Dynamics 365 en liña e vaia á páxina de solucións para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="f0342-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="f0342-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="f0342-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f0342-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 15 de actualización.</span><span class="sxs-lookup"><span data-stu-id="f0342-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="f0342-110">Esta versión ten un número de compilación de V3.10.5.28 e está dispoñible xeralmente a través dunha autoactualización desde xaneiro de 2020.</span><span class="sxs-lookup"><span data-stu-id="f0342-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="f0342-111">Versión 15 de actualización</span><span class="sxs-lookup"><span data-stu-id="f0342-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="f0342-112">Melloras</span><span class="sxs-lookup"><span data-stu-id="f0342-112">Enhancements</span></span>

- <span data-ttu-id="f0342-113">Xestión de proxectos</span><span class="sxs-lookup"><span data-stu-id="f0342-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f0342-114">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="f0342-114">Bug fixes</span></span>

- <span data-ttu-id="f0342-115">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="f0342-115">Time and Expense</span></span>

  - <span data-ttu-id="f0342-116">Corrixido: Engadiuse o tratamento de erros de carga na vista de conciliación.</span><span class="sxs-lookup"><span data-stu-id="f0342-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="f0342-117">Corrixido: Plataforma común de recursos do proxecto: Cambiouse o nome **Cantidade** para reducir a ambigüidade.</span><span class="sxs-lookup"><span data-stu-id="f0342-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="f0342-118">Corrixido: Axustouse a vista **Copiar columnas de entrada de tempo** para incluír o tipo.</span><span class="sxs-lookup"><span data-stu-id="f0342-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="f0342-119">Corrixido: A edición da duración de entrada de tempo na vista de grade usando números decimais produce un erro descoñecido para algúns números.</span><span class="sxs-lookup"><span data-stu-id="f0342-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="f0342-120">Xestión de proxectos</span><span class="sxs-lookup"><span data-stu-id="f0342-120">Project Management</span></span>

  - <span data-ttu-id="f0342-121">Corrixido: O menú despregable para **Usar en vista de rastrexo** agora expándese en función do ancho das opcións.</span><span class="sxs-lookup"><span data-stu-id="f0342-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="f0342-122">Corrixido: Ao xestionar proxectos no fuso horario +13, os cálculos de tarefas poden mostrar resultados incorrectos.</span><span class="sxs-lookup"><span data-stu-id="f0342-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="f0342-123">Corrixido: **Hora de finalización do membro do equipo** corrixiuse cando se usa un calendario de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="f0342-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="f0342-124">Corrixido: Reactivouse o **BPF** no formulario principal **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="f0342-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="f0342-125">Corrixido: O cálculo de atribucións xa non ignora un día.</span><span class="sxs-lookup"><span data-stu-id="f0342-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="f0342-126">Corrixido: Engadiuse unha nova faixa de notificación ao formulario do proxecto cando o fuso horario difire entre usuario e proxecto.</span><span class="sxs-lookup"><span data-stu-id="f0342-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="f0342-127">Sales</span><span class="sxs-lookup"><span data-stu-id="f0342-127">Sales</span></span>

  - <span data-ttu-id="f0342-128">Corrixido: A busca de categoría de estimación de gasto pódese usar para filtrar duplicados.</span><span class="sxs-lookup"><span data-stu-id="f0342-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="f0342-129">Corrixido: O código **PluginDomain.ExecuteInTryCatchBlock(..)** xa non oculta a orixe da excepción.</span><span class="sxs-lookup"><span data-stu-id="f0342-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="f0342-130">Corrixido: Xa non se recibe unha mensaxe de erro en **Busca de proxectos** no formulario **Liña de oferta** cando hai máis de 1000 proxectos.</span><span class="sxs-lookup"><span data-stu-id="f0342-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="f0342-131">Corrixido: A grade **Estimacións** para estimacións laborais e estimacións de gastos agora mostra o símbolo monetario correcto.</span><span class="sxs-lookup"><span data-stu-id="f0342-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="f0342-132">Corrixido: Despois de que unha organización actualice PSA desde a versión 14 de actualización á versión 15 de actualización, o separador **Programación** xa non aparece en branco no formulario **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="f0342-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]