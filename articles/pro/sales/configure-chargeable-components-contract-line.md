---
title: Configurar compoñentes imputables dunha liña de contrato baseado en proxecto - lite
description: Este tema ofrece información sobre como engadir compoñentes imputables a liñas de contrato en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 46429c94ca9aa1ebbbe9fc689a9a5bd6c52dc59e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177149"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Configurar compoñentes imputables dunha liña de contrato baseado en proxecto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha liña de contrato baseado en proxecto ten compoñentes *incluídos* e compoñentes *imputables*.

Os compoñentes incluídos son compoñentes suxeitos a:

  - Método de facturación e divisións de clientes
  - Límites non superables 
  - Configuración de frecuencia de facturas definida na liña de contrato baseado en proxecto

Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**. O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de contrato:

  - Imputable
  - Non imputable

Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.

A imputabilidade defínese nas tarefas dunha liña de contrato de proxecto e aplícase a todas as clases de transaccións incluídas na liña. Se o campo **Incluír tarefas** dunha liña de contrato está en branco ou definido como **Todo o proxecto**, o separador **Tarefas imputables** non estará dispoñible.

A imputabilidade definida nos roles dunha liña de contrato de proxecto só se aplica á clase de transacción **Tempo**. Se o campo **Incluír tempo** dunha liña de contrato está en branco ou definido como **Non**, o separador **Roles imputables** non estará dispoñible.

A imputabilidade definida nas categorías de transacción dunha liña de contrato de proxecto só se aplica á clase de transacción **Gasto**. Se o campo **Incluír gastos** dunha liña de contrato está en branco ou definido como **Non**, o separador **Categorías imputables** non estará dispoñible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualizar unha tarefa do proxecto como imputable ou non imputable

Unha tarefa de proxecto pode ser imputable ou non imputable nunha liña de contrato específica, o que fai posible a seguinte configuración:

Se inclúe unha liña de contrato baseado en proxecto inclúe **Tempo** e unha tarefa determinada, **T1** asóciase a ela como imputable. Se hai unha segunda liña de contrato que inclúa **Gasto**, pode asociar a tarefa T1 á liña de contrato como non imputable. O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos son non imputables.

O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** da liña de contrato actualizando o campo **Tipo de facturación** na subgrade de tarefas da liña de contrato. Como alternativa, pode actualizar o campo **Tipo de facturación** na subgrade da tarefa Configuración de facturación dun proxecto que mostra as liñas de contrato asociadas a unha tarefa.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualizar un rol do proxecto como imputable ou non imputable

Un rol pode ser imputable ou non imputable nunha liña de contrato específica.

O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de contrato. Para iso, actualice o campo **Tipo de facturación** na subgrade **Roles imputables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualizar unha categoría de transacción como imputable ou non imputable

Unha categoría de transacción pode ser imputable ou non imputable nunha liña de contrato específica.

O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de contrato baseado en proxecto. Para iso, actualice o campo **Tipo de facturación** na subgrade **Categorías imputables**.

### <a name="resolve-chargeability"></a>Resolver a imputabiidade

Unha estimación ou dato real creada para tempo só se considerará imputable se **Tempo** se inclúe na liña de contrato e se **Tarefa** e **Rol** están configurados como imputables na liña de contrato.

Unha estimación ou dato real creada para gasto só se considerará imputable se **Gasto** se inclúe na liña de contrato e se as categorías **Tarefa** e **Transacción** están configuradas como imputables na liña de contrato.


| Inclúe tempo | Inclúe gasto | Inclúe tarefas | Rol           | Categoría       | Tarefa                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Si           | Si              | Todo o proxecto | Imputable     | Imputable     | Facturación nun dato real de tempo: **Imputable** </br> Tipo de facturación no dato real de gasto: **Imputable**           |
| Si           | Si              | Tarefas seleccionadas | Imputable     | Imputable     | Facturación nun dato real de tempo: **Imputable** </br> Tipo de facturación no dato real de gasto: **Imputable**           |
| Si           | Si              | Tarefas seleccionadas | Non imputable | Imputable     | Facturación nun dato real de tempo: **Non imputable** </br> Tipo de facturación no dato real de gasto: **Imputable**       |
| Si           | Si              | Tarefas seleccionadas | Imputable     | Imputable     | Facturación nun dato real de tempo: **Non imputable** </br> Tipo de facturación no dato real de gasto: **Non imputable** |
| Si           | Si              | Tarefas seleccionadas | Non imputable | Imputable     | Facturación nun dato real de tempo: **Non imputable** </br> Tipo de facturación no dato real de gasto: **Non imputable** |
| Si           | Si              | Tarefas seleccionadas | Non imputable | Non imputable | Facturación nun dato real de tempo: **Non imputable** </br> Tipo de facturación no dato real de gasto: **Non imputable** |
| No            | Si              | Todo o proxecto | Non se pode configurar   | Imputable     | Facturación nun dato real de tempo: **Non dispoñible**</br>Tipo de facturación no dato real de gasto: **Imputable**          |
| No            | Si              | Todo o proxecto | Non se pode configurar   | Non imputable | Facturación nun dato real de tempo: **Non dispoñible**</br> Tipo de facturación no dato real de gasto: **Non imputable**     |
| Si           | No               | Todo o proxecto | Imputable     | Non se pode configurar   | Facturación nun dato real de tempo: **Imputable** </br> Tipo de facturación no dato real de gasto: **Non dispoñible**        |
| Si           | No               | Todo o proxecto | Non imputable | Non se pode configurar   | Facturación nun dato real de tempo: **Non imputable** </br>Tipo de facturación no dato real de gasto: **Non dispoñible**   |
