---
title: Crear campos e entidades personalizados
description: Este tema explica como crear conxuntos de opcións e entidades na súa propia solución na plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751451"
---
# <a name="create-custom-fields-and-entities"></a>Crear campos e entidades personalizados 

Realice os seguintes pasos sempre que queira crear un conxunto de opcións ou unha entidade personalizada na plataforma Power Apps.  
Os procedementos deste tema deberían realizarse mediante a interface web de Project Service Automation (PSA).

> [!IMPORTANT]
> Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada. Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia. Despois de facer todos os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crear unha solución personalizada para as dimensións de prezos
1. En PSA, prema en **Configuración** > **Solucións** e logo prema en **Nova** para crear unha nova solución. 
2. Poña nome á solución, **\<nome da súa organización> dimensións de prezos**, introduza a información restante necesaria e logo prema en **Gardar**.

> ![Creación dunha solución personalizada para as dimensións de prezos](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos

Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade. Ambos deben crearse na súa solución de prezos. Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.

### <a name="entity-based-dimensions"></a>Dimensións baseada en entidade

1. En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces en **\<nome da súa organización> dimensións de prezos**.
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.
3. Prema en **Nova** para crear unha nova entidade chamada **Título estándar**. Introduza a información necesaria restante e, a seguir, prema **Gardar**.

> ![Definición de entidade de título estándar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensións baseadas en conxunto de opcións 
Pode crear dúas dimensións baseadas en conxunto de opcións. Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo con localización **Casa** e o traballo **No sitio** e utilice **Horas de traballo do recurso** cos valores **Normal** e **Horas extra** para aplicar un aumento cando finalice o traballo.


1. En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces en **\<nome da súa organización> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**. 
3. Prema **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.

> ![Dimensión de prezos baseada en conxunto de opcións chamada Localización do traballo do recurso ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensión de prezos baseada en conxunto de opcións chamada Horas de traballo do recurso ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Crear datos para dimensións baseadas en entidade

Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo. Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**. Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.

1. En PSA prema **Localización avanzada**. Seleccione a entidade **Título estándar** e logo prema **Resultados**. Mostraranse todas as filas na entidade **Título estándar**.
2. Prema **Novo**. No campo **Nome** introduza "Enxeñeiro de sistemas" e logo prema **Gardar**.
3. Peche o formulario. 
4. Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".

> ![Datos de exemplo para a entidade Título estándar ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Engada todas as entidades PSA requiridas e os compoñentes relacionados á solución de dimensión de prezos
Terá que engadir as seguintes entidades de Project Service á súa solución de prezos. Siga os pasos deste procedemento para facer algúns cambios importantes do esquema na solución de prezos para que as entidades teñan coñecemento das novas dimensións de prezos.

1. En PSA, prema **Configuración** > **Solucións** e logo prema dúas veces en **\<nome da súa organización> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.
3. Na caixa de diálogo **Compoñentes da solución**, seleccione as seguintes entidades:

- Real
- Recurso reservable
- Liña de estimación
- Detalle da liña da factura
- Liña de diario
- Detalle da liña de contrato do proxecto
- Membro do equipo do proxecto
- Detalle da liña da oferta
- Sobreprezo de rol
- Prezo do rol 
- Entrada de tempo 

> ![Engadir entidades existentes á solución de dimensións de prezos](media/Existing-entities-to-PD-solution.png)

> ![Seleccionar compoñentes da solución](media/Dimension-Components.png)

> [!NOTE]
> Asegúrese de incluír todos os formularios e vistas para cada unha das entidades seleccionadas.

4. Cando se lle solicite incluír calquera entidade dependente para as entidades seleccionadas anteriormente, prema en **Non**.

> ![Non incluír todos os compoñentes relacionados](media/Do-not-include-required.png)


