---
title: Novidades ou cambios na versión 32 de actualización de Project Service Automation, V3
description: Este artigo mostra as funcionalidades e correccións que están dispoñibles la versión 32 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5124137c24da9b579ee1365524d66d9135b2d420
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912882"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novidades ou cambios na versión 32 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 32 de actualización. Esta versión ten un número de compilación de V3.10.53.108 e normalmente está dispoñible a través dunha actualización automática en xuño de 2021.

## <a name="update-release-32"></a>Versión 32 de actualización

### <a name="bug-fixes"></a>Correccións de erros

#### <a name="general"></a>Xeral

- Cando falla unha actualización importante, só se deben bloquear os puntos de entrada da aplicación principal para garantir que as entidades compartidas sexan aínda accesibles.

#### <a name="time-and-expense"></a>Tempo e gasto

Resolvéronse os seguintes problemas:

- **TimeEntriesImportFromResourceAssignment** non mantén os tempos de inicio e fin da porción de contorno de atribución de recursos.
- Cando selecciona **Abrir entrada** na grade **Entrada de tempo**, é posible que se lle impida seleccionar outros formularios.
- Mentres importa tarefas a entradas de tempo, a consulta de código de cliente pode xerar un URL longo que falla na consulta.
- Na grade **Entrada de tempo**, despois de que se elimine un valor dunha cela, o foco non permanece na grade.
- O botón **Rexeitar** eliminouse da vista **Aprobacións de procesamento** para aprobacións modernas.
- A estabilidade e o rendemento da aprobación masiva de entradas de tempo vense afectados por bloqueos e un fallo no tratamento adecuado das personalizacións relacionadas coa entidade **Entrada de tempo**.

#### <a name="project-planning"></a>Planificación de proxectos

- Xérase unha excepción de referencia nula cando se actualiza un proxecto que ten un valor nulo no campo **Unidade de contratación**.
- **Actualizar os totais do proxecto** calcula incorrectamente o custo restante e as vendas restantes nun proxecto.
- Os cálculos de prezos redundantes afectan ao rendemento relacionado coas actualizacións dos contornos de atribución de recursos.

#### <a name="resource-management"></a>Xestión de recursos

Corrixiuse o seguinte problema:

- Cando a capacidade do calendario dun recurso reservable é superior a 1, Project Service Automation recoñece incorrectamente a capacidade como 0 (cero). Polo tanto, prodúcese un bucle infinito na vista de programación.

#### <a name="sales"></a>Vendas

Resolvéronse os seguintes problemas:

- Cando se crea unha liña de diario que ten un tipo de transacción personalizado, prodúcese a seguinte excepción de referencia nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Os roles e categorías que están inactivos antes de copiar un orzamento non se deben engadir aos roles e categorías imputables da novo orzamento copiado.
- A data do documento e a data de contabilidade non están aliñadas coa data de inicio que se proporciona nun detalle da liña de factura que se crea directamente nun borrador de factura.
- As excepcións de referencia nulas xéranse en escenarios relacionados coa inactivación de roles e categorías antes de copiar un orzamento.
- A acción **Actualizar prezos** na páxina **Proxectos** non actualiza as estimacións de gastos e de material.
