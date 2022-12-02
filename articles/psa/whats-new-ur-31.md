---
title: Novidades ou cambios na versión 31 de actualización de Project Service Automation, V3
description: Este artigo mostra as funcionalidades e correccións que están dispoñibles la versión 31 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925026"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novidades ou cambios na versión 31 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 31 de actualización. Esta versión ten un número de compilación de V3.10.52.77 e está xeralmente dispoñible a través dunha actualización automática en maio de 2021.

## <a name="update-release-31"></a>Versión 31 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:

- Os botóns de comando de control de entrada de tempo na páxina **Recurso reservable** eran confusos.
- Xerouse unha excepción de referencia nula en **Project.SetTrackingFields** ao aprobar unha entrada de tempo.

**Xestión de recursos**

Resolvéronse os seguintes problemas:

- **Crear membro do equipo** non mostra correctamente a configuración de metadatos da configuración de reservas para **Estado de compromiso de reserva predefinido**.
- Ao actualizar de PSA 1.X a 3.X, o proceso de actualización falla en **UpgradeResourceRequirements**.


**Vendas**

Resolvéronse os seguintes problemas:

- Os ingresos reais converten as cantidades á moeda do proxecto na grade de rastrexo.
- O valor predefinido da moeda non está claro cando se crean liñas de diario, liñas de oferta e liñas de contrato en situacións nas que a moeda base dunha organización difire da moeda do proxecto.
- A consulta **Validación do diario de corrección pendente** non se filtra por proxecto.
- As vendas restantes calcúlanse incorrectamente nun proxecto.
- As ofertas baseadas nun contacto fallan cando se crean sen unha lista de prezos.
- Non se mostra ningún indicador de procesamento ao seleccionar **Confirmar factura**.
- Non se mostra ningún indicador de procesamento ao seleccionar **Crear factura**.
- Pechar unha oferta como perdida non cancela as reservas.







