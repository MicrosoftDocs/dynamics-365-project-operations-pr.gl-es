---
title: Crear un modelo de horas laborables
description: Este artigo describe como crear un modelo de horas de traballo en Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916056"
---
# <a name="create-a-work-hours-template-project-service"></a>Crear un modelo de horas laborables (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Para crear e xestionar un proxecto, debe aplicarlle un modelo de calendario. O modelo de calendario define os seguintes atributos do proxecto:

- Horas de traballo, incluídas as horas de inicio e fin
- Días laborables
- Excepcións do calendario como días non laborables

O modelo de calendario que se aplica a un proxecto é unha copia do modelo de calendario definido na configuración da súa organización.

> [!NOTE]
> Se cambia o modelo de calendario, eses cambios non se propagarán ás horas de traballo do proxecto. Para cambiar as horas de traballo do proxecto, hai que aplicar un novo modelo.

Para crear un modelo de calendario para a súa organización, hai dous requisitos clave:

- Defina as horas de traballo desexadas do modelo empregando un recurso reservable novo ou existente.
- Cree un novo modelo de calendario e asocie o modelo ao recurso reservable.

**Definir as horas de traballo do modelo**

1. Vaia a **Recursos** \> **Recursos**.
2. Cree un novo recurso para facer referencia a el no modelo de calendario ou seleccione un recurso existente.
3. Seleccione o separador **Horas de traballo** do recurso e siga as instrucións de [Establecer horas de traballo para un recurso](/dynamics365/field-service/set-work-hours-resource) para configurar as regras do calendario.

**Crear un novo modelo de calendario**

1. Vaia a **Configuración** \> **Modelo de calendario**.
2. Seleccione **Novo** e introduza un nome, unha descrición e un recurso do modelo.


> [!NOTE]
> Cando se fai referencia a un recurso nun modelo de calendario, asóciase unha copia do calendario do recurso ao modelo de calendario. Se cambian as horas de traballo do modelo copiado, eses cambios non se propagarán ao modelo de calendario.


### <a name="see-also"></a>Consulte tamén  
 [Configurar recursos](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
