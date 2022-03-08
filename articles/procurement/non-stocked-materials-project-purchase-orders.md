---
title: Pedir materiais sen fornecemento para un proxecto mediante pedidos de compra de proxectos
description: Este tema explica como pode pedir materiais sen fornecemento para un proxecto mediante pedidos de compra de proxectos.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563020"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Pedir materiais sen fornecemento para un proxecto mediante pedidos de compra de proxectos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

O departamento de adquisicións da súa organización podería usar [pedidos de compra](/dynamics365/supply-chain/procurement/purchase-order-overview) para rastrexar pedidos de produtos e servizos. Os pedidos de compra de materiais sen fornecemento poden atribuírse a un proxecto. A facturación destes pedidos de compra rexistra o custo do proxecto.

## <a name="prerequisites"></a>Requisitos previos
Complete os seguintes pasos para activar a funcionalidade de pedidos de compra do proxecto.

1. En Dynamics 365 Finance, vaia á área de traballo **Xestión de funcionalidades**.
2. Na lista de funcionalidades, busque e seleccione a funcionalidade **Activar pedidos de compra de proxectos en Project Operations para situacións baseadas en recursos/sen fornecemento**.
3. Seleccione **Activar**.
4. Configure os materiais sen fornecemento e as facturas pendentes do fornecedor como se describe en [Configurar os materiais sen fornecemento e as facturas pendentes do fornecedor](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Crear un pedido de compra do proxecto a partir da lista de pedidos de compra do proxecto

1. En Finance, vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Todos os proxectos** e seleccione un proxecto.
2. No panel de acción, no separador **Xestionar**, no grupo **Novo**, seleccione **Tarefa do elemento** > **Pedido de compra**.
3. Na páxina **Crear pedido de compra**, seleccione o fornecedor ao que desexa realizar o pedido de compra, introduza outra información segundo corresponda e logo seleccione **Aceptar**.
4. Na páxina **Pedido de compra**, na grade **Liñas de pedido de compra**, seleccione **Engadir liña**.
5. Introduza un número de artigo, cantidade, unidade, prezo unitario e outra información segundo corresponda.

    > [!NOTE]
    > Só os artigos e servizos sen fornecemento poden usarse cos pedidos de compra do proxecto. Non se admiten artigos con fornecemento nin categorías de adquisición.

6. Continúe engadindo artigos segundo sexa necesario e confirme o pedido de compra.

    Os recibos de pedidos e servizos poden rexistrarse creando e publicando un recibo de produto.

    > [!NOTE]
    > Os recibos de produto non se rexistran nos datos reais do proxecto en Microsoft Dataverse e non afectan ao libro maior auxiliar do proxecto.

    Despois de que un fornecedor envíe a factura por artigos e servizos no pedido de compra, o departamento de adquisicións pode xerar unha factura para o pedido de compra dirixíndose a **Factura** > **Xerar** > **Factura** no panel de acción. Para obter máis información sobre as facturas pendentes do fornecedor, consulte [Comprar materiais sen fornecemento mediante unha factura pendente do fornecedor](pending-vendor-invoices.md).