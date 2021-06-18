---
title: Novidades ou cambios na versión 28 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 28 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010514"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="bbdd8-103">Novidades ou cambios na versión 28 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="bbdd8-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bbdd8-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bbdd8-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bbdd8-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bbdd8-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bbdd8-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="bbdd8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bbdd8-109">Este tema mostra as funcionalidades e correccións novas ou modificadas para Project Service Automation V3, versión de actualización 28. Esta versión ten un número de compilación V3.10.46.32 e está dispoñible xeralmente mediante unha actualización automática en xaneiro de 2021.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="bbdd8-110">Versión 28 de actualización</span><span class="sxs-lookup"><span data-stu-id="bbdd8-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bbdd8-111">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="bbdd8-111">Bug fixes</span></span>

<span data-ttu-id="bbdd8-112">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="bbdd8-112">**Time and Expense**</span></span>

<span data-ttu-id="bbdd8-113">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="bbdd8-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbdd8-114">Os usuarios poden utilizar **Edición en masa** para actualizar as entradas de tempo aprobadas e enviadas.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="bbdd8-115">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="bbdd8-115">**Project Management**</span></span>

<span data-ttu-id="bbdd8-116">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="bbdd8-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbdd8-117">Nos casos en que o GUID da tarefa se interpreta como un número, non se poden abrir as tarefas para editar utilizando **Editar tarefa** na fita da páxina **Estrutura de subdivisión do traballo**.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="bbdd8-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bbdd8-118">**Sales**</span></span>

<span data-ttu-id="bbdd8-119">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="bbdd8-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbdd8-120">Xérase unha excepción de referencia nula cando se invoca o complemento **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="bbdd8-121">**Marcar como listo para facturar** na grade de fitos só actualiza parcialmente os atributos, agás o atributo **InvoiceStatus**, que se actualiza.</span><span class="sxs-lookup"><span data-stu-id="bbdd8-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]