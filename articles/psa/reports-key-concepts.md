---
title: Conceptos clave
description: Este tema fornece ligazóns a información sobre os conceptos clave para a xestión de recursos en Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 3a0305ab35a28348798f9d9c7452b3bee75412e4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601246"
---
# <a name="key-concepts"></a>Conceptos clave

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Na seguinte táboa defínense conceptos clave empregados na aplicación Dynamics 365 Project Service Automation.

| Concepto                    | Definición |
|----------------------------|------------|
| Membro do equipo do proxecto        | Como parte do equipo do proxecto, un membro do equipo do proxecto pode ser un recurso nomeado que ten reservas, un recurso nomeado que non ten reservas ou un recurso xenérico. Os recursos xenéricos non teñen reservas, son locais para o proxecto e non teñen restricións de capacidade nos proxectos. |
| Recurso xenérico de proxecto   | Un marcador de posición de recurso que lle permite formar un equipo e dotar de persoal un plan de proxecto sen ter que coñecer ao recurso nomeado. O calendario do proxecto úsase como calendario do recurso xenérico. Pódense engadir recursos xenéricos a un equipo de proxecto e atribuírlles tarefas. |
| Horas reservadas               | Fanse reservas duras de horas de recursos para un proxecto para garantir a finalización do traballo. As horas reservadas consúmense da capacidade global do recurso. As reservas son só de recursos nomeados e non de recursos xenéricos. |
| Horas atribuídas             | As horas do recurso atribúense a tarefas na programación do proxecto. As atribucións poden ser de recursos nomeados ou xenéricos. As atribucións poden ser independentes das reservas. |
| Horas requiridas             | A capacidade que se require, pero que aínda non cumpre un recurso nomeado. As horas requiridas son relevantes só para membros xenéricos do equipo que xeraron requisitos de recursos. |
| Demanda                     | A carga de traballo actual e entrante. En Project Service Automation, a demanda móstrase como requisitos de recursos ou solicitudes de recursos. |
| Requisito do recurso       | Unha entidade que se emprega para capturar horas requiridas, datas de inicio e finalización, habilidades, xeografía e outras dimensións de prezos para os recursos requiridos. Os requisitos dos recursos xéranse a partir de membros do equipo do proxecto ou creados individualmente. |
| Solicitude de recursos           | Unha entidade que se utiliza como "sobre" para levar o requisito de recurso que debe cumprir un xestor de recursos. |
| Rol predefinido de recurso      | O rol baixo o que se agrupa un recurso para o cálculo de utilización. Se supón que o recurso ten as habilidades necesarias para o rol e que cumprirá a utilización obxectivo para ese rol. |
| Unidade de organización de recursos | A unidade organizativa á que está atribuído un recurso. |
| Contorno                    | Horas de tarefa, requisito ou atribución tal como se descompoñen nunha distribución diaria. Por exemplo, unha tarefa de cinco días e 40 horas pódese moldear en oito horas ao día durante cinco días. |
| Vista de conciliación        | Unha vista que mostra as reservas e atribucións para cada membro do equipo do proxecto. Esta vista permite que o xestor de proxectos busque calquera desaxuste entre reservas e atribucións e tome medidas correctivas se ocorre algún desaxuste. |
| Horas de traballo                 | Entidade que se emprega para identificar a capacidade dos recursos e as horas laborables e non laborables. Esta entidade tamén se denomina calendario de recursos. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
