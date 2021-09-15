---
title: Xestionar varios clientes en ofertas de proxecto - lite
description: Este tema ofrece información sobre o traballo en ofertas con varios clientes que financiarán o proxecto. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec5cd77318afdbfb01af2f1dc9ad151849374593
ms.sourcegitcommit: bbcfb917667e319247f6e57143f87a3e89fa5077
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440775"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Xestionar varios clientes en ofertas de proxecto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

As ofertas de proxecto admiten a situación na que a proposta implica varios clientes que financiarán o acordo. O separador **Resumo** da oferta ten o campo **Cliente potencial** que identifica o cliente principal do acordo. Pódense configurar outros clientes para o acordo no separador **Clientes** da oferta do proxecto.

Todos os clientes da oferta no separador **Clientes** da oferta do proxecto son por defecto os clientes de liña da oferta en calquera **nova** liña de oferta baseada en proxecto creada para a oferta. Calquera liña de oferta baseada en proxecto existente non herdará os novos rexistros de clientes da oferta creados despois dela.

As liñas de oferta baseadas en produto asócianse automaticamente ao cliente principal que tamén é o cliente no campo **Cliente potencial** no separador **Resumo** da oferta.

Poden engadirse, actualizarse ou eliminarse clientes de oferta e clientes de liña de oferta en calquera momento antes de gañar a oferta.

## <a name="concept-of-a-primary-customer"></a>Concepto de cliente principal

O cliente que está no separador de resumo da oferta de proxecto como cliente potencial é o cliente principal da oferta. Cando intenta eliminar o cliente principal da lista de clientes da oferta, verá un erro de que non se pode eliminar un rexistro de cliente principal nunha oferta.

Non se debe actualizar o cliente principal desde a lista de clientes da oferta. Non obstante, pode influír no cliente principal cambiando o cliente potencial no separador **Resumo** da oferta. Cando se actualiza este campo no **Resumo da oferta**, o cliente potencial que se acaba de seleccionar engádese como novo cliente da oferta co indicador **Principal** activado. O antigo cliente potencial seguirá sendo un cliente na oferta.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Crear, actualizar ou eliminar un rexistro de cliente de oferta

Pódese crear, actualizar ou eliminar un cliente de oferta desde o separador **Clientes de oferta** na páxina **Oferta**. Os campos indicados na táboa seguinte están no rexistro de clientes de oferta dunha oferta de proxecto.

| **Campo** | **Localización** | **Descrición** | **Impacto descendente** |
| --- | --- | --- | --- |
| Conta | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Indica todas as contas activas. Este campo bloquéase despois de que se crea o rexistro. Se quere actualizalo, elimine o rexistro e créeo de novo. Se rexistrou algún dato real ou se o rexistro do cliente da oferta é un cliente principal, non se lle permitirá eliminar o rexistro. | Os clientes da oferta cópianse como clientes de liña de oferta cando se crea unha liña de oferta. Os clientes da oferta tamén se copian aos clientes do contrato do proxecto cando se gaña unha oferta. |
| Porcentaxe de división de facturación | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Representa a porcentaxe de cada transacción de vendas non facturada que se atribuirá a este cliente da oferta. | Copiado ás novas liñas de oferta e aos clientes de contrato de proxecto. |
| Facturar ao nome do contacto | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Este é un campo de texto e debe usarse para identificar a persoa de contacto da factura deste cliente. Estas son por defecto as do rexistro da conta relacionada | Copiouse aos clientes de contrato de proxecto cando se gañou unha oferta e á súa vez ao campo Facturar ao nome do contacto na factura que se xera para este cliente. |
| Facturar a nome | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Este campo de texto debe usarse para identificar a persoa de contacto da factura deste cliente. | Copiouse aos clientes de contrato de proxecto cando se gaña unha oferta e á súa vez ao campo **Facturar ao nome do contrato** na factura que se xera para este cliente. |
| Condicións de pagamento | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Este é un conxunto de opcións con valores que son por defecto os do no rexistro da conta relacionada. | Copiouse aos clientes de contrato de proxecto cando se gaña unha oferta e, á súa vez, ao campo **Facturar ao nome do contrato** na factura que se xera para este cliente. |
| É arredondamento | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Indica se este cliente é un cliente de redondeo predefinido para este acordo. | Copiado aos clientes do contrato do proxecto cando se gaña unha oferta. |
| Límite non superable | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Indica se hai un límite negociado ou tope para o importe total que se facturará a este cliente por este compromiso | Copiado aos clientes do contrato do proxecto cando se gaña unha oferta. |

## <a name="editing-billing-split-percentages"></a>Edición de porcentaxes divididas de facturación

Pode editar as porcentaxes divididas de facturación usando a experiencia de edición de grade en liña. Cando as porcentaxes de división de facturación non totalicen o 100 %, producirase un erro. Despois de actualizar as porcentaxes de división de facturación, actualice a páxina para eliminar o erro.

Tamén pode probar a seleccionar **Distribución uniforme** na subgrade dos clientes da oferta. Esta acción asigna divisións de facturación a todos os clientes da oferta. Se hai algún factor de redondeo, engadirase ao cliente de redondeo. Un dos clientes da oferta sempre está etiquetado como o cliente de redondeo. Isto significa que o rexistro do cliente da oferta ten o indicador **Redondeo** establecido como **Si**. Normalmente este é o principal cliente da oferta, pero se pode cambiar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
