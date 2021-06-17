---
title: Novidades ou cambios na versión 25 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 25 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 92dd74378457cf877e8ec26eb85a7883dda97d51
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000209"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="de036-103">Novidades ou cambios na versión 25 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="de036-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="de036-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="de036-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="de036-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="de036-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="de036-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="de036-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="de036-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="de036-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="de036-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="de036-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="de036-109">Este tema mostra as funcionalidades e correccións novas ou modificadas para Project Service Automation V3, versión de actualización 25. Esta versión ten un número de compilación V 3.10.43.76 e está dispoñible xeralmente mediante unha actualización automática en outubro de 2020.</span><span class="sxs-lookup"><span data-stu-id="de036-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="de036-110">Versión 25 de actualización</span><span class="sxs-lookup"><span data-stu-id="de036-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="de036-111">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="de036-111">Bug fixes</span></span>

<span data-ttu-id="de036-112">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="de036-112">**Time and Expense**</span></span>

<span data-ttu-id="de036-113">Corrixiuse o seguinte problema:</span><span class="sxs-lookup"><span data-stu-id="de036-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="de036-114">O gráfico de entrada de tempo que mostra datos adicionais baseados nun intervalo demasiado grande que se recupera.</span><span class="sxs-lookup"><span data-stu-id="de036-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="de036-115">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="de036-115">**Resource Management**</span></span>

<span data-ttu-id="de036-116">Corrixiuse o seguinte problema:</span><span class="sxs-lookup"><span data-stu-id="de036-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="de036-117">Engadiuse o código de Package Deployer para omitir a importación de parches de Universal Resource Scheduling se xa existe un parche de versión superior.</span><span class="sxs-lookup"><span data-stu-id="de036-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="de036-118">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="de036-118">**Project Management**</span></span>

<span data-ttu-id="de036-119">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="de036-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="de036-120">Corrixíronse as discrepancias de redondeo e taxa de cambio que dan lugar a nun custo planificado incorrecto na grade de rastrexo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="de036-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="de036-121">Admite a capacidade de amosar dúas ou máis grades de reacción no formulario **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="de036-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="de036-122">Proporciona validación para abordar a posibilidade de atribuír unha tarefa máis tarde da data de finalización do calendario, o que da lugar a un erro na atribución de recursos.</span><span class="sxs-lookup"><span data-stu-id="de036-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="de036-123">Mellorouse a xestión de erros para tratar a excepción de referencia nula xerada a partir do seguinte:</span><span class="sxs-lookup"><span data-stu-id="de036-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="de036-124">Complemento **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="de036-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="de036-125">**PreValidateProjectTaskCreate** cando se crea unha tarefa de proxecto sen un proxecto asociado</span><span class="sxs-lookup"><span data-stu-id="de036-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="de036-126">Complemento **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="de036-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="de036-127">Complemento **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="de036-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="de036-128">Complemento **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="de036-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="de036-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="de036-129">**Sales**</span></span>

<span data-ttu-id="de036-130">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="de036-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="de036-131">Mellorouse a xestión de erros para tratar excepcións de referencia nula xeradas a partir de **Copiar proxecto: Xestión de recursos Axuda de estimacións**.</span><span class="sxs-lookup"><span data-stu-id="de036-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="de036-132">**Non está listo para facturar** no **Traballo pendente de facturación de tempo e material** non borra o estado de facturación.</span><span class="sxs-lookup"><span data-stu-id="de036-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="de036-133">Corrixiuse o etiquetado incorrecto dos botóns de **Prezos** do separador **Prezo de rol** e **Artigos de catálogo**.</span><span class="sxs-lookup"><span data-stu-id="de036-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]