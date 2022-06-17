---
title: Novidades ou cambios na versión 40 de actualización de Project Service Automation, V3
description: Este artigo enumera as funcións e correccións que están dispoñibles en Microsoft Dynamics 365 Project Service Automation Actualizar a versión 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912790"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novidades ou cambios na versión 40 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo enumera as funcións e correccións novas ou modificadas para a actualización de Project Service Automation, versión 40, V3. Esta versión ten un número de compilación de V3.10.61.61 e está dispoñible xeralmente a través dunha actualización automática en febreiro de 2022.

## <a name="update-release-40"></a>Versión 40 de actualización

### <a name="features"></a>Funcionalidades
A fase 1 da actualización de Project Service Automation a Project Operations - Lite lanzarase en febreiro de 2022 para todos os clientes. Para comprobar a elegibilidade, consulte [Actualiza de Project Service Automation a Project Operations](upgrade-project-operations-non-stocked.md). Se a aplicación non aparece na súa instancia no Power Platform Centro de administración, póñase en contacto co servizo de asistencia e solicite que se habilite o voo para os teus ambientes. A túa solicitude debe incluír unha lista de ID do contorno nos que hai que activar o voo.

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Hora e gasto**
- Falta unha entrada de nota cando se rexeita ou cancela unha entrada de hora. 

**Vendas**

- Cando actualizas as estimacións de custos ou de vendas usando complementos listos para usar, tes permiso incorrecto para enviar cargas útiles JSON que non son válidas fóra da interface de usuario.
- Cando actualices as liñas de presupostos usando a vista rápida, podes activar as citas.
