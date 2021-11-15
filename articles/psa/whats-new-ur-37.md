---
title: Novidades ou cambios na versión 37 de actualización de Project Service Automation, V3
description: Este tema indica as funcionalidades e correccións dispoñibles na versión 37 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727603"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novidades ou cambios na versión 37 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 37 de actualización, V3. Esta versión ten un número de compilación V3.10.58.120 e está xeralmente dispoñible mediante unha actualización automática en novembro de 2021.

## <a name="update-release-37"></a>Versión 37 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Hora e gasto**
- Os usuarios non poden eliminar unha entrada de tempo borrando a cela.
- A vista **A miña aprobación con erros** só contén aprobacións de proxectos cun estado de **Enviado**.

**Xestión de proxectos**
- Os usuarios reciben un erro de excepción de referencia nula ao abrir un proxecto no complemento de escritorio de Microsoft se o nome do posto do membro do equipo do proxecto está baleiro.
- Non hai botón **Gardar** na páxina **Tarefa do proxecto**, polo que os usuarios non poden gardar os cambios nos rexistros de tarefas.
- Os usuarios non poden eliminar un proxecto que teña unha tarefa asociada a unha oferta cun estado de **Gañada**.

**Vendas**
- O campo **Moeda** na páxina **Proxecto** actualízase para que coincida coa moeda do modelo aplicado.
- O custo calcúlase incorrectamente en tarefas que teñen varias moedas.
