---
title: Resolver de prezos de custo en estimacións e datos reais - lite
description: Este tema ofrece información sobre como se resolven os prezos de custo das estimacións e os datos reais.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176789"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Resolver de prezos de custo en estimacións e datos reais - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Para resolver os prezos de custo e a lista de prezos de custo para estimacións e datos reais, o sistema utiliza a información dos campos **Data**, **Moeda** e **Unidade de contratación** do proxecto relacionado. Despois de resolverse a lista de prezos de custo, a aplicación resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para tempo

As liñas de estimacións para o tempo refírense aos detalles da liña de oferta e contrato para as atribucións de tempo e recursos nun proxecto.

Despois de resolver unha lista de prezos de custo, o sistema utiliza os campos **Rol** e **Unidade de Recursos** da liña de estimación para que o tempo coincida coas liñas de prezo de rol na lista de prezos. Esta coincidencia supón que está a usar unhas dimensións de prezos listas para usar para o custo de man de obra. Se configurou o sistema para que coincida cos campos en lugar de ou ademais de **Rol** e **Unidade de Recursos**, usarase unha combinación diferente para recuperar unha liña de prezo de rol coincidente. Se a aplicación atopa unha liña de prezo de rol que ten unha taxa de custo para a combinación de **Rol** e **Unidade de recursos**, esa é a taxa de custo predeterminada. Se a aplicación non pode coincidir cos valores de **Rol** e **Unidade de recursos**, recupera as liñas de prezo de rol cun rol coincidente, pero valores nulos de **Unidade de recursos**. Despois de ter un rexistro de prezos de rol coincidente, a taxa de custo predefínese a partir dese rexistro. 

> [!NOTE]
> Se configura unha priorización diferente de **Rol** e **Unidade de recursos** ou se ten outras dimensións con maior prioridade, este comportamento cambiará en consecuencia. O sistema recupera os rexistros de prezos de rol con valores que coinciden con cada un dos valores da dimensión de prezos por orde de prioridade con filas que teñen valores nulos para as últimas dimensións.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolución das taxas de custo nas liñas de datos reais e estimacións para gasto

As liñas de estimacións para o gasto refírense aos detalles da liña de oferta e contrato para gastos e as liñas de estimación de gasto nun proxecto.

Despois de resolver unha lista de prezos de custo, o sistema utiliza unha combinación dos campos **Categoría** e **Unidade** da liña de estimación para que un gasto coincida coas liñas de **Prezo de categoría** na lista de prezos resolta. Se o sistema atopa unha liña de prezo de categoría que ten unha taxa de custo para a combinación de **Categoría** e **Unidades**, esa é a taxa de custo predefinida. Se o sistema non pode coincidir cos valores de **Categoría** e **Unidade** ou se é capaz de atopar unha liña de prezo de categoría coincidente, pero o método de fixación de prezos non o é **Prezo por unidade**, a taxa de custo está predefinida en cero (0).
