---
title: Por que o prezo por defecto é cero nas ventas por tempo reais?
description: Resolución de problemas de por que o prezo por defecto é 0 nas vendas por tempo reais.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
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
ms.openlocfilehash: 5f72e0db94392a35fee9fdcf2c4adb8a08feef13
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146211"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Por que o prezo por defecto é cero nas ventas por tempo reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas Preguntas máis frecuentes aplícanse a valores reais onde a clase de transacción está definida a Tempo e o tipo de transacción é Vendas sen facturar. As tres seguintes comprobacións axudaranlle a solucionar por que os prezos (facturación) son por defecto 0 nos valores reais de vendas por tempo.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Verificación 1: Identificar a lista de prezos de vendas para o proxecto

Busque o proxecto no campo de proxectos do valor real e vaia á páxina de proxecto. A seguir, vaia ao separador Vendas e na grade de liñas de contrato do proxecto, prema na ligazón no campo Contrato do proxecto. Abrirase a páxina Contrato do proxecto. Na páxina Contrato do proxecto, vaia ao separador Listas de prezos do proxecto. Comprobe se hai polo menos unha lista de prezos anexada aquí. Se non hai ningunha lista de prezos anexada na grade Listas de prezos de proxecto en Contrato do proxecto, xa identificou o problema. Anexe unha lista de prezos á grade de Listas de prezos de proxecto. As listas de prezos que se poden anexar aquí deben ter o campo de contexto definido en Vendas e o campo de moeda na lista de prezos debe coincidir co campo de moneda no Contrato do proxecto. Cando faga as correccións necesarias, cree novamente unha entrada de tempo, apróbea e verifique que o valor real de vendas sen facturar mostra un prezo válido. 

Se ten unha ou varias listas de prezos anexadas na grade Listas de prezos de proxecto do Contrato do proxecto, vaia á seguinte verificación no documento.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Verificación 2: Algunha das listas de prezos identificadas enriba é válida para a data específica no valor real de vendas por tempo?

Para que Project Service considere unha lista de prezos como prezo por defecto, esa lista de prezos debe ser aplicable para a data no valor real de vendas por tempo. Comprobe o seguinte para ver se as listas de prezos identificados enriba son aplicables:
- Comprobe se as datas de inicio e fin no separador xeral para as listas de prezos anexada non están baleiras. Se as datas de inicio e fin nas listas de prezos identificadas enriba está baleiras, xa identificou o problema. 
- Anote o campo de data de inicio no seu valor real de vendas por tempo e comprobe se algunha das listas de prezos identificadas é aplicable para esa data. Por exemplo, a data do valor real de vendas por tempo debería estar entre a data de inicio e a data de fin na lista de prezos. 
    - Se non hai ningunha lista de prezos que cubra esa data no valor real de vendas por tempo, xa identificou o problema. Modificar as datas de inicio e fin da lista de prezos para asegurar que a lista de prezos cubra a data do valor real de vendas por tempo. 
    - Se hai máis dunha lista de prezos que cubra a data no valor real de vendas por tempo, xa identificou o problema. Pode corrixir isto editando as datas de inicio e fin das listas de prezos, de forma que haxa só unha lista de prezos que cubra a data do valor real de vendas por tempo. 
    - Se só hai unha lista de prezos que cubra esa data do valor real de vendas por tempo, vaia á Verificación 3.
Cando faga as correccións necesarias, cree novamente unha entrada de tempo, apróbea e verifique que o valor real de vendas por tempo mostra un prezo válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Verificación 3: Hai un prezo na lista de prezos para as dimensions de prezos no valor real de vendas por tempo?

Se concluíu correctamente as Verificacións 1 e 2, agora debe ter só unha lista de prezos é aplicable para a data do valor real de vendas por tempo. Abra esta Lista de prezos do proxecto e vaia ao separador Prezos de rol. Asegúrese de que hai unha liña na grade para as dimensións de tempo no valor real de vendas por tempo.

Se non hai ningunha fila na grade de prezos de rol para as dimensións de prezos no valor real de vendas por tempo, xa identificou o problema. Cree unha liña na grade de prezos de Rol para as dimensións de prezos no valor real de vendas por tempo. Cando termine, cree novamente unha entrada de tempo, apróbea e verifique que o valor real de vendas por tempo mostra un prezo válido.

Se aínda non ve un prezo válido no valor real de vendas por tempo despois de realizar as tres comprobacións anteriores, rexistre o tícket de asistencia. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]