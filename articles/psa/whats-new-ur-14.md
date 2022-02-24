---
title: Novidades ou cambios na versión 14 de actualización de Project Service Automation, V3
description: Este tema fornece información sobre as novidades e as modificacións na versión 14 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147156"
---
# <a name="project-service-automation-update-release-14-v3"></a>Versión 14 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización para a aplicación Dynamics 365 Project Service Automation (PSA). Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite o Centro de administración para Dynamics 365 en liña e vaia á páxina de solucións para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 14 de actualización. Esta versión ten un número de compilación de V3.10.4.21 e está dispoñible na seguinte programación:

- **Dispoñibilidade xeral (autoactualización):** Xaneiro de 2020
- **Autoactualización:** Febreiro de 2020

## <a name="update-release-14"></a>Versión 14 de actualización

### <a name="enhancements"></a>Melloras

- Sales

     - Os valores de campo personalizado de **Detalles de liña de oferta** cópianse a **Detalles da liña de contrato do proxecto** cando se actualiza unha oferta a **Pechada como gañada**.
     - Os proxectos confirmados poden ser **Pechado como perdido**.

- Xestión de recursos

     - Ao ampliar as reservas, pedirase aos usuarios cunha caixa de diálogo de confirmación que resuman os resultados da reserva e proporcionar unha ligazón a Manter reservas.


### <a name="bug-fixes"></a>Correccións de erros

- Tempo e gasto

     - Corrixido: Mellorou a experiencia do usuario cando o usuario non seleccionou ningunha entrada para corrixir.

- Xestión de recursos

     - Corrixido: A reserva dun recurso en varias ocasións desborda o nome do recurso reservable.

- Sales

     - Fixado: O prezo total de vendas non se calcula ata que o usuario tamén introduza un prezo de custo para estimacións de gastos nun proxecto.
     - Corrixido: Pechar unha oferta como **Gañada** falla se o contrato do proxecto asociado non está nun estado de **Borrador**.

