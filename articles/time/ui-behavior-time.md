---
title: Comportamento da IU de entrada de tempo
description: Este tema ofrece información sobre o comportamento da IU para a entrada de tempo.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0cb62231eb3b387b610b7510023994dce66b1cc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995889"
---
# <a name="time-entry-ui-behavior"></a>Comportamento da IU de entrada de tempo

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


A nova grade de **Entrada de tempo semanal** é un control personalizado que ten dúas seccións principais, **Dimensións** e **Duración**.

## <a name="keyboard-shortcuts"></a>Atallos de teclado
| Acción        | Atallo                  |
|------------   |------------------------   |
| Nova           | Alt + Maiús + n           |
| Copiar fila      | Alt + Maiús + c           |
| Editar entrada    | Alt + Maiús + e           |
| Editar fila      | Alt + Maiús + Ctrl + e    |
| Abrir entrada    | Alt + Maiús + o           |
| Enviar        | Alt + Maiús + s           |
| Recuperar        | Alt + Maiús + r           |
| Delete        | Alt + Maiús + d           |
| Copiar semana     | Alt + Maiús + w           |

## <a name="dimensions"></a>Dimensións
A sección **Dimensións** mostra as dimensións coas que se pode introducir o tempo. Admítense as seguintes dimensións listas para usar:

  - Project
  - Tarefa do proxecto
  - Rol
  - Tipo
  - Estado da entrada

A sección **Dimensións** non permite a edición entre liñas. Esta sección está apoiada por unha vista que permite engadir campos personalizados á grade de entrada de tempo semanal.

## <a name="duration"></a>Duración
A sección Duración mostra os días da semana como cabeceiras de columna. Esta sección permite a edición entre liñas. Despois de que se cree unha fila de entrada de tempo coas dimensións apropiadas, os usuarios poden introducir rapidamente, entre liñas, o tempo que dedicaron nesas dimensións.

## <a name="create-a-new-time-entry"></a>Crear unha nova entrada de tempo

1. Na grade de entrada de tempo, seleccione **Nova**. 
2. Na caixa de diálogo **Creación rápida de entrada de tempo**, seleccione a data da entrada de tempo.
3. Introduza datos para as dimensións **Proxecto**, **Tarefa do proxecto**, **Función** e **Duración**. Esta información debe engadirse en minutos, horas ou días escribindo **h**, **m** o **d**, xunto co número. 
4. Introduza unha descrición para a entrada e comentarios que se poden compartir externamente sobre a entrada de tempo. 

Cando garda a entrada, os valores introducidos aparecen na sección **Dimensións**. A información introducida no campo **Duración** aparece un campo na data na que se creou a entrada de tempo.

Os campos de busca están apoiados por vistas do sistema. Por exemplo, despois de que un usuario entre nun proxecto, o campo **Tarefa de proxecto** configúrase na vista **Copiar** por defecto. Para crear entradas de tempo para tarefas que non están atribuídas a un usuario, seleccione **Cambiar vista** na caixa de diálogo de busca e logo seleccione a vista **Todas as tarefas activas do proxecto**.

## <a name="edit-a-time-entry"></a>Editar unha entrada de tempo 
Os detalles dalgúns campos na páxina de entrada de tempo, como **Descrición** e **Comentarios externos**, non aparecen na grade de entrada de tempo semanal No seu lugar, un pequeno indicador triangular aparece nas celas de **Duración** que teñen estes detalles adicionais. 

1. Para editar unha entrada de tempo, seleccione a cela que desexa actualizar na entrada de tempo.
2. Seleccione **Editar detalles** para actualizar os datos no panel **Formulario principal de entrada de tempo**. 

## <a name="copy-a-time-entry-row"></a>Copiar una fila de entrada de tempo
Unha vez creada a fila, pode seleccionar **Copiar fila** para copiar toda a fila a unha nova fila. Cando se copia deste xeito unha fila, tamén se copian dimensións e duracións. Tamén pode seleccionar **Editar fila** para actualizar os valores de dimensión e duracións na sección **Duración**.

## <a name="open-a-time-entry-behavior"></a>Abrir un comportamento de entrada de tempo
Para apoiar a entrada rápida e óptima nos campos máis destacados, a grade de entrada de tempo semanal mostra un subconxunto de dimensións e duracións de tempo seleccionadas. Para ver todos os detalles dunha entrada de tempo única, en **Editar entrada**, seleccione **Abrir**.

## <a name="submit-a-time-entry"></a>Enviar unha entrada de tempo
Pode enviar unha única entrada ou un grupo de entradas de tempo seleccionando un bloque de celas ou unha fila de entrada de tempo enteira e, a seguir, seleccionando **Enviar**. As entradas de tempo enviadas aparecen como entradas que están pendentes de aprobación na páxina **Aprobación** dos responsables de aprobacións. Despois de que se envíen con éxito as entradas, non se poden editar.

## <a name="recall-a-time-entry"></a>Recuperar unha entrada de tempo
Pode recuperar as entradas de tempo que enviou. Pode recuperar unha única entrada de tempo, un bloque de entradas de tempo ou unha fila enteira de entradas de tempo. Pódense editar as entradas do tempo recuperadas.

## <a name="time-entry-status"></a>Estado da entrada de tempo

- **Borrador**: As novas entradas de tempo terán automaticamente un estado de **Borrador**. Só as entradas de tempo que teñen un estado de **Borrador** se poden eliminar.
- **Enviada**: Cando se envía unha entrada de tempo, o estado actualízase a **Enviada**. 
- **Aprobada**: Cando se aproba unha entrada de tempo, o estado actualízase a **Aprobada**. 
- **Devolta**: Se se rexeita unha entrada de tempo, o estado actualízase a **Devolta** e a entrada está dispoñible para a súa corrección e reenvío. 

## <a name="view-rejection-comments"></a>Ver comentarios sobre o rexeitamento
Cando un responsable de aprobacións rexeita unha entrada de tempo, pode engadir comentarios para axudar ao recurso a comprender o motivo do rexeitamento. Para ver os comentarios de rexeitamento dunha entrada de tempo, seleccione **Abrir entrada**. Os comentarios de rexeitamento mostraranse na liña de tempo. O usuario pode responder aos comentarios de rexeitamento antes de volver enviar a entrada.

## <a name="copy-week"></a>Copiar semana
Despois de que se creen algunhas entradas de tempo, os usuarios poden crear varias entradas de tempo ao mesmo tempo.

1. No formulario **Entradas de tempo**, seleccione **Copiar semana** para crear en masa entradas de tempo adicionais. 
2. Na caixa de diálogo **Copiar** na sección **Período desde**, utilice os campos **Data de inicio** e **Data de finalización** para definir o intervalo de datas do que vai copiar as entradas de tempo. 
3. Na sección **Período ata**, no campo **Data de inicio**, especifique a data para a que se van crear as entradas de tempo. 
4. Seleccione **Copiar**. Para a data especificada no **Período ata**, créase unha copia das entradas de tempo para o día correspondente da semana no **Período desde**. Por exemplo, a entrada de tempo para o luns da semana pasada cópiase no luns da semana que se especifica como **Período ata**.

## <a name="import"></a>Importar
O mesmo proceso básico úsase para importar desde reservas, atribucións e intercambios. Pode especificar o intervalo de datas do que se importan as reservas e, a seguir, seleccionar explicitamente as reservas deben copiarse como borradores de entradas de tempo. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
