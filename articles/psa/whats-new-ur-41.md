---
title: Novidades ou cambios na versión 41 de actualización de Project Service Automation, V3
description: Este artigo enumera as funcións e correccións que están dispoñibles en Microsoft Dynamics 365 Project Service Automation Actualizar a versión 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930546"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novidades ou cambios na versión 41 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo enumera as funcións e correccións novas ou modificadas para a actualización de Project Service Automation, versión 41, V3. Esta versión ten un número de compilación de V3.10.62.162 e está dispoñible xeralmente a través dunha autoactualización desde marzo de 2022.

## <a name="update-release-41"></a>Versión 41 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Xestión de proxectos**
- Cando tentas crear un proxecto a partir dun modelo baseado nun proxecto creado a partir do complemento de escritorio, aparece o seguinte erro: "Validación do campo de traballo planificado da asignación de recursos: a data de finalización de cada período de asignación de recursos non debe ser anterior ao seu inicio. Data".

**Hora e gasto**
- Cando tentas eliminar unha entrada de hora, aparece a seguinte mensaxe de erro: "Prodúcese un erro inesperado a partir do código ISV".

**Vendas**
- Cando crea unha factura para un fito de prezo fixo, o **Descrición** e **Descrición externa** os campos non están poboados. 
