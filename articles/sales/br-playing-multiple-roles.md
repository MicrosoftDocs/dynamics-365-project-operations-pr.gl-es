---
title: Estimar as vendas e os custos do proxecto cando un recurso reservable ten varios roles nun proxecto
description: Este artigo explica como usar as dimensións de prezos para admitir as estimacións de prezos e custos para un recurso que cumpre varias funcións nun proxecto.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9bb59537aaa75d9003925bec37642a2fa7c9ca22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923462"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimar as vendas e os custos do proxecto cando un recurso reservable ten varios roles nun proxecto 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento, despregamento de Lite - de acordo a facturación proforma, Project Operations para situacións baseadas en produción/con fornecemento_ 

As empresas baseadas en proxectos adoitan ter a necesidade dun recurso para cubrir múltiples roles nun proxecto. Cada rol pode ter un prezo e un custo diferentes. Isto significa que o tempo do mesmo recurso nun proxecto podería obter unha estimación financeira diferente segundo a factura e as taxas de custo de cada rol. Pode configurar os valores no rexistro de membro do equipo para o recurso nomeado con diferentes anulacións en cada unha das tarefas ás que está asignado o membro do equipo.

O seguinte exemplo explícalle como a simple substitución dun valor permite que un recurso teña varias funcións nun proxecto con custos e taxas de facturación diferentes.

## <a name="create-tasks"></a>Crear tarefas
Para crear tarefas, ten que engadir tarefas, así como tarefas de resumo, despois das cales ten que atribuír a tarefa antes de engadir a duración da tarefa. 

### <a name="add-tasks-and-summary-tasks"></a>Engadir tarefas e tarefas de resumo
Para engadir unha tarefa, siga os pasos que se indican a continuación:

1. Vaia a **Proxectos** e abra o proxecto ao que desexa engadir tarefas.
2. Seleccione **Engadir nova tarefa**. Nomee a tarefa e prema **Intro**.
3. Introduza outro nome de tarefa e prema **Intro**. Repita isto ata ter unha lista completa de tarefas.
3. Para aplicar sangría ás tarefas baixo **Resumo**, seleccione os tres puntos verticais xunto ao nome da tarefa e logo seleccione **Facer subtarefa**. 

  > [!TIP]
  > Para seleccionar máis dunha tarefa, seleccione unha tarefa, manteña premido **Ctrl** e, a seguir, seleccione outra tarefa.
  >
  > Tamén pode escoller **Promover subtarefa** para mover as tarefas desde debaixo das tarefas **Resumo**.

### <a name="assign-tasks"></a>Atribuír tarefas

Siga os pasos que se indican a continuación para atribuír tarefas:

1. Na columna **Atribuída a** para unha tarefa, seleccione a icona da persoa.
2. Elixa un membro do equipo da lista ou introduza texto para buscar un nome.

### <a name="add-task-duration-and-columns"></a>Engadir duración e columnas da tarefa

Moitas veces é máis doado comezar a construír o seu proxecto con duración. Siga os pasos que se indican a continuación para engadir a duración da tarefa:

1. Na columna **Duración** dunha tarefa, escriba o número de días que pensa que tardará en realizala. Se quere usar unha unidade de tempo diferente, introduza un número máis a palabra **horas**, **semanas** ou **meses**.
2. Se quere que a súa tarefa apareza como un fito en forma de diamante na vista de **Liña de tempo**, na columna **Duración**, introduza **0 días**.
3. Prema **Intro** para ir ao campo **Duración** da seguinte tarefa e continúe introducindo duracións.

  > [!NOTE]
  > Non pode introducir unha duración para as tarefas de resumo.

Pode engadir columnas ao seu proxecto para proporcionar máis detalles. Para iso, seleccione **Engadir columna**. 

Para máis información, consulte [Crear un proxecto](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar o rol e a unidade de organización dun membro xenérico do equipo do proxecto
Siga os pasos seguintes para configurar un rol e unha unidade organizativa para un membro xenérico do equipo.

1. Na páxina **Tarefas**, seleccione a fila **Tarefa** para **Tarefa A.**. 
2. En **Atribuída a**, seleccione **Engadir recurso xenérico**. Isto abre a páxina **Creación rápida de membro do equipo**.
3. No campo **Creación rápida de membro do equipo**, especifique os atributos do membro do equipo xenérico que pode realizar esta tarefa.
4. Seleccione o rol e a unidade organizativa axeitados e logo seleccione **Gardar e pechar**. Créase un membro xenérico do equipo que se asigna a esta tarefa. 
5. Repita os pasos 1-4 para **Tarefa B**. Non obstante, **Tarefa B** debe ter unha función e unidade organizativa diferentes atribuídas ao membro do equipo xenérico que **Tarefa A.**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Configurar o rol e a unidade de organización dunha tarefa do proxecto
Siga os pasos seguintes para configurar un rol e unha unidade organizativa para unha tarefa.

1. Despois de crear a **Tarefa A**, seleccione a tarefa e logo seleccione a icona **i** para abrir o panel **Detalles da tarefa**. 
2. No panel **Detalles da tarefa**, desprácese ata a parte inferior e seleccione **Ver detalles** para abrir a páxina **Detalles da tarefa**.
3. Na páxina **Detalles da tarefa**, en **Rol** e **Unidade Organizativa**, engada os valores necesarios para realizar esta tarefa para o recurso. 

  > [!NOTE]
  > Se completa este escenario empregando os datos de demostración de Project Operations, seleccione **Xefe de consultoría** para o rol, e **Fabrikam US** como unidade organizativa.

4. Seleccione **Tarefa B** e logo seleccione a tarefa.
5. Seleccione a icona **i** para abrir o panel **Detalles da tarefa**. 
6. No panel **Detalles da tarefa**, desprácese ata a parte inferior e seleccione **Ver detalles** para abrir a páxina **Detalles da tarefa**.
7. Na páxina **Detalles da tarefa**, en **Rol** e **Unidade Organizativa**, engada os valores necesarios para o recurso que realizaría esta tarefa. Os valores de **Rol** e **Unidade Organizativa** para **Tarefa B** deben ser diferentes dos de **Tarefa A.**. 

  > [!NOTE]
  > Se completa este escenario empregando os datos de demostración de Project Operations, seleccione **Técnico de rede** para o rol, e **Fabrikam US** como unidade organizativa.

8. Garde e peche a páxina **Detalles da tarefa**. 

## <a name="team-member-and-estimates-behavior"></a>Comportamento do membro do equipo e estimacións 
Para comprender o comportamento na grade **Membro do equipo** e as estimacións, siga os seguintes pasos.

1. Na grade **Membro do equipo**, seleccione os dous membros xenéricos do equipo e logo seleccione **Xerar requisitos**. Isto xerará requisitos de recursos. 
2. Seleccione a fila do membro do equipo para **Xefe de consultoría** e logo seleccione **Reservar**. O panel de programación ábrese cunha lista de recursos. Seleccione un recurso e logo seleccione **Reservar** para reservar o recurso para ese requisito.
3. Seleccione a fila do membro do equipo para **Técnico de rede** e logo seleccione **Reservar**. O panel de programación ábrese cunha lista de recursos. Seleccione o mesmo recurso que antes e logo seleccione **Reservar** para reservar o recurso para ese requisito.

### <a name="team-member-grid"></a>Grade de Membro do equipo 

Na grade **Membro do equipo**, os dous rexistros xenéricos de membros do equipo elimínanse e substitúense por un só recurso. Hai un conxunto de valores para ese recurso, que son un conxunto de valores predefinido para **Rol** e **Unidade Organizativa**.

Cando expande a fila dese rexistro de membro do equipo, pode ver distintas tarefas no rexistro de membro do equipo para ambas tarefas. Cada fila de atribucións ten valores específicos da tarefa para **Rol** e **Unidade organizativa**. 

### <a name="estimates-grid"></a>Grade de estimacións 

Na grade **Estimacións**, as dúas tarefas para o mesmo recurso teñen un prezo diferente. A atribución do recurso na **Tarefa A** ten un prezo empregando o valor do atributo **Rol** de **Xefe de consultoría**. A atribución do mesmo recurso na **Tarefa B** ten un prezo empregando o valor do atributo **Rol** de **Técnico de rede**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]