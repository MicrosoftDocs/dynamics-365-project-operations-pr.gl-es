---
title: Pagar ao recibir os pagamentos dos fornecedores
description: Este tema explica como usar o escenario de pagar ao recibir o pagamento (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525382"
---
# <a name="pay-when-paid-vendor-payments"></a>Pagar ao recibir os pagamentos dos fornecedores

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema explica como usar o escenario de pagar ao recibir o pagamento (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Crear un pedido de compra que teña condicións de PWP

Cando contabiliza unha factura dun fornecedor, se o fornecedor está suxeito a termos de PWP, eses termos móstranse nas liñas do pedido de compra (PO). Para crear un PO que teña termos de PWP, siga estes pasos.

1. En Microsoft Dynamics 365 Finance, siga un destes pasos::

    - Vaia a **Adquisición e abastecemento** \> **Pedidos de compra** \> **Todos os pedidos de compra**. No panel Acción, seleccione **Novo**. Na caixa de diálogo **Crear pedido de compra**, seleccione o fornecedor para o cal os termos PWP están configurados no proxecto, introduza outra información necesaria e, a continuación, seleccione **Aceptar**.
    - Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos**. No panel Acción, no separador **Xestionar**, seleccionar **Tarefa de artigo**. Seleccione o pedido de compra. Seleccione o fornecedor para o cal os termos de PWP están configurados no proxecto e, a seguir, seleccione **Aceptar**.

2. Na páxina **Pedido de compra**, no separador rápido **Liñas de pedido de compra**, seleccione **Engadir liña** para crear unha liña de pedido de compra.
3. Seleccione o número de artigo ou a categoría de adquisición e introduza os demais detalles necesarios. Revise os detalles da liña de PO para o fornecedor.

    A opción **Pagar ao recibir o pagamento** seleccionase automaticamente e o valor do campo **Porcentaxe limiar de PWP** se copia automaticamente do campo **Porcentaxe limiar de PWP** da páxina **Proxectos**.

4. Se non quere aplicar os termos de PWP ao fornecedor dunha liña de PO, borre a opción **Pagar ao recibir o pagamento**. Neste caso, a **Porcentaxe limiar de PWP** da liña de PO restablecerase a **0** (cero).
5. Na páxina **Pedido de compra**, no panel Acción, no separador **Comprar**, seleccione **Confirmar** para confirmar o pedido de compra.
6. No panel Acción, no separador **Factura**, seleccione **Factura** para xerar a factura do pedido de compra.

## <a name="create-a-project-invoice-proposal"></a>Crear unha proposta de facturas de proxecto

As propostas de factura de proxecto utilízanse para crear facturas de proxecto para o cliente. No escenario de PWP, os pagamentos dos fornecedores dependen dos pagamentos dos clientes segundo a configuración de PWP. Non obstante, hai opcións que lle permiten liberar os pagamentos sen os pagamentos dos clientes segundo o requira. Para crear unha factura de proxecto para o cliente, siga estes pasos.

1. Nas aplicacións de Customer Engagement, vaia a **Proxecto** \> **Proxectos** e seleccione o proxecto.
2. No separador **Datos reais**, seleccione a liña real xerada polo PO que ten o tipo de transacción **Vendas non facturadas**. A continuación, seleccione **Listo para facturar**.
3. Vaia a **Vendas** \> **Vendas** \> **Contrato do proxecto** e seleccione o contrato do proxecto.
4. No panel Acción, seleccione **Factura** para xerar a factura do cliente.
5. En Finance, vaia a **Xestión e contabilidade de proxectos** \> **Periódico** \> **Importar da táboa de transición** e seleccione **Aceptar** para xerar o diario de integración de Project Operations.
6. Vaia a **Xestión e contabilidade de proxectos** \> **Facturas do proxecto** \> **Proposta de factura do proxecto** e seleccione **Contabilizar** para contabilizar a proposta de factura que se xerou para o proxecto.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualizar o pagamento dun cliente e pagar ao fornecedor

Cando un fornecedor completa o seu traballo nun proxecto e lle envía unha factura, debe revisar o estado do proxecto e as facturas do cliente para determinar se se cumpriron os termos de PWP para o proxecto. Se se cumpriron os termos de PWP para o fornecedor, pode determinar que liñas da factura do provedor se pagan, en función dos pagamentos dos clientes polo proxecto. Se decide pagar ao fornecedor aínda que non se cumpriron as condicións de PWP, pode anular os termos de PWP na páxina **Factura do fornecedor que se paga ao recibir o pagamento**.

1. En Finance, vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos** e seleccione o proxecto.
2. No panel Acción, seleccione **Control** e, a seguir, seleccione **Facturas de fornecedores** para mostrar todas as facturas de fornecedores que se xeraron para o proxecto.
3. Na páxina **Facturas do fornecedor que se pagan ao recibir o pagamento**, no campo de busca, introduza valores para atopar a factura do fornecedor que desexa revisar e logo seleccione **Buscar**.
4. Seleccione a opción **Paga ao recibir o pagamento** para ver só facturas PWP.
5. No separador rápido **Liñas de factura do fornecedor**, seleccione as liñas que quere liberar para o pagamento.
6. Seleccione **Liberar o pagamento do fornecedor**. A opción **Pagar ao recibir o pagamento** está borrada e o valor do campo **Listo para o pagamento** cambia a **Si**.
