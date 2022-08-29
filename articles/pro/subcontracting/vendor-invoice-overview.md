---
title: Facturación de fornecedores - Concepto e creación
description: Este artigo describe o concepto de facturas de provedores, escenarios de uso e como crear facturas de provedores en Microsoft Dynamics 365 Project Operations.
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

Facturación de provedores en Microsoft Dynamics 365 Project Operations pódese usar para rexistrar os custos das entregas de servizos e/ou materiais nun proxecto por parte dos provedores.

Cando os servizos e/ou materiais son subcontratados a un provedor, un subcontrato representa o acordo contractual con ese provedor. A medida que o provedor presta os servizos ou os materiais son recibidos e utilizados nas tarefas do proxecto, os custos rexístranse no proxecto. Periódicamente, o provedor envía facturas que se verifican e coinciden cos custos que se rexistran no proxecto. Despois de completar o proceso de verificación, a factura do provedor é confirmada e liberada para o pago.

## <a name="scenarios-for-use"></a>Escenarios de uso

As facturas de provedores en Project Operations pódense usar para soportar dous escenarios distintos.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes utilizan as experiencias completas de subcontratación

As experiencias de facturas de provedores ofrecen un xeito de verificar e combinar as entradas de tempo, o uso de material e as entradas de gastos que fan referencia a compoñentes subcontratados coas liñas de facturas de provedores. Este proceso pódese usar para verificar a precisión das liñas de factura do provedor. Despois de completar o proceso de verificación e confirmar a factura do provedor, a aplicación reverterá os datos reais que foron rexistrados polos rexistros de tempo, gastos e uso de material aprobados e creará novos custos reais mediante as liñas de factura do provedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes non usan as experiencias de subcontratación completas, pero queren ter unha visión unificada dos custos dos proxectos en Operacións de proxectos

Se estás facendo un seguimento do proceso de subcontratación nun sistema de terceiros, podes rexistrar os custos dese sistema de terceiros en Project Operations creando facturas de provedores que non fagan referencia a subcontratos. Deste xeito, os seus xestores de proxectos poden ter unha visión única e unificada de todos os custos dun proxecto determinado.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Creación de facturas de provedores en Project Operations

As facturas de provedores pódense crear de dúas formas:

- Desde a páxina da lista de facturas de provedores ou a páxina de detalles dunha única factura de provedor
- Desde a páxina da lista de subcontratos ou a páxina de detalles dun único subcontrato

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creación a partir da páxina da lista de facturas de provedores ou da páxina de detalles

1. Ir a **Compras** \> **Facturas de provedores**.
2. Na páxina da lista de facturas de provedores ou na páxina de detalles dunha única factura de provedores, seleccione **Novo** para crear unha nova factura de provedor.

As facturas de provedores que se crean deste xeito tamén poden facer referencia a un subcontrato.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creación a partir da páxina da lista de subcontratos ou da páxina de detalles

1. Ir a **Compras** \> **Subcontratas**.
2. Seleccione un ou varios subcontratos.
3. Na páxina da lista de subcontratos ou na páxina de detalles dun único subcontrato, seleccione **Crear factura do provedor** para crear unha nova factura de provedor.

Unha nova factura de provedor en **Borrador** créase o estado para cada subcontrato que seleccionou.

As facturas de provedores que crea deste xeito sempre fan referencia ao subcontrato na cabeceira da factura de provedores. Cada liña do subcontrato que teña un método de facturación de material e tempo fará que se cree unha liña na factura do provedor. Cada liña do subcontrato que teña un método de facturación de prezo fixo fará que se cree unha liña na factura do provedor para cada fito da liña de subcontrato que teña un estado de **Listo para facturar**.

Os seguintes campos e rexistros relacionados copiaranse do subcontrato á cabeceira da factura do provedor:

- Vendedor.
- As listas de prezos relacionadas copiaranse na factura do provedor como listas de prezos.
- Moeda.
- Unidade de contratación.
- Termos de pago.

Para as liñas de subcontratación de tempo e material, os seguintes campos e rexistros relacionados copiaranse da liña de subcontratación á liña de factura do provedor:

- Referencias de liñas de subcontratación e subcontratación
- Clase de transacción
- Rol
- Categoría da transacción
- Campos de produtos
- Project
- Tarefa
- Recurso reservable

Para as liñas de subcontratación de prezo fixo, copiaranse os seguintes campos da liña de subcontrato e da liña de subcontrato á liña de factura do provedor:

- Referencias de liñas de subcontratación e subcontratación.
- Clase de transacción. Por defecto, o valor será **Fito**.
- O nome e o importe do fito copiaranse do fito da liña de subcontratación relacionada.
- O usuario poderá seleccionar un proxecto e tarefa na liña de factura do provedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
