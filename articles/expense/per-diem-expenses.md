---
title: Gastos diarios
description: Este tema ofrece información sobre como traballar cos gastos diarios.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596048"
---
# <a name="per-diem-expenses"></a>Gastos diarios

> [!IMPORTANT] 
> A funcionalidade que se describe neste tema está dispoñible para os usuarios destinatarios como parte dunha versión de vista previa.

Un pago diario é unha asignación diaria fixa e predeterminada que unha empresa paga aos seus empregados por aloxamento (hoteis), comidas e gastos imprevistos nos que incorren eses empregados mentres viaxan por motivos de traballo. A empresa paga este subsidio aos empregados en lugar de pagar os gastos de viaxe reais. Os empregados poden usar o seu **Incidentes/Outros** dieta para cubrir propinas, servizo de cuartos, lavandería ou limpeza en seco para reunións de negocios importantes. A taxa diaria pode variar, dependendo de se o empresario opta por reembolsar o custo combinado de aloxamento e comidas, ou só o custo das comidas e gastos imprevistos.

As taxas das dietas poden basearse na época do ano, na localización da viaxe ou en ambas. Cando creas unha regra de dietas, podes especificar que unha porcentaxe da taxa diaria será retenida se un empregado recibe comidas ou servizos gratuítos. Tamén pode establecer un número mínimo de horas e un número máximo de horas que a taxa de dieta pode aplicarse ao desprazamento dun empregado.

A dieta calcúlase como o subsidio total que se ofrece ao día menos a redución de comidas (custo das comidas gratuítas) que se lle proporciona ao empregado.

## <a name="configure-per-diems"></a>Configurar dietas

Para configurar os gastos diarios, siga estes pasos.

1. Ir a **Xestión de gastos** \> **Montar** \> **Xeral** \> **Parámetros de xestión de gastos**.
2. No **Por día** ficha, na **Calcula a redución de comidas por** campo, seleccione como se deben calcular as dietas:

    - **Tipo de comida por viaxe** – Calcula a dieta en función do tipo de comida que se introduce (almorzo, xantar ou cea) e da redución de comidas que se especifica para cada tipo de comida para a dieta durante a duración da viaxe.
    - **Tipo de comida por día** – Calcular a dieta en función do tipo de comida que se ingresa e da redución de comidas que se especifica para cada tipo de comida para a dieta por día.
    - **Número de comidas ao día** – Calcula a dieta en función do número de comidas que se introducen ao día e da redución de comidas polo número de comidas que se prestan cada día.

3. Ir a **Xestión de gastos** \> **Montar** \> **Cálculos e códigos** \> **Localizacións diarias**.
4. Engade lugares onde se poden usar dietas.
5. Para cada localización que engadas, no **As dietas** pestana, seleccione a taxa de viáticos e a moeda que son válidas entre datas de inicio e finalización específicas para aloxamento, comidas e outros gastos. Para configurar as taxas diarias e as moedas, vai a **Xestión de gastos** \> **Montar** \> **Cálculos e códigos** \> **As dietas**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>As dietas na interface de gastos reimaxinadas

A función diaria é compatible con reimaxinado **Xestión de gastos** espazo de traballo en Microsoft Dynamics 365 Finance versión 10.0.25 e posteriores.

Para activar as dietas, siga estes pasos.

1. No **Xestión de características** espazo de traballo, busque e seleccione **Informes de gastos reimaxinados** función da lista e, a continuación, seleccione **Habilita agora**.
2. Busca e selecciona o **Interface reimaxinada para o informe de gastos diarios** función da lista e, a continuación, seleccione **Habilita agora**.

## <a name="how-the-feature-works"></a>Como funciona a función

Esta sección ofrece exemplos de tres escenarios de configuración. Para cada exemplo, o **Calcula a redución de comidas por** campo está configurado con un valor diferente. Para os tres exemplos, o importe total a pagar é o mesmo ata que se aplique a redución de comidas. Despois dese punto, o importe total a pagar difire para cada exemplo.

Para crear o gasto diario que se utiliza para os tres exemplos, siga estes pasos.

1. Ir a **Espazos de traballo** \> **Xestión de gastos**.
2. Seleccione **Novo informe de gastos** ou seleccione un informe de gastos existente.
3. Engade un novo gasto. No **Categoría** campo, seleccione **Por día**. Selecciona a localización e as datas de inicio e fin da túa viaxe. A dieta de aloxamento, comidas e gastos adicionales (outros gastos) calcúlase en función da asignación diaria establecida para o lugar seleccionado.

    Por exemplo, vostede selecciona **Redmond (EEUU)** como a localización. A asignación diaria para ese lugar é de 150 dólares estadounidenses (150 USD) para aloxamento, USD 75 para comidas e USD 5 para gastos imprevistos. A data de inicio é o 10 de xaneiro e a data de finalización o 14 de xaneiro. Polo tanto, a duración seleccionada é de cinco días cando a configuración seleccionada son días naturais con hora, e a hora seleccionada comeza e remata ás 12:00 horas nas datas de inicio e finalización. Aquí están os cálculos:

    - Importe total a pagar = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Comida e porción incidental da cantidade total = 5 × (75 + 5) = USD 400

Se o almorzo, o xantar e a cea se proporcionaron durante a viaxe, esas comidas deberán contabilizarse como unha redución de comidas.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemplo 1: dietas nas que as reducións de comidas están baseadas no tipo de comida por viaxe

Neste exemplo, a redución da comida é do 30 por cento para o almorzo, do 30 por cento para o xantar e do 40 por cento para a cea. No **Parámetros de xestión de gastos** páxina, o **Calcula a redución de comidas por** campo está configurado en **Tipo de comida por viaxe**. Estes son os cálculos se se proporcionaron tres almorzos, dous xantares e cero ceas ao empregado:

- Redución das comidas = (3 ×\[ 75 × 30 %\]) + (2 ×\[ 75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Comidas e gastos adicionales = 400 – 112,50 = USD 287.50
- Importe total a pagar = subsidio total – Redución de comidas = 1.150 – 112,50 = USD 1,037.50

![Gasto diario onde a redución de comidas se basea no tipo de comida por viaxe.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemplo 2: dietas nas que as reducións de comidas están baseadas no tipo de comida por día

Neste exemplo, a redución da comida é do 30 por cento para o almorzo, do 30 por cento para o xantar e do 40 por cento para a cea. No **Parámetros de xestión de gastos** páxina, o **Calcula a redución de comidas por** campo está configurado como **Tipo de comida por día**. Neste caso, no **Comidas** reixa na **Editar gasto** caixa de diálogo, desmarque as caixas de verificación para indicar que comidas se lle proporcionaron durante a súa viaxe.

Por exemplo, estes son os cálculos se se proporcionou o almorzo durante os tres primeiros días da viaxe:

- Redución de comidas diarias para cada un dos tres primeiros días = 75 × 30 % = USD 22.50
- Redución total da comida = 3 × 22,50 = USD 67.50
- Comidas e incidentes dos días 1 ao 3 = 75 – 22.50 = USD 57.50
- Total de comidas e incidentes = Suma de comidas e incidentes en cinco días = 400 – 67,50 = USD 332.50
- Importe total a pagar = Importe total – Redución de comidas = 1.150 – 67,50 = USD 1,082.50

![Gasto diario onde a redución de comidas se basea no tipo de comida por día.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemplo 3: dietas cando as reducións de comidas se basean no número de comidas ao día

Neste exemplo, a redución de comidas calcúlase en función do número de comidas que se proporcionaron ao día (é dicir, o **Calcula a redución de comidas por** campo no **Parámetros de xestión de gastos** páxina está configurada como **Número de comidas ao día**). No **Comidas** reixa na **Editar gasto** caixa de diálogo, desmarque as caixas de verificación para indicar que comidas se proporcionaron.
Neste caso, a redución de comidas baséase só no número de comidas proporcionadas, e non no tipo de comida (Almorzo/xantar/cea).

Estes son os cálculos das dietas cando a asignación diaria é USD 150 para aloxamento, USD 75 para comidas e USD 5 para gastos imprevistos:

- **Importe total a pagar** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Unha comida:** Redución das comidas = 20 % = USD 15
- **Dúas comidas:** Redución das comidas = 50 % = USD 37.50
- **Tres comidas:** Redución das comidas = 100 % = USD 75

Aquí están os cálculos para o **dietas e gastos adicionales**, que inclúe USD 5 para incidentes:

- Día 1 - Ofrécese dúas comidas = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- Día 2 - Ofrécese dúas comidas = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- Día 3 - Unha comida proporcionada = (75 – 15) + 5 = 60 + 5 = USD 65
- Día 4: cero comidas = (75-0) + 5 = 75 + 5 = USD 80
- Día 5: proporcionaron tres comidas = (75 – 75) + 5 = 0 + 5 = USD 5

- Total de comidas e incidentes = Comidas e incidentes para o día 1+ Día 2 +Día 3+Día 4+ Día 5 = USD 235
- Redución total de comidas = Redución de comidas para o día 1+ Día 2 +Día 3+Día 4+ Día 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Importe total a pagar = subsidio total – Redución total de comidas = USD 1,150 - USD 165 = USD 985

![Gasto diario cando a redución de comidas se basea no número de comidas ao día.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partir da versión 10.0.23 de Finance, se utilizas a interface de gastos reimaxinada, non podes crear gastos diarios que teñan datas solapadas. Se o intentas, recibirás unha mensaxe de erro.
