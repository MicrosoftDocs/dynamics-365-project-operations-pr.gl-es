---
title: Visión xeral da facturación entre empresas
description: Este tema ofrece información e exemplos sobre a facturación entre empresas para proxectos.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287326"
---
# <a name="intercompany-invoicing-overview"></a>Visión xeral da facturación entre empresas

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

A súa organización pode ter varias divisións, filiais e outras persoas xurídicas que se transfiren produtos e servizos entre si para proxectos. A entidade legal que presta o servizo ou fornece o produto chámase *entidade legal prestamista*. A entidade legal que recibe o servizo ou produto chámase *entidade legal prestameira*.

A seguinte ilustración mostra un escenario típico no que dúas entidades legais, Contoso Robotics USA (a entidade legal en prestameira) e Contoso Robotics UK (a entidade legal prestamista), comparten recursos para entregar un proxecto ao cliente, Adventure Works. Para este escenario, Contoso Robotics USA está contratada para entregar o traballo a Adventure Works.

![Facturación entre empresas](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations usa o seguinte fluxo para procesar transaccións entre empresas:

1. Os recursos da entidade legal prestameira rexistran as transaccións de tempo ou gasto entre empresas reservando o tempo e os gastos contra proxectos da entidade legal prestameira.
2. Os custos de tempo e gasto rexístranse na empresa prestameira empregando a lista de prezos de custo unitarios da empresa prestameira.
3. As transaccións de vendas sen facturar entre empresas rexístranse na empresa prestameira empregando a lista de prezos de custo unitarios da empresa prestameira.
4. Os ingresos non facturados rexístranse na empresa prestameira mediante a lista de prezos de venda do contrato do proxecto. Pódese facturar ao cliente cando se rexistran ingresos non facturados. O cliente non ten que esperar a que remate o procesamento de facturas entre empresas.
5. As facturas de clientes entre empresas créanse periodicamente na empresa prestamista. As facturas créanse manualmente ou mediante un proceso automatizado periódico. Pódese crear unha única factura por cada entidade xurídica prestameira ou pódense crear facturas separadas por proxecto.
6. Cando a factura de cliente entre empresas se contabiliza na entidade legal prestamista, a factura de fornecedor pendente correspondente créase na entidade legal prestameira. Os custos da factura do fornecedor pendente rexistraranse no subprograma do proxecto cando se contabilice a factura.

O seguinte diagrama ilustra a facturación entre empresas relacionada con eventos de contabilidade e anotacións esperadas no libro maior xeral.

![Fluxo entre empresas](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Recursos adicionais

- [Configurar a facturación entre empresas](configure-intercompany-invoicing.md)
- [Rexistrar transaccións entre empresas](create-intercompany-transactions.md)
- [Crear facturas entre empresas de clientes e fornecedores](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]