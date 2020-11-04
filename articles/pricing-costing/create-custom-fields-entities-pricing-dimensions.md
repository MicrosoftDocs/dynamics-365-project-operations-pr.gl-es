---
title: Crear campos e entidades personalizados como dimensións de prezos
description: Este tema ofrece información sobre como crear conxuntos de opcións ou entidades personalizados.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076170"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Crear campos e entidades personalizados como dimensións de prezos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Realice os seguintes pasos sempre que queira crear un conxunto de opcións ou unha entidade personalizados.

> [!IMPORTANT]
> Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada. Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia. Despois de facer todos os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crear unha solución personalizada para as dimensións de prezos
1. Vaia a **Configuración** > **Solucións** e logo seleccione en **Nova** para crear unha nova solución. 
2. Poña nome á solución, **\<your organization name> dimensións de prezos** , introduza a información restante necesaria e logo seleccione **Gardar**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos

Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade. Ambos deben crearse na súa solución de prezos. Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.

### <a name="entity-based-dimensions"></a>Dimensións baseada en entidade

1. Vaia a **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.
3. Seleccione **Nova** para crear unha nova entidade chamada **Título estándar**. 
4. Introduza a información necesaria restante e, a seguir, seleccione **Gardar**.


### <a name="option-set-based-dimensions"></a>Dimensións baseadas en conxunto de opcións 
Pode crear dúas dimensións baseadas en conxunto de opcións. Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo con localización **Casa** e o traballo **No sitio** e utilice **Horas de traballo do recurso** cos valores **Normal** e **Horas extra** para aplicar un aumento cando finalice o traballo.


1. Vaia a **Configuración** > **Solucións** e prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**. 
3. Seleccione **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.

## <a name="create-data-for-entity-based-dimensions"></a>Crear datos para dimensións baseadas en entidade

Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo. Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**. Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.

1. Seleccione **Busca avanzada** , seleccione a entidade **Título estándar** e, a seguir, seleccione **Resultados**. Mostraranse todas as filas na entidade **Título estándar**.
2. Seleccione **Novo** e no campo **Nome** introduza "Enxeñeiro de sistemas" e logo seleccione **Gardar**.
3. Peche o formulario. 
4. Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Engada todas as entidades requiridas e os compoñentes relacionados á solución de dimensión de prezos
Terá que engadir as seguintes entidades á súa solución de prezos. Siga os pasos deste procedemento para facer algúns cambios importantes do esquema na solución de prezos para que as entidades teñan coñecemento das novas dimensións de prezos.

1. Seleccione **Configuración** > **Solucións** e prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.
3. Na caixa de diálogo **Compoñentes da solución** , seleccione as seguintes entidades:

  - Real
  - Recurso reservable
  - Liña de estimación
  - Detalle da liña da factura
  - Liña de diario
  - Detalle da liña de contrato do proxecto
  - Membro do equipo do proxecto
  - Detalle da liña da oferta
  - Sobreprezo do prezo da función
  - Prezo do rol 
  - Entrada de tempo 


> [!NOTE]
> Asegúrese de incluír todos os formularios e vistas para cada unha das entidades seleccionadas.

4. Cando se lle solicite incluír calquera entidade dependente para as entidades seleccionadas anteriormente, seleccione **Non**.

