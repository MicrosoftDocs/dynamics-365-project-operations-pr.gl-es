---
title: Integración de facturas do proxecto
description: Este tema ofrece información sobre a integración de escrita dual de Project Operations para a facturación do cliente.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581236"
---
# <a name="project-invoice-integration"></a>Integración de facturas do proxecto

Este tema ofrece información sobre a integración de escrita dual de Project Operations para a facturación do cliente.

En Project Operations, o xestor de proxectos xestiona o traballo pendente de facturación do proxecto e crea unha factura proforma para o cliente en Microsoft Dataverse. Baseándose nesta factura proforma, o empregado de contas pendentes de cobro ou o contable do proxecto crea unha factura orientada ao cliente. A integración de dobre escritura garante que os detalles da factura proforma se sincronicen coas aplicacións de Finanzas e Operacións. Despois de publicar a factura orientada ao cliente, o sistema actualiza os datos relevantes do proxecto en Dataverse co detalle de contabilidade. O seguinte gráfico ofrece unha visión conceptual de alto nivel desta integración.

   ![Integración de facturas do proxecto.](./media/DW5Invoicing.png)

Despois de que o director do proxecto confirme a factura proforma Dataverse, a información do encabezado da factura proforma sincronízase coas aplicacións de Finanzas e Operacións mediante o mapa de táboa de escritura dual, **Proposta de factura do proxecto V2 (facturas)**. Esta é unha integración unidireccional desde Dataverse ás aplicacións de Finanzas e Operacións. Non se admite a creación ou eliminación de propostas de factura de proxecto directamente nas aplicacións de Finanzas e Operacións.

Confirmación da factura en Dataverse tamén activa a lóxica empresarial para crear rexistros relacionados coa facturación na entidade **Datos reais**. Estes rexistros están sincronizados con Finanzas e Operacións mediante o mapa de táboa de escritura dual.**Reais de integración de operacións do proxecto (msdyn\_ reais).** Para obter máis información, consulte [Estimacións e datos reais do proxecto](resource-dual-write-estimates-actuals.md). 

As liñas de proposta de factura do proxecto créanse polo proceso periódico, **Transición de formulario de importación**. Este proceso baséase nos detalles dos datos reais de vendas facturadas na táboa **Transición de datos reais**. Para obter máis información, consulte [Xestionar as propostas de factura do proxecto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
