---
title: Novidades na versión 16 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 16 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751382"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="e40d8-103">Project Service Automation V3, versión 16 de actualización</span><span class="sxs-lookup"><span data-stu-id="e40d8-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="e40d8-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e40d8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e40d8-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="e40d8-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="e40d8-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e40d8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e40d8-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="e40d8-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="e40d8-108">Para obter máis información, consulte [Instalar e actualizar unha solución preferida](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page)</span><span class="sxs-lookup"><span data-stu-id="e40d8-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="e40d8-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 16 de actualización.</span><span class="sxs-lookup"><span data-stu-id="e40d8-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="e40d8-110">Esta versión ten un número de compilación de V3.10.6.34 e está dispoñible xeralmente a través dunha autoactualización desde xaneiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e40d8-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="e40d8-111">Versión 16 de actualización</span><span class="sxs-lookup"><span data-stu-id="e40d8-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e40d8-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="e40d8-112">Bug fixes</span></span>

-   <span data-ttu-id="e40d8-113">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="e40d8-113">Time and Expense</span></span>

    -   <span data-ttu-id="e40d8-114">Corrixido: Os usuarios que tentan enviar as entradas de tempo e gasto eliminadas para aprobacións recibirán agora os mensaxes de erro correspondentes.</span><span class="sxs-lookup"><span data-stu-id="e40d8-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="e40d8-115">Xestión de proxectos</span><span class="sxs-lookup"><span data-stu-id="e40d8-115">Project Management</span></span>

    -   <span data-ttu-id="e40d8-116">Corrixido: As unidades de recursos definidas para os membros do equipo nos modelos respéctanse e os modelos aplícanse a un novo proxecto.</span><span class="sxs-lookup"><span data-stu-id="e40d8-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="e40d8-117">Corrixido: Mellora da xestión da reasignación da propiedade de rexistros.</span><span class="sxs-lookup"><span data-stu-id="e40d8-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="e40d8-118">Corrixido: Os proxectos que están en proceso de copiarse non poderán copiarse ata que todas as operacións de copia estean rematadas.</span><span class="sxs-lookup"><span data-stu-id="e40d8-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="e40d8-119">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="e40d8-119">Resource Management</span></span>

    -   <span data-ttu-id="e40d8-120">Corrixido: Estender reservas agora xestiona correctamente as duracións curtas e xa non crea cero horas para as reservas estendidas.</span><span class="sxs-lookup"><span data-stu-id="e40d8-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="e40d8-121">Corrixido: A vista de reconciliación agora mostra cando a zona horaria do proxecto é +5:30 GMT e a hora do usuario é diferente.</span><span class="sxs-lookup"><span data-stu-id="e40d8-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="e40d8-122">Sales</span><span class="sxs-lookup"><span data-stu-id="e40d8-122">Sales</span></span>

    -   <span data-ttu-id="e40d8-123">Corrixido: Cando se elimina un proxecto asignado a unha liña de contrato e se asigna un novo proxecto, os rexistros reais do novo proxecto non se avaliaban de novo segundo as regras de facturación e prezos definidas na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="e40d8-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="e40d8-124">Isto corrixiuse nesta versión.</span><span class="sxs-lookup"><span data-stu-id="e40d8-124">This has been fixed in this release.</span></span> <span data-ttu-id="e40d8-125">Os prezos e os rexistros reais do proxecto recentemente asignado reverteranse e crearanse de novo correctamente segundo as regras de prezos e facturación da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="e40d8-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="e40d8-126">Como consecuencia, os rexistros reais do proxecto non asignado avaliaranse e crearanse de novo.</span><span class="sxs-lookup"><span data-stu-id="e40d8-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="e40d8-127">Corrixido: Engadiuse a validación adicional a un campo **Importe** da liña de estimación para asegurarse de que os valores nulos non persisten.</span><span class="sxs-lookup"><span data-stu-id="e40d8-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="e40d8-128">Corrixido: Cando se actualizaron os datos reais nun proxecto, engadiuse un botón de actualización ao formulario principal do proxecto para permitir aos usuarios sincronizar de novo os datos reais.</span><span class="sxs-lookup"><span data-stu-id="e40d8-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="e40d8-129">Corrixido: Cando os usuarios actualicen de 2.X a 3.X, permitiránse proxectos cun valor NULL para o nome do proxecto.</span><span class="sxs-lookup"><span data-stu-id="e40d8-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

