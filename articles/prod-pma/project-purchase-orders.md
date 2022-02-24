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
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076120"
---
# <a name="purchase-orders-for-a-project"></a>Pedidos de compra para un proxecto

[!include [banner](../includes/banner.md)]

Este artigo describe os diversos métodos que pode empregar para crear pedidos de compra para un proxecto. O método que utilice depende da finalidade co pedido de compra e cando os artigos comprados se consumen e se cobran a un proxecto.

### <a name="methods-for-creating-a-purchase-order"></a>Métodos para crear un pedido de compra

Podes usar un dos seguintes métodos para crear un pedido de compra en Xestión e de proxectos e contabilidade. A finalidade do pedido de compra determina cando se consume o pedido de compra e, polo tanto, cando se cobran artigos a un proxecto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Propósito</th>
<th>Consumo de artigos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cree un pedido de compra directamente desde un proxecto.</td>
<td>Utilice este método para comprar artigos dun fornecedor externo para o consumo nun proxecto. Pode crear o pedido de compra de dos xeitos:
<ul>
<li>Desde o propio proxecto. Neste caso, o proxecto xa está definido para o pedido de compra.</li>
<li>Ao navegar ata o pedido de compra do proxecto. Debe seleccionar o fornecedor e o proxecto para o que crear o pedido de compra.</li>
</ul></td>
<td>Os artigos consúmense cando se actualiza a factura do fornecedor.</td>
</tr>
<tr class="even">
<td>Cree un pedido de compra a partir dun pedido de venda.</td>
<td>Utilice este método para comprar artigos cando cree un pedido de venda desde un proxecto.</td>
<td>Os artigos consúmense cando o pedido de venda se factura ao cliente.</td>
</tr>
<tr class="odd">
<td>Cree un pedido de compra a partir dun requisito de artigo.</td>
<td>Utilice este método para comprar artigos cando cree un requisito de artigo desde un proxecto.</td>
<td>Os artigos consúmense cando se actualiza o requisito de artigo na folla de embalaxe.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Cando actualice a factura do fornecedor ou a folla de embalaxe, solicítaselle que actualice a folla de embalaxe no requisito do artigo.

Para obter máis información, consulte [Recibir artigos do pedido de compra a partir do requisito do artigo](tasks/receive-items-purchase-order-item-requirement.md).

