---
title: Determinar os prezos de venda das estimacións e reais do proxecto
description: Este artigo ofrece información sobre como se determinan os prezos de venda para as estimacións e os reais do proxecto.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410116"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Determinar os prezos de venda das estimacións e reais do proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Para determinar os prezos de venda en estimacións e reais en Microsoft Dynamics 365 Project Operations, o sistema utiliza primeiro a data e a moeda na estimación entrante ou no contexto real para determinar a lista de prezos de venda. No contexto real especificamente, o sistema usa o **Data da transacción** campo para determinar que lista de prezos é aplicable. Despois de determinar a lista de prezos de venda, o sistema determina a tarifa de vendas ou de facturación.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinación das taxas de vendas en liñas reais e estimativas para o tempo

Estimar contexto para **Tempo** refírese a:

- Detalles da liña de cotización para **Tempo**.
- Detalles da liña de contrato para **Tempo**.
- Asignacións de recursos nun proxecto.

Contexto real para **Tempo** refírese a:

- Liñas do diario de entrada e corrección para **Tempo**.
- Liñas de diario que se crean cando se envía unha entrada de tempo.
- Detalles da liña de factura para **Tempo**. 

Despois de determinar unha lista de prezos para as vendas, o sistema completa os seguintes pasos para introducir a tarifa de factura predeterminada.

1. O sistema coincide coa combinación de **Papel** e **Unidade de Recursos** campos no contexto estimativo ou real para **Tempo** contra as liñas de prezos do rol da lista de prezos. Esta coincidencia supón que estás a usar as dimensións de prezos listas para as tarifas de factura. Se configuraches o prezo para que estea baseado en campos distintos ou ademais de **Papel** e **Unidade de Recursos**, esa combinación de campos úsase para recuperar unha liña de prezos de función coincidente.
1. Se o sistema atopa unha liña de prezo de función que teña unha taxa de facturación para o **Papel** e **Unidade de Recursos** combinación, esa taxa de factura utilízase como tarifa de factura predeterminada.
1. Se o sistema non pode coincidir co **Papel** e **Unidade de Recursos** valores, recupera liñas de prezos de función que teñen valores coincidentes para o **Papel** campo pero valores nulos para o **Unidade de Recursos** campo. Despois de que o sistema atope un rexistro de prezo de función coincidente, a taxa de facturación dese rexistro empregarase como tarifa de factura predeterminada. Esta coincidencia supón unha configuración lista para a prioridade relativa de **Papel** contra **Unidade de Recursos** como dimensión de prezos de venda.

> [!NOTE]
> Se configura unha priorización diferente do **Papel** e **Unidade de Recursos** campos ou se ten outras dimensións que teñan maior prioridade, o comportamento anterior cambiará en consecuencia. O sistema recupera rexistros de prezos de función que teñen valores que coinciden con cada valor de dimensión de prezos por orde de prioridade. As filas que teñen valores nulos para esas dimensións son as últimas.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinación das taxas de vendas en liñas reais e estimativas para Gastos

Estimar contexto para **Gasto** refírese a:

- Detalles da liña de cotización para **Gasto**.
- Detalles da liña de contrato para **Gasto**.
- Liñas de estimación de gastos nun proxecto.

Contexto real para **Gasto** refírese a:

- Liñas do diario de entrada e corrección para **Gasto**.
- Liñas de diario que se crean cando se envía unha entrada de gasto.
- Detalles da liña de factura para **Gasto**. 

Despois de determinar unha lista de prezos para as vendas, o sistema completa os seguintes pasos para introducir o prezo unitario de venda predeterminado.

1. O sistema coincide coa combinación de **Categoría** e **Unidade** campos da liña de estimación para **Gasto** contra as liñas de prezos da categoría da lista de prezos.
1. Se o sistema atopa unha liña de prezos de categoría que teña unha taxa de vendas para o **Categoría** e **Unidade** combinación, esa taxa de vendas úsase como taxa de vendas predeterminada.
1. Se o sistema atopa unha liña de prezos de categoría coincidente, pódese utilizar o método de prezos para introducir o prezo de venda predeterminado. A seguinte táboa mostra o comportamento predeterminado dos prezos de gastos en Operacións do proxecto.

    | Contexto | Método de cálculo de prezos | Prezo predeterminado |
    | --- | --- | --- |
    | Estimación | Prezo por unidade | Baseado na liña de prezos da categoría. |
    |        | Ao custo | 0.00 |
    |        | Sobreprezo sobre o custo | 0.00 |
    | Dato real | Prezo por unidade | Baseado na liña de prezos da categoría. |
    |        | Ao custo | En función do custo real relacionado. |
    |        | Sobreprezo sobre o custo | Aplícase un recargo, tal e como se define na liña de prezos da categoría, á taxa de custo unitario do custo real relacionado. |

1. Se o sistema non pode coincidir co **Categoría** e **Unidade** valores, a taxa de vendas está establecida en **0** (cero) por defecto.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinación das taxas de venda nas liñas reais e estimativas de Material

Estimar contexto para **Material** refírese a:

- Detalles da liña de cotización para **Material**.
- Detalles da liña de contrato para **Material**.
- Liñas de estimación de material nun proxecto.

Contexto real para **Material** refírese a:

- Liñas do diario de entrada e corrección para **Material**.
- Liñas de diario que se crean cando se envía un rexistro de uso de material.
- Detalles da liña de factura para **Material**. 

Despois de determinar unha lista de prezos para as vendas, o sistema completa os seguintes pasos para introducir o prezo unitario de venda predeterminado.

1. O sistema coincide coa combinación de **Produto** e **Unidade** campos da liña de estimación para **Material** contra as liñas do artigo da lista de prezos da lista de prezos.
1. Se o sistema atopa unha liña de artigos da lista de prezos que ten unha taxa de vendas para o **Produto** e **Unidade** combinación, e se o método de prezos é **Importe da moeda**, utilízase o prezo de venda que se especifica na liña da lista de prezos. 
1. Se o **Produto** e **Unidade** os valores dos campos non coinciden ou se o método de prezos é distinto **Importe da moeda**, a taxa de vendas está establecida en **0** (cero) por defecto. Este comportamento ocorre porque Project Operations só admite o **Importe da moeda** método de prezos dos materiais que se usan nun proxecto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
