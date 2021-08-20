---
title: Sincronizar os datos reais do proxecto directamente desde Project Service Automation ao diario de integración do proxecto para publicalos en Finance and Operations
description: Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar os datos do proxecto directamente desde Microsoft Dynamics 365 Project Service Automation a Finance and Operations.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85b6c07464e919e363f28d8bc62115e8fb4c72ea6631269b98fd00f324a01cba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988109"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sincronizar os datos reais do proxecto directamente desde Project Service Automation ao diario de integración do proxecto para publicalos en Finance and Operations

[!include[banner](../includes/banner.md)]

Este tema describe os modelos e as tarefas subxacentes que se usan para sincronizar os datos do proxecto directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.

O modelo sincroniza as transaccións desde Project Service Automation a unha táboa de transición en Finanzas. Despois de completar a sincronización, vostede **debe** importar os datos da táboa de transición ao diario de integración.

> [!NOTE]
> - A integración dos datos reais do proxecto está dispoñible a partir da versión 8.0.1.
> - Se está a usar Enterprise edition 7.3.0 despois de instalar KB 4132657 e KB 4132660, poderá usar os modelos para integrar tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e datos reais e para configurar o bloqueo de funcionalidade. Se debe restablecer as distribucións contables, recomendámoslle que instale tamén KB 4131710.
> - Se está a usar a versión 7.3.0 e trae transaccións de tarifas desde Project Service Automation, debe instalar KB 4345320 para poder incluír esas tarifas na factura do proxecto.
> - Se introduce importes de impostos sobre vendas a tempo ou en transaccións de gastos en Project Service Automation, debe instalar Project Service Automation Update 7. En caso contrario, os datos fiscais non estarán vinculados aos datos reais de tempo ou gastos asociados e non se sincronizarán con Finanzas. Para obter máis información, contacte co Soporte técnico.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de datos de Project Service Automation a Finanzas

A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Project Service Automation e Finanzas. Os modelos de integración dispoñibles coa funcionalidade de integración de datos permiten o fluxo de datos sobre os datos reais do proxecto desde Project Service Automation ata Finanzas.

A seguinte ilustración mostra como se sincronizan os datos entre Project Service Automation e Finance.

[![Fluxo de datos para a integración de Project Service Automation con Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Datos reais do proxecto de Project Service Automation

### <a name="template-and-tasks"></a>Modelo e tarefas

Para acceder aos modelos dispoñibles, no centro de administración de Microsoft Power Apps, seleccione **Proxectos** e, despois, na esquina superior dereita, seleccione **Novo proxecto** para seleccionar modelos públicos.

O seguinte modelo e as tarefas subxacentes úsanse para sincronizar os datos reais do proxecto desde Project Service Automation ata Finanzas:

- **Nome do modelo en integración de datos:** Datos reais do proxecto (PSA a Fin e Ops)
- **Nome das tarefas do proxecto:**

    - Valores reais
    - Conexións da transacción

### <a name="entity-set"></a>Conxunto de entidades

| Project Service Automation | Finanzas                                   |
|----------------------------|----------------------------------------------------------|
| Valores reais                    | Entidade de integración para datos reais do proxecto                   |
| Conexións da transacción    | Entidade de integración para as relacións de transaccións do proxecto |

### <a name="entity-flow"></a>Fluxo de entidades

Os datos reais do proxecto xestiónanse en Project Service Automation e sincronízanse co diario de integración do proxecto en Finanzas. A contabilidade aplicarase en función das dimensións financeiras predefinidas e da configuración de contabilización.

### <a name="prerequisites"></a>Requisitos previos

Antes de que poida producirse a sincronización de datos reais, debe configurar os parámetros de integración de Project Service Automation e sincronizar proxectos, tarefas do proxecto e categorías de transaccións de gastos do proxecto.

### <a name="power-query"></a>Power Query

No modelo de datos reais do proxecto, debe usar Microsoft Power Query for Excel para completar estas tarefas:

- Transforme o tipo de transacción en Project Service Automation ao tipo de transacción correcto en Finanzas. Esta transformación xa está definida no modelo de datos reais do proxecto (PSA a Fin e Ops).
- Transforme o tipo de facturación en Project Service Automation ao tipo de facturación correcto en Finanzas. Esta transformación xa está definida no modelo de datos reais do proxecto (PSA a Fin e Ops). A seguir, o tipo de facturación asígnase á propiedade da liña, en función da configuración da páxina **Parámetros de integración de Project Service Automation**.
- Filtre a unidades organizativas de recursos específicos que deben sincronizarse con este modelo.
- Se os datos reais de tempo entre empresas ou gastos entre empresas se sincronizarán con Finanzas, deberá transformar a unidade organizativa do contrato á persoa xurídica correcta en Finanzas. No modelo de datos reais do proxecto (PSA a Fin e Ops) defínese unha columna condicional baseada en datos de demostración. Debe actualizar a última columna condicional inserida ás persoas xurídicas correctas. Se non, pode ocorrer un erro de integración ou as transaccións de datos reais incorrectas poden importarse a Finanzas.
- Se os datos reais de tempo entre empresas ou de gastos entre empresas non se sincronizarán con Finanzas, debe eliminar a última columna condicional inserida do seu modelo. Se non, pode ocorrer un erro de integración ou as transaccións de datos reais incorrectas poden importarse a Finanzas.

#### <a name="contract-organizational-unit"></a>Unidade organizativa do contrato
Para actualizar a columna condicional inserida no modelo, prema a frecha de **Asignar** para abrir a asignación. Seleccione a ligazón **Consulta e filtrado avanzados** para abrir Power Query.

- Se está a usar o modelo predefinido de datos reais do proxecto (PSA a Fin e Ops), en Power Query, seleccione a última **Condición inserida** desde a sección **Pasos aplicados**. Na entrada **Función**, substitúa **USSI** polo nome da persoa xurídica que se debería empregar coa integración. Engada condicións adicionais á entrada **Función** que precise e actualice a condición **else** de **USMF** á persoa xurídica correcta.
- Se está a crear un novo modelo, debe engadir a columna para admitir o tempo e os gastos entre empresas. Seleccione **Engadir columna condicional** e escriba un nome para a columna, como **LegalEntity**. Introduza unha condición para a columna, onde, se **msdyn\_contractorganizationalunitid.msdyn\_name** é \<organizational unit\>, entón \<enter the legal entity\>; senón nulo.

### <a name="template-mapping-in-data-integration"></a>Asignación de modelos na integración de datos

As seguintes ilustracións mostran un exemplo da asignación de tarefas do modelo en integración de datos. A asignación mostra a información de campo que se sincronizará de Project Service Automation a Finanzas.

[![Asignación de modelos - Datos reais.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Asignación de modelos - Conexións de transaccións.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importar desde a táboa de transición despois da integración desde Project Service Automation

O proceso periódico Importar desde a táboa de transición debe executarse despois da sincronización de datos reais desde Project Service Automation a Finanzas. Este proceso importará as transaccións do proxecto desde a táboa de transición ao diario de integración de Project Service Automation, onde se aplica a contabilidade e se poden contabilizar as transaccións importadas. Recomendamos que execute este proceso en modo por lotes; opcionalmente pódese configurar para que se execute como un lote recorrente.

## <a name="update-actuals-from-finance"></a>Actualizar datos reais desde Finanzas

### <a name="template-and-tasks"></a>Modelo e tarefas

O seguinte modelo e as tarefas subxacentes úsanse para sincronizar o número do vale e os impostos de vendas para as transaccións do proxecto contabilizadas desde Finanzas a Project Service Automation:

- **Nome do modelo en integración de datos:** Actualización de datos reais do proxecto (Fin Ops a PSA)
- **Nome das tarefas do proxecto:**

    - Valores reais 
    - Conexións da transacción

### <a name="entity-set"></a>Conxunto de entidades

| Finanzas                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entidade de integración para datos reais do proxecto                   | Valores reais                    |
| Entidade de integración para as relacións de transaccións do proxecto | Conexións da transacción    |

### <a name="entity-flow"></a>Fluxo de entidades

Os datos reais do proxecto xestiónanse en Project Service Automation e sincronízanse co diario de integración do proxecto en Finanzas. Despois de contabilizar os datos reais en Finanzas, actualízanse en Project Service Automation co número do vale de Finanzas. Se se engadiron impostos sobre vendas en Finanzas, créanse novos datos reais de impostos en Project Service Automation.

### <a name="power-query"></a>Power Query

No modelo actualización de datos reais do proxecto, debe usar Power Query para completar estas tarefas:

- Transforme o tipo de transacción en Finanzas ao tipo de transacción correcto en Project Service Automation. Esta transformación xa está definida na actualización de datos reais do proxecto (Fin Ops a PSA).
- Transforme o tipo de facturación en Finanzas ao tipo de facturación correcto en Project Service Automation. Esta transformación xa está definida na actualización de datos reais do proxecto (Fin Ops a PSA).

### <a name="template-mapping-in-data-integration"></a>Asignación de modelos na integración de datos

As seguintes ilustracións mostran exemplos das asignacións de tarefas do modelo en integración de datos. A asignación mostra a información de campo que se sincronizará de Finanzas a Project Service Automation.

[![Asignación de modelos - Actualización de datos reais.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Asignación de modelos - Actualización de transaccións.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]