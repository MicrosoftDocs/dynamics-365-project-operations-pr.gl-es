---
title: Configurar a quilometraxe empregando niveis de taxa de quilometraxe
description: Este artigo ofrece información sobre as taxas de quilometraxe e os niveis de taxas de quilometraxe.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064276"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configurar a quilometraxe empregando niveis de taxa de quilometraxe

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Cando se informa dun gasto e a categoría de gastos seleccionada é **Quilometraxe**, o importe para esa liña de gasto calcúlase de acordo coa cantidade de *taxa por quilometraxe*. Este importe determínase empregando niveis de quilometraxe definidos ou, se non se configuran niveis de taxa de quilometraxe, seguindo unha taxa de quilometraxe estándar. 

Os niveis de taxa de quilometraxe pódense configurar indo a **Xestión de gastos** > **Configurar** > **Xeral** > **Categorías de gasto** > **Quilometraxe** > **Configuración da categoría**.

Despois de actualizar a 10.0.18, se a súa organización usa a categoría de gasto de quilometraxe, considere activar a funcionalidade de quilometraxe despois de revisar os cambios de deseño seguintes. 

O novo deseño dos niveis de taxa de quilometraxe afecta a como se procesa o valor do campo **Cantidade**. Antes do lanzamento do 10.0.18, o valor do campo **Cantidade** considerouse o límite inferior. Cando a acumulación superou ese valor, utilizouse a taxa correspondente.  A partir de 10.0.18, o valor do campo **Cantidade** considérase o límite superior. A taxa correspondente úsase cando a acumulación de quilometraxe é inferior ao valor do campo **Cantidade**.  O novo modelo para os niveis de quilometraxe axuda á coherencia entre os niveis de quilometraxe e unha maior facilidade de uso.   

Todos os informes de gastos aprobados calcularanse de novo durante a publicación segundo o novo deseño.

## <a name="example"></a>Exemplo
 
### <a name="before-version-10018"></a>Antes da versión 10.0.18
Con dous niveis de taxa de quilometraxe, o campo **Cantidade** en cada nivel representa o límite de quilometraxe máis baixo. Actualmente, o primeiro nivel ten un valor de cero (0) e unha taxa de 0,45, e o segundo nivel ten un valor de 1000 e unha taxa de 0,25. Se as millas ou os quilómetros acumulados superan o valor do campo, úsase a taxa relacionada. Se non hai ningunha liña con cantidade cero, o sistema utiliza a taxa de quilometraxe definida na xestión de gastos. 
 
Se un empregado envía un informe de gastos con 1500 millas, as dúas liñas de quilometraxe do informe de gastos publicado serían: 1000 (taxa 0,45) + 500 (taxa 0,25) = 575,00.

### <a name="after-version-10018"></a>Despois da versión 10.0.18
En 10.0.18, o campo **Cantidade** de cada nivel representa o límite superior do nivel. Actualmente, o primeiro nivel ten un valor de 999 e unha taxa de 0,45, e o segundo nivel ten un valor de 999 999 999,00 e unha taxa de 0,25. Se as millas ou os quilómetros acumulados superan o valor do campo **Cantidade**, úsase a taxa relacionada. Se se superan todos os límites superiores, o sistema utiliza a taxa de quilometraxe definida na xestión de gastos. 
 
Para calcular correctamente o mesmo escenario, hai que cambiar a configuración do nivel. O campo **Cantidade** do primeiro nivel ten un valor de 999,00 e o valor de 999 999 999,00 no segundo nivel. Se un empregado supera a cantidade total de millas ou quilómetros no primeiro nivel, o sistema utiliza a taxa de quilometraxe que se define na xestión de gastos. 
  
Se un empregado envía un informe de gastos con 1500 millas, as dúas liñas de quilometraxe do informe de gastos publicado serían: 1000 (taxa 0,45) + 500 (taxa 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Activar a funcionalidade Cálculo da cantidade de quilometraxe para varios niveis de quilometraxe coa mesma taxa

A funcionalidade **Cálculo da cantidade de quilometraxe para varios niveis de quilometraxe coa mesma taxa** mellora o cálculo da taxa de quilometraxe. Complete os seguintes pasos para activar esta función.

1. Vaia a **Áreas de traballo** > **Xestión de funcionalidades**. 
2. Na lista, localice e seleccione **Cálculo da cantidade de quilometraxe para varios niveis de quilometraxe coa mesma taxa** e, a seguir, seleccione **Activar agora**.

Despois de activar a funcionalidade, restableza os niveis de quilometraxe para reflectir correctamente o valor do campo **Cantidade**. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Activa o cálculo dos totais de quilometraxe mediante a función ano fiscal

O **Cálculo dos totais de quilometraxe por ano fiscal** A función activa unha nova configuración nos parámetros de xestión de gastos que realiza cálculos totais de quilometraxe mediante ano fiscal en lugar do ano natural. Complete os seguintes pasos para activar esta función.

1. Vaia a **Áreas de traballo** > **Xestión de funcionalidades**.
1. Na lista, localice e seleccione **Cálculo dos totais de quilometraxe por ano fiscal** e, a continuación, seleccione **Habilita agora**.
1. Ir a **Xestión de gastos** > **Montar** > **Xeral** > **Parámetros de xestión de gastos**.
1. No **Parámetros de xestión de gastos** páxina, localiza e activa **Use ano fiscal para os totais de quilometraxe**.

Despois de activar **Use ano fiscal para os totais de quilometraxe**, os totais de quilometraxe calcúlanse mediante ano fiscal.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
