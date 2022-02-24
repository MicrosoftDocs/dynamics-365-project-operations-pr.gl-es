---
title: Resolver prezos de vendas para estimacións e datos reais de proxecto
description: Este tema ofrece información sobre como se resolven os prezos de venda das estimacións e dos datos reais do proxecto.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3bf4686b414300370e6b364834b33edad98b7f39
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877354"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Resolver prezos de vendas para estimacións e datos reais de proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Cando se resolvan os prezos de venda das estimacións e dos datos reais en Dynamics 365 Project Operations, o sistema utiliza por primeira vez a data e a moeda da oferta ou contrato do proxecto relacionado para resolver a lista de prezos de vendas. Despois de resolverse a lista de prezos de vendas, o sistema resolve a taxa de vendas ou factura.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Resolver taxas de vendas nas liñas de datos reais e estimacións para tempo

En Project Operations, as liñas de estimación para o tempo úsanse para indicar os detalles da liña de oferta e da liña do contrato e as atribucións de recursos no proxecto.

Despois de resolverse unha lista de prezos para vendas, o sistema completa os seguintes pasos para predefinir a taxa de facturación.

1. O sistema utiliza os campos **Rol** e **Unidade de recursos** da liña de estimación para que o tempo coincida coas liñas de prezo de rol na lista de prezos resolta. Esta coincidencia supón que está a usar unhas dimensións de prezos listas para taxas de facturación. Se configurou os prezos segundo os outros campos en lugar de ou ademais de **Rol** e **Unidade de recursos**, esa é a combinación que se utilizará para recuperar unha liña de prezo de rol coincidente.
2. Se o sistema atopa unha liña de prezo de rol que ten unha taxa de facturación para a combinación de campos **Rol** e **Unidade de recursos**, esa é a taxa de facturación predefinida.
3. Se a aplicación non pode coincidir cos valores de campo de **Rol** e **Unidade de recursos**, recupera as liñas de prezo de rol cun rol coincidente, pero valores nulos de **Unidade de recursos**. Despois de que o sistema atope un rexistro de prezo de rol coincidente, predeterminará a taxa de facturación dese rexistro. Esta coincidencia supón unha configuración lista para usar para a prioridade relativa de **Rol** fronte a **Unidade de Recursos** como dimensión de prezos de venda.

> [!NOTE]
> Se configurou unha priorización diferente de **Rol** e **Unidade de recursos** ou se ten outras dimensións con maior prioridade, este comportamento cambiará en consecuencia. O sistema recupera os rexistros de prezos de rol con valores coincidentes de cada un dos valores da dimensión de prezos por orde de prioridade con filas que teñen valores nulos para as últimas dimensións.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Resolver taxas de vendas nas liñas de datos reais e estimacións para gasto

En Project Operations, as liñas de estimación para o gasto úsanse para indicar os detalles da liña de oferta e da liña do contrato para gastos e las liñas de estimación de gasto do proxecto.

Despois de resolverse unha lista de prezos para vendas, o sistema completa os seguintes pasos para predefinir o prezo de vandas da unidae.

1. O sistema utiliza unha combinación dos campos **Categoría** e **Unidade** da liña de estimación para que un gasto coincida coas liñas de prezo de categoría na lista de prezos que se resolveu.
2. Se o sistema atopa unha liña de prezo de categoría que ten unha taxa de vendas para a combinación dos campos **Categoría** e **Unidade**, esa é a taxa de vendas predefinida.
3. Se o sistema atopa unha liña de prezo de categoría coincidente, pódese usar o prezo de vendas como método de fixación de prezos por defecto. A seguinte táboa mostra o comportamento predefinido do prezo do gasto en Project Operations.

    | Contexto | Método de cálculo de prezos | Prezo predefinido |
    | --- | --- | --- |
    | Estimación | Prezo por unidade | Baseado na liña de prezo da categoría |
    | &nbsp; | Ao custo | 0.00 |
    | &nbsp; | Sobreprezo sobre o custo | 0.00 |
    | Dato real | Prezo por unidade | Baseado na liña de prezo da categoría |
    | &nbsp; | Ao custo | Baseado no dato real de custo relacionado |
    | &nbsp; | Sobreprezo sobre o custo | Aplicar un sobreprezo como se define na liña de prezo da categoría na taxa de custo unitario do dato real de custo relacionado |

4. Se o sistema non pode facer coincidir os valores dos campos **Categoría** e **Unidade** valores, a taxa de vendas é cero (0) por defecto.

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Resolución das taxas de vendas nas liñas de datos reais e estimacións para material

En Project Operations, as liñas de estimación para material refírense aos detalles da liña de oferta e de contrato para os materiais e as liñas de estimación de material do proxecto.

Despois de resolverse unha lista de prezos para vendas, o sistema completa os seguintes pasos para predefinir o prezo de vandas da unidae.

1. O sistema usa a combinación dos campos **Produto** e **Unidade** na liña de estimación para que o material coincida coas liñas de elementos da lista de prezos da lista de prezos que se resolveu.
2. Se o sistema atopa unha liña de elementos de lista de prezos que ten unha taxa de vendas para a combinación dos campos **Produto** e **Unidade** e o método de fixación de prezos é **Importe da moeda** úsase o prezo de vendas especificado na liña da lista de prezos.
3. Se os valores dos campos **Produto** e **Unidade** non coinciden, a taxa de vendas por defecto é cero.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
