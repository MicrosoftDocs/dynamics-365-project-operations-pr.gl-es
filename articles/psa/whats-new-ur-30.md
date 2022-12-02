---
title: Novidades ou cambios na versión 30 de actualización de Project Service Automation, V3
description: Este artigo mostra as funcionalidades e correccións que están dispoñibles la versión 30 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: ad00b126a13e18a5de47df335aea06b9690efa13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925072"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novidades ou cambios na versión 30 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 30 de actualización. Esta versión ten un número de compilación de V3.10.51.61 e está xeralmente dispoñible a través dunha actualización automática en abril de 2021.

## <a name="update-release-30"></a>Versión 30 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:

- Prodúcese un erro ao crear e gardar unha entrada de tempo na páxina **Creación rápida** páxina se se elimina o campo **Rol**.
- O filtro de entrada de tempo aplica un operador de filtro incorrecto.
- As follas de control horario copiadas non se amosan automaticamente cando selecciona **Copiar semana** no control de entrada de tempo.

**Xestión de recursos**

Resolvéronse os seguintes problemas:

- Cando amplía unha reserva, o estado da reserva atribuído á reserva dura é incorrecto. A extensión dunha reserva respecta o estado da reserva definido como **Comprometido** nos metadatos de configuración da reserva.
- Cando non se especifica un estado de reserva válido, a mensaxe de erro non está localizada correctamente.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- Os proxectos non se poden crear nunha moeda e inclúen tarefas relacionadas noutra moeda.

**Vendas**

Resolvéronse os seguintes problemas:

- Cando se copia unha lista de prezos, os prezos non se actualizan.
- Pechar unha oferta como gañada falla cando o detalle do custo ten un valor para a orixe.
- Na entidade **Tarefa de proxecto**, cambiouse o nome de **Custo estimado** a **Custo planificado (base)**.
- Xérase unha excepción de referencia nula cando se crean ou se eliminan facturas.
