---
title: Xestionar varios clientes en liñas de oferta baseada en proxecto
description: Este tema ofrece información sobre como xestionar varios clientes en liñas de oferta baseada en proxecto.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4fa0adc877797d782173f29690b33d38ba7f8dcd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277921"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Xestionar varios clientes en liñas de oferta baseada en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

As liñas de oferta baseada en proxecto admiten situacións nas que cada liña de oferta ten unha lista de clientes que a pagan. Esta lista de clientes da liña de oferta baseada en proxecto pode ser a mesma que a lista de clientes da oferta. Tamén pode cambiar a lista de clientes para que sexan diferentes. Para crear o eventual contrato do proxecto cando se gañe unha oferta de proxecto, a lista de clientes da liña de oferta baseada en proxecto copiarase na liña de contrato baseado en proxecto correspondente. Os clientes da oferta baseada en proxecto cópianse no contrato do proxecto.

Cando factura o contrato eventual do proxecto, a lista de clientes da liña de contrato baseado en proxecto ten prioridade sobre a lista do contrato do proxecto. A lista de clientes do contrato de proxecto só se usa para predefinir novas liñas de contrato de proxecto.

Todos os clientes da oferta no separador **Clientes** da oferta do proxecto son por defecto os clientes de liña da oferta en calquera nova liña de oferta baseada en proxecto creada para a oferta de proxecto. Calquera liña de oferta baseada en proxecto existente non herda os novos rexistros de clientes da oferta creados despois dela.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Crear, actualizar ou eliminar un rexistro de cliente de liña de oferta

Pode crear, actualizar ou eliminar un cliente de liña de oferta no separador **Clientes de liña de oferta** na páxina **Liña de oferta baseada en proxecto**. Cando engade un novo cliente na liña de oferta baseada en proxecto, o cliente tamén se engade á oferta global como cliente da oferta, cunha porcentaxe de división de facturación predefinida na oferta global do 0 %. A porcentaxe de división de facturación na oferta global cópiase ás novas liñas de oferta e ao eventual contrato do proxecto. Non obstante, cando factura desde o contrato, úsase a porcentaxe de división de facturación no nivel da liña de oferta, non a porcentaxe de oferta de facturación no nivel de contrato global. 

A seguinte táboa mostra os campos do rexistro de cliente de liña de oferta dunha liña de oferta baseada en proxecto.

| Campo | Localización | Descrición e orientación | Impacto descendente |
| --- | --- | --- | --- |
| **Conta** | Unha grade editable no separador **Clientes de liña de oferta**, o formulario principal e o formulario de creación rápida para un cliente de liña de oferta. | Indica todas as contas activas. Este campo bloquéase despois de que se crea o rexistro. Se precisa actualizar o campo, elimine e cree de novo o rexistro. Se gravou algún dato real, non pode eliminar o rexistro. | Cando escolle unha conta da lista principal de contas para engadir, o cliente da liña de oferta tamén se engade como cliente da oferta Os clientes de liña de oferta tamén se copian aos clientes de liña de contrato do proxecto cando se gaña unha oferta. |
| **Porcentaxe de división de facturación** | Unha grade editable no separador **Clientes de liña de oferta**, o formulario principal e o formulario de creación rápida para un cliente de liña de oferta. | Representa a porcentaxe de cada transacción de vendas non facturada que se atribuirá a este cliente de liña de oferta. | Copiado aos clientes de liña de contrato de proxecto. |
| **Límite non superable** | Unha grade editable no separador **Clientes de liña de oferta**, o formulario principal e o formulario de creación rápida para un cliente de liña de oferta. | Indica se hai un límite negociado ou tope para o importe total que se facturará a este cliente por esta liña ofertada. | Copiado aos clientes de liña de contrato do proxecto cando se gaña unha oferta. |
| **Empresa propietaria** | Unha grade editable no separador **Clientes de liña de oferta**, o formulario principal e o formulario de creación rápida para un cliente de liña de oferta. | A entidade legal na que este cliente está establecido no módulo **Xestión e contabilidade de proxectos**. Este campo é de só lectura e configúrase na empresa propietaria da oferta. A lista de clientes para engadir no campo **Conta** xa está filtrado na lista da empresa propietaria no módulo **Xestión e contabilidade de proxectos** de Project Operations. | A empresa propietaria equivale ao concepto de entidade legal. Todos os custos e ingresos que se derivan deste proxecto contabilízanse no libro maior da empresa propietaria. |
| **É arredondamento** | Unha grade editable no separador **Clientes de liña de oferta**, o formulario principal e o formulario de creación rápida para un cliente de liña de oferta. | Indica se este cliente é un cliente de redondeo predefinido para esta liña de oferta baseada en proxecto. | Copiado aos clientes de contrato do proxecto cando se gaña unha oferta. |

## <a name="edit-billing-split-percentages"></a>Editar porcentaxes divididas de facturación

Pode editar porcentaxes divididas de facturación en liña. Cando as porcentaxes de división de facturación non totalicen o 100 %, prodúcese un erro. Despois de editar as porcentaxes de división de facturación, actualice a páxina de liña de oferta para eliminar o erro.

Utilice a acción de distribución uniforme na subgrade de clientes de liña de oferta para asignar divisións de facturación a todos os clientes de liña de oferta. Se hai un factor de redondeo, engadirase ao cliente de redondeo. Un dos clientes da liña de oferta sempre está etiquetado como cliente de redondeo, o que significa que o rexistro de cliente da liña de oferta ten o indicador de redondeo establecido en **Si**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]