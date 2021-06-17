---
title: Novidades ou cambios na versión 26 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 26 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6aafe66fe8c63dc886455a36e93f32d4a581d5cc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005564"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="9e811-103">Versión 26 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="9e811-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9e811-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9e811-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9e811-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="9e811-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9e811-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9e811-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9e811-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="9e811-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9e811-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="9e811-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9e811-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 26 de actualización, V3.</span><span class="sxs-lookup"><span data-stu-id="9e811-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="9e811-110">Esta versión ten un número de compilación de V3.10.44.59 e está dispoñible xeralmente a través dunha actualización automática en decembro de 2020.</span><span class="sxs-lookup"><span data-stu-id="9e811-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="9e811-111">Versión 26 de actualización</span><span class="sxs-lookup"><span data-stu-id="9e811-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9e811-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="9e811-112">Bug fixes</span></span>

<span data-ttu-id="9e811-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="9e811-113">**Time and Expense**</span></span>

<span data-ttu-id="9e811-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9e811-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9e811-115">Os usuarios poden cambiar a tarefa nunha entrada de tempo aprobada/enviada.</span><span class="sxs-lookup"><span data-stu-id="9e811-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="9e811-116">Erro de "Referencia de obxecto non definida" ao gardar a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="9e811-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="9e811-117">A importación de entradas de tempo a partir das atribucións de recursos crea entradas de tempo cos valores de data e hora incorrectos.</span><span class="sxs-lookup"><span data-stu-id="9e811-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="9e811-118">Cando se instalan Project Service Automation e a aplicación Field Service, o botón **Novo** móstrase dúas veces na barra de comandos para as entradas de tempo na aplicación Field Service.</span><span class="sxs-lookup"><span data-stu-id="9e811-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="9e811-119">As actualizacións das celas **Permitir unidade** e **Grupo de unidades** agora funcionan na grade **Estimacións de gastos**.</span><span class="sxs-lookup"><span data-stu-id="9e811-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="9e811-120">O formulario **Actualizar edición de entrada de tempo** inclúe **Liña de tempo**.</span><span class="sxs-lookup"><span data-stu-id="9e811-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="9e811-121">A aprobación do tempo para as entradas de tempo que non sexan do proxecto bloquea o sistema cando se busca un rol de responsable de aprobación de proxecto.</span><span class="sxs-lookup"><span data-stu-id="9e811-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="9e811-122">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="9e811-122">**Resource Management**</span></span>

<span data-ttu-id="9e811-123">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9e811-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="9e811-124">Engadiuse a validación no complemento **PostProjectCreate** para comprobar se hai un requisito principal antes de crealo.</span><span class="sxs-lookup"><span data-stu-id="9e811-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="9e811-125">O formulario de creación rápida **Membro do equipo do proxecto** produce unha excepción de referencia nula se se eliminan campos do formulario.</span><span class="sxs-lookup"><span data-stu-id="9e811-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="9e811-126">Xerar requisitos para 12 horas ao longo dun ano fallará.</span><span class="sxs-lookup"><span data-stu-id="9e811-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="9e811-127">Mellorouse a excepción de referencia nula da mensaxe de erro durante a creación de requisitos de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e811-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="9e811-128">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="9e811-128">**Project Management**</span></span>

<span data-ttu-id="9e811-129">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9e811-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="9e811-130">Validación mellorada para abordar a excepción de referencia nula xerada no complemento **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="9e811-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="9e811-131">Os proxectos publicados polo complemento de escritorio Microsoft Project eliminan tarefas sen atribuír.</span><span class="sxs-lookup"><span data-stu-id="9e811-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="9e811-132">Engadiuse unha nova validación cando a referencia do proxecto dunha tarefa non é válida debido a unha excepción de referencia nula no complemento **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="9e811-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="9e811-133">A grade de membros do equipo non mostra atribucións distintas no rexistro de membros do equipo.</span><span class="sxs-lookup"><span data-stu-id="9e811-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="9e811-134">Engadíronse novas mensaxes de validación e erro debido a unha excepción de referencia nula no complemento **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="9e811-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="9e811-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9e811-135">**Sales**</span></span>

<span data-ttu-id="9e811-136">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9e811-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="9e811-137">Ao seleccionar unha liña baseada en proxecto en oferta ou contrato, o botón **Suxestión** só debería ser visible cando se selecciona unha liña baseada en produto asociada a un produto existente.</span><span class="sxs-lookup"><span data-stu-id="9e811-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="9e811-138">Separe o privilexio **Create_Product** do privilexio **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="9e811-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="9e811-139">A eliminación dunha liña de factura provoca un fallo de referencia nula en **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="9e811-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]