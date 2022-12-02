---
title: Visión xeral dos datos reais
description: Neste artigo se proporciona información sobre datos reais do proxecto.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 35282e6c51fff28dbbb0a5a7de760788416ed0e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929074"
---
# <a name="actuals-overview"></a>Visión xeral dos datos reais

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os datos reais son la cantidade de traballo que realizou nun proxecto. É posible rastrexar os datos reais do proxecto ata os seus documentos de orixe. Eses documentos de orixe inclúen tempo, gasto, entradas no diario e tamén facturas.

![Como se rastrexan os datos reais do proxecto ata os documentos de orixe.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Envío dunha entrada de tempo

En PSA, cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario. Unha liña é para o custo e a outra é para as vendas sen facturar. Cando se envía unha entrada de tempo para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo. 

A lóxica para especificar prezos predefinidos reside na liña de diario. Todos os valores de campo dunha entrada de tempo cópianse á liña de diario. Estes campos inclúen a data da transacción, a liña de contrato á que está asignado o proxecto e o resultado da moeda na lista de prezos correspondente. 

Os campos que afectan aos prezos predefinidos, por exemplo, **Rol** e **Unidade organizativa**, fan que se introduza o prezo adecuado por defecto na liña de diario. Se engade un campo personalizado na entrada de tempo e desexa que o valor de campo se propague aos datos reais, cree o campo na entidade Datos reais e utilice as asignacións de campos para copiar o campo da entrada de tempo aos datos reais.

## <a name="submitting-an-expense-entry"></a>Envío dunha entrada de gasto

En PSA, cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de tempo e materiais, créanse dúas liñas de diario. Unha liña é para o custo e a outra é para as vendas sen facturar. Cando se envía unha entrada de gasto para un proxecto que está asignado a unha liña de contrato de prezo fixo, só se crea unha liña de diario para o custo.

A lóxica para especificar os prezos predefinidos para os gastos basease na categoría de gasto seleccionada na páxina **Entrada de gasto**. A fecha da transacción, a liña de contrato á que está asignado o proxecto e a moeda utilízanse para determinar a lista de prezos adecuada. Non obstante, para o prezo, o importe que introduce o usuario establécese directamente nas liñas de diario de gasto para custo e vendas por defecto.

Na versión actual de PSA, a especificación de prezos predeterminados por entrada segundo a categoría nas entradas de gasto non está dispoñible.

## <a name="using-entry-journals-to-record-costs"></a>Utilización de diarios de entradas para rexistrar custos

En PSA, os diarios de entradas permiten rexistrar o custo ou os ingresos nas clases de material, tarifa, tempo, gasto ou transacción de impostos. Un diario ten un encabezado, liñas e unha acción **Confirmar**. Este son algúns escenarios nos que podería usar un diario:

- Debe rexistrar os custos reais do material e as vendas nun proxecto.
- Debe mover os datos reais de transaccións doutro sistema a PSA.
- Debe rexistrar os custos que se produciron noutro sistema, como os custos de adquisición ou subcontratación.

> [!IMPORTANT]
> O uso de diarios de entradas para crear o datos reais debe facelo só un usuario que teña pleno coñecemento do impacto contable que teñen os datos reais no proxecto. Isto é debido a que a aplicación non valida o tipo de liña de diario ou o prezo relacionado que se introduce na liña de diario. Debido ao impacto deste tipo de diario, teña a precaución adecuada sobre quen ten acceso a crear diarios de entradas.     


## <a name="recording-actuals-based-on-project-events"></a>Rexistro de datos reais baseados en eventos de proxecto

PSA rexistra as transaccións financeiras que se producen durante un proxecto. Estas transaccións rexístranse como **datos reais**. As seguintes táboas mostran os diferentes tipos de datos reais que se crean dependendo de se o proxecto é un proxecto de tempo e materiais ou de prezo fixo, de se está en fase de prevenda ou de se é un proxecto interno.

**O recurso pertence á mesma unidade organizativa que a unidade de contratación do proxecto**

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

**O recurso pertence a unha unidade organizativa que é distinta da unidade de contratación do proxecto**

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
