---
title: Crear solucións personalizadas para as dimensións de prezos
description: Este tema explica como crear unha solución personalizada ao crear dimensións de prezos personalizadas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284986"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Crear solucións personalizadas para as dimensións de prezos

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Todos os cambios de dimensións de prezos personalizadas deberían estar nunha solución separada. Esta importante boa práctica proporciona flexibilidade no futuro para actualizar ou eliminar os cambios segundo sexa necesario, axudará á reutilización do seu traballo e facilita levar estes cambios a outra instancia. Despois de facer os cambios necesarios, exporte esta solución como **Solución xestionada** e impórtea a outras instancias para reutilizar a súa configuración de prezos.

1. Seleccione **Configuración** > **Solucións** e logo seleccione **Nova**. 
2. Poña nome á solución, **\<your organization name> dimensións de prezos**, introduza a información restante necesaria e logo seleccione **Gardar**.

> ![Creación dunha solución personalizada para as dimensións de prezos](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Engadir todas as entidades requiridas e os compoñentes relacionados á solución de dimensión de prezos
Terá que engadir as seguintes entidades de Project Service á súa solución de prezos. Complete os pasos deste procedemento para facer algúns cambios importantes do esquema na solución de prezos para que as entidades teñan coñecemento das novas dimensións de prezos.

1. Seleccione **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Engadir existente** > **Entidades**.
3. Na caixa de diálogo **Compoñentes da solución**, seleccione as seguintes entidades:

- Dato real
- Recurso reservable
- Liña de estimación
- Tarefa do proxecto
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

4. Cando se lle solicite incluír calquera entidade dependente para as entidades seleccionadas, seleccione **Non**.

> ![Non incluír todos os compoñentes relacionados](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]