---
title: Configurar os modelos de custo
description: Este artigo ofrece información sobre como crear e usar modelos de custo en Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ffb45d46cf1305fffd5933f4c10b169bf802046d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918402"
---
# <a name="set-up-cost-templates"></a>Configurar os modelos de custo

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


Este artigo ofrece información sobre como crear e usar modelos de custo en Project Operations. Un modelo de custo determina:

- As categorías de proxecto para as transaccións previstas e reais que se incluirán nunha porcentaxe do cálculo de finalización do proxecto. O valor de porcentaxe de finalización úsase entón para calcular a cantidade de ingresos recoñecidos.
- Se a porcentaxe de finalización se pode modificar se se calcula automaticamente.
- Se a porcentaxe de finalización se calcula en función de cantidades ou unidades.

## <a name="cost-template-example"></a>Exemplo de modelo de custo

Está a traballar nun proxecto de deseño de sitios web para un cliente no que cobra unha tarifa plana de 10 000 USD. Vostede prevé que levará 100 horas (5000 USD) completar o proxecto. Tamén prevé dous billetes de avión e catro noites nun hotel para viaxes ao centro do cliente (1800 USD). Isto xera un custo total previsto de 6800 USD.

Cando executa o proceso de recoñecemento de ingresos a prezo fixo para crear unha estimación a final de mes, comproba que traballou 35 horas no proxecto. Isto aínda non inclúe custos de voos nin de hotel. Tamén tivo un asistente que realizou cinco horas de investigación para o proxecto a un custo de 100 USD, que non tiña previsto.

Cando calcula o valor de porcentaxe de finalización deste proxecto, ten as seguintes opcións:

- Quere incluír todos os custos (horas e gastos) ou só as horas?
- Quere incluír todas as horas ou só as horas previstas?
- Quere calcular a porcentaxe de finalización en función do custo en dólares das horas planificadas (5000 USD) ou só do número de horas (100)?

As súas respostas a estas preguntas determinan as opcións que establece no modelo de custo e as categorías que selecciona nas liñas do modelo de custo.

A seguinte táboa ilustra os resultados de diferentes métodos de cálculo do valor da porcentaxe de finalización deste escenario.

| Finalización baseada en | Custo en dólares ou unidades | Porcentaxe de finalización | Cálculo |
| --- | --- | --- | --- |
| Todas as horas, sen gastos | Custo en dólares | 37 % 35 x 50 USD + 100 USD = 1850 USD 1850 USD/5000 USD |
| Todas as horas, sen gastos | Unidades de medida | 40 % | 40 horas/100 horas (incluídas cinco horas non planificadas) |
| Horas planificadas, sen gastos | Custo en dólares ou unidade | 35 % | 35/100 horas ou 35 x 50 USD/5000 |
| Todas as horas e gastos | Custo en dólares | 27,2 % | 1850 USD/6800 USD |

Decidir que enfoque tomar para crear un modelo de custo pode depender de varias consideracións:

- Se inclúe horas non planificadas no modelo de custos, corre o risco de alcanzar o 100 por cento antes de que remate o proxecto. Isto débese a que as horas reais serán maiores que as previstas. Se usa algún dos dous primeiros métodos indicados na táboa, debería cambiar o plan (unidades previstas) cando teña coñecemento de desviacións. Neste caso, engadiría ou restaría segundo o seu coñecemento do que se require para rematar o proxecto. Se o proxecto necesitará outras 65 horas para completalo, engadiría cinco horas ao plan para un total de 105. Se sabe que o seu asistente realizará outras cinco horas de investigación, o total converterase en 110 horas.
- Se utiliza o terceiro método indicado na táboa, só actualizaría as horas planificadas para o seu propio tempo para manter o cálculo de porcentaxe de finalización exacto. A súa rendibilidade cambiará cando se rexistren as horas non planificadas, pero seguirá cunha traxectoria de porcentaxe de finalización coñecida.
- Se usa o cuarto método indicado na táboa, o risco é que os gastos se produzan en momentos irregulares e que non se reflictan no seu progreso para a finalización. Polo tanto, se se inclúen os gastos, poden causar que a súa porcentaxe de finalización flutúe máis do desexable. Por exemplo, como aínda non colleu un voo, a súa porcentaxe de finalización foi do 27 por cento en vez do 35 ou 37 por cento se basea o cálculo só no tempo. Se fixera unha viaxe durante dúas noites e pronosticara os custos do voo e do hotel con precisión, a porcentaxe de finalización sería do 40,4 por cento (1850 USD por man de obra e 900 USD por gastos = 2750 USD/ 6800 USD = 40,4 por cento). Polo tanto, incorrer en gastos por só unha viaxe en avión cambiaría a porcentaxe de finalización do 27 por cento ao 40 por cento.

## <a name="create-cost-templates"></a>Crear modelos de custo
Para crear modelos de custo, siga estes pasos:

1. Para acceder aos modelos de custo, no ambiente de Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Configurar** > **Estimacións** > **Modelo de custo**.
2. Seleccione **Novo** para crear un novo modelo de custo. Introduza un nome e unha descrición.
3. Proporcione un ID de liña de custo para cada tipo de transacción.
4. Seleccione un método de finalización predefinido:

  - **Automático**: A porcentaxe de finalización calcúlase automaticamente nun proxecto. Non se pode modificar o valor resultante.
  - **Manual**: A porcentaxe de finalización calcúlase automaticamente nun proxecto. Pódese modificar o valor resultante.

  > [!NOTE]
  > Para os cálculos manuais, a porcentaxe de realización mantense en **Cálculo manual** no separador **Xeral** na páxina **Estimación**.

5. En **Finalización baseada en**, seleccione un dos seguintes valores:

  - **Importe**: O importe en divisa de contabilidade calcula a porcentaxe de finalización.
  - **Unidade**: A cantidade calcula a porcentaxe de finalización.
  - **Liña recta**: O sistema calcula a porcentaxe de finalización de forma proporcional empregando as datas de inicio e fin do proxecto para determinar a duración do proxecto.

6. Seleccione **Liñas de custo** para revisar as liñas de custo do modelo de custo. Requírese polo menos unha liña de custo para cada tipo de transacción. Non obstante, pode crear varias liñas de custo para os mesmos tipos de transacción e establecer os atributos desexados para estas liñas.
7. No separador **Categorías**, seleccione as categorías do proxecto para incluír na liña do modelo de custo.
8. No separador **Xeral**, seleccione se se incluirá esta liña na porcentaxe de cálculo de finalización.
9. Seleccione o método de custo para completar que se empregará ao calcular a porcentaxe de finalización.


[!INCLUDE[footer-include](../includes/footer-banner.md)]