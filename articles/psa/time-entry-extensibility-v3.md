---
title: Personalizar entrada de tempo semanal
description: Este tema proporciona información sobre como implantar regras de negocio personalizadas para apoiar as prácticas dunha organización.
author: stsporen
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
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
ms.openlocfilehash: cc395e77e987dac062251ef87fcf8295305178e2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076219"
---
# <a name="customize-weekly-time-entry"></a>Personalizar entrada de tempo semanal 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En Microsoft Dynamics 365 Project Service Automation versión 3.3, Microsoft introduciu unha rede moderna que permite aos recursos de proxectos introducir rapidamente o tempo para ata unha semana cada vez. A nova grade de entrada de tempo semanal pode mostrar os totais das entradas por data, fila ou semana. Os recursos poden facer copias das entradas de tempo da semana e tamén copiar en masa das semanas anteriores. Os personalizadores do sistema poden personalizar a vista engadindo campos, engadindo buscas a outras entidades e implantando regras de negocio personalizadas para apoiar as prácticas da súa organización.

Accédese á entrada de tempo e á nova grade de tempo semanal través do mapa do sitio. A experiencia de entrada de tempo personalizada non extensible que formaba parte das versións anteriores de PSA substituíuse pola grade de entrada de tempo semanal extensible, e tamén por unha experiencia alternativa na grade e o calendario de só lectura. Por mor deste cambio, os usuarios poden introducir o tempo en cantidades semanais.

## <a name="page-layout"></a>Deseño da páxina
A nova grade de entrada de tempo semanal é un control personalizado que ten unha barra de ferramentas e dúas seccións principais, **Dimensións** e **Duración**. A barra de ferramentas inclúe un botón que se aplica só a este control personalizado para a grade de entrada de tempo. Pola contra, os botóns do panel de acción na parte superior da páxina aplícanse aos tres tipos de controis que son compatibles para a entrada de tempo: o control semanal de entrada de tempo, o control de só lectura e o control de calendario.

### <a name="dimensions"></a>Dimensións
A sección **Dimensións** mostra, como cabeceiras de columna, todas as dimensións coas que se pode introducir o tempo. Admítense as seguintes dimensións listas para usar:

- Proxecto
- Tarefa do proxecto
- Rol
- Tipo
- Estado da entrada

A sección **Dimensións** non permite a edición entre liñas. Esta sección está apoiada por unha vista que permite engadir campos personalizados á grade de entrada de tempo semanal. Para obter información sobre como engadir campos personalizados, consulte a sección "Extensibilidade" máis adiante neste tema.

### <a name="duration"></a>Duración
A sección Duración mostra os días da semana como cabeceiras de columna. Esta sección permite a edición entre liñas. Despois de que se cree unha fila de entrada de tempo que teña as dimensións apropiadas, os usuarios poden introducir rapidamente, entre liñas, o tempo que dedicaron nesas dimensións.

## <a name="create-a-new-time-entry"></a>Crear unha nova entrada de tempo
Para crear unha nova entrada de tempo na grade de entrada de tempo, seleccione **Nova**. Aparece a caixa de diálogo **Creación rápida de entrada de tempo**. Nesta caixa de diálogo, os usuarios poden seleccionar a data de entrada de tempo e logo introducir datos para as dimensións **Proxecto** , **Tarefa de proxecto** , **Rol** e **Duración** en minutos, horas ou días escribindo **h** , **m** ou **d** , xunto co número. Os usuarios tamén poden introducir unha descrición e comentarios que se poden compartir externamente para a entrada de tempo. Cando os usuarios gardan os seus cambios, os valores que introduciron con respecto ás dimensións aparecen na sección **Dimensións**. A información sobre a duración que introduciron no campo **Duración** aparece un campo na data na que se creou a entrada de tempo.

Os campos de busca están apoiados por vistas do sistema. Por exemplo, despois de que un usuario entre nun proxecto, o campo **Tarefa de proxecto** configúrase na vista **Copiar** por defecto. Para crear entradas de tempo para tarefas que non están atribuídas a un usuario, seleccione **Cambiar vista** na caixa de diálogo de busca e logo seleccione a vista **Todas as tarefas activas do proxecto**.

## <a name="edit-a-time-entry"></a>Editar unha entrada de tempo
Os detalles dalgúns campos na páxina de entrada de tempo, como **Descrición** e **Comentarios externos** , non aparecen na grade de entrada de tempo semanal No seu lugar, un pequeno indicador triangular aparece nas celas de duración que teñen estes detalles adicionais. Seleccione a cela e logo seleccione **Editar detalles** para ver os datos no panel **Edición rápida**. Para editar ou actualizar os detalles dunha entrada de tempo específica que non forma parte da grade de entrada de tempo semanal, os usuarios deben abrir o panel **Edición rápida**.

## <a name="copy-a-time-entry-row"></a>Copiar una fila de entrada de tempo
Unha vez creada a primeira fila de entrada, os usuarios poden seleccionar **Copiar fila** para copiar toda a fila a unha nova fila. Cando se copia deste xeito unha fila, tamén se copian dimensións e duracións. Os usuarios tamén poden seleccionar **Editar fila** para actualizar os valores de dimensión e duracións entre liñas na sección **Duración**.

## <a name="open-a-time-entry"></a>Abrir unha entrada de tempo
Para apoiar a entrada rápida e óptima nos campos máis destacados, a grade de entrada de tempo semanal mostra un subconxunto de dimensións e duracións de tempo seleccionadas. Para ver todos os detalles dunha entrada de tempo única, en **Editar entrada** , seleccione **Abrir**.

## <a name="submit-a-time-entry"></a>Enviar unha entrada de tempo
Os usuarios poden enviar unha única entrada ou un grupo de entradas de tempo seleccionando un bloque de celas ou unha fila de entrada de tempo enteira e, a seguir, seleccionando **Enviar**. As entradas de tempo enviadas aparecen como entradas que están pendentes de aprobación na páxina **Aprobación** dos responsables de aprobacións. Despois de que se envíen con éxito as entradas, non se poden editar.

## <a name="recall-a-time-entry"></a>Recuperar unha entrada de tempo
Pode recuperar as entradas de tempo que enviou. Pode recuperar unha única entrada de tempo, un bloque de entradas de tempo ou unha fila enteira de entradas de tempo. As entradas de tempo recuperadas están dispoñibles para que os recursos as editen.

## <a name="time-entry-status"></a>Estado da entrada de tempo
As novas entradas de tempo terán automaticamente un estado de **Borrador**. Cando se envía unha entrada de tempo, o estado actualízase a **Enviado**. Cando se aproba unha entrada de tempo, o estado actualízase a **Aprobado**. Se se rexeita unha entrada de tempo, o estado actualízase a **Devolto** e a entrada está dispoñible para a súa corrección e reenvío. Só as entradas de tempo que teñen un estado de **Borrador** se poden eliminar.

## <a name="view-rejection-comments"></a>Ver comentarios sobre o rexeitamento
Cando un responsable de aprobacións rexeita unha entrada de tempo, pode engadir comentarios de rexeitamento para axudar ao recurso a comprender o motivo do rexeitamento. Para ver os comentarios de rexeitamento dunha entrada de tempo, seleccione **Abrir entrada**. Os comentarios de rexeitamento mostraranse na liña de tempo. Na liña de tempo, o recurso pode responder aos comentarios sobre o rexeitamento antes de enviar de novo a entrada.

## <a name="copy-week"></a>Copiar semana
Despois de crear unhas poucas entradas de tempo, os usuarios poden seleccionar **Copiar semana** para crear entradas de tempo adicionais en masa. Aparece a caixa de diálogo **Copiar**. Na sección **Período desde** , utilice os campo **Data de inicio** e **Data de finalización** , para definir o intervalo de datas do que vai copiar as entradas de tempo. Na sección **Período ata** , no campo **Data de inicio** , especifique a data para a que se van crear as entradas de tempo. Seleccione **Copiar**. Para a data especificada no período "ata", créase unha copia das entradas de tempo para o día correspondente da semana no período "desde". Por exemplo, a entrada de tempo para o luns da semana pasada cópiase no luns da semana que se especifica como período "ata".

## <a name="import"></a>Importación
O mesmo proceso básico úsase para importar desde reservas, atribucións e intercambios. Os usuarios poden especificar o intervalo de datas do que se importan as reservas. Despois deberán seleccionar explicitamente as reservas que se deberían copiar nos borradores de entradas de tempo. Na versión anterior, as entradas suxeridas aparecían na grade e no calendario, e perdíanse ao actualizar a sesión.

## <a name="extensibility"></a>Extensibilidade
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Engadir campos personalizados que teñan buscas a outras entidades
Hai tres pasos principais para engadir un campo personalizado á grade de entrada de tempo semanal.

1.  Engada o campo personalizado á caixa de diálogo de creación rápida.
2.  Configure a grade para mostrar o campo personalizado.
3.  Engada o campo personalizado ao fluxo de tarefas de edición de filas ou ao fluxo de tarefas de edición de celas, segundo corresponda.

Tamén debe asegurarse de que o novo campo ten as validacións requiridas no fluxo de tarefas de edición de filas ou celas. Como parte deste paso, ten que bloquear o campo, en función do estado da entrada de tempo.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Engadir o campo personalizado á caixa de diálogo de creación rápida.
Debe engadir o campo personalizado á caixa de diálogo de creación rápida de entrada de tempo. para que os usuarios poidan introducir un valor para el cando engaden entradas de tempo empregando botón **Novo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grade para mostrar o campo personalizado
Hai dous xeitos de engadir un campo personalizado á grade de entrada de tempo semanal. A primeira opción é personalizar a vista **As miñas entradas por de tempo semanal** e engádalle o campo personalizado. Pode escoller a posición e o tamaño do campo personalizado na grade editando esas propiedades na vista.

A segunda opción é crear unha nova vista de entrada de tempo personalizada e definila como vista por defecto. Esta vista debería conter os campos **Descrición** e **Comentarios externos** , ademais das columnas que desexa ter na grade. Pode escoller a posición, o tamaño e a orde de clasificación por defecto da grade editando esas propiedades na vista. A seguir, configure o control personalizado para esta vista para que sexa un control de **Grade de entrada de tempo**. Engada este control á vista e seleccióneo para web, teléfono e tableta. A seguir, configure os parámetros para a grade de entrada de tempo semanal. Configure o campo **Data de inicio** en **msdyn_date** , configure o campo **Duración** en **msdyn_duration** e configure o campo **Estado** en **msdyn_entrystatus**. Para a vista por defecto, o campo **Lista de estado de só lectura** está configurado como **192350002,192350003,192350004** , o campo **Fluxo de tarefas de edición de filas** está configurado como **msdyn_timeentryrowedit** , e o campo **Fluxo de tarefas de edición de celas** está configurado como **msdyn_timeentryedit**. Pode personalizar estes campos para engadir ou eliminar o estado de só lectura ou para empregar unha experiencia baseada en tarefas (TBX) diferente para a edición de filas ou celas. Estes campos deben estar vencellados a un valor estático.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Engadir o campo personalizado ao fluxo de tarefas de edición adecuado
As páxinas de TBX que se usan para editar pódense atopar en **Procesos**. As páxinas predefinidas son **Project Service - Edición de fila de entrada de tempo** e **Servizo de proxectos - Edición de entrada de tempo**. Pode editar estas páxinas predefinidas ou crear novas páxinas de TBX personalizadas.

> [!NOTE] 
> Ambas opcións eliminarán algún filtro listo para usar nas entidades **Proxecto** e **Tarefa do proxecto** , de xeito que todas as vistas de busca das entidades serán visibles. Ao principio, só son visibles as vistas de busca relevantes.

Debe determinar o fluxo de tarefas adecuado para o campo personalizado. Moi probablemente, se engadiu o campo á grade, debería ir no fluxo de tarefas de edición de filas que se usa para campos que se aplican a toda a fila de entradas de tempo. Se o campo personalizado ten un valor único todos os días, como un campo personalizado para **Hora de finalización** , debería ir no fluxo de tarefas de edición de celas.

Para engadir un campo personalizado a un fluxo de tarefas, arrastre o elemento **Campo** á posición adecuada na páxina e logo estableza as súas propiedades. Estableza a propiedade **Fonte** en **Entrada horaria** e estableza a propiedade **Campo de datos** no campo personalizado. A propiedade **Campo** especifica o nome en pantalla na páxina de TBX. Seleccione **Aplicar** para gardar os cambios no campo. A seguir, seleccione **Actualizar** para gardar os cambios na páxina.

Para usar unha nova páxina de TBX personalizada, cree un novo proceso. Estableza a categoría en **Fluxo do proceso de negocio** , configure a entidade en **Entrada de tempo** e configure o tipo de proceso de negocio en **Executar o proceso como fluxo de tarefas**. En **Propiedades** , a propiedade **Nome da páxina** debería configurarse segundo o nome en pantalla da páxina. Engada todos os campos relevantes á páxina de TBX. Garde e active o proceso, e, a seguir, actualice a propiedade de control personalizado para o fluxo de tarefas correspondente ao valor de **Nome** no proceso.

### <a name="add-new-option-set-values"></a>Engadir valores de novo conxunto de opcións
Para engadir valores de conxunto de opcións a un campo listo para usar, abra a páxina de edición do campo e, a seguir, en **Tipo** , seleccione **Editar** xunto ao conxunto de opcións. A seguir, engada unha nova opción que teña unha etiqueta e unha cor personalizadas. Se desexa engadir un novo estado de entrada de tempo, o campo listo para usar denomínase **Estado de entrada** , non **Estado**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designe un novo estado de entrada de tempo como só de lectura
Para designar un novo estado de entrada de tempo como só de lectura, engada o novo valor de entrada de tempo (o número, non a etiqueta) á propiedade **Lista de estado de só lectura**. A parte editable da grade de entrada de tempo bloquearase para as filas que teñan o novo estado.
A seguir, engada regras de negocio para bloquear todos os campos nas páxinas de TBX **Edición de fila de entrada de tempo** e **Edición de entrada de tempo**. Pode acceder ás regras de negocio para estas páxinas abrindo o editor fluxo do proceso de negocio para a páxina e logo seleccionando **Regras de negocio**. Pode engadir o novo estado á condición nas regras de negocio existentes ou pode engadir unha nova regra de negocio para o novo estado.

### <a name="add-custom-validation-rules"></a>Engadir regras de validación personalizadas
Hai dous tipos de regras de validación que pode engadir para a experiencia de grade de entrada de tempo semanal: • Regras de negocio do lado do cliente que funcionan nas caixas de diálogo de creación rápida e nas páxinas de TBX • Validacións de complemento do lado do servidor que se aplican a todas as actualizacións de entradas de tempo.

#### <a name="business-rules"></a>Regras de negocio
Use regras de negocio para bloquear e desbloquear campos, introducir valores predefinidos en campos e definir validacións que requiran información só do rexistro de entrada de tempo actual. Pode acceder ás regras de negocio para unha páxina de TBX abrindo o editor fluxo do proceso de negocio para a páxina e logo seleccionando **Regras de negocio**. Pode editar as regras de negocio existentes ou engadir unha nova regra de negocio. Para validacións aínda máis personalizadas, pode utilizar unha regra de negocio para executar JavaScript.

#### <a name="plug-in-validations"></a>Validacións de complementos
Debe usar as validacións de complementos para calquera validación que requira máis contexto do que está dispoñible nun rexistro de entrada única ou para calquera validación que desexe executar nas actualizacións entre liñas na grade. Para completar a validación, cree un complemento personalizado na entidade **Entrada de tempo**.

> [!IMPORTANT] 
> Na actualidade, un problema coñecido nas páxinas de TBX impide aos usuarios corrixir información e volver a seleccionar Feito cando unha actualización mostra un erro nunha validación de complemento. Como solución, configure as validacións de regras de negocio para evitar o máximo posible esta situación.
