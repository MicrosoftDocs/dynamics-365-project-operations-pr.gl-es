---
title: Rendemento de proposta de factura de proxecto
description: Este tema ofrece información sobre melloras de rendemento para as propostas de factura do proxecto.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920300"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="d63c6-103">Rendemento de proposta de factura de proxecto</span><span class="sxs-lookup"><span data-stu-id="d63c6-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d63c6-104">Cando crea unha nova proposta de factura, é posible que teña problemas de rendemento a medida que aumenta o número de proxectos e subproxectos.</span><span class="sxs-lookup"><span data-stu-id="d63c6-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="d63c6-105">Para mellorar o rendemento, está dispoñible unha función que reduce o tempo necesario para crear unha nova proposta de factura para as transaccións do proxecto contabilizadas.</span><span class="sxs-lookup"><span data-stu-id="d63c6-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d63c6-106">Activar a mellora do rendemento das propostas de factura do proxecto</span><span class="sxs-lookup"><span data-stu-id="d63c6-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d63c6-107">Para activar a función de mellora do rendemento das propostas de factura do proxecto, complete os seguintes pasos.</span><span class="sxs-lookup"><span data-stu-id="d63c6-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="d63c6-108">Vaia a **Xestión de funcionalidades** > **Todo**.</span><span class="sxs-lookup"><span data-stu-id="d63c6-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d63c6-109">Na lista de funcionalidades, localice **Mellora do rendemento das propostas de factura do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="d63c6-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d63c6-110">Seleccione **Activar agora**.</span><span class="sxs-lookup"><span data-stu-id="d63c6-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="d63c6-111">Actualice o explorador e cree unha nova proposta de factura.</span><span class="sxs-lookup"><span data-stu-id="d63c6-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d63c6-112">Desactivar a mellora do rendemento das propostas de factura do proxecto</span><span class="sxs-lookup"><span data-stu-id="d63c6-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d63c6-113">Complete os seguintes pasos para desactivar a mellora do rendemento das propostas de factura do proxecto.</span><span class="sxs-lookup"><span data-stu-id="d63c6-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="d63c6-114">Vaia a **Xestión de funcionalidades** > **Todo**.</span><span class="sxs-lookup"><span data-stu-id="d63c6-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d63c6-115">Na lista de funcionalidades, localice **Mellora do rendemento das propostas de factura do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="d63c6-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d63c6-116">Seleccione **Desactivar**.</span><span class="sxs-lookup"><span data-stu-id="d63c6-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="d63c6-117">Actualice o explorador.</span><span class="sxs-lookup"><span data-stu-id="d63c6-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="d63c6-118">O rendemento da proposta de factura non se pode aplicar cando as regras de facturación están activadas ou se están executando procesos por lotes.</span><span class="sxs-lookup"><span data-stu-id="d63c6-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
