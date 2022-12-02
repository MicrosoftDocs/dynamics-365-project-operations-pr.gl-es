---
title: Novidades ou cambios na versión 45 de actualización de Project Service Automation, V3
description: Este artigo indica as funcionalidades e correccións dispoñibles na versión 45 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169177"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novidades ou cambios na versión 45 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 45 de actualización, V3. Esta versión ten un número de compilación de V3.10.76.168 e está xeralmente dispoñible a través dunha actualización automática en xullo de 2022.

## <a name="update-release-45"></a>Versión 45 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Vendas**

- Os usuarios non poden crear facturas correctamente despois de tentar crear unha factura sen ningunha venda sen facturar, se tamén están vendo a mesma instancia da páxina e non a actualizan.

**Hora e gasto**

- Cando se activan Aprobacións modernas e se aproba a aprobación dun proxecto recuperada, a fase de rexistro actualízase incorrectamente para **Solicitude de recuperación aprobada**.
- Cando se activan as Aprobacións modernas e os fluxos de nube están inactivos, o proceso de aprobación non se realiza correctamente e non se notifica aos usuarios que envían ou aproban.
