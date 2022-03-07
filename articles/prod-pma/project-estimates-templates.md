---
title: Sincronizar estimacións de proxectos directamente desde Project Service Automation a Finance and Operations
description: Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as estimacións de horas do proxecto e as estimacións de gastos do proxecto directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6696449d80e0915a0c878dbe75cfdf6e268b98ad9f6453bcfc4b424db68021e4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988199"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar estimacións de proxectos directamente desde Project Service Automation a Finance and Operations

[!include[banner](../includes/banner.md)]

Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar as estimacións de horas do proxecto e as estimacións de gastos do proxecto directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE]
> - A integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades está dispoñible na versión 8.0.
> - A integración dos datos reais está dispoñible a partir da versión 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de datos de Project Service Automation a Finanzas

A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas. Os modelos de integración dispoñibles coa funcionalidade de integración de datos permiten o fluxo de datos sobre as estimacións de horas do proxecto e as estimacións de gastos do proxecto de Project Service Automation a Finanzas.

A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.

[![Fluxo de datos para a integración de Project Service Automation con Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimacións de horas do proxecto

### <a name="template-and-tasks"></a>Modelo e tarefas

Para acceder aos modelos dispoñibles, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.

O seguinte modelo e as tarefas subxacentes úsanse para sincronizar as estimacións de horas do proxecto de Project Service Automation a Finanzas:

- **Nome do modelo en integración de datos:** Estimacións de horas do proxecto (PSA a Fin e Ops)
- **Nome das tarefas do proxecto:**

    - Relacións de transacción
    - Estimacións de gastos

### <a name="entity-set"></a>Conxunto de entidades

| Project Service Automation | Finanzas                                       |
|----------------------------|-----------------------------------------------|
| Tarefas do proxecto              | Entidade de integración para estimacións de horas do proxecto |

### <a name="entity-flow"></a>Fluxo de entidades

As estimacións de horas do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como previsións de horas do proxecto.

### <a name="prerequisites"></a>Requisitos previos

Antes de que poida producirse a sincronización das estimacións de horas do proxecto, debe sincronizar proxectos, tarefas do proxecto e categorías de transaccións de gastos do proxecto.

### <a name="power-query"></a>Power Query

No modelo de estimacións de horas do proxecto, debe usar Microsoft Power Query for Excel para completar estas tarefas:

- Establecer o ID de modelo de previsión predefinido que se usará cando a integración cree novas previsións de horas.
- Filtrar os rexistros específicos de recursos na tarefa que fallarán na integración nas previsións de horas.
- Filtrar as filas de categoría de transaccións baleiras. O incumprimento desta tarefa pode provocar previsións de horas incorrectas.

#### <a name="set-the-default-forecast-model-id"></a>Establecer o ID de modelo de previsión predeterminado

Para actualizar o ID de modelo de previsión predefinido no modelo, prema a frecha de **Asignar** para abrir a asignación. A seguir, seleccione a ligazón **Consulta e filtrado avanzados**.

- Se está a usar o modelo predefinido de estimacións de horas do proxecto (PSA a Fin e Ops), seleccione a última **Condición inserida** na lista de **Pasos aplicados**. Na entrada **Función**, substitúa **O\_forecast** polo nome do ID de modelo de previsión que se debería empregar coa integración. O modelo predefinido ten un ID de modelo de previsión a partir dos datos de demostración.
- Se está a crear un novo modelo, debe engadir esta columna. En Power Query, seleccione **Engadir columna condicional** e escriba un nome para a nova columna, como **ModelID**. Introduza a condición para a columna, onde, se a tarefa de proxecto non é nula, entón \<enter the forecast model ID\>; senón nulo.

#### <a name="filter-out-resource-specific-records"></a>Filtrar rexistros específicos de recursos

O modelo de estimacións de horas do proxecto (PSA a Fin e Ops) ten un filtro predeterminado que elimina os rexistros específicos de recursos. Se crea o seu propio modelo, debe engadir este filtro. Seleccione a ligazón **Consulta e filtrado avanzados** para filtrar na columna **msdyn\_islinetask** para que só se inclúan os rexistros **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrar as filas de categoría de transaccións baleiras

Debe engadir un filtro para eliminar as filas que teñan categorías de transaccións baleiras. Esta tarefa é necesaria, independentemente de se está a usar o modelo predefinido ou se está a crear o seu propio modelo. Este filtro elimina as filas resumidas de Project Service Automation que poidan causar que as previsións de horas en Finanzas sexan incorrectas. Seleccione a ligazón **Consulta e filtrado avanzados** para filtrar rexistros nulos na columna **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Asignación de modelos na integración de datos

A seguinte ilustración mostra un exemplo da asignación de tarefas do modelo en integración de datos. A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.

[![Asignación de tarefas de modelos na integración de datos.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Estimación de gastos do proxecto

### <a name="template-and-tasks"></a>Modelo e tarefas

O seguinte modelo e as tarefas subxacentes úsanse para sincronizar as estimacións de gastos do proxecto de Project Service Automation a Finanzas:

- **Nome do modelo en integración de datos:** Estimacións de gastos do proxecto (PSA a Fin e Ops)
- **Nome das tarefas do proxecto:**

    - Relacións de transacción 
    - Estimacións de gastos

### <a name="entity-set"></a>Conxunto de entidades

| Project Service Automation | Finanzas                                                  |
|----------------------------|----------------------------------------------------------|
| Conexións da transacción    | Entidade de integración para as relacións de transaccións do proxecto |
| Liñas de estimación             | Entidade de integración para estimacións de gastos do proxecto         |

### <a name="entity-flow"></a>Fluxo de entidades

As estimacións de gastos do proxecto xestiónanse en Project Service Automation e sincronízanse con Finanzas como previsións de gastos do proxecto.

### <a name="prerequisites"></a>Requisitos previos

Antes de que poida producirse a sincronización das estimacións de gastos do proxecto, debe sincronizar proxectos, tarefas do proxecto e categorías de transaccións de gastos do proxecto.

### <a name="power-query"></a>Power Query

No modelo de estimacións de gastos do proxecto, debe usar Power Query para completar as seguintes tarefas:

- Filtrar para incluír só rexistros de liñas de estimación de gastos.
- Establecer o ID de modelo de previsión predefinido que se usará cando a integración cree novas previsións de horas.
- Transformar os tipos de facturación.
- Transformar os tipos de transacción.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrar para incluír só liñas de estimación de gastos

O modelo de estimacións de gastos do proxecto (PSA a Fin e Ops) ten un filtro predefinido que só inclúe liñas de gasto na integración. Se crea o seu propio modelo, debe engadir este filtro. Seleccione a tarefa **Relacións de transacción** e prema a frecha **Asignar** para abrir a asignación. Seleccione a ligazón **Consulta e filtrado avanzados**. Filtre a columna **msdyn\_transactiontype1** para que só inclúa **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Establecer o ID de modelo de previsión predeterminado

Para actualizar o ID de modelo de previsión predefinido no modelo, seleccione a tarefa **Estimacións de gastos** e, a seguir, prema a frecha de **Asignar** para abrir a asignación. Seleccione a ligazón **Consulta e filtrado avanzados**.

- Se está a usar o modelo predefinido de estimacións de gastos do proxecto (PSA a Fin e Ops), en Power Query, seleccione a primeira **Condición inserida** desde a sección **Pasos aplicados**. Na entrada **Función**, substitúa **O\_forecast** polo nome do ID de modelo de previsión que se debería empregar coa integración. O modelo predefinido ten un ID de modelo de previsión a partir dos datos de demostración.
- Se está a crear un novo modelo, debe engadir esta columna. En Power Query, seleccione **Engadir columna condicional** e escriba un nome para a nova columna, como **ModelID**. Introduza a condición para a columna, onde, se a ID de liña de estimación non é nula, entón \<enter the forecast model ID\>; senón nulo.

#### <a name="transform-the-billing-types"></a>Transformar os tipos de facturación

O modelo de estimacións de gastos do proxecto (PSA a Fin e Ops) inclúe unha columna condicional que se usa para transformar os tipos de facturación que se reciben de Project Service Automation durante a integración. Se crea o seu propio modelo, debe engadir esta columna condicional. Seleccione a ligazón **Consulta e filtrado avanzados** e logo seleccione **Engadir columna condicional**. Introduza un nome para a nova columna, como **Tipo de facturación**. A seguir, introduza a seguinte condición:

Se **msdyn\_billingtype** = 192350000, entón **Non imputable**  
pero se **msdyn\_billingtype** = 192350001, entón **Imputable**  
pero se **msdyn\_billingtype** = 192350002, entón **Gratuíto**  
pero **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformar os tipos de transacción

O modelo de estimacións de gastos do proxecto (PSA a Fin e Ops) inclúe unha columna condicional que se usa para transformar os tipos de transacción que se reciben de Project Service Automation durante a integración. Se crea o seu propio modelo, debe engadir esta columna condicional. Seleccione a ligazón **Consulta e filtrado avanzados** e logo seleccione **Engadir columna condicional**. Introduza un nome para a nova columna, como **Tipo de transacción**. A seguir, introduza a seguinte condición:

Se **msdyn\_transactiontypecode** = 192350000, entón **Custo**  
pero se **msdyn\_transactiontypecode** = 192350005, entón **Vendas**  
pero **null**

### <a name="template-mapping-in-data-integration"></a>Asignación de modelos na integración de datos

As seguintes ilustracións mostran exemplos das asignacións de tarefas do modelo en integración de datos. A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.

[![Asignación de modelos de transaccións de estimación de gastos.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Asignación de modelos de estimacións de gastos.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]