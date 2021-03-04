---
title: Novidades ou cambios na versión 24 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 24 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146706"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="bcc42-103">Versión 24 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="bcc42-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bcc42-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bcc42-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bcc42-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="bcc42-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bcc42-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bcc42-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bcc42-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="bcc42-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bcc42-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="bcc42-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bcc42-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 24 de actualización.</span><span class="sxs-lookup"><span data-stu-id="bcc42-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="bcc42-110">Esta versión ten un número de compilación de V 3.10.42.43 e está dispoñible xeralmente a través dunha autoactualización desde outubro de 2020.</span><span class="sxs-lookup"><span data-stu-id="bcc42-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="bcc42-111">Versión 24 de actualización</span><span class="sxs-lookup"><span data-stu-id="bcc42-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bcc42-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="bcc42-112">Bug fixes</span></span>

<span data-ttu-id="bcc42-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bcc42-113">**Sales**</span></span>

<span data-ttu-id="bcc42-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="bcc42-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bcc42-115">Problema ao configurar a lista de prezos predefinida dos produtos.</span><span class="sxs-lookup"><span data-stu-id="bcc42-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="bcc42-116">O rendemento de gañar oferta é lento debido á copia da lista de prezos integrada e os rexistros de prezos de rol.</span><span class="sxs-lookup"><span data-stu-id="bcc42-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="bcc42-117">**Contrato de proxecto/Plataforma común de vendas** > **Elemento da liña de produtos/Cantidade da liña de pedido** redondéase automaticamente ao numero enteiro máis próximo.</span><span class="sxs-lookup"><span data-stu-id="bcc42-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="bcc42-118">Eleve os privilexios do sistema ao ler listas de prezos.</span><span class="sxs-lookup"><span data-stu-id="bcc42-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="bcc42-119">Copie os campos de enderezo do cliente **address1_freighttermscode** e **address1_shippingmethodcode** en Oferta/Pedido.</span><span class="sxs-lookup"><span data-stu-id="bcc42-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="bcc42-120">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="bcc42-120">**Time and Expense**</span></span>

<span data-ttu-id="bcc42-121">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="bcc42-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="bcc42-122">A **Grade de entrada de tempo** non admite o comportamento de tempo **Só data**.</span><span class="sxs-lookup"><span data-stu-id="bcc42-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="bcc42-123">**Entrada de tempo** non se actualiza automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bcc42-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="bcc42-124">É necesaria unha actualización manual.</span><span class="sxs-lookup"><span data-stu-id="bcc42-124">A manual refresh is required.</span></span>
- <span data-ttu-id="bcc42-125">Non se poden importar as entradas de tempo dunha atribución cando hai unha pausa (0 horas) nas atribucións dun recurso.</span><span class="sxs-lookup"><span data-stu-id="bcc42-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="bcc42-126">Cando cree unha entrada de tempo, configure o inicio igual que **data_msdyn**.</span><span class="sxs-lookup"><span data-stu-id="bcc42-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="bcc42-127">Volva activar a edición en masa para a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="bcc42-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="bcc42-128">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="bcc42-128">**Resource Management**</span></span>

<span data-ttu-id="bcc42-129">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="bcc42-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="bcc42-130">Tratar de actualizar o estado dunha reserva de entre días sen un requisito activará unha excepción de referencia nula.</span><span class="sxs-lookup"><span data-stu-id="bcc42-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="bcc42-131">Erro ao cargar a **Vista de reconciliación**.</span><span class="sxs-lookup"><span data-stu-id="bcc42-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="bcc42-132">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="bcc42-132">**Project Management**</span></span>

<span data-ttu-id="bcc42-133">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="bcc42-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="bcc42-134">No **Programa do proxecto**, ao cambiar de **Manual** a **Automático**, gardar automaticamente non se está completando.</span><span class="sxs-lookup"><span data-stu-id="bcc42-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="bcc42-135">Os custos de gastos non deben calcularse para a variación na **Grade de rastrexo de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="bcc42-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="bcc42-136">Comportamento incoherente das columnas **Etiqueta de estimacións** durante a carga fronte ao cambio do tipo **Fase de tempo**.</span><span class="sxs-lookup"><span data-stu-id="bcc42-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="bcc42-137">É posible que o custo real dun proxecto non reflicta os totais de **Datos reais**.</span><span class="sxs-lookup"><span data-stu-id="bcc42-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="bcc42-138">**Data de finalización estimada** no separador **Resumo** non coincide co **Programa WBS**.</span><span class="sxs-lookup"><span data-stu-id="bcc42-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="bcc42-139">**Actualizar as horas reais** ao cancelar sangría non funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="bcc42-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="bcc42-140">Un xestor de proxectos fóra da **BU** raíz non pode crear un proxecto.</span><span class="sxs-lookup"><span data-stu-id="bcc42-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="bcc42-141">Os cambios na tarefa ou na categoría en **Estimacións de gastos** non persisten.</span><span class="sxs-lookup"><span data-stu-id="bcc42-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="bcc42-142">**Copia do contrato** copia os programas de facturación e o estado de execución.</span><span class="sxs-lookup"><span data-stu-id="bcc42-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="bcc42-143">O botón **Actualizar datos reais** calcula incorrectamente as tarefas de resumo.</span><span class="sxs-lookup"><span data-stu-id="bcc42-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="bcc42-144">Suplemento de Microsoft Project: Corrixe un erro de referencia nula se algún membro do equipo ten unha unidade de recursos baleira.</span><span class="sxs-lookup"><span data-stu-id="bcc42-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

