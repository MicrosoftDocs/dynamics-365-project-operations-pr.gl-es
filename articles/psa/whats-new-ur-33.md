---
title: Novidades ou cambios na versión 33 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 33 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334536"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="fcc91-103">Novidades ou cambios na versión 33 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="fcc91-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fcc91-104">Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fcc91-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="fcc91-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="fcc91-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fcc91-106">É compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fcc91-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fcc91-107">Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización.</span><span class="sxs-lookup"><span data-stu-id="fcc91-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="fcc91-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="fcc91-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fcc91-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 33 de actualización.</span><span class="sxs-lookup"><span data-stu-id="fcc91-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="fcc91-110">Esta versión ten un número de compilación de V3.10.54.98 e está xeralmente dispoñible a través dunha actualización automática en xullo de 2021.</span><span class="sxs-lookup"><span data-stu-id="fcc91-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="fcc91-111">Versión 33 de actualización</span><span class="sxs-lookup"><span data-stu-id="fcc91-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fcc91-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="fcc91-112">Bug fixes</span></span>

<span data-ttu-id="fcc91-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="fcc91-113">**Time and Expense**</span></span>

<span data-ttu-id="fcc91-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="fcc91-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="fcc91-115">Dous campos bloqueados, **msdyn_description** e **msdyn_externaldescription** pódense editar despois do envío.</span><span class="sxs-lookup"><span data-stu-id="fcc91-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="fcc91-116">Prodúcese unha mensaxe de erro se se crea un gasto que non está relacionado cun proxecto.</span><span class="sxs-lookup"><span data-stu-id="fcc91-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="fcc91-117">Cando se crea unha entrada de tempo, o rol de recurso predeterminado é un rol inactivo.</span><span class="sxs-lookup"><span data-stu-id="fcc91-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="fcc91-118">As liñas de diario asociadas a un gasto recuperado e eliminado non se eliminan.</span><span class="sxs-lookup"><span data-stu-id="fcc91-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="fcc91-119">No **Formulario de creación rápida de entrada de tempo**, actualice a vista **Lista de tarefas do proxecto** para cambiar a data mostrada por defecto á data de inicio da tarefa.</span><span class="sxs-lookup"><span data-stu-id="fcc91-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="fcc91-120">Cando crea unha entrada de tempo desde o separador **Relacionado** do recurso reservable, a entrada de tempo créase incorrectamente para o usuario que iniciou sesión no canto do recurso reservable principal.</span><span class="sxs-lookup"><span data-stu-id="fcc91-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="fcc91-121">Engádense novos campos á caixa de diálogo **MDD de aprobacións en masa**.</span><span class="sxs-lookup"><span data-stu-id="fcc91-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="fcc91-122">**Planificación de proxectos**</span><span class="sxs-lookup"><span data-stu-id="fcc91-122">**Project planning**</span></span>

<span data-ttu-id="fcc91-123">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="fcc91-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="fcc91-124">Rendemento lento da creación de proxectos cando os modelos de hora de traballo do proxecto se aplican con calendarios complexos.</span><span class="sxs-lookup"><span data-stu-id="fcc91-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="fcc91-125">Cando a data de inicio é maior que a data de finalización, amósase un erro no modelo de copia de proxecto debido ás diferenzas no compoñente de tempo de cada campo.</span><span class="sxs-lookup"><span data-stu-id="fcc91-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="fcc91-126">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="fcc91-126">**Resource management**</span></span>

<span data-ttu-id="fcc91-127">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="fcc91-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="fcc91-128">Utilízase un parámetro incorrecto na consulta de utilización de recursos e o XML dá lugar a resultados de filtros incorrectos na grade **Utilización de recursos**.</span><span class="sxs-lookup"><span data-stu-id="fcc91-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="fcc91-129">A confirmación de **Estender reservas** mostra a data de finalización incorrecta das reservas.</span><span class="sxs-lookup"><span data-stu-id="fcc91-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="fcc91-130">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="fcc91-130">**Sales**</span></span>

<span data-ttu-id="fcc91-131">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="fcc91-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="fcc91-132">Aparecerá unha mensaxe de erro se se crea un prezo de categoría con valores que faltan.</span><span class="sxs-lookup"><span data-stu-id="fcc91-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="fcc91-133">Prodúcese unha mensaxe de erro se se crea un fito da liña de contrato sen unha liña de pedido.</span><span class="sxs-lookup"><span data-stu-id="fcc91-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
