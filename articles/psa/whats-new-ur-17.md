---
title: Novidades ou cambios na versión 17 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 17 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006689"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="40f71-103">Versión 17 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="40f71-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="40f71-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="40f71-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="40f71-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="40f71-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="40f71-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="40f71-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="40f71-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="40f71-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="40f71-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="40f71-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="40f71-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 17 de actualización.</span><span class="sxs-lookup"><span data-stu-id="40f71-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="40f71-110">Esta versión ten un número de compilación de V3.10.6.34 e está dispoñible xeralmente a través dunha autoactualización desde marzo de 2020.</span><span class="sxs-lookup"><span data-stu-id="40f71-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="40f71-111">Versión 17 de actualización</span><span class="sxs-lookup"><span data-stu-id="40f71-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="40f71-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="40f71-112">Bug fixes</span></span>

<span data-ttu-id="40f71-113">**Xeral**</span><span class="sxs-lookup"><span data-stu-id="40f71-113">**General**</span></span>

- <span data-ttu-id="40f71-114">Corrixido: Actualizar Project Service Automation para aplicar as licenzas dos membros do equipo (a plataforma común de recursos do proxecto incluirá os metadatos de Team Member Service 3.x)</span><span class="sxs-lookup"><span data-stu-id="40f71-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="40f71-115">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="40f71-115">**Time and Expense**</span></span>

- <span data-ttu-id="40f71-116">Corrixido: Non é posible cambiar unha estimación de gastos dun prezo non cero a cero (0).</span><span class="sxs-lookup"><span data-stu-id="40f71-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="40f71-117">O cambio ignórase.</span><span class="sxs-lookup"><span data-stu-id="40f71-117">The change is ignored.</span></span>

<span data-ttu-id="40f71-118">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="40f71-118">**Project Management**</span></span>

- <span data-ttu-id="40f71-119">Corrixido: Engadiuse un control de valores nulos no nome do posto dun membro do equipo.</span><span class="sxs-lookup"><span data-stu-id="40f71-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="40f71-120">Corrixido: O campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** quedou desfasado.</span><span class="sxs-lookup"><span data-stu-id="40f71-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="40f71-121">Corrixido: A actualización de 2.x a 3.x agora xestiona contornos de esforzo baleiros nas asignacións de tarefas.</span><span class="sxs-lookup"><span data-stu-id="40f71-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="40f71-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="40f71-122">**Sales**</span></span>

- <span data-ttu-id="40f71-123">Corrixido: **Invoice.PreValidateInvoiceUpdate** agora xestiona adecuadamente o escenario de reasignar correctamente os propietarios de rexistros.</span><span class="sxs-lookup"><span data-stu-id="40f71-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="40f71-124">Corrixido: Cando a clase de transacción é **Tempo**, **UnitGroup** é non editable para todas as entidades, incluidas **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="40f71-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="40f71-125">Non obstante, **Unidade** é non editable só para **JournalLine** e **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="40f71-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]