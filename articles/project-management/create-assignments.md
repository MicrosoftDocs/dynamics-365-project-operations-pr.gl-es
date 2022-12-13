---
title: Crear atribucións de recursos
description: Este artigo ofrece información sobre como crear atribucións de recursos xenéricos e nomeados.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811991"
---
# <a name="create-resource-assignments"></a>Crear atribucións de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


A atribución de recursos é a asociación directa dun membro do equipo do proxecto a unha tarefa de nó folla. Este artigo fornece información sobre as diferentes formas de atribuír recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un membro do equipo xenérico a través da atribución de tarefas


Cando crea un membro do equipo xenérico mediante a atribución de tarefas, crea un marcador de posición ou un recurso xenérico. Este recurso xenérico describe as características do recurso nomeado que finalmente quere traballar nas tarefas. A continuación, xera un requisito ou envía unha solicitude mediante o requisito que se utiliza para buscar e reservar o recurso nomeado.

1. Na grade Programación para unha tarefa, seleccione a icona de Recurso na cela **Recurso**.
2. Escriba un nome para servir como nome do recurso de marcador de posición. Por exemplo, Xestor de programa.
3. Seleccione **Crear** e, no campo **Creación rápida de membro do equipo** de proxecto á dereita, defina o rol para o recurso xenérico.
4. Atribúa tarefas segundo sexa necesario a este recurso de marcador de posición seleccionando o recurso no **Selector de recursos** para a tarefa. Os recursos aparecen en **Membros do equipo**.
5. Cando remate de asignar o recurso xenérico, na pestana  **Equipo**, seleccione o recurso xenérico e, a continuación, seleccione **Xerar requisito** para crear un requisito de recurso para o recurso xenérico.
6. Seleccione **Reservar** para o recurso xenérico e, a seguir, pode utilizar o panel de programación para localizar e reservar un recurso real. Tamén pode enviar o requisito para conclusión por un xestor de recursos.
7. Cando o recurso xenérico se cumpre completamente cun recurso nomeado, o recurso xenérico elimínase do equipo. (O cumprimento parcial dos requisitos de recursos non dará lugar a unha asignación de recursos.) As asignacións de tarefas para o recurso xenérico asígnanse ao recurso nomeado que cumpriu o requisito de recursos do recurso xenérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuír un recurso denominado da lista de todos os recursos que se poden reservar.

Pode utilizar a caixa de busca no **Selector de recursos** para buscar todos os recursos que se poden reservar activos en Project Service e atribuílos a calquera tarefa nó folla. Os recursos atribuídos deste xeito engádense ao equipo sen reservas. Isto é similar a engadir un membro do equipo e seleccionar **Ningún** como método de asignación. O recurso móstrase nos separadores **Equipo**, **Atribución de recursos** e **Conciliación** como recursos co só atribucións e sen reserva. Reservaos se desexas utilizar a súa dispoñibilidade.

1. Desde a grade de tarefas, panel ou liña de tempo, desprácese ata o a cela **Atribuído a**.
2. Na caixa de busca, comece a escribir un nome. Os resultados de busca para o nome móstranse no **Selector de recursos** en **Outros recursos**.
3. Seleccione o recurso que desexa asignar á tarefa ou seleccione o nome do recurso en **Outros recursos do equipo**.

## <a name="editing-resource-assignment-contours"></a>Edición de contornos de atribución de recursos

Por defecto, cando se asignan recursos a unha tarefa na programación, o seu esforzo distribúese linealmente a cada recurso, en función das horas de traballo dese recurso e do modo de programación do proxecto. Un xestor de proxecto pode usar a grella de asignación de recursos para refinar as estimacións de esforzo de cada recurso que se asigna a unha ou moitas tarefas nas diferentes escalas de tempo. Esta función axuda aos xestores de proxectos a producir estimacións de custos e vendas máis precisas, que están dirixidas polos contornos de asignación de recursos que se xeran cando se asigna un recurso a unha tarefa. Ademais, os xestores de proxectos poden reflectir máis facilmente a demanda de recursos necesaria para crear a demanda nun requisito de recursos.

### <a name="navigation"></a>Navegación

Para acceder á cuadrícula de edición de contornos, o xestor do proxecto selecciona primeiro a pestana **Tarefas** na páxina principal do proxecto e despois selecciona **Atribucións** tab.

![Pestana Tarefas na pestana Tarefas da páxina principal do proxecto.](media/AssignmentGrid.png)

A grella admite dous métodos de agrupación: **grupo por recurso** e **grupo por tarefa**. A diferenza da vista de grade, as columnas non se poden configurar. As únicas columnas visibles son **Asignado a**, **Nome da tarefa**, **Inicio da tarefa**,** Finalización da tarefa **e** Esforzo da tarefa **.

Cando a grella se renderiza inicialmente, comeza no contorno de asignación máis cedo. Se a túa axenda non contén ningunha tarefa que teña esforzo, a grella estará en branco e non mostrará nada.

![Grella de asignación en branco.](media/emptyassignmentgrid.png)

Se queres ver os teus contornos e diferentes escalas de tempo, tamén están dispoñibles a grella de asignación de recursos de só lectura e a grella de conciliación de recursos.

### <a name="resource-calendars"></a>Calendarios de recursos

A posibilidade de editar un contorno para un día específico réxese polos días laborables do recurso, tal e como se reflicte no seu calendario. Se unha cela está desactivada para un determinado recurso, ese recurso non ten días laborables durante ese período.

Os contornos dun recurso poden estenderse máis aló das datas actuais de inicio e finalización da tarefa asignada. Se se actualiza un contorno para que sexa posterior á última data de finalización dunha tarefa ou á primeira data de inicio dunha tarefa, a data de finalización ou de inicio da tarefa cambiarase segundo corresponda. Non obstante, se se actualiza un contorno para que sexa anterior á data de inicio dunha tarefa que está ligada a un predecesor, a actualización fallará porque a asignación fará que a tarefa se inicie antes de que se complete o seu predecesor e ese comportamento non é actualmente. apoiado.

### <a name="co-authoring"></a>Coautoría

Os cambios na grella de asignación de recursos reflíctense automaticamente en todas as vistas asociadas, incluídas as vistas de gráfico, cronoloxía, taboleiro e grella. Se varios usuarios están revisando o proxecto ao mesmo tempo, calquera cambio que faga un usuario reflectirase na grella. Pola contra, os cambios que se fagan na grella de asignación de recursos mostraranse a todos os demais usuarios que estean vendo o proxecto na mesma sesión.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
