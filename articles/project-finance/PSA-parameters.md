---
title: Parámetros de integración de Project Service Automation
description: Este tema explica como configurar como se introducen os datos predefinidos cando se integra Microsoft Dynamics 365 for Project Service Automation con Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: ade812ac-2f8f-4761-a474-0fd7246967df
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e46823f8bd3aef2ba9be271560c3a532be8ef0d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751375"
---
# <a name="project-service-automation-integration-parameters"></a>Parámetros de integración de Project Service Automation

[!include[banner](../includes/banner.md)]

Na páxina **Parámetros de integración de Project Service Automation**, pode configurar como se introducen os datos predefinidos cando se integra Dynamics 365 Project Service Automation con Dynamics 365 Finance. Para que os proxectos se sincronicen con éxito de Project Service Automation a Finanzas, debe configurar os seguintes campos.

Para abrir a páxina **Parámetros de integración de Project Service Automation**, vaia a **Xestión de proxectos e contabilidade** \> **Configurar** \> **Parámetros de integración de Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - A integración de tarefas do proxecto, categorías de transaccións de gastos, estimacións de horas, estimacións de gastos e bloqueo de funcionalidades están dispoñibles na versión 8.0.
> - A integración dos datos reais está dispoñible a partir da versión 8.0.1.


| Separador                    | Campo                | Descripción |
|------------------------|----------------------|-------------|
| Xeral                | Tipo de proxecto predefinido | Seleccione o tipo de proxecto predefinido. Cando os proxectos se sincronizan desde Project Service Automation, este valor úsase se non proporcionou un valor predefinido no modelo de integración. Durante a sincronización, o campo **Tipo de proxecto** dos novos proxectos establécese neste valor. Non obstante, o valor pode actualizarse cando as liñas do contrato do proxecto se sincronizan con Project Service Automation. |
|                        | Categoría de tempo        | Seleccione a categoría de tempo predefinida. Este valor utilízase cando as estimacións de horas se sincronizan desde Project Service Automation. Cando as estimacións de horas e os datos reais horas se sincronizan desde Project Service Automation, o campo **Categoría** das novas previsións de horas do proxecto en Finanzas establécese neste valor. |
|                        | Categoría de tarifas         | Seleccione a categoría de tarifas predefinida. Este valor utilízase cando os datos reais de tarifas se sincronizan desde Project Service Automation. Cando os datos reais de tarifas se sincronizan desde Project Service Automation, o campo **Categoría** das novas transaccións de tarifas do proxecto en Finanzas establécese neste valor. |
| Valores predefinidos do grupo do proxecto | Tipo de proxecto         | Prema **Nova** para engadir unha fila onde pode seleccionar o tipo de proxecto para o que desexa definir o grupo de proxectos predefinido. Un tipo de proxecto específico só se pode seleccionar unha vez na configuración. |
|                        | Grupo de proxectos        | Seleccione o grupo de proxectos predefinido para o tipo de proxecto seleccionado. Cando se sincronizan novos proxectos desde Project Service Automation, o campo **Grupo de proxectos** establécese no valor predefinido para o tipo de proxecto se non proporcionou un valor predefinido no modelo de integración. |
| Valores predefinidos de tipo de facturación  | Tipo de facturación         | Prema **Nova** para engadir unha fila onde pode seleccionar o tipo de facturación para o que desexa definir a propiedade de liña predefinida. Un tipo de facturación específico só se pode seleccionar unha vez na configuración. |
|                        | Propiedade de liña        | Seleccione a propiedade de liña predefinida para o tipo de facturación seleccionado. Cando se sincronizan novas estimacións de horas, novas estimacións de gastos ou novos datos reais desde Project Service Automation, o campo **Propiedade de liña** establécese no valor predefinido para o tipo de facturación. |
| Bloqueo de funcionalidade  | Non aplicable       | Seleccione a funcionalidade para desactivar en Finanzas para proxectos e contratos que se orixinaron desde Project Service Automation. Por exemplo, pode desactivar a capacidade de editar contratos e proxectos, crear estruturas de subdivisión do traballo e introducir follas de control horario en Finanzas. Os campos relacionados coa contabilidade seguirán activados, aínda que a configuración dos parámetros faga que non estean dispoñibles. Por defecto, todas as funcionalidades están habilitadas. |
