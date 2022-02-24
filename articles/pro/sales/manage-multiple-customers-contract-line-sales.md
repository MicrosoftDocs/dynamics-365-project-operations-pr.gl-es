---
title: Xestionar de varios clientes en liñas de oferta baseada en contrato - lite
description: Este tema ofrece información sobre a xestión de varios clientes en liñas de contrato baseado en proxecto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f28e7d1363647621f7bd23504aa6d4ea3fc95fc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181610"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Xestionar de varios clientes en liñas de oferta baseada en contrato - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

As liñas de contrato baseado en proxecto poden incluír unha lista de clientes responsables do pagamento. Esta lista de clientes da liña de contrato baseado en proxecto pode ser a mesma que a lista de clientes do contrato, pero iso non é necesario. Cando se gaña unha oferta de proxecto e se crea un contrato de proxecto, a lista de clientes da liña de oferta cópiase na liña de contrato correspondente. Os clientes da oferta cópianse no contrato.

Cando se factura o contrato do proxecto, a lista de clientes da liña de contrato baseado en proxecto ten prioridade sobre a lista de clientes do contrato. A lista de clientes do contrato de proxecto só se usa para predefinir novas liñas de contrato.

Todos os clientes do contrato no separador **Clientes** do contrato do proxecto son por defecto clientes da liña de contrato en calquera nova liña de contrato creada para o contrato do proxecto. As liñas de contrato existentes non herdarán os novos rexistros de clientes do contrato creados despois delas.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Crear, actualizar ou eliminar un rexistro de cliente de liña de contrato

Pode crear, actualizar ou eliminar un cliente de liña de contrato no separador Clientes de liña de contrato na paxina Liña de contrato baseado en proxecto. Cando se engade un novo cliente na liña de contrato baseado en proxecto, tamén se engade ao contrato global como cliente do contrato cunha porcentaxe de facturación por defecto de cero por cento. A porcentaxe de división de facturación sobre o contrato global cópiase ás novas liñas de contrato e ao contrato do proxecto eventual. Non obstante, cando se factura a partir do contrato, é a porcentaxe da división de facturación no nivel da liña de contrato que se usa e non a porcentaxe de división de facturación no nivel do contrato global.

Abaixo amósanse os campos do rexistro de cliente de liña de **Contrato** dunha liña de contrato baseado en proxecto para ter en conta mentres traballa con ela:

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| **Conta** | Grade editable no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Todas as contas activas. Este campo bloquéase despois de que se crea o rexistro. Para actualizar o campo, elimine o rexistro e cree un novo rexistro. Se rexistrou algún dato real, non pode eliminar o rexistro. Non obstante, pode marcar a porcentaxe de división de facturación como cero para esa conta. Cando o rexistro está marcado como cero, os custos e ingresos futuros que se atribúan ou dividen a este cliente están afectados. | Cando escolle unha conta da lista principal de contas para engadilas e gardalas, o cliente da liña de contrato tamén se engade como cliente do contrato. Os clientes da liña de contrato úsanse cando se xeran facturas. |
| **Porcentaxe de división de facturación** | Grade editable no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Este campo representa a porcentaxe de cada transacción de vendas sen facturar que se atribuirá a este cliente de liña de contrato. | Os clientes da liña de contrato e as porcentaxes de división de facturación úsanse cando se crean datos reais despois da aprobación e cando se xera a factura. |
| **Límite non superable** | Grade editable no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Indica se hai un límite negociado ou tope do importe global que se lle facturará a este cliente pola liña de contrato. | O límite non superable para o cliente da liña de contrato úsase cando se crean os datos reais e se xeran as facturas. |
| **É arredondamento** | Grade editable no separador **Clientes de contrato** e formularios **Principal** e de **Creación rápida** para un cliente de liña de contrato. | Este campo indica se este cliente é un cliente de redondeo predefinido para esta liña de contrato baseado en proxecto. | Cando xera un dato real segundo a porcentaxe de división de facturación, pode haber algunhas diferenzas de redondeo. A este cliente atribúenselle as diferenzas de redondeo neste caso. |

## <a name="edit-billing-split-percentages"></a>Editar porcentaxes divididas de facturación

As porcentaxes de división de facturación poden editarse na grade. Cando as porcentaxes de división de facturación non totalicen o 100 por cento, producirase un erro. Despois de editar as porcentaxes de facturación, actualice a páxina para eliminar o erro.

Tamén pode seleccionar **Distribución uniforme** na subgrade dos clientes da liña de contrato. Esta acción distribúe uniformemente as divisións de facturación a todos os clientes da liña de contrato. Se hai algún factor de redondeo, engadirase ao cliente de redondeo. Un cliente de liña de contrato sempre está etiquetado como cliente de **Redondeo** coa marca **Redondeo** definida como **Si**.
