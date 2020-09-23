---
title: Escenarios de varias moedas (versión 3.x)
description: Este tema fornece información sobre escenarios de varias moedas.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4b589142-952d-4121-ab5c-3aa7a85690e2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9dbd7755e2dc4bd33f264feb7d8bf9f2a4a0787
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751348"
---
# <a name="multiple-currency-scenarios"></a>Escenarios de varias moedas

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 ten dous conceptos de moedas:

- **Moeda de transacción** - A moeda na que se produce unha transacción. 
- **Moeda base** - A moeda da instancia de Dynamics 365. Esta moeda configúrase cando se fornece unha instancia de Dynamics 365. Non se pode modificar.

Por exemplo, Contoso EU vendeu 100 camisetas a un cliente no Reino Unido por 15 libras esterlinas (GBP) cada unha. Na seguinte táboa móstrase como se rexistra esta transacción na entidade Pedir produto.

| Produto | Cantidade | Prezo por unidade | Moeda | Importe | Taxa de cambio | Prezo por unidade (base)| Cantidade (base)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Camiseta | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 $               | 1725 $       |

A columna **Moeda** mostra a moeda da transacción, que é a moeda na que se produciu a venda. A columna **Taxa de cambio** é o tipo de cambio entre a moeda da transacción e a moeda base. A moeda base é o dólar estadounidense (USD). Esta moeda base configurouse cando se forneceu unha instancia de Dynamics 365.
Como mostra a táboa, todas as transaccións rexístranse tanto na moeda da transacción como na moeda base. Dynamics 365 usa o tipo de cambio de moeda para calcular os importes da moeda base.

## <a name="project-service-automation-extensions"></a>Instalar extensións de Project Service Automation

Dynamics 365 Project Service Automation inflúe na moeda da transacción, porque as transaccións comerciais adoitan ter dous aspectos: custo e vendas.

Considéranse transaccións comerciais as seguintes entidades:

- Detalle da liña da oferta
- Detalle da liña de contrato do proxecto
- Liña de estimación
- Liña de diario
- Detalle da liña de factura
- Real

En cada unha destas entidades, hai un rexistro que representa o importe de custo ou o importe de vendas. En canto a calquera entidade de Dynamics 365 que teña un campo **Cantidade**, cada rexistro inclúe cantidades na moeda da transacción e na moeda base. 

PSA amplía o concepto de moeda da transacción para custo e vendas das seguintes formas:

- A moeda da transacción do custo para as transaccións de tempo sempre provén da moeda da unidade da organización que posúe ou xestiona o proxecto. Esta unidade da organización coñécese como unidade de contratación.
- A moeda da transacción de vendas para as transaccións de tempo e gasto sempre provén da moeda do contrato do proxecto.
- A moeda da transacción de custo para gastos provén da moeda na que se creou a entrada de gasto.

## <a name="multiple-currency-scenario"></a>Escenario de varias moedas

Esta sección describe un exemplo dun proxecto que Contoso UK entrega para un cliente que se chama Fabrikam, de Xapón. Móstrase como se configurou o escenario:

1. Configúranse GBP e iens xaponeses (JPY) en **Configuración** \> **Xestión de empresa** \> **Moedas**. 
2. Configúrase unha conta de cliente que leva o nome **Fabrikam - Xapón** e selecciónase JPY como moeda na conta.
3. Configúrase unha unidade da organización que leva o nome **Contoso Reino Unido** e selecciónase GBP como moeda.
4. Créase un contrato de proxecto, onde **Contoso Reino Unido** se especifica como unidade contratante e **Fabrikam - Xapón** se especifica como cliente.
5. Créanse liñas de contrato do proxecto a partir dos arranxos de facturación das distintas clases de transacción do proxecto, como a facturación para tempo fronte a facturación para gastos.
6. Créase un proxecto onde **Contoso Reino Unido** se especifica como unidade contratante. Este proxecto créase e asígnase ás liñas de contrato do proxecto.


Durante a estimación que usa o detalle da liña de oferta, o detalle da liña de contrato do proxecto ou na liña de estimación da programación, sempre se crean dous rexistros na entidade. Un rexistro é para o custo e o outro rexistro é para as vendas.

- Por defecto, a moeda da transacción no rexistro de custo establécese na moeda da unidade de contratación do proxecto. Neste exemplo, a moeda é GBP.
- Por defecto, a moeda da transacción no rexistro de vendas establécese na moeda do contrato do proxecto. Neste exemplo, a moeda é JPY.

Cando se crean datos reais para tempo usando a entrada de tempo ou a liña de diario, prodúcese o seguinte comportamento:

- Por defecto, a moeda da transacción no rexistro de custo establécese na moeda da unidade de contratación do proxecto.
- Por defecto, a moeda da transacción no rexistro de vendas establécese na moeda do contrato do proxecto.

Cando se crean datos reais para gastos mediante entrada de gasto ou a liña de diario, prodúcese o seguinte comportamento:

- Pode rexistrar o importe do gasto en calquera moeda. Seleccione a moeda usando o selector de moeda na páxina **Entrada de gasto** ou na páxina **Liña de diario**. Por defecto, a moeda da transacción para o rexistro de custo establécese na moeda da entrada de gasto. 
- Por defecto, a moeda da transacción para o rexistro de vendas é a moeda do contrato do proxecto. Para establecer esta moeda, o sistema converte primeiro o importe da transacción na moeda que o usuario introduciu na moeda base. Despois converte o importe á moeda do contrato do proxecto. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Cálculo de agrupamentos cando se rexistran datos reais do proxecto en varias moedas de transacción

Dynamics 365 xestiona automaticamente os agrupamentos de importes en diferentes moedas. Este é un exemplo.

| Clase de transacción | Tipo de transacción| Date   | Recurso | Categoría da transacción | Cantidade | Prezo por unidade | Importe      | Taxa de cambio | Cantidade en base |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Vendas sen facturar   | 14-xun | Henrique  |                      | 8 horas    | 20.000 JPY    | 160.000 JPY | 123           | 1300,81 USD    |
| Time              | Vendas sen facturar   | 15-xun | Henrique  |                      | 8 horas    | 20.000 JPY    | 160.000 JPY | 123           | 1300,81 USD    |
| Gasto           | Vendas sen facturar   | 16-xun | Henrique  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Gasto           | Vendas sen facturar   | 17-xun | Henrique  | Aluguer de coche           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Para calcular o valor total de vendas sen facturar no proxecto, pode crear un campo de agrupamento para o campo **Cantidade** en todos os datos reais de vendas sen facturar. O campo de agrupamento é unha construción de Dynamics 365 que permite fórmulas rápidas sobre rexistros relacionados.
