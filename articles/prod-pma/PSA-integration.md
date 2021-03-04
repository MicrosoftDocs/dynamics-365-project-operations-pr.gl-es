---
title: Visión xeral de Project Service Automation
description: Este tema ofrece información sobre a solución de integración Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642451"
---
# <a name="project-service-automation-overview"></a>Visión xeral de Project Service Automation

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

A solución de integración de Project Service Automation a Finanzas usa a funcionalidade de Integración de datos para sincronizar datos entre instancias de Dynamics 365 Finance e Dynamics 365 Project Service Automation a través de Common Data Service. A integración de modelos dispoñible coa funcionalidade de integración de datos permite o fluxo de proxectos, contratos de proxectos, liñas de contratos de proxectos, fitos da liña de contratos de proxectos, tarefas de proxectos, categorías de transaccións de datos, estimacións de horas e estimacións de gastos de Project Service Automation a Finanzas.

> [!NOTE]
> - Se está a usar a versión 7.3.0, debe instalar KB 4074835. Despois poderá integrar proxectos de prezo fixo.
> - Se está a usar a versión 7.3.0 e trae transaccións de tarifas desde Project Service Automation, debe instalar KB 4345320 para poder incluír esas tarifas na factura do proxecto.
> - Se está a usar a versión 8.0, poderá usar a integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades.
> - Se está a usar a versión 8.0.1 ou posterior, poderá sincronizar os datos reais.

Antes de poder integrar Project Service Automation Finance, debe configurar os parámetros de integración de Project Service Automation. Para obter máis información, consulte [Parámetros de integración de Project Service Automation](PSA-parameters.md).

Esta solución de integración permite a sincronización directa nos seguintes escenarios:

- Manter contratos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.
- Crear proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.
- Manter liñas de contratos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.
- Manter fitos de liñas de contratos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.
- Manter tarefas de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.
- Manter contratos de categorías de transaccións de gastos en Finanzas e sincronizalos directamente desde Finanzas a Project Service Automation.
- Crear estimacións de horas de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.
- Crear estimacións de gastos de proxectos en Project Service Automation e sincronizalos directamente desde Project Service Automation a Finance.
- Crear datos reais de tempo, gastos e tarifas de proxectos en Project Service Automation e cree transaccións de proxectos no diario de integración de Project Service Automation para que poidan contabilizarse en Finanzas.

## <a name="data-synchronization"></a>Sincronización de datos

A seguinte ilustración mostra como se sincronizan os datos como parte da integración entre Project Service Automation e Finanzas.

> [!NOTE]
> Non están dispoñibles todos os modelos actualmente. Os modelos publicaranse a medida que se completen.

[![Integración de Project Service Automation con Finanzas](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Requisitos do sistema para Finanzas

Para usar a solución de integración de Project Service Automation a Finanzas, debe instalar Enterprise edition 7.3 coa plataforma 12 ou posterior.

## <a name="system-requirements-for-project-service-automation"></a>Requisitos do sistema para Project Service Automation

Para usar a solución de integración de Project Service Automation a Finanzas, debe instalar os seguintes compoñentes:

- Dynamics 365 Project Service Automation versión 9.0.0.0 ou posterior
- Solución de posible a interesado a efectivo para Dynamics 365 Sales, versión 1.14.0.0 (v14) ou posterior
- Solución de Project Service Automation a Finanzas para Dynamics 365 Project Service Automation versión 1.0.0.0 o posterior

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instalar a solución de integración de Project Service Automation a Finanzas na súa instancia de Project Service Automation

Descargue a solución de integración de Project Service Automation a Finanzas del [Centro de descargas de Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) e siga as instrucións que se inclúen coa solución.


[!INCLUDE[footer-include](../includes/footer-banner.md)]