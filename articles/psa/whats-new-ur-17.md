---
title: Novidades ou cambios na versión 17 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 17 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076088"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versión 17 de actualización de Project Service Automation, V3

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.  Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 17 de actualización. Esta versión ten un número de compilación de V3.10.6.34 e está dispoñible xeralmente a través dunha autoactualización desde marzo de 2020.


## <a name="update-release-17"></a>Versión 17 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Xeral**

- Corrixido: Actualizar Project Service Automation para aplicar as licenzas dos membros do equipo (a plataforma común de recursos do proxecto incluirá os metadatos de Team Member Service 3.x)
 
**Tempo e gasto**

- Corrixido: Non é posible cambiar unha estimación de gastos dun prezo non cero a cero (0). O cambio ignórase.

**Xestión de proxectos**

- Corrixido: Engadiuse un control de valores nulos no nome do posto dun membro do equipo.
- Corrixido: O campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** quedou desfasado.
- Corrixido: A actualización de 2.x a 3.x agora xestiona contornos de esforzo baleiros nas asignacións de tarefas.

**Sales**

- Corrixido: **Invoice.PreValidateInvoiceUpdate** agora xestiona adecuadamente o escenario de reasignar correctamente os propietarios de rexistros.
- Corrixido: Cando a clase de transacción é **Tempo** , **UnitGroup** é non editable para todas as entidades, incluidas **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** e **ContractLineDetails**. Non obstante, **Unidade** é non editable só para **JournalLine** e **InvoiceLineDetails**.


