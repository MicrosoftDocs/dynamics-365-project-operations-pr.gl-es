---
title: Crear calendarios de facturas nunha liña de contrato de proxecto
description: Este artigo ofrece información sobre a creación de programacións e fitos de facturación.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1a6d0647ee012212a74a674cfa4e995d0e375b77
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824718"
---
# <a name="create-invoice-schedules-on-a-project-contract-line"></a>Crear calendarios de facturas nunha liña de contrato de proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Pode anexar unha programación de facturas nunha liña de contrato baseado en proxecto. A facturación só se permite despois de gañar o contrato para crear un contrato de proxecto. As programacións de facturas permiten crear borradores de facturas dunha liña de contrato baseado en proxecto automaticamente. Se ten previsto crear sempre facturas manualmente, pode omitir a creación de programacións de facturas nunha liña de contrato baseado en proxecto ou nunha liña de contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Crear unha programación de facturas de tempo e material nunha liña de contrato baseado en proxecto

Cando a liña de contrato baseado en proxecto ten un método de facturación de tempo e material, pode crear una programación de facturas baseada en datas. Para xerar automaticamente unha programación de facturas baseada en datas, complete os seguintes pasos.

1. Vaia a **Configuración** > **Frecuencias de facturas** para configurar a frecuencia das facturas.
2. Abra o contrato do proxecto e no separador **Resumo** e estableza a data de entrega solicitada.
3. Abra a liña de contrato de tempo e material para a que desexa crear unha programación de facturas baseada na data. 
4. No separador **Programación de facturas**, seleccione unha data de inicio de facturación e a frecuencia das facturas. 
5. Na subgrade, seleccione **Xerar unha programación de facturas**.

    O sistema xera a programación das facturas coa seguinte información de campo:

    - **Data de execución da factura** establécese na data segundo a frecuencia das facturas.
    - **Data de corte da transacción** establécese o día anterior á **Data de execución da factura**.
    - **Estado de execución** configúrase automaticamente en **Non executar**. Cando a tarefa de creación automática de facturas se execute durante unha determinada **Data de execución da factura**, actualiza este campo a **Execución correcta** ou **Erro na execución**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Crear unha programación de facturas de prezo fixo para unha liña de contrato baseado en proxecto

Cando unha liña de contrato baseada en proxecto ten un método de facturación a prezo fixo, pode crear unha programación de facturas baseada en fitos. Complete os seguintes pasos para xerar automaticamente unha programación de facturas baseada en fitos para un conxunto fixo de fitos que se distribúen por igual durante o período do calendario.

1. Vaia a **Configuración** > **Frecuencias de facturas** para configurar a frecuencia das facturas.
2. Abra o contrato do proxecto e no separador **Resumo** e estableza a data de entrega solicitada.
3. Abra a liña de contrato de prezo fixo na que necesita crear un calendario de fitos. 
4. No separador **Programación de facturas (fitos de facturación)**, seleccione unha data de inicio de facturación e a frecuencia das facturas. 
5. Na subgrade, seleccione **Xerar fitos periódicos**.

    O sistema xera a programación das facturas coa seguinte información de fitos.

    - **Nome do fito** establécese na data que se dita en función da frecuencia das facturas.
    - **Data do fito** establécese na data que se dita en función da frecuencia das facturas.
    - **Importe de fito** calcúlase dividindo o importe do contrato na liña de contrato baseado en proxecto polo número de fitos ditados pola frecuencia, o inicio da facturación e as datas de entrega solicitadas.
    - Se a liña de contrato ten un valor no campo **Importe estimado do imposto**, este campo tamén se reparte a cada fito por igual cando se xeran fitos periódicos.

Os fitos de facturación deberían ser iguais ao valor contratado da liña de contrato baseado en proxecto. Se non son iguais, prodúcese un erro. Pode corrixir ese erro comprobando que os fitos de facturación totalizan o valor contratado da liña creando, editando ou eliminando fitos. Despois de facer os cambios, actualice a páxina.

### <a name="manually-create-milestones"></a>Crear fitos manualmente

Os fitos de prezo fixo pódense xerar manualmente cando non se dividen periodicamente. Para crear un fito manualmente, complete os seguintes pasos.

1. Abra a liña de contrato de prezo fixo na que quere crear un fito. 
2. No separador **Programación de facturas**, na subgrade, seleccione **+ Crear un novo fito de liña de contrato**.
3. No formulario **Creación de fito**, introduza a información requirida baseándose na seguinte táboa. 

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| Nome do fito | Creación rápida | Campo de texto para o nome do fito. | Este campo inclúese no fito da liña de contrato do proxecto e na factura. |
| Tarefa do proxecto | Creación rápida | Se o fito está ligado a unha tarefa do proxecto, use esta referencia para engadir lóxica personalizada e establecer o estado do fito en función do estado da tarefa. | Non hai ningún impacto descendente desta referencia a unha tarefa. |
| Data do fito | Creación rápida | A data na que o proceso de creación automática de facturas debería buscar o estado deste fito para consideralo para a facturación. | Isto inclúese no fito da liña de contrato do proxecto e na factura. |
| Estado da factura | Creación rápida | Cando se crea o fito, este estado sempre se define como **Non está listo para facturar** ou **Non iniciado**. | Isto inclúese no fito da liña de contrato do proxecto e na factura. |
| Cantidade da liña | Creación rápida | O importe ou o valor do fito que se facturará ao cliente. | Este campo inclúese no fito da liña de contrato do proxecto e na factura, |
| Impostos | Creación rápida | O importe do imposto aplicado no fito. | Isto inclúese no fito da liña de contrato do proxecto e na factura. |

4. Seleccione **Gardar e pechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
