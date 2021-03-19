---
title: Datos reais
description: Este tema ofrece información sobre como traballar con datos reais en Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
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
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291797"
---
# <a name="actuals"></a>Datos reais 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Os datos reais son la cantidade de traballo que realizou nun proxecto. Créanse como resultado de entradas de tempo e gastos, e entradas de diario e facturas.

## <a name="journal-lines-and-time-submission"></a>Liñas de diario e envío de tempo

Para obter máis información sobre a entrada de tempo, consulte [Visión xeral da entrada de tempo](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tempo e materiais

Cando unha entrada de tempo que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.

### <a name="fixed-price"></a>Prezo fixo

Cando unha entrada de tempo que se envía está ligada a un proxecto que está asignado a unha liña de contrato de prezo fixo, o sistema crea unha liña de diario para o custo.

### <a name="default-pricing"></a>Prezos predefinidos

A lóxica para crear prezos predefinidos reside na liña de diario. Os valores de campo da entrada de tempo cópianse á liña de diario. Estes valores inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente.

Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade organizativa**, utilízanse para determinar o prezo adecuado por defecto na liña de diario. Pode engadir un campo personalizado na entrada de tempo. Se desexa que o valor de campo se propague aos datos reais, cree o campo na entidade Datos reais e utilice as asignacións de campos para copiar o campo da entrada de tempo aos datos reais.

## <a name="journal-lines-and-basic-expense-submission"></a>Liñas de diario e envío de gastos básicos

Para obter máis información sobre a entrada de gasto, consulte [Visión xeral do gasto](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tempo e materiais

Cando unha entrada de gasto básico que se envía está ligada a un proxecto asignado a unha liña de contrato de tempo e materiais, o sistema crea dúas liñas de diario, unha para o custo e outra para as vendas non facturadas.

### <a name="fixed-price"></a>Prezo fixo

Cando unha entrada de gasto básico que se envía está ligada a un proxecto que está asignado a unha liña de contrato de prezo fixo, o sistema crea unha liña de diario para o custo.

### <a name="default-pricing"></a>Prezos predefinidos

A lóxica para introducir os prezos por defecto dos gastos baséase na categoría de gasto. A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada. Non obstante, por defecto, o importe que se introduce para o propio prezo establécese directamente nas liñas de diario de gasto para custo e vendas.

A especificación de prezos predeterminados por entrada segundo a categoría nas entradas de gasto non está dispoñible.

## <a name="use-entry-journals-to-record-costs"></a>Utilizar diarios de entradas para rexistrar custos

Pode usar diarios de entradas para rexistrar os custos ou ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos. Os diarios pódense usar para os seguintes fins:

- Rexistra o custo real dos materiais e as vendas nun proxecto.
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