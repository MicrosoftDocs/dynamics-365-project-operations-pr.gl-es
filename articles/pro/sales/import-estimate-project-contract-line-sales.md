---
title: Importar unha estimación a unha liña de contrato baseado en proxecto - lite
description: Este tema ofrece información sobre como importar estimacións financeiras dun proxecto a unha liña de contrato.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b462af163fef1bfcbbc4f945df722d4e8a71fb1a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177464"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importar unha estimación a unha liña de contrato baseado en proxecto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Dynamics 365 Project Operations, pode importar estimacións dun proxecto a unha liña de contrato baseado en proxecto.

1. Verifique que o campo **Proxecto** da liña de contrato baseado en proxecto está enchido.
2. No separador **Detalles de liña de contrato**, na subgrade, seleccione **Importar desde a estimación do proxecto**. Ábrese unha páxina de diálogo con opcións de resumo. As opcións de resumo dispoñibles son **Clase de transacción**, **Categoría**, **Rol** e **Tarefa de proxecto**.
3. En función da selección de resumo, cópianse as estimacións do proxecto para todas as clases de transaccións e tarefas incluídas nesta liña de contrato. Para comprobar que clases de transacción se inclúen, seleccione o separador **Xeral** na liña de contrato baseado en proxecto e comprobe os valores dos campos **Incluír tempo**, **Incluír gastos** e **Incluír taxas**. 
4. Para ver que tarefas están incluídas, seleccione o separador **Tarefas imputables** na liña de contrato. Segundo as tarefas asociadas que teñen o campo **Clases de transaccións incluídas** definido como **Si**, todas as estimacións para esas combinacións de tarefas e clases de transaccións impórtanse á liña de contrato.

Cando importe estimacións, o sistema predefine os prezos en función das listas de prezos do proxecto anexas ao contrato e do tipo de facturación configurado na liña de contrato. Se unha tarefa, rol ou categoría está configurado na liña de contrato como non imputable, a liña de estimación importada non será imputable e non se sumará ao valor contratado da liña de contrato.

Cando unha liña de contrato ten detalles de liña, os campos **Valor do contrato** e **Imposto estimado** da liña de contrato están resumidos e non se poden editar.

Cando se seleccionan varias opcións de resumo, o sistema tenta resumir mediante todas as opcións seleccionadas. A saída de resumo produce máis liñas de contrato importadas que se selecciona só unha opción de resumo.

Por exemplo, se o proxecto ten as seguintes liñas de estimación de gastos:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Cando o usuario selecciona resumir por **Clase de transacción**, importarase a seguinte información:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Cando o usuario selecciona resumir por **Clase de transacción** e **Categoría**, importarase a seguinte información:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Cando o usuario selecciona resumir por **Clase de transacción**, **Categoría** e **Tarefa nó folla**, importarase o seguinte. Teña en conta que este resultado é o mesmo que no proxecto:

| Tarefa | Categoría | Data | Importe | Prezo por unidade | Importe  |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifas aéreas | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |
