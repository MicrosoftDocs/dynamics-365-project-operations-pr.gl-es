---
title: Cambios de entidade, control e interface de usuario (Project Service Automation 3.x)
description: Este tema describe os cambios de solucións para Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148731"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Cambios de entidade, control e interface de usuario (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Co lanzamento de Microsoft Dynamics Project Service Automation (PSA) 3.x, fixéronse moitos cambios nas entidades, nos controis, nas vistas e na interface de usuario. Neste tema fornécese información acerca destes importantes cambios:

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relacións primarias-secundarias para as entidades de documento de vendas, liña de documento de vendas, detalle de liña de documento de vendas
En versións de Dynamics 365 Project Service Automation (PSA) lanzadas antes da versión 3.0, algunhas das relacións entre as entidades de documentos de vendas, liñas de documento de vendas e detalles de liña de documento de vendas implementáronse a través de campos de cadea que terían unha representación de cadeas de GUID da entidade relacionada. Isto debeuse ás limitacións da plataforma que requirían un código personalizado significativo nos lados do servidor e do cliente da solución para que esas relacións funcionasen de xeito semellante ás típicas relacións de entidades de Dynamics CRM e para facer que os campos de cadea actúen como campos de busca.

PSA 3.0 foi actualizado para aproveitar as novas relacións de entidades entre as entidades de documento de vendas e liña de documento de vendas.

Debido a que os campos de busca agora se poden usar para indicar referencias a entidades, os campos que contiñan o valor da cadea de GUID da entidade relacionada nas versións anteriores xa non son necesarios e polo tanto quedaron desfasados. Tamén quedou desfasado o código personalizado do lado do cliente e do servidor que xestiona as relacións definidas polos campos de cadea herdados.

### <a name="entity-schema-changes"></a>Cambios do esquema da entidade
A seguinte táboa ofrece unha lista de un a un dos campos de cadea desfasados e os novos campos de busca para as entidades. 

 Entidade |   Campo desfasado (cadea) | Novo campo (busca)
--- | --- | ---
invoicedetail (liña de factura) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (dato real) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (programa de facturas de liña de contrato de proxecto) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (fito de liña de contrato de proxecto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (feito) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (detalle de liña de factura) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (liña de diario) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (categoría de recurso de liña de contrato de proxecto) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (detalle de liña de contrato de proxecto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (categoría de transacción de liña de contrato de proxecto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (clasificación de transacción de liña de contrato de proxecto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (programa de facturas de liña de oferta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (categoría de recurso de liña de oferta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (fito de liña de oferta) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (detalle de liña de oferta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (categoría de transacción de liña de oferta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (clasificación de transacción de liña de oferta) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (liña de pedido) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Vistas e controis personalizados desfasados
As seguintes vistas e controis personalizados e os seus artefactos relacionados quedaron desfasados.

- Vista de imputabilidade.
- Controis de grade personalizados para amosar detalles de liña de oferta na páxina **Información do proxecto** da liña de oferta.
- Controis de grade personalizados para amosar detalles de liña de contrato de proxecto na páxina **Información do proxecto** da liña de pedido de vendas.

> [!NOTE]
> Para ver a lista completa de recursos desfasados, consulte [Recursos web desfasados en Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Módulo de aplicación de interface de cliente unificada
Coa introdución dos módulos de aplicación de interface de cliente unificada (UCI), as entradas do mapa do sitio de PSA elimináronse do sistema.  
A funcionalidade relacionada co cambio de formulario para Oportunidade, Oferta, Pedido, Factura quedou desfasada xa que non é necesaria porque o módulo de aplicación UCI inclúe só versións PSA dos formularios.  

Os seguintes recursos web quedaron desfasados:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Para ver a lista completa de recursos desfasados, consulte [Recursos web desfasados en Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


