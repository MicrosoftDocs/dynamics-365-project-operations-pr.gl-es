---
title: Crear campos e entidades personalizados
description: Este tema explica como crear conxuntos de opcións e entidades na súa propia solución na plataforma Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d2fbe6a4061a93ac3186bbc8624bf5d16209cdf9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574382"
---
# <a name="create-custom-fields-and-entities"></a>Crear campos e entidades personalizados 

[!include [banner](../includes/psa-now-project-operations.md)]

Realice os seguintes pasos sempre que queira crear un conxunto de opcións ou unha entidade personalizada na plataforma Power Apps.  
Os procedementos deste tema deberían realizarse mediante a interface web de Project Service Automation (PSA).

> [!IMPORTANT]
> Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada. Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia. Despois de facer todos os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos

Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade. Ambos deben crearse na súa solución de prezos. Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.

### <a name="entity-based-dimensions"></a>Dimensións baseada en entidade

1. En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.
3. Prema en **Nova** para crear unha nova entidade chamada **Título estándar**. Introduza a información necesaria restante e, a seguir, prema **Gardar**.

> ![Definición de entidade de título estándar.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensións baseadas en conxunto de opcións 
Pode crear dúas dimensións baseadas en conxunto de opcións. Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo con localización **Casa** e o traballo **No sitio** e utilice **Horas de traballo do recurso** cos valores **Normal** e **Horas extra** para aplicar un aumento cando finalice o traballo.


1. En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**. 
3. Prema **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.

> ![Dimensión de prezos baseada en conxunto de opcións chamada Localización do traballo do recurso.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensión de prezos baseada en conxunto de opcións chamada Horas de traballo do recurso.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Crear datos para dimensións baseadas en entidade

Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo. Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**. Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.

1. En PSA prema **Localización avanzada**. Seleccione a entidade **Título estándar** e logo prema **Resultados**. Mostraranse todas as filas na entidade **Título estándar**.
2. Prema **Novo**. No campo **Nome** introduza "Enxeñeiro de sistemas" e logo prema **Gardar**.
3. Peche o formulario. 
4. Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".

> ![Datos de exemplo para a entidade Título estándar.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
