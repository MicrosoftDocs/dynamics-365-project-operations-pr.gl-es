---
title: Novidades ou cambios na versión 42 de actualización de Project Service Automation, V3
description: Este tema indica as funcionalidades e correccións dispoñibles na versión 42 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589194"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novidades ou cambios na versión 42 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 42 de actualización, V3. Esta versión ten un número de compilación de V3.10.73.61 e está xeralmente dispoñible a través dunha actualización automática en abril de 2022.

## <a name="update-release-42"></a>Versión 42 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Hora e gasto**

- Cando se rexeita unha folla de horas, o usuario que a rexeitou identifícase incorrectamente como **Sistema**.
- Cando se importan entradas horarias, o **Categoría de recursos** falta o valor.
- Os aprobadores de proxectos poden aprobar proxectos enviados cando os seus permisos non estean especificamente definidos **Pode aprobar**.

**Vendas**

- Cando se rexistran datos reais en tarefas que non son de nivel raíz, os custos reais agréganse incorrectamente.
