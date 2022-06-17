---
title: Crear facturas baseadas en proxecto correctivas
description: Este artigo ofrece información sobre facturas correctivas en Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 86bb05242c74e97533c7555ffa645278c8519430
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927878"
---
# <a name="create-corrective-project-based-invoices"></a>Crear facturas baseadas en proxecto correctivas 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Pódese corrixir unha factura de proxecto confirmada para procesar cambios ou créditos segundo se negociaron co cliente e o xestor do proxecto.

Para editar unha factura confirmada, abra a factura confirmada e seleccione **Corrixir esta factura**. 

> [!NOTE]
> Esta selección non está dispoñible a menos que se confirme unha factura do proxecto.

A partir da factura confirmada créase un novo borrador de factura. Todos os detalles da liña de factura da factura confirmada anteriormente copianse no novo borrador. Os seguintes son algúns puntos clave para axudar a comprender mellor os detalles da liña na nova factura corrixida:

- Todas as cantidades actualízanse a cero. Isto supón que todos os elementos facturados están totalmente abonados. Se é necesario, pode actualizar manualmente estas cantidades para reflectir a cantidade que se está a facturar e non a cantidade que se vai aboar. En función da cantidade que introduza, a aplicación calcula a cantidade aboada. Este importe reflíctese nos datos reais que se crean cando se confirma a factura corrixida. Se está a facer cambios no importe do imposto, debe ingresar o importe do imposto correcto e non o importe do imposto que vai aboar.
- As correccións de fitos sempre se procesan como abonos completos.
- Os importes de retencións ou adiantos pódense corrixir se se facturou ao cliente un importe incorrecto.
- As conciliacións de retencións e adiantos pódense corrixir se se utilizou un importe incorrecto para conciliar os cargos dunha factura confirmada previamente.

> [!IMPORTANT]
> Os detalles da liña de factura que son correccións doutros cargos xa facturados teñen o campo **Corrección** campo definido como **Si**. As facturas que corrixiron os detalles da liña de factura teñen un campo chamado **Ten correccións** que tamén está establecido en **Si**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Datos reais creados na confirmación dunha factura correctiva

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
            <td width="216" rowspan="4" valign="top">
                <p>
Confirme a corrección dun adianto ou retención facturado.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación. Este importe é positivo porque está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Créase un dato real de reversión das vendas facturadas polo importe da retención ou o adianto para reverter as vendas facturadas orixinais.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Créase un novo dato real de vendas facturadas para o importe corrixido da liña de factura corrixida baseada en retención ou adianto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de vendas non facturadas dun importe negativo da liña de factura corrixida baseada en retención ou adianto, que se utilizará para a conciliación.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Unha confirmación da corrección dunha retención ou un adianto conciliado previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación. Este importe é positivo e está destinado a cancelar o negativo que se creou cando se produciu a conciliación previa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de inversión das vendas facturadas polo importe da factura previa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Créase un novo dato real de vendas facturadas para o importe da retención que se aplica na factura corrixida.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de vendas non facturadas cun importe negativo da retención ou o adianto sobrante corrixido, que se utilizará para a conciliación de facturas posteriores.
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
O estado da factura no fito actualízase de <b>Factura do cliente contabilizada</b> a <b>Listo para facturar</b>.
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
Non compatible </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
