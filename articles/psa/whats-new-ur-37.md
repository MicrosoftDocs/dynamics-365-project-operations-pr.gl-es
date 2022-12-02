---
title: Novidades ou cambios na versión 37 de actualización de Project Service Automation, V3
description: Este artigo indica as funcionalidades e correccións dispoñibles na versión 37 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922496"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novidades ou cambios na versión 37 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 37 de actualización, V3. Esta versión ten un número de compilación V3.10.58.120 e está xeralmente dispoñible mediante unha actualización automática en novembro de 2021.

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
