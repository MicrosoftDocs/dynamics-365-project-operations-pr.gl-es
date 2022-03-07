---
title: Engadir membros do equipo desde a grade de membros do equipo
description: Este tema fornece información sobre como pode xestionar recursos dos membros do equipo.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c4ff7792a9a99cbbe791a10dbc5157ffd51de285c02f23471532a09e7a55b031
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008404"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Engadir membros do equipo desde a grade de membros do equipo

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations inclúe un panel de xestor de recursos que ofrece unha visión xeral da demanda e utilización de recursos en toda a organización. Podes usar os gráficos deste panel para visualizar a seguinte información:

- **Demanda de recursos**: O gráfico **Solicitude de recursos activos** mostra os recursos enviados. Os recursos agrúpanse por rol ou proxecto.
- **Demanda de recursos non enviados**: O gráfico **Demanda de recursos non enviados** mostra todos os requisitos de recursos que non se enviaron. Esta gráfica axuda aos xestores de recursos a ver a demanda que non é firme e pode enviarse mediante unha solicitude de recursos.
- **Utilización facturable a semana pasada**: O gráfico **Utilización por rol** mostra a porcentaxe da utilización facturable real da organización por rol fronte a utilización facturable obxectivo por rol.

    > [!NOTE]
    > Para facer que o gráfico **Utilización por rol** estea dispoñible, cree un traballo que execute o fluxo de traballo **UpdateRoleUtilization**. Este traballo recorrente execútase cada sete días para calcular a utilización facturable dos sete días anteriores. Os resultados agrúpanse por rol.

## <a name="manage-project-team-members"></a>Xestionar membros do equipo de proxecto

Os xestores de proxectos poden usar o panel de xestor de recursos para xestionar os recursos dos proxectos. Por exemplo, poden engadir un membro do equipo directamente a un proxecto e reservar un membro do equipo para cumprir os requisitos de recursos capturados por un recurso xenérico.

### <a name="add-a-team-member-directly-to-a-project"></a>Engadir un membro do equipo directamente a un proxecto

Para engadir un membro do equipo directamente a un proxecto, no formulario **Proxectos**, no separador **Equipo**, seleccione **Novo**. Aparecerá a caixa de diálogo **Creación rápida: Membro de equipo de proxecto**. Nesta caixa de diálogo, pode realizar estas tarefas:

- **Reservar un recurso nomeado**: No campo **Recurso reservable**, seleccione o nome do recurso. A seguir, seleccione o rol, estableza o período e seleccione un método de asignación. O recurso nomeado que seleccionou engádese ao proxecto mediante o método de asignación seleccionado e o calendario de recursos.
- **Engadir un recurso xenérico**: Deixe o campo **Recurso reservable** en branco e, a seguir, seleccione o rol, estableza o período e seleccione o método de asignación preferido. Engádese un recurso xenérico ao equipo como marcador de posición. O marcador de posición mantén o patrón de demanda que se usa para reservar recursos nomeados no equipo. O requisito faise segundo o calendario do proxecto.
- **Engadir un recurso nomeado ao equipo sen consumir capacidade do recurso**: No campo **Recurso reservable**, seleccione un recurso. Seleccione o período e logo seleccione **Ningún** como método de asignación. O recurso engádese ao equipo, pero a capacidade do recurso non se consume a través dunha reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservar un membro do equipo para cumprir os requisitos dun recurso xenérico

En Project Operations, pode reservar un recurso xenérico nun equipo do proxecto. Tamén pode especificar o rol, a capacidade requirida e como se distribúe esa capacidade. Para o requisito de recurso, pode especificar os atributos asociados ao recurso xenérico. Estes atributos inclúen habilidades requiridas, a unidade organizativa preferida e recursos preferentes.

Complete os seguintes pasos para especificar as habilidades necesarias nun recurso xenérico para un programador.

1. No formulario **Proxectos**, no separador **Equipo**, seleccione **Novo** para reservar un recurso xenérico.
2. Na vista **Todos os membros do equipo**, na columna **Requisito de recurso**, seleccione a ligazón para engadir as habilidades necesarias para o recurso xenérico.
3. No formulario **Requisito de recurso** que aparece, na grade **Habilidades**, seleccione os puntos suspensivos (**...**) e, a seguir, seleccione **Engadir unha nova característica de requisito** para engadir as habilidades necesarias para o seu programador.
4. No formulario de diálogo **Creación rápida: característica de requisito** que aparece no campo **Característica**, seleccione a habilidade requirida.
5. No campo **Valor de clasificación**, seleccione o nivel de competencia para esa habilidade. 
6. No campo **Requisito de recurso**, estableza o requisito para obter recursos orixe de unidades organizativas ou incluso recursos nomeados. Ao concluír, seleccione **Gardar**.
7. No formulario **Requisito de recurso**, seleccione **Reservar** para cumprir o requisito de recurso. Tamén pode seleccionar o recurso xenérico na grade **Todos os membros do equipo** e, a seguir, seleccione **Reservar**.

    > [!NOTE]
    > Neste exemplo, hai 40 horas requiridas pero non hai horas reservadas reais, porque os recursos xenéricos non teñen reservas. Ademais, non hai horas atribuídas, porque o recurso xenérico se engadiu directamente ao equipo en lugar de engadilo mediante a atribución de tarefas.

    No formulario **Asistente de programación** pode filtrar os recursos dispoñibles segundo os requisitos que se especifican no requisito de recurso. Os recursos clasifícanse segundo os parámetros de ordenación que se especifican no panel de programación.

   Algúns dos filtros máis usados son:

    - **Características xunto cunha clasificación**: Filtrar por habilidades, certificacións e outras calidades de recursos, ademais das clasificacións de competencia.
    - **Roles**: Filtrar por roles predefinidos que se atribúen aos recursos reservables.
    - **Unidades organizativas**: Filtrar os recursos reservables polas unidades organizativas ás que están atribuídos.

8. Se non está satisfeito cos resultados da busca de requisitos iniciais, pode cambiar os criterios de filtro. Expanda o panel **Vista de filtro** á esquerda e, a seguir, seleccione **Buscar** para buscar recursos adicionais. Para cambiar como se clasifican os resultados, seleccione **Ordenar**.
9. Seleccione recursos segundo a demanda que se especifica no requisito, como se indica na parte superior da grade. Pode limpar a selección de celas da grade e deixar aberta esa capacidade do recurso. Só un recurso á vez pode seleccionarse como reservado.
10. Seleccione **Reservar** para reservar o recurso seleccionado e deixar aberto o panel de programación para que poida seleccionar recursos adicionais. Alternativamente, seleccione **Reservar e saír** para reservar o recurso seleccionado e pechar o panel de programación.
11. Volva á vista **Todos os membros do equipo**. Na grade, observe que o recurso xenérico foi substituído polo recurso nomeado, e que figuran 40 horas como reservadas para ese recurso.

    > [!NOTE]
    > Non se amosan horas atribuídas porque se reservaron directamente no equipo. Non foron reservados mediante a atribución de tarefas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Atribuír recursos xenéricos a tarefas e xerar requisitos de recursos

En Project Operations, pode crear tarefas e despois asignarlles recursos xenéricos. A seguir, a demanda de recursos pode ser representada polos marcadores de posición mentres estima a súa programación e cifras financeiras. Pode xerar requisitos de recursos para os recursos xenéricos e cumprilos.

1. No formulario **Proxectos**, no separador **Programación**, seleccione **Engadir** para crear unha tarefa.
2. No campo **Recursos**, seleccione o símbolo de **Selector de recursos**. O Selector de recursos aparece e amosa aos membros do equipo existentes para o proxecto.
3. Introduza o nome do novo recurso xenérico e logo seleccione **Crear**.
4. Na caixa de diálogo **Creación rápida: membro do equipo de proxecto** que aparece, no campo **Rol**, seleccione o recurso requirido. 
5. No campo **Unidade de recursos**, seleccione a unidade organizativa para o recurso xenérico. Seleccione **Gardar**. Agora o membro do equipo xenérico atribúese á tarefa.

   No separador **Equipo**, verá o novo membro xenérico do equipo. Teña en conta que só ten atribuídas horas. Estas horas son a suma de todas as tarefas atribuídas ao membro do equipo xenérico. O membro do equipo xenérico non ten as horas requiridas ou un requisito de recurso.

6. Agora pode atribuír o membro do equipo xenérico a outras tarefas mediante o Selector de recursos.

   Cando termine de atribuír o recurso xenérico a tarefas, pode xerar un requisito de recurso para o recurso xenérico.

7. No separador **Equipo**, seleccione o recurso xenérico e, a seguir, seleccione **Xerar requisito**. Cando se xera o requisito, o membro do equipo xenérico terá horas e unha ligazón para o requisito do recurso.

  Despois de reservar un recurso nomeado, o recurso xenérico elimínase do equipo e substitúese polo recurso nomeado. No separador **Programación**, elimínanse as atribucións do recurso xenérico e substitúense polo recurso nomeado.

  > [!NOTE]
  > Este comportamento só se produce cando un recurso nomeado está totalmente reservado para o requisito de recurso xenérico. Cando un recurso nomeado substitúe parcialmente o requisito de recurso xenérico ou varios recursos nomeados substitúen o requisito de recurso xenérico, o recurso xenérico permanece atribuído á tarefa.

Project Operations non atribúe ambos recursos á tarefa, porque ese comportamento produciría unha programación menos previsible. Neste sinxelo exemplo, é fácil dividir as horas por igual entre dous recursos. Non obstante, en escenarios máis complexos que impliquen múltiples tarefas e múltiples recursos, PSA tería que facer suposicións sobre como debería asignar as reservas que se reciben para varios recursos en varias tarefas.

Por iso, nestes escenarios, o xestor de proxectos é o responsable de analizar as múltiples reservas e atribuílas segundo sexa necesario. Para asignar as reservas, o xestor de proxectos atribúe as tarefas dos recursos xenéricos aos recursos nomeados e logo usa a vista **Conciliación** para asegurarse de que a asignación funciona coas reservas.

### <a name="edit-a-resource-requirement"></a>Editar un requisito de recurso

Despois de que se crease un requisito de recurso, un xestor de proxectos ou xestor de recursos pode querer editar os detalles para refinar os criterios de busca cando se emprega o panel de programación. Para editar o requisito de recurso, siga estes pasos.

1. No formulario **Proxectos**, no separador **Equipo**, seleccione a ligazón a calquera requisito nun recurso xenérico.
2. No formulario **Requisito de recurso** formulario que aparece, introduza a información de campo necesaria

   No formulario **Requisito de recurso**, o xestor de proxectos ou o xestor de recursos tamén pode definir habilidades, roles, preferencias de recursos e a unidade organizativa preferida.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Actualizar as reservas de recursos despois de que sexan reservadas nun proxecto

Despois de engadir un recurso xenérico ou nomeado a un equipo de proxecto, pode cambiar as reservas do recurso.

1. No formulario **Proxecto**, no separador **Equipo**, seleccione un membro do equipo e, a seguir, seleccione **Manter reservas**.
 
   O panel de programación aparece e mostra as reservas do membro do equipo do proxecto. Expanda o rexistro do membro do equipo para ver as horas reservadas con este proxecto e outros proxectos que estean consumindo a capacidade do membro do equipo.

2. Seleccione e arrastre a reserva para estendela ou acurtala. Aparece a caixa de diálogo **Crear reserva de recurso** que permite axustar a reserva.
3. Prema botón dereito na reserva. Pode empregar o menú de atallo para realizar as seguintes accións:

    - Cambiar o estado da reserva
    - Editar a reserva
    - Substituír un recurso no equipo do proxecto

### <a name="change-the-booking-status"></a>Cambiar o estado da reserva

Pode cambiar calquera estado de reserva predefinido ou personalizado.

Os seguintes estados están incluídos en Project Operations:

- **Cancelado**: Cancela a reserva dun recurso e libera a capacidade do recurso.
- **Reserva dura**: Consume a capacidade dun recurso. Unha reserva normalmente ten este estado cando se abre **Manter reservas** dende a grade **Todos os membros do equipo** no formulario **Proxectos**.
- **Reserva branda**: Engade un recurso a un equipo pero non consume a capacidade do recurso. Este estado indica que o recurso reservouse para traballos potenciais, pero aínda ten capacidade se é necesario noutros traballos. Na vista de dispoñibilidade global dos recursos, as reservas brandas teñen un estado diferente das reservas duras.
- **Proposto**: Representa a proposta dun xestor de recursos ou xestor de proxectos para un recurso. As propostas non consumen a capacidade dun recurso e o recurso non se engade ao equipo do proxecto. Para facer unha reserva dura dun recurso no equipo, o xestor de proxectos debe aceptar a proposta.

### <a name="submit-resource-requests"></a>Enviar solicitudes de recursos

As solicitudes de recursos úsanse para cubrir a demanda ou requisito de recursos que debe cumprir un xestor de recursos. Para un recurso xenérico que xa está no equipo, pode enviar unha solicitude de recurso directamente. Pódese realizar unha solicitude de recursos de dous xeitos:

- O xestor de recursos cumpre directamente a solicitude. Neste caso, o recurso xenérico substitúese por unha reserva dura que ten un recurso nomeado.
- O xestor de recursos propón un recurso ao xestor de proxectos e o xestor de proxectos aproba ou rexeita o recurso proposto.

#### <a name="direct-fulfillment-of-resource-requests"></a>Cumprimento directo das solicitudes de recursos

Cando se xera un requisito de recurso, o xestor de proxectos pode enviar unha solicitude de recurso para un recurso xenérico seleccionando o recurso e, a seguir, seleccionando **Enviar solicitude**. Os comentarios sobre o recurso pódense proporcionar ao xestor de recursos que cumpra a solicitude. Despois de enviar a solicitude, o campo **Estado** para o membro do equipo cambiase a **Enviado**. Cando o xestor de recursos cumpre a solicitude, o membro do equipo xenérico substitúese polo recurso nomeado na grade **Todos os membros do equipo**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Usar unha proposta de recurso para solicitudes de recursos

En lugar de reservar directamente un recurso nunha solicitude de recurso, un xestor de recursos pode propor un recurso ao xestor de proxectos. Un xestor de recursos pode usar esta opción cando non se dispón dunha coincidencia exacta para os requisitos. Cando un xestor de recursos propón un recurso, o xestor de proxectos ve que o campo **Estado** para o membro do equipo xenérico cambia a **Necesita revisión**.

Pode ver o recurso proposto xunto cunha visualización do efecto da reserva da proposta. 

1. Prema dúas veces no membro do equipo que ten o estado de **Necesita revisión**. 
2. Seleccione o separador **Recursos propostos**.
3. Seleccione **Aceptar todas as propostas** para aceptar todos os recursos propostos ou **Rexeitar todas as propostas** para rexeitalos. Se acepta os recursos propostos, farase unha reserva dura no proxecto como membros do equipo e substitúen aos recursos xenéricos.

> [!NOTE]
> Debe aceptar ou rexeitar todos os recursos propostos. Non pode aceptalos ou rexeitalos parcialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituír un recurso no equipo do proxecto

Ás veces, un xestor de proxectos debe substituír un membro reservado dun equipo nun proxecto.

1. No formulario **Proxectos**, no separador **Equipo**, seleccione un recurso que necesita un substituto e, a seguir, seleccione **Manter reservas**.
2. Expanda o recurso para ver os proxectos aos que está asignado.
3. Co botón secundario, prema o proxecto e, a seguir, seleccione **Substituír recurso**.
4. Se coñece o recurso que desexa que substitúa ao recurso actual, seleccione ou escriba o nome e, a seguir, seleccione **Volver atribuír**.

Ou se precisa buscar un recurso, complete os seguintes pasos.

1. Seleccione **Buscar substitución**.

   O Asistente de programación devolve unha lista de substitutos dispoñibles. No Asistente de programación, pode filtrar os recursos dispoñibles para atopar un substituto adecuado.

2. Para substituír o recurso, seleccione o recurso que desexe e, a seguir, seleccione **Substituír**.   

   As reservas e atribucións substitúense co novo recurso.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Conciliar reservas de membros de equipo e atribucións

Para os membros do equipo, as reservas e atribucións están emparelladas libremente. Noutras palabras, os recursos poden ter atribucións pero sen reservas ou poden ter reservas pero sen atribucións. O ideal sería que as reservas e atribucións estivesen aliñadas, de xeito que os recursos teñan capacidade comprometida para realizar as atribucións de tarefas. Non obstante, as reservas poden estar baseadas na dispoñibilidade e os calendarios de tarefas poderían cambiar a medida que o proxecto continúe. Polo tanto, o emparellamento libre de reservas e atribucións proporciona flexibilidade.

Projecto Operations ten unha grade **Conciliación** que permite aos xestores de proxectos concilien as reservas dos membros do equipo e as súas atribucións para os equipos de proxecto.

O separador **Conciliación** mostra reservas e atribucións ata o nivel da tarefa individual para cada membro do equipo. Amosa horas en celas que representan períodos de tempo desde meses ata días.

O separador tamén mostra un total neto global do proxecto, xunto cunha columna total.

Para cada recurso, o separador calcula a diferenza entre as reservas do membro do equipo e un resumo das atribucións do membro do equipo. O ideal sería que esta diferenza fose 0 (cero). Noutras palabras, non debería haber ningunha diferenza entre reservas e atribucións. As diferenzas están coloreadas e sombreadas para chamar a atención sobre dúas condicións:

- **Escaseza de reservas**: Prodúcese cando un recurso ten máis atribucións que reservas. Debido a que non se reservou esta capacidade, un xestor de proxectos podería querer corrixir esta condición ampliando as reservas do recurso para cubrir o déficit.
- **Exceso de reservas**: Prodúcese cando se reservou un recurso para o proxecto pero non foi asignado a tarefas. Esta condición pode ser aceptable nos casos en que o recurso foi reservado para o proxecto antes de que se producise a atribución de tarefas. Non obstante, noutros casos, non está previsto atribuír tarefas ao recurso. Nestes casos, o xestor do proxecto debería considerar a cancelación das reservas do recurso, de xeito que a capacidade poida utilizarse para outro proxecto.

Nalgúns casos, cando ve o tempo a un nivel superior ao nivel de día (por exemplo, a nivel de mes), pode que vexa unha diferenza neta de cero para un recurso. Noutras palabras, reservas = atribucións. Non obstante, se ve o tempo a nivel de semana, é posible que vexa que hai atribucións de cero horas e reservas de 40 horas na primeira semana, pero atribucións de 40 horas e reservas de cero horas na segunda semana. En xeral, as reservas e atribucións conciliaranse, pero difiren dunha semana a outra.

Cando vexa o tempo a niveis máis altos, as celas do separador **Conciliación** ten un indicador para informar de que hai diferenzas a niveis máis baixos. Prema dúas veces nunha cela para facer zoom para ver a diferenza. A seguir, pode premer co botón dereito para facer zoom. Ao seleccionar un recurso e despois seleccionar **Seguinte diferenza** na barra de ferramentas da grade, pode ir á seguinte diferenza entre reservas e atribucións para ese recurso. Seleccione **Diferenza anterior** para volver. Tamén pode desactivar o indicador de diferenzas e o comportamento de navegación en **Configuración**.

Se ten atribucións de tarefas para un recurso pero non ten reservas, no formulario **Proxectos**, no separador **Conciliación**, seleccione a escaseza de reservas e logo seleccione **Estender a reserva**. Aparece a caixa de diálogo **Estender reserva** e mostra a reserva que é necesaria para resolver a escaseza do recurso. A caixa de diálogo tamén amosa as reservas existentes do recurso en todos os proxectos ou outras entidades programables. Se selecciona **Aceptar** para crear a reserva para o recurso, independentemente da dispoñibilidade dese recurso, pode causar un exceso de reservas.

O xestor de proxectos ou xestor de recursos pode utilizar o panel de programación para xestionar calquera situación na que un recurso estea sobrecargado fóra da súa capacidade.


[!INCLUDE[footer-include](../includes/footer-banner.md)]