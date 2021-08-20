---
title: Desactivar unha dimensión de prezos
description: Este tema mostra como configurar as dimensións de prezos na solución Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9f690dfdb40e962ef329f323716f3f755493805d764dbfaa2d4f9d042231cee7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006784"
---
# <a name="turn-off-a-pricing-dimension"></a>Desactivar unha dimensión de prezos

[!include [banner](../includes/psa-now-project-operations.md)]

Pode que necesite revisar e actualizar a súa estratexia de prezos cada poucos anos. Todas as actualizacións que faga pode requirir que desactive unha dimensión de prezos existente e cree unha nova. Por exemplo, pode ter un prezo anterior por **Rol**, pero agora decidiu establecer os prezos por **Experiencia laboral**. Isto pode requirir que desactive **Rol** como dimensión de prezos e cree **Experiencia laboral** como unha nova dimensión de prezos. 

Para desactivar unha dimensión de prezos, independentemente de se é lista para usar ou personalizada, pode configurar os campos **Aplicable ao custo** e **Aplicable ás vendas** da dimensión de prezos en **Non**.

Non obstante, cando faga isto, pode que reciba a seguinte mensaxe de erro.

![Erro de proceso de negocio ao desactivar unha dimensión de prezos.](media/Business-Process-Error.png)


Esta mensaxe de erro indica que hai rexistros de prezos previamente configurados para a dimensión que se vai desactivar. Todos os rexistros de **Prezo de rol** e **Sobreprezo de rol** que fan referencia a unha dimensión deben ser eliminados antes de que se poida establecer a aplicabilidade da dimensión en **Non**. Esta regra aplícase tanto ás dimensións de prezos listas para usar como ás dimensións de prezos personalizadas que creou. O motivo desta validación é porque Project Service ten unha restrición de que cada rexistro de **Prezo de rol** debe ter unha combinación única de dimensións. Por exemplo, nunha lista de prezos chamada **Taxas de custos de EUA 2018**, ten as seguinte filas de **Prezo de rol**. 

| Título estándar         | Unidade organizativa    |Unidade   |Prezo  |Moeda  |
| -----------------------|-------------|-------|-------|----------|
| Enxeñeiro de sistemas|Contoso EUA|Hora| 100|USD|
| Enxeñeiro de sistemas sénior|Contoso EUA|Hora| 150| USD|


Cando desactive **Título estándar** como dimensión de prezos e o motor de prezos de Project Service busque un prezo, só empregará o valor **Unidade organizativa** do contexto de entrada. Se a **Unidade organizativa** do contexto de entrada é "Contoso Estados Unidos", o resultado non será determinista porque coincidirán as dúas filas. Para evitar este escenario, cando cree rexistros de **Prezo de rol**, Project Service valida que a combinación de dimensións é única. Se a dimensión está desactivada despois da creación de rexistros de **Prezo de rol**, pódese violar esta restrición. Polo tanto, é necesario que antes de desactivar unha dimensión, elimine todas as filas de **Prezo de rol** e **Sobreprezo de rol** que encheu ese valor de dimensión.



[!INCLUDE[footer-include](../includes/footer-banner.md)]