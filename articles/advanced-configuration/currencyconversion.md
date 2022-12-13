---
title: Configura a conversión de moeda para calcular os prezos de venda a partir das taxas de custo
description: Este artigo explica como configurar o comportamento de conversión de moeda que se utilizará en Microsoft Dynamics 365 Project Operations cando se xeren transaccións de vendas a partir de transaccións de custo.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816689"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Configura a conversión de moeda para calcular os prezos de venda a partir das taxas de custo

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

En Microsoft Dynamics 365 Project Operations, os prezos de venda das categorías de gastos pódense configurar como valores numéricos ou poden configurarse para que se calculen en función do custo en que se incorre.

Cando se configuran para calculalos en función do custo incorrido, están dispoñibles as seguintes opcións:

- Ao custo
- Marca a porcentaxe sobre o custo

Nos escenarios nos que o custo do gasto se incorre nunha moeda que difire da moeda de vendas para o contrato do proxecto, é necesaria a conversión de moeda para calcular o prezo de venda en función do custo.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportamento de conversión de moeda que utiliza tipos de cambio Dataverse nativos

De forma predeterminada, Project Operations usa os tipos de cambio de moeda almacenados na táboa Moeda en Dataverse. Para configurar Project Operations para que utilicen tipos de cambio nativos para calcular os prezos de venda a partir do custo, siga estes pasos.

1. Vaia a **Operacións do proxecto \> Configuración \> Parámetros**.
1. Abre a páxina de detalles do **parámetro do proxecto** .
1. Establece o campo  **Lóxica de conversión de moeda**  nun valor en branco.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportamento de conversión de moeda que utiliza os tipos de cambio das aplicacións financeiras e de operacións

Os tipos de cambio da táboa Moeda que están dispoñibles nativamente en Dataverse non entran en vigor. Polo tanto, é posible que non sempre se adapten aos requisitos que ten para o cálculo dos prezos de venda a partir das taxas de custo.

Podes utilizar os tipos de cambio do contorno financeiro e operativo para calcular o prezo de venda na moeda de vendas a partir dunha taxa de custo na moeda de custo. Para configurar este comportamento de conversión de moeda, siga estes pasos.

1. Na páxina **Parámetros do proxecto**, engade o campo **Lóxica de conversión de moeda** . A continuación, garda e publica a personalización.
1. Vaia a **Operacións do proxecto \> Configuración \> Parámetros**.
1. Abre a páxina de detalles do **parámetro do proxecto** . 
1. Establece o campo **Comportamento de conversión de moeda** en **Ampliado coa opción predeterminada**.
1. Dálle permiso ao **usuario da aplicación de escritura dual** rol de seguranza **Lectura global**  ás seguintes táboas:

    - msdyn\_ taxas de cambio de divisas
    - msdyn\_ pares de cambio de divisas
    - msdyn\_ tipos de intercambio

1. No teu entorno financeiro e operativo, executa os seguintes mapas de dobre escritura coa sincronización inicial:

    - Tipo de tipo de cambio (msdyn\_ exchangeratetypes)
    - Par de divisas do tipo de cambio (msdyn\_ currencyexchangeratepairs)
    - Tipos de cambio de CDS (msdyn\_ taxas de cambio de divisas)

Despois de completar estes cambios, a escritura dual fará que os tipos de cambio do entorno financeiro e operativo estean dispoñibles en Dataverse. A continuación, Project Operations utilizará eses tipos de cambio para converter os tipos de custo na moeda de vendas do contrato.

> [!NOTE]
> Este comportamento de conversión de moeda só aplícase ao cálculo dos prezos de venda a partir das taxas de custo. Non se utilizará para calcular xenericamente os valores da moeda base. Os valores da moeda base sempre usarán tipos de cambio Dataverse nativos, independentemente de que completes este procedemento.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
