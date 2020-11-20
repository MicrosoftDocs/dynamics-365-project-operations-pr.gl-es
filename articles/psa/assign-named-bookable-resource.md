---
title: Reservar recursos reservables nomeados para un equipo de proxectos e atribuír tarefas
description: Este tema fornece información sobre como reservar recursos nomeados para equipos de proxectos e atribuírlles tarefas.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130171"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Reservar recursos reservables nomeados para un equipo de proxectos e atribuír tarefas 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode engadir un recurso nomeado ao seu equipo de proxectos reservándoo directamente ao equipo. Para facelo, siga os pasos que se indican a continuación:

1. En Project Service Automation, vaia a **Proxectos** e seleccione abrir o proxecto para o que vai reservar.
2. Na páxina **Proxecto**, no separador **Equipo**, prema **Novo**. 

![Engadir un membro do equipo no separador do equipo](media/RM-how-to-1.png)

3. Na caixa de diálogo **Creación rápida de membro do equipo de proxecto**, seleccione o recurso reservable. O campo **Rol** encherase co rol predefinido do recurso se ten un atribuído. Pode cambiar o rol se fose necesario. 
4. Seleccione as datas desde e ata nas que se necesitará o recurso e seleccione o método de atribución da capacidade do recurso. 
5. Se desexa que o membro do equipo sexa o responsable da a probación do proxecto, seleccione **Si** no campo **Responsable de aprobación do proxecto**. Isto suporá que o membro do equipo pode aprobar as entradas de tempo e gastos presentadas para este proxecto. 
6. Prema **Gardar**.

![Engadir un membro do equipo no formulario de creación rápida](media/RM-how-to-2.png)


Agora pode atribuír o recurso reservado a tarefas do proxecto. Na páxina **Proxecto**, prema o separador **Programación** para atribuír tarefas ao novo recurso. O selector de recursos que se inicia desde o campo **Recursos** na grada de tarefas amosará os membros do equipo que pode seleccionar.

![Atribución dun membro do equipo a unha tarefa no separador de programación](media/RM-how-to-3.png)

Na versión 3 para Project Service Automation (PSA), as reservas de recursos e as atribucións de tarefas non están moi integradas. Isto significa que cando utiliza o selector de recursos na programación, pode atribuír tarefas aos membros do equipo durante máis horas das que cobren as súas reservas no proxecto.
Podes ver as diferenzas entre as reservas e atribucións dos membros do equipo no separador **Equipo** ou no separador **Reconciliación de recursos**. Tamén pode reconciliar as diferenzas entre reservas e atribucións de recursos a un nivel máis detallado.

![Separador de reconciliación de recursos](media/RM-how-to-4.png)

Tamén pode usar o selector de recursos no separador **Programación** para buscar e seleccionar recursos reservables que xa non forman parte do equipo do proxecto. Estes móstranse no selector de recursos como **Outros recursos**.

![Atribución dun recurso que non é membro do equipo a unha tarefa](media/RM-how-to-5.png)

Cando fai isto, o recurso engádese ao equipo do proxecto e atribúese á tarefa, pero non se xeran reservas.

![Membro do equipo con atribucións e sen reservas](media/RM-how-to-6.png)

Pode usar a capacidade de extensión de recursos no separador **Reconciliación** ou o **Panel de programación** para reservar a capacidade do recurso para o proxecto.

![Extensión das reservas para un membro do equipo no separador de reconciliación de recursos](media/RM-how-to-7.png)

Despois de que un membro do equipo estea reservado no seu proxecto, pode manter as reservas ou usar o panel de programación para xestionar as súas reservas.
