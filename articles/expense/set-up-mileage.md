---
title: Configurar a quilometraxe empregando niveis de taxa de quilometraxe
description: Este artigo ofrece información sobre as taxas de quilometraxe e os niveis de taxas de quilometraxe.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930132"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
