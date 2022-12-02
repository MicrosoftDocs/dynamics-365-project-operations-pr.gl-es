---
title: Ampliación das entradas de tempo
description: Este artigo ofrece información sobre como os programadores poden ampliar o control de entradas de tempo.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914768"
---
# <a name="extending-time-entries"></a>Ampliación das entradas de tempo

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations inclúe un control personalizado de entrada de tempo extensible. Este control inclúe as seguintes funcionalidades:

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
Cada entrada de tempo está asociada a un rexistro de orixe de tempo. Este rexistro determina que aplicacións deben procesar a entrada de tempo e como.

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

1. Engada o campo personalizado á caixa de diálogo **Creación rápida**.
2. Configure a grade para mostrar o campo personalizado.
3. Engada o campo personalizado á páxina **Edición de filas** ou **Edición de entradas de tempo**, segundo corresponda.

Asegúrese de que o novo campo ten as validacións requiridas na páxina **Edición de filas** ou **Edición de entradas de tempo**. Como parte desta tarefa, bloquee o campo, en función do estado da entrada de tempo.

Cando engade un campo personalizado á grade **Entrada de tempo** e despois crea entradas de tempo directamente na grade, o campo personalizado para esas entradas establécese automaticamente para que coincida coa fila. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Engadir o campo personalizado á caixa de diálogo de creación rápida
Engada o campo personalizado á caixa de diálogo **Creación rápida: crear entrada de tempo**. Os usuarios poden introducir un valor cando engaden entradas de tempo seleccionando **Nova**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grade para mostrar o campo personalizado
Hai dous xeitos de engadir un campo personalizado á grade **Entrada de tempo semanal**.

- Personalice a vista **As miñas entradas de tempo semanal** e engádalle o campo personalizado. Pode especificar a posición e o tamaño do campo personalizado na grade editando as propiedades na vista.
- Cree unha nova vista de entrada de tempo personalizada e definila como vista por defecto. Esta vista debería conter os campos **Descrición** e **Comentarios externos**, ademais das columnas que desexa incluír na grade. Pode especificar a posición, o tamaño e a orde de clasificación por defecto da grade editando as propiedades na vista. A seguir, configure o control personalizado para esta vista para que sexa un control de **Grade de entrada de tempo**. Engada o control á vista e seleccióneo para **Web**, **Teléfono** e **Tableta**. A seguir, configure os parámetros para a grade **Entrada de tempo semanal**. Configure o campo **Data de inicio** en **msdyn\_date**, configure o campo **Duración** en **msdyn\_duration** e configure o campo **Estado** en **msdyn\_entrystatus**. O campo **Lista de estado de só lectura** está configurado como **192350002 (Enviado)**, **192350003 (Enviado)** ou **192350004 (Solicitude de retirada)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Engadir o campo personalizado á páxina de edición adecuada
As páxinas que se usan para editar unha entrada de tempo ou unha fila de entradas de tempo pódense atopar en **Formularios**. O botón **Editar entrada** da grade abre a páxina **Editar entrada**, e o botón **Editar fila** abre a páxina **Edición de filas**. Pode editar estas páxinas para que inclúan campos personalizados.

Ambas opcións eliminan algún filtro listo para usar nas entidades **Proxecto** e **Tarefa do proxecto**, de xeito que todas as vistas de busca das entidades son visibles. Ao principio, só son visibles as vistas de busca relevantes.

Debe determinar a páxina adecuada para o campo personalizado. Moi probablemente, se engadiu o campo á grade, debería ir na páxina **Edición de filas** que se usa para campos que se aplican a toda a fila de entradas de tempo. Se o campo personalizado ten un valor único na fila todos os días (por exemplo, é un campo personalizado para a hora de finalización), debe ir na páxina **Edición de entrada de tempo**.

Para engadir un campo personalizado a unha páxina, arrastre o elemento **Campo** á posición adecuada na páxina e logo estableza as súas propiedades.

### <a name="add-new-option-set-values"></a>Engadir valores de novo conxunto de opcións
Para engadir os valores do conxunto de opcións a un campo listo para usar, siga estes pasos.

1. Abra a páxina de edición do campo e, a seguir, en **Tipo**, seleccione **Editar** xunto ao conxunto de opcións.
2. Engada unha nova opción que teña unha etiqueta e unha cor personalizadas. Se desexa engadir un novo estado de entrada de tempo, o campo listo para usar denomínase **Estado de entrada**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designe un novo estado de entrada de tempo como só de lectura
Para designar un novo estado de entrada de tempo como só de lectura, engada o novo valor de entrada de tempo á propiedade **Lista de estado de só lectura**. Asegúrese de engadir o número, non a etiqueta. A parte editable da grade de entrada de tempo bloquearase agora para as filas que teñan o novo estado. Para configurar a propiedade **Lista de estado de só lectura** de xeito diferente para vistas de **Entrada de tempo** diferentes, engada a grade **Entrada de tempo** na sección de **Controis personalizados** dunha vista e configure os parámetros segundo corresponda.

A seguir, engada regras de negocio para bloquear todos os campos nas páxinas **Edición de filas** e **Edición de entradas de tempo**. Para acceder ás regras de negocio para estas páxinas, abra o editor de formularios para casa páxina e logo seleccione **Regras de negocio**. Pode engadir o novo estado á condición nas regras de negocio existentes ou pode engadir unha nova regra de negocio para o novo estado.

### <a name="add-custom-validation-rules"></a>Engadir regras de validación personalizadas
Pode engadir dous tipos de regras de validación para a experiencia da grade **Entrada de tempo semanal**:

- Regras de negocio do lado do cliente que funcionan nas páxinas
- Validacións de complementos do servidor que se aplican a todas as actualizacións de entrada de tempo

#### <a name="client-side-business-rules"></a>Regras de negocio do lado do cliente
Use regras de negocio para bloquear e desbloquear campos, introducir valores predefinidos en campos e definir validacións que requiran información só do rexistro de entrada de tempo actual. Para acceder ás regras de negocio para unha páxina, abra o editor de formularios e logo seleccione **Regras de negocio**. Pode editar as regras de negocio existentes ou engadir unha nova regra de negocio.

#### <a name="server-side-plug-in-validations"></a>Validacións de complementos do lado do servidor
Debe usar as validacións de complementos para calquera validación que requira máis contexto do que está dispoñible nun rexistro de entrada única. Tamén debe usalos para calquera validación que queira executar nas actualizacións en liña na grade. Para completar as validacións, cree un complemento personalizado na entidade **Entrada de tempo**.

### <a name="limits"></a>Límites
Actualmente, a grade **Entrada de tempo** ten un límite de tamaño de 500 filas. Se hai máis de 500 filas, o exceso de filas non se mostrará. Non hai forma de aumentar este límite de tamaño.

### <a name="copying-time-entries"></a>Copiar as entradas de tempo
Use a vista **Copiar columnas de entrada de tempo** para definir a lista de campos para copiar durante a entrada de tempo. **Data** e **Duración** son campos obrigatorios e non se deben eliminar da vista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
