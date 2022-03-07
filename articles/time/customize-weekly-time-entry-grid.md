---
title: Ampliación das entradas de tempo
description: Este tema ofrece información sobre como os programadores poden ampliar o control de entradas de tempo.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 190ad9e1f9ced690aee953ed992bf7aa2844c3b3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076031"
---
# <a name="extending-time-entries"></a>Ampliación das entradas de tempo

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations inclúe un control personalizado de entradas de tempo ampliables. Este control inclúe as seguintes funcionalidades:

- Introducir o tempo horizontalmente durante unha semana
- Totais por día, fila ou semana
- Copiar filas ou semanas
- Entrada de tempo a través de HH:mm ou HH.hh (convértese automaticamente a HH.hh)
- Importar desde atribucións, reservas ou compromisos

É posible ampliar as entradas de tempo en dúas áreas:
- [Engadir entradas de tempo personalizadas para o seu propio uso](#add)
- [Personalizar o control de entradas de tempo](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Engadir entradas de tempo personalizadas para o seu propio uso

As entradas de tempo son unha entidade básica utilizada en varias situacións. Na onda 1 de abril de 2020, introduciuse a solución básica de TESA. TESA ofrece unha entidade de **Configuración** e un novo rol de seguranza **Usuario de entrada de tempo**. Os novos campos, **msdyn_start** e **msdyn_end**, que teñen unha relación directa con **msdyn_duration**, tamén se incluíron. A nova entidade, rol de seguranza, e os campos permiten un enfoque máis unificado do tempo en múltiples produtos.


### <a name="time-source-entity"></a>Entidade de orixe de tempo
| Campo | Descripción | 
|-------|------------|
| Nome  | O nome da entrada de orixe de tempo empregada como valor de selección cando se crean entradas de tempo. |
| Orixe de tempo por defecto [Orixe de tempo: isdefault] | Por defecto, só se pode marcar unha orixe de tempo de xeito predefinido. Isto permite que as entradas sexan por defecto unha orixe de tempo se non se especifica unha. |
|Tipo de orixe de tempo [Orixe do tempo: sourcetype] | O tipo de orixe é unha opción (Tipo de orixe de entrada de tempo) que permite a asociación da orixe de tempo a unha aplicación. Microsoft reserva valores superiores a 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entradas de tempo e entidade de orixe de tempo
Cada entrada de tempo está asociada a un rexistro de orixe de tempo. Este rexistro determina como e que aplicacións deben procesar a entrada de tempo.

As entradas de tempo sempre son un bloque de tempo contiguo co inicio, o final e a duración ligados.

A lóxica actualizará automaticamente o rexistro de entrada de tempo nas seguintes situacións:

- Se se proporcionan dous dos tres campos seguintes, o terceiro calcúlase automaticamente: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Os campos **msdyn_start** e **msdyn_end** son conscientes do fuso horario.
- As entradas de tempo creadas con só **data_msdyn** e **msdyn_duration** especificados comezarán á media noite. Os campos **msdyn_start** e **msdyn_end** actualizaranse como corresponda.

#### <a name="time-entry-types"></a>Tipos de entradas de tempo

Os rexistros de entrada de tempo teñen un tipo asociado que define o comportamento no fluxo de envío para a aplicación asociada.

|Etiqueta | Valor|
|-----|-----|
|En pausa   |192,355,000|
|Viaxe | 192,355,001|
|Horas extra   | 192,354,320|
|Traballar   | 192,350,000|
|Ausencia    | 192,350,001|
|Vacacións   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personalizar o control de entradas de tempo semanal
Os programadores poden engadir campos e buscas adicionais a outras entidades e implementar regras de ne personalizadas para apoiar os seus escenarios empresariais.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Engadir campos personalizados con buscas a outras entidades
Hai tres pasos principais para engadir un campo personalizado á grade de entrada de tempo semanal.

1. Engada o campo personalizado á caixa de diálogo de creación rápida.
2. Configure a grade para mostrar o campo personalizado.
3. Engada o campo personalizado ao fluxo de tarefas de edición de filas ou ao fluxo de tarefas de edición de celas.

Asegúrese de que o novo campo ten as validacións requiridas no fluxo de tarefas de edición de filas ou celas. Como parte deste paso, bloquee o campo en función do estado da entrada de tempo.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Engadir o campo personalizado á caixa de diálogo de creación rápida.
Engada o campo personalizado á caixa de diálogo **Creación rápida de entrada de tempo**. Despois, cando se engaden as entradas de tempo, pode introducirse un valor seleccionando **Nova**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grade para mostrar o campo personalizado
Hai dous xeitos de engadir un campo personalizado á grade de entrada de tempo semanal:

  - Personalizar unha vista e engadir un campo personalizado
  - Crear unha nova entrada de tempo personalizada por defecto 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Personalizar unha vista e engadir un campo personalizado

Personalice a vista **As miñas entradas de tempo semanal** e engádalle o campo personalizado. Pode escoller a posición e o tamaño do campo personalizado na grade editando as propiedades na vista.

#### <a name="create-a-new-default-custom-time-entry"></a>Crear unha nova entrada de tempo personalizada por defecto

Esta vista debería conter os campos **Descrición** e **Comentarios externos**, ademais das columnas que desexa ter na grade. 

1. Escolla a posición, o tamaño e a orde de clasificación por defecto da grade editando esas propiedades na vista. 
2. Configure o control personalizado para esta vista para que sexa un control de **Grade de entrada de tempo**. 
3. Engada este control á vista e seleccióneo para web, teléfono e tableta. 
4. Configure os parámetros para a grade de entrada de tempo semanal. 
5. Configure o campo **Data de inicio** en **msdyn_date**, configure o campo **Duración** en **msdyn_duration** e configure o campo **Estado** en **msdyn_entrystatus**. 
6. Para a vista predefinida, o campo **Lista de estado de só lectura** está definido como **192350002,192350003,192350004**. O campo **Fluxo de tarefas de edición de filas** está definido como **msdyn_timeentryrowedit**. O campo **Fluxo de tarefas de edición de celas** está definido como **msdyn_timeentryedit**. 
7. Pode personalizar estes campos para engadir ou eliminar o estado de só lectura ou para empregar unha experiencia baseada en tarefas (TBX) diferente para a edición de filas ou celas. Estes campos agora están vencellados a un valor estático.


> [!NOTE] 
> Ambas opcións eliminarán algún filtro listo para usar nas entidades **Proxecto** e **Tarefa do proxecto**, de xeito que todas as vistas de busca das entidades serán visibles. Ao principio, só son visibles as vistas de busca relevantes.

Determine o fluxo de tarefas adecuado para o campo personalizado. Se engadiu o campo á grade, debería ir no fluxo de tarefas de edición de filas que se usa para campos que se aplican a toda a fila de entradas de tempo. Se o campo personalizado ten un valor único todos os días, como un campo personalizado para **Hora de finalización**, debería ir no fluxo de tarefas de edición de celas.

Para engadir un campo personalizado a un fluxo de tarefas, arrastre o elemento **Campo** á posición adecuada na páxina e logo estableza as propiedades do campo. Estableza a propiedade **Fonte** en **Entrada horaria** e estableza a propiedade **Campo de datos** no campo personalizado. A propiedade **Campo** especifica o nome en pantalla na páxina de TBX. Seleccione **Aplicar** para gardar os cambios no campo e logo seleccione **Actualizar** para gardar os cambios na páxina.

Para usar unha nova páxina de TBX personalizada, cree un novo proceso. Estableza a categoría en **Fluxo do proceso de negocio**, configure a entidade en **Entrada de tempo** e configure o tipo de proceso de negocio en **Executar o proceso como fluxo de tarefas**. En **Propiedades**, a propiedade **Nome da páxina** debería configurarse segundo o nome en pantalla da páxina. Engada todos os campos relevantes á páxina de TBX. Garde e active o proceso. Actualice a propiedade de control personalizado para o fluxo de tarefas correspondente ao valor de **Nome** no proceso.

### <a name="add-new-option-set-values"></a>Engadir valores de novo conxunto de opcións
Para engadir valores de conxunto de opcións a un campo listo para usar, abra a páxina de edición do campo e en **Tipo**, seleccione **Editar** xunto ao conxunto de opcións. Engada unha nova opción que teña unha etiqueta e unha cor personalizadas. Se desexa engadir un novo estado de entrada de tempo, o campo listo para usar denomínase **Estado de entrada**, non **Estado**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designe un novo estado de entrada de tempo como só de lectura
Para designar un novo estado de entrada de tempo como só de lectura, engada o novo valor de entrada de tempo á propiedade **Lista de estado de só lectura**. A parte editable da grade de entrada de tempo bloquearase para as filas que teñan o novo estado.
A seguir, engada regras de negocio para bloquear todos os campos nas páxinas de TBX **Edición de fila de entrada de tempo** e **Edición de entrada de tempo**. Pode acceder ás regras de negocio para estas páxinas abrindo o editor fluxo do proceso de negocio para a páxina e logo seleccionando **Regras de negocio**. Pode engadir o novo estado á condición nas regras de negocio existentes ou pode engadir unha nova regra de negocio para o novo estado.

### <a name="add-custom-validation-rules"></a>Engadir regras de validación personalizadas
Hai dous tipos de regras de validación que pode engadir para a experiencia da grade de entrada de tempo semanal:

- Regras de negocio do lado do cliente que funcionan en cadros de diálogo de creación rápida e en páxinas TBX.
- Validacións de complementos do servidor que se aplican a todas as actualizacións de entrada de tempo.

#### <a name="business-rules"></a>Regras de negocio
Use regras de negocio para bloquear e desbloquear campos, introducir valores predefinidos en campos e definir validacións que requiran información só do rexistro de entrada de tempo actual. Pode acceder ás regras de negocio para unha páxina de TBX abrindo o editor fluxo do proceso de negocio para a páxina e logo seleccionando **Regras de negocio**. Pode editar as regras de negocio existentes ou engadir unha nova regra de negocio. Para validacións aínda máis personalizadas, pode utilizar unha regra de negocio para executar JavaScript.

#### <a name="plug-in-validations"></a>Validacións de complementos
Use as validacións de complementos para calquera validación que requira máis contexto do que está dispoñible nun rexistro de entrada única ou para calquera validación que desexe executar nas actualizacións entre liñas na grade. Para completar a validación, cree un complemento personalizado na entidade **Entrada de tempo**.

### <a name="copying-time-entries"></a>Copiar as entradas de tempo
Use a vista **Copiar columnas de entrada de tempo** para definir a lista de campos para copiar durante a entrada de tempo. **Data** e **Duración** son campos obrigatorios e non se deben eliminar da vista.
