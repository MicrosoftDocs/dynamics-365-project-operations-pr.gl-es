---
title: Importar unha estimación a unha liña de contrato baseado en proxecto
description: Este tema ofrece información sobre como importar estimacións dun proxecto a unha liña de contrato.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d51eb890a4744051ddd7268e1f1f11b15a23b609
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278371"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importar unha estimación a unha liña de contrato baseado en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

En Dynamics 365 Project Operations, pode importar estimacións desde un proxecto a unha liña de contrato baseado en proxecto.

1. Verifique que o campo **Proxecto** da liña de contrato baseado en proxecto está enchido.
2. No separador **Detalles de liña de contrato**, na subgrade, seleccione **Importar desde a estimación do proxecto**. Ábrese unha páxina de diálogo con opcións de resumo. As opcións de resumo dispoñibles son **Clase de transacción**, **Categoría**, **Función** e **Tarefa de proxecto**. En función das selección para o resumo, cópianse as estimacións do proxecto para todas as clases de transaccións incluídas nesta liña de contrato. 
3. Para comprobar que clases de transacción se inclúen, seleccione o separador **Xeral** na liña de contrato baseada en proxecto e comprobe os valores dos campos **Incluír tempo**, **Incluír gastos**, e **Incluír taxas**.

Cando importe estimacións, a aplicación predefine os prezos en función das listas de prezos do proxecto anexas ao contrato e do tipo de facturación configurado na liña de contrato. Se un rol ou categoría está configurado na liña de contrato como non imputable, a liña de estimación importada para ese rol ou categoría non é imputable e non se sumará ao valor contratado da liña de contrato.

Cando unha liña de contrato ten detalles de liña, os campos **Valor do contrato** e **Imposto estimado** da liña de contrato están resumidos e non se poden editar.

Cando se seleccionan varias opcións de resumo, o sistema tenta resumir mediante todas as opcións seleccionadas. A saída de resumo produce máis liñas de contrato importadas que se selecciona só unha opción de resumo.

Por exemplo, se o proxecto tiña as seguintes liñas de estimación de gastos:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Cando o usuario selecciona resumir por **Clase de transacción**, importarase a seguinte información:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Cando o usuario selecciona resumir por **Clase de transacción** e **Categoría**, importarase a seguinte información:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Cando o usuario selecciona resumir por **Clase de transacción**, **Categoría** e **Tarefa nó folla**, importarase o seguinte. Teña en conta que este resultado é o mesmo que no proxecto:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]