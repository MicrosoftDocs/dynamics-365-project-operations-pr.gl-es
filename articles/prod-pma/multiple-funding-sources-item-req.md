---
title: Requisitos de elementos para contratos de proxectos con múltiples fontes de financiamento
description: Este artigo ofrece información sobre como configurar e usar os requisitos de elementos con varias fontes de financiamento.
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

- **Fonte de financiamento** – A entidade que financia a obra do contrato do proxecto. Esta entidade pode ser unha organización interna ou unha conta de factura externa (cliente ou subvención).
- **Cliente do proxecto** – A entidade á que se entrega o traballo do proxecto.
- **Conta de factura** – A entidade externa que sufraga a obra do proxecto.

## <a name="example"></a>Exemplo

Contoso gañou un contrato de renovación de equipos con dous dos seus clientes: Adatum US e Adatum Corporate. O contrato inclúe hardware e servizos de instalación que serán entregados a Adatum US (o cliente do proxecto). O hardware será financiado por Adatum Corporate (conta de factura 1), e os traballos de instalación serán financiados por Adatum US (conta de factura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configura regras predeterminadas da conta de factura para os requisitos dos artigos

### <a name="prerequisites"></a>Requisitos previos

- Microsoft Dynamics 365 Finanzas **versión 10.0.27 ou posterior** é necesario para utilizar requisitos de artigo que teñan varias contas de factura.
- O seu administrador do sistema debe activar o **Permitir os requisitos de elementos con varias fontes de financiamento para os escenarios abastecidos ou baseados na produción de Project Operations** característica no **Xestión de características** espazo de traballo.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configura as regras predeterminadas da conta de factura

Para configurar as regras predeterminadas para a conta de factura, siga estes pasos.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Parámetros de Xestión e contabilidade de proxectos**.
1. No **Xeral** ficha, na **Pedidos de venda e requisitos de artigos** sección, configure o **Permitir proxectos con múltiples fontes de financiamento** opción a **Si**.
1. No **Cliente predeterminado** campo, especifique de onde procede o cliente de entrega do proxecto sobre o requisito do artigo por defecto:

    - **Da fonte de financiamento** – O cliente de entrega do proxecto por defecto procede da fonte de financiamento. Se co contrato do proxecto están asociadas varias fontes de financiamento, utilizarase a primeira fonte de financiamento da lista.
    - **Do proxecto** – O cliente de entrega do proxecto predeterminado procede do cliente seleccionado no **Conta de rexistro do proxecto** campo.

1. Opcional: establece ou cambia a conta de factura predeterminada nos rexistros do proxecto:

    1. Ir a **Xestión de proxectos e contabilidade** \> **Proxectos** \> **Todos os proxectos**, e abra os detalles do rexistro do proxecto.
    2. No **Xeral** ficha, configure ou actualice **Conta de factura predeterminada** campo. A conta que especifique utilizarase como conta de factura predeterminada para os requisitos de artigos novos que se crean para o proxecto. Se deixa o campo en branco, a conta de factura da fonte de financiamento do primeiro contrato do proxecto empregarase por defecto. Non obstante, os usuarios poderán cambiar a conta cando garden o rexistro.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Seleccione a conta de factura que quere utilizar cando cree un requisito de artigo

Para seleccionar a conta de factura a utilizar cando cree un requisito de artigo, siga estes pasos.

1. Ir a **Xestión de proxectos e contabilidade** \> **Proxectos** \> **Todos os proxectos**, e seleccione o rexistro do proxecto.
1. No **Planificar** ficha, seleccione **Requisitos dos elementos**.
1. Crea un novo rexistro de requisitos de elementos.

    - Por defecto, o **Conta de factura** campo do rexistro establécese na conta de factura establecida para o proxecto. Podes cambiar o valor do **Conta de factura** campo e despois garde o rexistro. Despois de gardar o rexistro, xa non podes actualizar **Conta de factura** valor. Se debes actualizar o **Conta de factura** valor para o requisito de elemento, elimine o requisito de elemento existente e, a continuación, cree un novo que teña o valor desexado.
    - Por defecto, o **Cliente** campo para o requisito do elemento establécese en función do **Cliente predeterminado** valor que se establece no **Xestión de proxectos e parámetros contables** páxina.

    Cando se garda o rexistro de requisitos do elemento, o sistema asóciao co **Pedido de venda de requisitos de artigo** rexistro de cabeceira. Se ningunha cabeceira de pedido de venda aberta ten a conta de factura seleccionada, o sistema creará unha e asociará a liña de requisitos de artigo.

> [!NOTE]
> Os requisitos de elementos sempre se facturan na conta de factura que se establece no rexistro. O sistema actualmente non admite regras de asignación de fondos que teñan requisitos de elementos e non dividirá a publicación en función da configuración das regras de asignación de fondos.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Crea un requisito de elemento a partir dun rexistro de previsión de elementos

Para crear un requisito de elemento a partir dun rexistro de previsión de elementos, siga estes pasos.

1. Ir a **Xestión de proxectos e contabilidade** \> **Proxectos** \> **Todos os proxectos** e seleccione o rexistro do proxecto.
1. No **Planificar** ficha, seleccione **Previsións de elementos**.
1. Crea un novo rexistro de previsión de elementos.
1. Opcional: no **Proxecto** ficha, na **Fonte de financiamento** campo, seleccione a conta de factura desexada.
1. Seleccione **Crear requisito de elemento**, e confirma a mensaxe que recibe.

    > [!NOTE]
    > O sistema copia o **Fonte de financiamento** valor desde o rexistro de previsión de elementos ata o rexistro de requisitos de elementos recentemente creado.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Conta de factura predeterminada cando o sistema crea automaticamente un requisito de artigo desde unha liña de orde de compra

Se o **Crear requisito de elemento** opción está definida en **Si** no **Xestión de proxectos e parámetros contables** páxina, o sistema crea automaticamente un requisito de artigo cando se garda unha nova liña de pedido de compra do proxecto. Por defecto, o **Conta de factura** e **Requisito do elemento** campos están definidos co valor de **Conta de factura predeterminada** campo no rexistro do proxecto. Actualmente, o sistema non admite a actualización nin o cambio da conta de factura para rexistros deste tipo.
