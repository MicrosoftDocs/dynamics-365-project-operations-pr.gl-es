---
title: Configurar e usar pagamentos de fornecedores que se pagan ao recibir o pagamento
description: Este tema explica como crear termos de pagamento ao recibir o pagamento (PWP) para que poida liberar pagamentos parciais ao fornecedor, en función dos pagamentos dos clientes.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 9976dadf57f1c84bf3f295ff3c8359c16e4849a3bf887f8bd33e46a04e2a5952
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008854"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Configurar e usar pagamentos de fornecedores que se pagan ao recibir o pagamento

[!include [banner](../includes/banner.md)]

Cando vostede aprobe que un vendedor traballe como subcontratista, quizais queira reter o pagamento ata que o seu cliente lle pague o proxecto. Para permitir esta situación, pode configurar termos de pagamento ao recibir o pagamento (PWP) cando configura o pedido de compra (PO) co fornecedor.

Por exemplo, cando un cliente paga un importe dunha factura do proxecto, pode liberar parte ou a totalidade do importe da factura do fornecedor. Simplemente configure os termos de PWP que especifiquen que se pagará ao fornecedor despois de recibir unha porcentaxe do pagamento relacionado do cliente. Se recibe un pagamento parcial dun cliente, pode liberar manualmente algunhas das facturas do fornecedor relacionadas.

O seguinte exemplo describe o proceso cando se usan termos de PWP.

## <a name="example"></a>Exemplo

A súa organización acepta subministrar a un cliente 100 ordenadores que teñen instalado software por un prezo de 150,00 dólares estadounidenses (USD) por ordenador. Logo contrata a un fornecedor para que lle subministre os ordenadores que teñen instalado o software. Segundo o contrato, o cliente debe aprobar a calidade dos ordenadores antes de pagarlle á súa organización. A política da súa organización é reter o pagamento aos fornecedores ata que o cliente lle pague. Polo tanto, configurou o proxecto para que teña unha porcentaxe de PWP do 100 por cento.

O fornecedor envíalle os 100 ordenadores que teñen instalado o software, xunto cunha factura por 10 000,00 USD. Debido a que os termos de PWP están configurados para o seu proxecto, non paga ao fornecedor unha vez recibidos os ordenadores. En vez diso, envía os ordenadores ao cliente, xunto cunha factura por 15 000.00. O cliente inspecciona os ordenadores e aproba o importe total da factura do proxecto.

Despois de recibir o pagamento completo do cliente, pagará ao fornecedor 10 000.00, o importe total da factura do fornecedor.

## <a name="set-up-pwp-terms-for-a-project"></a>Configurar os termos de PWP para un proxecto

Cando configura os termos de PWP para un proxecto, debe especificar, como porcentaxe, a cantidade mínima que un cliente lle debe pagar polo proxecto antes de pagarlle ao fornecedor. O importe limiar calcúlase automaticamente nas facturas do cliente para o proxecto. Siga estes pasos para configurar a porcentaxe limiar para os termos de PWP.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos**.
2. Busque e abra o proxecto para o que desexa configurar os termos de PWP.
3. No separador rápido **Acordos de fornecedores**, seleccione **Engadir liña**.
3. No campo **Código de conta**, seleccione unha das seguintes opcións:

    - **Táboa** – Os termos de PWP aplícanse a un único fornecedor.
    - **Grupo** – Os termos de PWP aplícanse a todos os fornecedores dun grupo de fornecedores.
    - **Todos** – Os termos de PWP aplícanse a todos os fornecedores.

4. Se seleccionou **Táboa** ou **Grupo** no paso anterior, no campo **Fornecedor/Grupo de Fornecedores**, seleccione o fornecedor ou grupo de fornecedores aos que se aplican os termos de PWP. Se seleccionou **Todos** no paso anterior, o campo **Fornecedor/Grupo de fornecedores** non se pode editar.
5. Se se configuran os termos de retención do provedor para o fornecedor no proxecto, no campo **Termos de retención do fornecedor**, seleccione o ID da regra para os termos de retención.
6. No campo **Porcentaxe limiar de PWP**, introduza a porcentaxe limiar para o proxecto. A porcentaxe que introduza para o proxecto define a cantidade mínima que o cliente debe pagarlle antes de pagarlle ao fornecedor.

## <a name="create-a-po-that-has-pwp-terms"></a>Crear un PO que teña termos de PWP

Cando contabiliza unha factura dun fornecedor, se o fornecedor está suxeito a termos de PWP, eses termos móstranse nas liñas do PO. Para crear un PO que teña termos de PWP, siga estes pasos.

1. Vaia a **Adquisición e abastecemento** \> **Pedidos de compra** \> **Todos os pedidos de compra**.
2. No panel Acción, seleccione **Novo**. Despois, na caixa de diálogo **Crear pedido de compra**, introduza a información requirida e seleccione **Aceptar**.

    Como alternativa, abra un PO existente na páxina de lista **Todos os pedidos de compra**.

4. Na páxina **Pedido de compra**, no separador rápido **Liñas de pedido de compra**, revise os detalles da liña de PO para o fornecedor. A opción **Pagar ao recibir o pagamento** seleccionase automaticamente e o valor do campo **Porcentaxe limiar de PWP** se copia automaticamente do campo **Porcentaxe limiar de PWP** da páxina **Proxectos**.
6. Se non quere aplicar os termos de PWP ao fornecedor dunha liña de PO, borre a opción **Pagar ao recibir o pagamento**. Neste caso, a **Porcentaxe limiar de PWP** da liña de PO restablecerase a 0 (cero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualizar o pagamento dun cliente e pagar ao fornecedor

Cando un fornecedor completa o seu traballo nun proxecto e lle envía unha factura, debe revisar o estado do proxecto e as facturas do cliente para determinar se se cumpriron os termos de PWP para o proxecto. Se se cumpriron os termos de PWP para o fornecedor, pode determinar que liñas da factura do provedor se pagan, en función dos pagamentos dos clientes polo proxecto. Se decide pagar ao fornecedor aínda que non se cumpriron as condicións de PWP, pode anular os termos de PWP na páxina **Factura do fornecedor que se paga ao recibir o pagamento**.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Consultas e informes** \> **Consultas de retención** \> **Factura do fornecedor que se paga ao recibir o pagamento**.
2. Na páxina **Facturas do fornecedor que se pagan ao recibir o pagamento**, no campo de busca, introduza valores para atopar a factura do fornecedor que desexa revisar e logo seleccione **Buscar**.
3. No separador rápido **Liñas de factura do fornecedor**, seleccione as liñas que quere cambiar.
4. Se as condicións de **Pagar ao recibir o pagamento** se cumpren para a liña de factura, seleccione **Liberar o pagamento do fornecedor**. A opción **Pagar ao recibir o pagamento** está borrada e o valor do campo **Listo para o pagamento** cambia a **Si**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]