---
title: Reservar recursos nomeados a partir de requisitos de recursos
description: Este artigo ofrece información sobre como reservar recursos con nome para un requisito de recursos xenéricos.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916240"
---
# <a name="book-named-resources-from-resource-requirements"></a>Reservar recursos nomeados a partir de requisitos de recursos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode reservar un recurso nomeado para substituír un recurso xenérico que teña un requisito de recursos.

1. En Project Service Automation (PSA), na páxina **Proxectos** prema no separador **Equipo**.
2. Seleccione o recurso xenérico que ten un requisito de recursos da lista e logo prema en **Reservar**. Ou abra o requisito de recursos e logo prema en **Reservar**.


![Reserva dun membro xenérico do equipo.](media/RM-how-to-14.png)


3. Na páxina **Asistente de programación**, seleccione un recurso nomeado para reservar no seu equipo de proxecto e logo prema en **Reservar**.

![Reserva dun membro xenérico do equipo usando o asistente de programación.](media/RM-how-to-15.png)

Cando a reserva está completa e cumprida por un recurso nomeado, o recurso xenérico substitúese polo recurso nomeado.

![O membro nomeado do equipo substitúe a un membro xenérico do equipo.](media/RM-how-to-16.png)

As asignacións do programa actualízanse co recurso nomeado tamén.

![Membro do equipo nomeado asignado ás tarefas do proxecto.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Cumprir un recurso xenérico con varios recursos nomeados
Cumprir un requisito para un recurso xenérico con varios recursos nomeados é similar a asignar un único recurso nomeado. Por exemplo, hai unha tarefa cunha duración de cinco días e 120 horas de esforzo. Esta tarefa non se pode completar cun recurso que traballa un día típico de oito horas durante unha semana de cinco días. 

![Unha tarefa que necesita 120 horas de esforzo ao longo de cinco días.](media/RM-how-to-21.png)

O requisito é de 120 horas de enxeñería robótica durante cinco días, é dicir, 24 horas ao día.

![Requisito por día.](media/RM-how-to-22.png)

Este é un exemplo de cando se necesitan varios recursos nomeados para cumprir unha solicitude de recursos xenéricos. Deberá reservar varios recursos para cumprir o requisito.

![Reservar varios recursos para cumprir o requisito.](media/RM-how-to-23.png)

A principal diferenza neste escenario é que o recurso xenérico permanece no equipo asignado á tarefa e os membros do equipo de recursos nomeados reservados non se asignan como parte do posto. O xestor do proxecto pode atribuír o traballo segundo corresponda aos recursos nomeados. A vista **Reconciliación** pode axudar a un xestor de proxectos a dividir as reservas entre varios recursos para a asignación de tarefas. Isto non se fai de xeito automático porque en calquera escenario máis complicado que o simple exemplo anterior, como cando hai un paquete de tarefas que conforman o requisito, a intención de como o xestor de proxectos quere atribuír debe ser asumida polo sistema. Debido a que o sistema non pode entender a intención, é probable que as suposicións sexan diferentes do previsto e se produza un resultado incorrecto ou imprevisible. O resultado previsible é que o recurso xenérico permaneza asignado ata que o responsable do proxecto cree asignacións deliberadamente, coa asistencia da vista **Reconciliación**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
