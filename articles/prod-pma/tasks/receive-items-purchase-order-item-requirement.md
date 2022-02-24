---
title: Recibir artigos do pedido de compra a partir do requisito do artigo
description: Este tema explica como recibir artigos dun pedido de compra a partir dun requisito de artigo.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076299"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Recibir artigos do pedido de compra a partir do requisito do artigo

[!include [banner](../../includes/banner.md)]

Este tema explica como recibir artigos dun pedido de compra a partir dun requisito de artigo.

Ao usar un requisito de artigo en lugar dunha transacción de artigo, pode planificar a entrega xusto antes de que o artigo se use, crear un pedido de compra, incluír o artigo no marco do acordo comercial e incluír o requisito de artigo na planificación da produción. 

Esta tarefa utiliza o conxunto de datos USSI.

1. No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Proxectos > Todos os proxectos**.
2. Na lista, seleccione a ligazón da fila desexada.
3. No panel Acción, seleccione **Planificar**.
4. Seleccione **Requisitos do artigo**.
5. Seleccione **Nova**.
6. Na nova fila, introduza ou seleccione un valor no campo **Número do artigo**.
7. No campo **Cantidade**, introduza un número.
8. Seleccione **Gardar**.
9. No panel Acción, seleccione **Xestionar**.
10. Seleccione **Funcións**.
11. Señeccione **Crear pedido de compra**.
12. Seleccione a caixa de verificación **Incluír todos**.
13. No campo **Conta de fornecedor**, introduza ou seleccione un valor.
14. Seleccione **Aceptar**.
15. No panel de navegación, vaia a **Módulos > Contas pendentes de pago > Pedidos de compra > Todos os pedidos de compra**.
16. Na lista, seleccione a ligazón da fila desexada.
17. No panel Acción, seleccione **Comprar**.
18. Seleccione **Confirmar**.
19. No panel Acción, seleccione **Recibir**.
20. Seleccione **Recibo de produto**.
21. No campo **Recibo de produto**, escriba un valor.
22. Seleccione **Aceptar**.

