---
title: Xestionar unha factura proforma baseada en proxecto
description: Este tema ofrece información sobre como xestionar e traballar con facturas proforma baseadas en proxecto.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c61b0d887ae35988f1765d40de0447aa5fd7efd4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593748"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Xestionar unha factura proforma baseada en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

En Dynamics 365 Project Operations, as facturas proforma créanse como unha extensión das facturas en Dynamics 365 Sales. Non obstante, hai moitas diferenzas no proceso de facturación entre Sales e Project Operations á hora de facturar. Por exemplo, non é posible crear unha nova factura a partir da páxina **Lista de facturas** en Project Operations, pero é posible facelo en Sales. Estas diferenzas e extensións están dispoñibles para permitir procesos de facturación para proxectos que son diferentes dunha factura típica para un pedido de vendas.

> [!IMPORTANT]
> Debido ás diferenzas, non empregue facturas indistintamente en Sales e Project Operations.

## <a name="invoice-header"></a>Cabeceira de factura

A seguinte información está dispoñible nunha cabeceira de factura proforma en Project Operations.

| Campo | Localización | Descripción |
| --- | --- | --- | 
| **Identificador da factura** | Separador **Resumo** | O ID que se xera automaticamente cando se crea unha factura proforma. Un campo de só lectura que está bloqueado para a edición. Este campo úsase como referencia para cada factura proforma. |
| **Nome** | Separador **Resumo** | Defínao no nome do contrato do proxecto por defecto. Este campo pódese editar. | 
| **Moeda** | Separador **Resumo** | Defínao na moeda do proxecto por defecto. Un campo de só lectura que está bloqueado para a edición. |
| **Lista de prezos** | Separador **Resumo** | Defínao na lista de prezos do proxecto por defecto. Un campo de só lectura que está bloqueado para a edición. | 
| **Oportunidade** | Separador **Resumo** | A referencia á oportunidade vinculada. Un campo de só lectura que está bloqueado para a edición. | 
| **Contrato** | Separador **Resumo** | A referencia ao contrato do proxecto vinculado. Un campo de só lectura que está bloqueado para a edición. | 
| **Cliente** | Separador **Resumo** | A referencia ao contrato do proxecto vinculado. Un campo de só lectura que está bloqueado para a edición. |
| **Descrición** | Separador **Resumo** | O campo de texto que describe a factura. Este campo pódese editar. | 
| **Facturar a** e campos relacionados | **Separador Resumo** | Os valores predefinidos establécense a partir do cliente do contrato do proxecto. Este campo pódese editar.  | 
| **Estado** | Separador **Resumo** | Establece as seguintes opcións: **Activo**, **Pechado**, **Pagado** e **Cancelado**, e pode editarse. Os estados non compatibles para Project Operations inclúen **Pechado** e **Cancelado**. </br> O estado está establecido en **Activo** cando se crea a factura. </br>O estado debe establecerse en **Pagado** só despois de confirmar a factura.  | 
| **Estado da factura do proxecto** | Separador **Resumo** | Establece as seguintes opcións: **Borrador**, **En revisión** e **Confirmado** e pode editarse. Nos estados **Borrador** e **En revisión**, pódese editar a factura. A factura non se pode editar despois de confirmala. | 
| **Importe detallado** | Separador **Resumo** | A suma de importes en todas as liñas de factura despois dos adiantos e as deducións. Un campo de só lectura que está bloqueado para a edición.  Este campo úsase para calcular o importe final. | 
| **Desconto (%)** | Separador **Resumo** | Este campo pódese editar para introducir unha porcentaxe de desconto. Este campo non está admitido pola funcionalidade de Project Operations. Este é un campo non admitido.|  
| **Importe de desconto** | Separador **Resumo** | Este campo pódese editar para introducir o importe de desconto. Este campo non está admitido pola funcionalidade de Project Operations. Este é un campo non admitido. |  
| **Cantidade antes de frete** | **Separador Resumo** | Aplicarase o importe total da factura despois dos descontos. Un campo de só lectura que está bloqueado para a edición. Este campo úsase para calcular o importe final.  | 
| **Cantidade do frete** | Separador **Resumo** | Este campo pódese editar para introducir o importe de frete. Este campo non está admitido pola funcionalidade de Project Operations. Este é un campo non admitido. |
| **Imposto total** | Separador **Resumo** | O imposto total de todas as liñas de factura na factura. Un campo de só lectura que está bloqueado para a edición. | 
| **Cantidade total** | Separador **Resumo** | A suma do importe despois dos descontos e impostos. A suma é o importe que o cliente debe pagar. | 

## <a name="project-based-invoice-lines"></a>Liñas de factura baseada en proxecto

En Project Operations, sempre hai unha liña de factura por cada liña de contrato de proxecto. A liña de factura créase aínda que non haxa datos reais. A seguinte información está dispoñible nunha cabeceira de factura proforma.

| Campo | Localización | Descripción | 
| --- | --- | --- |
| **Identificador da factura** | Separador **Xeral** | A referencia ao identificador da factura. Un campo de só lectura que está bloqueado para a edición. A ligazón do identificador da factura pódese usar para volver á cabeceira da factura. | 
| **Nome** | Separador **Xeral** | O nome da liña de factura definido por defecto a partir do nome da liña de contrato. Este campo pódese editar. |
| **Project** | Separador **Xeral** | O proxecto na liña de contrato do proxecto relacionado. Un campo de só lectura que está bloqueado para a edición. A ligazón do proxecto pódese usar para navegar ao proxecto. | 
| **Método de facturación** | Separador **Xeral** | O método de facturación na liña de contrato do proxecto relacionado. Un campo de só lectura que está bloqueado para a edición. |
| **Cantidade da liña de contrato** | Separador **Xeral** | O importe do contrato na liña de contrato do proxecto relacionado. Un campo de só lectura que está bloqueado para a edición. | 
| **Facturado ata esta data** | Separador **Xeral** | A suma de importes en todos os detalles da liña de factura desta factura. Un campo de só lectura que está bloqueado para a edición. | 
| **Importe** | Separador **Xeral** | A suma de importes en todos os detalles da liña de factura imputables desta factura. Un campo de só lectura que está bloqueado para a edición. Este campo úsase para calcular o importe final na cabeceira da factura. | 
| **Imposto** | Separador **Xeral** | A suma de importes de impostos en todos os detalles da liña de factura desta liña de factura. Un campo de só lectura que está bloqueado para a edición. Este campo úsase para calcular o importe do imposto final na cabeceira da factura. | 
| **Importe estendido** | Separador **Xeral** | A suma de importes totais (**Imposto + Importes**) en todos os detalles de liña de factura imputables desta liña de factura. Un campo de só lectura que está bloqueado para a edición. Este campo úsase para calcular o importe final na cabeceira da factura. |

## <a name="invoice-line-details"></a>Detalles da liña da factura

Cada liña de factura dunha factura de proxecto inclúe os detalles da liña de factura. Estes detalles de liña están relacionados cos datos reais e fitos de vendas non facturadas relacionadas coa liña de contrato referenciada pola liña de factura. Todas estas transaccións están marcadas **Listo para facturar**.

Para unha liña de **Factura de tempo e material**, os detalles da liña de factura agrúpanse en **Imputable**, **Non imputable** e **Gratuíto** na páxina **Liña de factura**. Os detalles da **Liña de factura imputable** ao total da liña de factura. **Gratuíto** e **Datos reais non imputables** non se suman ao total da liña de factura.

Para unha liña de **Factura de prezo fixo**, os detalles da liña da factura créanse a partir de fitos marcados como **Listo para facturar** na liña de contrato relacionada. Despois de crear o detalle da liña de factura a partir dun fito, o estado de facturación do fito actualízase a **Factura do cliente creada**.

### <a name="edit-invoice-line-details"></a>Editar detalles da liña de factura

Os seguintes campos están dispoñibles no detalle da liña de factura que está apoiado por un dato real de vendas non facturadas:

| Campo | Descripción |
| --- | --- | 
| **Liña de factura** | A referencia ao **identificador da liña de factura**. Este campo é de só lectura e está bloqueado para a súa edición. Esta ligazón pódese usar para volver á cabeceira da factura. | 
| **Descrición** | Unha descrición do detalle da liña de factura. Definido por defecto desde o campo **Comentarios internos** na **Entrada de tempo** e desde o campo **Descrición** en **Entrada de gasto**. O campo pódese editar.| 
| **Descrición externa** | Unha descrición do detalle da liña de factura. Definido por defecto desde o campo **Comentarios externos** na **Entrada de tempo** e desde o campo **Descrición** en **Entrada de gasto**. O campo pódese editar. Esta descrición pode usarse para determinar o que debe figurar na factura impresa que se enviará ao cliente. En Project Operations, unha factura proforma non ten todas as funcións necesarias para configurar os axustes de impresión dunha factura. | 
| **Data de inicio** | Este é un campo de só lectura establecido por defecto a partir do dato real de orixe. |
| **Project** | Este é un campo de só lectura que se define por defecto a partir do dato real de orixe ao proxecto na liña de contrato relacionada. |  
| **Tarefa** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Categoría da transacción** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Rol** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |  
| **Recurso reservable** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Empresa de recursos** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Unidade de recursos** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Importe** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |  
| **Programación de unidades** | Para o detalle da liña de factura para tempo, sempre se define como tempo e non se pode editar. Para os gastos, defínese por defecto a partir do dato real de gasto de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Unidade** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |  
| **Prezo** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Moeda** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Importe** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Impostos** | Definido por defecto a partir do dato real de orixe. O campo pódese editar.| 
| **Importe estendido** | Un campo calculado, calculado como **Importe + Imposto**. Un campo de só lectura que está bloqueado para a edición. | 
| **Tipo de facturación** | Definido por defecto a partir do dato real de orixe. O campo pódese editar. Ao seleccionar **imputable** engádese a liña ao total da liña de factura. **Gratuíto** e **Non imputable** excluirano do total da liña de factura.| 
| **Seleccionar produto** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Produto** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Nome do produto** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |  
| **Descrición do produto fóra de catálogo** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Tipo de transacción** | Este é un campo de só lectura establecido por defecto a partir do dato real de orixe a **Vendas facturadas**. |  
| **Clase de transacción** | Definido por defecto a partir do dato real de orixe. Un campo de só lectura que está bloqueado para a edición. | 

Os seguintes campos están dispoñibles nun detalle da liña de factura que está apoiado por un fito.

| Campo | Descripción |
| --- | --- | 
| **Liña de factura** | Referencia ao **identificador da liña de factura**. Un campo de só lectura que está bloqueado para a edición. A ligazón pódese usar para volver á cabeceira da factura.  | 
| **Descrición** | Descrición do detalle da liña de factura. Definido por defecto a partir da descrición do fito de orixe. | 
|**Descrición externa** | Descrición do detalle da liña de factura que se define por defecto a partir da descrición do fito de orixe. Este campo pode usarse para determinar o que debe figurar na factura impresa que se enviará ao cliente. Unha factura proforma en Project Operations non ten todas as funcións necesarias para configurar os axustes de impresión dunha factura. | 
| **Data de inicio** | Definido por defecto a partir da data de **Fito** no fito de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Project** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Tarefa** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Categoría da transacción** | Un campo de só lectura que está bloqueado para a edición. |
| **Rol** | Un campo de só lectura que está bloqueado para a edición. | 
| **Recurso reservable** | Un campo de só lectura que está bloqueado para a edición. | 
| **Unidade de recursos** | Un campo de só lectura que está bloqueado para a edición. | 
| **Programación de unidades** | Un campo de só lectura que está bloqueado para a edición. | 
| **Unidade** | Un campo de só lectura que está bloqueado para a edición. | 
| **Prezo** | Definido por defecto a partir do importe do fito de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Moeda** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Importe** | Definido por defecto a partir do importe do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Imposto** | Definido por defecto a partir do importe do imposto no fito de orixe. Un campo de só lectura que está bloqueado para a edición. |
| **Importe estendido** | Definido por defecto a partir do importe estendido no fito de orixe. O campo pódese editar. | 
| **Tipo de facturación** | Definido sempre por defecto en **Imputable**. Un campo de só lectura que está bloqueado para a edición. |
| **Tipo de transacción** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | 
| **Clase de transacción** | Definido por defecto a partir do fito de orixe. Un campo de só lectura que está bloqueado para a edición. | 

## <a name="refresh-invoice-transactions"></a>Actualizar transaccións de factura

Se ten datos reais que chegaron despois de crearse a factura, pode incluílos na factura.

1. Na **Vista de traballo pendente de facturación**, marque os datos como **Listo para facturar**.   
2. Abra o borrador da factura proforma e, na franxa **Accións**, seleccione **Actualizar transaccións de liña de factura**.

  Os detalles da liña de factura créanse para calquera dato real que estea datado e marcado como **Listo para facturar**, pero non está incluído na factura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
