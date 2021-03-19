---
title: Estimar as vendas e os custos do proxecto cando un recurso reservable ten varios roles para un proxecto
description: Este tema fornece información sobre como se poden usar dimensións de prezos para soportar prezos e custos dun recurso que cumpra múltiples funcións nun proxecto.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290987"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Estimar as vendas e os custos do proxecto cando un recurso reservable ten varios roles para un proxecto 

[!include [banner](../includes/psa-now-project-operations.md)]

As empresas baseadas en proxectos adoitan ter a necesidade dun recurso para realizar múltiples funcións nun proxecto. Cada unha destas funcións podería ter un prezo e un custo diferentes, o que significa que o tempo do mesmo recurso no proxecto podería obter unha estimación financeira diferente segundo as taxas de custo e facturación de cada unha das funcións. Project Service Automation permite configurar os valores no rexistro do membro do equipo para o recurso nomeado e permite diferentes anulacións en cada unha das tarefas ás que está asignado o membro do equipo.

O seguinte exemplo explica como a simple anulación deste valor permite que un recurso teña varios roles nun proxecto con taxas de custo e facturación diferentes.

## <a name="create-tasks"></a>Crear tarefas
Cree dúas tarefas de proxecto durante 40 horas cada unha, Tarefa A e Tarefa B. Seleccione a Tarefa A como predecesora da Tarefa B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configure o rol e a unidade de organización para un membro xenérico do equipo do proxecto

1. Na páxina **Programar**, seleccione a fila **Tarefa** para a Tarefa A. 
2. No campo **Recursos**, seleccione **Crear** na lista despregable.
3. No campo **Creación rápida de membro do equipo**, especifique os atributos do membro do equipo xenérico que pode realizar esta tarefa.
4. Seleccione o rol e a unidade organizativa axeitados e logo seleccione **Gardar e pechar**. Créase un membro xenérico do equipo que se asigna a esta tarefa. 

Repita estes pasos para a Tarefa B e asegúrese de que o rol e a unidade organizativa do membro do equipo xenérico creado para a Tarefa B son diferentes dos da Tarefa A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configure o rol e a unidade de organización para unha tarefa do proxecto

1. Despois de crear a Tarefa A, seleccione a tarefa e logo seleccione **Editar tarefa**.
2. Na páxina **Detalles da tarefa**, busque os campos **Rol** e **Unidade organizativa**, engada os valores que se requiren dun recurso que realizaría esta tarefa. 

  > [!NOTE]
  > Se está completando estes escenarios usando os datos de demostración de Project Service Automation, seleccione **Xefe de consultoría** para o rol, e **Fabrikam US** como unidade organizativa.

3. Seleccione a Tarefa B e, a seguir, seleccione **Editar tarefa**.
4. Na páxina **Detalles da tarefa**, busque os campos **Rol** e **Unidade organizativa**, engada os valores que se requiren dun recurso que realizaría esta tarefa. Asegúrese de que os valores dos campos **Función** e **Unidade Organizativa** para a tarefa B sexan diferentes dos valores para a tarefa A. 

  > [!NOTE]
  > Se está completando estes escenarios usando os datos de demostración de Project Service Automation, seleccione **Técnico de rede** para o rol, e **Fabrikam US** como unidade organizativa.

5. Garde e peche a páxina **Detalles da tarefa**. 

## <a name="team-member-and-estimates-behavior"></a>Comportamento do membro do equipo e estimacións 

1. Na páxina **Detalles da tarefa**, en **Membro do equipo**, seleccione os dous membros xenéricos do equipo e logo seleccione **Xerar requisitos**. 
2. Selecciona a fila do membro do equipo para **Xefe de consultoría** e logo seleccione **Reservar**. Ábrese o panel de programación e reserva un recurso para ese requisito.
3. Seleccione a fila do membro do equipo para **Técnico de rede** e logo seleccione **Reservar**. Ábrese o panel de programación e reserva o mesmo recurso para ese requisito.

### <a name="team-member-grid"></a>Grade de Membro do equipo 
Na grade **Membro do equipo**, observe que os dous rexistros xenéricos de membros do equipo se eliminaron e se substituíron por un recurso. Hai un conxunto de valores para ese recurso que mostra un conxunto de valores predefinido para **Rol** e **Unidade organizativa**.
Cando amplía a fila dese rexistro de membro do equipo, pode ver distintas tarefas no rexistro de membro do equipo para ambas tarefas. Cada fila de atribucións ten valores específicos da tarefa para **Rol** e **Unidade organizativa**. 

### <a name="estimates-grid"></a>Grade de estimacións 
Cando navegue á grade **Estimacións**, notará que as dúas atribucións para o mesmo recurso teñen un prezo diferente.
A atribución do recurso na Tarefa A ten un prezo empregando o valor do atributo **Rol** de **Xefe de consultoría**. A atribución do mesmo recurso na Tarefa B ten un prezo empregando o valor do atributo **Rol** de **Técnico de rede**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]