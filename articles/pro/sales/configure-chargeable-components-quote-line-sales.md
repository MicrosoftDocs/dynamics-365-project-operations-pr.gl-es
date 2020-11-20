---
title: Configurar os compoñentes imputables dunha liña de oferta - lite
description: Este tema ofrece información sobre a configuración de compoñentes imputables e non imputables nunha liña de oferta baseada en proxecto.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177104"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Configurar os compoñentes imputables dunha liña de oferta - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha liña de oferta baseada en proxecto ten o concepto de compoñentes *incluídos* e compoñentes *imputables*.

Os compoñentes incluídos están suxeitos a:

  - Método de facturación e divisións de clientes
  - Límites non superables 
  - Configuración de frecuencia de facturas definida na liña de oferta baseada en proxecto

Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**. O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de oferta:

  - Imputable
  - Non imputable

Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.

A imputabilidade defínese nas tarefas dunha liña de oferta de proxecto e aplícase a todas as clases de transaccións incluídas nesa liña. Se o campo **Incluír tarefas** dunha liña de contrato está definido como **Todo o proxecto** ou se deixa en branco, o separador **Tarefas imputables** non está dispoñible.

A imputabilidade defínese nos roles dunha liña de oferta de proxecto só se aplica á clase de transacción **Tempo**. Se o campo **Incluír tempo** está definido como **Non** nunha liña de oferta de proxecto, o separador **Roles imputables** non está dispoñible.

A imputabilidade defínese nas categorías de transacción dunha liña de oferta de proxecto e só se aplica á clase de transacción **Gasto**. Se o campo **Incluír gastos** está definido como **Non** nunha liña de oferta de proxecto, o separador **Categorías imputables** non está dispoñible.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Actualizar unha tarefa de proxecto para que sexa imputable ou non imputable

Unha tarefa de proxecto pode ser imputable ou non imputable no contexto dunha liña de oferta baseada en proxecto específica, o que fai posible a seguinte configuración:

Se unha liña de oferta baseada en proxecto inclúe **Tempo** e a tarefa **T1**, a tarefa está asociada á liña de oferta como imputable. Se hai unha segunda liña de oferta que inclúa **Gasto**, pode asociar a tarefa **T1** á liña de oferta como non imputable. O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos rexistrados na tarefa son non imputables.

O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Tarefas da liña de oferta**. Como alternativa, pode actualizar o tipo de facturación para unha tarefa de proxecto no campo **Tipo de facturación** na subgrade na configuración de facturación de tarefas que mostra as liñas de oferta asociadas a unha tarefa.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizar un rol para que sexa imputable ou non imputable

Un rol pode ser imputable ou non imputable no contexto dunha liña de oferta específica baseada en proxecto.

O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Roles imputables**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizar unha categoría de transacción para que sexa imputable ou non imputable

Unha categoría de transacción pode ser imputable ou non imputable nunha liña de oferta específica.

O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Categorías imputables**.

### <a name="resolve-chargeability"></a>Resolver a imputabiidade
Unha estimación ou dato real creada para tempo só se considerará imputable se **Tempo** se inclúe na liña de oferta e se **Tarefa** e **Rol** están configurados como imputables na liña de oferta.

Unha estimación ou dato real creada para gasto só se considerará imputable se **Gasto** se inclúe na liña de oferta e se **Tarefa** e **Categoría de transacción** están configurados como imputables na liña de oferta.

| Inclúe tempo | Inclúe gasto | Tarefas incluídas | Rol | Categoría | Tarefa | Facturación |
| --- | --- | --- | --- | --- | --- | --- |
| Si | Si | Todo o proxecto | Imputable | Imputable | Non se pode configurar | Facturación nun dato real de tempo: Imputable </br>Tipo de facturación no dato real de gasto: Imputable |
| Si | Si | Só tarefas seleccionadas | Imputable | Imputable | Imputable | Facturación nun dato real de tempo: Imputable</br>Tipo de facturación no dato real de gasto: Imputable |
| Si | Si | Só tarefas seleccionadas | Non imputable | Imputable | Imputable | Facturación nun dato real de tempo: Non imputable</br>Tipo de facturación no dato real de gasto: Imputable |
| Si | Si | Só tarefas seleccionadas | Imputable | Imputable | Non imputable | Facturación nun dato real de tempo: Non imputable</br> Tipo de facturación no dato real de gasto: Non imputable |
| Si | Si | Só tarefas seleccionadas | Non imputable | Imputable | Non imputable | Facturación nun dato real de tempo: Non imputable</br> Tipo de facturación no dato real de gasto: Non imputable |
| Si | Si | Só tarefas seleccionadas | Non imputable | Non imputable | Imputable | Facturación nun dato real de tempo: Non imputable</br> Tipo de facturación no dato real de gasto: Non imputable |
| No | Si | Todo o proxecto | Non se pode configurar | Imputable | Non se pode configurar | Facturación nun dato real de tempo: Non dispoñible </br>Tipo de facturación no dato real de gasto: Imputable |
| No | Si | Todo o proxecto | Non se pode configurar | Non imputable | Non se pode configurar | Facturación nun dato real de tempo: Non dispoñible </br>Tipo de facturación no dato real de gasto: Non imputable |
| Si | No | Todo o proxecto | Imputable | Non se pode configurar | Non se pode configurar | Facturación nun dato real de tempo: Imputable</br>Tipo de facturación no dato real de gasto: Non dispoñible |
| Si | No | Todo o proxecto | Non imputable | Non se pode configurar | Non se pode configurar | Facturación nun dato real de tempo: Non imputable </br>Tipo de facturación no dato real de gasto: Non dispoñible |
