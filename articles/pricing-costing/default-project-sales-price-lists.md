---
title: Listas de prezos predefinidas
description: Este artigo ofrece información sobre as vendas predeterminadas e as listas de prezos de custo en Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410260"
---
# <a name="default-price-lists"></a>Listas de prezos predefinidas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

## <a name="sales-price-lists"></a>Listas de prezos de vendas

Todas as ofertas e contratos do proxecto en Dynamics 365 Project Operations conteñen unha lista de prezos de venda predefinida. 

### <a name="price-list-default-on-project-quotes"></a>Lista de prezos predefinida nas ofertas de proxecto
O sistema completa o seguinte proceso para determinar que lista de prezos predefinirá nunha oferta de proxecto:

1. O sistema analiza as listas de prezos que se anexan ás listas de prezos de proxecto da conta. 
1. Se non hai listas de prezos do proxecto anexas ao rexistro da conta, o sistema mira as listas de prezos de venda anexas aos parámetros do proxecto que coincidan coa moeda da cotización do proxecto.
1. A seguir, o sistema comproba a efectividade da data das listas de prezos que coinciden co intervalo de datas da oferta do proxecto. Especificamente, a data na que se creou a oferta.
1. Se hai varias listas de prezos efectivas para a data da oferta do proxecto, todas as listas de prezos predefínense na oferta do proxecto.
1. Se non hai listas de prezos en vigor para a data da oferta do proxecto, non hai ningunha lista de prezos predefinida na oferta do proxecto. Na oferta do proxecto aparecerá unha mensaxe de advertencia. A mensaxe indica que os datos reais e as estimacións do proxecto non terán prezo porque non hai listas de prezos do proxecto anexas.

### <a name="price-list-default-on-project-contracts"></a>Lista de prezos predefinida nos contratos de proxecto 
O sistema completa o seguinte proceso para determinar que lista de prezos predefinirá nun contrato de proxecto:

1. Se o contrato se crea a partir dunha oferta, as listas de prezos do proxecto cópianse por separado e anéxanse ao contrato do proxecto.
1. Se o contrato se crea desde cero, o sistema examina as listas de prezos que se anexan ás listas de prezos do proxecto da conta. Se non hai listas de prezos de proxecto anexadas ao rexistro da conta, o sistema busca listas de prezos de vendas anexas aos parámetros do proxecto que coinciden coa moeda do contrato do proxecto.
1. A seguir, o sistema comproba a efectividade da data das listas de prezos que coinciden co intervalo de datas do contrato do proxecto. Especificamente, a data na que se creou o contrato.
1. Se hai varias listas de prezos efectivas para a data do contrato do proxecto, todas as listas de prezos predefínense no contrato.
1. Se non hai listas de prezos en vigor para a data do contrato, non hai ningunha lista de prezos predefinida para o contrato. No contrato do proxecto aparecerá unha mensaxe de advertencia. A mensaxe indica que os datos reais e as estimacións do proxecto non terán prezo porque non hai listas de prezos do proxecto anexas.

## <a name="cost-price-lists"></a>Listas de prezos de custo

As listas de prezos de custo non están predefinidas en ningunha entidade en Project Operations. A determinación da lista de prezos de custo a utilizar para os custos do proxecto faise sempre por transacción. O sistema completa o seguinte proceso para determinar que lista de prezos se usará para os custos do proxecto:

1. O sistema analiza as listas de prezos que se anexan á unidade organizativa de contratación do proxecto.
1. A continuación, o sistema analiza a data de efectividade das listas de prezos que coinciden coa data do contexto da estimación entrante ou do contexto real.

    - *Contexto estimativo* refírese a calquera dos tres contextos de estimación nas operacións do proxecto:

        - Liña de estimación de proxecto
        - Detalle da liña da oferta
        - Detalle da liña de contrato

    - *Contexto real* refírese a calquera das tres fontes de datos reais nas operacións do proxecto:

       - Liñas de diario de entrada que se crean manualmente ou liñas de diario de corrección que se crean nun diario de corrección
       - Liñas de diario que se crean durante o envío de rexistros de tempo, gasto ou uso de material
       - Detalle da liña de factura

    Cando as operacións do proxecto coincidan coa data de efectividade da liña de rexistro de entrada ou o detalle da liña de factura no *contexto real*, usa o **Data da transacción** campo.

    - Se varias listas de prezos son efectivas para a data do contexto da estimación entrante ou do contexto real, selecciónase a lista de prezos creada máis recentemente.
    - Se non se anexa ningunha lista de prezos á unidade organizativa de contratación do proxecto, o sistema analiza as listas de prezos de custo que se anexan aos parámetros do proxecto que coincidan coa moeda do proxecto.

## <a name="enable-multi-currency-cost-price-list"></a>Activar lista de prezos de custo de varias divisas

Esta configuración pódese atopar en **Configuración** \> **Parámetros**. O valor predefinido é **Non**.

Cando esta configuración está activada (é dicir, o valor establécese en **Si**), o sistema se comporta do seguinte xeito:

- Permite asociar listas de prezos de custo en calquera moeda coa unidade organizativa. Por exemplo, unha lista de prezos de custo na moeda EUR pódese anexar a unha unidade organizativa na moeda USD. O sistema seguirá validando que as listas de prezos de custo que están anexas a unha unidade organizativa non teñen datas de vixencia superpostas.
- Valida que as listas de prezos de custo que se anexan aos parámetros do proxecto non teñen unha data de efectividade superposta, aínda que teñan moedas diferentes. Este comportamento difire do comportamento predeterminado (é dicir, o comportamento cando se establece o valor en **Non**). No comportamento predeterminado, só as listas de prezos de custo que teñan o **mesmo** a moeda está validada para que as datas non se solapen.
- Para un contexto de transacción entrante, determina a lista de prezos de custo baseándose só na data de vixencia. Este comportamento difire do comportamento predeterminado, onde o sistema selecciona a lista de prezos de custo que coincide tanto coa moeda do proxecto como coa data de vixencia.

Debido a estes cambios no comportamento, os clientes de Project Operations poderán manter unha lista de prezos de custo global que será relevante para toda a empresa. Non terán que ter listas de prezos en cada moeda de operacións. A lista de prezos global terá efectos de data e permitirá configurar as taxas de custo en calquera moeda para unha combinación específica de valores de dimensións de prezos. A moeda da lista de prezos de custo só se usa para introducir valores predeterminados cando **Prezos dos roles**, **das categorías**, e **Lista de prezos** créanse rexistros de elementos. Non se utilizará para determinar a lista de prezos.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
