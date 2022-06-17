---
title: Novidades ou cambios na versión 17 de actualización de Project Service Automation, V3
description: Este artigo enumera as funcións e correccións dispoñibles na actualización de Project Service Automation, versión 17, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915688"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versión 17 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.  Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo enumera as funcións e correccións novas ou modificadas para PSA V3, actualización 17. Esta versión ten un número de compilación de V3.10.6.34 e está dispoñible xeralmente a través dunha autoactualización desde marzo de 2020.


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
- Corrixido: Cando a clase de transacción é **Tempo**, **UnitGroup** é non editable para todas as entidades, incluidas **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**. Non obstante, **Unidade** é non editable só para **JournalLine** e **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
