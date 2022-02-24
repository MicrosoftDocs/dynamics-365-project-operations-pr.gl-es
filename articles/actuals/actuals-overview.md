---
title: Datos reais
description: Este tema ofrece información sobre como traballar con datos reais en Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852542"
---
# <a name="actuals"></a>Datos reais 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os datos reais representan o progreso financeiro e programado revisado e aprobado nun proxecto. Créanse como resultado da aprobación das entradas de tempo, gasto e uso de material e as entradas do diario e facturas.

## <a name="journal-lines-and-time-submission"></a>Liñas de diario e envío de tempo

Para obter máis información sobre a entrada de tempo, consulte [Visión xeral da entrada de tempo](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tempo e materiais

Cando unha entrada de tempo que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.

### <a name="fixed-price"></a>Prezo fixo

Cando unha entrada de tempo que se envía está ligada a un proxecto que está asignado a unha liña de contrato de prezo fixo, o sistema crea unha liña de diario para o custo.

### <a name="default-pricing"></a>Prezos predefinidos

A lóxica para crear prezos predefinidos reside na liña de diario. Os valores de campo da entrada de tempo cópianse á liña de diario. Estes valores inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente.

Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade de recursos**, utilízanse para determinar o prezo adecuado por defecto na liña de diario. Pode engadir un campo personalizado na entrada de tempo. Se desexa que o valor do campo se propague aos datos reais, cree o campo nas táboas **Datos reais** e **Liña de diario**. Use código personalizado para propagar o valor do campo seleccionado desde a entrada de tempo ata os datos reais a través da liña do diario empregando as orixes das transaccións. Para obter máis información sobre as orixes e conexións das transaccións, consulte [Ligar datos reais cos rexistros orixinais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Liñas de diario e envío de gastos básicos

Para obter máis información sobre a entrada de gasto, consulte [Visión xeral do gasto](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tempo e materiais

Cando unha entrada de gasto básico que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.

### <a name="fixed-price"></a>Prezo fixo

Cando se liga unha entrada de gasto básica enviada a un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.

### <a name="default-pricing"></a>Prezos predefinidos

A lóxica para introducir os prezos por defecto dos gastos baséase na categoría de gasto. A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada. Os campos que afectan aos prezos predefinidos, por exemplo, **Categoría de transacción** e **Unidade**, utilízanse para determinar o prezo adecuado por defecto na liña de diario. Non obstante, isto só funciona cando o método de fixación de prezos na lista de prezos é **Prezo por unidade**. Se o método de fixación de prezos é **Ao custo** ou **Sobreprezo sobre o custo**, o prezo introducido cando se crea a entrada de gasto úsase para o custo e o prezo da liña do diario de vendas calcúlase en función do método de fixación de prezos. 

Pode engadir un campo personalizado na entrada de gasto. Se desexa que o valor do campo se propague aos datos reais, cree o campo nas táboas **Datos reais** e **Liña de diario**. Use código personalizado para propagar o valor do campo seleccionado desde a entrada de tempo ata os datos reais a través da liña do diario empregando as orixes das transaccións. Para obter máis información sobre as orixes e conexións das transaccións, consulte [Ligar datos reais cos rexistros orixinais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Presentación de rexistro de liñas de diario e uso de material

Para obter máis información sobre a entrada de gasto, consulte [Rexistro do uso de material](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Tempo e materiais

Cando unha entrada de rexistro do uso de material enviada está ligada a un proxecto que está asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.

### <a name="fixed-price"></a>Prezo fixo

Cando se liga unha entrada de rexistro do uso de material básica enviada a un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.

### <a name="default-pricing"></a>Prezos predefinidos

A lóxica para introducir os prezos predefinidos do material baséase na combinación de produtos e unidades. A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada. Os campos que afectan aos prezos predefinidos, por exemplo, **ID de produto** e **Unidade de recursos**, utilízanse para determinar o prezo adecuado por defecto na liña de diario. Non obstante, isto só funciona para produtos de catálogo. Para os produtos fóra de catálogo, o prezo introducido cando se crea a entrada do rexistro do uso de material utilízase para o custo e o prezo de venda nas liñas do diario. 

Pode engadir un campo personalizado na entrada de **Rexistro do uso de material**. Se desexa que o valor do campo se propague aos datos reais, cree o campo nas táboas **Datos reais** e **Liña de diario**. Use código personalizado para propagar o valor do campo seleccionado desde a entrada de tempo ata os datos reais a través da liña do diario empregando as orixes das transaccións. Para obter máis información sobre as orixes e conexións das transaccións, consulte [Ligar datos reais cos rexistros orixinais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Utilizar diarios de entradas para rexistrar custos

Pode usar diarios de entradas para rexistrar os custos ou ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos. Os diarios pódense usar para os seguintes fins:

- Mova os datos reais de transaccións doutro sistema a Microsoft Dynamics 365 Project Operations.
- Rexistrar os custos que se produciron noutro sistema. Estes custos poden incluír gastos de adquisición ou subcontratación.

> [!IMPORTANT]
> A aplicación non valida o tipo de liña de diario nin o prezo relacionado que se introduce na liña de diario. Polo tanto, só un usuario que coñeza perfectamente o impacto contable que teñen os datos reais no proxecto debería usar os diarios de entradas para crear datos reais. Debido ao impacto deste tipo de diario, debe escoller con atención quen ten acceso para crear diarios de entradas.

## <a name="record-actuals-based-on-project-events"></a>Rexistrar datos reais baseados en eventos de proxecto

Project Operations rexistra as transaccións financeiras que se producen durante un proxecto. Estas transaccións rexístranse como datos reais. As seguintes táboas mostran os diferentes tipos de datos reais que se crean dependendo de se o proxecto é un proxecto de tempo e materiais ou de prezo fixo, de se está en fase de prevenda ou de se é un proxecto interno.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>O recurso pertence á mesma unidade organizativa que a unidade de contratación do proxecto

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Proxecto facturable ou vendido</th>
<th rowspan="3">Proxecto na fase de prevendas</th>
<th rowspan="3">Proxecto interno</th>
</tr>
<tr>
<th colspan="2">Tempo e materiais</th>
<th colspan="2">Prezo fixo</th>
</tr>
<tr>
<th>Valores reais</th>
<th>Moeda da transacción</th>
<th>Prezo fixo</th>
<th>Moeda da transacción</th>
</tr>
</thead>
<tbody>
<tr>
<td>Créase unha entrada de tempo.</td>
<td colspan="6">Non hai actividade na entidade Datos reais</td>
</tr>
<tr>
<td>Envíase unha entrada de tempo.</td>
<td colspan="6">Non hai actividade na entidade Datos reais</td>
</tr>
<tr>
<td rowspan="2">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</td>
<td>Dato real de custo</td>
<td>Moeda da unidade de contratación</td>
<td rowspan="2">Dato real de custo</td>
<td rowspan="2">Moeda da unidade de contratación
<td rowspan="2">Dato real de custo</td>
<td rowspan="2">Dato real de custo</td>
</tr>
<tr>
<td>Dato real de vendas sen facturar: imputable</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="3">O tempo se aproba e diminúen as horas facturables durante a aprobación.</td>
<td>Dato real de custo</td>
<td>Moeda da unidade de contratación</td>
<td rowspan="3">Dato real de custo</td>
<td rowspan="3">Moeda da unidade de contratación</td>
<td rowspan="3">Dato real de custo</td>
<td rowspan="3">Dato real de custo</td>
</tr>
<tr>
<td>Dato real de vendas sen facturar: imputable para a nova cantidade</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Dato real de vendas sen facturar: non imputable para a diferencia</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="2">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</td>
<td>Inversión de vendas sen facturar</td>
<td>Moeda de contrato de proxecto</td>
<td rowspan="2">Vendas facturadas para fito</td>
<td rowspan="2">Moeda de contrato de proxecto</td>
<td rowspan="2">Non aplicable</td>
<td rowspan="2">Non aplicable</td>
</tr>
<tr>
<td>Vendas facturadas</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="3">Confírmase unha factura e prodúcese unha diminución das horas facturables.</td>
<td>Inversión de vendas sen facturar</td>
<td>Moeda de contrato de proxecto</td>
<td rowspan="3">Non aplicable</td>
<td rowspan="3">Non aplicable</td>
<td rowspan="3">Non aplicable</td>
<td rowspan="3">Non aplicable</td>
</tr>
<tr>
<td>Vendas facturadas: imputables para a nova cantidade</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Vendas facturadas: non imputables para a diferencia</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="2">Corríxese unha factura para aumentar a cantidade imputable.</td>
<td>Vendas facturadas: inversión</td>
<td>Moeda de contrato de proxecto</td>
<td rowspan="5">
<ul>
<li>Inversión de vendas facturadas para fito</li>
<li>Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></li>
</ul>
</td>
<td rowspan="5">Moeda de contrato de proxecto</td>
<td rowspan="5">Non aplicable</td>
<td rowspan="5">Non aplicable</td>
</tr>
<tr>
<td>Vendas facturadas</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="3">Corríxese unha factura para diminuír a cantidade imputable.</td>
<td>Vendas facturadas: inversión</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Vendas facturadas para a nova cantidade</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Vendas sen facturar: imputables para a diferencia</td>
<td>Moeda de contrato de proxecto</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>O recurso pertence a unha unidade organizativa que é distinta da unidade de contratación do proxecto

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Proxecto facturable ou vendido</th>
<th rowspan="3">Proxecto na fase de prevendas</th>
<th rowspan="3">Proxecto interno</th>
</tr>
<tr>
<th colspan="2">Tempo e materiais</th>
<th colspan="2">Prezo fixo</th>
</tr>
<tr>
<th>Valores reais</th>
<th>Moeda da transacción</th>
<th>Prezo fixo</th>
<th>Moeda da transacción</th>
</tr>
</thead>
<tbody>
<tr>
<td>Créase unha entrada de tempo.</td>
<td colspan="6">Non hai actividade na entidade Datos reais</td>
</tr>
<tr>
<td>Envíase unha entrada de tempo.</td>
<td colspan="6">Non hai actividade na entidade Datos reais</td>
</tr>
<tr>
<td rowspan="4">O tempo se aproba e non cambian nin aumentan as horas facturables durante a aprobación.</td>
<td>Dato real de custo</td>
<td>Moeda da unidade de contratación</td>
<td rowspan="4">Dato real de custo</td>
<td rowspan="4">Moeda da unidade de contratación</td>
<td rowspan="4">Dato real de custo</td>
<td rowspan="4">Dato real de custo</td>
</tr>
<tr>
<td>Dato real de vendas sen facturar: imputable</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Custo da unidade de recursos</td>
<td>Moeda da unidade de recursos</td>
</tr>
<tr>
<td>Vendas entre organizacións</td>
<td>Moeda da unidade de contratación</td>
</tr>
<tr>
<td rowspan="5">O tempo se aproba e diminúen as horas facturables durante a aprobación.</td>
<td>Dato real de custo</td>
<td>Moeda da unidade de contratación</td>
<td rowspan="5">Dato real de custo</td>
<td rowspan="5">Moeda da unidade de contratación</td>
<td rowspan="5">Dato real de custo</td>
<td rowspan="5">Dato real de custo</td>
</tr>
<tr>
<td>Custo da unidade de recursos</td>
<td>Moeda da unidade de recursos</td>
</tr>
<tr>
<td>Vendas entre organizacións</td>
<td>Moeda da unidade de contratación</td>
</tr>
<tr>
<td>Dato real de vendas sen facturar: imputable para a nova cantidade</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Dato real de vendas sen facturar: non imputable para a diferencia</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="2">Confírmase unha factura e non cambian nin aumentan as horas facturables durante a aprobación.</td>
<td>Inversión de vendas sen facturar</td>
<td>Moeda de contrato de proxecto</td>
<td rowspan="2">Vendas facturadas para fito</td>
<td rowspan="2">Moeda de contrato de proxecto</td>
<td rowspan="2">Non aplicable</td>
<td rowspan="2">Non aplicable</td>
</tr>
<tr>
<td>Vendas facturadas</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="3">Confírmase unha factura e prodúcese unha diminución das horas facturables.</td>
<td>Inversión de vendas sen facturar</td>
<td>Moeda de contrato de proxecto</td>
<td rowspan="3">Non aplicable</td>
<td rowspan="3">Non aplicable</td>
<td rowspan="3">Non aplicable</td>
<td rowspan="3">Non aplicable</td>
</tr>
<tr>
<td>Vendas facturadas: imputables para a nova cantidade</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Vendas facturadas: non imputables para a diferencia</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="2">Corríxese unha factura para aumentar a cantidade imputable.</td>
<td>Vendas facturadas: inversión</td>
<td>Moeda de contrato de proxecto</td>
<td rowspan="5">
<ul>
<li>Inversión de vendas facturadas para fito</li>
<li>Cambio do estado de fito de <strong>Facturado</strong> a <strong>Listo para facturar</strong></li>
</ul>
</td>
<td rowspan="5">Moeda de contrato de proxecto</td>
<td rowspan="5">Non aplicable</td>
<td rowspan="5">Non aplicable</td>
</tr>
<tr>
<td>Vendas facturadas</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td rowspan="3">Corríxese unha factura para diminuír a cantidade imputable.</td>
<td>Vendas facturadas: inversión</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Vendas facturadas para a nova cantidade</td>
<td>Moeda de contrato de proxecto</td>
</tr>
<tr>
<td>Vendas sen facturar: imputables para a diferencia</td>
<td>Moeda de contrato de proxecto</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
