---
title: Sincronizar capacidade de recursos
description: Este tema ofrece información sobre como sincronizar a capacidade dun recurso entre calendarios e proxectos.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997509"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="4030f-103">Sincronizar capacidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4030f-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4030f-104">Os procesos de sincronización de recursos axudan a garantir que a información do calendario e do calendario base chega á programación de recursos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="4030f-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="4030f-105">Se se cambia o calendario, os procesos realizan as actualizacións necesarias para a programación dos recursos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="4030f-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="4030f-106">Os procesos tamén axudan a mellorar o rendemento, porque a información dos recursos do calendario está sincronizada con antelación.</span><span class="sxs-lookup"><span data-stu-id="4030f-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="4030f-107">Polo tanto, as actualizacións da información de programación de recursos prodúcense con maior rapidez.</span><span class="sxs-lookup"><span data-stu-id="4030f-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="4030f-108">Recomendámoslle que programe os procesos como un lote en vez de un á vez.</span><span class="sxs-lookup"><span data-stu-id="4030f-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="4030f-109">En caso contrario, existe o risco de que alguén esqueza as datas incluídas na última sincronización da información.</span><span class="sxs-lookup"><span data-stu-id="4030f-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="4030f-110">Se non se utilizan datas inclusivas, poden producirse lagoas durante a sincronización de datas.</span><span class="sxs-lookup"><span data-stu-id="4030f-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sincronización do calendario](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="4030f-112">Sincronizar agrupamentos de capacidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4030f-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="4030f-113">O proceso de sincronización está deseñado para sincronizar toda a información do calendario de recursos.</span><span class="sxs-lookup"><span data-stu-id="4030f-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="4030f-114">Esta información inclúe información do calendario base sobre calquera cambio na táboa de capacidade do calendario dos recursos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="4030f-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="4030f-115">Se se engaden novos recursos no proxecto, a sincronización axuda a garantir que a información actualizada do calendario está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="4030f-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="4030f-116">Esta sincronización pódese facer en calquera momento.</span><span class="sxs-lookup"><span data-stu-id="4030f-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="4030f-117">Recomendámoslle que use un lote.</span><span class="sxs-lookup"><span data-stu-id="4030f-117">We recommend that you use a batch.</span></span> <span data-ttu-id="4030f-118">As opcións están dispoñibles durante a sincronización das reservas de capacidade.</span><span class="sxs-lookup"><span data-stu-id="4030f-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="4030f-119">Seleccione **Xestión de proxectos e contabilidade** &gt; **Periódico** &gt; **Sincronización de capacidade** &gt; **Sincronizar agrupamentos de capacidade de recursos**.</span><span class="sxs-lookup"><span data-stu-id="4030f-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="4030f-120">Configure as opcións na táboa seguinte.</span><span class="sxs-lookup"><span data-stu-id="4030f-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="4030f-121">Opción</span><span class="sxs-lookup"><span data-stu-id="4030f-121">Option</span></span>      | <span data-ttu-id="4030f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4030f-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="4030f-123">Código do período</span><span class="sxs-lookup"><span data-stu-id="4030f-123">Period code</span></span> | <span data-ttu-id="4030f-124">Opcionalmente, seleccione o código do intervalo de datas do libro maior para establecer as datas de inicio e finalización do proceso de sincronización para os agrupamentos de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="4030f-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4030f-125">Data de inicio</span><span class="sxs-lookup"><span data-stu-id="4030f-125">Start date</span></span>  | <span data-ttu-id="4030f-126">Introduza a data de inicio do proceso de sincronización para os agrupamentos de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="4030f-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4030f-127">Data de finalización</span><span class="sxs-lookup"><span data-stu-id="4030f-127">End date</span></span>    | <span data-ttu-id="4030f-128">Introduza a data de finalización do proceso de sincronización para os agrupamentos de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="4030f-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="4030f-129">[![Proceso de sincronización](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="4030f-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]