---
title: Novidades ou cambios na versión 23 de actualización de Project Service Automation, V3
description: Este artigo enumera as funcións e correccións dispoñibles na actualización 23 de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913027"
---
# <a name="project-service-automation-update-release-23-v3"></a>Versión 23 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo enumera as funcións e correccións novas ou modificadas para Project Service Automation V3, actualización 23. Esta versión ten un número de compilación de V 3.10.34.30 e está dispoñible xeralmente a través dunha autoactualización desde agosto de 2020.

## <a name="update-release-23"></a>Versión 23 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:
- Manexar a caixa de edge en **Eliminar membro do equipo do proxecto** para proporcionar unha excepción significativa.
- A importación de atribucións ten como resultado unha pantalla de eliminación en branco.

**Xestión de recursos**

Resolvéronse os seguintes problemas:

- O **Cartón de recursos da grade de utilización de recursos** mostra datos incorrectos cando a escala de tempo é superior a cinco días.
- Cando os clientes crean un recurso reservable, o complemento intermitentemente non engade automaticamente o recurso a un grupo de Microsoft Office 365.
- A vista **Conciliación** mostra incorrectamente os contornos manuais na vista **Semana** ou **Mes**.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- Un número excesivo de entidades **RetrieveMultiple for usersettings** están causando un rendemento degradado para as aprobacións de proxectos e outras operacións.
- A busca de recursos da grade **Planificación de tarefas** está limitada a só amosar ata cinco membros do equipo do equipo do proxecto. 
- A busca de recursos da grade **Planificación de tarefas** non filtra os recursos inactivos.
- O modo manual non funciona como se esperaba na estrutura de subdivisión do traballo da planificación do proxecto.
- A grade **Planificación de tarefas** mostra **Categorías de transaccións inactivas**.
- A grade **Atribución de recursos** redondea incorrectamente cando unha tarefa ten varias atribucións.
- Os valores de redondeo son diferentes entre o custo planificado e o custo real para unha soa tarefa.

**Sales**

Resolvéronse os seguintes problemas:

- Ao premer dúas veces **Obter todas as categorías de transaccións** créanse varias liñas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
