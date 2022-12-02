---
title: Facturación de fornecedores - Concepto e creación
description: Este artigo describe o concepto de facturas de fornecedor, escenarios de uso e como crear facturas de fornecedor en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261932"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Facturación de fornecedores - Concepto e creación

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

A facturación de fornecedores en Microsoft Dynamics 365 Project Operations pódese usar para rexistrar os custos das entregas de servizos e/ou materiais nun proxecto por parte dos fornecedores.

Cando os servizos e/ou materiais son subcontratados a un fornecedor, un subcontrato representa o acordo contractual con ese fornecedor. A medida que o fornecedor presta os servizos ou os materiais son recibidos e utilizados nas tarefas do proxecto, os custos rexístranse no proxecto. Periodicamente, o fornecedor envía facturas que se verifican e coinciden cos custos que se rexistran no proxecto. Despois de completar o proceso de verificación, a factura do fornecedor é confirmada e liberada para o pago.

## <a name="scenarios-for-use"></a>Escenarios de uso

As facturas de fornecedor en Project Operations pódense usar para dous escenarios distintos.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes utilizan as experiencias completas de subcontratación

As experiencias de factura de fornecedor ofrecen un xeito de verificar e combinar as entradas de tempo, o uso de material e as entradas de gastos que fan referencia a compoñentes subcontratados coas liñas de factura do fornecedor. Este proceso pódese usar para verificar a precisión das liñas de factura do fornecedor. Despois de que se complete o proceso de verificación e se confirme a factura do fornecedor, a aplicación reverterá os datos reais que foron rexistrados polos rexistros de tempo, gastos e uso de material aprobados e creará novos datos reais de custo mediante as liñas de factura do fornecedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes non usan as experiencias de subcontratación completas, pero queren ter unha visión unificada dos custos dos proxectos en Project Operations

Se está a facer un seguimento do proceso de subcontratación nun sistema de terceiros, pode rexistrar os custos dese sistema de terceiros en Project Operations creando facturas do fornecedor que non fagan referencia a subcontratos. Deste xeito, os seus xestores de proxectos poden ter unha visión única e unificada de todos os custos dun proxecto determinado.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Creación de facturas do fornecedor en Project Operations

É posible crear facturas do fornecedor de dúas maneiras:

- Desde a páxina da lista de facturas do fornecedor ou a páxina de detalles dunha única factura do fornecedor
- Desde a páxina da lista de subcontratos ou a páxina de detalles dun único subcontrato

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creación a partir da páxina da lista de facturas do fornecedor ou da páxina de detalles

1. Vaia a **Compras** \> **Facturas do fornecedor**.
2. Na páxina da lista de facturas do fornecedor ou na páxina de detalles dunha única factura do fornecedor, seleccione **Nova** para crear unha nova factura do fornecedor.

As facturas do fornecedor que se crean deste xeito tamén poden facer referencia a un subcontrato.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creación a partir da páxina da lista de subcontratos ou da páxina de detalles

1. Vaia a **Compras** \> **Subcontratos**.
2. Seleccione un ou máis subcontratos.
3. Na páxina da lista de subcontratos ou na páxina de detalles dun único subcontrato, seleccione **Crear factura do fornecedor** para crear unha nova factura do fornecedor.

Unha nova factura de fornecedor en estado **Borrador** créase para cada subcontrato que seleccionou.

As facturas do fornecedor que cree deste xeito sempre fan referencia ao subcontrato na cabeceira da factura do fornecedor. Cada liña do subcontrato que teña un método de facturación de material e tempo fará que se cree unha liña na factura do fornecedor. Cada liña do subcontrato que teña un método de facturación de prezo fixo fará que se cree unha liña na factura do fornecedor para cada fito da liña de subcontrato que teña un estado de **Listo para facturar**.

Os seguintes campos e rexistros relacionados copiaranse do subcontrato á cabeceira da factura do fornecedor:

- Fornecedor.
- As listas de prezos relacionadas copiaranse na factura do fornecedor como listas de prezos.
- Moeda.
- Unidade de contratación.
- Condicións de pagamento.

Para as liñas de subcontratación de tempo e material, os seguintes campos e rexistros relacionados copiaranse da liña de subcontratación á liña de factura do fornecedor:

- Referencias de subcontratación e liñas de subcontratación
- Clase de transacción
- Rol
- Categoría da transacción
- Campos do produto
- Project
- Tarefa
- Recurso reservable

Para as liñas de subcontratación de prezo fixo, os seguintes campos e rexistros relacionados copiaranse da liña de subcontratación e o fito de liña de subcontratación á liña de factura do fornecedor:

- Referencias de subcontratación e liñas de subcontratación.
- Clase de transacción. Por defecto, o valor será **Fito**.
- O nome e o importe do fito copiaranse do fito da liña de subcontratación relacionada.
- O usuario poderá seleccionar un proxecto e unha tarefa na liña de factura do fornecedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
