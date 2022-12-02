---
title: Importar estimacións para un proxecto a unha liña de oferta de proxecto
description: Este artigo ofrece información sobre como importar estimacións dun proxecto a unha liña de oferta de proxecto.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc5b6279a2123604291da35c9da2bf63dbe475b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915044"
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
