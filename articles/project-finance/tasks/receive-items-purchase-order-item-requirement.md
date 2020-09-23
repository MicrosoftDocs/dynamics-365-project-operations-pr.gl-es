---
title: Recibir artigos do pedido de compra a partir do requisito do artigo
description: Este tema explica como recibir artigos dun pedido de compra a partir dun requisito de artigo.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751321"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="2d3a2-103">Recibir artigos do pedido de compra a partir do requisito do artigo</span><span class="sxs-lookup"><span data-stu-id="2d3a2-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d3a2-104">Este tema explica como recibir artigos dun pedido de compra a partir dun requisito de artigo.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="2d3a2-105">Ao usar un requisito de artigo en lugar dunha transacción de artigo, pode planificar a entrega xusto antes de que o artigo se use, crear un pedido de compra, incluír o artigo no marco do acordo comercial e incluír o requisito de artigo na planificación da produción.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="2d3a2-106">Esta tarefa utiliza o conxunto de datos USSI.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2d3a2-107">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Proxectos > Todos os proxectos**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="2d3a2-108">Na lista, seleccione a ligazón da fila desexada.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="2d3a2-109">No panel Acción, seleccione **Planificar**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="2d3a2-110">Seleccione **Requisitos do artigo**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="2d3a2-111">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-111">Select **New**.</span></span>
6. <span data-ttu-id="2d3a2-112">Na nova fila, introduza ou seleccione un valor no campo **Número do artigo**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="2d3a2-113">No campo **Cantidade**, introduza un número.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="2d3a2-114">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-114">Select **Save**.</span></span>
9. <span data-ttu-id="2d3a2-115">No panel Acción, seleccione **Xestionar**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="2d3a2-116">Seleccione **Funcións**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-116">Select **Functions**.</span></span>
11. <span data-ttu-id="2d3a2-117">Señeccione **Crear pedido de compra**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="2d3a2-118">Seleccione a caixa de verificación **Incluír todos**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="2d3a2-119">No campo **Conta de fornecedor**, introduza ou seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="2d3a2-120">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-120">Select **OK**.</span></span>
15. <span data-ttu-id="2d3a2-121">No panel de navegación, vaia a **Módulos > Contas pendentes de pago > Pedidos de compra > Todos os pedidos de compra**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="2d3a2-122">Na lista, seleccione a ligazón da fila desexada.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="2d3a2-123">No panel Acción, seleccione **Comprar**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="2d3a2-124">Seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="2d3a2-125">No panel Acción, seleccione **Recibir**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="2d3a2-126">Seleccione **Recibo de produto**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="2d3a2-127">No campo **Recibo de produto**, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="2d3a2-128">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2d3a2-128">Select **OK**.</span></span>

