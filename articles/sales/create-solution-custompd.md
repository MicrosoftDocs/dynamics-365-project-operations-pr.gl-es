---
title: Crear unha solución para as dimensións de prezos personalizadas
description: Este tema fornece información sobre como crear solucións para dimensións de prezos personalizadas.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 753f0c4496bafd43d7e4a399cedeb355c2163c7ce56d932b2c786d5f2e672b6b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992204"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Crear unha solución para as dimensións de prezos personalizadas

 _**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_ 

>[!IMPORTANT]
>Todos os cambios de dimensións de prezos personalizadas deberían estar nunha solución separada. Esta importante boa práctica permite a flexibilidade para actualizar ou eliminar os cambios segundo sexa necesario, axuda á reutilización do seu traballo e facilita levar estes cambios a outras instancias. Despois de facer todos os cambios necesarios, exporte esta solución como unha solución **Xestionada** e logo impórtea a outras instancias para a súa reutilización.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Crear unha solución para as dimensións de prezos personalizadas

1.  Seleccione **Configuración** > **Solucións** e logo seleccione **Nova**.
2.  Poña nome á solución, *Dimensións de prezos de <your organization name>*.
3. Introduza a información necesaria restante e, a seguir, seleccione **Gardar**.

  ![Creación dunha solución de dimensión de prezos personalizada.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Engadir todas as entidades requiridas e os compoñentes relacionados á solución de dimensión de prezos

Engada as seguintes entidades de Project Service á súa solución de prezos para facer cambios importantes no esquema da solución de prezos. Despois de completar este procedemento, as entidades recoñecerán as novas dimensións de prezos.

1.  Seleccione **Configuración** > **Solucións** e logo prema dúas veces en **Dimensións de prezos de <*nome da súa organización*>**.
2.  No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.
3.  Na caixa de diálogo **Compoñentes da solución**, seleccione as seguintes entidades:
 
   - **Dato real**
   - **Recurso reservable**
   - **Liña de estimación**
   - **Tarefa do proxecto**
   - **Detalle da liña da factura**
   - **Liña de diario**
   - **Detalle da liña de contrato do proxecto**
   - **Membro do equipo do proxecto**
   - **Detalle da liña da oferta**
   - **Sobreprezo do prezo da función**
   - **Prezo do rol**
   - **Entrada de tempo**
 
   ![Engadir entidades existentes á solución de dimensións de prezos personalizada.](./media/Existing-entities-to-PD-solution.png)
 
 4. Para cada entidade, revise os compoñentes que se engaden e a lista final de activos da entidade para cada entidade. 

   >[!NOTE]
   > Inclúa todos os formularios e vistas para cada unha das entidades seleccionadas.

  ![Entidades engadidas.](./media/solution-component-selection.png)


5.  Cando se lle solicite que inclúa entidades dependentes para as entidades seleccionadas, seleccione **Non, non incluír os compoñentes necesarios.**

    ![Inclusión de entidades dependentes.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]