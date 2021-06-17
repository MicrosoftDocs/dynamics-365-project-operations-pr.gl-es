---
title: Crear entradas de tempo
description: Este tema fornece información sobre como crear entradas de tempo.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999264"
---
# <a name="create-time-entries"></a><span data-ttu-id="35a9d-103">Crear entradas de tempo</span><span class="sxs-lookup"><span data-stu-id="35a9d-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="35a9d-104">En versións anteriores de Dynamics 365 Project Service Automation, as entradas de tempo introducíanse semanalmente.</span><span class="sxs-lookup"><span data-stu-id="35a9d-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="35a9d-105">Na versión 3 de Project Service Automation, as entradas de tempo introdúcense diariamente.</span><span class="sxs-lookup"><span data-stu-id="35a9d-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="35a9d-106">Non obstante, despois de crear unhas poucas entradas, pode crealas ou copialas en masa.</span><span class="sxs-lookup"><span data-stu-id="35a9d-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="35a9d-107">Crear unha entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="35a9d-107">Create a time entry</span></span>

<span data-ttu-id="35a9d-108">Siga estes pasos para crear unha entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="35a9d-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="35a9d-109">Na páxina **Entradas de tempo**, seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="35a9d-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="35a9d-110">Na caixa de diálogo **Creación rápida: entrada de tempo**, introduza a duración da entrada de tempo en minutos, horas ou días.</span><span class="sxs-lookup"><span data-stu-id="35a9d-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="35a9d-111">A duración debe introducirse co seguinte formato: *x* minutos, *x* horas ou *x* días.</span><span class="sxs-lookup"><span data-stu-id="35a9d-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="35a9d-112">Horas e días tamén poden introducirse como valores decimais, por exemplo *x.x* horas ou *x.x* días.</span><span class="sxs-lookup"><span data-stu-id="35a9d-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="35a9d-113">Seleccione o tipo de entrada de tempo e o proxecto para o que está a introducir a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="35a9d-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="35a9d-114">No campo **Tarefa de proxecto**, busque a tarefa para esta entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="35a9d-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="35a9d-115">Se está a crear unha entrada de tempo para unha tarefa que non está asignada a un usuario, no campo **Tarefa de proxecto**, seleccione o botón **Buscar**, seleccione **Cambiar vista** e, a seguir, seleccione **Todas as tarefas activas do proxecto** para facer unha lista de todas as tarefas.</span><span class="sxs-lookup"><span data-stu-id="35a9d-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="35a9d-116">Introduza unha descrición, se é necesaria unha descrición, e seleccione **Gardar e pechar**.</span><span class="sxs-lookup"><span data-stu-id="35a9d-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="35a9d-117">Despois de que se cree e garde a entrada de tempo, pode editala na grade de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="35a9d-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="35a9d-118">A grade de entrada de tempo admite dous formatos:</span><span class="sxs-lookup"><span data-stu-id="35a9d-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="35a9d-119">Pode introducir as entradas de temo no formato **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="35a9d-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="35a9d-120">Este formato convértese en horas e fraccións.</span><span class="sxs-lookup"><span data-stu-id="35a9d-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="35a9d-121">Pode introducir horas e fraccións directamente.</span><span class="sxs-lookup"><span data-stu-id="35a9d-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="35a9d-122">Teña en conta que as fraccións dunha hora non son minutos.</span><span class="sxs-lookup"><span data-stu-id="35a9d-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="35a9d-123">Polo tanto, 1,5 horas representa 1 hora e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="35a9d-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="35a9d-124">A mesma regra aplícase ás fraccións dun día.</span><span class="sxs-lookup"><span data-stu-id="35a9d-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="35a9d-125">Un día é de 24 horas e 0,5 días representa 12 horas.</span><span class="sxs-lookup"><span data-stu-id="35a9d-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="35a9d-126">Creación de entradas de tempo en masa</span><span class="sxs-lookup"><span data-stu-id="35a9d-126">Bulk create time entries</span></span>

<span data-ttu-id="35a9d-127">Despois de crear unhas poucas entradas de tempo, pode copialas para crear entradas de tempo adicionais en masa.</span><span class="sxs-lookup"><span data-stu-id="35a9d-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="35a9d-128">Na páxina **Entradas de tempo**, seleccione **Copiar semana**.</span><span class="sxs-lookup"><span data-stu-id="35a9d-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="35a9d-129">No grupo de campos **Período desde**, nos campos **Data de inicio** e **Data de finalización**, defina o intervalo de datas do que vai copiar as entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="35a9d-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="35a9d-130">No grupo de campos **Período ata**, no campo **Data de inicio**, especifique a data para a que se van crear as entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="35a9d-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="35a9d-131">Seleccione **Copiar** para crear unha copia das entradas de tempo que corresponden ao día da semana que se especifica no grupo de campos **Período ata**.</span><span class="sxs-lookup"><span data-stu-id="35a9d-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="35a9d-132">Por exemplo, a entrada de tempo para o luns da semana pasada cópiase ao luns da semana que se especifica no grupo de campos **Período ata**.</span><span class="sxs-lookup"><span data-stu-id="35a9d-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="35a9d-133">Datos de importación para entradas de tempo</span><span class="sxs-lookup"><span data-stu-id="35a9d-133">Import data for time entries</span></span>

<span data-ttu-id="35a9d-134">Pode importar datos das reservas e atribucións do proxecto.</span><span class="sxs-lookup"><span data-stu-id="35a9d-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="35a9d-135">Cando importe datos, pode especificar o intervalo de datas das reservas para importar e, a seguir, seleccionar explicitamente as reservas que se deben crear como entradas de tempo **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="35a9d-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="35a9d-136">Agrupar, ordenar, buscar e filtrar capacidades</span><span class="sxs-lookup"><span data-stu-id="35a9d-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="35a9d-137">Pode agrupar e filtrar as entradas de tempo polas dimensións que se especifican nas columnas.</span><span class="sxs-lookup"><span data-stu-id="35a9d-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="35a9d-138">No campo **Agrupar por**, seleccione a dimensión que se vai usar para filtrar as entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="35a9d-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="35a9d-139">Tamén pode ordenar os rexistros de entrada de tempo en orde ascendente ou descendente empregando a frecha de ordenación nas cabeceiras de columna.</span><span class="sxs-lookup"><span data-stu-id="35a9d-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="35a9d-140">Ademais, pode mostrar ou ocultar entradas seleccionando o botón **Filtro** nas cabeceiras da columna e, a seguir, na caixa **Buscar**, introducindo o texto que se debe usarse para buscar entradas de tempo por nome de proxecto, tarefa de proxecto, entrada de tempo ou recurso.</span><span class="sxs-lookup"><span data-stu-id="35a9d-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]