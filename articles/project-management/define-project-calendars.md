---
title: Definir calendarios de proxectos
description: Este tema ofrece información sobre como aplicar un modelo de calendario a un proxecto para rastrexar a programación do proxecto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998994"
---
# <a name="define-project-calendars"></a><span data-ttu-id="4266f-103">Definir calendarios de proxectos</span><span class="sxs-lookup"><span data-stu-id="4266f-103">Define project calendars</span></span>

<span data-ttu-id="4266f-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="4266f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4266f-105">Para crear e xestionar un proxecto, debe aplicarlle un modelo de calendario.</span><span class="sxs-lookup"><span data-stu-id="4266f-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="4266f-106">O modelo de calendario define os seguintes atributos do proxecto:</span><span class="sxs-lookup"><span data-stu-id="4266f-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="4266f-107">Horas de traballo, incluídas as horas de inicio e fin</span><span class="sxs-lookup"><span data-stu-id="4266f-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="4266f-108">Días laborables</span><span class="sxs-lookup"><span data-stu-id="4266f-108">Working days</span></span>
- <span data-ttu-id="4266f-109">Excepcións do calendario como días non laborables</span><span class="sxs-lookup"><span data-stu-id="4266f-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="4266f-110">O modelo de calendario que se aplica a un proxecto é unha copia do modelo de calendario definido na configuración da súa organización.</span><span class="sxs-lookup"><span data-stu-id="4266f-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="4266f-111">Se cambia o modelo de calendario, eses cambios non se propagarán ás horas de traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="4266f-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="4266f-112">Para cambiar as horas de traballo do proxecto, hai que aplicar un novo modelo.</span><span class="sxs-lookup"><span data-stu-id="4266f-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="4266f-113">Para crear un modelo de calendario para a súa organización, hai dous requisitos clave:</span><span class="sxs-lookup"><span data-stu-id="4266f-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="4266f-114">Defina as horas de traballo desexadas do modelo empregando un recurso reservable novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="4266f-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="4266f-115">Cree un novo modelo de calendario e asocie o modelo ao recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="4266f-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="4266f-116">**Definir as horas de traballo do modelo**</span><span class="sxs-lookup"><span data-stu-id="4266f-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="4266f-117">Vaia a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="4266f-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="4266f-118">Cree un novo recurso para facer referencia a el no modelo de calendario ou seleccione un recurso existente.</span><span class="sxs-lookup"><span data-stu-id="4266f-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="4266f-119">Seleccione o separador **Horas de traballo** do recurso e siga as instrucións de [Establecer horas de traballo para un recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar as regras do calendario.</span><span class="sxs-lookup"><span data-stu-id="4266f-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="4266f-120">**Crear un novo modelo de calendario**</span><span class="sxs-lookup"><span data-stu-id="4266f-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="4266f-121">Vaia a **Configuración** \> **Modelo de calendario**.</span><span class="sxs-lookup"><span data-stu-id="4266f-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="4266f-122">Seleccione **Novo** e introduza un nome, unha descrición e un recurso do modelo.</span><span class="sxs-lookup"><span data-stu-id="4266f-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="4266f-123">Cando se fai referencia a un recurso nun modelo de calendario, asóciase unha copia do calendario do recurso ao modelo de calendario.</span><span class="sxs-lookup"><span data-stu-id="4266f-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="4266f-124">Se cambian as horas de traballo do modelo copiado, eses cambios non se propagarán ao modelo de calendario.</span><span class="sxs-lookup"><span data-stu-id="4266f-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="4266f-125">Agora pode asociar o modelo de traballo a un modelo de calendario de proxecto.</span><span class="sxs-lookup"><span data-stu-id="4266f-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

