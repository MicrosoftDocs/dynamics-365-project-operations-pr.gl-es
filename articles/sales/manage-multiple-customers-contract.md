---
title: Xestionar varios clientes nunha en contratos de proxecto
description: Este tema ofrece información sobre como xestionar varios clientes nun contrato de proxecto.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dda8bc58c00082a9ef3835ea293003c63013983f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277966"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Xestionar varios clientes nunha en contratos de proxecto

Este tema ofrece información sobre como xestionar varios clientes nun contrato de proxecto. Pode usar un contrato de proxecto cando se precise un acordo contractual para varios clientes para financiar un acordo. Na páxina **Contrato do proxecto**, o separador **Resumo** inclúe información sobre o cliente principal dun acordo. Pódense engadir outros clientes que participen no acordo ao separador **Clientes**.

Todos os clientes do contrato no separador **Clientes** do contrato do proxecto son por defecto clientes da liña de contrato en calquera nova liña de contrato baseado en proxecto creada para o contrato do proxecto. As liñas de contrato baseado en proxecto existentes non herdan novos clientes de contrato a medida que se crean nun momento posterior.

Pode engadir, actualizar ou eliminar clientes de contrato e de liña de contrato en calquera momento antes de que se gañe o contrato. Un cliente no contrato do proxecto debe establecerse como cliente na empresa propietaria ou entidade legal na páxina **Clientes**. As entidades legais configúranse no módulo **Xestión e contabilidade de proxectos** de Dynamics 365 Project Operations e están dispoñibles como empresas nos módulos **Vendas de proxecto** e **Entrega** de Project Operations.

## <a name="primary-customers"></a>Clientes primarios

O cliente potencial que aparece no separador **Resumo** do contrato do proxecto é o cliente principal do contrato. Non pode actualizar o cliente primario lista de clientes do contrato. Se tenta eliminar o cliente principal dunha lista de clientes do contrato, producirase un erro que di de que non se pode eliminar un rexistro de cliente principal nun contrato. En lugar diso, cambie o cliente no campo **Cliente potencial** no separador **Resumo** do contrato do proxecto. Cando actualice este campo, se engade o novo cliente seleccionado como novo cliente do contrato coa marca **Primario** en **Si**. O cliente principal anterior segue sendo un cliente no contrato, pero xa non é o cliente principal.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Crear, actualizar ou eliminar un rexistro de cliente de contrato

Pode crear, actualizar ou eliminar un cliente de contrato no separador **Clientes de contrato** na páxina **Contrato**. Os seguintes campos están incluídos no rexistro de cliente de contrato dun contrato de proxecto.

| **Campo** | **Localización** | **Descrición** | 
| --- | --- | --- | 
| Conta | Grade editable no separador **Clientes de contrato** e os formularios principal e de creación rápida para un cliente de contrato. | Indica todas as contas activas. Este campo bloquéase despois de que se crea o rexistro. Para actualizar o rexistro, ten que eliminalo e logo crealo de novo. Se rexistrou algún dato real ou se o rexistro do cliente de contrato é un cliente principal, non pode eliminar o rexistro. Cando se crea unha liña de contrato, os clientes de contrato cópianse como clientes de liña de contrato. |
| Porcentaxe de división de facturación | Grade editable no separador **Clientes de contrato** e os formularios principal e de creación rápida para un cliente de contrato. | Representa a porcentaxe de cada transacción de vendas sen facturar que se atribúe ao cliente de contrato. Cando se crean novas liñas de contrato de proxecto, a porcentaxe dividida de facturación copiarase ás novas liñas de contrato creadas e aos clientes de liña de contrato do proxecto. |
| Facturar ao nome do contacto | Grade editable no separador **Clientes de contrato** e os formularios principal e de creación rápida para un cliente de contrato. | Este campo de texto debería usarse para identificar a persoa de contacto da factura para o cliente. O valor por defecto ven do rexistro de conta relacionado. O nome do contacto cópiase a **Facturar a nome de contrato** na factura que se xera para o cliente. |
| Nome de facturación | Grade editable no separador **Clientes de contrato** e os formularios principal e de creación rápida para un cliente de contrato. | Use este campo para identificar a persoa de contacto da factura para o cliente. O valor por defecto ven do rexistro de conta relacionado. O nome cópiase ao campo **Facturar a nome de contrato** da factura que se xera para o cliente. |
| Condicións de pagamento | Grade editable no separador **Clientes de contrato** e páxinas principal e de creación rápida para un cliente de contrato. | O valor por defecto ven do rexistro de conta relacionado. Os termos cópianse a **Facturar a nome de contrato** na factura que se xera para o cliente. |
| Empresa propietaria | Grade editable no separador **Clientes de contrato de proxecto** e as páxinas principal e de creación rápida para un cliente de contrato de proxecto. | A entidade legal na que está configurado o cliente no módulo **Xestión e contabilidade de proxectos**. Este campo é de só lectura e configúrase á empresa propietaria do contrato do proxecto.</br>A lista de clientes para engadir no campo **Conta** xa está filtrado na lista da empresa propietaria no módulo **Xestión e contabilidade de proxectos** de Project Operations. A empresa propietaria é igual á entidade legal no módulo **Xestión e contabilidade de proxectos** de Project Operations. Todos os custos e ingresos derivados do proxecto contabilízanse no libro maior xeral da empresa propietaria. |
| É arredondamento | Grade editable no separador **Clientes de contrato** e os formularios principal e de creación rápida para un cliente de contrato. | Indica se o cliente é un cliente de redondeo predefinido para o acordo. Só pode haber un cliente de redondeo nun contrato de proxecto. Cando o custo e as vendas non facturadas divídense por cantidade conducen a unha diferenza de redondeo, esa diferenza aplícase ao dato real que se asigna ao cliente. |
| Límite non superable | Grade editable no separador **Clientes de contrato** e os formularios principal e de creación rápida para un cliente de contrato. | Indica se hai un límite negociado ou tope do importe global que se lle facturará ao cliente polo compromiso. O límite non superable configurado a nivel do cliente de contrato avalíase nos datos reais de vendas sen facturar que fan referencia ao cliente do contrato. |

## <a name="edit-billing-split-percentages"></a>Editar porcentaxes divididas de facturación

Pode editar as porcentaxes de división de facturación na grade. Cando as porcentaxes de división de facturación non totalicen o 100 por cento, prodúcese un erro. Despois de editar unha porcentaxes de división de facturación, actualice a páxina **Contrato de proxecto** para eliminar o erro.

Tamén pode seleccionar **Distribución uniforme** na subgrade de clientes de contrato do proxecto. As divisións de facturación asígnanse a todos os clientes do contrato do proxecto. Se hai algún factor de redondeo, o factor engadirase ao cliente de redondeo. Un dos clientes do contrato sempre ten a marca de **Redondeo** definida como **Si**. Ese cliente é o cliente de redondeo. Normalmente, o cliente de redondeo tamén é o cliente principal do contrato, pero iso non é necesario.


[!INCLUDE[footer-include](../includes/footer-banner.md)]