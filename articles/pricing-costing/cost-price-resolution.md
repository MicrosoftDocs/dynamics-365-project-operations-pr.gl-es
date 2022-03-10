---
title: Resolución de prezos de custo para estimacións e datos reais
description: Este tema ofrece información sobre como se resolven os prezos de custo para as estimacións e os datos reais.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003679"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Resolución de prezos de custo para estimacións e datos reais

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Para resolver os prezos de custo e a lista de prezos de custo para estimacións e datos reais, o sistema utiliza a información dos campos **Data**, **Moeda** e **Unidade de contratación** do proxecto relacionado. Despois de resolverse a lista de prezos de custo, a aplicación resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para tempo

As liñas de estimacións para o tempo refírense aos detalles da liña de oferta e contrato para as atribucións de tempo e recursos nun proxecto.

Despois de resolver unha lista de prezos de custo, o sistema utiliza os campos **Rol**, **Empresa de recursos** e **Unidade de recursos** da liña de estimación para que o tempo coincida coas liñas de prezo de rol na lista de prezos. Esta coincidencia supón que está a usar unhas dimensións de prezos listas para usar para o custo de man de obra. Se configurou o sistema para que coincida cos campos en lugar de ou ademais de **Rol**, **Empresa de recursos** e **Unidade de recursos**, usarase unha combinación diferente para recuperar unha liña de prezo de rol coincidente. Se a aplicación atopa unha liña de prezo de rol que ten unha taxa de custo para a combinación de **Rol**, **Empresa de recursos** e **Unidade de recursos**, esa é a taxa de custo predeterminada. Se a aplicación non pode facer coincidir exactamente a combinación de **Rol**, **Empresa de recursos** e **Unidade de recursos**, recuperará liñas de prezo de rol cun valor de rol coincidente, pero ten valores nulos para **Unidade de recursos** e **Empresa de recursos**. Despois de atopar un rexistro de prezo de rol coincidente cun valor de prezo de rol coincidente, a taxa de custo é a predefinida nese rexistro. 

> [!NOTE]
> Se configura unha priorización diferente de **Rol**, **Empresa de recursos** e **Unidade de recursos** ou se ten outras dimensións con maior prioridade, este comportamento cambiará en consecuencia. O sistema recupera os rexistros de prezos de rol con valores que coinciden con cada un dos valores da dimensión de prezos por orde de prioridade con filas que teñen valores nulos para as dimensións que quedan en último lugar na orde de prioridade.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para gasto

As liñas de estimacións para o gasto refírense aos detalles da liña de oferta e contrato para gastos e as liñas de estimación de gasto nun proxecto.

Despois de resolver unha lista de prezos de custo, o sistema utiliza unha combinación dos campos **Categoría** e **Unidade** da liña de estimación para que un gasto coincida coas liñas de **Prezo de categoría** na lista de prezos resolta. Se o sistema atopa unha liña de prezo de categoría que ten unha taxa de custo para a combinación de **Categoría** e **Unidades**, esa é a taxa de custo predefinida. Se o sistema non pode coincidir cos valores de **Categoría** e **Unidade** ou se é capaz de atopar unha liña de prezo de categoría coincidente, pero o método de fixación de prezos non o é **Prezo por unidade**, a taxa de custo está predefinida en cero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para material

As liñas de estimación para material refírense aos detalles da liña de oferta e de contrato para os materiais e as liñas de estimación de material dun proxecto.

Despois de resolverse unha lista de prezos de custo, o sistema usa unha combinación dos campos **Produto** e **Unidade** na liña de estimación para que unha estimación material coincida coas liñas de **Elementos da lista de prezos** na lista de prezos resolta. Se o sistema atopa unha liña de prezo do produto que ten unha taxa de custo para a combinación de campos **Produto** e **Unidade**, a taxa de custo está predefinida. Se o sistema non pode facer coincidir os valores de **Produto** e **Unidade**, o custo unitario por defecto é cero. Este valor predefinido tamén se producirá se hai unha liña de elemento da lista de prezos coincidente, pero o método de fixación de prezos baséase nun custo estándar ou un custo actual que non está definido no produto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
