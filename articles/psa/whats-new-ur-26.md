---
title: Novidades ou cambios na versión 26 de actualización de Project Service Automation, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643261"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="8e8df-102">Versión 26 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="8e8df-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="8e8df-103">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8e8df-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8e8df-104">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="8e8df-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8e8df-105">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8e8df-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8e8df-106">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="8e8df-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8e8df-107">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="8e8df-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8e8df-108">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 26 de actualización, V3.</span><span class="sxs-lookup"><span data-stu-id="8e8df-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="8e8df-109">Esta versión ten un número de compilación de V3.10.44.59 e está dispoñible xeralmente a través dunha actualización automática en decembro de 2020.</span><span class="sxs-lookup"><span data-stu-id="8e8df-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="8e8df-110">Versión 26 de actualización</span><span class="sxs-lookup"><span data-stu-id="8e8df-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="8e8df-111">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="8e8df-111">Bug fixes</span></span>

<span data-ttu-id="8e8df-112">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="8e8df-112">**Time and Expense**</span></span>

<span data-ttu-id="8e8df-113">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8e8df-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="8e8df-114">Os usuarios poden cambiar a tarefa nunha entrada de tempo aprobada/enviada.</span><span class="sxs-lookup"><span data-stu-id="8e8df-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="8e8df-115">Erro de "Referencia de obxecto non definida" ao gardar a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="8e8df-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="8e8df-116">A importación de entradas de tempo a partir das atribucións de recursos crea entradas de tempo cos valores de data e hora incorrectos.</span><span class="sxs-lookup"><span data-stu-id="8e8df-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="8e8df-117">Cando se instalan Project Service Automation e a aplicación Field Service, o botón **Novo** móstrase dúas veces na barra de comandos para as entradas de tempo na aplicación Field Service.</span><span class="sxs-lookup"><span data-stu-id="8e8df-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="8e8df-118">As actualizacións das celas **Permitir unidade** e **Grupo de unidades** agora funcionan na grade **Estimacións de gastos**.</span><span class="sxs-lookup"><span data-stu-id="8e8df-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="8e8df-119">O formulario **Actualizar edición de entrada de tempo** inclúe **Liña de tempo**.</span><span class="sxs-lookup"><span data-stu-id="8e8df-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="8e8df-120">A aprobación do tempo para as entradas de tempo que non sexan do proxecto bloquea o sistema cando se busca un rol de responsable de aprobación de proxecto.</span><span class="sxs-lookup"><span data-stu-id="8e8df-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="8e8df-121">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="8e8df-121">**Resource Management**</span></span>

<span data-ttu-id="8e8df-122">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8e8df-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="8e8df-123">Engadiuse a validación no complemento **PostProjectCreate** para comprobar se hai un requisito principal antes de crealo.</span><span class="sxs-lookup"><span data-stu-id="8e8df-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="8e8df-124">O formulario de creación rápida **Membro do equipo do proxecto** produce unha excepción de referencia nula se se eliminan campos do formulario.</span><span class="sxs-lookup"><span data-stu-id="8e8df-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="8e8df-125">Xerar requisitos para 12 horas ao longo dun ano fallará.</span><span class="sxs-lookup"><span data-stu-id="8e8df-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="8e8df-126">Mellorouse a excepción de referencia nula da mensaxe de erro durante a creación de requisitos de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e8df-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="8e8df-127">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="8e8df-127">**Project Management**</span></span>

<span data-ttu-id="8e8df-128">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8e8df-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="8e8df-129">Validación mellorada para abordar a excepción de referencia nula xerada no complemento **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="8e8df-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="8e8df-130">Os proxectos publicados polo complemento de escritorio Microsoft Project eliminan tarefas sen atribuír.</span><span class="sxs-lookup"><span data-stu-id="8e8df-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="8e8df-131">Engadiuse unha nova validación cando a referencia do proxecto dunha tarefa non é válida debido a unha excepción de referencia nula no complemento **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="8e8df-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="8e8df-132">A grade de membros do equipo non mostra atribucións distintas no rexistro de membros do equipo.</span><span class="sxs-lookup"><span data-stu-id="8e8df-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="8e8df-133">Engadíronse novas mensaxes de validación e erro debido a unha excepción de referencia nula no complemento **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="8e8df-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="8e8df-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8e8df-134">**Sales**</span></span>

<span data-ttu-id="8e8df-135">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8e8df-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="8e8df-136">Ao seleccionar unha liña baseada en proxecto en oferta ou contrato, o botón **Suxestión** só debería ser visible cando se selecciona unha liña baseada en produto asociada a un produto existente.</span><span class="sxs-lookup"><span data-stu-id="8e8df-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="8e8df-137">Separe o privilexio **Create_Product** do privilexio **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="8e8df-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="8e8df-138">A eliminación dunha liña de factura provoca un fallo de referencia nula en **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="8e8df-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
