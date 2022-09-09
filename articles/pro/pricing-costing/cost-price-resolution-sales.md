---
title: Determinar as taxas de custo para as estimacións e os reais do proxecto
description: Este artigo ofrece información sobre como se determinan as taxas de custo para as estimacións e os reais do proxecto.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410147"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Determinar as taxas de custo para as estimacións e os reais do proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Para determinar a lista de prezos de custo e as taxas de custo nos contextos estimativos e reais, o sistema utiliza a información do **Data**, **·**, e **Unidade de Contratación** campos do proxecto relacionado.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinación das taxas de custo en contextos estimativos e reais para o Tempo

Estimar contexto para **Tempo** refírese a:

- Detalles da liña de cotización para **Tempo**.
- Detalles da liña de contrato para **Tempo**.
- Asignacións de recursos nun proxecto.

Contexto real para **Tempo** refírese a:

- Liñas do diario de entrada e corrección para **Tempo**.
- Liñas de diario que se crean cando se envía unha entrada de tempo.

Despois de determinar unha lista de prezos de custo, o sistema completa os seguintes pasos para introducir a taxa de custo predeterminada.

1. O sistema coincide coa combinación de **Papel** e **Unidade de Recursos** campos no contexto estimativo ou real para **Tempo** contra as liñas de prezos do rol da lista de prezos. Esta coincidencia supón que estás utilizando as dimensións de prezos estándar para o custo laboral. Se configurou o sistema para que coincida con campos distintos ou ademais de **Papel** e **Unidade de Recursos**, úsase unha combinación diferente para recuperar unha liña de prezos de función coincidente.
1. Se o sistema atopa unha liña de prezo de función que teña unha taxa de custo para o **Papel** e **Unidade de Recursos** combinación, esa taxa de custo utilízase como taxa de custo predeterminada.
1. Se o sistema non pode coincidir co **Papel** e **Unidade de Recursos** valores, recupera liñas de prezos de función que teñen valores coincidentes para o **Papel** campo pero valores nulos para o **Unidade de Recursos** campo. Despois de que o sistema teña un rexistro de prezos de función coincidente, a taxa de custo deste rexistro empregarase como taxa de custo predeterminada.

> [!NOTE]
> Se configura unha priorización diferente do **Papel** e **Unidade de Recursos** campos ou se ten outras dimensións que teñan maior prioridade, o comportamento anterior cambiará en consecuencia. O sistema recupera rexistros de prezos de función que teñen valores que coinciden con cada valor de dimensión de prezos por orde de prioridade. As filas que teñen valores nulos para esas dimensións son as últimas.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinación das taxas de custo nas liñas reais e estimativas de Gasto

Estimar contexto para **Gasto** refírese a:

- Detalles da liña de cotización para **Gasto**.
- Detalles da liña de contrato para **Gasto**.
- Estimacións de gastos nun proxecto.

Contexto real para **Gasto** refírese a:

- Liñas do diario de entrada e corrección para **Gasto**.
- Liñas de diario que se crean cando se envía unha entrada de gasto.

Despois de determinar unha lista de prezos de custo, o sistema completa os seguintes pasos para introducir a taxa de custo predeterminada.

1. O sistema coincide coa combinación de **Categoría** e **Unidade** campos no contexto estimativo ou real para **Gasto** contra as liñas de prezos da categoría da lista de prezos.
1. Se o sistema atopa unha liña de prezos de categoría que teña unha taxa de custo para o **Categoría** e **Unidade** combinación, esa taxa de custo utilízase como taxa de custo predeterminada.
1. Se o sistema non pode coincidir co **Categoría** e **Unidade** valores, o prezo establécese en **0** (cero) por defecto.
1. No contexto da estimación, se o sistema pode atopar unha liña de prezos de categoría correspondente, pero o método de prezos é algo distinto **Prezo por Unidade**, a taxa de custo está establecida en **0** (cero) por defecto.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinación das taxas de custo en liñas reais e estimativas para o material

Estimar contexto para **Material** refírese a:

- Detalles da liña de cotización para **Material**.
- Detalles da liña de contrato para **Material**.
- Estimacións materiais nun proxecto.

Contexto real para **Material** refírese a:

- Liñas do diario de entrada e corrección para **Material**.
- Liñas de diario que se crean cando se envía un rexistro de uso de material.

Despois de determinar unha lista de prezos de custo, o sistema completa os seguintes pasos para introducir a taxa de custo predeterminada.

1. O sistema utiliza a combinación de **Produto** e **Unidade** campos no contexto estimativo ou real para **Material** contra as liñas do artigo da lista de prezos da lista de prezos.
1. Se o sistema atopa unha liña de artigos da lista de prezos que teña unha taxa de custo para o **Produto** e **Unidade** combinación, esa taxa de custo utilízase como taxa de custo predeterminada.
1. Se o sistema non pode coincidir co **Produto** e **Unidade** valores, o custo unitario establécese en **0** (cero) por defecto.
1. No contexto estimativo ou real, se o sistema pode atopar unha liña de artigos da lista de prezos coincidente, pero o método de fixación de prezos é diferente **Importe da moeda**, o custo unitario establécese en **0** por defecto. Este comportamento ocorre porque Project Operations só admite o **Importe da moeda** método de prezos dos materiais que se usan nun proxecto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
