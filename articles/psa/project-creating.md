---
title: Programas de proxecto
description: Este tema fornece información sobre como crear unha programación.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: dd8e916b06d4d8ee77c800f601fb517d797b5c6d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998454"
---
# <a name="project-schedules"></a>Programas de proxecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Unha programación de proxecto communica que traballo debe realizarse, que recursos van realizar o traballo e o intervalo temporal no que se debe concluír o traballo. Reflicte todo o traballo asociado á entrega do proxecto a tempo. En Dynamics 365 Project Service Automation, crea unha programación de proxecto dividindo o traballo en tarefas xestionables, estimando o tempo que se require para realizar cada tarefa, establecendo dependencias de tarefas, establecendo duracións de tarefas e estimando os recursos xenéricos que realizarán as tarefas. A programación do proxecto créase no separador **Programación** da páxina do proxecto.
 
## <a name="tasks"></a>Tarefas

O primeiro paso para crear unha programación de proxecto é dividir o traballo en partes manexables. A programación en PSA admite as seguintes funcionalidades:

- Nó de raíz de proxecto
- Tarefas de resumo ou contedor
- Tarefas de nó folla

### <a name="project-root-node"></a>Nó de raíz de proxecto

O nó raíz do proxecto é a tarefa de resumo do primeiro nivel para o proxecto. Todas as outras tarefas de proxecto créanse nela. O nome do nó raíz é sempre o nome do proxecto. O esforzo, as datas e a duración do nó raíz resúmense segundo os valores da xerarquía de abaixo. Non pode editar as propiedades do nó raíz. Tampouco pode eliminar o nodo raíz.

### <a name="summary-or-container-tasks"></a>Tarefas de resumo ou contedor 

As tarefas de resumo teñen subtarefas ou tarefas contedor debaixo. Non teñen esforzo laboral nin custo propio. En cambio, o seu esforzo laboral e custo son un resumo do esforzo laboral e do custo das súas tarefas contedor. A data de inicio da tarefa resumo é a data de inicio das tarefas contedor e a data de finalización é a data de finalización das tarefas contedor. Pódese editar o nome dunha tarefa resumo, pero non se poden editar as propiedades de programación (esforzo, datas e duración). Se elimina unha tarefa resumo, tamén eliminará as súa tarefas contedor.

### <a name="leaf-node-tasks"></a>Tarefas de nó folla

As tarefas de nó folla representan o traballo máis granular no proxecto. Teñen un esforzo estimado, recursos, datas de inicio e fin planificadas e unha duración.
 
## <a name="creating-a-task-hierarchy"></a>Creación dunha xerarquía de tarefas

Pode crear unha xerarquía de tarefas utilizando as seguintes opcións:

- Botón **Engadir tarefa**
- Botón **Aplicar sangría de tarefa**
- Botón **Anular sangría de tarefa**
- Botóns **Mover arriba** e **Mover abaixo**
- Atallos de teclado e accesibilidade

### <a name="add-task"></a>Engadir tarefa

O botón **Engadir tarefa** permite crear unha nova tarefa na xerarquía. Se non selecciona unha posición, a tarefa insírese ao final. 

Asignase un ID de programación a cada tarefa. O ID de programación representa a profundidade e a posición da tarefa na xerarquía. Emprega numeración de esquema. Para tarefas do primeiro nivel baixo o nó raíz do proxecto, úsase un esquema de numeración de 1, 2, 3, etc. Para tarefas baixo o primeiro nivel, úsase un esquema de numeración de 1.1, 1.2, 1.3, etc.

### <a name="indent-task"></a>Aplicar sangría á tarefa

Cando se aplicou a sangría a unha tarefa, convértese en dependente da tarefa que está directamente por riba dela. A identificación de programación da tarefa recalcularase para que estea baseada na identificación de programación da súa nova matriz e siga o esquema de numeración. A tarefa matriz agora é unha tarefa resumo ou unha tarefa contedor. Polo tanto, convértese nun resumo das súas tarefas dependentes.

### <a name="outdent-task"></a>Cancelar sangría dunha tarefa 

Cando se cancelou a sangría dunha tarefa, xa non depende da tarefa que foi a súa matriz. A seguir, o ID de programación recalculase de xeito que reflicta a profundidade e posición actualizadas da tarefa na xerarquía. O esforzo, custo e datas da tarefa matriz anterior recalculanse para que non inclúan esta tarefa.

### <a name="move-up-and-move-down"></a>Mover arriba e mover abaixo. 

Os botóns **Mover arriba** e **Mover abaixo** cambian a posición dunha tarefa dentro da súa xerarquía matriz. As modificacións deste tipo non afectan ao esforzo, o custo, as datas ou a duración da tarefa. Só o ID de programación da tarefa vese afectado. O ID de programación recalcúlase de xeito que reflicta a nova posición da tarefa na xerarquía na lista de tarefas dependentes da matriz.

### <a name="accessibility-and-keyboard-shortcuts"></a>Atallos de teclado e accesibilidade

A grade **Programación** é totalmente accesible e pode usarse con lectores de pantalla como Narrator, JAWS ou NVDA. Pode moverse pola área da grade mediante as teclas de frecha (como en Microsoft Excel), pode usar a tecla TAB para avanzar nos elementos interactivos da interface de usuario e pode usar a tecla de frecha cara abaixo, a tecla Intro ou a barra espazadora para seleccionar e invocar os menús despregables. As cabeceiras de columna tamén son interactivas. Pode ocultar e amosar columnas, usar a tecla TAB e as teclas de frecha para moverse polas cabeceiras das columnas e usar os botóns de acción da barra de ferramentas. Ademais, pode empregar os seguintes atallos de teclado:

- **Actualizar**: ALT+MAIÚS+F5
- **Engadir**: ALT+MAIÚS+Inserir
- **Eliminar**: ALT+MAIÚS+Eliminar
- **Mover cara arriba/abaixo**: ALT+MAIÚS+Frechas arriba/abaixo
- **Aplicar sangría/Cancelar sangría**: ALT_MAIÚS+Frechas esquerda/dereita
- **Expandir/Contraer xerarquías**: Teclas ALT+MAIÚS+ Máis/Menos

## <a name="task-attributes"></a>Atributos de lista

O nome dunha tarefa describe o traballo que precisa ser concluído. En PSA, os atributos asociados a unha tarefa describen a programación da tarefa e os seus requisitos de persoal.

> ![Atributos de lista](media/project-2.png)
 
### <a name="schedule-attributes"></a>Programar atributos

Os atributos **Esforzo**, **Data de inicio**, **Data de finalización** e **Duración** definen a programación para a tarefa.

Outros atributos de programación inclúen:

- **Horas de esforzo**: Introduza unha estimación das horas necesarias para completar a tarefa. 
- **Duración**: Especifique o número de días laborables que se requiren para completar a tarefa.
- **Identificador de programación**: Este ID xerado automaticamente úsase para ordenar tarefas na xerarquía. As dependencias entre as tarefas xestionan a orde real na que se traballa nas tarefas.
 
### <a name="staffing-attributes"></a>Atributos de persoal

Pódese acceder a atributos de persoal a través do campo **Recursos** na programación. Pode buscar un recurso existente ou premer en **Crear** e no panel **Creación rápida**, engadir un membro do equipo do proxecto como novo recurso.

Os campos **Rol**, **Unidade de recursos** e **Nome do posto** úsanse para describir os requisitos de persoal para a tarefa. Estes atributos de persoal xunto coa programación de tarefas úsanse para atopar os recursos dispoñibles para facer esta tarefa.

**Rol** - Especifique o tipo de recurso que se require para realizar a tarefa.

**Unidade de recursos** - Especifique a unidade desde a que se deben atribuír os recursos para a tarefa. Este atributo afecta ao custo e ás estimacións de vendas da tarefa se o custo e a taxa de factura do recurso están establecidos en función das unidades de recursos.

**Nome do posto** - Insira un nome sinxelo para o recurso xenérico que serve como marcador de posición para o recurso que finalmente fará o traballo.

O campo **Recursos** contén o nome de posto do recurso xenérico ou recurso nomeado cando se atopa.

O campo **Categoría** contén os valores que indican un tipo de traballo máis amplo no que se pode agrupar a tarefa. Este campo non afecta a programación nin a dotación de persoal. Úsase só para informes.

### <a name="task-dependencies"></a>Dependencias de tarefa 

Pode usar a programación en PSA para crear relacións predecesoras entre tarefas. O campo **Predecesor** en **Tarefas** leva un ou varios valores para indicar as tarefas das que depende unha tarefa. Cando se atribúe valores predecesores a unha tarefa, a tarefa só pode iniciarse despois de que conclúan todas as tarefas predecesoras. Por mor da dependencia, a data de inicio prevista da tarefa restablécese á data na que se completaron as tarefas predecesoras.

O modo de tarefa non ten efecto nas actualizacións que se realizan ás datas de inicio e finalización das tarefas predecesoras/dependentes.

## <a name="task-mode"></a>Modo de tarefa 

O modo de tarefa determina a programación de tarefas de nós folla. PSA admite dous modos de tarefa para cada tarefa: programación automática e programación manual.

### <a name="auto-scheduling"></a>Programación automática 
 
Cando establece o modo de tarefa a **Programada automaticamente**, o motor de programación de tarefas usa as regras de programación nos seguintes atributos de tarefa para determinar a programación para a tarefa:

#### <a name="scheduling-rules"></a>Regras de programación

Por defecto, se un nó folla non ten predecesores, a súa data de inicio establécese na data de inicio da programación do proxecto. A duración dunha tarefa de nó folla calcúlase sempre como o número de días laborables entre as datas de inicio e fin. Cando unha tarefa se programa automaticamente, o motor de programación segue as regras seguintes:

- As datas de inicio e fin da tarefa sempre deben ser días laborables segundo o calendario de programación do proxecto. 
- Para calquera tarefa que teña predecesores, a data de inicio establécese automaticamente na última data de fin dos seus predecesores
- O esforzo calcúlase mediante esta fórmula: Número de persoas × Duración × Horas nun día laboral estándar no calendario do proxecto.

### <a name="manual-scheduling"></a>Programación manual

Se as regras de programación automática non cumpren os seus requisitos, pode configurar o modo de tarefa para a tarefa **Programado manualmente**. Este axuste fai que o motor de programación non calcule os valores para outros atributos de programación. Independentemente do modo de tarefa, se establece predecesores en tarefas, sempre afectará á data de inicio da tarefa dependente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]