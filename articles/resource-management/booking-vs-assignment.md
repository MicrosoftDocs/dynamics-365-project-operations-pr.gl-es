---
title: Reservas fronte a atribucións
description: Este tema ofrece información sobre as diferenzas entre as reservas de recursos e as atribucións de recursos.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012764"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="ff355-103">Reservas fronte a atribucións</span><span class="sxs-lookup"><span data-stu-id="ff355-103">Bookings vs assignments</span></span>

<span data-ttu-id="ff355-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="ff355-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ff355-105">As reservas son a atribución branda o dura de recursos a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="ff355-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="ff355-106">As reservas duras consumen a capacidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="ff355-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="ff355-107">As reservas representan conceptos organizativos para os equipos para que poidan comprender como se utilizarán os recursos en varios proxectos.</span><span class="sxs-lookup"><span data-stu-id="ff355-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="ff355-108">Dynamics 365 Project Operations considera que as reservas son un concepto a nivel de proxecto.</span><span class="sxs-lookup"><span data-stu-id="ff355-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="ff355-109">A diferenza das reservas, as atribucións son o compromiso de recursos para as tarefas do proxecto na programación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="ff355-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="ff355-110">Os recursos poden ser nomeados ou xenéricos.</span><span class="sxs-lookup"><span data-stu-id="ff355-110">The resources can be named or generic.</span></span>  <span data-ttu-id="ff355-111">Cando se deriva un requisito de recurso das atribucións de tarefas do proxecto, Project Operations utiliza os contornos de esforzo da atribución de recursos para construír os contornos dos detalles do requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="ff355-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="ff355-112">Non obstante, non se mantén a referencia ás atribucións de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff355-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="ff355-113">As actualizacións das reservas derivadas do requisito de recurso non actualizan ningunha atribución de recurso.</span><span class="sxs-lookup"><span data-stu-id="ff355-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="ff355-114">Normalmente, a suma das reservas dun recurso igualará a suma das atribucións do recurso nunha ou varias tarefas.</span><span class="sxs-lookup"><span data-stu-id="ff355-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="ff355-115">Non obstante, Project Operations non fai cumprir este acordo.</span><span class="sxs-lookup"><span data-stu-id="ff355-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="ff355-116">A vista **Conciliación** mostra ao xestor de proxectos lugares onde as reservas e atribucións dun recurso non coinciden.</span><span class="sxs-lookup"><span data-stu-id="ff355-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]