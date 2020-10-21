---
title: Xestionar de varios clientes en ofertas de proxecto
description: Este tema ofrece información sobre o traballo en ofertas que inclúen a varios clientes que financiarán o proxecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908126"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Xestionar de varios clientes en ofertas de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As ofertas de proxecto admiten a situación na que a proposta implica varios clientes que financiarán o acordo. O separador **Resumo** da oferta ten o campo **Cliente potencial**, que identifica o cliente principal do acordo. Pódense configurar outros clientes para o acordo no separador **Clientes** da oferta do proxecto.

Todos os clientes da oferta no separador **Clientes** da oferta do proxecto son por defecto os clientes de liña da oferta en calquera **nova** liña de oferta baseada en proxecto creada para a oferta. Calquera liña de oferta baseada en proxecto existente non herdará os novos rexistros de clientes da oferta creados despois dela.

Poden engadirse, actualizarse ou eliminarse clientes de oferta e clientes de liña de oferta en calquera momento antes de gañar a oferta. Un cliente válido na oferta debe establecerse como cliente na empresa propietaria ou entidade legal na páxina **Clientes**. As entidades legais créanse no módulo **Xestión e contabilidade de proxectos** de Dynamics 365 Project Operations e están dispoñibles como empresas nos módulos **Vendas e entrega de proxectos** de Project Operations.

## <a name="concept-of-a-primary-customer"></a>Concepto de cliente principal

O cliente que aparece no separador **Resumo** da oferta de proxecto como cliente potencial é o cliente principal da oferta. Se intenta eliminar o cliente principal da lista de clientes da oferta, recibirá un erro de que non se pode eliminar un rexistro de cliente principal nunha oferta.

Non se debe actualizar o cliente principal desde a lista de clientes da oferta. Non obstante, pode influír no cliente principal cambiando o cliente potencial no separador **Resumo** da oferta. Cando se actualiza este campo no **Resumo da oferta**, o cliente potencial que se acaba de seleccionar engádese como novo cliente da oferta co indicador **Principal** activado. O antigo cliente potencial seguirá sendo un cliente na oferta.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Crear, actualizar ou eliminar un rexistro de cliente de oferta

Pódese crear, actualizar ou eliminar un cliente de oferta desde o separador **Clientes de oferta** na páxina **Oferta**. Os campos indicados na táboa seguinte están no rexistro de clientes de oferta dunha oferta de proxecto.

| **Campo** | **Localización** | **Relevancia, finalidade e orientación** | **Impacto descendente** |
| --- | --- | --- | --- |
| Conta | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Indica todas as contas activas. Este campo bloquéase despois de que se crea o rexistro. Se quere actualizalo, elimine o rexistro e créeo de novo. Se rexistrou algún dato real ou se o rexistro do cliente da oferta é un cliente principal, poderá eliminar o rexistro. | Os clientes da oferta cópianse como clientes de liña de oferta cando se crea unha liña de oferta. Os clientes da oferta tamén se copian aos clientes do contrato do proxecto cando se gaña unha oferta. |
| Porcentaxe de división de facturación | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Representa a porcentaxe de cada transacción de vendas non facturada que se atribuirá a este cliente da oferta. | Copiado ás novas liñas de oferta creadas e aos clientes de contrato de proxecto. |
| Facturar ao nome do contacto | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Este é un campo de texto e debe usarse para identificar a persoa de contacto da factura deste cliente. Estas son por defecto as do rexistro da conta relacionada | Copiouse aos clientes de contrato de proxecto cando se gañou unha oferta e á súa vez ao campo Facturar ao nome do contacto na factura que se xera para este cliente. |
| Facturar a nome | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Este campo de texto debe usarse para identificar a persoa de contacto da factura deste cliente. | Copiouse aos clientes de contrato de proxecto cando se gaña unha oferta e á súa vez ao campo **Facturar ao nome do contrato** na factura que se xera para este cliente. |
| Condicións de pagamento | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Este é un conxunto de opcións con valores que son por defecto os do no rexistro da conta relacionada. | Copiouse aos clientes de contrato de proxecto cando se gaña unha oferta e á súa vez ao campo **Facturar ao nome do contrato** na factura que se xera para este cliente. |
| É arredondamento | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Indica se este cliente é un cliente de redondeo predefinido para este acordo. | Copiado aos clientes do contrato do proxecto cando se gaña unha oferta. |
| Empresa propietaria | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | A entidade legal coa que este cliente está establecido no módulo **Xestión de proxectos e contabilidade**. Este campo é de só lectura e configúrase na empresa propietaria da oferta. A lista de clientes para engadir no campo **Conta** xa está filtrado na lista desta empresa propietaria no módulo **Xestión e contabilidade de proxectos** de Project Operations. | A empresa propietaria equivale ao concepto de entidade legal no módulo **Xestión e contabilidade de proxectos** de Project Operations. Todos os custos e ingresos derivados deste proxecto contabilízanse no libro maior da empresa propietaria, |
| Límite non superable | Grade editable no separador **Clientes de oferta** e os formularios **Principal** e **Creación rápida** para un cliente da oferta. | Indica se hai un límite negociado ou tope para o importe total que se facturará a este cliente por este compromiso. | Copiado aos clientes do contrato do proxecto cando se gaña unha oferta. |

## <a name="editing-billing-split-percentages"></a>Edición de porcentaxes divididas de facturación

Pode editar as porcentaxes divididas de facturación usando a experiencia de edición de grade en liña. Cando as porcentaxes de división de facturación non totalicen o 100 %, producirase un erro. Despois de actualizar as porcentaxes de división de facturación, actualice a páxina para eliminar o erro.

Tamén pode probar a seleccionar **Distribución uniforme** na subgrade dos clientes da oferta Esta acción asigna divisións de facturación a todos os clientes da oferta. Se hai algún factor de redondeo, engadirase ao cliente de redondeo. Un dos clientes da oferta sempre está etiquetado como o cliente de redondeo. Isto significa que o rexistro do cliente da oferta ten o indicador **Redondeo** establecido como **Si**. Normalmente este é o principal cliente da oferta, pero se pode cambiar.