---
title: Determinar taxas de custo para estimacións e datos reais baseados en proxecto
description: Este artigo ofrece información sobre como se determinan as taxas de custo das estimacións e dos datos reais baseados en proxecto.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475271"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Determinar taxas de custo para estimacións e datos reais baseados en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Para determinar os prezos de custo en estimacións e datos reais en Microsoft Dynamics 365 Project Operations, o sistema utiliza primeiro a data e a moeda no contexto da estimación ou dato real entrante para determinar a lista de prezos de vendas. No contexto real especificamente, o sistema usa o campo **Data da transacción** para determinar que lista de prezos é aplicable. O valor **Data da transacción** da estimación ou dato real entrante compárase cos valores de **Inicio efectivo (independente da zona horaria)** e **Fin efectivo (independente da zona horaria)** na lista de prezos. Despois de determinar a lista de prezos de custo, o sistema determina a taxa de custo.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinación das taxas de custo en contextos de datos reais e estimacións para tempo

O contexto de estimación para **Tempo** refírese a:

- Detalles da liña de oferta para **Tempo**.
- Detalles da liña de contrato para **Tempo**.
- Atribucións de recursos nun proxecto.

O contexto de datos reais para **Tempo** refírese a:

- Entrada e corrección de liñas de diario para **Tempo**.
- Liñas de diario que se crean cando se envía unha entrada de tempo.

Despois de determinar unha lista de prezos de custo, o sistema completa os seguintes pasos para introducir a taxa de custo predefinida.

1. O sistema fai coincidir a combinación dos campos **Rol**, **Empresa de recursos** e **Unidade de recursos** no contexto de estimación ou dato real para **Tempo** contra as liñas de prezos do rol na lista de prezos. Esta coincidencia supón que está a usar as dimensións de prezos estándar para o custo da man de obra. Se configurou o sistema para que coincida cos campos distintos de ou ademais de **Rol**, **Empresa de recursos** e **Unidade de recursos**, úsase unha combinación diferente para recuperar unha liña de prezo de rol coincidente.
1. Se o sistema atopa unha liña de prezo de rol que ten unha taxa de custo para a combinación de **Rol**, **Empresa de recursos** e **Unidade de recursos**, esa taxa de custo utilízase como a taxa de custo predeterminada.
1. Se o sistema non pode facer coincidir os valores de **Rol**, **Empresa de recursos** e **Unidade de recursos**, elimina a dimensión que ten a prioridade máis baixa, busca liñas de prezos de rol que teñan coincidencias para os outros dous valores de dimensión e continúa baixando progresivamente as dimensións ata que se atope unha fila de prezos de rol coincidente. A taxa de custo dese rexistro empregarase como taxa de custo predeterminada. Se o sistema non atopa unha fila de prezo de rol coincidente, o prezo establecerase en **0** (cero) por defecto.

> [!NOTE]
> Se configura unha priorización diferente dos campos **Rol** e **Unidade de recursos** ou se ten outras dimensións con maior prioridade, este comportamento cambiará en consecuencia. O sistema recupera rexistros de prezos de rol que teñen valores que coinciden con cada valor de dimensión de prezos por orde de prioridade. As filas que teñen valores nulos para esas dimensións son as últimas.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinación das taxas de custo nas liñas de datos reais e estimacións para gasto

O contexto de estimación para **Gasto** refírese a:

- Detalles da liña de oferta para **Gasto**.
- Detalles da liña de contrato para **Gasto**.
- Estimacións de gastos nun proxecto.

O contexto de dato real para **Gasto** refírese a:

- Entrada e corrección de liñas de diario para **Gasto**.
- Liñas de diario que se crean cando se envía unha entrada de gasto.

Despois de determinar unha lista de prezos de custo, o sistema completa os seguintes pasos para introducir a taxa de custo predefinida.

1. O sistema fai coincidir a combinación dos campos **Categoría** e **Unidade** na liña de estimación ou dato real para **Gasto** contra as liñas de prezo de categoría na lista de prezos.
1. Se o sistema atopa unha liña de prezo de categoría que ten unha taxa de custo para a combinación de **Categoría** e **Unidades**, esa taxa de custo utilízase como taxa de custo predefinida.
1. Se o sistema non pode facer coincidir os valores de **Categoría** e **Unidade**, o prezo establécese en **0** (cero) por defecto.
1. No contexto da estimación, se o sistema pode atopar una liña de prezo de categoría que coincida, pero o método de fixación de prezos é algo distinto a **Prezo por unidade**, a taxa de custo establécese en **0** (cero) por defecto.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinación das taxas de custo nas liñas de datos reais e estimacións para material

O contexto de estimación para **Material** refírese a:

- Detalles da liña de oferta para **Material**.
- Detalles da liña de contrato para **Material**.
- Estimacións de material nun proxecto.

O contexto de dato real para **Material** refírese a:

- Entrada e corrección de liñas de diario para **Material**.
- Liñas de diario que se crean cando se envía un rexistro de uso de material.

Despois de determinar unha lista de prezos de custo, o sistema completa os seguintes pasos para introducir a taxa de custo predefinida.

1. O sistema usa a combinación dos campos **Produto** e **Unidade** na liña de estimación ou dato real para **Material** contra as liñas de elemento de lista de prezos na lista de prezos.
1. Se o sistema atopa unha liña de elemento de lista de prezos que ten unha taxa de custo para a combinación de **Produto** e **Unidade**, esa taxa de custo utilízase como taxa de custo predefinida.
1. Se o sistema non pode facer coincidir os valores de **Produto** e **Unidade**, o custo unitario establécese en **0** (cero) por defecto.
1. No contexto da estimación ou dato real, se o sistema pode atopar una liña de elemento de lista de prezos que coincida, pero o método de fixación de prezos é algo distinto a **Importe da moeda**, o custo unitario establécese en **0** por defecto. Este comportamento ocorre porque Project Operations só admite o método de fixación de prezos **Importe da moeda** para os materiais que se usan nun proxecto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
