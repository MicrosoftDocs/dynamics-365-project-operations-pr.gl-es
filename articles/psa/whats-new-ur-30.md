---
title: Novidades ou cambios na versión 30 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 30 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010424"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="8831e-103">Novidades ou cambios na versión 30 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="8831e-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8831e-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8831e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8831e-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="8831e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8831e-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8831e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8831e-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="8831e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8831e-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution.md)</span><span class="sxs-lookup"><span data-stu-id="8831e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="8831e-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 30 de actualización.</span><span class="sxs-lookup"><span data-stu-id="8831e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="8831e-110">Esta versión ten un número de compilación de V3.10.51.61 e está xeralmente dispoñible a través dunha actualización automática en abril de 2021.</span><span class="sxs-lookup"><span data-stu-id="8831e-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="8831e-111">Versión 30 de actualización</span><span class="sxs-lookup"><span data-stu-id="8831e-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8831e-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="8831e-112">Bug fixes</span></span>

<span data-ttu-id="8831e-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="8831e-113">**Time and Expense**</span></span>

<span data-ttu-id="8831e-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8831e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8831e-115">Prodúcese un erro ao crear e gardar unha entrada de tempo na páxina **Creación rápida** páxina se se elimina o campo **Rol**.</span><span class="sxs-lookup"><span data-stu-id="8831e-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="8831e-116">O filtro de entrada de tempo aplica un operador de filtro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="8831e-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="8831e-117">As follas de control horario copiadas non se amosan automaticamente cando selecciona **Copiar semana** no control de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="8831e-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="8831e-118">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="8831e-118">**Resource Management**</span></span>

<span data-ttu-id="8831e-119">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8831e-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="8831e-120">Cando amplía unha reserva, o estado da reserva atribuído á reserva dura é incorrecto.</span><span class="sxs-lookup"><span data-stu-id="8831e-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="8831e-121">A extensión dunha reserva respecta o estado da reserva definido como **Comprometido** nos metadatos de configuración da reserva.</span><span class="sxs-lookup"><span data-stu-id="8831e-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="8831e-122">Cando non se especifica un estado de reserva válido, a mensaxe de erro non está localizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="8831e-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="8831e-123">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="8831e-123">**Project Management**</span></span>

<span data-ttu-id="8831e-124">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8831e-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="8831e-125">Os proxectos non se poden crear nunha moeda e inclúen tarefas relacionadas noutra moeda.</span><span class="sxs-lookup"><span data-stu-id="8831e-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="8831e-126">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="8831e-126">**Sales**</span></span>

<span data-ttu-id="8831e-127">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8831e-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="8831e-128">Cando se copia unha lista de prezos, os prezos non se actualizan.</span><span class="sxs-lookup"><span data-stu-id="8831e-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="8831e-129">Pechar unha oferta como gañada falla cando o detalle do custo ten un valor para a orixe.</span><span class="sxs-lookup"><span data-stu-id="8831e-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="8831e-130">Na entidade **Tarefa de proxecto**, cambiouse o nome de **Custo estimado** a **Custo planificado (base)**.</span><span class="sxs-lookup"><span data-stu-id="8831e-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="8831e-131">Xérase unha excepción de referencia nula cando se crean ou se eliminan facturas.</span><span class="sxs-lookup"><span data-stu-id="8831e-131">A null reference exception is generated when invoices are created or deleted.</span></span>
