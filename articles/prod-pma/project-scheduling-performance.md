---
title: Rendemento de programación de recursos de proxecto
description: Este tema ofrece información sobre como mellorar o rendemento da programación de recursos para un gran número de proxectos.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076115"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="5ee60-103">Rendemento de programación de recursos de proxecto</span><span class="sxs-lookup"><span data-stu-id="5ee60-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="5ee60-104">Os problemas de rendemento relacionados coa programación de recursos poden ocorrer cando o número de proxectos alcanza os miles.</span><span class="sxs-lookup"><span data-stu-id="5ee60-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="5ee60-105">Para mellorar o rendemento da programación de recursos, está dispoñible unha función que permite aos usuarios reducir o tempo que tardan en lanzar o formulario de dispoñibilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="5ee60-106">En concreto, isto elimina o proceso de sincronización acumulativa de recursos e usa a táboa **ResProjectResource** para acelerar a busca de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="5ee60-107">Teña en conta que a táboa **Resrollup** deixará de usarse.</span><span class="sxs-lookup"><span data-stu-id="5ee60-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ee60-108">Se existe unha dependencia do proceso de sincronización de acumulación de recursos ou da táboa **ResProjectResource** , non use esta función.</span><span class="sxs-lookup"><span data-stu-id="5ee60-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="5ee60-109">Activar a mellora do rendemento da programación de recursos</span><span class="sxs-lookup"><span data-stu-id="5ee60-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="5ee60-110">Para activar a mellora do rendemento da programación de recursos, complete os seguintes pasos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="5ee60-111">Vaia a **Xestión de funcionalidades** > **Todas** e na lista de funcionalidades, localice **Activar a función de mellora do rendemento da programación de recursos do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="5ee60-112">Seleccione **Activar agora**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="5ee60-113">Se non atopa a función na lista, seleccione **Comprobar se hai actualizacións** para actualizar a lista.</span><span class="sxs-lookup"><span data-stu-id="5ee60-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="5ee60-114">Actualice o explorador e despois vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Recursos do proxecto** > **Sincronizar a capacidade dos calendarios de recursos en todas as empresas**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="5ee60-115">Axuste **Eliminar os rexistros de capacidade existentes** en **Si** para eliminar datos anteriores.</span><span class="sxs-lookup"><span data-stu-id="5ee60-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="5ee60-116">Se quere xerar datos incrementais, configúreo en **Non**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="5ee60-117">No campo **Código do período** , seleccione o período no que se deben xerar os datos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="5ee60-118">Se selecciona un código de período, non é preciso definir unha data de inicio e finalización.</span><span class="sxs-lookup"><span data-stu-id="5ee60-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="5ee60-119">Se deixa o campo **Código do período** en branco, seleccione datas específicas de inicio e finalización para xerar datos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="5ee60-120">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="5ee60-121">Isto distribuirá datos xerais á táboa **ResCalendarCapacity** entre todas as empresas do seu ambiente, polo que o traballo por lotes só precisa executarse nunha entidade legal.</span><span class="sxs-lookup"><span data-stu-id="5ee60-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="5ee60-122">Os datos deste traballo por lotes son necesarios para calcular a capacidade do recurso a través do calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="5ee60-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="5ee60-123">Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Recursos do proxecto** > **Poboar recursos do proxecto en todas as empresas** e logo seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="5ee60-124">Este é o script de actualización de datos para datos xerais nas táboas **ResProjectResource** , **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="5ee60-125">Os valores para o campo **PSAPRojSchedRole.RootActivity**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="5ee60-126">Se non se executa, recibirá un aviso cando intente executar operacións de programación de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="5ee60-127">Desactivar a mellora do rendemento da programación de recursos</span><span class="sxs-lookup"><span data-stu-id="5ee60-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="5ee60-128">Vaia a **Xestión de funcionalidades** > **Todas** e busque **Activar a función de mellora do rendemento da programación de recursos do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="5ee60-129">Seleccione a funcionalidade e logo seleccione o botón **Desactivar**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="5ee60-130">Actualice o explorador.</span><span class="sxs-lookup"><span data-stu-id="5ee60-130">Refresh your browser.</span></span>
4. <span data-ttu-id="5ee60-131">Vaia a **Xestión de proxectos e contabilidade** > **Periódico** > **Sincronización de capacidade** > **Sincronizar agrupamentos de capacidade de recursos**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="5ee60-132">Na paxina **Sincronización de acumulación de capacidade** , axuste **Eliminar os rexistros de capacidade existentes** en **Si** para eliminar datos anteriores.</span><span class="sxs-lookup"><span data-stu-id="5ee60-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="5ee60-133">Se quere xerar datos incrementais, configúreo en **Non**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="5ee60-134">No campo **Código do período** , seleccione o período no que se deben xerar os datos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="5ee60-135">Se selecciona un código de período, non é preciso definir unha data de inicio e finalización.</span><span class="sxs-lookup"><span data-stu-id="5ee60-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="5ee60-136">Se deixa o campo **Código do período** en branco, seleccione datas específicas de inicio e finalización para xerar datos.</span><span class="sxs-lookup"><span data-stu-id="5ee60-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="5ee60-137">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="5ee60-138">Isto distribuirá datos xerais á táboa **ResRollup** entre todas as empresas do seu ambiente, polo que o traballo por lotes só precisa executarse nunha entidade legal.</span><span class="sxs-lookup"><span data-stu-id="5ee60-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="5ee60-139">Este traballo por lotes é necesario para todas as vistas de **Dispoñibilidade de recursos**.</span><span class="sxs-lookup"><span data-stu-id="5ee60-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="5ee60-140">Se non se executa este traballo por lotes, os datos de **Resrollup** os datos xeraranse sobre a marcha, o que pode levar algún tempo.</span><span class="sxs-lookup"><span data-stu-id="5ee60-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
