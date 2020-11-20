---
title: Novidades ou cambios na versión 22 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 22 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126616"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="57959-103">Versión 22 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="57959-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="57959-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="57959-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="57959-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="57959-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="57959-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="57959-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="57959-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="57959-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="57959-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="57959-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="57959-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 22 de actualización.</span><span class="sxs-lookup"><span data-stu-id="57959-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="57959-110">Esta versión ten un número de compilación de V 3.10.33.48 e está xeralmente dispoñible a través dunha actualización automática en xuño de 2020.</span><span class="sxs-lookup"><span data-stu-id="57959-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="57959-111">Versión 22 de actualización</span><span class="sxs-lookup"><span data-stu-id="57959-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="57959-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="57959-112">Bug fixes</span></span>



<span data-ttu-id="57959-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="57959-113">**Time and Expense**</span></span>

<span data-ttu-id="57959-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="57959-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="57959-115">As **Entradas de tempo** non se engaden automaticamente na programación de entradas de tempo despois da importación.</span><span class="sxs-lookup"><span data-stu-id="57959-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="57959-116">O selector de datas da grade **Entrada de tempo** non recoñece a configuración rexional dun usuario.</span><span class="sxs-lookup"><span data-stu-id="57959-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="57959-117">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="57959-117">**Resource Management**</span></span>

<span data-ttu-id="57959-118">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="57959-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="57959-119">No modo manual, os cambios nos contornos de **Atribución do recurso** non se recoñecen ao xerar **Requisitos do recurso**.</span><span class="sxs-lookup"><span data-stu-id="57959-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="57959-120">**Solicitudes de recursos** non admite estados de solicitude personalizados.</span><span class="sxs-lookup"><span data-stu-id="57959-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="57959-121">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="57959-121">**Project Management**</span></span>

<span data-ttu-id="57959-122">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="57959-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="57959-123">Ao premer dúas veces en EstimateGridControl non se analizarán correctamente os números do formato holandés.</span><span class="sxs-lookup"><span data-stu-id="57959-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="57959-124">As horas atribuídas non se actualizan correctamente cando as tarefas se cambian mediante o complemento de cliente de escritorio de Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="57959-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="57959-125">As grades de rastrexo e estimacións de proxectos mostran un código de moeda de vendas incorrecto cando a moeda do contrato é diferente da moeda do cliente e a organización está configurada para mostrar códigos de moeda en lugar de símbolos de moeda.</span><span class="sxs-lookup"><span data-stu-id="57959-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="57959-126">A data de finalización dun membro do equipo engadirá un día se o horario de traballo é de 24 horas ao día.</span><span class="sxs-lookup"><span data-stu-id="57959-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="57959-127">Na programación do proxecto, ao engadir unha categoría de transacción a unha tarefa non se activa o aforro automático.</span><span class="sxs-lookup"><span data-stu-id="57959-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="57959-128">Aparece o seguinte erro ao engadir un membro do equipo ao modelo do proxecto: "Non se poden asociar requisitos de recursos aos modelos de proxecto".</span><span class="sxs-lookup"><span data-stu-id="57959-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="57959-129">O script de regra de fita "msdyn.Approval.CanApproveOrReject" mostra un erro de tempo de espera.</span><span class="sxs-lookup"><span data-stu-id="57959-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="57959-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="57959-130">**Sales**</span></span>

<span data-ttu-id="57959-131">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="57959-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="57959-132">A mensaxe de erro de validación non se mostra cando se selecciona unha Lista de prezos de custo na busca de Lista de prezos no formulario/entidade "Lista de prezos de proxecto de nova oferta".</span><span class="sxs-lookup"><span data-stu-id="57959-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="57959-133">O peche do presuposto como gañado non navega ata o contrato creado se un BPF anexado á oferta está na fase final.</span><span class="sxs-lookup"><span data-stu-id="57959-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="57959-134">A inversión de **Vendas sen facturar** está ligada ao custo orixinal cando se recupera unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="57959-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="57959-135">Despois de seleccionar o botón **Confirmar**, o estado da factura non cambia a **Confirmada** a menos que se actualice a factura.</span><span class="sxs-lookup"><span data-stu-id="57959-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
