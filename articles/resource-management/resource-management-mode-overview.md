---
title: Visión xeral dos modos de xestión de recursos
description: Neste tema se proporciona información sobre a funcionalidade de xestión de recursos en Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930089"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="fdd03-103">Visión xeral dos modos de xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="fdd03-103">Resource management modes overview</span></span>

<span data-ttu-id="fdd03-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="fdd03-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fdd03-105">Dynamics 365 Project Operations admite dous modos para que poida executar o fluxo de reservas global.</span><span class="sxs-lookup"><span data-stu-id="fdd03-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="fdd03-106">O modo de xestión defínese como un parámetro do proxecto e pódese modificar se o seu negocio precisa cambiar.</span><span class="sxs-lookup"><span data-stu-id="fdd03-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="fdd03-107">Modo central</span><span class="sxs-lookup"><span data-stu-id="fdd03-107">Central mode</span></span>
<span data-ttu-id="fdd03-108">Para as organizacións que centralizan a asignación de recursos a proxectos, o modo central proporciona un xeito de garantir que os xestores de proxectos poidan definir os requisitos de recursos a nivel de proxecto.</span><span class="sxs-lookup"><span data-stu-id="fdd03-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="fdd03-109">O cumprimento dos requisitos de recursos delegase nun xestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdd03-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="fdd03-110">Os xestores de proxectos poden aceptar ou rexeitar os recursos propostos polo xestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdd03-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Modo central](./media/resource-management-central.png)

<span data-ttu-id="fdd03-112">Para xestionar recursos co modo Central, consulte:</span><span class="sxs-lookup"><span data-stu-id="fdd03-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="fdd03-113">Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="fdd03-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="fdd03-114">Reservar recursos nomeados a partir de requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="fdd03-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="fdd03-115">Enviar unha solicitude de recurso</span><span class="sxs-lookup"><span data-stu-id="fdd03-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="fdd03-116">Cumprir unha solicitude de recursos</span><span class="sxs-lookup"><span data-stu-id="fdd03-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="fdd03-117">Aceptar ou rexeitar un recurso de proxecto proposto desde unha solicitude de recurso</span><span class="sxs-lookup"><span data-stu-id="fdd03-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="fdd03-118">Modo híbrido</span><span class="sxs-lookup"><span data-stu-id="fdd03-118">Hybrid mode</span></span>
<span data-ttu-id="fdd03-119">Para as organizacións que requiren flexibilidade na asignación de recursos, o modo híbrido permite tanto aos xestores de proxectos como aos xestores de recursos reservar recursos.</span><span class="sxs-lookup"><span data-stu-id="fdd03-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Modo híbrido](./media/resource-management-hybrid.png)

<span data-ttu-id="fdd03-121">Ademais do proceso de modo central admitido, consulte os seguintes temas para xestionar todos os demais fluxos de reservas admitidos no modo híbrido:</span><span class="sxs-lookup"><span data-stu-id="fdd03-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="fdd03-122">Reservar un recurso directamente para un proxecto:</span><span class="sxs-lookup"><span data-stu-id="fdd03-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="fdd03-123">Reservar recursos reservables nomeados para un equipo de proxectos e atribuír tarefas</span><span class="sxs-lookup"><span data-stu-id="fdd03-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="fdd03-124">Reservar un recursos a partir dun requisito de recursos:</span><span class="sxs-lookup"><span data-stu-id="fdd03-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="fdd03-125">Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="fdd03-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="fdd03-126">Reservar recursos nomeados a partir de requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="fdd03-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
