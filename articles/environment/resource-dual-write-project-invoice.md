---
title: Integración de facturas do proxecto
description: Este tema ofrece información sobre a integración de escrita dual de Project Operations para a facturación do cliente.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993239"
---
# <a name="project-invoice-integration"></a>Integración de facturas do proxecto

Este tema ofrece información sobre a integración de escrita dual de Project Operations para a facturación do cliente.

En Project Operations, o xestor de proxectos xestiona o traballo pendente de facturación do proxecto e crea unha factura proforma para o cliente en Microsoft Dataverse. Baseándose nesta factura proforma, o empregado de contas pendentes de cobro ou o contable do proxecto crea unha factura orientada ao cliente. A integración de escrita dual garante que os detalles da factura proforma estean sincronizados coas aplicacións de Finance and Operations. Despois de publicar a factura orientada ao cliente, o sistema actualiza os datos relevantes do proxecto en Dataverse co detalle de contabilidade. O seguinte gráfico ofrece unha visión conceptual de alto nivel desta integración.

   ![Integración de facturas do proxecto.](./media/DW5Invoicing.png)

Despois de que o xefe de proxecto confirme a factura proforma en Dataverse, a información da cabeceira da factura proforma sincronízase coas aplicacións de Finance and Operations que usan o mapa da táboa de escrita dual, **Proposta de factura do proxecto V2 (facturas)**. Esta é unha integración unidireccional desde Dataverse ás aplicacións de Finance and Operations. Non se admite a creación ou eliminación de propostas de facturas do proxecto directamente nas aplicacións de Finance and Operations.

Confirmación da factura en Dataverse tamén activa a lóxica empresarial para crear rexistros relacionados coa facturación na entidade **Datos reais**. Estes rexistros sincronízanse con Finance and Operations mediante o mapa da táboa de escritura dual, **Datos reais de integración de Project Operations (msdyn\_actuals).** Para obter máis información, consulte [Estimacións e datos reais do proxecto](resource-dual-write-estimates-actuals.md). 

As liñas de proposta de factura do proxecto créanse polo proceso periódico, **Transición de formulario de importación**. Este proceso baséase nos detalles dos datos reais de vendas facturadas na táboa **Transición de datos reais**. Para obter máis información, consulte [Xestionar as propostas de factura do proxecto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
