---
title: Ver a utilización imputable de recursos
description: Este tema fornece información sobre a vista de utilización de recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122161"
---
# <a name="view-chargeable-utilization-for-resources"></a>Ver a utilización imputable de recursos
 
A **Vista de utilización** na páxina **Utilización de recursos de Project Service** a páxina mostra a utilización imputable por cada recurso reservable. Porque a vista está baseada no panel de programación, de forma que atopará moitas das mesmas funcións.

> ![Captura da visualización de utilización](media/FAQ-utilization-1.png)
 

O cálculo da utilización imputable funciona da seguinte maneira:

   Utilización imputable = (Horas reais imputables) / (capacidade do recurso).

O celas representan a utilización imputable calculada para o período seleccionado (días, semanas ou meses).

As cores en cada cela mostrar a utilización imputable para un recurso comparada coa utilización imputable de destino. 

A utilization de destino pódese definir no rol predefinido do recurso ou no recurso individual. O cálculo busca no individual o destino en primeiro lugar e, a seguir, no rol predefinido do recurso.

## <a name="set-target-on-a-resource"></a>Establecer o destino nun recurso

1. Vaia a **Recursos** \> **Recursos**. 
2. Seleccione un recurso para abrir o rexistro. 
3. No separador **Project Service**, pode definir a utilización obxectivo do recurso.

> ![Captura de utilizar o separador Project Service para definir a utilización de destino](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Estableza a utilización obxectivo nun rol

1. Vaia a **Recursos** \> **Roles de recursos**. 
2. Seleccione un rol e abra o rexistro. 
3. Defina a utilización de destino para o rol.

> ![Captura de utilizar os roles de recursos para definir a utilización de destino](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calcular a utilización imputable dun recurso

Para calcular a utilización imputable para un recurso, terá que cumprir algúns requisitos previos. 

### <a name="set-default-role-for-individual-resource"></a>Estableza o rol por defecto para cada recurso individual

En primeiro lugar, a utilización obxectivo debe definirse no recurso individual ou nos roles do recurso. Se está a usar roles de recursos para destinos, cada recurso individual debe ter un rol predefinido. 

1. Para definir isto, vaia a **Recursos** \> **Recursos**. 
2. Seleccione un recurso, abra o rexistro e logo seleccione o separador **Project Service**. 
3. Na grade **Rol do recurso**, comprobe que hai un rol para o recurso e que **É predefinido** está configurado en **Si**.
 
### <a name="change-billing-type-for-resource-role"></a>Cambiar tipo de facturación deste rol do recurso

Os roles de recurso deben definirse para ter un tipo de facturación **Imputable**. 

1. Vaia a **Recursos** \> **Roles de recursos**. 
2. Abra o rexistro que quere actualizar e, a seguir, defina o tipo de facturación predefinido en **Imputable**.

### <a name="set-working-hours-for-resource-role"></a>Definir as horas laborables para o rol de recurso
 
O recurso debe ter horas de traballo para o cálculo de capacidade. 

1. Vaia a **Recursos** \> **Recursos**. 
2. Seleccione un recurso para abrir o rexistro e, a seguir, seleccione **Mostrar horas laborables**. 
3. Pode actualizar en masa a lista de recursos aplicándolles un **Modelo de horas de traballo** desde a visualización de **Lista de recursos**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Resolución de problemas de horas reais imputables

As horas reais imputables orixínanse da entidade **Valores reais**. Os valores reais co tipo de facturación **Imputable** están incluídos no cálculo e, por este motivo, debe ter proxectos onde os valores reais son imputables.

Se non está a ver a utilización imputable, ofrecémoslle algunhas cousas pode comprobar:

- O recurso ten horas laborables definidas para a capacidade.
- O recurso ten en un destino de utilización individualmente definido ou ten un rol predefinido atribuído. O rol ten un destino de utilización definido.
- Os valores reais teñen un tipo de facturación **Imputable** para o período do que espera un cálculo de utilización. Comprobe o seguinte se está a ver os valores reais con tipos de facturación que non sexan imputables:

  - O rol utilizado no valor real ten un tipo de facturación predefinido que non é imputable.
  - O rol na liña de contrato do proxecto que fai de copia de seguranza do proxecto está definido en non imputable.
  - O proxecto non ten unha liña de contrato asociada.

