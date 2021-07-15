---
title: Visión xeral do proceso de facturación
description: Este tema ofrece unha visión xeral do proceso de facturación en Project Operations para escenarios baseados en recursos/sen fornecemento.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369014"
---
# <a name="invoicing-process-overview"></a>Visión xeral do proceso de facturación

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Project Operations para escenarios baseados en recursos/sen fornecemento ofrecen capacidades completas adaptadas ás necesidades do xestor de proxectos e do empregado de contas por cobrar/contable do proxecto. Para o proceso de facturación, o xestor do proxecto xestiona os traballos pendentes de facturación do proxecto e o empregado/contable do proxecto crea un documento preciso de factura orientada ao cliente.

![Diagrama do fluxo de facturación](./media/invoicing-flow.png)

A liña de contrato do proxecto define o método de facturación das transaccións do proxecto asociado. Cando o xestor de proxectos aproba transaccións de tempo e gastos, o sistema rexistra as transaccións na entidade **Datos reais do proxecto** e envía a información ao módulo **Xestión de proxectos e contabilidade** en Dynamics 365 Finance. A continuación, o contable do proxecto revisa e publica os rexistros usando o [Diario de Project Operations Integration](../project-accounting/project-operations-integration-journal.md). Este diario inclúe importantes datos contables para datos reais do proxecto, como facturación, grupo de impostos sobre vendas, grupo de impostos sobre vendas individuais de facturación e dimensións financeiras.

O xestor de proxectos pode revisar as transaccións de vendas sen facturar empregando o método de facturación de tempo e material en [Traballos pendentes de facturación de tempo e material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) e a facturación a prezo fixo en [Fitos de prezo fixo](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Estas vistas permítenlle filtrar e seleccionar as transaccións que cómpre incluír no seguinte ciclo de facturación e logo marcalas como **Listo para facturar**.

Pode [crear manualmente unha factura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) ou usar un [proceso periódico](../proforma-invoicing/configure-automated-invoice-creation.md). O xestor de proxecto pode [axustar un borrador de factura proforma](../proforma-invoicing/manage-proforma-invoice.md) segundo sexa necesario e logo confirmalo.

A factura proforma confirmada envíase ao módulo **Xestión de proxectos e contabilidade** en Finance. O contable do proxecto dá formato e actualiza a proposta de factura do proxecto e, a seguir, publica e imprime o documento. As facturas do proxecto publicadas rexístranse no libro maior, así como nas contas do cliente e do proxecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]