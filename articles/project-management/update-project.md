---
title: Actualizar un proxecto
description: Neste tema se proporciona información sobre actualizar proxectos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286381"
---
# <a name="update-a-project"></a><span data-ttu-id="1faed-103">Actualizar un proxecto</span><span class="sxs-lookup"><span data-stu-id="1faed-103">Update a project</span></span>

<span data-ttu-id="1faed-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1faed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1faed-105">Abaixo amósase un resumo dos campos que se poden actualizar nun proxecto despois de que se creou e as consecuencias aplicables das actualizacións.</span><span class="sxs-lookup"><span data-stu-id="1faed-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="1faed-106">Campos de detalle do proxecto</span><span class="sxs-lookup"><span data-stu-id="1faed-106">Project detail fields</span></span>

- <span data-ttu-id="1faed-107">**Nome**: O título do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="1faed-108">**Descrición**: Unha visión xeral do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="1faed-109">**Cliente**: A empresa á que se entregará o proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="1faed-110">**Modelo de calendario**: As horas de traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="1faed-111">Cando se cambia o campo, recalculase toda a programación.</span><span class="sxs-lookup"><span data-stu-id="1faed-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="1faed-112">**Moeda**: A moeda para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="1faed-113">Este campo é por defecto a moeda definida na unidade de contratación.</span><span class="sxs-lookup"><span data-stu-id="1faed-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="1faed-114">Cando se actualiza a unidade de contratación, tamén se actualiza o campo.</span><span class="sxs-lookup"><span data-stu-id="1faed-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="1faed-115">**Unidade de contratación**: A unidade organizativa que representa ao grupo ou división da empresa que é o principal responsable de gañar a venda e xestionar a entrega de traballos e servizos ao cliente.</span><span class="sxs-lookup"><span data-stu-id="1faed-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="1faed-116">**Xestor de proxectos**: O membro do equipo do proxecto que ten a autoridade para revisar e aprobar as entradas de tempo e os gastos.</span><span class="sxs-lookup"><span data-stu-id="1faed-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="1faed-117">Estimar campos</span><span class="sxs-lookup"><span data-stu-id="1faed-117">Estimate fields</span></span>

- <span data-ttu-id="1faed-118">**Data de inicio estimada**: A data na que comezará o proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="1faed-119">Cando se actualiza este campo, as tarefas do proxecto moveranse proporcionalmente coa nova data de inicio.</span><span class="sxs-lookup"><span data-stu-id="1faed-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="1faed-120">**Data de finalización**: A data na que está previsto que remate o proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="1faed-121">**Esforzo**: O esforzo estimado do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="1faed-122">Cando se engaden tarefas ao proxecto, este campo xa non se pode editar.</span><span class="sxs-lookup"><span data-stu-id="1faed-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="1faed-123">**Custo laboral estimado**: O custo laboral estimado do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="1faed-124">Cando se engaden custos laborais ao proxecto, este campo xa non se pode editar.</span><span class="sxs-lookup"><span data-stu-id="1faed-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="1faed-125">**Gastos estimados**: Os gastos estimados do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="1faed-126">Cando se engaden gastos ao proxecto, este campo xa non se pode editar.</span><span class="sxs-lookup"><span data-stu-id="1faed-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="1faed-127">Campos reais do proxecto</span><span class="sxs-lookup"><span data-stu-id="1faed-127">Project actual fields</span></span>
- <span data-ttu-id="1faed-128">**Inicio real**: A data de inicio do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="1faed-129">**Final real**: Actualizarase cando se complete un proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="1faed-130">Campos de estado do proxecto</span><span class="sxs-lookup"><span data-stu-id="1faed-130">Project status fields</span></span>

- <span data-ttu-id="1faed-131">**Estado xeral do proxecto**: A saúde xeral do proxecto proporcionada polo xestor do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="1faed-132">**Comentarios**: Unha narración sobre a saúde actual do proxecto proporcionada polo xestor do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1faed-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]