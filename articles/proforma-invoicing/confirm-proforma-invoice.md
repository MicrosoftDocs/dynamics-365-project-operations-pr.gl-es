---
title: Confirmar unha factura proforma
description: Este tema ofrece información sobre a confirmación dunha factura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128101"
---
# <a name="confirm-a-proforma-invoice"></a>Confirmar unha factura proforma

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Despois de confirmarse unha factura proforma, o estado da factura do proxecto actualízase a **Confirmado**. Cando se confirma unha factura, convértese en de só lectura. No futuro, a factura só se poderá corrixir se hai correccións ou créditos iniciados polo cliente ou cando se marca como pagada.

A seguinte táboa mostra os datos reais creados polo sistema. Estes datos actuais créanse cando se realizan determinadas operacións no borrador da factura do proxecto antes de que se confirme.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Escenario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Datos reais creados na confirmación</strong>
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
Un novo dato real de vendas sen facturar é imputable polas horas e o importe do detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un novo dato real de vendas sen facturar que non é imputable polas horas e o importe restantes despois de deducir las cifras correctas no detalle da liña de factura editada, unha reversión do dato real de vendas non facturadas e un dato real de vendas facturadas equivalente.
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
Un dato real de vendas facturadas pola cantidade e o importe na aprobación de gasto orixinal.
                </p>
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
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]