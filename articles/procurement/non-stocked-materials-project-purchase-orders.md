---
title: Pedir materiais sen fornecemento para un proxecto mediante pedidos de compra de proxectos
description: Este tema explica como pode pedir materiais sen fornecemento para un proxecto mediante pedidos de compra de proxectos.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612701"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Pedir categorías de adquisición ou materiais non abastecidos para un proxecto mediante pedidos de compra do proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

O departamento de adquisicións da súa organización podería usar [pedidos de compra](/dynamics365/supply-chain/procurement/purchase-order-overview) para rastrexar pedidos de produtos e servizos. As ordes de compra para categorías de aprovisionamento ou materiais que non sexan de stock pódense atribuír a un proxecto. A facturación destes pedidos de compra rexistra o custo do proxecto.

## <a name="prerequisites"></a>Requisitos previos
Complete os seguintes pasos para activar a funcionalidade de pedidos de compra do proxecto.

1. En Dynamics 365 Finance, vai ao **Xestión de características** espazo de traballo.
2. Na lista de funcionalidades, busque e seleccione a funcionalidade **Activar pedidos de compra de proxectos en Project Operations para situacións baseadas en recursos/sen fornecemento**.
3. Seleccione **Activar**.
4. Configure os materiais sen fornecemento e as facturas pendentes do fornecedor como se describe en [Configurar os materiais sen fornecemento e as facturas pendentes do fornecedor](configure-materials-nonstocked.md).
5. Configure as categorías de adquisición como se describe en [Use categorías de adquisición con pedidos de compra de proxectos e facturas de provedores pendentes](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Crear un pedido de compra do proxecto a partir da lista de pedidos de compra do proxecto

1. En Finance, vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Todos os proxectos** e seleccione un proxecto.
2. No panel de acción, no separador **Xestionar**, no grupo **Novo**, seleccione **Tarefa do elemento** > **Pedido de compra**.
3. Na páxina **Crear pedido de compra**, seleccione o fornecedor ao que desexa realizar o pedido de compra, introduza outra información segundo corresponda e logo seleccione **Aceptar**.
4. Na páxina **Pedido de compra**, na grade **Liñas de pedido de compra**, seleccione **Engadir liña**.
5. Introduza un número de artigo ou categoría de adquisición, cantidade, unidade, prezo unitario e outra información segundo corresponda.

    > [!NOTE]
    > Só se poden utilizar categorías de compras, artigos non abastecidos e servizos coas ordes de compra do proxecto. Non se admiten os artigos almacenados.

6. Continúe engadindo artigos ou categorías de adquisición segundo sexa necesario e confirme a orde de compra.

    Os recibos de pedidos e servizos poden rexistrarse creando e publicando un recibo de produto.

    > [!NOTE]
    > Os recibos de produto non se rexistran nos datos reais do proxecto en Microsoft Dataverse e non afectan ao libro maior auxiliar do proxecto.

    Despois de que un fornecedor envíe a factura por artigos e servizos no pedido de compra, o departamento de adquisicións pode xerar unha factura para o pedido de compra dirixíndose a **Factura** > **Xerar** > **Factura** no panel de acción. Para obter máis información sobre as facturas pendentes do fornecedor, consulte [Comprar materiais sen fornecemento mediante unha factura pendente do fornecedor](pending-vendor-invoices.md).
