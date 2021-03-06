---
title: Crear atribucións de recursos
description: Este tema ofrece información sobre como crear atribucións de recursos xenéricos e nomeados.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906157"
---
# <a name="create-resource-assignments"></a>Crear atribucións de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


A atribución de recursos é a asociación directa dun membro do equipo do proxecto a unha tarefa de nó folla. Este tema fornece información sobre as diferentes formas de atribuír recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un membro do equipo xenérico a través da atribución de tarefas


Cando crea un membro do equipo xenérico mediante a atribución de tarefas, crea un marcador de posición ou un recurso xenérico. Este recurso xenérico describe as características do recurso nomeado que vostede desexa que traballe nas tarefas. A seguir, pode xerar un requisito, ou enviar unha solicitude utilizando o requisito, que se utiliza para buscar e reservar o recurso nomeado.

1. Na grade Programación para unha tarefa, seleccione a icona de Recurso na cela **Recurso**.
2. Escriba un nome que sirva como nome do recurso marcador de posición. Por exemplo, Xestor de programa.
3. Seleccione **Crear** e, no campo **Creación rápida de membro do equipo** de proxecto á dereita, defina o rol para o recurso xenérico.
4. Atribúa tarefas segundo sexa necesario a este recurso de marcador de posición seleccionando o recurso no **Selector de recursos** para a tarefa. Os recursos aparecen en **Membros do equipo**.
5. Cando remate a atribución do recurso xenérico, seleccione o recurso xenérico no separador **Equipo** e, a seguir, seleccione **Xerar requisito** para crear un requisito de recurso para o recurso xenérico.
6. Seleccione **Reservar** para o recurso xenérico e, a seguir, pode utilizar o panel de programación para localizar e reservar un recurso real. Tamén pode enviar o requisito para conclusión por un xestor de recursos.
7. Cando o recurso xenérico se cumpre completamente (o cumprimento parcial dos requisitos do recurso non dará lugar a unha asignación de recurso) cun recurso nomeado, o recurso xenérico elimínase do equipo. As atribucións de tarefas para o recurso xenérico atribúense ao recurso nomeado que cumpriu o requisito do recurso xenérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuír un recurso denominado da lista de todos os recursos que se poden reservar.

Pode utilizar a caixa de busca no **Selector de recursos** para buscar todos os recursos que se poden reservar activos en Project Service e atribuílos a calquera tarefa nó folla. Os recursos atribuídos deste xeito engádense ao equipo sen reservas. Isto é similar a engadir un membro do equipo e seleccionar **Ningún** como método de asignación. O recurso móstrase nos separadores **Equipo**, **Atribución de recursos** e **Conciliación** como recursos co só atribucións e sen reserva. Reservaos se desexas utilizar a súa dispoñibilidade.

1. Desde a grade de tarefas, panel ou liña de tempo, desprácese ata o a cela **Atribuído a**.
2. Na caixa de busca, comece a escribir un nome. Os resultados de busca para o nome móstranse no **Selector de recursos** en **Outros recursos**.
3. Seleccione o recurso que desexa asignar á tarefa ou seleccione o nome do recurso en **Outros recursos do equipo**.
