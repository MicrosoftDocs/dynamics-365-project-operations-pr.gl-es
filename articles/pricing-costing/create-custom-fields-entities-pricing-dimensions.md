---
title: Crear campos e entidades personalizados como dimensións de prezos
description: Este tema ofrece información sobre como crear conxuntos de opcións ou entidades personalizados.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000524"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Crear campos e entidades personalizados como dimensións de prezos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Realice os seguintes pasos cando queira crear un conxunto de opcións ou unha entidade personalizada para usala como dimensións de prezos. Para obter máis información, consulte [Visión xeral das dimensións de prezos](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Recomendamos que faga todos os cambios de dimensións de prezos personalizados nunha solución separada. Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios cando sexa necesario. Isto tamén axudará á reutilización do seu traballo e facilitará o traslado destes cambios a outra instancia. Despois de facer todos os cambios necesarios, exporte esta solución como **Solución administrada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados e conxuntos de opcións na solución de dimensións de prezos

Unha dimensión de prezos pode ser un conxunto de opcións ou unha entidade. Ambos deben crearse na súa solución de prezos. Os pasos deste procedemento explican como crear dimensións baseadas en entidade e dimensións baseadas en conxunto de opcións.

### <a name="entity-based-dimensions"></a>Dimensións baseada en entidade
Para crear dimensións baseadas en entidade, siga estes pasos:

1. Vaia a **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades**.
3. Seleccione **Nova** para crear unha nova entidade chamada **Título estándar**. 
4. Introduza a información necesaria restante e, a seguir, seleccione **Gardar**.

> ![Definición de entidade de título estándar](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensións baseadas en conxunto de opcións 
Pode crear dúas dimensións baseadas en conxunto de opcións. 

- Utilice **Localización do traballo do recurso** para rastrexar o prezo do traballo na localización **Casa** e o traballo **No sitio**. 
- Utilice **Horas de traballo do recurso** con valores **Normal** e **Horas extra** para aplicar un sobreprezo cando remate o traballo.

O seguinte gráfico ofrece unha vista da dimensión **Localización do traballo do recurso**. 

> ![Dimensión de prezos baseada en conxunto de opcións chamada Localización do traballo do recurso](media/Option-set-PD-called-Resource-Work-Location.png)

O seguinte gráfico ofrece unha vista da dimensión **Horas de traballo do recurso**. 

> ![Dimensión de prezos baseada en conxunto de opcións chamada Horas de traballo do recurso](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Vaia a **Configuración** > **Solucións** e prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Conxuntos de opcións**. 
3. Seleccione **Novo** para crear un novo conxunto de opcións, introduza a información restante necesaria e logo prema **Gardar**.

## <a name="create-data-for-entity-based-dimensions"></a>Crear datos para dimensións baseadas en entidade

Pode crear datos para as dimensións baseadas na entidade manualmente ou mediante importación de Microsoft Excel ou chamadas de servizo. Siga os pasos deste procedemento para crear dous títulos estándar, **Enxeñeiro de sistemas** e **Enxeñeiro principal de sistemas** desde a dimensión baseada en entidade, **Título estándar**. Se os datos que desexa crear son pequenos, como no seguinte exemplo, pode usar un formulario estándar.

1. Seleccione **Busca avanzada**.
2. Seleccione a entidade **Título estándar** e logo seleccione **Resultados**. Mostraranse todas as filas na entidade **Título estándar**.
3. Seleccione **Novo** e no campo **Nome** introduza "Enxeñeiro de sistemas" e logo seleccione **Gardar**.
4. Peche a páxina. 
5. Repita os pasos 1 - 3 para crear outro título estándar para "Enxeñeiro principal de sistemas".

> ![Datos de exemplo para a entidade Título estándar](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]