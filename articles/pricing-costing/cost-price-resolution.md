---
title: Resolución de prezos de custo para estimacións e datos reais
description: Este tema ofrece información sobre como se resolven os prezos de custo para as estimacións e os datos reais.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119687"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Resolución de prezos de custo para estimacións e datos reais

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Para resolver os prezos de custo e a lista de prezos de custo para estimacións e datos reais, o sistema utiliza a información dos campos **Data**, **Moeda** e **Unidade de contratación** do proxecto relacionado. Despois de resolverse a lista de prezos de custo, a aplicación resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para tempo

As liñas de estimacións para o tempo refírense aos detalles da liña de oferta e contrato para as atribucións de tempo e recursos nun proxecto.

Despois de resolver unha lista de prezos de custo, o sistema utiliza os campos **Rol**, **Empresa de recursos** e **Unidade de recursos** da liña de estimación para que o tempo coincida coas liñas de prezo de rol na lista de prezos. Esta coincidencia supón que está a usar unhas dimensións de prezos listas para usar para o custo de man de obra. Se configurou o sistema para que coincida cos campos en lugar de ou ademais de **Rol**, **Empresa de recursos** e **Unidade de recursos**, usarase unha combinación diferente para recuperar unha liña de prezo de rol coincidente. Se a aplicación atopa unha liña de prezo de rol que ten unha taxa de custo para a combinación de **Rol**, **Empresa de recursos** e **Unidade de recursos**, esa é a taxa de custo predeterminada. Se a aplicación non pode coincidir cos valores de **Rol**, **Empresa de recursos** e **Unidade de recursos**, recupera as liñas de prezo de rol cun rol coincidente, pero valores nulos de **Unidade de recursos**. Despois de ter un rexistro de prezos de rol coincidente, a taxa de custo predefínese a partir dese rexistro. 

> [!NOTE]
> Se configura unha priorización diferente de **Rol**, **Empresa de recursos** e **Unidade de recursos** ou se ten outras dimensións con maior prioridade, este comportamento cambiará en consecuencia. O sistema recupera os rexistros de prezos de rol con valores que coinciden con cada un dos valores da dimensión de prezos por orde de prioridade con filas que teñen valores nulos para as últimas dimensións.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para gasto

As liñas de estimacións para o gasto refírense aos detalles da liña de oferta e contrato para gastos e as liñas de estimación de gasto nun proxecto.

Despois de resolver unha lista de prezos de custo, o sistema utiliza unha combinación dos campos **Categoría** e **Unidade** da liña de estimación para que un gasto coincida coas liñas de **Prezo de categoría** na lista de prezos resolta. Se o sistema atopa unha liña de prezo de categoría que ten unha taxa de custo para a combinación de **Categoría** e **Unidades**, esa é a taxa de custo predefinida. Se o sistema non pode coincidir cos valores de **Categoría** e **Unidade** ou se é capaz de atopar unha liña de prezo de categoría coincidente, pero o método de fixación de prezos non o é **Prezo por unidade**, a taxa de custo está predefinida en cero (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]