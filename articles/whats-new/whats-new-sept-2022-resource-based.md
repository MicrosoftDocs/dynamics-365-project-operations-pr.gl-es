---
title: Novidades de setembro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de setembro de 2022 de Microsoft Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634803"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de setembro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.46.0.60
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.29

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

| Área de funcionalidades | Nome da funcionalidade | Máis información |
| --- | --- | --- |
| Xestión de oportunidades | **Revisión de activación de ofertas**<br>Project Operations ofrece o soporte total do proceso de vendas. As ofertas do proxecto pódense activar para representar un estado no que a oferta é só de lectura e está a ser revisada. As ofertas activadas pódense revisar para crear novas ofertas que teñan un número de revisión incrementado. As ofertas de proxecto activadas ou as revisións de ofertas pódense pechar como gañadas ou perdidas. | [Activar e revisar unha oferta de proxecto](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturación e prezos | **Prezo predefinido independente da zona horaria**<br>Project Operations introduciu o concepto de data independente da zona horaria en todos os datos reais do proxecto. Un campo novo, **Data da transacción**, agora está dispoñible nas liñas e datos reais do diario, e utilizarase para almacenar a data na que se produciu a transacción, pero sen converter esa data en horario universal coordinado. Esta data utilizarase para procesos posteriores, como o incumprimento de prezos e a creación de facturas. | <p>[Determinar taxas de custo para estimacións e datos reais baseados en proxecto](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinar prezos de vendas para estimacións e datos reais baseados en proxectos](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturación e prezos | **Anulacións de prezos con datas efectivas en Project Operations**<br>Anulacións de prezos con datas efectivas proporciona unha forma de anular ou cambiar prezos específicos na lista de prezos. | [Anulacións de prezos con datas efectivas](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontratación | **Subcontratación e conciliación de facturas de fornecedores**<br>Esta funcionalidade permite aos clientes crear subcontratos para adquirir tempo de recursos, categorías de gastos e materiais que se usan para o traballo do proxecto. Tamén permite aos clientes rexistrar, nas aplicacións de finanzas e operacións, facturas de fornecedores que estarán dispoñibles para os xestores de proxectos en Dataverse para verificación. | <p>[Xestión de subcontratos](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Crear facturas de fornecedor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tempo e gasto | **Responsable de aprobacións global**<br>Esta funcionalidade permite o fornecedor de software independente (ISV) e a aprobación centralizada, independentemente do estado do proxecto ou do membro do equipo no proxecto. | [Seguridade e aprobacións](/dynamics365/project-operations/approvals/approvals-security) |
| Xestión de gastos | **Capacidade de contabilizar a responsabilidade de gastos na moeda do fornecedor**<br>Esta funcionalidade permite contabilizar os informes de gastos nunha moeda de fornecedor para o método de pagamento en efectivo. | [Capacidade de contabilizar a responsabilidade de gastos na moeda do fornecedor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Adquisicións do proxecto | **Pagar ao recibir os pagamentos dos fornecedores**<br>Esta funcionalidade permite usar a funcionalidade Pagar ao recibir o pagamento (PWP) con ambientes sen fornecemento de Project Operations. Permite bloquear/reter os pagos do fornecedor, en función das condicións de retención, ata que se reciba o pagamento do cliente. | [Pagar ao recibir os pagamentos dos fornecedores](/dynamics365/project-operations/procurement/pay-when-paid) |
| Adquisicións do proxecto | **Solicitudes de compra do proxecto**<br>Esta funcionalidade permite aos usuarios crear pedidos de compra relacionados con proxectos en persoas xurídicas cando está activada a integración de Project Operations on Dynamics 365 Customer Engagement. Os pedidos de compra do proxecto pódense utilizar para rexistrar a adquisición de material sen fornecemento contra o proxecto pola persoa do departamento de Adquisicións. Os pedidos de compra do proxecto non se sincronizarán con Dataverse. Non obstante, pode usar unha entidade virtual para mostrar as liñas de pedido de compra do proxecto en Dataverse para información do xestor de proxectos. O custo da factura do fornecedor relacionado co proxecto está integrado coa entidade Datos reais do proxecto en Dataverse. O custo do proxecto rexístrase no libro auxiliar do proxecto utilizando el diario de integración de Project Operations. | |
|Planificación e rastrexo de proxectos|**Use as API de programación de proxectos para realizar operacións con entidades de programación** </br> </br>A API de edición de contornos de asignación de recursos permite aos programadores especificar mediante programación o esforzo dunha atribución de tarefas en calquera intervalo de datas compatible para unha planificación do esforzo por fases máis detallada.|[Use as API de programación de proxectos para realizar operacións con entidades de programación](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte táboa mostra os mapas de escrita dual que foron modificados ou engadidos na versión de Project Operations de setembro de 2022.

| Asignación de entidades | Versión actualizada | Comentarios |
| -------------- | ------------------- | ------------|
| Datos reais de integración de Project Operations (msdyn_actuals) | 1.0.0.15 | Este mapa admite o procesamento de datos reais de subcontratos con Project Operations para escenarios baseados en recursos. |
| Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Este mapa admite o procesamento de datos reais de subcontratos con Project Operations para escenarios baseados en recursos. |
| Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Este mapa admite o procesamento de datos reais de subcontratos con Project Operations para escenarios baseados en recursos. |

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2754422 | As estimacións de materiais e gastos non se transmiten en Finance cando se copian os proxectos en Dataverse. |
| Tempo e gasto | 2787409 | Un responsable de aprobacións non válido pode aprobar unha entrada de tempo non do proxecto. |
| Xestión de oportunidades | 2788907 | Actualizouse a mensaxe de erro na validación da unicidade para as liñas de pedido que inclúen marcas. |
| Tempo e gasto | 2842253 | Xestión de excepcións nulas para a aprobación do tempo. |
| Facturación e prezos | 2844181 | O fallo ao obter o ID de correlación bloquea a creación da factura. |
| Facturación e prezos | 2876628 | QLD, CLD - A resolución da lista de prezos estimada debe utilizar os campos de rango de datas herdados da lista de prezos. |
| Subcontratación | 2893222 | Se non se especifica ningunha función para unha liña de subcontrato, debería ser posible seleccionar esa liña nun membro do equipo para calquera rol. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión e contabilidade de proxectos en Finance

Para obter información sobre as correccións incluídas nesta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) e vexa o [artigo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>As funcionalidades están activadas de forma predefinida na próxima versión

A seguinte táboa indica as funcións que están activadas por defecto na versión 10.0.30. A maioría das funcións que se activaron automaticamente pódense desactivar en [Xestión de funcionalidades](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, algunhas funcións que se activaron automaticamente poden eliminarse da xestión de funcionalidades e converterse en obrigatorias. Este cambio garante que os clientes estean a utilizar a funcionalidade actual, de xeito que as melloras poden incorporarse á funcionalidade actual a medida que se engaden. As funcionalidades nunca se activarán automaticamente en menos dun ano, a non ser que se determine que son esenciais.

| Nome da funcionalidade | Activar data | Funcionalidade engadida | Estado da funcionalidade | Módulo |
| --- | --- | --- |--- |--- |
| Activar a operación asíncrona cando o usuario necesite cambiar entre as operacións de sincronización e asíncrona | 21 de outubro de 2022 | 9 de abril de 2021 | Activado por defecto | Xestión de gastos |
| Avaliación da política de gastos para os recibos necesarios | 21 de outubro de 2022 | 20 de decembro de 2021 | Activado por defecto | Xestión de gastos |
| Vista de lista dos informes de gastos creados polos traballadores delegados | 21 de outubro de 2022 | 19 de febreiro de 2020 | Activado por defecto | Xestión de gastos |
| Totais de quilometraxe por ano fiscal | 21 de outubro de 2022 | 10 de maio de 2022 | Activado por defecto | Xestión de gastos |
