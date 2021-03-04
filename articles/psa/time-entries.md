---
title: Crear entradas de tempo
description: Este tema fornece información sobre como crear entradas de tempo.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149676"
---
# <a name="create-time-entries"></a>Crear entradas de tempo

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En versións anteriores de Dynamics 365 Project Service Automation, as entradas de tempo introducíanse semanalmente. Na versión 3 de Project Service Automation, as entradas de tempo introdúcense diariamente. Non obstante, despois de crear unhas poucas entradas, pode crealas ou copialas en masa.

## <a name="create-a-time-entry"></a>Crear unha entrada de tempo

Siga estes pasos para crear unha entrada de tempo.

1. Na páxina **Entradas de tempo**, seleccione **Nova**.
2. Na caixa de diálogo **Creación rápida: entrada de tempo**, introduza a duración da entrada de tempo en minutos, horas ou días. A duración debe introducirse co seguinte formato: *x* minutos, *x* horas ou *x* días. Horas e días tamén poden introducirse como valores decimais, por exemplo *x.x* horas ou *x.x* días.
3. Seleccione o tipo de entrada de tempo e o proxecto para o que está a introducir a entrada de tempo.
4. No campo **Tarefa de proxecto**, busque a tarefa para esta entrada de tempo.

    > [!NOTE]
    > Se está a crear unha entrada de tempo para unha tarefa que non está asignada a un usuario, no campo **Tarefa de proxecto**, seleccione o botón **Buscar**, seleccione **Cambiar vista** e, a seguir, seleccione **Todas as tarefas activas do proxecto** para facer unha lista de todas as tarefas.

5. Introduza unha descrición, se é necesaria unha descrición, e seleccione **Gardar e pechar**.

Despois de que se cree e garde a entrada de tempo, pode editala na grade de entrada de tempo. A grade de entrada de tempo admite dous formatos:

- Pode introducir as entradas de temo no formato **hh:mm**. Este formato convértese en horas e fraccións.
- Pode introducir horas e fraccións directamente.

Teña en conta que as fraccións dunha hora non son minutos. Polo tanto, 1,5 horas representa 1 hora e 30 minutos. A mesma regra aplícase ás fraccións dun día. Un día é de 24 horas e 0,5 días representa 12 horas.

## <a name="bulk-create-time-entries"></a>Creación de entradas de tempo en masa

Despois de crear unhas poucas entradas de tempo, pode copialas para crear entradas de tempo adicionais en masa.

1. Na páxina **Entradas de tempo**, seleccione **Copiar semana**.
2. No grupo de campos **Período desde**, nos campos **Data de inicio** e **Data de finalización**, defina o intervalo de datas do que vai copiar as entradas de tempo.
3. No grupo de campos **Período ata**, no campo **Data de inicio**, especifique a data para a que se van crear as entradas de tempo.
4. Seleccione **Copiar** para crear unha copia das entradas de tempo que corresponden ao día da semana que se especifica no grupo de campos **Período ata**. Por exemplo, a entrada de tempo para o luns da semana pasada cópiase ao luns da semana que se especifica no grupo de campos **Período ata**.

## <a name="import-data-for-time-entries"></a>Datos de importación para entradas de tempo

Pode importar datos das reservas e atribucións do proxecto. Cando importe datos, pode especificar o intervalo de datas das reservas para importar e, a seguir, seleccionar explicitamente as reservas que se deben crear como entradas de tempo **Borrador**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Agrupar, ordenar, buscar e filtrar capacidades

Pode agrupar e filtrar as entradas de tempo polas dimensións que se especifican nas columnas. No campo **Agrupar por**, seleccione a dimensión que se vai usar para filtrar as entradas de tempo. Tamén pode ordenar os rexistros de entrada de tempo en orde ascendente ou descendente empregando a frecha de ordenación nas cabeceiras de columna. Ademais, pode mostrar ou ocultar entradas seleccionando o botón **Filtro** nas cabeceiras da columna e, a seguir, na caixa **Buscar**, introducindo o texto que se debe usarse para buscar entradas de tempo por nome de proxecto, tarefa de proxecto, entrada de tempo ou recurso.
