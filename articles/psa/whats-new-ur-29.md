---
title: Novidades ou cambios na versión 29 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 29 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 56cf47d207c7ee518d5d4b53866c3d6ddf1d1fb3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587216"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novidades ou cambios na versión 29 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 29 de actualización. Esta versión ten un número de compilación de V3.10.47.7 e está dispoñible xeralmente a través dunha actualización automática en febreiro de 2021.

## <a name="update-release-29"></a>Versión 29 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:

- Os usuarios non poden ver as horas de traballo rexistradas en días non laborables na grade de entrada de tempo.
- As entradas de gastos aprobadas pódense editar na grade.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- Falta a lóxica de validación para garantir que as horas de esforzo de atribución de recursos non poidan ser negativas.
- A acción personalizada **AssignResourcesForTask** actualiza todos os campos en vez de só os campos modificados.
- Ao copiar un proxecto nun ambiente con complementos ou fluxos de traballo rexistrados no evento **CreateProject**, o atributo **msdyn_bulkgenerationstatus** non se actualiza se falla **CopyWBSToProject**.
- Ao ampliar o calendario do proxecto, os días hábiles non se ordenan en orde ascendente e provocan o fallo dalgunhas actualizacións das tarefas do proxecto.
- Cambiar o xestor de proxectos nun proxecto existente desencadea a lóxica predefinida da unidade organizativa.

**Vendas**

Resolvéronse os seguintes problemas:

- O separador **Execución do contrato** na páxina **Contrato** falla en silencio durante o inicio cando non hai liñas de contrato.
