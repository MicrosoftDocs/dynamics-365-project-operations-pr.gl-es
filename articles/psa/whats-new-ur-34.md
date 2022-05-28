---
title: Novidades ou cambios na versión 34 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 34 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588688"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novidades ou cambios na versión 34 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 34 de actualización. Esta versión ten un número de compilación de V3.10.55.38 e está xeralmente dispoñible a través dunha actualización automática en xullo de 2021.

## <a name="update-release-34"></a>Versión 34 de actualización

### <a name="bug-fixes"></a>Correccións de erros
Resolvéronse os seguintes problemas.

**Xeral**

- As actualizacións xeradas polo editor non activan o novo fluxo de traballo de aprobación moderno.
- Os atributos **Estado obxectivo** e **Tipo de acción** faltan na páxina principal de **Conxunto de aprobacións**.

**Tempo e gasto**

- Non se puido aprobar unha solicitude de retirada usando o fluxo de aprobación moderno.
- A copia dunha semana de entradas de tempo non funciona cando se copian entradas que non están relacionadas co usuario que iniciou sesión.

**Planificación de proxectos**

- Os contornos de atribución de recursos están corrompidos ao importar desde o complemento de escritorio Microsoft Project.

**Xestión de recursos**

- Cando publica un proxecto desde o complemento de cliente de escritorio Microsoft Project, cambia a data de finalización dos requisitos existentes.
- A precisión decimal supera os dous decimais no diálogo de confirmación de estender reservas.

**Vendas**

- Cando engade unha liña baseada en produtos cun produto existente a un contrato de proxecto, móstrase a excepción **clave non atopada no dicionario**.
- Os clientes potenciais non se poden cualificar cando un tipo de pedido se asigna desde un cliente potencial a unha oportunidade.
