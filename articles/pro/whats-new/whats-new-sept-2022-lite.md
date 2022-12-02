---
title: Novidades de setembro de 2022 - Despregamento de Project Operations lite
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de setembro de 2022 do despregamento lite de Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634850"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novidades de setembro de 2022 - Despregamento de Project Operations lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.46.0.60

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

| Área de funcionalidades | Nome da funcionalidade | Máis información |
| --- | --- | --- |
| Xestión de oportunidades | **Revisión de activación de ofertas**<br>Project Operations ofrece o soporte total do proceso de vendas. As ofertas do proxecto pódense activar para representar un estado no que a oferta é só de lectura e está a ser revisada. As ofertas activadas pódense revisar para crear novas ofertas que teñan un número de revisión incrementado. As ofertas de proxecto activadas ou as revisións de ofertas pódense pechar como gañadas ou perdidas. | [Activar e revisar unha oferta de proxecto](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturación e prezos | **Prezo predefinido independente da zona horaria**<br>Project Operations introduciu o concepto de data independente da zona horaria en todos os datos reais do proxecto. Un campo novo, **Data da transacción**, agora está dispoñible nas liñas e datos reais do diario, e utilizarase para almacenar a data na que se produciu a transacción, pero sen converter esa data en horario universal coordinado. Esta data utilizarase para procesos posteriores, como o incumprimento de prezos e a creación de facturas. | <p>[Determinar taxas de custo para estimacións e datos reais baseados en proxecto](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinar prezos de vendas para estimacións e datos reais baseados en proxectos](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturación e prezos | **Anulacións de prezos con datas efectivas en Project Operations**<br>Anulacións de prezos con datas efectivas proporciona unha forma de anular ou cambiar prezos específicos na lista de prezos. | [Anulacións de prezos con datas efectivas](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tempo e gasto | **Responsable de aprobacións global**<br>Esta función permite o fornecedor de software independente (ISV) e a aprobación centralizada, independentemente do estado do proxecto ou do membro do equipo no proxecto. | [Seguridade e aprobacións](/dynamics365/project-operations/approvals/approvals-security) |
|Planificación e rastrexo de proxectos|**Use as API de programación de proxectos para realizar operacións con entidades de programación** </br> </br>A API de edición de contornos de asignación de recursos permite aos programadores especificar mediante programación o esforzo dunha atribución de tarefas en calquera intervalo de datas compatible para unha planificación do esforzo por fases máis detallada.|[Use as API de programación de proxectos para realizar operacións con entidades de programación](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2754422 | As estimacións de materiais e gastos non se transmiten a Dynamics 365 Finance cando se copian os proxectos en Dataverse. |
| Tempo e gasto | 2787409 | Un responsable de aprobacións non válido pode aprobar unha entrada de tempo non do proxecto. |
| Xestión de oportunidades | 2788907 | Actualizouse a mensaxe de erro na validación da unicidade para as liñas de pedido que inclúen marcas. |
| Tempo e gasto | 2842253 | Xestión de excepcións nulas para a aprobación do tempo. |
| Facturación e prezos | 2844181 | O fallo ao obter o ID de correlación bloquea a creación da factura. |
| Facturación e prezos | 2876628 | QLD, CLD - A resolución da lista de prezos estimada debe utilizar os campos de rango de datas herdados da lista de prezos. |
| Subcontratación | 2893222 | Se non se especifica ningunha función para unha liña de subcontrato, debería ser posible seleccionar esa liña nun membro do equipo para calquera rol. |
