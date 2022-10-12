---
title: Novidades de setembro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de setembro de 2022 de Microsoft Dynamics 365 Project Operations para escenarios baseados en recursos/non abastecidos.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621321"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de setembro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.46.0.60
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.29

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

| Área de funcionalidades | Nome da característica | Máis información |
| --- | --- | --- |
| Xestión de oportunidades | **Revisión e Activación de Presupostos**<br>Project Operations ofrece o soporte total do proceso de vendas. As citas do proxecto pódense activar para representar un estado no que a cita é só de lectura e está a ser revisada. As comiñas activadas pódense revisar para crear novas comiñas que teñan un número de revisión incrementado. As citas de proxectos activadas ou as revisións de presupostos pódense pechar como gañadas ou perdidas. | [Activar e revisar unha oferta de proxecto](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturación e prezos | **Prezo predeterminado independente da zona horaria**<br>Project Operations introduciu o concepto de data independente da zona horaria en todos os datos reais do proxecto. Un novo campo, **Data da transacción**, agora está dispoñible nas liñas e reais do diario, e utilizarase para almacenar a data na que se produciu a transacción, pero sen converter esa data en Tempo Universal Coordinado. Esta data utilizarase para procesos posteriores, como o incumprimento de prezos e a creación de facturas. | <p>[Determinar as taxas de custo para as estimacións e os reais baseados en proxectos](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determine os prezos de venda para estimacións e reais baseadas en proxectos](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturación e prezos | **Anulacións de prezos en vigor na data nas operacións do proxecto**<br>As anulacións de prezos efectivas na data ofrecen unha forma de anular ou cambiar prezos específicos na lista de prezos. | [Anulacións de prezos en vigor na data](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontratación | **Subcontratación e conciliación de facturas de provedores**<br>Esta función permite aos clientes crear subcontratos para comprar tempo de recursos, categorías de gastos e materiais que se usan para o traballo do proxecto. Tamén permite aos clientes rexistrar, nas aplicacións de finanzas e operacións, facturas de provedores que estarán dispoñibles para os xestores de proxectos en Dataverse para verificación. | <p>[Xestión de subcontratación](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Crear facturas de fornecedor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tempo e gasto | **Aprobador global**<br>Esta función permite o provedor de software independente (ISV) e a aprobación centralizada, independentemente do estado do proxecto ou do membro do equipo no proxecto. | [Seguridade e aprobacións](/dynamics365/project-operations/approvals/approvals-security) |
| Xestión de gastos | **Capacidade de contabilizar a responsabilidade de gastos na moeda do provedor**<br>Esta función permite que os informes de gastos se publiquen nunha moeda do provedor para o método de pago en efectivo. | [Capacidade de contabilizar a responsabilidade de gastos na moeda do provedor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Contratación de proxectos | **Paga cando se pagan os pagos do provedor**<br>Esta función permite que a función Pagar cando se pague (PWP) se utilice con ambientes sen existencias de Project Operations. Permite bloquear/reter os pagos do provedor, en función dos termos de retención, ata que se reciba o pago do cliente. | [Paga cando se pagan os pagos do provedor](/dynamics365/project-operations/procurement/pay-when-paid) |
| Contratación de proxectos | **Solicitudes de compra de proxectos**<br>Esta función permite aos usuarios crear pedidos de compra relacionados con proxectos en persoas xurídicas nas que estea activada a integración de Operacións de proxectos na integración Dynamics 365 Customer Engagement. As ordes de compra do proxecto pódense utilizar para rexistrar a adquisición de material non abastecido contra o proxecto pola persoa do departamento de Adquisicións. Non se sincronizarán as ordes de compra do proxecto Dataverse. Non obstante, podes usar unha entidade virtual para mostrar as liñas de pedido de compra do proxecto Dataverse para obter información do xestor de proxectos. O custo da factura do provedor relacionado co proxecto está integrado coa entidade Reais do proxecto en Dataverse. O custo do proxecto rexístrase no sublibro do proxecto mediante o diario de integración de operacións do proxecto. | |

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte táboa mostra os mapas de dobre escritura que se modificaron ou engadiron na versión de setembro de 2022 de Project Operations.

| Asignación de entidades | Versión actualizada | Comentarios |
| -------------- | ------------------- | ------------|
| Datos reais de integración de Project Operations (msdyn_actuals) | 1.0.0.15 | Este mapa admite o procesamento de subcontratos reais con Project Operations para escenarios baseados en recursos. |
| Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Este mapa admite o procesamento de subcontratos reais con Project Operations para escenarios baseados en recursos. |
| Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Este mapa admite o procesamento de subcontratos reais con Project Operations para escenarios baseados en recursos. |

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, sigue as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2754422 | As estimacións de materiais e gastos non chegan a Finanzas cando se copian os proxectos Dataverse. |
| Tempo e gasto | 2787409 | Un aprobador non válido pode aprobar unha entrada de tempo non do proxecto. |
| Xestión de oportunidades | 2788907 | Actualizouse a mensaxe de erro na validación da unicidade para as liñas de pedido que inclúen marcas. |
| Tempo e gasto | 2842253 | Xestión de excepcións nulas para a aprobación do tempo. |
| Facturación e prezos | 2844181 | O fallo ao obter o ID de correlación bloquea a creación da factura. |
| Facturación e prezos | 2876628 | QLD, CLD: a resolución estimativa da lista de prezos debe utilizar os campos de intervalo de datas heredados da lista de prezos. |
| Subcontratación | 2893222 | Se non se especifica ningunha función para unha liña de subcontrato, debería ser posible seleccionar esa liña nun membro do equipo para calquera rol. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión de proxectos e contabilidade en Finanzas

Para obter información sobre as correccións de erros que se inclúen nesta actualización, inicie sesión en Microsoft Dynamics Servizos de ciclo de vida e consulta [Artigo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>As funcións están activadas de forma predeterminada na próxima versión

A seguinte táboa enumera as funcións que están activadas por defecto na versión 10.0.30. A maioría das funcións que se activaron automaticamente pódense desactivar en [Xestión de características](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, algunhas funcións que se activaron automaticamente poden eliminarse da xestión de funcións e converterse en obrigatorias. Este cambio garante que os clientes estean a utilizar a funcionalidade actual, de xeito que as melloras poden incorporarse á funcionalidade actual a medida que se engaden. As funcións nunca se activarán automaticamente en menos dun ano, a non ser que se determine que son esenciais.

| Nome da característica | Activar data | Función engadida | Estado da funcionalidade | Módulo |
| --- | --- | --- |--- |--- |
| Activa a operación asíncrona cando o usuario necesite cambiar entre as operacións de sincronización e asíncrona | 21 de outubro de 2022 | 9 de abril de 2021 | Activado por defecto | Xestión de gastos |
| Avaliación da política de gastos para os recibos necesarios | 21 de outubro de 2022 | 20 de decembro de 2021 | Activado por defecto | Xestión de gastos |
| Vista de lista dos informes de gastos creados polos traballadores delegados | 21 de outubro de 2022 | 19 de febreiro de 2020 | Activado por defecto | Xestión de gastos |
| Cálculo dos totais de quilometraxe por ano fiscal | 21 de outubro de 2022 | 10 de maio de 2022 | Activado por defecto | Xestión de gastos |
