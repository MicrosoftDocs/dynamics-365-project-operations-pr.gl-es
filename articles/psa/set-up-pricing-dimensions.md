---
title: Configuración de campos personalizados como dimensións de prezos
description: Este tema fornece información sobre a configuración de dimensións de prezos personalizadas.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
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
ms.openlocfilehash: 9503b6528f91f86cc1ebe1c7ed6111171e74c4a3cbf83b3f68810c3ee5efdd28
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002329"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Configuración de campos personalizados como dimensións de prezos 

[!include [banner](../includes/psa-now-project-operations.md)]

Antes de comezar, este tema asume que completou os procedementos nos temas [Crear campos e entidades personalizados](create-custom-fields-entities.md) e [Engadir campos personalizados a configuración de prezos e entidades transaccionais](field-references.md). Se non completou eses procedementos, volva e compléteos e despois volva a este tema. 

Este tema fornece información sobre a configuración de dimensións de prezos personalizadas. Na interface web de Project Service, na páxina **Parámetros**, o separador **Dimensións de prezos baseados na cantidade** mostra os rexistros das entidades de dimensións de prezos. Por defecto, a instalación de Project Service crea 2 filas na grade neste separador:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Unidade organizativa)

> [!IMPORTANT]
> Non elimine estas filas. Non obstante, se non os precisa, pode facelos non aplicables nun contexto específico configurando **Aplicable ao custo**, **Aplicable ás vendas**, e **Aplicable á compra** como **Non**. Configurar estes valores do atributo como **Non** ten o mesmo efecto que non ter o campo como unha dimensión de prezos.

Para que un campo se converta nunha dimensión de prezos, debe:

- Crearse como campo nas entidades **Prezo de rol** e **Sobreprezo de rol**. Para obter máis información sobre como facer isto, consulte [Engadir campos personalizados á configuración de prezos e ás entidades transaccionais](field-references.md).
- Crearse como unha fila na táboa **Dimensión de prezos**. Por exemplo, engada filas de dimensións de prezos como se mostra no gráfico seguinte. 

![Filas de dimensións de prezos baseadas en importe.](media/Amt-based-PD.png)

Teña en conta que as horas de traballo dos recursos (**msdyn_resourceworkhours**) engadíronse como dimensión baseada en sobreprezo e engadíronse á grade no separador **Dimensión de prezos baseada en sobre prezo**.

![Filas de dimensión de prezos baseada en sobreprezo.](media/Markup-based-PD.png)

> [!IMPORTANT]
> Calquera cambio nos datos da dimensión de prezos desta táboa, xa existente ou nova, propágase á lóxica de negocio de prezos de Project Service só despois de actualizar a caché. A actualización da caché pode tardar ata 10 minutos. Agarde ese período de tempo ver os cambios na lóxica de establecemento de prezos predefinidos que debe resultar dos cambios nos datos da dimensión de prezos.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributos da táboa de dimensións de prezos
As seguintes seccións fornecen información sobre os distintos atributos da táboa **Dimensións de prezos**.

### <a name="pricing-dimension-name"></a>Tipo de dimensión de prezos
Este valor debe ser o mesmo que o nome do esquema do campo engadido á táboa **Prezo de rol** para dimensións de prezos personalizadas. Para obter máis información sobre como engadir campos á táboa **Prezo de rol**, consulte a táboa [Engadir campos personalizados á configuración de prezos e entidades transaccionais](field-references.md).

### <a name="type-of-dimension"></a>Tipo de dimensión
Hai dous tipos de dimensións de prezos:
  
  - **Dimensións baseadas en importe**: Os valores de dimensión do contexto de entrada fanse coincidir cos valores de dimensión da liña **Prezo de rol** o prezo/custo predefínese directamente a partir da táboa **Prezo de rol**.
  - **Dimensións baseadas en sobreprezo**: Estas son as dimensións nas que Project Service adoptará o seguinte proceso en 3 pasos para obter o prezo/custo
 
    1. Project Service fai coincidir os valores de dimensións non baseados en sobreprezo do contexto de entrada coa liña de prezo de rol para obter a taxa base.
    2. Project Service fai coincidir todos os valores de dimensións do contexto de entrada coa liña **Sobpreprezo de rol** para obter unha porcentaxe de sobreprezo.
    3. Project Service aplica a porcentaxe de sobreprezo do segundo paso á taxa base obtida da táboa **Prezo de rol** no primeiro paso para chegar ao prezo/custo final.
   
   A seguinte táboa ilustra o cálculo de sobreprezos.
  
| Rol        | Unidade organizativa    |Localización do traballo      |Título estándar      |Horas laborables do recurso      |  Sobreprezo|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Onsite            |                    |Horas extra                 |15     |
|             | Contoso India|Local             |                    |Horas extra                 |10     |
|             | Contoso EUA   |Local             |                    |Horas extra                 |20     |


Se un recurso de Contoso India cuxa taxa base é 100 USD está a traballar no sitio e rexistra 8 horas de tempo regular e 2 horas extraordinarias na entrada de tempo, o motor de prezos de Project Service empregará a taxa base de 100 durante as 8 horas para rexistrar 800 USD. Durante as 2 horas extraordinarias, aplicarase un 15 % de sobreprezo á taxa base de 100 para obter un prezo unitario de 115 USD e rexistrará un custo total de 230 USD.

### <a name="applicable-to-cost"></a>Aplicable a custo 
Se isto está definido en **Si**, indica que o valor da dimensión do contexto de entrada debe usarse para coincidir co **Prezo de rol** e o **Sobreprezo de rol** ao recuperar as taxas de custo e sobreprezo.

### <a name="applicable-to-sales"></a>Aplicable a vendas
Se isto está definido en **Si**, indica que o valor da dimensión do contexto de entrada debe usarse para coincidir co **Prezo de rol** e o **Sobreprezo de rol** ao recuperar as taxas de facturación e sobreprezo.

### <a name="applicable-to-purchase"></a>Como a compra
Se isto está definido en **Si**, indica que o valor da dimensión do contexto de entrada debe usarse para coincidir co **Prezo de rol** e o **Sobreprezo de rol** ao recuperar o prezo de compra. Na actualidade Project Service non admite escenarios de subcontratación, polo que este campo non se usa. 

### <a name="priority"></a>Prioridade
Establecer a prioridade de dimensión axuda a que os prezos de Project Service produzan un prezo incluso cando non pode atopar unha coincidencia exacta entre os valores da dimensión de entrada e os valores das táboas **Prezo de rol** ou **Sobreprezo de rol**. Neste escenario, Project Service empregará valores nulos para valores de dimensións non coincidentes ponderando as dimensións en orde da súa prioridade.

- **Prioridade de custos**: O valor da prioridade de custos dunha dimensión indicará o peso desa dimensión ao comparalo coa configuración dos prezos de custo. O valor de **Prioridade de custos** ten que ser único en todas as dimensións que sexan **Aplicables ao custo**.
- **Prioridade de vendas**: O valor da prioridade de vendas da dimensión indicará o peso desa dimensión ao comparalo coa configuración dos prezos de vendas ou taxas de facturación. O valor de **Prioridade de vendas** ten que ser único en todas as dimensións que sexan **Aplicables a vendas**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]