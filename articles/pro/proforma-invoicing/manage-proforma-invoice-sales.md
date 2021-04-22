---
title: Xestionar unha factura proforma de proxecto
description: Este tema ofrece información sobre como traballar con facturas proforma de proxecto.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2146e62bddc4a6286fa303ff2cc2c5622ea3133c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866904"
---
# <a name="manage-a-proforma-project-invoice"></a>Xestionar unha factura proforma de proxecto 

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Dynamics 365 Project Operations, as facturas proforma créanse como unha extensión das facturas en Dynamics 365 Sales. Non obstante, hai moitas diferenzas no proceso de facturación entre Sales e Project Operations á hora de facturar. Por exemplo, non é posible crear unha nova factura a partir da páxina **Lista de facturas** en Project Operations, pero é posible facelo en Sales. Estas diferenzas e extensións están dispoñibles para permitir procesos de facturación para proxectos que son diferentes dunha factura típica para un pedido de vendas.

> [!IMPORTANT]
> Debido ás diferenzas, non empregue facturas indistintamente en Sales e Project Operations.

## <a name="invoice-header"></a>Cabeceira de factura

A seguinte información está dispoñible nunha cabeceira de factura proforma en Project Operations.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| **Identificador da factura** | Separador **Resumo** | O ID que se xera automaticamente cando se crea unha factura proforma. Un campo de só lectura que está bloqueado para a edición. | Este campo úsase como referencia para cada factura proforma. |
| **Nome** | Separador **Resumo** | Defínao no nome do contrato do proxecto por defecto. Este campo pode ser editado polo usuario. | &nbsp;  |
| **Moeda** | Separador **Resumo** | Defínao na moeda do proxecto por defecto. Un campo de só lectura que está bloqueado para a edición. |&nbsp; |
| **Lista de prezos** | Separador **Resumo** | Defínao na lista de prezos do proxecto por defecto. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Oportunidade** | Separador **Resumo** | A referencia á oportunidade vinculada. Un campo de só lectura que está bloqueado para a edición. | &nbsp;  |
| **Contrato** | Separador **Resumo** | A referencia ao contrato do proxecto vinculado. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Cliente** | Separador **Resumo** | A referencia ao contrato do proxecto vinculado. Un campo de só lectura que está bloqueado para a edición. |&nbsp;  |
| **Descrición** | Separador **Resumo** | O campo de texto que describe a factura. Este campo pode ser editado polo usuario. | &nbsp; |
| **Facturar a** e campos relacionados | **Separador Resumo** | Os valores predefinidos establécense a partir do cliente do contrato do proxecto. Este campo pode ser editado polo usuario.  | &nbsp; |
| **Estado** | Separador **Resumo** | Establece as seguintes opcións: **Activo**, **Pechado**, **Pagado** e **Cancelado**, e pode ser editado polo usuario. | Os estados non compatibles para Project Operations inclúen **Pechado** e **Cancelado**. </br> O estado está establecido en **Activo** cando se crea a factura. </br>O estado debe establecerse en **Pagado** só despois de confirmar a factura. |
| **Estado da factura do proxecto** | Separador **Resumo** | Establece as seguintes opcións: **Borrador**, **En revisión** e **Confirmado**, e pode ser editado polo usuario. | Nos estados **Borrador** e **En revisión**, pódese editar a factura. A factura non se pode editar despois de confirmala. |
| **Importe detallado** | Separador **Resumo** | A suma de importes en todas as liñas de factura despois dos adiantos e as deducións. Un campo de só lectura que está bloqueado para a edición. | Este campo úsase para calcular o importe final. |
| **Desconto (%)** | Separador **Resumo** | Este campo pódese editar para introducir unha porcentaxe de desconto. Este campo non está admitido pola funcionalidade de Project Operations. | Este é un campo non admitido. |
| **Importe de desconto** | Separador **Resumo** | Este campo pódese editar para introducir o importe de desconto. Este campo non está admitido pola funcionalidade de Project Operations. | Este é un campo non admitido. |
| **Cantidade antes de frete** | **Separador Resumo** | Aplicarase o importe total da factura despois dos descontos. Un campo de só lectura que está bloqueado para a edición. | Este campo úsase para calcular o importe final. |
| **Cantidade do frete** | Separador **Resumo** | Este campo pódese editar para introducir o importe de frete. Este campo non está admitido pola funcionalidade de Project Operations. | Este é un campo non admitido. |
| **Imposto total** | Separador **Resumo** | O imposto total de todas as liñas de factura na factura. Un campo de só lectura que está bloqueado para a edición. | Ningún |
| **Importe total** | Separador **Resumo** | A suma do importe despois dos descontos e impostos. | A suma é o importe que o cliente debe pagar. |
## <a name="project-based-invoice-lines"></a>Liñas de factura baseada en proxecto

En Project Operations, sempre hai unha liña de factura por cada liña de contrato de proxecto. A liña de factura créase aínda que non haxa datos reais. A seguinte información está dispoñible nunha cabeceira de factura proforma.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| **Identificador da factura** | Separador **Xeral** | A referencia ao identificador da factura. Un campo de só lectura que está bloqueado para a edición. | A ligazón do identificador da factura pódese usar para volver á cabeceira da factura. |
| **Nome** | Separador **Xeral** | O nome da liña de factura definido por defecto a partir do nome da liña de contrato. Este campo pode ser editado polo usuario. | &nbsp; |
| **Project** | Separador **Xeral** | O proxecto na liña de contrato do proxecto relacionado. Un campo de só lectura que está bloqueado para a edición. | A ligazón do proxecto pódese usar para navegar ao proxecto. |
| **Método de facturación** | Separador **Xeral** | O método de facturación na liña de contrato do proxecto relacionado. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Cantidade da liña de contrato** | Separador **Xeral** | O importe do contrato na liña de contrato do proxecto relacionado. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Facturado ata esta data** | Separador **Xeral** | A suma de importes en todos os detalles da liña de factura desta factura. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Importe** | Separador **Xeral** | A suma de importes en todos os detalles da liña de factura imputables desta factura. Un campo de só lectura que está bloqueado para a edición. | Este campo úsase para calcular o importe final na cabeceira da factura. |
| **Imposto** | Separador **Xeral** | A suma de importes de impostos en todos os detalles da liña de factura desta liña de factura. Un campo de só lectura que está bloqueado para a edición. | Este campo úsase para calcular o importe do imposto final na cabeceira da factura. |
| **Importe estendido** | Separador **Xeral** | A suma de importes totais (**Imposto + Importes**) en todos os detalles de liña de factura imputables desta liña de factura. Un campo de só lectura que está bloqueado para a edición. | Este campo úsase para calcular o importe final na cabeceira da factura. |


## <a name="invoice-line-details"></a>Detalles da liña da factura

Cada liña de factura dunha factura de proxecto inclúe os detalles da liña de factura. Estes detalles de liña están relacionados cos datos reais e fitos de vendas non facturadas relacionadas coa liña de contrato referenciada pola liña de factura. Todas estas transaccións están marcadas **Listo para facturar**.

Para unha liña de **Factura de tempo e material**, os detalles da liña de factura agrúpanse en **Imputable**, **Non imputable** e **Gratuíto** na páxina **Liña de factura**. Os detalles da **Liña de factura imputable** ao total da liña de factura. **Gratuíto** e **Datos reais non imputables** non se suman ao total da liña de factura.

Para unha liña de **Factura de prezo fixo**, os detalles da liña da factura créanse a partir de fitos marcados como **Listo para facturar** na liña de contrato relacionada. Despois de crear o detalle da liña de factura a partir dun fito, o estado de facturación do fito actualízase a **Factura do cliente creada**.

### <a name="edit-invoice-line-details"></a>Editar detalles da liña de factura

Os seguintes campos están dispoñibles nun detalle da liña de factura que está apoiado por un dato real de vendas non facturadas:

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| **Liña de factura** | A referencia ao **identificador da liña de factura**. Campo de só lectura, bloqueado para a edición. | Esta ligazón pódese usar para volver á cabeceira da factura. |
| **Descrición** | Unha descrición do detalle da liña de factura. Definido por defecto desde o campo **Comentarios internos** na **Entrada de tempo** e desde o campo **Descrición** en **Entrada de gasto**. O campo pode ser editado polo usuario.| &nbsp; |
| **Descrición externa** | Unha descrición do detalle da liña de factura. Definido por defecto desde o campo **Comentarios externos** na **Entrada de tempo** e desde o campo **Descrición** en **Entrada de gasto**. O campo pode ser editado polo usuario. | Esta descrición pode usarse para determinar o que debe figurar na factura impresa que se enviará ao cliente. En Project Operations, unha factura proforma non ten todas as funcións necesarias para configurar os axustes de impresión dunha factura. |
| **Data de inicio** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | Este campo pódese editar nun novo detalle de liña de factura que non se apoia nun dato real de orixe. |
| **Project** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | Defínao por defecto no proxecto da liña de contrato relacionada. |
| **Tarefa** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nun dato real de orixe. Unha lista despregable mostra todas as tarefas asociadas á liña de contrato de proxecto relacionada.  |
| **Categoría da transacción** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nunha orixe real. |
| **Rol** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nun dato real de orixe. |
| **Recurso reservable** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nunha orixe real. |
| **Unidade de recursos** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nun dato real de orixe. |
| **Cantidade** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nun dato real de orixe. |
| **Programación de unidades** | Para o detalle da liña de factura para tempo, sempre se define como tempo e non se pode editar. Para os gastos, defínese por defecto a partir do dato real de gasto de orixe. Un campo de só lectura que está bloqueado para a edición. | Definido por defecto en **Tempo** nunha nova liña de factura que non se apoia nun dato real. |
| **Unidade** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nun dato real de orixe |
| **Prezo** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | O campo pódese editar nun novo detalle de liña de factura que non se apoia nun dato real de orixe. Se non se introduce ningún valor, establécese por defecto despois de **Gardar**. |
| **Moeda** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | Establécese por defecto a partir da cabeceira da factura cando se crea un novo detalle de factura sen o apoio dun dato real.  Un campo de só lectura que está bloqueado para a edición. |
| **Importe** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | Calculado como **Cantidade \* Prezo** ao crear un novo detalle de factura sen o apoio dun dato real. Calcúlase despois de **Gardar**. Un campo de só lectura que está bloqueado para a edición. |
| **Imposto** | Definido por defecto a partir do dato real de orixe. O campo pode ser editado polo usuario | O campo pode ser editado polo usuario cando crea un novo detalle de liña de factura sen o apoio dun dato real. |
| **Importe estendido** | Un campo calculado, calculado como **Importe + Imposto**. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Tipo de facturación** | Definido por defecto a partir do dato real de orixe. O campo pode ser editado polo usuario. | Ao seleccionar **imputable** engádese a liña ao total da liña de factura. **Gratuíto** e **Non imputable** excluirano do total da liña de factura. |
| **Seleccionar produto** | Establecido por defecto a partir do dato real de orixe, este é un campo de só lectura. | Cando crea un novo detalle de liña de factura sen un dato real de respaldo, pódese editar este campo. |
| **Produto** | Establecido por defecto a partir do dato real de orixe, este é un campo de só lectura. | Cando cree un novo detalle de liña de factura sen un respaldo real, este campo pode editarse se o campo **Seleccionar produto** está definido como **Produto existente**. |
| **Nome do produto** | Establecido por defecto a partir do dato real de orixe, este é un campo de só lectura. | Nunha nova liña de factura, onde se selecciona o ID do produto do catálogo, este campo configúrase co nome do produto. Para un produto fóra de catálogo, o campo configúrase co nome fóra de catálogo. |
| **Descrición do produto fóra de catálogo** | Establecido por defecto a partir do dato real de orixe, este campo é de só lectura. | Cando crea un novo detalle de liña de factura sen un dato real de respaldo, pode engadir unha descrición do produto. |
| **Tipo de transacción** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | Definido por defecto en **Vendas facturadas** e bloqueado ao crear un novo **Detalle da liña de factura** sen o apoio dun dato real.  |
| **Clase de transacción** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | Definido de xeito predefinido en función de se o usuario elixe crear un de talle de liña de factura de **Tempo**, **Gasto**, **Material** ou **Taxa** detalle da liña de factura á vez que se crea un novo **Detalle de liña de factura** sen un dato real de respaldo. Bloqueado para a edición. |

Os seguintes campos están dispoñibles nun detalle da liña de factura que está apoiado por un fito:

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| **Liña de factura** | Referencia ao **identificador da liña de factura**. Un campo de só lectura que está bloqueado para a edición. | A ligazón pódese usar para volver á cabeceira da factura. |
| **Descrición** | Descrición do detalle da liña de factura. Definido por defecto a partir da descrición do fito de orixe. | &nbsp; |
|**Descrición externa** | Descrición do detalle da liña de factura que se define por defecto a partir da descrición do fito de orixe. | Este campo pode usarse para determinar o que debe figurar na factura impresa que se enviará ao cliente. Unha factura proforma en Project Operations non ten todas as funcións necesarias para configurar os axustes de impresión dunha factura. |
| **Data de inicio** | Definido por defecto a partir da data de **Fito** no fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Project** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Tarefa** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Categoría da transacción** | Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Rol** | Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Recurso reservable** | Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Unidade de recursos** | Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Programación de unidades** | Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Unidade** | Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Prezo** | Definido por defecto a partir do importe do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Moeda** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. |&nbsp; |
| **Importe** | Definido por defecto a partir do importe do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Imposto** | Definido por defecto a partir do importe do imposto no fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Importe estendido** | Definido por defecto a partir do importe estendido no fito de orixe. O campo pode ser editado polo usuario | &nbsp; |
| **Tipo de facturación** | Definido sempre por defecto en **Imputable**. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Tipo de transacción** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |
| **Clase de transacción** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Crear novos detalles de liña de factura

Nas liñas de factura de tempo e material, pode crear novos detalles da liña de factura. Estes detalles da liña de factura non están apoiados por un dato real. Na liña de factura dunha liña de factura de tempo e material, pode seleccionar **Novo** para crear un novo detalle de liña de factura para as clases de transaccións incluídas na liña de contrato.

## <a name="refresh-invoice-transactions"></a>Actualizar transaccións de factura

Se ten datos reais que chegaron despois de crearse a factura, pode incluílos na factura.

1. Na **Vista de traballo pendente de facturación**, marque os datos como **Listo para facturar**.   
2. Abra o borrador da factura proforma e, na fita **Accións**, prema **Actualizar transaccións de liña de factura**.

  Isto crea detalles da liña de factura para calquera dato que estea datado e marcado como **Listo para facturar**; pero non está incluído na factura.

## <a name="product-based-invoice-lines"></a>Liñas de factura baseada en produto

En Project Operations, pode crear liñas de factura para produtos que non se aplican a ningún proxecto ou para todos os proxectos xunto con liñas de factura baseada en proxecto. Estas liñas de factura créanse como liñas de contrato baseado en produto e despois márcanse como listas para facturar, engádense como liñas de factura baseada en produto.

Despois de engadir liñas de factura baseada en produto, non se poden cambiar. Non obstante, pódense eliminar do borrador de factura proforma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
