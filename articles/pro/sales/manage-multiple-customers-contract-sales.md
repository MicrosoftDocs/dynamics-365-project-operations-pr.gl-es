---
title: Xestionar varios clientes nunha en contratos de proxecto - lite
description: Este tema ofrece información sobre a xestión de varios clientes en contratos de proxecto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181315"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Xestionar varios clientes nunha en contratos de proxecto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Os contratos de proxecto en Dynamics 365 Project Operations admiten o escenario no que un acordo contractual implica varios clientes que financian un acordo. O separador **Resumo** na páxina **Contrato de proxecto** inclúe o campo **Cliente**. Este campo identifica o cliente principal da oferta. Pódense configurar outros clientes no separador **Clientes** da páxina **Contrato de proxecto**.

Todos os clientes do contrato que aparecen no contrato do proxecto son por defecto clientes da liña de contrato en calquera nova liña de contrato creada para o contrato do proxecto. As liñas de contrato baseado en proxecto existentes non herdan novos clientes de contrato a medida que se crean novos rexistros.

As liñas de contrato baseado en produto asócianse automaticamente ao cliente principal.

Pódense engadir, actualizar ou eliminar clientes de contrato e clientes de liña de contrato en calquera momento antes de gañar o contrato.

## <a name="primary-customer"></a>Cliente principal

O cliente que aparece no separador **Resumo** do contrato do proxecto, xa que o cliente potencial é o cliente principal do contrato. Cando tenta eliminar o cliente principal da lista de clientes do contrato, recibirá unha mensaxe de erro de que non se pode eliminar un rexistro de cliente principal nun contrato.

O cliente principal non se pode actualizar na lista de clientes do contrato. En vez diso, cambie o cliente potencial no separador **Resumo** do contrato. Cando se actualiza este campo na páxina **Resumo do contrato**, engádese o novo cliente como novo cliente de contrato coa marca **Principal**. O cliente principal anterior seguirá sendo un cliente no contrato.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Crear, actualizar ou eliminar un rexistro de cliente de contrato

Pódese crear, actualizar ou eliminar un cliente de contrato no separador **Clientes** na páxina **Contrato de proxecto**. Os campos da seguinte táboa figuran no rexistro de clientes de contrato dun contrato de proxecto e deben terse en conta mentres traballa co contrato.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| **Conta** | A grade pode editarse no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Indica todas as contas activas. Este campo bloquéase despois de que se crea o rexistro. Para actualizar a conta, elimine o rexistro e créeo de novo. Se rexistrou algún dato real ou se o rexistro do cliente de contrato é un cliente principal, non pode eliminar o rexistro. | Os clientes de contrato cópianse como clientes de liña de contrato cando se crea unha liña de contrato. |
| **Porcentaxe de división de facturación** | A grade pode editarse no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Representa a porcentaxe de cada transacción de vendas sen facturar que se atribúe a este cliente de liña de contrato. | Copiado a novas liñas de contrato e a clientes de liña de contrato de proxecto en novas liñas de contrato de proxecto. |
| **Facturar ao nome do contacto** | A grade pode editarse no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Este campo de texto debe usarse para identificar a persoa de contacto da factura deste cliente. Este campo tómase por defecto do rexistro de conta relacionado. | Copiado no campo **Factura a nome de contrato** da factura que se xera para este cliente. |
| **Nome de facturación** | A grade pode editarse no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato | Este campo de texto debe usarse para identificar a persoa de contacto da factura deste cliente. Este campo tómase por defecto do rexistro de conta relacionado. | Copiado no campo **Factura a nome de contrato** da factura que se xera para este cliente. |
| **Termos de pagamento** | A grade pode editarse no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Os valores tómanse por defecto do rexistro de conta relacionado. | Copiado no campo **Factura a nome de contrato** da factura que se xera para este cliente. |
| **É arredondamento** | A grade pode editarse no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato. | Indica se este cliente é un cliente de redondeo predefinido para este acordo. Só pode haber un cliente de redondeo nun contrato de proxecto. | Cando o custo e as vendas non facturadas por cantidade conducen a unha diferenza de redondeo, esa diferenza aplícase ao dato real que se asigna a este cliente. |
| **Límite non superable** | A grade pode editarse no separador **Clientes de contrato** e os formularios **Principal** e **Creación rápida** para un cliente de contrato | Indica se hai un límite negociado ou tope do importe global que se lle facturará ao cliente por este compromiso. | O **Límite non superable** configurado a nivel do cliente avaliarase nos **Datos reais de vendas sen facturar** que fan referencia a este cliente do contrato. |

## <a name="edit-billing-split-percentages"></a>Editar porcentaxes divididas de facturación

As porcentaxes de división de facturación poden editarse mediante a experiencia de edición da grade en liña. Cando as porcentaxes de división de facturación non totalicen o 100 por cento, recibirá un erro. Despois de editar as porcentaxes de facturación, actualice a páxina para rexeitar o erro.

Tamén pode seleccionar **Distribución uniforme** na subgrade **Clientes contratados** para asignar divisións de facturación uniformemente a todos os clientes do contrato. Se hai un factor de redondeo, engadirase ao cliente de redondeo. Un dos clientes do contrato sempre está etiquetado como cliente de **redondeo**, o que significa que o rexistro de cliente de contrato ten definida a marca de redondeo en **Si**. Normalmente, este é o cliente principal do contrato, pero tamén se pode cambiar.
