---
title: Custos e ingresos de proxecto
description: Este tema fornece información sobre a estimación de custos e ingresos dos proxectos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: fe51af8adb7c3831a57494b8359def2a0176b552efe16feb53a2a265f5ffcb0c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002554"
---
# <a name="project-costs-and-revenue"></a>Custos e ingresos de proxecto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As estimacións de proxecto fornecen a visualización financeira para o traballo estimado e programado na programación do proxecto. O separador **Estimacións** da páxina **Proxectos** mostra o impacto nos custos e ingresos do traballo que está a planificar. Tamén ofrece información sobre moitas dimensións predefinidas. 

> ![Separador Estimacións.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Valores de custo e vendas do proxecto

As listas de prezo definen as taxas de custo e facturación nun proxecto. Pode determinar o custo e o impacto nos ingresos do traballo, en función dos roles asociados ao nome do posto e ao recurso nomeado que está asignado a unha tarefa. Se hai tarefas que non teñen atribucións (xenéricas ou nomeadas), non pode obter estimacións de custos nin de vendas. Os valores de custos e vendas consideran a data que se define nas listas de prezos.

### <a name="default-cost-price"></a>Prezo de custo predefinido  

Todos os proxectos pertencen a unha organización. Esta organización móstrase no campo **Unidade contratante** no proxecto. A lista de prezos que está asociada á unidade contratante úsase para determinar o prezo unitario. Para determinar os prezos de custo correctos nos roles para a data que se define nas liñas de estimación, busque a combinación de rol, unidade e unidade organizativa na lista de prezos de custo. 

Para que se poidan calcular os seus prezos de custo, todas as tarefas deben estar atribuídas a un recurso. Todas as tarefas non asignadas terán un prezo de custo de 0,00.

Se a combinación de rol, unidade e unidade organizativa non devolve un prezo de custo da lista de prezos da unidade contratante, o sistema ignora a unidade. No seu lugar, busca a combinación de só rol e unidade organizativa. Se se atopa un prezo de custo, úsanse factores de conversión para convertelo á unidade que seleccionou na liña de estimación.

Se a combinación de rol, unidade e unidade organizativa non devolve un prezo de custo da lista de prezos, o sistema ignora a unidade contratante. No seu lugar, busca a combinación de rol e unidade para establecer o prezo por defecto (despois de aplicar calquera conversión).

Se o sistema non atopa un prezo para o rol, logo o prezo de custo na liña de estimación establécese nun valor por defecto de **0,00**. Todas as cantidades de custo nas liñas de estimación de custo do proxecto se rexistran na moeda da unidade contratante.

> [!NOTE]
> Por defecto, Microsoft Dynamics 365 garda as cantidades de custos na súa moeda base. Non obstante, as cantidades de custo que se amosan no separador **Estimacións** están na moeda da unidade contratante.  

### <a name="default-sales-price"></a>Prezo de vendas predefinido 

A lista de prezos de vendas está determinada pola entidade de vendas á que se anexa o proxecto ou polo cliente do proxecto. Cando unha entidade de vendas, como oportunidade, oferta ou contrato, está asociada ao proxecto, o prezo de vendas da entidade de vendas está determinado pola lista de prezos que está asociada á oferta ou ao contrato. Se a oferta ou o contrato teñen unha lista de prezos personalizada, esa lista de prezos utilízase como a lista de prezos de vendas predefinida para as estimacións de proxecto. Se non hai asociación a entidades de vendas, a lista de prezos de vendas predefinida a partir dos parámetros úsase como a lista de prezos de vendas predefinida correspondente á moeda do cliente que se define no proxecto.

Cada liña de estimación ten unha unidade de recursos que está asociada a ela. A unidade de recursos indica a unidade organizativa da que se reservan recursos para completar a tarefa. Para determinar o prezo de vendas dos roles asociados, busque a combinación de rol, unidade e unidade de recursos na lista de prezos de vendas. Se non hai atribucións na tarefa, o prezo de vendas para a tarefa é 0,00.

Se a combinación de rol, unidade e unidade de recursos non devolve un prezo de vendas da lista de prezos de vendas, o sistema ignora a unidade. No seu lugar, busca a combinación de só rol e unidade de recursos. Se se atopa un prezo de vendas, úsanse factores de conversión para convertelo á unidade que seleccionou na liña de estimación de vendas. 

Se a combinación de rol e unidade de recursos non devolve un prezo de vendas da lista de prezos de vendas, o sistema ignora a unidade de recursos. No seu lugar, busca a combinación de rol e unidade para establecer o prezo por defecto (despois de aplicar calquera conversión).

Se o sistema non atopa un prezo para o rol, logo o prezo de vendas na liña de estimación establécese nun valor por defecto de **0,00**.

O separador **Estimacións** ten unha vista de grade que amosa liñas de estimación. A grade inclúe columnas para a unidade, prezo total de custo e prezo total de vendas, como se mostra na seguinte ilustración. 

> ![Vista de grade no separador Estimacións.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Visualización en fase de tempo das estimacións de proxecto

A visualización de fase de tempo das estimacións do proxecto mostra os datos de estimación da vista de grade a través da liña de tempo, nunha escala de tempo que seleccione. Por defecto, os datos de estimación pivotan na dimensión **Rol**.

> ![Visualización de fase de tempo para as estimacións de proxecto.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Asignación de esforzo estimado baseada no modo de tarefa

Na visualización de fase de tempo, vostede distribúe o esforzo total que se estima para a tarefa distribúese atribuíndo un número de horas de esforzo por unidade de tempo na escala de tempo seleccionada. O modo de tarefa determina como se atribúe o esforzo na duración da tarefa. Os dous tipos de atribución son **Uniforme** e **Baseada en horas laborables**.

### <a name="work-hours-based-allocation"></a>Atribución baseada en horas laborables
 
No modo de tarefa de programación automática, as horas predefinidas diarias dos recursos de tarefas establécense na taxa de hora completa do traballo. Este comportamento aplícase ao atribuír o esforzo dividíndoo pola duración da tarefa tamén na visualización de fases de tempo. Por exemplo, se estima que unha tarefa vai ser concluída por un recurso na escala de tempo **Día**, o esforzo atribuído por día non superará as horas laborables por día definidas no calendario de proxecto. Por tanto, a atribución de esforzo sempre garante que as estimacións dos recursos se usen o día completo.

### <a name="even-allocation"></a>Atribución uniforme

No modo de tarefa programado manualmente, non se usan as horas laborables do calendario do proxecto. No seu lugar, a programación de tarefa está baseada na información de usuario. Para estas tarefas, a atribución do esforzo por período de tempo unitario da escala temporal seleccionada non ten ningún factor limitante. O esforzo total na tarefa está dividido equitativamente e atribuído para cada período de tempo unitario da escala temporal seleccionada. Polo tanto, o modo de tarefa definido na tarefa determina a distribución do esforzo ou a atribución do esforzo por período de tempo unitario nas estimacións de fases de tempo.

## <a name="grouping-and-time-phasing-options"></a>Opcións de agrupamento e fases de tempo

Esta visualización de fase de tempo mostra a distribución do esforzo, o custo e as estimacións de vendas por día, semana, mes ou ano. Por defecto, os datos de estimación pivotan na dimensión **Rol**. Non obstante, pode usar a opción **Agrupar por** para pivotar sobre outras dúas dimensións: **Categoría** e **Recurso**.

Tanto na vista de grade como na visualización de fase de tempo, pode seleccionar que campos se mostran. Os totais de cada bloque de tempo móstranse na parte inferior do proxecto. Amosan o esforzo, o custo e as vendas estimadas totais para o día, semana, mes ou ano. O prezo de custo e o prezo de vendas predefinidos son efectivos nunha data. Noutras palabras, cambian para cada recurso, en función da visualización de fase de tempo que selecciona.

## <a name="expense-estimates"></a>Estimacións de gastos

O botón **Engadir unha nova estimación de gasto** da vista de grade permítelle rexistrar todos os gastos que se produzan no proxecto, pero que non están directamente relacionados co traballo. Pode rexistrar as estimacións de gastos para unha tarefa específica ou para todo o proxecto. Seleccione as categorías de gastos e a data na que ten previsto incorrer no gasto. Se a lista de prezos de custo e a lista de prezos de vendas asociadas teñen os prezos predefinidos (ou porcentaxes de sobreprezo definidos para categorías de gastos), introdúcense automaticamente na liña de estimación en asociación cando se produce a asociación.


[!INCLUDE[footer-include](../includes/footer-banner.md)]