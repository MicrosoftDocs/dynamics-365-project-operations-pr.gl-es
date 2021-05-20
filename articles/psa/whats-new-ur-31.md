---
title: Novidades ou cambios na versión 31 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 31 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945533"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="9513b-103">Novidades ou cambios na versión 31 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="9513b-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9513b-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9513b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9513b-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="9513b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9513b-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9513b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9513b-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="9513b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9513b-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="9513b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9513b-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 31 de actualización.</span><span class="sxs-lookup"><span data-stu-id="9513b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="9513b-110">Esta versión ten un número de compilación de V3.10.52.77 e está xeralmente dispoñible a través dunha actualización automática en maio de 2021.</span><span class="sxs-lookup"><span data-stu-id="9513b-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="9513b-111">Versión 31 de actualización</span><span class="sxs-lookup"><span data-stu-id="9513b-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9513b-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="9513b-112">Bug fixes</span></span>

<span data-ttu-id="9513b-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="9513b-113">**Time and Expense**</span></span>

<span data-ttu-id="9513b-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9513b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9513b-115">Os botóns de comando de control de entrada de tempo na páxina **Recurso reservable** eran confusos.</span><span class="sxs-lookup"><span data-stu-id="9513b-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="9513b-116">Xerouse unha excepción de referencia nula en **Project.SetTrackingFields** ao aprobar unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="9513b-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="9513b-117">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="9513b-117">**Resource Management**</span></span>

<span data-ttu-id="9513b-118">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9513b-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="9513b-119">**Crear membro do equipo** non mostra correctamente a configuración de metadatos da configuración de reservas para **Estado de compromiso de reserva predefinido**.</span><span class="sxs-lookup"><span data-stu-id="9513b-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="9513b-120">Ao actualizar de PSA 1.X a 3.X, o proceso de actualización falla en **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="9513b-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="9513b-121">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="9513b-121">**Sales**</span></span>

<span data-ttu-id="9513b-122">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9513b-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="9513b-123">Os ingresos reais converten as cantidades á moeda do proxecto na grade de rastrexo.</span><span class="sxs-lookup"><span data-stu-id="9513b-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="9513b-124">O valor predefinido da moeda non está claro cando se crean liñas de diario, liñas de oferta e liñas de contrato en situacións nas que a moeda base dunha organización difire da moeda do proxecto.</span><span class="sxs-lookup"><span data-stu-id="9513b-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="9513b-125">A consulta **Validación do diario de corrección pendente** non se filtra por proxecto.</span><span class="sxs-lookup"><span data-stu-id="9513b-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="9513b-126">As vendas restantes calcúlanse incorrectamente nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="9513b-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="9513b-127">As ofertas baseadas nun contacto fallan cando se crean sen unha lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="9513b-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="9513b-128">Non se mostra ningún indicador de procesamento ao seleccionar **Confirmar factura**.</span><span class="sxs-lookup"><span data-stu-id="9513b-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="9513b-129">Non se mostra ningún indicador de procesamento ao seleccionar **Crear factura**.</span><span class="sxs-lookup"><span data-stu-id="9513b-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="9513b-130">Pechar unha oferta como perdida non cancela as reservas.</span><span class="sxs-lookup"><span data-stu-id="9513b-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







