---
title: Confirmar unha factura proforma de proxecto
description: Este tema ofrece información sobre a confirmación das facturas proforma do proxecto en Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867084"
---
# <a name="confirm-a-proforma-project-invoice"></a>Confirmar unha factura proforma de proxecto 

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_


Despois de confirmarse unha factura proforma, o estado da factura do proxecto actualízase a **Confirmado**. Cando se confirma unha factura, convértese en de só lectura. No futuro, a factura só se poderá corrixir se hai correccións iniciadas polo cliente ou créditos.

A seguinte táboa mostra os datos reais creados polo sistema. Estes datos actuais créanse cando se realizan determinadas operacións no borrador da factura do proxecto antes de que se confirme.

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
Facturación dunha retención ou un adianto </p>
            </td>
            <td width="408" valign="top">
                <p>
Un dato real de vendas facturadas de tipo <strong>Retención</strong> créase polo importe do adianto ou da retención.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de vendas non facturadas dun importe negativo da retención ou do adianto que se utilizará para a conciliación
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Despois de conciliar completamente unha retención ou un adianto nunha factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación. Este importe é positivo xa que está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real das vendas facturadas polo importe desta factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Despois de conciliar parcialmente unha retención ou un adianto nunha factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas sen facturar da retención ou do adianto que se creou para a conciliación. Este importe é positivo xa que está destinado a cancelar o negativo que se creou cando se facturou a retención ou o adianto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real das vendas facturadas polo importe desta factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de vendas non facturadas negativo do importe restante da retención ou do adianto que se utilizará para a conciliación en futuras facturas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación dunha transacción de tempo sen modificacións no borrador de factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de vendas facturadas por horas e importe na aprobación de tempo orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación dunha transacción temporal editada para reducir a cantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que non é imputable polas horas e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación dunha transacción temporal editada para aumentar a cantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas sen facturar por horas e importe na aprobación de tempo orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación dunha transacción de gasto sen modificacións no borrador de factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de vendas facturadas pola cantidade e o importe na aprobación de gasto orixinal </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación dunha transacción de gasto que foi editada para reducir a cantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que non é imputable pola cantidade e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación dunha transacción de gasto que foi editada para aumentar a cantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas sen facturar pola cantidade e o importe na aprobación de gasto orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas e un dato real de vendas facturadas equivalente. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación dunha transacción de material sen modificacións no borrador de factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas sen facturar para a cantidade e o importe na aprobación de uso de material orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real das vendas facturadas para a cantidade e o importe na aprobación de uso de material orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación dunha transacción de material que se editou para reducir a cantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas sen facturar para a cantidade e o importe na aprobación de tempo orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que non é imputable pola cantidade e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación dunha transacción de material que se editou para aumentar a cantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión das vendas sen facturar para a cantidade e o importe na aprobación de uso de material orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar é imputable pola cantidade e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación dunha taxa.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Unha reversión de vendas sen facturar polo importe da taxa na liña de diario.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un dato real de vendas facturadas pola cantidade e o importe na liña de diario da taxa orixinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturación dun fito.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Un dato real de vendas facturadas polo importe do fito no fito orixinal da liña de contrato do proxecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturación dunha liña de contrato baseado en produto.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Un dato real de vendas facturadas para a liña de produto coa cantidade e importe procedentes da liña de contrato baseado en produto.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
