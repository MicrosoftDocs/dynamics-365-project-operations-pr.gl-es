---
title: Visión xeral do asistente de programación
description: Este tema ofrece información sobre como traballar co asistente de programación para reservar recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075988"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="ae202-103">Visión xeral do asistente de programación</span><span class="sxs-lookup"><span data-stu-id="ae202-103">Schedule assistant overview</span></span>

<span data-ttu-id="ae202-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="ae202-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae202-105">O asistente de programación utilízase para reservar recursos en función dos requisitos definidos polo xestor de proxectos.</span><span class="sxs-lookup"><span data-stu-id="ae202-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="ae202-106">O asistente de programación confía nos parámetros proporcionados no requisito de recursos para atopar o recurso.</span><span class="sxs-lookup"><span data-stu-id="ae202-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="ae202-107">O asistente de programación recomenda recursos que se axusten aos requisitos relevantes, como ventás de tempo ou habilidades necesarias.</span><span class="sxs-lookup"><span data-stu-id="ae202-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="ae202-108">Despois de identificar os recursos adecuados, o xestor de recursos ou proxectos pode reservar o recurso para o traballo.</span><span class="sxs-lookup"><span data-stu-id="ae202-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ae202-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae202-109">Prerequisites</span></span>

<span data-ttu-id="ae202-110">O asistente de programación forma parte da solución Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="ae202-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="ae202-111">Esta solución inclúese e instálase con Dynamics 365 Project Operations, Dynamics 365 Field Service e Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="ae202-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="ae202-112">Combinar requisitos e recursos</span><span class="sxs-lookup"><span data-stu-id="ae202-112">Matching requirements and resources</span></span>

<span data-ttu-id="ae202-113">Un requisito de recursos xerado baséase en detalles como:</span><span class="sxs-lookup"><span data-stu-id="ae202-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="ae202-114">Características</span><span class="sxs-lookup"><span data-stu-id="ae202-114">Characteristics</span></span>
-   <span data-ttu-id="ae202-115">Funcións</span><span class="sxs-lookup"><span data-stu-id="ae202-115">Roles</span></span>
-   <span data-ttu-id="ae202-116">Unidades empresariais</span><span class="sxs-lookup"><span data-stu-id="ae202-116">Business units</span></span>
-   <span data-ttu-id="ae202-117">Preferencias de recurso</span><span class="sxs-lookup"><span data-stu-id="ae202-117">Resource preferences</span></span>
-   <span data-ttu-id="ae202-118">Contornos de esforzo</span><span class="sxs-lookup"><span data-stu-id="ae202-118">Effort contours</span></span>
-   <span data-ttu-id="ae202-119">Fuso horario</span><span class="sxs-lookup"><span data-stu-id="ae202-119">Time zone</span></span>

<span data-ttu-id="ae202-120">O asistente de programación utiliza estes detalles para filtrar os recursos.</span><span class="sxs-lookup"><span data-stu-id="ae202-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="ae202-121">Iniciar o asistente de programación</span><span class="sxs-lookup"><span data-stu-id="ae202-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="ae202-122">Hai dous xeitos de iniciar o asistente de programación.</span><span class="sxs-lookup"><span data-stu-id="ae202-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="ae202-123">Se está a usar o modo híbrido, na grade de membros do equipo pode seleccionar calquera membro do equipo cun requisito de recurso non cumprido e logo seleccionar **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="ae202-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="ae202-124">Se está a usar o modo central, o xestor de recursos atopa e selecciona o recurso.</span><span class="sxs-lookup"><span data-stu-id="ae202-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="ae202-125">Filtros do asistente de programación</span><span class="sxs-lookup"><span data-stu-id="ae202-125">Schedule assistant filters</span></span>

<span data-ttu-id="ae202-126">Despois de executar o asistente de programación, os detalles do requisito de recursos móstranse como valores filtrados no panel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="ae202-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="ae202-127">O xestor de recursos ou o xestor de proxectos poden axustar os resultados axustando os filtros para satisfacer as necesidades de programación.</span><span class="sxs-lookup"><span data-stu-id="ae202-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="ae202-128">O panel de filtros mostra opcións relacionadas co traballo, incluídas:</span><span class="sxs-lookup"><span data-stu-id="ae202-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="ae202-129">Inicio e fin do traballo</span><span class="sxs-lookup"><span data-stu-id="ae202-129">Work start and end</span></span>
-   <span data-ttu-id="ae202-130">Características</span><span class="sxs-lookup"><span data-stu-id="ae202-130">Characteristics</span></span>
-   <span data-ttu-id="ae202-131">Funcións</span><span class="sxs-lookup"><span data-stu-id="ae202-131">Roles</span></span>
-   <span data-ttu-id="ae202-132">Unidades organizativas</span><span class="sxs-lookup"><span data-stu-id="ae202-132">Organizational units</span></span>
-   <span data-ttu-id="ae202-133">Empresa de recursos</span><span class="sxs-lookup"><span data-stu-id="ae202-133">Resourcing company</span></span>
-   <span data-ttu-id="ae202-134">Tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="ae202-134">Resource types</span></span>
-   <span data-ttu-id="ae202-135">Recursos preferidos</span><span class="sxs-lookup"><span data-stu-id="ae202-135">Preferred resources</span></span>
