---
title: Novidades de setembro de 2022 - Despregamento de Project Operations lite
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de setembro de 2022 de Microsoft Dynamics 365 Project Operations despregamento lite.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621324"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novidades de setembro de 2022 - Despregamento de Project Operations lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.46.0.60

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

| Área de funcionalidades | Nome da característica | Máis información |
| --- | --- | --- |
| Xestión de oportunidades | **Revisión e Activación de Presupostos**<br>Project Operations ofrece o soporte total do proceso de vendas. As citas do proxecto pódense activar para representar un estado no que a cita é só de lectura e está a ser revisada. As comiñas activadas pódense revisar para crear novas comiñas que teñan un número de revisión incrementado. As citas de proxectos activadas ou as revisións de presupostos pódense pechar como gañadas ou perdidas. | [Activar e revisar unha oferta de proxecto](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturación e prezos | **Prezo predeterminado independente da zona horaria**<br>Project Operations introduciu o concepto de data independente da zona horaria en todos os datos reais do proxecto. Un novo campo, **Data da transacción**, agora está dispoñible nas liñas e reais do diario, e utilizarase para almacenar a data na que se produciu a transacción, pero sen converter esa data en Tempo Universal Coordinado. Esta data utilizarase para procesos posteriores, como o incumprimento de prezos e a creación de facturas. | <p>[Determinar as taxas de custo para as estimacións e os reais baseados en proxectos](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determine os prezos de venda para estimacións e reais baseadas en proxectos](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturación e prezos | **Anulacións de prezos en vigor na data nas operacións do proxecto**<br>As anulacións de prezos efectivas na data ofrecen unha forma de anular ou cambiar prezos específicos na lista de prezos. | [Anulacións de prezos en vigor na data](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tempo e gasto | **Aprobador global**<br>Esta función permite o provedor de software independente (ISV) e a aprobación centralizada, independentemente do estado do proxecto ou do membro do equipo no proxecto. | [Seguridade e aprobacións](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2754422 | As estimacións de materiais e gastos non se transmiten a Dynamics 365 Finance cando se copian os proxectos en Dataverse. |
| Tempo e gasto | 2787409 | Un aprobador non válido pode aprobar unha entrada de tempo non do proxecto. |
| Xestión de oportunidades | 2788907 | Actualizouse a mensaxe de erro na validación da unicidade para as liñas de pedido que inclúen marcas. |
| Tempo e gasto | 2842253 | Xestión de excepcións nulas para a aprobación do tempo. |
| Facturación e prezos | 2844181 | O fallo ao obter o ID de correlación bloquea a creación da factura. |
| Facturación e prezos | 2876628 | QLD, CLD: a resolución estimativa da lista de prezos debe utilizar os campos de intervalo de datas heredados da lista de prezos. |
| Subcontratación | 2893222 | Se non se especifica ningunha función para unha liña de subcontrato, debería ser posible seleccionar esa liña nun membro do equipo para calquera rol. |
