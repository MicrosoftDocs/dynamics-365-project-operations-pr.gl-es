---
title: Novidades ou cambios na versión 14 de actualización de Project Service Automation, V3
description: Este tema fornece información sobre as novidades e as modificacións na versión 14 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147156"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="99468-103">Versión 14 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="99468-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="99468-104">Comprácenos anunciar a última actualización para a aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="99468-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="99468-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="99468-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="99468-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="99468-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="99468-107">Para actualizar a esta versión, visite o Centro de administración para Dynamics 365 en liña e vaia á páxina de solucións para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="99468-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="99468-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="99468-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="99468-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 14 de actualización.</span><span class="sxs-lookup"><span data-stu-id="99468-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="99468-110">Esta versión ten un número de compilación de V3.10.4.21 e está dispoñible na seguinte programación:</span><span class="sxs-lookup"><span data-stu-id="99468-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="99468-111">**Dispoñibilidade xeral (autoactualización):** Xaneiro de 2020</span><span class="sxs-lookup"><span data-stu-id="99468-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="99468-112">**Autoactualización:** Febreiro de 2020</span><span class="sxs-lookup"><span data-stu-id="99468-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="99468-113">Versión 14 de actualización</span><span class="sxs-lookup"><span data-stu-id="99468-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="99468-114">Melloras</span><span class="sxs-lookup"><span data-stu-id="99468-114">Enhancements</span></span>

- <span data-ttu-id="99468-115">Sales</span><span class="sxs-lookup"><span data-stu-id="99468-115">Sales</span></span>

     - <span data-ttu-id="99468-116">Os valores de campo personalizado de **Detalles de liña de oferta** cópianse a **Detalles da liña de contrato do proxecto** cando se actualiza unha oferta a **Pechada como gañada**.</span><span class="sxs-lookup"><span data-stu-id="99468-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="99468-117">Os proxectos confirmados poden ser **Pechado como perdido**.</span><span class="sxs-lookup"><span data-stu-id="99468-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="99468-118">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="99468-118">Resource Management</span></span>

     - <span data-ttu-id="99468-119">Ao ampliar as reservas, pedirase aos usuarios cunha caixa de diálogo de confirmación que resuman os resultados da reserva e proporcionar unha ligazón a Manter reservas.</span><span class="sxs-lookup"><span data-stu-id="99468-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="99468-120">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="99468-120">Bug fixes</span></span>

- <span data-ttu-id="99468-121">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="99468-121">Time and Expense</span></span>

     - <span data-ttu-id="99468-122">Corrixido: Mellorou a experiencia do usuario cando o usuario non seleccionou ningunha entrada para corrixir.</span><span class="sxs-lookup"><span data-stu-id="99468-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="99468-123">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="99468-123">Resource Management</span></span>

     - <span data-ttu-id="99468-124">Corrixido: A reserva dun recurso en varias ocasións desborda o nome do recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="99468-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="99468-125">Sales</span><span class="sxs-lookup"><span data-stu-id="99468-125">Sales</span></span>

     - <span data-ttu-id="99468-126">Fixado: O prezo total de vendas non se calcula ata que o usuario tamén introduza un prezo de custo para estimacións de gastos nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="99468-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="99468-127">Corrixido: Pechar unha oferta como **Gañada** falla se o contrato do proxecto asociado non está nun estado de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="99468-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

