---
title: Atribuír recursos reservables xenéricos a unha tarefa e un equipo de proxectos
description: Este tema fornece información sobre a reserva de recursos xenéricos a tarefas e equipos de proxectos.
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
ms.openlocfilehash: d9a81d7242e78dafad871bb07c03459f1de21884d196c6ee7dd9619b2c410404
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007099"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ademais de reservar e atribuír recursos nomeados ou reais ao seu proxecto, pode atribuír recursos xenéricos ás tarefas do proxecto. Estes recursos poden servir como marcadores de posición para os recursos nomeados ata que estea listo para dotar de persoal ao seu proxecto con recursos nomeados. 

1. En Project Service Automation (PSA), abra a páxina **Proxecto** e no separador **Programa** escolla o nome do posto do recurso xenérico na cela **Recurso** do programa. Ou prema a icona **Recurso** na cela para abrir o selector de recursos e logo introduza o nome do recurso xenérico que desexa crear.

![Creación e asignación dun membro xenérico do equipo.](media/RM-how-to-9.png)

Isto abrirá o panel **Creación rápida: Membro do equipo do proxecto**. 

2. Introduza a función e a unidade de organización do membro do equipo de recursos xenéricos e logo prema **Gardar**.

![Creación rápida de membro xenérico do equipo.](media/RM-how-to-10.png)

3. Despois de crear o novo membro do equipo de recursos xenéricos, atribuirase á tarefa. Pode continuar atribuíndo ese recurso xenérico a outras tarefas da programación de tarefas.

![Asignación de membro xenérico de equipo existente a tarefas.](media/RM-how-to-11.png)

4. Despois de atribuír o recurso xenérico, pode xerar un requisito de recurso e cumprilo reservando directamente ou enviando unha solicitude de recurso a un xestor de recursos.

![Xeración dun requisito para un membro xenérico do equipo.](media/RM-how-to-12.png)

Na grade do membro do equipo, ademais de poder empregar o selector de recursos como se mencionou anteriormente, pode engadir recursos xenéricos directamente. Os recursos engádense cun requisito de recurso baseado nas datas de comezo/final e método de atribución especificados no panel **Creación rápida: Membro do equipo do proxecto**.

Pode ver unha diferenza se engade directamente o membro do equipo xenérico e despois atribúe máis tarefas ao recurso xenérico das que solicitaron horas para cubrir. Prema **Xerar requisito** para rexenerar o requisito para equilibrar as horas solicitadas coas atribucións.

Tamén pode premer a ligazón **Requisito do recurso** na grade do equipo para abrir o requisito e engadir habilidades, recursos preferidos, etc.

![Requisito do recurso.](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]