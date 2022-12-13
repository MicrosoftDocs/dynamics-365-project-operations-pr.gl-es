---
title: Calendarios de facturas nas liñas de cotización do proxecto
description: Este artigo ofrece información sobre a creación de programacións de facturas e fitos para as liñas de oferta.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 98006cc2857f01298054c4f0e70781bf4b8b474b
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825751"
---
# <a name="invoice-schedules-on-project-quote-lines"></a>Calendarios de facturas nas liñas de cotización do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Unha liña de cotización do proxecto dá a posibilidade de expresar un calendario de facturas. Isto é opcional durante a fase de oferta porque a aplicación non admite a facturación dun proxecto cando está ligado a unha liña de oferta. A facturación só se permite despois de gañar a oferta. O único impacto descendente da creación dunha programación de facturas durante a fase de oferta é que esta programación de facturas se copia á liña de contrato baseado en proxecto. Se non crea unha programación de facturas durante a fase de oferta, poderá facelo na liña de contrato baseado en proxecto.

En xeral, a finalidade das programacións de facturas é permitir a creación automática de borradores de facturas para unha liña de contrato baseado en proxecto. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-quote-line"></a>Cree un calendario de facturas de material e tempo para unha liña de cotización do proxecto

Cando o método de facturación dunha liña de oferta baseada en proxecto é Tempo e material, o sistema xera una programación de facturas baseada en datas. Para xerar automaticamente unha programación de facturas baseada en datas, complete os seguintes pasos.

1. Vaia a **Configuración** > **frecuencias de facturas** e configure unha frecuencia de facturas.
2. Na páxina **Ofertas**, abra a oferta do proxecto e na páxina **Resumo**, estableza a data de entrega solicitada.
3. Abra a liña de oferta de tempo e material para a que precisa crear unha programación de facturas baseada en datas. 
4. No separador **Programación de facturas**, seleccione valores nos campos **Comezo da facturación** e **Frecuencia das facturas**. 
5. Na subgrade, seleccione **Xerar unha programación de facturas**.
6. A aplicación xera a programación de facturas cos campos **Data de execución da factura**, **Data de corte da transacción**, e **Estado de execución** configurados do seguinte xeito:

    - **Data de execución da factura** establécese na data obrigada en función da frecuencia da factura.
    - **Data de corte da transacción** establécese o día anterior á **Data de execución da factura**.
    - **Estado de execución** configúrase automaticamente en **Non executar**. Cando a tarefa de creación automática de facturas se execute durante unha determinada data de execución da factura, actualizará este campo a **Execución correcta** ou **Erro na execución**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-quote-line"></a>Cree unha programación de facturas de prezo fixo para unha liña de cotización do proxecto

Cando a liña de oferta baseada en proxecto ten un método de facturación **Fixo**, o sistema crea unha programación de facturas baseada en fitos. Complete os seguintes pasos para xerar automaticamente esta programación para un conxunto fixo de fitos que se distribúen igualmente para o período do calendario.

1. Vaia a **Configuración** > **frecuencias de facturas** e configure unha frecuencia de facturas.
2. Na páxina **Ofertas**, abra a oferta do proxecto e na páxina **Resumo**, estableza a data de entrega solicitada.
3. Abra a liña de oferta de prezo fixo para a que necesita crear unha programación de fitos. 
4. No separador **Programación de facturas**, seleccione valores nos campos **Comezo da facturación** e **Frecuencia das facturas**. 
5. Na subgrade, seleccione **Xerar fitos periódicos**.
6. A aplicación xera a programación de facturas cun nome, data e importe de fito.

    - O nome do fito establécese na data obrigada en función da frecuencia das facturas.
    - O data do fito establécese na data obrigada en función da frecuencia das facturas.
    - O importe do fito calcúlase dividindo o importe da oferta na liña de oferta baseada en proxecto polo número de fitos obrigado pola frecuencia e o inicio da facturación e as datas de entrega solicitadas.
    - Se a liña de oferta tamén ten o importe do imposto estimado, este valor divídese entre cada fito por igual cando se xeran fitos periódicos.

### <a name="manually-create-milestones"></a>Crear fitos manualmente

Os fitos de prezo fixo tamén se poden xerar manualmente cando non se dividen periodicamente. Para crear un fito manualmente:

Abra a liña de oferta de prezo fixo na que necesita crear un fito. No separador **Programación da factura**, na subgrade, seleccione **+ Crear un novo fito da liña de oferta** e introduza a información requirida baseándose na seguinte táboa.

| **Campo** | **Localización** | **Descrición** | **Impacto descendente** |
| --- | --- | --- | --- |
| Nome do fito | Creación rápida | O nome do fito. | Isto propágase ao fito da liña de contrato do proxecto e á factura |
| Tarefa do proxecto | Creación rápida | Se o fito está ligado á tarefa do proxecto, pode usar esta referencia para engadir unha lóxica personalizada para establecer o estado do fito en función do estado da tarefa. | A aplicación non ten ningún impacto descendente desta referencia a unha tarefa. |
| Data do fito | Creación rápida | Estableza a data na que o proceso de creación automática de facturas debería buscar o estado deste fito para consideralo para a facturación. | Isto propágase ao fito da liña de contrato do proxecto e á factura. |
| Estado da factura | Creación rápida | Cando se crea un fito, este estado sempre se define como **Non está preparado para a facturación**. | Isto propágase ao fito da liña de contrato do proxecto e á factura. |
| Cantidade da liña | Creación rápida | Importe ou valor do fito que se facturará ao cliente. | Isto propágase ao fito da liña de contrato do proxecto e á factura. |
| Impostos | Creación rápida | Importe do imposto que se aplicará ao fito. | Isto propágase ao fito da liña de contrato do proxecto e á factura. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
