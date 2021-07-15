---
title: Novidades ou cambios na versión 33 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 33 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334536"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novidades ou cambios na versión 33 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 33 de actualización. Esta versión ten un número de compilación de V3.10.54.98 e está xeralmente dispoñible a través dunha actualización automática en xullo de 2021.

## <a name="update-release-33"></a>Versión 33 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:

- Dous campos bloqueados, **msdyn_description** e **msdyn_externaldescription** pódense editar despois do envío.
- Prodúcese unha mensaxe de erro se se crea un gasto que non está relacionado cun proxecto.
- Cando se crea unha entrada de tempo, o rol de recurso predeterminado é un rol inactivo.
- As liñas de diario asociadas a un gasto recuperado e eliminado non se eliminan.
- No **Formulario de creación rápida de entrada de tempo**, actualice a vista **Lista de tarefas do proxecto** para cambiar a data mostrada por defecto á data de inicio da tarefa.
- Cando crea unha entrada de tempo desde o separador **Relacionado** do recurso reservable, a entrada de tempo créase incorrectamente para o usuario que iniciou sesión no canto do recurso reservable principal.
- Engádense novos campos á caixa de diálogo **MDD de aprobacións en masa**.

**Planificación de proxectos**

Resolvéronse os seguintes problemas:
- Rendemento lento da creación de proxectos cando os modelos de hora de traballo do proxecto se aplican con calendarios complexos.
- Cando a data de inicio é maior que a data de finalización, amósase un erro no modelo de copia de proxecto debido ás diferenzas no compoñente de tempo de cada campo.

**Xestión de recursos**

Resolvéronse os seguintes problemas:
- Utilízase un parámetro incorrecto na consulta de utilización de recursos e o XML dá lugar a resultados de filtros incorrectos na grade **Utilización de recursos**.
- A confirmación de **Estender reservas** mostra a data de finalización incorrecta das reservas.

**Vendas**

Resolvéronse os seguintes problemas:
- Aparecerá unha mensaxe de erro se se crea un prezo de categoría con valores que faltan.
- Prodúcese unha mensaxe de erro se se crea un fito da liña de contrato sen unha liña de pedido.
