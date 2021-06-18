---
title: Conciliar reservas e atribucións
description: Neste tema se proporciona información sobre datos reais.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 73cbc89ae4350cbd568f1bb978825ff53da07afb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008894"
---
# <a name="reconcile-bookings-and-assignments"></a>Conciliar reservas e atribucións

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As reservas de proxectos dun membro do equipo de proxecto e as atribucións de tarefas están emparelladas libremente. Polo tanto, un recurso pode ter tarefas que non corresponden ás reservas e reservas que non correspondan ás atribucións de tarefas. O ideal é que as reservas e atribucións do proxecto estean aliñadas, de xeito que os recursos teñan capacidade comprometida para realizar as súas atribucións de tarefas. Non obstante, a realidade é que as reservas poden ocorrer en función da dispoñibilidade, e os calendarios de tarefas poden cambiar a medida que o proxecto continúa durante o seu ciclo de vida. Polo tanto, o emparellamento libre permite flexibilidade.

Por mor do emparellamento libre de reservas de proxectos e atribucións de tarefas, o separador **Conciliación** está incluído na entidade Proxecto. Este separador axuda aos xestores de proxectos concilien as reservas dos membros do equipo e as súas atribucións para o seu equipo de proxecto.

Para cada membro nomeado do equipo, o separador **Conciliación** mostra reservas e atribucións ata o nivel da tarefa individual para cada membro do equipo. Amosa horas en celas que poden representar períodos de tempo desde meses ata días.

No campo **Escala de tempo**, pode seleccionar **Mes**, **Semana** ou **Día**. Por defecto está seleccionado **Semana**. Non obstante, pode cambiar o valor por defecto seleccionando o botón **Configuración**. Cando se abre o separador **Conciliación**, amosa a data actual, pero pode usar o control de calendario para avanzar ou retroceder no tempo. Cando un proxecto ten unha data de inicio que está no futuro, o separador mostra esa data cando se abre. O control de calendario tamén ten opcións que permiten pasar ás datas de inicio e finalización do proxecto.

Pode usar os controis de expansión de cada recurso para amosar os detalles das reservas dese recurso. Tamén pode ampliar as asignacións de cada recurso ao nivel da tarefa individual.

A parte inferior do separador **Conciliación** mostra un total neto global do proxecto, e o separador tamén inclúe unha columna total. Para cada recurso, o separador toma a diferenza entre as reservas do membro do equipo no proxecto e un resumo das atribucións dese membro do equipo. O ideal sería que a diferenza fose 0 (cero). Noutras palabras, non debería haber ningunha diferenza entre reservas e atribucións de tarefas do recurso. As diferenzas indícanse por cor e sombreado para indicar dúas condicións:

- **Escaseza de reservas** - A escaseza de reservas prodúcese cando un recurso ten máis atribucións que reservas. Debido a que non se reservou esta capacidade, un xestor de proxectos pode corrixir esta condición ampliando as reservas do recurso para cubrir a escaseza.
- **Exceso de reservas** - O exceso de reservas prodúcese cando se reservou un recurso para o proxecto pero non foi asignado a tarefas. Esta condición podería ser aceptable se, por exemplo, o recurso é reservado antes de que se produza a atribución de tarefas. Non obstante, noutros casos, podería non estar previsto atribuír tarefas ao recurso. Nestes casos, o xestor do proxecto debería considerar a cancelación das reservas do recurso, de xeito que a capacidade poida utilizarse para outro proxecto.

> [!NOTE]
> A lenda destas condicións pode estar oculta para deixar máis espazo para a grade. Neste caso, pode facer visible a lenda seleccionando o botón **Configuración**.

Nalgúns casos, cando o campo **Escala de tempo** está definido nun nivel superior a **Día**, pódense calcular as diferenzas como 0 (cero). Por exemplo, no nivel **Mes**, a diferenza neta para un recurso podería ser 0 (cero) para indicar que as reservas son iguais ás atribucións. Non obstante, se ve o tempo a nivel de **Semana**, é posible que vexa que hai atribucións de 0 (cero) horas e reservas de 40 horas na primeira semana do mes, pero atribucións de 40 horas e reservas de 0 (cero) horas na segunda semana do mes. Aínda que as reservas e as tarefas totais para o mes son iguais, difiren por semana.

Cando vexa o tempo a niveis de tempo máis altos, as celas do separador **Conciliación** mostra un indicador de cela para informar de que hai diferenzas a niveis de tempo máis baixos. Por exemplo, na seguinte ilustración, un indicador de cela aparece na cela para o mes de outubro de 2018 para o recurso que leva o nome de Lúa Hervés. Polo tanto, pode ver que, a pesar de que as reservas e atribucións do recurso son iguais cando se agroman no nivel **Mes**, non coinciden en niveis máis baixos.

![Reservas e atribucións non coincidentes a nivel mensual](media/reconcile-assignments-01.JPG)

Prema dúas veces nunha cela para ampliar ao seguinte nivel inferior e vexa a diferenza. Por exemplo, se preme dúas veces sobre a diferenza de outubro de 2018 para Lúa Hervés, fai a busca ata o nivel **Semana**. Pode ver que o recurso ten reservas de 16 horas pero non hai tarefas nas dúas primeiras semanas de outubro, e 16 horas de tarefas pero non ten reservas na terceira semana de outubro.

![Reservas e atribucións non coincidentes a nivel semanal](media/reconcile-assignments-02.JPG)

Pode premer co botón dereito sobre unha cela para ampliar o seguinte nivel superior. Tamén pode desactivar o indicador de cela seleccionando o botón **Configuración**. 

Tamén pode usar os botóns **Anterior** e **Seguinte** por riba da grade para moverse por todas as diferenzas no seu proxecto. Para usar estes botóns, primeiro debe seleccionar un recurso. Seleccione **Seguinte** para ir á seguinte diferenza entre reservas e atribucións para ese recurso. Seleccione **Anterior** para ir á diferenza anterior.

En situacións nas que ten atribucións de tarefas para un recurso pero non ten reservas, na páxina Proxectos, pode seleccionar a escaseza de reservas e logo seleccionar **Estender a reserva**. Podes ver a reserva que é necesaria para atallar a escaseza do recurso. Tamén pode ver as reservas do recurso no proxecto actual e noutros proxectos. Seleccione **Aceptar** para crear a reserva para o recurso independentemente da dispoñibilidade actual. O xestor de proxectos ou xestor de recursos pode utilizar o panel de programación para xestionar calquera situación na que un recurso estea sobrecargado fóra da súa capacidade porque se estenderon as súas reservas.

## <a name="managing-with-time-zones"></a>Xestión con fusos horarios
Para garantir resultados precisos e previsibles ao usar Estender reserva, deben cumprirse dous requisitos previos clave:  

- O usuario debe configurar o fuso horario do seu dispositivo para que coincida co fuso horario definido na Configuración de personalización do sistema.
 
  ![Configuración do fuso horario en Windows 10](media/reconcile-assignments-03.png)

  ![Configuración do fuso horario na configuración de personalización](media/reconcile-assignments-04.png)
 
- O recurso reservable debe ter polo menos un minuto de tempo de traballo que se superpón cos contornos que se empregan para definir a extensión solicitada. Por exemplo, o seguinte exemplo mostra os recursos de revisión cun horario de traballo que está entre as 9:00 e as 19:00. 

  ![Comparación de contornos de recursos](media/reconcile-assignments-05.png)

A seguinte táboa mostra:

- Un modelo de calendario do proxecto.
- Recurso A: Este recurso ten o mesmo calendario e está no mesmo fuso horario que o proxecto. A hora de inicios das reservas será ás 9:00.
- Recurso B: Este recurso está situado nun fuso diferente ao do proxecto e, polo tanto, comeza ás 7:00 no seu fuso horario. Non obstante, as reservas comezarán ás 9:00 xa que esa é a hora de inicio máis temperá do contorno da tarefa.
- Recursos C e D: Os recursos atópanse tamén en diferentes fusos horarios, diferentes entre si e do proxecto, e as súas reservas non comezan antes que as súas respectivas horas de inicio dispoñibles.

|Entidade  |Calendario  |
|-|-|
|Modelo de calendario do proxecto   | ![calendario do proxecto](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendario do recurso A](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendario do recurso B](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendario do recurso C](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendario do recurso D](media/reconcile-assignments-09.png)  |
 
Cando navegue á vista de reconciliación, mostraranse as asignacións de recursos e as escasezas de reservas asociadas.
 ![Vista de conciliación antes da extensión](media/reconcile-assignments-10.png)

Despois de executar a función Estender reserva en cada recurso, as reservas esténdense con éxito para cada recurso. Isto débese a que o horario de traballo de cada recurso se superpuxo aos contornos da escaseza.
 ![Vista de conciliación despois da extensión da reserva](media/reconcile-assignments-11.png) 

Non obstante, unha ollada máis atenta aos detalles das reservas mostra diferenzas na hora de inicio das reservas. As reservas non comezarán antes da hora de inicio do contorno de asignación nin antes da hora de inicio dispoñible do recurso.
 ![Novas reservas dos recursos no panel de programación](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]