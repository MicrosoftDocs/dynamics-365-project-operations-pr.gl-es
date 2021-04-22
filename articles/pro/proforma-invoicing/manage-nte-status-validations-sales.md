---
title: Xestionar o estado de non superar e as validacións
description: Este tema ofrece información sobre as comprobacións de límite non superable realizadas en Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7026ff654a9db8e8a22bcef544b043af39865559
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866725"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Xestionar o estado de non superar e as validacións 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

## <a name="not-to-exceed-on-approvals"></a>Non superable nas aprobacións

Cando se envía unha entrada de tempo, gasto ou uso de material, créase un rexistro de aprobación. Se a aprobación é imputable e se asigna a unha liña de contrato de tempo e material, o sistema realiza unha comprobación de validación de non superable nos seguintes niveis:

  - Comprobar o límite establecido para o cliente na liña de contrato do proxecto
  - Comprobar o límite establecido para o cliente na liña de contrato
  - Comprobar o límite establecido para o cliente
  - Comprobar o límite establecido para o cliente no contrato

As comprobacións en cada nivel implican garantir que o importe do valor das vendas desta aprobación non infrinxirá o límite non superable nese nivel despois de contabilizar o importe do traballo pendente de facturación xa rexistrado e o importe facturado ata ese momento nese nivel.

Se supera a comprobación, a aprobación recibirá un estado de validación de **Correcto**.

Se non supera a comprobación, a aprobación recibirá un estado de validación de **Erro**. O detalle da validación de non superable informará ao usuario en que nivel fallou a validación.

Cando a entrada, o gasto ou o uso do material enviado considérase non imputable, o estado de validación de non exceder establécese en **Non aplicable** co detalle de validación igual a **Non aplicable**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Non superable en datos reais de vendas non facturadas

Cando se aproba unha entrada de tempo, gasto ou uso de material, créanse rexistros de custo e datos reais de vendas non facturados. Se a o dato real de vendas non facturadas creado é imputable e se asigna a unha liña de contrato de tempo e material, a aplicación realiza unha comprobación de validación de non superable nos seguintes niveis:

  - Comprobar o límite establecido para o cliente da liña de contrato do proxecto
  - Comprobar o límite establecido para o cliente na liña de contrato
  - Comprobar o límite establecido para o cliente
  - Comprobar o límite establecido para o cliente no contrato

As comprobacións en cada nivel garanten que o importe do valor das vendas do dato real non infrinxirá o límite non superable nese nivel despois de contabilizar o importe do traballo pendente de facturación xa rexistrado e o importe facturado ata ese momento nese nivel.

Se supera a comprobación, o dato real de vendas non facturadas reciben o estado non superable de **Confirmado**.

Se non supera a comprobación, o dato real de vendas non facturadas reciben o estado non superable de **Erro**. O detalle da validación informa ao usuario en que nivel fallou a validación.

Cando o dato real de vendas non facturadas se considera no imputable ou gratuíto, se non hai ningunha configuración de límite non superable en ningún dos catro niveis ou se o dato real que se está a crear é Custo, Retención, Unidade de recursos ou Vendas entre organizacións, os campos **Estado non superable** e **Detalle de validación de non superable** deben estar establecidos en **Non aplicable**.

## <a name="reset-the-not-to-exceed-status"></a>Restablecer o estado non superable

Pode realizar un restablecemento masivo do estado non superable. Os xestores de proxectos poden axustar a validación de non superable para priorizar a facturación dun traballo, tempo, gasto ou uso de material determinado sobre outros que xa están comprometidos a partir do importe non superable.

Despois de restablecer o estado de non superable nos datos reais de vendas non facturadas, o importe confirmado redúcese. O xestor do proxecto pode seleccionar outra entrada de traballo, tempo, gasto ou uso de material que anteriormente fallou na validación de non superable e reavaliar. Coa redución do importe comprometido, estes datos reais pasan a validación, o que axuda ao xestor de proxectos a exercer unha maior influencia e control sobre as transaccións facturables nese período.

Para restablecer o estado de non superable, seleccione un ou máis datos reais da vista **Traballo pendente de facturación de tempo e material** ou **Datos reais** e logo seleccione **Restablecer o estado de non superable**.

O estado de non superable restablécese a **Non avaliado** en todos os datos reais seleccionados relevantes. Os datos reais que restablecen o estado de non superable son os datos reais de vendas sen facturar que aínda non están facturados, non están nun borrador de factura e están marcados como imputables. Ignorase calquera outro dato real seleccionado.

## <a name="reevaluate-not-to-exceed-status"></a>Volver avaliar estado de non superable

Pode realizar un reavaliación masiva do estado de non superable. A reavaliación do estado de non superable é útil cando:

  - Houbo unha renegociación de límites non superables co cliente e haberá que volver avaliar os datos reais.
  - O xestor do proxecto quere axustar a facturación do traballo pendente de vendas non facturadas priorizando un traballo sobre outro.

Para reavaliar o estado de non superable, seleccione un ou máis datos reais da vista **Traballo pendente de facturación de tempo e material** ou **Datos reais** e logo seleccione **Reavaliar o estado de non superable**.

Todos os datos relevantes seleccionados cun límite non superable serán avaliados en comparación coa configuración do límite non superable. Os datos reais que son relevantes para reavaliar o estado de non superable son os datos reais de vendas sen facturar que non están facturados, non están nun borrador de factura e están marcados como imputables. Calquera outro dato real seleccionado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
