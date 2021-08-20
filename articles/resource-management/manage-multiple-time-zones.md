---
title: Xestionar fusos horarios
description: Cando se crea un proxecto, o seu fuso horario baséase no fuso horario definido no modelo de hora de traballo aplicado.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d3fc0453e3038839107a98c4179e6bd4aede95cf4a5fcfe2d52f823b83029485
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988694"
---
# <a name="manage-time-zones"></a>Xestionar fusos horarios

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


## <a name="projects"></a>Proxectos

Cando se crea un proxecto, o fuso horario baséase no fuso horario definido no modelo de hora de traballo aplicado. En **Proxecto**, as datas son sempre relativas ao fuso horario do usuario que iniciou sesión en cada separador, agás o separador **Tarefa**. Cando vexa a estrutura de subdivisión do traballo, as datas sempre se amosarán no fuso horario do proxecto.

## <a name="tasks"></a>Tarefas

Cando se crea unha tarefa, a hora de inicio, a hora de finalización e as horas/día están controladas polas horas de traballo do proxecto. Por exemplo, se se crea unha tarefa cun proxecto cuxo fuso horario é -8 PST e ten o seguinte horario de traballo: de 9:00 a 17:00 de luns a venres, calquera tarefa creada sen unha atribución respectará a hora de inicio e hora de finalización do calendario do proxecto.

## <a name="manage-resources-with-time-zones"></a>Xestionar recursos con fusos horarios

Para obter resultados precisos e predicibles ao usar **Ampliar reserva**, hai dous requisitos previos clave que deben cumprirse:  

- O usuario debe configurar o fuso horario do seu dispositivo para que coincida co fuso horario definido no sistema **Configuración de personalización**.
 
  ![Configuración do fuso horario en Windows 10.](media/reconcile-assignments-03.png)

  ![Configuración do fuso horario na configuración de personalización.](media/reconcile-assignments-04.png)
 
- O recurso reservable debe ter polo menos un minuto de tempo de traballo que se superpón cos contornos que se empregan para definir a extensión solicitada. Por exemplo, os seguintes recursos con horario de traballo comprendido entre as 9:00 e as 19:00. 

  ![Comparación de contornos de recursos.](media/reconcile-assignments-05.png)

A seguinte táboa mostra:

- Un modelo de calendario do proxecto
- Recurso A: Este recurso ten o mesmo calendario e está no mesmo fuso horario que o proxecto. A hora de inicios das reservas será ás 9:00.
- Recurso B: Este recurso está situado nun fuso horario diferente do proxecto e comeza ás 7:00 AM no seu fuso horario. Non obstante, as reservas comezarán ás 9:00 xa que esa é a hora de inicio máis temperá do contorno da tarefa.
- Recursos C e D: Os recursos localízanse en diferentes fusos horarios, ambos diferentes entre si e do proxecto, e as súas reservas non comezan antes das respectivas horas de inicio dispoñibles.

|Entity  |Calendario  |
|-|-|
|Modelo de calendario do proxecto   | ![calendario do proxecto.](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendario do recurso A.](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendario do recurso B.](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendario do recurso C.](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendario do recurso D.](media/reconcile-assignments-09.png)  |
 
Cando navegue á vista **Conciliación**, móstranse as atribucións de recursos e as carencias de reservas asociadas.

![Vista de conciliación antes da extensión.](media/reconcile-assignments-10.png)

Despois de que se empregou a funcionalidade de ampliación de reservas para cada recurso, as reservas amplíanse con éxito para cada recurso porque as horas de traballo de cada recurso superpuxéronse aos contornos da escaseza.

![Vista de conciliación despois da extensión da reserva.](media/reconcile-assignments-11.png) 

Teña en conta que unha ollada máis atenta aos detalles das reservas mostra diferenzas na hora de inicio das reservas. As reservas comezan non antes da hora de inicio do contorno da atribución nin antes da hora de inicio dispoñible do recurso.

![Novas reservas dos recursos no panel de programación.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]