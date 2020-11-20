---
title: Configurar compoñentes imputables dunha liña de contrato baseado en proxecto
description: Este tema ofrece información sobre os compoñentes incluídos, imputables e non imputables nas liñas de contrato.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d6f67d5dc6b94148d437b3399229c1235c702c6a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128686"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurar compoñentes imputables dunha liña de contrato baseado en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Unha liña de contrato baseada en proxecto ten o concepto de compoñentes incluídos, imputables e non imputables.

Os compoñentes incluídos están suxeitos ao método de facturación, divisións de clientes, os límites que non se deben superar e configuración de frecuencia de facturas definidos na liña de contrato baseado en proxecto.

Un subconxunto dos compoñentes incluídos pódese marcar como imputable ao actualizar o campo **Tipo de facturación**.

Os compoñentes imputables poden definirse en roles e categorías de transacción.

Para unha liña de contrato de proxecto, a imputabilidade definida nun rol só se aplica á clase de transacción **Tempo**. Se o campo **Incluír tempo** está definido como **Non** nunha liña de contrato de proxecto, o separador **Roles imputables** non está dispoñible.

A imputabilidade definida nas categorías de transacción dunha liña de contrato de proxecto só se aplica á clase de transacción **Gasto**. Se **Incluír gastos** está definido como **Non** nunha liña de contrato de proxecto, o separador **Categorías imputables** non está dispoñible.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizar un rol para que sexa imputable ou non imputable

Un rol pode ser imputable ou non imputable nunha liña de contrato baseado en proxecto.

No separador **Roles imputables** dunha liña de contrato baseado en proxecto, na subgrade **Categorías imputables**, no campo **Tipo de facturación**, actualice o tipo de facturación para un rol.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizar unha categoría de transacción para que sexa imputable ou non imputable

Unha categoría de transacción pode ser imputable ou non imputable nunha liña de contrato baseado en proxecto específica.

No separador **Categorías imputables** dunha liña de contrato baseado en proxecto, na subgrade **Categorías imputables**, no campo **Tipo de facturación**, actualice o tipo de facturación para unha transacción.

### <a name="resolve-chargeability"></a>Resolver a imputabiidade

Unha estimación ou dato real creada para tempo só se considerará imputable se o tempo se inclúe na liña de contrato e se o rol está configurado como imputables na liña de contrato.

Unha estimación ou dato real creada para gasto só se considerará imputable se o gasto se inclúe na liña de contrato e se a categoría de transacción está configurada como imputable na liña de contrato.

| Inclúe tempo | Inclúe gasto | Rol | Categoría | Tarefa |
| --- | --- | --- | --- | --- |
| Si | Si | Imputable | Imputable | Facturación nun dato real de tempo: Imputable </br>Tipo de facturación nun dato real de gasto: Imputable |
| Si | Si | Non imputable | Imputable | Facturación nun dato real de tempo: Non imputable </br>Tipo de facturación nun dato real de gasto: Imputable |
| Si | Si | Non imputable | Non imputable | Facturación nun dato real de tempo: Non imputable </br>Tipo de facturación nun dato real de gasto: Non imputable |
| No | Si | Non se pode configurar | Imputable | Facturación nun dato real de tempo: Non dispoñible </br>Tipo de facturación nun dato real de gasto: Imputable |
| No | Si | Non se pode configurar | Non imputable | Facturación nun dato real de tempo: Non dispoñible </br>Tipo de facturación nun dato real de gasto: Non imputable |
| Si | No | Imputable | Non se pode configurar | Facturación nun dato real de tempo: Imputable </br>Tipo de facturación nun dato real de gasto: Non dispoñible |
| Si | No | Non imputable | Non se pode configurar | Facturación nun dato real de tempo: Non imputable </br> Tipo de facturación nun dato real de gasto: Non dispoñible |
