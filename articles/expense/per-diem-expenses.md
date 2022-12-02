---
title: Gastos de dietas
description: Este artigo ofrece información sobre como traballar con gastos de dietas.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923186"
---
# <a name="per-diem-expenses"></a>Gastos de dietas

> [!IMPORTANT] 
> A funcionalidade que se describe neste artigo está dispoñible para os usuarios obxectivo como parte dunha versión preliminar.

Un pagamento de dietas é unha asignación diaria fixa e predeterminada que unha empresa paga aos seus empregados por aloxamento (hoteis), comidas e gastos incidentais nos que incorren eses empregados mentres viaxan por motivos de traballo. A empresa paga este subsidio aos empregados en lugar de pagar os gastos de viaxe reais. Os empregados poden usar a súa asignación de dietas de **Gastos imprevistos/Outros** para cubrir propinas, servizo de habitacións, lavandería ou limpeza en seco para reunións de negocios importantes. A taxa diaria pode variar, dependendo de se o empresario opta por reembolsar o custo combinado de aloxamento e comidas, ou só o custo das comidas e gastos imprevistos.

As taxas das dietas poden basearse na época do ano, na localización da viaxe ou en ambas. Cando crea unha regra de dietas, pode especificar que se reterá unha porcentaxe da taxa de dietas se un empregado recibe comidas ou servizos de cortesía. Tamén pode establecer un número mínimo de horas e un número máximo de horas que a taxa de dietas se pode aplicar ás viaxes dun empregado.

As dietas calcúlanse como o subsidio total que se ofrece ao día menos a redución de comidas (custo das comidas gratuítas) que se lle proporciona ao empregado.

## <a name="configure-per-diems"></a>Configurar dietas

Para configurar os gatos de dietas, siga estes pasos.

1. Vaia a **Xestión de gastos** \> **Configuración** \> **Xeral** \> **Parámetros de xestión de gastos**.
2. No separador **Dietas**, no campo **Calcular redución de comidas por**, seleccione como se deben calcular as dietas:

    - **Tipo de comida por viaxe** – Calcular a dieta en función do tipo de comida que se introduce (almorzo, xantar ou cea) e da redución de comidas que se especifica para cada tipo de comida para a dieta durante a viaxe.
    - **Tipo de comida por día** – Calcular a dieta en función do tipo de comida que se introduce (almorzo, xantar ou cea) e da redución de comidas que se especifica para cada tipo de comida para a dieta por día.
    - **Número de comidas por día** – Calcular a dieta en función do número de comidas que se introducen ao día e da redución de comidas polo número de comidas que se proporcionan cada día.

3. Vaia a **Xestión de gastos** \> **Configuración** \> **Cálculos e códigos** \> **Localizacións de dietas**.
4. Engada as localizacións onde se poden usar dietas.
5. Para cada localización que engada, no separador **Dietas**, seleccione unha taxa de dietas e a moeda que sexa válida entre unha data específica de inicio e fin para hotel, comidas e outros gastos. Para configurar as taxas e moedas de dietas, vaia a **Xestión de gastos** \> **Configuración** \> **Cálculos e códigos** \> **Dietas**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>As dietas na interface de gastos reinventadas

A función de dietas é compatible coa área de traballo **Xestión de gastos** en Microsoft Dynamics 365 Finance versión 10.0.25 e posteriores.

Para activar as dietas, siga estes pasos.

1. Na área de traballo **Xestión de funcionalidades**, busque e seleccione a funcionalidade **Informes de gastos reinventados** na lista e, a seguir, seleccione **Activar agora**.
2. Busque e seleccione a funcionalidade **Interface de dietas para informe de gastos reinventado** na lista e logo seleccione **Activar agora**.

## <a name="how-the-feature-works"></a>Como funciona a funcionalidade

Esta sección ofrece exemplos de tres escenarios de configuración. Para cada exemplo, o campo **Calcula a redución de comidas por** está configurado cun valor diferente. Para os tres exemplos, o importe total a pagar é o mesmo ata que se aplique a redución de comidas. Despois dese punto, o importe total a pagar difire para cada exemplo.

Para crear o gasto de dietas que se utiliza para os tres exemplos, siga estes pasos.

1. Vaia a **Áreas de traballo** \> **Xestión de gastos**.
2. Seleccione **Novo informe de gastos** ou seleccione un informe de gastos existente.
3. Engada un novo gasto. No campo **Categoría**, seleccione **Dieta**. Seleccione a localización e as datas de inicio e fin da súa viaxe. A dieta por aloxamento, comidas e gastos imprevistos (outros gastos) calcúlase en función da asignación diaria establecida para o lugar seleccionado.

    Por exemplo, vostede selecciona **Redmond (EEUU)** como a localización. A asignación diaria para ese lugar é de 150 dólares estadounidenses (150 USD) para aloxamento, 75 USD para comidas e 5 USD para gastos imprevistos. A data de inicio é o 10 de xaneiro e a data de finalización o 14 de xaneiro. Polo tanto, a duración seleccionada é de cinco días cando a configuración seleccionada son días naturais con hora, e a hora seleccionada comeza e remata ás 12:00 horas nas datas de inicio e finalización. Aquí están os cálculos:

    - Importe total a pagar = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
    - Comida e porción incidental da cantidade total = 5 × (75 + 5) = 400 USD

Se o almorzo, o xantar e a cea se proporcionaron durante a viaxe, esas comidas deberán contabilizarse como unha redución de comidas.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemplo 1: Dietas nas que as reducións de comidas están baseadas no tipo de comida por viaxe

Neste exemplo, a redución da comida é do 30 por cento para o almorzo, do 30 por cento para o xantar e do 40 por cento para a cea. Na páxina **Parámetros de xestión de gastos**, o campo **Calcular redución de comidas por** está configurado como **Tipo de comida por viaxe**. Estes son os cálculos se se proporcionaron tres almorzos, dous xantares e cero ceas ao empregado:

- Redución das comidas = (3 × \[75 × 30 %\]) + (2 × \[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Comidas e gastos imprevistos = 400 – 112,50 = 287,50 USD
- Importe total a pagar = Subsidio total – Redución de comidas = 1150 – 112,50 = 1037,50 USD

![Gasto de dietas no que a redución de comidas está baseada no tipo de comida por viaxe.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemplo 2: Dietas nas que as reducións de comidas están baseadas no tipo de comida por día

Neste exemplo, a redución da comida é do 30 por cento para o almorzo, do 30 por cento para o xantar e do 40 por cento para a cea. Na páxina **Parámetros de xestión de gastos**, o campo **Calcular redución de comidas por** está configurado como **Tipo de comida por día**. Neste caso, na grade **Comidas** na caixa de diálogo **Editar gasto**, desmarque as caixas de verificación para indicar que comidas se lle proporcionaron durante a súa viaxe.

Por exemplo, estes son os cálculos se se proporcionou o almorzo durante os tres primeiros días da viaxe:

- Redución de comidas diarias para cada un dos tres primeiros días = 75 × 30 % = 22,50 USD
- Redución total de comidas = 3 × 22,50 = 67,50 USD
- Comidas e gastos imprevistos dos días 1 ao 3 = 75 – 22,50 = 57,50 USD
- Total de comidas e gastos imprevistos = Suma de comidas e gastos imprevistos en cinco días = 400 – 67,50 = 332,50 USD
- Importe total a pagar = Importe total – Redución de comidas = 1150 – 67,50 = 1082,50 USD

![Gasto de dietas no que a redución de comidas está baseada no tipo de comida por día.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemplo 3: Dietas nas que as reducións de comidas están baseadas no número de comidas por día

Neste exemplo, a redución de comidas calcúlase en función do número de comidas que se proporcionaron ao día (é dicir, o campo **Calcular a redución de comidas por** na páxina **Parámetros de xestión de gastos** está configurado como **Número de comidas ao día**). Na grade **Comidas** na caixa de diálogo **Editar gasto**, desmarque as caixas de verificación para indicar que comidas se proporcionaron.
Neste caso, a redución de comidas baséase só no número de comidas proporcionadas, e non no tipo de comida (almorzo/xantar/cea).

Estes son os cálculos das dietas cando a asignación diaria é 150 USD para aloxamento, 75 USD para comidas e 5 USD para gastos imprevistos:

- **Importe total a pagar** = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
- **Unha comida:** Redución de comidas = 20 % = 15 USD
- **Dúas comidas:** Redución de comidas = 50 % = 37,50 USD
- **Tres comidas:** Redución de comidas = 100 % = 75 USD

Aquí están os cálculos para a **asignación de dietas e gastos imprevistos**, que inclúe 5 USD para gastos imprevistos:

- Día 1 - Dúas comidas proporcionadas = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Día 2 - Dúas comidas proporcionadas = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Día 3 - Unha comida proporcionada = (75 – 15) + 5 = 60 + 5 = 65 USD
- Día 4 - Cero comidas proporcionadas = (75 – 0) + 5 = 75 + 5 = 80 USD
- Día 5 - Tres comidas proporcionadas = (75 – 75) + 5 = 0 + 5 = 5 USD

- Total de comidas e gastos imprevistos = Comidas e gastos imprevistos para o día 1+ día 2 +día 3+día 4+ día 5 = 235 USD
- Redución total de comidas = Redución de comidas para o día 1+ día 2 +día 3+día 4+ día 5= 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Importe total a pagar = Subsidio total – Redución total de comidas = 1150 USD – 165 USD = 985 USD

![Gasto de dietas no que a redución de comidas está baseada no número de comidas por día.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partir da versión 10.0.23 de Finance, se usa a interface de gastos reinventada, non pode crear gastos de dietas que teñan datas solapadas. Se o intenta, recibirá unha mensaxe de erro.
