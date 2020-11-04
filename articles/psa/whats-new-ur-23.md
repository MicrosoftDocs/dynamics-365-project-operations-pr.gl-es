---
title: Novidades ou cambios na versión 23 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 23 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076079"
---
# <a name="project-service-automation-update-release-23-v3"></a>Versión 23 de actualización de Project Service Automation, V3

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 23 de actualización. Esta versión ten un número de compilación de V 3.10.34.30 e está dispoñible xeralmente a través dunha autoactualización desde agosto de 2020.

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