---
title: Novidades ou cambios na versión 16 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 16 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f577cd8407b0f12607c56891eeadb1071f659cff67bd9f086a6b3bbec6376e9d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004399"
---
# <a name="project-service-automation-update-release-16-v3"></a>Versión 16 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.  Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar e actualizar unha solución preferida](/dynamics365/project-service/upgrade-psa-home-page)
Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 16 de actualización. Esta versión ten un número de compilación de V3.10.6.34 e está dispoñible xeralmente a través dunha autoactualización desde xaneiro de 2020.


## <a name="update-release-16"></a>Versión 16 de actualización

### <a name="bug-fixes"></a>Correccións de erros

-   Tempo e gasto

    -   Corrixido: Os usuarios que tentan enviar as entradas de tempo e gasto eliminadas para aprobacións recibirán agora os mensaxes de erro correspondentes.

-   Xestión de proxectos

    -   Corrixido: As unidades de recursos definidas para os membros do equipo nos modelos respéctanse e os modelos aplícanse a un novo proxecto.

    -   Corrixido: Mellora da xestión da reasignación da propiedade de rexistros.

    -   Corrixido: Os proxectos que están en proceso de copiarse non poderán copiarse ata que todas as operacións de copia estean rematadas.

-   Xestión de recursos

    -   Corrixido: Estender reservas agora xestiona correctamente as duracións curtas e xa non crea cero horas para as reservas estendidas.

    -   Corrixido: A vista de reconciliación agora mostra cando a zona horaria do proxecto é +5:30 GMT e a hora do usuario é diferente.

-   Sales

    -   Corrixido: Cando se elimina un proxecto asignado a unha liña de contrato e se asigna un novo proxecto, os rexistros reais do novo proxecto non se avaliaban de novo segundo as regras de facturación e prezos definidas na liña de contrato. Isto corrixiuse nesta versión. Os prezos e os rexistros reais do proxecto recentemente asignado reverteranse e crearanse de novo correctamente segundo as regras de prezos e facturación da liña de contrato. Como consecuencia, os rexistros reais do proxecto non asignado avaliaranse e crearanse de novo.

    -   Corrixido: Engadiuse a validación adicional a un campo **Importe** da liña de estimación para asegurarse de que os valores nulos non persisten.

    -   Corrixido: Cando se actualizaron os datos reais nun proxecto, engadiuse un botón de actualización ao formulario principal do proxecto para permitir aos usuarios sincronizar de novo os datos reais.

    -   Corrixido: Cando os usuarios actualicen de 2.X a 3.X, permitiránse proxectos cun valor NULL para o nome do proxecto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]