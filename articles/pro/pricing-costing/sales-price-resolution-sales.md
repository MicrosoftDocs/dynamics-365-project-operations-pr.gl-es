---
title: Determinar prezos de vendas para estimacións e datos reais de proxecto
description: Este artigo ofrece información sobre como se determinan os prezos de vendas das estimacións e dos datos reais do proxecto.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475182"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Determinar prezos de vendas para estimacións e datos reais de proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Para determinar os prezos de vendas en estimacións e datos reais en Microsoft Dynamics 365 Project Operations, o sistema utiliza primeiro a data e a moeda no contexto da estimación ou dato real entrante para determinar a lista de prezos de vendas. No contexto real especificamente, o sistema usa o campo **Data da transacción** para determinar que lista de prezos é aplicable. O valor **Data da transacción** da estimación ou dato real entrante compárase cos valores de **Inicio efectivo (independente da zona horaria)** e **Fin efectivo (independente da zona horaria)** na lista de prezos. Despois de determinar a lista de prezos de vendas, o sistema determina a taxa de vendas ou factura.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinar taxas de vendas nas liñas de datos reais e estimacións para tempo

O contexto de estimación para **Tempo** refírese a:

- Detalles da liña de oferta para **Tempo**.
- Detalles da liña de contrato para **Tempo**.
- Atribucións de recursos nun proxecto.

O contexto de datos reais para **Tempo** refírese a:

- Entrada e corrección de liñas de diario para **Tempo**.
- Liñas de diario que se crean cando se envía unha entrada de tempo.
- Detalles da liña de factura para **Tempo**. 

Despois de determinar unha lista de prezos para vendas, o sistema completa os seguintes pasos para introducir a taxa de facturación predefinida.

1. O sistema fai coincidir a combinación dos campos **Rol** e **Unidade de recursos** no contexto de estimación ou dato real para **Tempo** contra as liñas de prezos do rol na lista de prezos. Esta coincidencia supón que vostede está a usar unhas dimensións de prezos listas para taxas de facturación. Se configurou os prezos para que estean baseados en campos distintos de ou ademais de **Rol** e **Unidade de recursos**, esa combinación de campos utilizarase para recuperar unha liña de prezo de rol coincidente.
1. Se o sistema atopa unha liña de prezo de rol que ten unha taxa de facturación para a combinación de campos **Rol** e **Unidade de recursos**, esa é a taxa de facturación que se utiliza como predefinida.
1. Se o sistema non pode facer coincidir cos valores de **Rol** e **Unidade de recursos**, recupera as liñas de prezo de rol que teñen valores coincidentes para o campo **Rol**, pero valores nulos para o campo **Unidade de recursos**. Despois de que o sistema atopa un rexistro de prezo de rol coincidente, a taxa de facturación utilizarase como taxa de facturación predefinida. Esta coincidencia supón unha configuración lista para usar para a prioridade relativa de **Rol** fronte a **Unidade de Recursos** como dimensión de prezos de venda.

> [!NOTE]
> Se configura unha priorización diferente dos campos **Rol** e **Unidade de recursos** ou se ten outras dimensións con maior prioridade, este comportamento cambiará en consecuencia. O sistema recupera rexistros de prezos de rol que teñen valores que coinciden con cada valor de dimensión de prezos por orde de prioridade. As filas que teñen valores nulos para esas dimensións son as últimas.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinar taxas de vendas nas liñas de datos reais e estimacións para gasto

O contexto de estimación para **Gasto** refírese a:

- Detalles da liña de oferta para **Gasto**.
- Detalles da liña de contrato para **Gasto**.
- Liñas de estimacións de gastos nun proxecto.

O contexto de dato real para **Gasto** refírese a:

- Entrada e corrección de liñas de diario para **Gasto**.
- Liñas de diario que se crean cando se envía unha entrada de gasto.
- Detalles da liña de factura para **Gasto**. 

Despois de determinar unha lista de prezos para vendas, o sistema completa os seguintes pasos para introducir o prezo de vendas da unidade predefinido.

1. O sistema fai coincidir a combinación dos campos **Categoría** e **Unidade** da liña de estimación para **Gasto** coas liñas de prezo de categoría na lista de prezos.
1. Se o sistema atopa unha liña de prezo de categoría que ten unha taxa de vendas para a combinación dos campos **Categoría** e **Unidade**, esa é a taxa de vendas que se utiliza como predefinida.
1. Se o sistema atopa unha liña de prezo de categoría coincidente, o método de fixación de prezos poderíase usar para introducir o prezo de vendas predefinido. A seguinte táboa mostra o comportamento predefinido para prezos do gasto en Project Operations.

    | Contexto | Método de cálculo de prezos | Prezo predefinido |
    | --- | --- | --- |
    | Estimación | Prezo por unidade | Baseado na liña de prezo da categoría. |
    |        | Ao custo | 0.00 |
    |        | Sobreprezo sobre o custo | 0.00 |
    | Dato real | Prezo por unidade | Baseado na liña de prezo da categoría. |
    |        | Ao custo | Baseado no dato real de custo relacionado. |
    |        | Sobreprezo sobre o custo | Aplícase un sobreprezo como se define na liña de prezo da categoría na taxa de custo unitario do dato real de custo relacionado. |

1. Se o sistema non pode facer coincidir os valores de **Categoría** e **Unidade**, a taxa de vendas establécese en **0** (cero) por defecto.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinar as taxas de vendas nas liñas de datos reais e estimacións para material

O contexto de estimación para **Material** refírese a:

- Detalles da liña de oferta para **Material**.
- Detalles da liña de contrato para **Material**.
- Liñas de estimacións de material nun proxecto.

O contexto de dato real para **Material** refírese a:

- Entrada e corrección de liñas de diario para **Material**.
- Liñas de diario que se crean cando se envía un rexistro de uso de material.
- Detalles da liña de factura para **Material**. 

Despois de determinar unha lista de prezos para vendas, o sistema completa os seguintes pasos para introducir o prezo de vendas da unidade predefinido.

1. O sistema fai coincidir a combinación dos campos **Produto** e **Unidade** na liña de estimación para **Material** coas liñas de elementos da lista de prezos da lista de prezos.
1. Se o sistema atopa unha liña de elementos de lista de prezos que ten unha taxa de vendas para a combinación dos campos **Produto** e **Unidade** e se o método de fixación de prezos é **Importe da moeda** úsase o prezo de vendas especificado na liña da lista de prezos. 
1. Se os valores dos campos **Produto** e a **Unidade** non coinciden ou se o método de prezos é distinto de **Importe da moeda**, a taxa de vendas establécese en **0** (cero) por defecto. Este comportamento ocorre porque Project Operations só admite o método de fixación de prezos **Importe da moeda** para os materiais que se usan nun proxecto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
