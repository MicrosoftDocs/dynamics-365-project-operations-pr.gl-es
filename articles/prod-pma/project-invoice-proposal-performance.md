---
title: Rendemento de proposta de factura de proxecto
description: Este tema ofrece información sobre melloras de rendemento para as propostas de factura do proxecto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269788"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="a9b82-103">Rendemento de proposta de factura de proxecto</span><span class="sxs-lookup"><span data-stu-id="a9b82-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9b82-104">Cando crea unha nova proposta de factura, é posible que teña problemas de rendemento a medida que aumenta o número de proxectos e subproxectos.</span><span class="sxs-lookup"><span data-stu-id="a9b82-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="a9b82-105">Para mellorar o rendemento, está dispoñible unha función que reduce o tempo necesario para crear unha nova proposta de factura para as transaccións do proxecto contabilizadas.</span><span class="sxs-lookup"><span data-stu-id="a9b82-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="a9b82-106">Activar a mellora do rendemento das propostas de factura do proxecto</span><span class="sxs-lookup"><span data-stu-id="a9b82-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="a9b82-107">Para activar a función de mellora do rendemento das propostas de factura do proxecto, complete os seguintes pasos.</span><span class="sxs-lookup"><span data-stu-id="a9b82-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="a9b82-108">Vaia a **Xestión de funcionalidades** > **Todo**.</span><span class="sxs-lookup"><span data-stu-id="a9b82-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="a9b82-109">Na lista de funcionalidades, localice **Mellora do rendemento das propostas de factura do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="a9b82-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="a9b82-110">Seleccione **Activar agora**.</span><span class="sxs-lookup"><span data-stu-id="a9b82-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="a9b82-111">Actualice o explorador e cree unha nova proposta de factura.</span><span class="sxs-lookup"><span data-stu-id="a9b82-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="a9b82-112">Desactivar a mellora do rendemento das propostas de factura do proxecto</span><span class="sxs-lookup"><span data-stu-id="a9b82-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="a9b82-113">Complete os seguintes pasos para desactivar a mellora do rendemento das propostas de factura do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a9b82-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="a9b82-114">Vaia a **Xestión de funcionalidades** > **Todo**.</span><span class="sxs-lookup"><span data-stu-id="a9b82-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="a9b82-115">Na lista de funcionalidades, localice **Mellora do rendemento das propostas de factura do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="a9b82-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="a9b82-116">Seleccione **Desactivar**.</span><span class="sxs-lookup"><span data-stu-id="a9b82-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="a9b82-117">Actualice o explorador.</span><span class="sxs-lookup"><span data-stu-id="a9b82-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="a9b82-118">O rendemento da proposta de factura non se pode aplicar cando se activan as regras de facturación.</span><span class="sxs-lookup"><span data-stu-id="a9b82-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="a9b82-119">Durante o proceso por lotes para crear propostas de factura, o número de subtarefas dividirá as tarefas a un número máximo en función do número de contratos con transaccións facturables, independentemente do que introducise.</span><span class="sxs-lookup"><span data-stu-id="a9b82-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="a9b82-120">Por exemplo, se introduce **3** para o número de subtarefas para a creación de propostas de factura por lotes e só hai dous contratos con transaccións facturables, só se crean dúas subtarefas.</span><span class="sxs-lookup"><span data-stu-id="a9b82-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
