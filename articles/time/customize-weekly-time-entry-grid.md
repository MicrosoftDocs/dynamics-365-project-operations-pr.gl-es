---
title: Ampliación das entradas de tempo
description: Este tema ofrece información sobre como os programadores poden ampliar o control de entradas de tempo.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582984"
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

- O **msdyn_start** e **msdyn_end** os campos son conscientes do fuso horario.
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

1. Engade o campo personalizado ao **Creación rápida** caixa de diálogo.
2. Configure a grade para mostrar o campo personalizado.
3. Engade o campo personalizado ao **Edición de filas** ou **Edición de entrada de hora** páxina, segundo corresponda.

Asegúrese de que o novo campo teña as validacións requiridas no **Edición de filas** ou **Edición de entrada de hora** páxina. Como parte desta tarefa, bloquea o campo en función do estado da entrada de tempo.

Cando engades un campo personalizado ao **Entrada horaria** grella e despois cree entradas de tempo directamente na grella, o campo personalizado para esas entradas establécese automaticamente para que coincida coa fila. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Engade o campo personalizado ao cadro de diálogo Creación rápida
Engade o campo personalizado ao **Creación rápida: crear entrada de tempo** caixa de diálogo. Os usuarios poden introducir un valor cando engaden entradas de tempo seleccionando **Nova**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grade para mostrar o campo personalizado
Hai dúas formas de engadir un campo personalizado ao **Entrada horaria semanal** reixa.

- Personaliza o **As miñas entradas de tempo semanais** ver e engadirlle o campo personalizado. Podes especificar a posición e o tamaño do campo personalizado na grade editando as propiedades na vista.
- Crea unha nova vista de entrada de hora personalizada e configúraa como vista predeterminada. Esta vista debe conter **Descrición** e **Comentarios externos** campos ademais das columnas que desexa que inclúa a grade. Podes especificar a posición, o tamaño e a orde predeterminada da grade editando as propiedades na vista. A seguir, configure o control personalizado para esta vista para que sexa un control de **Grade de entrada de tempo**. Engade o control á vista e selecciónao para **Web**, **·**, e **Tablet**. A continuación, configure os parámetros para **Entrada horaria semanal** reixa. Establece o **Data de inicio** campo a **msdyn\_ data**, establece o **Duración** campo a **msdyn\_ duración**, e configura o **Estado** campo a **msdyn\_ estado de entrada**. O **Lista de estado de só lectura** campo está configurado en **192350002 (Aprobado)**, **(Enviado)**, ou **192350004 (Solicitude de retirada)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Engade o campo personalizado á páxina de edición adecuada
As páxinas que se usan para editar unha entrada de tempo ou unha fila de entradas de tempo pódense atopar en **Formularios**. O **Editar entrada** botón da grella abre o **Editar entrada** páxina, e o **Editar fila** botón abre o **Edición de filas** páxina. Podes editar estas páxinas para que inclúan campos personalizados.

Ambas as opcións eliminan algúns filtros predeterminados **Proxecto** e **Tarefa do proxecto** entidades, para que todas as vistas de busca das entidades sexan visibles. Ao principio, só son visibles as vistas de busca relevantes.

Debes determinar a páxina adecuada para o campo personalizado. O máis probable é que, se engadiches o campo á grella, debería ir ao **Edición de filas** páxina que se usa para os campos que se aplican a toda a fila de entradas de tempo. Se o campo personalizado ten un valor único na fila todos os días (por exemplo, se é un campo personalizado para a hora de finalización), debería ir ao **Edición de entrada de hora** páxina.

Para engadir o campo personalizado a unha páxina, arrastre a **Campo** elemento na posición adecuada na páxina e, a continuación, configure as súas propiedades.

### <a name="add-new-option-set-values"></a>Engadir valores de novo conxunto de opcións
Para engadir valores conxunto de opcións a un campo listo para usar, siga estes pasos.

1. Abre a páxina de edición do campo e, a continuación, debaixo **Tipo**, seleccione **Editar** xunto ao conxunto de opcións.
2. Engada unha nova opción que teña unha etiqueta e unha cor personalizadas. Se desexa engadir un novo estado de entrada de hora, chámase o campo de lista **Estado de entrada**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designe un novo estado de entrada de tempo como só de lectura
Para designar un novo estado de entrada de tempo como só de lectura, engada o novo valor de entrada de tempo á propiedade **Lista de estado de só lectura**. Asegúrate de engadir o número, non a etiqueta. A parte editable da grella de entrada de tempo agora bloquearase para as filas que teñan o novo estado. Para configurar o **Lista de estado de só lectura** propiedade diferente para diferente **Entrada horaria** vistas, engade o **Entrada horaria** cuadrícula nunha vista **Controis personalizados** sección e configure os parámetros segundo corresponda.

A continuación, engade regras comerciais para bloquear todos os campos do **Edición de filas** e **Edición de entrada de hora** páxinas. Para acceder ás regras comerciais destas páxinas, abra o editor de formularios para cada páxina e, a continuación, seleccione **Regras comerciais**. Pode engadir o novo estado á condición nas regras de negocio existentes ou pode engadir unha nova regra de negocio para o novo estado.

### <a name="add-custom-validation-rules"></a>Engadir regras de validación personalizadas
Podes engadir dous tipos de regras de validación para o **Entrada horaria semanal** experiencia na rede:

- Regras comerciais do lado do cliente que funcionan nas páxinas
- Validacións de complementos do servidor que se aplican a todas as actualizacións de entrada de tempo

#### <a name="client-side-business-rules"></a>Regras comerciais do lado do cliente
Use regras de negocio para bloquear e desbloquear campos, introducir valores predefinidos en campos e definir validacións que requiran información só do rexistro de entrada de tempo actual. Para acceder ás regras comerciais dunha páxina, abra o editor de formularios e, a continuación, seleccione **Regras comerciais**. Pode editar as regras de negocio existentes ou engadir unha nova regra de negocio.

#### <a name="server-side-plug-in-validations"></a>Validacións de complementos do lado do servidor
Deberías usar validacións de complementos para todas as validacións que requiran máis contexto do que hai dispoñible nun rexistro de entrada única. Tamén deberías usalos para calquera validación que queiras executar nas actualizacións en liña na grella. Para completar as validacións, cree un complemento personalizado no ficheiro **Entrada horaria** entidade.

### <a name="limits"></a>Límites
Actualmente, o **Entrada horaria** a grade ten un límite de tamaño de 500 filas. Se hai máis de 500 filas, non se mostrarán as filas en exceso. Non hai forma de aumentar este límite de tamaño.

### <a name="copying-time-entries"></a>Copiar as entradas de tempo
Use a vista **Copiar columnas de entrada de tempo** para definir a lista de campos para copiar durante a entrada de tempo. **Data** e **Duración** son campos obrigatorios e non se deben eliminar da vista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
