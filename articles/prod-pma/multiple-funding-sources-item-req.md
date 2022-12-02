---
title: Requisitos de elementos para contratos de proxectos con múltiples fontes de financiamento
description: Este artigo ofrece información sobre como configurar e usar os requisitos de artigo con varias fontes de financiamento.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028471"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Requisitos de elementos para contratos de proxectos con múltiples fontes de financiamento

_**Aplícase a:** Project Operations para situacións baseadas en produción/con fornecemento_

Algúns acordos contractuais para entregas baseadas en proxectos poden requirir varias fontes de financiamento. Este artigo explica como seleccionar e configurar as fontes de financiamento desexadas cando se requiren varias fontes para un proxecto ou contrato de proxecto.

## <a name="terminology"></a>Terminoloxía

- **Fonte de financiamento** – A entidade que financia o traballo do contrato do proxecto. Esta entidade pode ser unha organización interna ou unha conta de factura externa (cliente ou subvención).
- **Cliente do proxecto** – A entidade á que se entrega o traballo do proxecto.
- **Conta de factura** – A entidade externa que paga o traballo do proxecto.

## <a name="example"></a>Exemplo

Contoso gañou un contrato de renovación de equipos con dous dos seus clientes: Adatum US e Adatum Corporate. O contrato inclúe hardware e servizos de instalación que serán entregados a Adatum US (o cliente do proxecto). O hardware será financiado por Adatum Corporate (conta de factura 1), e os traballos de instalación serán financiados por Adatum US (conta de factura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurar regras predeterminadas da conta de factura para os requisitos de artigo

### <a name="prerequisites"></a>Requisitos previos

- Microsoft Dynamics 365 Finance **versión 10.0.27 ou posterior** é necesario para utilizar requisitos de artigo que teñan varias contas de factura.
- O seu administrador do sistema debe activar a funcionalidade **Permitir os requisitos de artigo con varias fontes de financiamento para os escenarios con fornecemento/baseados na produción de Project Operations** na área de traballo **Xestión de funcionalidade**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurar as regras predeterminadas da conta de factura

Para configurar as regras predeterminadas para a conta de factura, siga estes pasos.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Parámetros de Xestión e contabilidade de proxectos**.
1. No separador **Xeral**, na sección **Pedidos de vendas e requisitos de artigo**, configure a opción **Permitir proxectos con múltiples fontes de financiamento** en **Si**.
1. No campo **Cliente predeterminado**, especifique de onde procede o cliente de entrega do proxecto sobre o requisito de artigo por defecto:

    - **Da fonte de financiamento** – O cliente de entrega do proxecto por defecto procede da fonte de financiamento. Se se asocian varias fontes de financiamento ao contrato do proxecto, utilizarase a primeira fonte de financiamento da lista.
    - **Do proxecto** – O cliente de entrega do proxecto predeterminado procede do cliente seleccionado no campo **Conta de rexistro do proxecto**.

1. Opcional: estableza ou cambie a conta de factura predeterminada nos rexistros do proxecto:

    1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos** e abra os detalles de rexistro do proxecto.
    2. No separador **Xeral**, configure ou actualice o campo **Conta de factura predeterminada**. A conta que especifique utilizarase como conta de factura predeterminada para os requisitos de artigos novos que se crean para o proxecto. Se deixa o campo en branco, a conta de factura da fonte de financiamento do primeiro contrato do proxecto empregarase por defecto. Non obstante, os usuarios poderán cambiar a conta cando garden o rexistro.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Seleccione a conta de factura que quere utilizar cando cree un requisito de artigo

Para seleccionar a conta de factura que quere utilizar cando cree un requisito de artigo, siga estes pasos.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos** e seleccione o rexistro de proxecto.
1. No separador **Plan**, seleccione **Requisitos de artigo**.
1. Crear un novo rexistro de requisito de artigo.

    - Por defecto, o campo **Conta de factura** do rexistro establécese na conta de factura establecida para o proxecto. Pode cambiar o valor do campo **Conta de factura** e despois garde o rexistro. Despois de gardar o rexistro, xa non pode actualizar o valor **Conta de factura**. Se debe actualizar o valor **Conta de factura** para o requisito de artigo, elimine o requisito de artigo existente e, a continuación, cree un novo que teña o valor desexado.
    - Por defecto, o campo **Cliente** para o requisito do artigo establécese en función do valor **Cliente predeterminado** que se establece na páxina **Xestión de proxectos e parámetros contables**.

    Cando se garda o rexistro de requisitos do artigo, o sistema asóciao ao rexistro de cabeceira **Pedido de venda de requisitos de artigo**. Se ningunha cabeceira de pedido de venda aberto ten a conta de factura seleccionada, o sistema creará unha e asociará a ela a liña de requisitos de artigo.

> [!NOTE]
> Os requisitos de artigo sempre se facturan na conta de factura que se establece no rexistro. Actualmente, o sistema non admite regras de asignación de fondos que teñan requisitos de artigo e non dividirá a contabilización en función da configuración das regras de asignación de fondos.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Crear un requisito de artigo a partir dun rexistro de previsión de artigos

Para crear un requisito de artigo a partir dun rexistro de previsión de artigos, siga estes pasos.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos** e seleccione o rexistro de proxecto.
1. No separador **Plan**, seleccione **Previsións de artigos**.
1. Crear un novo rexistro de previsión de artigo.
1. Opcional: no separador **Proxecto**, no campo **Fonte de financiamento**, seleccione a conta de factura desexada.
1. Seleccione **Crear requisito de artigo**, e confirme a mensaxe que recibe.

    > [!NOTE]
    > O sistema copia o valor de **Fonte de financiamento** desde o rexistro de previsión de artigo ata o rexistro de requisito de artigo recentemente creado.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Conta de factura predeterminada cando o sistema crea automaticamente un requisito de artigo desde unha liña de orde de compra

Se a opción **Crear requisito de artigo** está definida en **Si** na páxina **Xestión de proxectos e parámetros contables**, o sistema crea automaticamente un requisito de artigo cando se garda unha nova liña de pedido de compra do proxecto. Por defecto, os campos **Conta de factura** e **Requisito de artigo** defínense co valor do campo **Conta de factura predeterminada** no rexistro do proxecto. Actualmente, o sistema non admite a actualización nin o cambio da conta de factura para rexistros deste tipo.
