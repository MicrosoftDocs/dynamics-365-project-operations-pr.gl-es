---
title: Crear un modelo de horas laborables
description: Este tema describe como crear un modelo de horas laborables en Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997194"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="d892a-103">Crear un modelo de horas laborables (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d892a-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d892a-104">Para crear e xestionar un proxecto, debe aplicarlle un modelo de calendario.</span><span class="sxs-lookup"><span data-stu-id="d892a-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="d892a-105">O modelo de calendario define os seguintes atributos do proxecto:</span><span class="sxs-lookup"><span data-stu-id="d892a-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="d892a-106">Horas de traballo, incluídas as horas de inicio e fin</span><span class="sxs-lookup"><span data-stu-id="d892a-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="d892a-107">Días laborables</span><span class="sxs-lookup"><span data-stu-id="d892a-107">Working days</span></span>
- <span data-ttu-id="d892a-108">Excepcións do calendario como días non laborables</span><span class="sxs-lookup"><span data-stu-id="d892a-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="d892a-109">O modelo de calendario que se aplica a un proxecto é unha copia do modelo de calendario definido na configuración da súa organización.</span><span class="sxs-lookup"><span data-stu-id="d892a-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d892a-110">Se cambia o modelo de calendario, eses cambios non se propagarán ás horas de traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="d892a-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="d892a-111">Para cambiar as horas de traballo do proxecto, hai que aplicar un novo modelo.</span><span class="sxs-lookup"><span data-stu-id="d892a-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="d892a-112">Para crear un modelo de calendario para a súa organización, hai dous requisitos clave:</span><span class="sxs-lookup"><span data-stu-id="d892a-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="d892a-113">Defina as horas de traballo desexadas do modelo empregando un recurso reservable novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="d892a-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="d892a-114">Cree un novo modelo de calendario e asocie o modelo ao recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="d892a-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="d892a-115">**Definir as horas de traballo do modelo**</span><span class="sxs-lookup"><span data-stu-id="d892a-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="d892a-116">Vaia a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="d892a-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="d892a-117">Cree un novo recurso para facer referencia a el no modelo de calendario ou seleccione un recurso existente.</span><span class="sxs-lookup"><span data-stu-id="d892a-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="d892a-118">Seleccione o separador **Horas de traballo** do recurso e siga as instrucións de [Establecer horas de traballo para un recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar as regras do calendario.</span><span class="sxs-lookup"><span data-stu-id="d892a-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="d892a-119">**Crear un novo modelo de calendario**</span><span class="sxs-lookup"><span data-stu-id="d892a-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="d892a-120">Vaia a **Configuración** \> **Modelo de calendario**.</span><span class="sxs-lookup"><span data-stu-id="d892a-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="d892a-121">Seleccione **Novo** e introduza un nome, unha descrición e un recurso do modelo.</span><span class="sxs-lookup"><span data-stu-id="d892a-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="d892a-122">Cando se fai referencia a un recurso nun modelo de calendario, asóciase unha copia do calendario do recurso ao modelo de calendario.</span><span class="sxs-lookup"><span data-stu-id="d892a-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="d892a-123">Se cambian as horas de traballo do modelo copiado, eses cambios non se propagarán ao modelo de calendario.</span><span class="sxs-lookup"><span data-stu-id="d892a-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="d892a-124">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="d892a-124">See Also</span></span>  
 [<span data-ttu-id="d892a-125">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="d892a-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
