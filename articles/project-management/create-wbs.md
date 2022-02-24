---
title: Crear unha estrutura de subdivisión do traballo
description: Este tema explica como crear unha estrutura de subdivisión do traballo (WBS) que inclúa os controis básicos na nova interface de programación.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841337"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Crear unha estrutura de subdivisión do traballo (WBS)

Unha programación de proxecto comunica que traballo debe realizarse, que recursos van realizar o traballo e o intervalo temporal no que se debe completar o traballo. A programación reflicte todo o traballo asociado coa entrega do proxecto a tempo. En Dynamics 365 Project Operations, vostede crea unha programación facendo o seguinte:

  - Dividir o traballo en tarefas manexables.
  - Estimar o tempo necesario para facer cada tarefa.
  - Definir as dependencias das tarefas.
  - Definir as duracións das tarefas.
  - Estimar os recursos xenéricos que farán as tarefas. 

A programación do proxecto créase no separador **Programar** da páxina do **Proxecto**.

## <a name="tasks"></a>Tarefas

O primeiro paso para crear unha programación de proxecto é dividir o traballo en partes manexables. A programación en Project Operations admite as seguintes funcionalidades:

- Tarefas de resumo ou contedor
- Tarefas de nó folla

### <a name="summary-tasks"></a>Tarefas de resumo

As tarefas de resumo poden almacenar outras tarefas de resumo ou tarefas de nó folla. Non teñen esforzo laboral nin custo propio. En cambio, o seu esforzo laboral e custo son un resumo do esforzo laboral e do custo das súas tarefas contedor. A data de inicio da tarefa resumo é a data de inicio das tarefas contedor e a data de finalización é a data de finalización das tarefas contedor. Pódese editar o nome dunha tarefa resumo, pero non se poden editar as propiedades de programación, incluídas esforzo, datas e duración. Se elimina unha tarefa resumo, tamén eliminará as súa tarefas contedor.

### <a name="leaf-node-tasks"></a>Tarefas de nó folla

As tarefas de nó folla representan o traballo máis granular no proxecto. Teñen un esforzo estimado, recursos, datas de inicio e fin planificadas e unha duración.

## <a name="create-a-task-hierarchy"></a>Crear unha xerarquía de tarefas

### <a name="add-a-task"></a>Engadir unha tarefa

Siga os pasos que se indican a continuación para engadir unha ou máis tarefas.

1. Vaia a **Proxectos** e seleccione e abra o rexistro do proxecto para o que desexa crear unha programación. 
2. Seleccione o separador **Tarefas**. 
3. Seleccione **Engadir nova tarefa**, insira un nome para a tarefa e logo prema Intro.
2. Insira outro nome de tarefa e prema Intro de novo ata que teña unha lista completa de tarefas.

### <a name="manage-hierarchy-of-a-task"></a>Xestionar a xerarquía dunha tarefa

Cando se aplicou a sangría a unha tarefa, convértese en dependente da tarefa que está directamente por riba dela. A identificación de programación da tarefa recalcularase para que estea baseada na identificación de programación da súa nova matriz e siga o esquema de numeración. A tarefa principal agora é unha tarefa de resumo. Polo tanto, convértese nun resumo das súas tarefas dependentes. Cando se sube o nivel dunha tarefa, xa non depende da tarefa que foi a súa matriz. A seguir, o ID de programación recalculase de xeito que reflicta a profundidade e posición actualizadas da tarefa na xerarquía. O esforzo, custo e datas da tarefa matriz anterior recalculanse para que non inclúan esta tarefa.

Siga os pasos que se indican a continuación para subir ou baixar o nivel dunha tarefa.

1. Na páxina **Proxecto**, no separador **Tarefas**, en **Tarefas de resumo**, seleccione os tres puntos verticais xunto ao nome da tarefa e logo seleccione **Facer subtarefa**. 
2. Selecciona a tarefa que baixa ou sube de nivel. Para seleccionar máis dunha tarefa, seleccione unha tarefa, manteña premido Ctrl e, a seguir, seleccione tarefas adicionais.
2. Seleccione **Baixar nivel** ou **Subir nivel de subtarefa** para mover as tarefas desde debaixo ou fóra das tarefas de resumo.

### <a name="move-tasks-up-and-down"></a>Mover tarefas arriba e abaixo

As tarefas pódense mover a calquera nivel da estrutura de subdivisión do traballo de dous xeitos:

- Seleccione unha ou máis tarefas e arrástreas ata o lugar desexado.
- Seleccione unha ou máis tarefas, prema o botón dereito e seleccione **Cortar**, seleccione a cela de destino na programación e prema co botón dereito e seleccione **Pegar**.

## <a name="task-attributes"></a>Atributos de lista

O nome dunha tarefa describe o traballo que precisa ser concluído. En Project Operations, os atributos asociados a unha tarefa describen a programación da tarefa e os seus requisitos de persoal.

## <a name="schedule-attributes"></a>Programar atributos

Os atributos **Esforzo**, **Data de inicio**, **Data de finalización** e **Duración** definen a programación para a tarefa.

A seguinte táboa mostra atributos de programación adicionais.

| **Nome para mostrar final** | **Descrición final** |
| --- | --- |
| Esforzo realizado (horas) | Traballos completados para a tarefa en horas. |
| Duración | Mostra a duración en días da tarefa. |
| Esforzo total | Total de traballos para a tarefa en horas. |
| Rematar | Data e hora de finalización. |
| % concluído | A porcentaxe da tarefa que está completa. |
| Depósito do proxecto | O panel de tarefas pode agruparse por depósito para que cada depósito teña a súa propia columna. |
| Esforzo restante (horas) | O traballo restante para a tarefa en horas. |
| Iniciar | Data e hora de inicio. |
| Nome | Nome a tarefa do proxecto. |
| ID | O ID da tarefa da estrutura de subdivisión do traballo. |

## <a name="staffing-attributes"></a>Atributos de persoal

Pódese acceder a atributos de persoal a través do campo **Recursos** na programación. Pode buscar un recurso existente ou seleccionar **Crear** e no panel **Creación rápida**, engadir un membro do equipo do proxecto como novo recurso.

Os campos **Rol**, **Unidade de recursos** e **Nome do posto** úsanse para describir os requisitos de persoal para a tarefa. Estes atributos de persoal, xunto coa programación de tarefas, úsanse para atopar os recursos dispoñibles para facer esta tarefa.

   - **Rol**: Especifique o tipo de recurso que se require para realizar a tarefa.
   - **Unidade de recursos**: Especifique a unidade desde a que se deben atribuír os recursos para a tarefa. Este atributo afecta ao custo e ás estimacións de vendas da tarefa se o custo e a taxa de factura do recurso están establecidos en función das unidades de recursos.
   - **Nome do posto**: Insira un nome sinxelo para o recurso xenérico que serve como marcador de posición para o recurso que finalmente fará o traballo.

O campo **Recursos** contén o nome de posto do recurso xenérico ou recurso nomeado cando se atopa.

O campo **Categoría** contén os valores que indican un tipo de traballo máis amplo no que se pode agrupar a tarefa. Este campo non afecta a programación nin a dotación de persoal. Pola contra, o campo úsase só para informar.

## <a name="task-dependencies"></a>Dependencias de tarefa

Pode usar a programación en Project Operations para crear relacións predecesoras entre tarefas. O campo **Predecesor** utiliza un ou varios valores para indicar as tarefas das que depende unha tarefa. Cando se atribúe valores predecesores a unha tarefa, a tarefa só pode iniciarse despois de que conclúan todas as tarefas predecesoras. Por mor da dependencia, a data de inicio prevista da tarefa restablécese á data na que se completaron as tarefas predecesoras.

O modo de tarefa non ten efecto nas actualizacións que se realizan ás datas de inicio e finalización das tarefas predecesoras/dependentes.

## <a name="accessibility-and-keyboard-shortcuts"></a>Atallos de teclado e accesibilidade

A grade **Programación** é totalmente accesible e pode usarse con lectores de pantalla como Narrator, JAWS ou NVDA. Pode moverse pola área da grade mediante as teclas de frecha (como en Microsoft Excel), pode usar a tecla TAB para avanzar nos elementos interactivos da interface de usuario e pode usar a tecla de frecha cara abaixo, a tecla Intro ou a barra espazadora para seleccionar e abrir os menús despregables.
