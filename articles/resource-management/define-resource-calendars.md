---
title: Definir calendarios de recursos
description: Este tema ofrece información sobre como definir os calendarios de horas de traballo para recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279811"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="81dfe-103">Definir calendarios de recursos</span><span class="sxs-lookup"><span data-stu-id="81dfe-103">Define resource calendars</span></span>

<span data-ttu-id="81dfe-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="81dfe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81dfe-105">Cada recurso reservable que traballa nun proxecto debe ter un calendario de horas de traballo para definir a súa dispoñibilidade.</span><span class="sxs-lookup"><span data-stu-id="81dfe-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="81dfe-106">As horas de traballo dun recurso pódense definir de dúas maneiras:</span><span class="sxs-lookup"><span data-stu-id="81dfe-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="81dfe-107">Definir regras de calendario individuais para un recurso</span><span class="sxs-lookup"><span data-stu-id="81dfe-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="81dfe-108">Aplicar un modelo de calendario existente para o recurso</span><span class="sxs-lookup"><span data-stu-id="81dfe-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="81dfe-109">Definir as horas de traballo dun recurso</span><span class="sxs-lookup"><span data-stu-id="81dfe-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="81dfe-110">No menú **Recursos**, seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="81dfe-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="81dfe-111">Na vista de grade, seleccione o **Recurso reservable** aplicable.</span><span class="sxs-lookup"><span data-stu-id="81dfe-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="81dfe-112">Na páxina **Detalles do recurso**, seleccione o separador **Horas de traballo**. Por defecto, o calendario de recursos reservables é o horario de traballo do modelo de horas de traballo por defecto definido para a organización.</span><span class="sxs-lookup"><span data-stu-id="81dfe-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="81dfe-113">Para actualizar as horas de traballo, prema co botón dereito na data de inicio da regra de calendario proposta que se definirá.</span><span class="sxs-lookup"><span data-stu-id="81dfe-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="81dfe-114">Use o menú de regras de calendario para definir unha regra de calendario para un día específico, o resto da serie ou todo o calendario.</span><span class="sxs-lookup"><span data-stu-id="81dfe-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="81dfe-115">Despois de seleccionar a opción, pode definir:</span><span class="sxs-lookup"><span data-stu-id="81dfe-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="81dfe-116">O día da semana onde se aplicarán as horas de traballo.</span><span class="sxs-lookup"><span data-stu-id="81dfe-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="81dfe-117">As horas de traballo de cada día.</span><span class="sxs-lookup"><span data-stu-id="81dfe-117">The working times within each day.</span></span>
    - <span data-ttu-id="81dfe-118">O fuso horario local da regra de calendario.</span><span class="sxs-lookup"><span data-stu-id="81dfe-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="81dfe-119">Se é o caso, tamén se pode especificar o tempo non laborable para a regra.</span><span class="sxs-lookup"><span data-stu-id="81dfe-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="81dfe-120">Aplicación dun modelo de calendario a un recurso</span><span class="sxs-lookup"><span data-stu-id="81dfe-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="81dfe-121">No menú **Recursos**, seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="81dfe-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="81dfe-122">Na vista de grade, seleccione ata 25 **Recursos reservables** para actualizar.</span><span class="sxs-lookup"><span data-stu-id="81dfe-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="81dfe-123">Seleccione **Establecer calendario** e un diálogo solicitaralle unha lista de modelos de horas de traballo dispoñibles.</span><span class="sxs-lookup"><span data-stu-id="81dfe-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="81dfe-124">Seleccione o modelo que desexe usar e, a seguir, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="81dfe-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]