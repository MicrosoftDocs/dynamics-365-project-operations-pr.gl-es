---
title: Integración de facturas do proxecto
description: Este artigo ofrece información sobre a integración de escrita dual de Project Operations para a facturación do cliente.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029022"
---
# <a name="project-invoice-integration"></a>Integración de facturas do proxecto

Este artigo ofrece información sobre a integración de escrita dual de Project Operations para a facturación do cliente.

En Project Operations, o xestor de proxectos xestiona o traballo pendente de facturación do proxecto e crea unha factura proforma para o cliente en Microsoft Dataverse. Baseándose nesta factura proforma, o empregado de contas pendentes de cobro ou o contable do proxecto crea unha factura orientada ao cliente. A integración de escrita dual garante que os detalles da factura proforma estean sincronizados coas aplicacións de finanzas e operacións. Despois de publicar a factura orientada ao cliente, o sistema actualiza os datos relevantes do proxecto en Dataverse co detalle de contabilidade. O seguinte gráfico ofrece unha visión conceptual de alto nivel desta integración.

   ![Integración de facturas do proxecto.](./media/DW5Invoicing.png)

Despois de que o xefe de proxecto confirme a factura proforma en Dataverse, a información da cabeceira da factura proforma sincronízase coas aplicacións de finanzas e operacións que usan o mapa da táboa de escrita dual, **Proposta de factura do proxecto V2 (facturas)**. Esta é unha integración unidireccional desde Dataverse ás aplicacións de finanzas e operacións. Non se admite a creación ou eliminación de propostas de facturas do proxecto directamente nas aplicacións de finanzas e operacións.

Confirmación da factura en Dataverse tamén activa a lóxica empresarial para crear rexistros relacionados coa facturación na entidade **Datos reais**. Estes rexistros sincronízanse con finanzas e operacións mediante o mapa da táboa de escritura dual, **Datos reais de integración de Project Operations (msdyn\_actuals).** Para obter máis información, consulte [Estimacións e datos reais do proxecto](resource-dual-write-estimates-actuals.md). 

As liñas de proposta de factura do proxecto créanse polo proceso periódico, **Transición de formulario de importación**. Este proceso baséase nos detalles dos datos reais de vendas facturadas na táboa **Transición de datos reais**. Para obter máis información, consulte [Xestionar as propostas de factura do proxecto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
