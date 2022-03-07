---
title: Determinar o custo e ingresos estimados dun proxecto
description: Como determinar estimacións de custos e ingresos do proxecto en Project Service
author: ruhercul
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 38de99680f4ba67b8eb593ec575c2a796fcfb59436fea5323dd1d86d7cf3d797
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002599"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Determinar o custo e ingresos estimados dun proxecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

As estimacións de proxecto fornecen a visualización financeira para o traballo estimado e programado na estrutura de subdivisión do traballo. A visualización de estimacións indica o impacto do custo e ingresos do traballo planificado. A visualización de estimacións fornece unha ferramenta para ver a información nun número de dimensions predefinidas para informar mellor do impacto financeiro do proxecto.  
  
## <a name="cost-and-sales-value-of-the-project"></a>O valor do custo e vendas do proxecto  
As listas de prezo do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definen as taxas de custo e facturación para roles que usan os proxectos. Segundo os roles asociados a tarefas na estrutura de subdivisión do traballo do proxecto, pode determinar o impacto do custo e os ingresos do traballo.  
  
## <a name="cost-price-defaulting"></a>Predeterminación do prezo de custo  
Cada proxecto pertence a unha organización (indicada na **Unidade Propietaria** do proxecto). A lista de prezos asociada coa unidade da organización propietaria determina o prezo de custo da unidade. A [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determina os prezos de custo dos roles buscando a combinación de role, unidade e unidade de organización na lista de prezos de custo para obter o prezo de custo correcto para a data efectiva nas liñas de estimación.  
  
Se a combinación de rol, unidade e unidade da organización non teñen como resultado un prezo de custo da lista de prezos da unidade propietaria, a unidade exclúese en favor da combinación de rol e unidade de organización. Se hai un prezo de custo, convértese á unidade que escolle na liña de estimación.  
  
Se a combinación de rol e unidade da organización non provoca un prezo de custo, a unidade da organización queda excluída en favor dunha combinación de rol e unidade, e o prezo é o predeterminado despois de aplicar unha conversión, se é necesario.  
  
 Se non existe un prezo para o rol, logo o prezo de custo é por defecto 0,00 na liña de estimación.  
  
 Todas as cantidades de custo nas liñas de estimación de custo do proxecto están na moeda da unidade da organización propietaria.  
  
## <a name="sales-price-defaulting"></a>Predeterminación do prezo de vendas  
A lista de prezos de vendas está baseada na entidade de vendas á que está anexado o proxecto. A lista de prezos de vendas asociada coa oferta ou co contrato determina o prezo de vendas da unidade. Se a oferta ou o contrato teñen unha lista de prezos personalizada, esta é a lista de prezos de vendas predefinida para as estimacións de proxecto. Se non hai ningunha asociación ás entidades de vendas, logo a lista de prezos de vendas configurada en parámetros será a lista de prezos de vendas predefinida do proxecto. Cada liña de estimación ten unha unidade de organización de recurso asociada para indicar a unidade de organización na que se reservan os recursos para concluír a tarefa. O prezo de vendas para os roles asociados está determinado pola combinación de rol, unidade e unidade de organización de recurso na lista de prezos de vendas para obter o prezo de vendas correcto para a data efectiva nas liñas de estimación.  
  
Se a combinación de rol, unidade e unidade de organización de vendas non provoca un prezo de vendas na lista de prezos de vendas, o sistema ignorará a unidade e buscará a combinación de rol e unidade de organización de recursos. Se se atopa un prezo de vendas, convértese á unidade que vostede escolla na liña de estimación de vendas.  
  
Se o sistema non atopa un prezo para o rol, logo o prezo de vendas é por defecto 0,00 na liña de estimación.  
  
A visualización de estimacións ten unha visualización de grade que mostra unha grade das liñas de estimación con unidade e custo total e prezo de venda.  
  
## <a name="time-phased-view-of-project-estimates"></a>Visualización en fase de tempo das estimacións de proxecto  
Na visualización en fase de tempo para estimacións de proxecto, os datos de estimación da visualización de grade é vertical por defecto por rol, e mostra os datos de estimación na liña de tempo na escala temporal escollida.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Atribución estimada de esforzo baseadae no modo de tarefa  
Na visualización de fase de tempo, o esforzo total estimado para a tarefa distribúese atribuíndo un número de horas de esforzo por unidade de tempo da escala temporal escollida. En Project Service, o modo de tarefa determina como se atribúe o esforzo na duración da tarefa. Os dous tipos de atribución son atribución baseada en horas laborables e atribución uniforme. 
  
## <a name="work-hours-based-allocation"></a>Atribución baseada en horas laborables  
O modo de tarefa de programación automática para unha tarefa estipula que para o número de recursos estimados na tarefa, estímase que se usen durante todas as horas laborables por día. Isto aplícase ao atribuír o esforzo dividíndoo pola duración das tarefas tamén na visualización de fases de tempo. Por exemplo, nunha escala temporal 'Día', para unha tarefa que se estima vai ser concluída por un recurso, o esforzo atribuído por día non superará as horas laborables por día definidas no calendario de proxecto. Por tanto, a atribución de esforzo sempre asegura que as estimacións dos recursos se usen o día completo.  
  
## <a name="even-distribution"></a>Distribución uniforme  
O modo de tarefa programada manualmente non respecta as horas laborables, o calendario do proxecto ou o número de recursos definidos na tarefa. A programación de tarefa está baseada na información de usuario. Para estas tarefas, a atribución do esforzo por período de tempo unitario da escala temporal escollida non ten ningún factor limitante. O esforzo total na tarefa está dividido equitativamente e atribuído para cada período de tempo unitario da escala temporal escollida.  
  
Deste modo, o modo de tarefa definido na tarefa determina a distribución do esforzo ou a atribución do esforzo por período de tempo unitario nas estimacións de fases de tempo.  
  
## <a name="grouping-and-time-phasing-options"></a>Opcións de agrupamento e fases de tempo  
Esta visualización axuda a entender a distribución do esforzo, o custo e as estimacións de vendas por día, semana, mes ou ano. A opción Agrupar por permite poñer en vertical as estimacións de datos en dúas dimensions diferentes: categoría e recurso. Tanto na visualización de grade como na visualización de fase de tempo pode escoller os campos que se mostran. Os totais para cada un dos bloques de tempo móstranse na parte inferior indicando o esforzo total estimado, custo e vendas para o día, semana, mes ou ano.  
  
O prezo de custo e o prezo de vendas predefinidos son efectivos nunha data. Cando as taxas para os roles se cambian, estarán máis transparentes na visualización de fases de tempo ao visualizar datos de estimación en vertical en 'Recurso' e fases de tempo por semana.  
  
## <a name="expense-estimates"></a>Estimacións de gastos  
Calquera gasto do proxecto que non está directamente relacionado co traballo que se pode gastar pode rexistrarse na estimación do proxecto na visualización de grade. Utilizando a opción **Engadir estimación de gasto** na visualización de grade, pode obter isto. As estimacións de gastos poden rexistrarse para unha tarefa específica ou para todo o proxecto. Pode escoller categorías de gasto nestas liñas e escoller unha data provisional cando se espera que se incorra no gasto. Se a lista de prezos de vendase e custo asociada ten os prezos predefinidos ou porcentaxes de sobreprezo definidos para categorías de gastos, volverá ao valor predefinido na liña de estimación en asociación.  
  
### <a name="see-also"></a>Consulte tamén  
 [Guía do xestor de proxectos](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]