---
title: Sincronice as tarefas do proxecto directamente desde Project Service Automation ata Finanzas e Operacións
description: Este tema describe o modelo e a tarefa subxacente que se usan para sincronizar directamente as tarefas do proxecto Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 666e0d757969b32f16e08128d9f78a2ffe1e8357
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683308"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronice as tarefas do proxecto directamente desde Project Service Automation ata Finanzas e Operacións

[!include[banner](../includes/banner.md)]

Este tema describe o modelo e a tarefa subxacente que se usan para sincronizar directamente as tarefas do proxecto Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE]
> - A integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades están dispoñibles na versión 8.0.
> - Se está a usar Enterprise edition 7.3.0, despois de instalar KB 4132657 e KB 4132660, poderá usar os modelos para integrar tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e datos reais e para configurar o bloqueo de funcionalidade. Se debe restablecer as distribucións contables, recomendámoslle que instale tamén KB 4131710.
> - A integración dos datos reais está dispoñible a partir da versión 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de datos de Project Service Automation a Finanzas

A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas. O modelo de integración dispoñible coa funcionalidade de integración de datos permite o fluxo de datos sobre as tarefas do proxecto de Project Service Automation a Finanzas.

A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.

[![Fluxo de datos para a integración de Project Service Automation con Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Modelo e tarefa

Para acceder ao modelo, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.

O seguinte modelo e a tarefa subxacente úsanse para sincronizar as tarefas do proxecto de Project Service Automation a Finanzas:

- **Nome do modelo en integración de datos:** Tarefas do proxecto (PSA a Fin e Ops)
- **Nome da tarefa do proxecto:** Tarefas do proxecto

Antes de que poida producirse a sincronización de tarefas de proxectos e proxectos, debe sincronizar os contratos do proxecto e os proxectos.

## <a name="entity-set"></a>Conxunto de entidades

| Project Service Automation | Finanzas                             |
|----------------------------|-------------------------------------|
| Tarefas do proxecto              | Entidade de integración para a tarefa do proxecto |

## <a name="entity-flow"></a>Fluxo de entidades

As tarefas do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como tarefas de proxecto.

## <a name="prerequisites-and-mapping-setup"></a>Requisitos previos e configuración de asignación

Antes de que poida producirse a sincronización de tarefas de proxectos e proxectos, debe sincronizar os contratos do proxecto e os proxectos.

## <a name="power-query"></a>Power Query

Debes usar Microsoft Power Query para que Excel filtre os datos se se cumpre esta condición:

- Ten rexistros específicos de recursos nunha tarefa do proxecto.

Se debes usar Power Query, siga esta pauta:

- O modelo de tarefas do proxecto (PSA a Fin e Ops) ten un filtro predefinido que exclúe os rexistros específicos do recurso dunha tarefa do proxecto configurando o filtro en **IsLineTask** a **False**. Se crea o seu propio modelo, debe engadir este filtro.

## <a name="template-mapping-in-data-integration"></a>Asignación de modelos na integración de datos

A seguinte ilustración mostra un exemplo das asignacións de tarefas do modelo en integración de datos. A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.

[![Asignación de modelos.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]