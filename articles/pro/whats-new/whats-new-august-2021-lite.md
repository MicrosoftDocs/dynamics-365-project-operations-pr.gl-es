---
title: 'Novidades de agosto de 2021: despregamento de Project Operations lite'
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de agosto de 2021 da implantación de Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 84318a26d97355fe56794e1d1532576cde4af661
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922036"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Novidades de agosto de 2021: despregamento de Project Operations lite

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este artigo aplícase ao seguinte Dynamics 365 Project Operations compoñentes e versións:

  - Project Operations en ambiente de Dataverse versión 4.13.0.152

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- **Conxuntos de aprobacións**: A aprobación reúne as solicitudes de aprobación do tempo, gastos ou uso de material do grupo en subconxuntos de operacións máis pequenos. Esta agrupación permite procesar as aprobacións por proxecto, nunha orde específica por proxecto e permite reintentar e secuenciar. Agrupar as solicitudes mellora a fiabilidade e rastrexabilidade do procesamento de aprobacións para grandes volumes de aprobacións. Para obter máis información, consulte [Conxuntos de aprobacións](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Facturación e prezos | 2295625 | O nome do fito debe copiarse da programación da factura ao detalle da liña de factura. |
| Facturación e prezos | 2316323 | O desconto non debe ser editable nunha factura proforma en Project Operations para escenarios baseados en recursos. |
|   Xestión de oportunidades | 2338619 | As regras de negocio **Oportunidade** e **Oferta** deben invocarse só nas páxinas. |
| Xestión de recursos | 2316523 | Ao usar **Enviar solicitude** dun requisito de recurso que ten un rol asociado non debería mostrarse un erro. |
| Xestión de recursos | 2326885 | A creación dun requisito de recursos a través dun proxecto non debería mostrar un erro. |
| Tempo e gasto | 2335584 | Fluxos de tarefas obsoletos na entrada de tempo. |
| Tempo e gasto | 2336884 | O botón de entrada de tempo **Copiar semana** debe funcionar para máis que o usuario actual. |
