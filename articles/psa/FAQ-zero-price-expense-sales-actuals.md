---
title: Por que o prezo por defecto é cero nas vendas de gastos reais?
description: As tres seguintes comprobacións axudaranlle a solucionar por que os prezos son por defecto 0 nos valores reais de vendas por gastos.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5840bda4f74c720bfcdc7f4e84c8f22e0c6163ec
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076152"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Por que o prezo por defecto é cero nas vendas de gastos reais?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas Preguntas máis frecuentes aplícanse a gastos reais onde a clase de transacción está definida a Gastos e o tipo de transacción é Vendas sen facturar. As tres seguintes comprobacións axudaranlle a solucionar por que os prezos (facturación) son por defecto 0 nos valores reais de vendas por gastos.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Verificación 1: Identificar a lista de prezos de vendas para o proxecto

Busque o proxecto no campo de proxectos do valor real e vaia á páxina de proxecto. A seguir, vaia ao separador Vendas. Na grade de liñas de contrato do proxecto, prema na ligazón no campo Contrato do proxecto. Abrirase a páxina Contrato do proxecto. Na páxina Contrato do proxecto, vaia ao separador Listas de prezos do proxecto. Comprobe se hai polo menos unha lista de prezos anexada aquí.

Se non hai ningunha lista de prezos anexada na grade Listas de prezos de proxecto en Contrato do proxecto, faga o seguinte:

- Anexe unha lista de prezos á grade de Listas de prezos de proxecto. As listas de prezos que se poden anexar aquí deben ter o campo de contexto definido en Vendas e o campo de moeda na lista de prezos debe coincidir co campo de moneda no Contrato do proxecto. Cando faga as correccións necesarias, cree novamente unha entrada de gasto, apróbea e verifique que o valor real de vendas sen facturar mostra un prezo válido.
- Se ten unha ou varias listas de prezos anexadas na grade Listas de prezos de proxecto do Contrato do proxecto, vaia a Verificación 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Verificación 2: Algunha das listas de prezos identificadas enriba é válida para a data específica no valor real de gasto?

Para que Project Service considere unha lista de prezos como prezo por defecto, esa lista de prezos debe ser aplicable para a data no valor real de vendas por gastos. Comprobe o seguinte para ver se as listas de prezos identificados enriba son aplicables:

- Comece por comprobar se as datas de inicio e fin no separador xeral para as listas de prezos anexada non están baleiras. Se as datas de inicio e fin nas listas de prezos identificadas enriba está baleiras, xa identificou o problema. 
- Anote o campo de data de inicio no seu valor real de vendas por gastos e comprobe se algunha das listas de prezos identificadas é aplicable para esa data. Por exemplo, a data do valor real de gasto debería estar entre a data de inicio e a data de fin na lista de prezos. 
    - Se non hai ningunha lista de prezos que cubra esa data no valor real de vendas por gastos, xa identificou o problema. Modificar as datas de inicio e fin da lista de prezos para asegurar que a lista de prezos cubra a data do valor real de gasto. 
    - Se hai máis dunha lista de prezos que cubra a data no valor real de vendas por gastos, xa identificou o problema. Pode corrixir isto editando as datas de inicio e fin das listas de prezos, de forma que haxa só unha lista de prezos que cubra a data do valor real de gasto. 
    - Se só hai unha lista de prezos que cubra esa data do valor real de gasto, vaia á Verificación 3.
Cando faga as correccións necesarias, cree novamente unha entrada de gasto, apróbea e verifique que o valor real de vendas sen facturar mostra un prezo válido.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Verificación 3: Hai un prezo válido para a categoría de gasto na lista de prezos do proxecto aplicable? 

Se concluíu correctamente as Verificacións 1 e 2, agora debe ter só unha lista de prezos do proxecto é aplicable para a data do valor real de vendas por gastos. Abra esta Lista de prezos do proxecto e vaia ao separador Prezos de categoría. Asegúrese de que hai unha liña na grade para a categoría de gasto específica no valor real de gasto.
 
- Se non hai ningunha fila, xa identificou o problema. Cree unha liña na grade de prezos Categoría para a categoría no seu valor real de gasto. Cando termine, cree novamente unha entrada de gasto, apróbea e verifique que o valor real de vendas sen facturar mostra un prezo válido. 
- Se hai unha fila para a categoría de gasto na grade de prezos de categoría, comprobe se ten un prezo válido.

Para comprender que é un prezo válido, utilice estos métodos:

- Se o campo Método de definición de prezos na liña de prezos de Categoría está definido en Ao custo, a seguir, a unidade de cambio no valor real de vendas de Gastos estará predefinido ao valor da entrada Gasto.
- Se o campo Método de definición de prezos na liña de prezos de Categoría está definido en Porcentaxe de sobreprezo, a seguir, verifique se o campo Porcentaxe está definido nun valor válido. A taxa de unidade no seu valor real de vendas por gastos predefínese aplicándolle este porcentaxe de sobreprezo ao prezo na entrada de Gasto.
- Se o campo Método de definición de prezos na liña de prezos de Categoría está definido en Prezo por unidade, a seguir, verifique se o campo Precio está definido nun valor válido. A taxa de unidade no seu valor real de vendas por gastos estará predefinido á cantidade de moeda especificada no campo Prezo.

Se o axuste de prezo para a categoría de gasto non é válida, xa identificou o problema. A solución é editar a liña de prezos de categoría cun prezo válido para a categoría de gasto segundo as regras de arriba. Cando termine, cree novamente unha entrada de gasto, apróbea e verifique que o valor real de vendas sen facturar ten un prezo válido.

Se aínda non ve un prezo válido no valor real de vendas por gastos despois de realizar as tres comprobacións anteriores, rexistre o tícket de asistencia.


