---
title: Grupos de unidades e unidades
description: Este artigo fornece información sobre os grupos de unidades e as unidades.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: ed413cc927901308a111263dbad1a59af8fce620
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933398"
---
# <a name="unit-groups-and-units"></a>Grupos de unidades e unidades

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os grupos de unidades e as unidades son entidades básicas en Microsoft Dynamics 365. Unha unidade é unha única unidade de medida e pódense agrupar varias unidades en grupos de unidades. Ás veces a un grupo de unidades chámaselle un programa de unidades na interface de usuario (IU) de Dynamics 365. 

Este son algúns exemplos de unidades e grupos de unidades:
 
- **Grupo de unidades**: Distancia 
    - **Unidades**: Milla, quilómetro, etc.
- **Grupo de unidades**: Tempo
    - **Unidades**: Hora, día, semana, etc. 

Cando configure varias unidades nun grupo de unidades, tamén debe configurar un factor de conversión entre elas designando a primeira unidade que configurou como unidade predefinida ou principal para o grupo de unidades. 

Por exemplo, no grupo de unidades **Tempo**, se configura **Hora** como primeira unidade, o sistema designa **Hora** como unidade predefinida. Se a seguinte unidade que configurou é **Día**, debe configurar un factor de conversión para **Día** a **Hora**. Se logo engade **Semana** como terceira unidade, ten que configurar un factor de conversión para **Semana** en termos de **Día** ou **Hora**. 

A seguinte imaxe mostra un exemplo de configuración para a unidade **Día**, onde o campo **Cantidade** mostra o número de horas que hai nun día e **Semana**, onde o campo **Cantidade** mostra o número de días que están nunha semana.

> ![Grupo de unidades: Páxina de información.](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Uso das unidades e os grupos de unidades

Dynamics 365 Project Service Automation usa unidades e grupos de unidades para procesar estimacións e entradas tanto para gastos como para tempo. 

Para gastos, cada categoría de gasto ten un grupo de unidades e unha unidade por defecto. Estes valores introdúcense como valores predefinidos nas entradas de lista de prezos para categorías de gasto. 

Por exemplo, ten unha categoría de gasto que leva o nome **Quilometraxe**. Ten un grupo de unidades que leva o nome **Distancia** e unha unidade predefinida co nome **Milla**. Se configura o grupo de unidades **Distancia** para que teña dúas unidades ( **Milla** e **Quilómetro**), pode establecer dous prezos para a categoría **Quilometraxe** nunha lista de prezos: prezo por milla e prezo por quilómetro.

| Categoría de gasto  | Grupo de unidades  | Unidade      | Método de cálculo de prezos  | Prezo por unidade  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Quilometraxe           | Distancia      | Milla      | Prezo por unidade    | 10 USD            |
| Quilometraxe           | Distancia      | Quilómetro | Prezo por unidade    |  6 USD            |

Cando introduce un gasto nun proxecto, o sistema determina o prezo a través da combinación da categoría e a unidade no gasto. 

| Descrición de gasto        | Categoría de gasto  | Unidade  | Cantidade  | Prezo por unidade   |
|----------------------------|---------------------|-------|-----------|----------------|
| Conducir á localización do cliente | Quilometraxe             | Milla  | 10        | 10 USD         |

Para o tempo, cada cabeceira da lista de prezos ten un campo **Unidade de tempo por defecto**. O valor establécese ao crear a cabeceira da lista de prezos. Esta unidade úsase para establecer todos os prezos baseados en roles nesa lista de prezos.

As liñas de estimación para o campo **Tempo na oferta** pódense expresar en calquera unidade de tempo. Non obstante, as liñas de estimación dos proxectos e as entradas de tempo para os proxectos só poden usar a unidade de tempo **Hora**. Se a unidade na entrada de tempo ou a liña da estimación non coincide coa unidade da liña de lista prezos para ese rol, o sistema converte o prezo ás unidades definidas na estimación do proxecto ou na transacción real do proxecto.

O seguinte exemplo mostra como PSA usa o grupo de unidades, as unidades e os factores de conversión.
- Unidades

   - **Grupo de unidades**: Tempo 
   - **Unidades**: Hora 
    
    - **Día** - Factor de conversión: 8 horas       
    - **Semana** - Factor de conversión: 40 horas  
        
- Configuración da lista de prezos no proxecto A:

    - **Nome**: Prezos de vendas do Reino Unido 2016 
    - **Unidade de tempo predefinida**: Día 
    - **Moeda**: GBP

| Rol      | Grupo de unidades | Unidade | Unidade organizativa | Prezo   |
|-----------|------------|------|---------------------|---------|
| Programador | Time       | Day  | Contoso Reino Unido          | 800 GBP |

### <a name="time-entry"></a>Entrada de tempo

Na seguinte táboa móstrase a transacción de vendas resultante creada por PSA para un proxecto de tres horas.


| Proxecto   | Tarefa    | Rol      | Cantidade | Unidade  | Prezo por unidade | Importe de vendas sen facturar |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Proxecto A | Deseño  | Programador | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Preguntas frecuentes sobre a unidade de tempo

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>PSA converte a diferentes unidades no caso dos gastos?
Non. A conversión de unidades funciona só para o tempo. Para gastos, se o sistema non atopa un prezo para a combinación da categoría de gasto e a unidade, o prezo está fixado en 0,00 por defecto.

### <a name="why-does-psa-convert-time-units"></a>Por que PSA converte unidades de tempo?
Nalgúns países ou rexións, hai un requisito legal de que as taxas de facturación se establezan en días. A negociación de prezos e os descontos durante o ciclo da oferta realízase mediante tarifas de día para cada rol facturable. A estimación do programa e a entrada de tempo realízanse en horas. Para permitir esta diferenza de unidades de tempo, PSA converte unidades de tempo.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Pódense cambiar as unidades de tempo segundo as estimacións do proxecto?
Non. Actualmente a estimación do programa está restrinxida ás horas e non se pode cambiar.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Pódense editar, eliminar e engadir unidades e grupos de unidades?
Si. Con excepción do grupo de unidades **Tempo** e a unidade **Hora**, pódense eliminar ou editar todas as unidades e pódense engadir novas unidades. En PSA, o grupo de unidades **Tempo** e a unidade **Hora** non se poden eliminar. Non obstante, pódense actualizar cun texto traducido para o campo **Nome**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
