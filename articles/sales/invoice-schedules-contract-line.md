---
title: Cree calendarios de facturas nunha liña de contrato baseada en proxectos
description: Este artigo ofrece información sobre como crear programacións de facturas e fitos nas liñas de contrato.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: afc6357b7b221b91674035ae3181ef84eed8d586
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825095"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line"></a>Cree calendarios de facturas nunha liña de contrato baseada en proxectos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Pode crear unha programación de facturas nunha liña de contrato baseado en proxecto. A facturación só se permite despois de gañar o contrato e crear un contrato de proxecto. Unha programación de facturas permite crear automaticamente borradores de facturas para unha liña de contrato baseado en proxecto. Non obstante, se só crea facturas manualmente, pode omitir a creación de programacións de facturas nas liñas de contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Crear unha programación de facturas de tempo e material para unha liña de contrato

Cando a liña de contrato baseado en proxecto ten un método de facturación de tempo e material, pode crear una programación de facturas baseada en datas. Para xerar automaticamente unha programación de facturas baseada en datas, complete os seguintes pasos.

1. Vaia a **Configuración** > **Frecuencias de facturas** e configure unha frecuencia de facturas.
2. Vaia ao rexistro do contrato do proxecto e no separador **Resumo**, no campo **Data de entrega solicitada**, seleccione unha data.
3. Abra a liña de contrato **Tempo e material** para a que vai crear unha programación de facturas baseada en datas. 
4. No separador **Programación de facturas**, seleccione a data de inicio da facturación e a frecuencia das facturas.
5. Na subgrade, seleccione **Xerar unha programación de facturas**. A programación de facturas xérase cos campos **Data de execución da factura**, **Data de corte da transacción**, e **Estado de execución** configurados do seguinte xeito:

    - **Data de execución da factura**: Esta data depende da frecuencia da factura.
    - **Data de corte da transacción**: O día anterior á data de execución da factura.
    - **Estado de execución**: Configúrase automaticamente en **Non executar**. Cando a tarefa de creación automática de facturas se execute durante unha determinada data de execución da factura, actualiza este campo a **Execución correcta** ou **Erro na execución**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Crear unha programación de facturas de prezo fixo para unha liña de contrato

Cando a liña de contrato o ten un método de facturación fixo, pode crear unha programación de facturas baseada en fitos. 

> [!NOTE]
> Non se poden crear fitos nunha liña de contrato se non hai ningún proxecto asignado á liña de contrato.

Complete os seguintes pasos para xerar unha programación de facturas baseada en fitos para un conxunto fixo de fitos que se distribúen igualmente para o período do calendario.

1. Vaia a **Configuración** > **Frecuencias de facturas** e configure unha frecuencia de facturas.
2. Vaia ao rexistro do contrato do proxecto e no separador **Resumo**, no campo **Data de entrega solicitada**, seleccione unha data.
3. Abra a liña de contrato de **Prezo fixo** para a que esta a crear unha programación de fitos. No separador **Fitos de facturación**, seleccione a data de inicio da facturación e a frecuencia das facturas. 
4. Na subgrade, seleccione **Xerar fitos periódicos**. A programación de facturas xérase cos campos **Nome do fito**, **Data do Fito** e **Cantidade de fitos** configurados do seguinte xeito:

    - **Nome do fito**: Este nome está ditado pola frecuencia da factura.
    - **Data do fito**: Esta data depende da frecuencia da factura.
    - **Importe do fito**: Este importe calcúlase dividindo o importe do contrato na liña de contrato polo número de fitos obrigado pola frecuencia e o inicio da facturación e as datas de entrega solicitadas.

    Se a liña de contrato ten un valor no campo **Importe estimado do imposto**, este campo tamén se reparte a cada fito por igual cando se xeran fitos periódicos.

Os fitos de facturación deben ser iguais ao valor contratado da liña de contrato. Se non o son, recibirá un erro na páxina **Liña de contrato**. Pode corrixir o erro comprobando que os fitos de facturación totalizan o valor contratado da liña creando, editando ou eliminando fitos. Despois de realizados os cambios, actualice a páxina para eliminar o erro.

### <a name="manually-create-milestones"></a>Crear fitos manualmente

Pode xerar fitos de prezo fixo manualmente cando non se dividen periodicamente. Complete os seguintes pasos para crear manualmente un fito.

1. Abra a liña de contrato de prezo fixo para a que está a crear un fito e, no separador **Programación de facturas**, na subgrade, seleccione **+ Crear un novo fito de liña de contrato**. 
2. Na páxina **Creación de fitos**, introduza a información requirida baseándose na seguinte táboa.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| Nome do fito | Creación rápida | Campo de texto para o nome do fito. | Isto trasládase ao fito da liña de contrato do proxecto e á factura. |
| Tarefa do proxecto | Creación rápida | Se o fito está ligado á tarefa do proxecto, use esta referencia para engadir unha lóxica personalizada para establecer o estado do fito en función do estado da tarefa. | A aplicación non ten ningún impacto descendente desta referencia a unha tarefa. |
| Data do fito | Creación rápida | Estableza a data na que o proceso de creación automática de facturas debería buscar o estado deste fito para consideralo para a facturación. | Isto trasládase ao fito da liña de contrato do proxecto e á factura. |
| Estado da factura | Creación rápida | Cando se crea un fito, este estado sempre se define como **Non está preparado para a facturación** ou **Non iniciado**. | Isto trasládase ao fito da liña de contrato do proxecto e á factura. |
| Cantidade da liña | Creación rápida | Importe ou valor do fito que se facturará ao cliente. | Isto trasládase ao fito da liña de contrato do proxecto e á factura. |
| Impostos | Creación rápida | O importe do imposto aplicado no fito. | Isto trasládase ao fito da liña de contrato do proxecto e á factura. |

3. Seleccione **Gardar e pechar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
