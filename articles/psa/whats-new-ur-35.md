---
title: Novidades ou cambios na versión 35 de actualización de Project Service Automation, V3
description: Este artigo indica as funcionalidades e correccións dispoñibles na versión 35 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912836"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novidades ou cambios na versión 35 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 35 de actualización, V3. Esta versión ten un número de compilación de V3.10.56.110 e está xeralmente dispoñible a través dunha actualización automática en setembro de 2021.

## <a name="update-release-35"></a>Versión 35 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Tempo e gasto**

- O responsable de aprobacións de proxectos recibe un erro de privilexio de lectura cando aproba as entradas de gasto cun rol de **Responsable de aprobacións de proxectos**.
- O responsable de aprobacións de proxectos recibe un erro de privilexio de escritura en **msdyn_projectapproval** cando cancela unha entrada de tempo aprobada cun rol de **Responsable de aprobacións de proxectos**.
- Cando selecciona **Copiar semana** nunha entrada de tempo no módulo da aplicación Dynamics 365 para teléfonos - Project Resource Hub, prodúcese o seguinte erro: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE. "
- A política **Tentar de novo** aproba automaticamente as entradas que foron previamente rexeitadas.
- A subgrade **Conxuntos de aprobacións** mostra accións de fita non aplicables.
- Faltan as iconas para **Tarefa do proxecto** e **Rol do recurso** na entidade **Entrada de tempo**.
- Cando importa as atribucións de recursos, as entradas de tempo importadas non teñen a duración correcta para as tarefas creadas mediante tarefas en modo manual.
- Falta **Eliminar** na páxina **Busca avanzada de rexistros de entrada de tempo**.
- Falta **Gardar** na páxina **Información de entrada de hora**. Este problema impide gardar os cambios cando se pecha a páxina.

**Planificación de proxectos**

- As grades **Atribución de recursos** e **Conciliación de recursos** non ordenan alfabeticamente os atributos agrupados.
- Non se poden crear tarefas se o comportamento da data está personalizado para **Só data**.

**Xestión de recursos**

- Se Dynamics 365 Field Service Project Service Automation están instalados, prodúcense problemas de superposición cando **Visualización asociada do requisito do recurso** está asociado a unha páxina principal.
- Ao premer dúas veces **Gardar** na caixa de diálogo **Creación rápida de membro do equipo** non se pode crear o requisito do recurso.

**Vendas**

- Prodúcese unha excepción se elimina unha tarefa asociada a unha oferta que ten un estado de **Gañada**.
