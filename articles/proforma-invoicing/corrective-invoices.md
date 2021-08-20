---
title: Facturas baseadas en proxecto correctivas
description: Este tema ofrece información sobre como crear e confirmar facturas baseadas en proxecto correctivas en Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997154"
---
# <a name="corrective-project-based-invoices"></a>Facturas baseadas en proxecto correctivas

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Pódese corrixir unha factura de proxecto confirmada para procesar cambios ou créditos segundo se negociaron co cliente e o xestor do proxecto.

Para editar unha factura confirmada, abra a factura confirmada e seleccione **Corrixir esta factura**. 

> [!NOTE]
> Esta selección non está dispoñible a menos que se confirme unha factura do proxecto ou a factura baseada en proxecto conteña adiantos ou retencións ou conciliacións de adiantos ou retencións.

A partir da factura confirmada créase un novo borrador de factura. Todos os detalles da liña de factura da factura confirmada anteriormente copianse no novo borrador. Os seguintes son algúns dos puntos clave para comprender os detalles da liña da nova factura corrixida:

- Todas as cantidades actualízanse a cero. Dynamics 365 Project Operations supón que todos os elementos facturados están totalmente abonados. Se é necesario, pode actualizar manualmente estas cantidades para reflectir a cantidade que se está a facturar e non a cantidade que se vai aboar. En función da cantidade que introduza, a aplicación calcula a cantidade aboada. Este importe reflíctese nos datos reais que se crean cando se confirma a factura corrixida. Se está a facer cambios no importe do imposto, debe ingresar o importe do imposto correcto e non o importe do imposto que vai aboar.
- As correccións de fitos sempre se procesan como abonos completos.


> [!IMPORTANT]
> Para os detalles da liña de factura que son correccións doutros cargos xa facturados, o campo **Corrección** está definido como **Si**. Para facturas que teñen os detalles da liña de factura corrixidos, o campo **Ten correccións** está definido como **Si**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Datos reais creados cando se confirma unha factura correctiva

A seguinte táboa indica os datos reais que se crean cando se confirma unha factura correctiva.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Escenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Datos reais creados na confirmación</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación do abono total dunha transacción de tempo facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar por horas e importe no detalle da liña de factura orixinal para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación do abono parcial nunha transacción temporal.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas facturadas por horas e importe facturados no detalle da liña de factura orixinal para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión disto e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que é imputable para as horas e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación do abono total dunha transacción de gasto facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para o gasto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación do abono parcial dunha transacción de gasto facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para un gasto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura corrixida, unha reversión disto e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que é imputable para a cantidade e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación do crédito total dunha transacción de material facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas facturadas para a cantidade e o importe no detalle da liña de factura para material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar para a cantidade e o importe no detalle da liña de factura para material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación do crédito parcial dunha transacción de material.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas facturadas para a cantidade e o importe facturados no detalle da liña de factura para material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión desta e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que é imputable para a cantidade e o importe restantes despois de deducir as cifras corrixidas no detalle da liña de factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación do abono total dunha transacción de taxa facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación do abono parcial dunha transacción de taxa facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas facturadas por cantidade e importe facturados no detalle da liña de factura orixinal para a taxa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura correctiva editada, unha reversión disto e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturación do abono total dunha transacción de fito facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas facturadas por horas e importe no detalle da liña de factura orixinal para o fito.
                </p>
                <p>
O estado da factura do fito actualízase desde <b>Factura do cliente contabilizada</b> a <b>Listo para facturar</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturación do abono parcial dunha transacción de fito facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Non se admite este escenario.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
