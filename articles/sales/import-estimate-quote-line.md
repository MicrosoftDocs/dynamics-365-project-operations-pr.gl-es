---
title: Importar estimacións para un proxecto a unha liña de oferta de proxecto
description: Este tema ofrece información sobre como importar estimacións dun proxecto a unha liña de oferta de proxecto.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a9ac27b7694927f9cea88b49310f3106fbc6542cc0f7f1756744b970358c1057
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993509"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Importar estimacións para un proxecto a unha liña de oferta de proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


Se se crea un proxecto durante a fase de prevenda, pode seleccionar importar a estimación financeira do proxecto á liña de oferta baseada en proxecto.

1. Asegúrese de que a liña de oferta baseada en proxecto conteña a información do proxecto no campo **Proxecto**.
2. No separador **Detalles de liña de oferta**, seleccione **Importar desde estimación de proxecto**.
3. Na páxina de diálogo que se abre, seleccione unha das seguintes opcións de resumo:

  - **Clase de transacción**
  - **Categoría**
  - **Rol** 
  - **Tarefa do proxecto**

En función da súa selección, cópianse as estimacións do proxecto para todas as clases de transaccións incluídas nesta liña de oferta. Para comprobar que clases de transacción se inclúen, seleccione o separador **Xeral** na liña de oferta baseada en proxecto e comprobe os valores de **Incluír tempo**, **Incluír gastos**, e **Incluír taxas**.

Cando importe estimacións, o sistema predefinirá os prezos en función das listas de prezos do proxecto anexas á oferta e do tipo de facturación configurado na liña de oferta baseada en proxecto. Se un rol ou categoría está configurado na liña de oferta baseada en proxecto como non imputable, a liña de estimación importada establecerase como non imputable e non se sumará ao valor ofertado da liña de oferta.

Cando unha liña de oferta ten detalles de liña, os campos **Valor da oferta** e **Imposto estimado** da liña de oferta están resumidos e non se poden editar.

Cando se seleccionan varias opcións de resumo, o sistema tenta resumir mediante todas as opcións seleccionadas. O resultado é que a saída das liñas de oferta importadas será maior que se seleccionase só unha opción de resumo.

Por exemplo, se o proxecto ten as seguintes liñas de estimación de gastos.

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Cando o usuario selecciona resumir por clase de transacción, importarase a seguinte información.

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

Cando o usuario selecciona resumir por clase de transacción e categoría, importarase a seguinte información.

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Cando o usuario selecciona resumir por clase de transacción, categoría e tarefa nó folla, importarase a seguinte información. Teña en conta que este resultado é o mesmo que no proxecto.

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
