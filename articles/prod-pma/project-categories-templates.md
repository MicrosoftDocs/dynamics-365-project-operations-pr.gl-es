---
title: Sincronizar as categorías de gastos do proxecto entre Finance and Operations e Project Service Automation
description: Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as categorías de gastos do proxecto entre Microsoft Dynamics 365 Finance e Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289637"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sincronizar as categorías de gastos do proxecto entre Finance and Operations e Project Service Automation

[!include[banner](../includes/banner.md)]

Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as categorías de gastos do proxecto entre Dynamics 365 Finance e Dynamics 365 Project Service Automation.

> [!NOTE]
> - A integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades están dispoñibles na versión 8.0.
> - A integración dos datos reais está dispoñible a partir da versión 8.0.1.
> - Se está a usar Enterprise edition 7.3.0, despois de instalar KB 4132657 e KB 4132660, poderá usar os modelos para integrar tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e datos reais e para configurar o bloqueo de funcionalidade. Se debe restablecer as distribucións contables, recomendámoslle que instale tamén KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Fluxo de datos para Project Service Automation e Finanzas

A solución de integración de Project Service Automation e Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas. Os modelos de integración dispoñibles coa funcionalidade de integración de datos permiten o fluxo de datos sobre as categorías de transaccións de gastos do proxecto entre Finanzas e Project Service Automation.

Se as categorías de gastos do proxecto se controlan en Finanzas, o fluxo de integración é primeiro de Finanzas a Project Service Automation. A seguir, actualízanse os ID de integración das categorías de gastos do proxecto mediante a sincronización de Project Service Automation a Finanzas.

Se as categorías de gastos do proxecto se controlan en Project Service Automation, o fluxo de integración é primeiro de Project Service Automation a Finanzas. As categorías do proxecto xa deben estar configuradas en Finanzas antes da sincronización desde Project Service Automation. A seguir, sincronice de novo de Finanzas a Project Service Automation e logo de Project Service Automation a Finanzas de novo. Deste xeito, axudará a garantir que as categorías están vinculadas e que non se crean duplicados.

> [!NOTE]
> Normalmente, as categorías de gastos do proxecto contrólanse en Finanzas. Non obstante, se non e así ou se xa se crearon categorías de gastos en Project Service Automation, primeiro debe sincronizar empregando o modelo de categorías de transaccións de gastos de proxecto (PSA a Fin e Ops). A seguir, sincronízase usando o modelo de categorías de transaccións de gastos do proxecto (Fin e Ops a PSA). A seguir, debería executar a sincronización de Project Service Automation a Finanzas unha vez máis.
>
> Se sincroniza primeiro desde Project Service Automation, antes de executar a sincronización deben cumprirse os seguintes requisitos en Finanzas:
>
> - A categoría compartida que coincida coa categoría de proxecto configurada en Project Service Automation debe existir e debe estar activada para **Proxecto** e **Gasto**.
> - Para cada persoa xurídica de Finanzas coa que se debe integrar, deben existir as seguintes categorías de proxectos:
>
>     - **A categoría do proxecto** existe. 
>     - **Usar en Gasto** está activada.
>     - **Activar en diario** está activada.
>     - **Tipo de transacción** está establecido en **Gasto**.

A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.

[![Fluxo de datos para a integración de Project Service Automation con Finanzas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sincronización da categoría de gastos do proxecto de Finanzas a Project Service Automation

### <a name="template-and-task"></a>Modelo e tarefa

Para acceder ao modelo, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.

O seguinte modelo e a tarefa subxacente úsanse para sincronizar as categorías de gastos do proxecto desde Finanzas ata Project Service Automation:

- **Nome do modelo en integración de datos:** Categorías de transaccións de gastos do proxecto (Fin e Ops a PSA)
- **Nome da tarefa do proxecto:** Sincronizar categorías con PSA

### <a name="entity-set"></a>Conxunto de entidades

| Finanzas                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entidade de integración para categorías | Categorías de transaccións     |

### <a name="entity-flow"></a>Fluxo de entidades

As categorías de gastos do proxecto xestiónanse en Finanzas e se sincronizan con Project Service Automation como categorías de transaccións.

### <a name="power-query"></a>Power Query

Cando se sincronice con Project Service Automation, debe empregar Microsoft Power Query for Excel para establecer o tipo de facturación na categoría de transaccións. O modelo de categorías de transaccións de gastos do proxecto (Fin e Ops a PSA) ofrece unha columna predefinida e asignación. Se crea o seu propio modelo, debe engadir unha columna condicional en Power Query. Siga estes pasos.

1. Prema na frecha para abrir a asignación da tarefa de categorías de gastos do proxecto no modelo de categorías de transaccións de gastos de proxecto (Fin e Ops a PSA).
2. Prema a ligazón **Consulta e filtrado avanzados** para abrir Power Query.
2. Seleccione **Engadir columna condicional**.
3. Introduza un nome para a nova columna, como **Tipo de facturación**.
4. Introduza a seguinte condición: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Prema **Aceptar** na columna.
6. Asegúrese de asignar esta nova columna na páxina de asignación.

A seguinte ilustración mostra un exemplo da asignación de tarefas do modelo en integración de datos. A asignación mostra a información de campo que se sincronizará de Finanzas a Project Service Automation.

[![Asignación de modelos de categoría de gastos do proxecto a Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sincronización da categoría de gastos do proxecto de Project Service Automation a Finanzas

### <a name="template-and-task"></a>Modelo e tarefa

O seguinte modelo e a tarefa subxacente úsanse para sincronizar as categorías de gastos do proxecto de Project Service Automation a Finanzas:

- **Nome do modelo en integración de datos:** Categorías de transaccións de gastos do proxecto (PSA a Fin e Ops)
- **Nome da tarefa do proxecto:** Sincronizar categorías con Fin Ops

### <a name="entity-set"></a>Conxunto de entidades

| Project Service Automation | Finanzas                           |
|----------------------------|-----------------------------------|
| Categorías de transaccións     | Entidade de integración para categorías |

### <a name="entity-flow"></a>Fluxo de entidades

As categorías de gastos do proxecto xestiónanse en Finanzas e se sincronizan con Project Service Automation como categorías de transaccións. A sincronización de novo con Finanzas actualiza a categoría do proxecto en Finanzas co ID de integración desde Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Asignación de modelos na integración de datos

A seguinte ilustración mostra un exemplo da asignación de tarefas do modelo en integración de datos.

> [!NOTE]
> A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.

[![Asignación de modelos de Project Service Automation a Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]