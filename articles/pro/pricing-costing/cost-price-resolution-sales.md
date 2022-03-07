---
title: Resolver prezos de custo en estimacións e datos reais de proxecto
description: Este tema ofrece información sobre como se resolven os prezos de custo das estimacións e dos datos reais do proxecto.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997559"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Resolver prezos de custo en estimacións e datos reais de proxecto 

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Para resolver os prezos de custo e a lista de prezos de custo para estimacións e datos reais, o sistema utiliza a información dos campos **Data**, **Moeda** e **Unidade de contratación** do proxecto relacionado. Despois de resolverse a lista de prezos de custo, a aplicación resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para tempo

As liñas de estimacións para o tempo refírense aos detalles da liña de oferta e contrato para as atribucións de tempo e recursos nun proxecto.

Despois de resolver unha lista de prezos de custo, os campos **Función** e **Unidade de Recursos** da liña de estimación para o tempo coinciden coas liñas de prezo da función na lista de prezos. Esta coincidencia supón que está a usar as dimensións de prezos estándar para o custo da man de obra. Se configurou o sistema para que coincida cos campos en lugar de ou ademais de **Rol** e **Unidade de Recursos**, usarase unha combinación diferente para recuperar unha liña de prezo de rol coincidente. Se a aplicación atopa unha liña de prezo de rol que ten unha taxa de custo para a combinación de **Rol** e **Unidade de recursos**, esa é a taxa de custo predeterminada. Se a aplicación non pode coincidir cos valores de **Rol** e **Unidade de recursos**, recupera as liñas de prezo de rol cun rol coincidente, pero valores nulos de **Unidade de recursos**. Despois de ter un rexistro de prezos de rol coincidente, a taxa de custo predefínese a partir dese rexistro. 

> [!NOTE]
> Se configura unha priorización diferente de **Rol** e **Unidade de recursos** ou se ten outras dimensións con maior prioridade, este comportamento cambiará en consecuencia. O sistema recupera os rexistros de prezos de rol con valores que coinciden con cada un dos valores da dimensión de prezos por orde de prioridade con filas que teñen valores nulos para as últimas dimensións.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para gasto

As liñas de estimacións para o gasto refírense aos detalles da liña de oferta e contrato para gastos e as liñas de estimación de gasto nun proxecto.

Despois de resolverse unha lista de prezos de custos, o sistema usa unha combinación dos campos **Categoría** e **Unidade** da liña de estimación de gastos para comparar coas liñas de **Categoría de prezo** na lista de prezos resolta. Se o sistema atopa unha liña de prezo de categoría que ten unha taxa de custo para a combinación de **Categoría** e **Unidades**, esa é a taxa de custo predefinida. Se o sistema non pode facer coincidir os valore de **Categoría** e **Unidade** ou se é capaz de atopar unha liña de prezo de categoría coincidente, pero o método de fixación do prezo non o é **Prezo por unidade**, a taxa de custo é cero (0) por defecto.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para material

As liñas de estimación para material refírense aos detalles da liña de oferta e de contrato para os materiais e as liñas de estimación de material dun proxecto.

Despois de resolverse unha lista de prezos de custo, o sistema usa unha combinación dos campos **Produto** e **Unidade** na liña de estimación para que unha estimación material coincida coas liñas de **Elementos da lista de prezos** na lista de prezos resolta. Se o sistema atopa unha liña de prezo do produto que ten unha taxa de custo para a combinación de campos **Produto** e **Unidade**, a taxa de custo está predefinida. Se o sistema non pode facer coincidir os valores de **Produto** e **Unidade**, ou se pode atopar unha liña de elemento da lista de prezos coincidente pero o método de fixación de prezos baséase no custo estándar ou no custo actual e ningún deles está definido no produto, o custo unitario será por defecto cero.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
