---
title: Configurar os compoñentes imputables dunha liña de oferta baseada en proxecto
description: Este tema ofrece información sobre compoñentes incluídos, imputables e non imputables en liñas de oferta baseada en proxecto.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 251d0013b445d2f7d17fbe1908f0db2e05cfc2670ac667deb363c98f608a2aef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003994"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configurar os compoñentes imputables dunha liña de oferta baseada en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Unha liña de oferta baseada en proxecto pode ter compoñentes incluídos e compoñentes imputables.

Os compoñentes incluídos están suxeitos ao método de facturación, as divisións de clientes, os límites non superables e a configuración de frecuencia de facturación que se definen na liña de oferta baseada en proxecto.
Pódese marcar un subconxunto dos compoñentes incluídos como imputable mediante o uso de **Tipo de facturación**. Pode seleccionar unha das seguintes opcións no campo **Tipo de facturación** no contexto dunha liña de oferta:

   - Imputable
   - Non imputable

Os compoñentes imputables poden definirse en roles e categorías de transacción.

A imputabilidade que se define nos roles para unha liña de oferta de proxecto só se aplica á clase de transacción **Tempo**. Se unha liña de oferta de proxecto ten **Incluír tempo** = **Non**, o separador **Roles imputables** non está dispoñible.

A imputabilidade que se define nas categorías de transacción para unha liña de oferta de proxecto só se aplica á clase de transacción **Gasto**. Se unha liña de oferta de proxecto ten **Incluír gastos** = **Non**, o separador **Categorías imputables** non está dispoñible.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizar un rol para que sexa imputable ou non imputable
Un rol pode ser imputable ou non imputable nunha liña de oferta baseada en proxecto. O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de oferta baseada en proxecto. Para facer isto, actualice **Tipo de facturación** na subgrade **Roles imputables**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizar unha categoría de transacción para que sexa imputable ou non imputable
Unha categoría de transacción pode ser imputable ou non imputable nunha liña de oferta baseada en proxecto. O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de oferta baseada en proxecto. Para iso, actualice o campo **Tipo de facturación** na subgrade **Categorías imputables**. 

## <a name="resolve-chargeability"></a>Resolver a imputabiidade

Unha estimación ou un dato real creado para tempo só se considerará imputable se o tempo se inclúe na liña de oferta e se o rol está configurado como imputable.
Unha estimación ou un dato real creado para un gasto só se considerará imputable se o gasto se inclúe na liña de oferta e se a categoría de transacción está configurada como imputable na liña de oferta. A seguinte táboa mostra como se impón por defecto a imputabilidade en cada dato real. Os valores predefinidos baséanse nos compoñentes incluídos e no tipo de facturación que se configura na liña de oferta.

| Inclúe tempo | Inclúe gasto | Rol | Categoría | Tarefa |
| --- | --- | --- | --- | --- |
| Si | Si | Imputable | Imputable | Facturación nun dato real de tempo: Imputable </br>Tipo de facturación nun dato real de gasto: Imputable |
| Si | Si | Non imputable | Imputable | Facturación nun dato real de tempo: Non imputable </br>Tipo de facturación nun dato real de gasto: Imputable |
| Si | Si | Non imputable | Non imputable | Facturación nun dato real de tempo: Non imputable </br>Tipo de facturación nun dato real de gasto: Non imputable |
| No | Si | Non se pode configurar | Imputable | Facturación nun dato real de tempo: Non dispoñible </br>Tipo de facturación nun dato real de gasto: Imputable |
| No | Si | Non se pode configurar | Non imputable | Facturación nun dato real de tempo: Non dispoñible </br>Tipo de facturación nun dato real de gasto: Non imputable |
| Si | No | Imputable | Non se pode configurar | Facturación nun dato real de tempo: Imputable </br>Tipo de facturación nun dato real de gasto: Non dispoñible |
| Si | No | Non imputable | Non se pode configurar | Facturación nun dato real de tempo: Non imputable </br> Tipo de facturación nun dato real de gasto: Non dispoñible |


[!INCLUDE[footer-include](../includes/footer-banner.md)]