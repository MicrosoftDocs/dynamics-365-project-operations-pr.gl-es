---
title: Pedidos de compra para un proxecto
description: Este artigo describe os diversos métodos que pode empregar para crear pedidos de compra para un proxecto. O método que utilice depende da finalidade co pedido de compra e cando os artigos comprados se consumen e se cobran a un proxecto.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289187"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="3d7b8-104">Pedidos de compra para un proxecto</span><span class="sxs-lookup"><span data-stu-id="3d7b8-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d7b8-105">Este artigo describe os diversos métodos que pode empregar para crear pedidos de compra para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="3d7b8-106">O método que utilice depende da finalidade co pedido de compra e cando os artigos comprados se consumen e se cobran a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="3d7b8-107">Métodos para crear un pedido de compra</span><span class="sxs-lookup"><span data-stu-id="3d7b8-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="3d7b8-108">Podes usar un dos seguintes métodos para crear un pedido de compra en Xestión e de proxectos e contabilidade.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="3d7b8-109">A finalidade do pedido de compra determina cando se consume o pedido de compra e, polo tanto, cando se cobran artigos a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d7b8-110">Método</span><span class="sxs-lookup"><span data-stu-id="3d7b8-110">Method</span></span></th>
<th><span data-ttu-id="3d7b8-111">Propósito</span><span class="sxs-lookup"><span data-stu-id="3d7b8-111">Purpose</span></span></th>
<th><span data-ttu-id="3d7b8-112">Consumo de artigos</span><span class="sxs-lookup"><span data-stu-id="3d7b8-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d7b8-113">Cree un pedido de compra directamente desde un proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="3d7b8-114">Utilice este método para comprar artigos dun fornecedor externo para o consumo nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="3d7b8-115">Pode crear o pedido de compra de dos xeitos:</span><span class="sxs-lookup"><span data-stu-id="3d7b8-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="3d7b8-116">Desde o propio proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-116">From the project itself.</span></span> <span data-ttu-id="3d7b8-117">Neste caso, o proxecto xa está definido para o pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="3d7b8-118">Ao navegar ata o pedido de compra do proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="3d7b8-119">Debe seleccionar o fornecedor e o proxecto para o que crear o pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="3d7b8-120">Os artigos consúmense cando se actualiza a factura do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d7b8-121">Cree un pedido de compra a partir dun pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="3d7b8-122">Utilice este método para comprar artigos cando cree un pedido de venda desde un proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="3d7b8-123">Os artigos consúmense cando o pedido de venda se factura ao cliente.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d7b8-124">Cree un pedido de compra a partir dun requisito de artigo.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="3d7b8-125">Utilice este método para comprar artigos cando cree un requisito de artigo desde un proxecto.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="3d7b8-126">Os artigos consúmense cando se actualiza o requisito de artigo na folla de embalaxe.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="3d7b8-127">Cando actualice a factura do fornecedor ou a folla de embalaxe, solicítaselle que actualice a folla de embalaxe no requisito do artigo.</span><span class="sxs-lookup"><span data-stu-id="3d7b8-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="3d7b8-128">Para obter máis información, consulte [Recibir artigos do pedido de compra a partir do requisito do artigo](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="3d7b8-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]