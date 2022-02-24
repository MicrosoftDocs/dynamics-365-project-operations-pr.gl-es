---
title: Novidades ou cambios na versión 28 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 28 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150621"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novidades ou cambios na versión 28 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións novas ou modificadas para Project Service Automation V3, versión de actualización 28. Esta versión ten un número de compilación V3.10.46.32 e está dispoñible xeralmente mediante unha actualización automática en xaneiro de 2021.

## <a name="update-release-28"></a>Versión 28 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:

- Os usuarios poden utilizar **Edición en masa** para actualizar as entradas de tempo aprobadas e enviadas.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- Nos casos en que o GUID da tarefa se interpreta como un número, non se poden abrir as tarefas para editar utilizando **Editar tarefa** na fita da páxina **Estrutura de subdivisión do traballo**.

**Sales**

Resolvéronse os seguintes problemas:

- Xérase unha excepción de referencia nula cando se invoca o complemento **GetEstimatesForProject**.
- **Marcar como listo para facturar** na grade de fitos só actualiza parcialmente os atributos, agás o atributo **InvoiceStatus**, que se actualiza.

