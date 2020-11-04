---
title: Definir calendarios de recursos
description: Este tema ofrece información sobre como definir os calendarios de horas de traballo para recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075980"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="d4b44-103">Definir calendarios de recursos</span><span class="sxs-lookup"><span data-stu-id="d4b44-103">Define resource calendars</span></span>

<span data-ttu-id="d4b44-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="d4b44-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d4b44-105">Cada recurso reservable que traballa nun proxecto debe ter un calendario de horas de traballo para definir a súa dispoñibilidade.</span><span class="sxs-lookup"><span data-stu-id="d4b44-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="d4b44-106">As horas de traballo dun recurso pódense definir de dúas maneiras:</span><span class="sxs-lookup"><span data-stu-id="d4b44-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="d4b44-107">Definir regras de calendario individuais para un recurso</span><span class="sxs-lookup"><span data-stu-id="d4b44-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="d4b44-108">Aplicar un modelo de calendario existente para o recurso</span><span class="sxs-lookup"><span data-stu-id="d4b44-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="d4b44-109">Definir as horas de traballo dun recurso</span><span class="sxs-lookup"><span data-stu-id="d4b44-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="d4b44-110">No menú **Recursos** , seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="d4b44-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="d4b44-111">Na vista de grade, seleccione o **Recurso reservable** aplicable.</span><span class="sxs-lookup"><span data-stu-id="d4b44-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="d4b44-112">Na páxina **Detalles do recurso** , seleccione o separador **Horas de traballo**. Por defecto, o calendario de recursos reservables é o horario de traballo do modelo de horas de traballo por defecto definido para a organización.</span><span class="sxs-lookup"><span data-stu-id="d4b44-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="d4b44-113">Para actualizar as horas de traballo, prema co botón dereito na data de inicio da regra de calendario proposta que se definirá.</span><span class="sxs-lookup"><span data-stu-id="d4b44-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="d4b44-114">Use o menú de regras de calendario para definir unha regra de calendario para un día específico, o resto da serie ou todo o calendario.</span><span class="sxs-lookup"><span data-stu-id="d4b44-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="d4b44-115">Despois de seleccionar a opción, pode definir:</span><span class="sxs-lookup"><span data-stu-id="d4b44-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="d4b44-116">O día da semana onde se aplicarán as horas de traballo.</span><span class="sxs-lookup"><span data-stu-id="d4b44-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="d4b44-117">As horas de traballo de cada día.</span><span class="sxs-lookup"><span data-stu-id="d4b44-117">The working times within each day.</span></span>
    - <span data-ttu-id="d4b44-118">O fuso horario local da regra de calendario.</span><span class="sxs-lookup"><span data-stu-id="d4b44-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="d4b44-119">Se é o caso, tamén se pode especificar o tempo non laborable para a regra.</span><span class="sxs-lookup"><span data-stu-id="d4b44-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="d4b44-120">Aplicación dun modelo de calendario a un recurso</span><span class="sxs-lookup"><span data-stu-id="d4b44-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="d4b44-121">No menú **Recursos** , seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="d4b44-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="d4b44-122">Na vista de grade, seleccione ata 25 **Recursos reservables** para actualizar.</span><span class="sxs-lookup"><span data-stu-id="d4b44-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="d4b44-123">Seleccione **Establecer calendario** e un diálogo solicitaralle unha lista de modelos de horas de traballo dispoñibles.</span><span class="sxs-lookup"><span data-stu-id="d4b44-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="d4b44-124">Seleccione o modelo que desexe usar e, a seguir, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="d4b44-124">Select the template you want to use, and then select **Apply**.</span></span>
