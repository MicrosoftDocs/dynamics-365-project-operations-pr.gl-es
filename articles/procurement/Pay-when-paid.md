---
title: Paga cando se pagan os pagos do provedor
description: Este tema explica como usar o escenario de pago cando se paga (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Paga cando se pagan os pagos do provedor

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema explica como usar o escenario de pago cando se paga (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Crea unha orde de compra que teña condicións de PWP

Cando publica unha factura dun provedor, se o provedor está suxeito aos termos de PWP, eses termos móstranse nas liñas do pedido de compra (PO). Para crear un PO que teña termos de PWP, siga estes pasos.

1. En Microsoft Dynamics 365 Finance, siga un destes pasos:

    - Vaia a **Adquisición e abastecemento** \> **Pedidos de compra** \> **Todos os pedidos de compra**. No panel Acción, seleccione **Novo**. No **Crear pedido de compra** caixa de diálogo, seleccione o provedor para o cal os termos PWP están configurados no proxecto, introduza outra información necesaria e, a continuación, seleccione **OK**.
    - Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos**. No panel de accións, no **Xestionar** ficha, seleccione **Tarefa do elemento**. Seleccione o pedido de compra. Seleccione o provedor para o cal os termos de PWP están configurados no proxecto e, a continuación, seleccione **Ok**.

2. No **Orde de compra** páxina, na **Liñas de pedido de compra** Ficha rápida, seleccione **Engadir liña** para crear unha liña de pedido de compra.
3. Seleccione o número de artigo ou a categoría de adquisición e introduza os demais detalles necesarios. Revisa os detalles da liña de pedidos para o provedor.

    A opción **Pagar ao recibir o pagamento** seleccionase automaticamente e o valor do campo **Porcentaxe limiar de PWP** se copia automaticamente do campo **Porcentaxe limiar de PWP** da páxina **Proxectos**.

4. Se non quere aplicar os termos de PWP ao fornecedor dunha liña de PO, borre a opción **Pagar ao recibir o pagamento**. Neste caso, o **Porcentaxe de limiar de PWP** reiniciarase o campo para a liña PO **0** (cero).
5. No **Orde de compra** páxina, no Panel de accións, na páxina **Compra** ficha, seleccione **Confirmar** para confirmar a orde de compra.
6. No panel de accións, no **Factura** ficha, seleccione **Factura** para xerar a factura da orde de compra.

## <a name="create-a-project-invoice-proposal"></a>Crear unha proposta de factura do proxecto

As propostas de factura de proxecto utilízanse para crear facturas de proxecto para o cliente. No escenario PWP, os pagos dos provedores dependen dos pagos dos clientes segundo a configuración do PWP. Non obstante, hai opcións que che permiten liberar os pagos sen os pagos dos clientes segundo o requiras. Para crear unha factura de proxecto para o cliente, siga estes pasos.

1. Nas aplicacións de participación do cliente, vai a **Proxecto** \> **Proxectos**, e selecciona o proxecto.
2. No **Reais** pestana, seleccione a liña real xerada polo PO que ten o **Vendas sen facturar** tipo de transacción. A continuación, seleccione **Listo para facturar**.
3. Ir a **Vendas** \> **Vendas** \> **Contrato do proxecto**, e seleccione o contrato do proxecto.
4. No panel de accións, seleccione **Factura** para xerar a factura do cliente.
5. En Finanzas, vai a **Xestión de proxectos e contabilidade** \> **Periódico** \> **Importar desde a táboa de preparación**, e seleccione **Ok** para xerar o diario de integración de operacións do proxecto.
6. Ir a **Xestión de proxectos e contabilidade** \> **Facturas do proxecto** \> **Proposta de factura do proxecto**, e seleccione **Publicación** para publicar a proposta de factura que se xerou para o proxecto.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualizar o pagamento dun cliente e pagar ao fornecedor

Cando un provedor completa o seu traballo nun proxecto e che envía unha factura, debes revisar o estado do proxecto e as facturas dos clientes para determinar se se cumpriron os termos do PWP para o proxecto. Se se cumpriron os termos de PWP para o fornecedor, pode determinar que liñas da factura do provedor se pagan, en función dos pagamentos dos clientes polo proxecto. Se decide pagar ao fornecedor aínda que non se cumpriron as condicións de PWP, pode anular os termos de PWP na páxina **Factura do fornecedor que se paga ao recibir o pagamento**.

1. En Finanzas, vai a **Xestión de proxectos e contabilidade** \> **Proxectos** \> **Todos os proxectos**, e selecciona o proxecto.
2. No panel de accións, seleccione **Control** e, a continuación, seleccione **Facturas de provedores** para mostrar todas as facturas de provedores que se xeraron para o proxecto.
3. Na páxina **Facturas do fornecedor que se pagan ao recibir o pagamento**, no campo de busca, introduza valores para atopar a factura do fornecedor que desexa revisar e logo seleccione **Buscar**.
4. Seleccione o **Paga cando se paga** opción para ver só facturas PWP.
5. No **Liñas de facturas de provedores** Pestana Rápida, selecciona as liñas que queres liberar para o pago.
6. Seleccione **Liberar o pago do provedor**. A opción **Pagar ao recibir o pagamento** está borrada e o valor do campo **Listo para o pagamento** cambia a **Si**.
