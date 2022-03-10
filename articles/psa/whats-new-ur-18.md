---
title: Novidades ou cambios na versión 18 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 18 de actualización de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 43491a3820d84e9d2a43e678f2604e234e18794d9e28889429debc0b991bbfac
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004354"
---
# <a name="project-service-automation-update-release-18-v3"></a>Versión 18 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 18 de actualización. Esta versión ten un número de compilación de V3.10.8.12 e está xeralmente dispoñible a través dunha actualización automática en abril de 2020.

## <a name="update-release-18"></a>Versión 18 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

- Corrixido: Os fluxos **Recuperar**, **Solicitar** e **Cancelar aprobación** lanzan excepcións con mensaxes de erro pouco claras.
- Corrixido: Cando **Cancelar a aprobación** falla para un gasto, non se lanza un erro de excepción relevante.
- Corrixido: A grade Entrada de tempo xestiona de forma incorrecta os días non laborables en Australia despois do cambio da hora de verán (DST) en outubro.
- Corrixido: A lóxica por defecto incorrecta impide a presentación de gastos.
- Corrixido: Cando falla a aprobación de entrada de tempo, a aprobación permanece en estado de **Pendente**.
- Corrixido: Erros de SQL nas aprobacións en masa (paralización/tempo esgotado).
- Corrixido: Problemas de rendemento importantes na experiencia do usuario causados pola actualización dos membros do equipo mentres aproban as entradas de tempo.

**Xestión de proxectos**

- Corrixido: A notificación do fuso horario mudouse da vista **Conciliación** ao formulario principal **Proxecto**.
- Corrixido: O modelo do calendario non está predefinido correctamente cando se abre un novo formulario de proxecto.
- Corrixido: Nos exploradores baseados en chromium, os usuarios non poden seleccionar facilmente as tarefas predecesoras para eliminar.
- Corrixido: Ao crear ou copiar **Proxecto desde modelo baleiro** obtéñense asignacións non relacionadas.
- Corrixido: En casos específicos de edge, a creación dunha nova asignación desde a grade de tarefas ten como resultado a creación de rexistros duplicados.
- Corrixido: En modo manual, os usuarios non poden actualizar as datas de inicio de tarefas como posteriores á data gardada.

**Xestión de recursos**

- Corrixido: A fila de subtotal da vista **Conciliación** calcula incorrectamente a diferenza das reservas despois de ampliar as reservas.
- Corrixido: A vista **Conciliación** mostra incorrectamente as asignacións de recursos cando o recurso reservable ten un calendario que non coincide co calendario do proxecto.

**Sales**

- Corrixido: Cando se aproban de novo as entradas de tempo (**Aprobar > Cancelar >** aprobar de novo), créase un duplicado real non imputable.


[!INCLUDE[footer-include](../includes/footer-banner.md)]