---
title: Por que o prezo por defecto é cero nos custos de tempo reais?
description: Resolución de problemas de por que o prezo por defecto é 0 nos custos por tempo reais.
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
ms.openlocfilehash: 65f2bc773a376800928cc3746691061d8e290f74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285796"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Por que o prezo por defecto é cero nos custos de tempo reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas Preguntas máis frecuentes aplícanse a valores reais onde a clase de transacción está definida a Tempo e o tipo de transacción é Custo. As tres seguintes comprobacións axudaranlle a solucionar por que o prezo son por defecto 0 nos valores reais de custos por tempo.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Verificación 1: Identificar a lista de prezos de custos para o proxecto

Busque o proxecto no campo de proxectos do valor real e vaia á páxina de proxecto. Prema a ligazón de unidade de contrato no campo. Na páxina Unidade de contrato, comprobe se a unidade de contrato ten unha lista de prezos na grade de Listas de prezos de custo.

Se hai máis dunha lista de prezos, xa identificou o problema. Project Service só admite unha lista de prezos por unidade organizativa. Elimina todas as listas de prezos desta entidade até que haxa só unha lista de prezos anexada a grade de Listas de prezos de custo da unidade organizativa.

Se non hai ningunha lista de prezos anexada á unidade organizativa, anote a moeda da unidade organizativa. Vaia a Project Service e, a seguir, Parámetros e abra o separador Listas de prezos. Comprobe se hai algunha lista de prezos con contexto definido como Custo e a moeda que coincide coa moeda da unidade organizativa.
 
Se non hai ningunha lista de prezos que se correspondan con esos criterios, xa identificou o problema. Asegúrese de ter polo menos unha lista de prezos cun contexto definido en Custo e cunha moeda que coincida coa moeda da unidade organizativa.

Se hai máis dunha lista de prezos que se correspondan con esos criterios, siga lendo este documento para facer máis comprobacións.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Verificación 2: Algunha das listas de prezos identificadas enriba é válida para a data específica no valor real de vendas por custo?

Para que Project Service considere unha lista de prezos como prezo por defecto, esa lista de prezos debe ser aplicable para a data no valor real de vendas por custo. Comprobe o seguinte para ver se as listas de prezos identificados enriba son aplicables:

- Comprobe se as datas de inicio e fin no separador xeral para as listas de prezos anexada non están baleiras. Se as datas de inicio e fin nas listas de prezos identificadas enriba está baleiras, xa identificou o problema. 
- Anote o campo de data de inicio no seu valor real de vendas por custo e comprobe se algunha das listas de prezos identificadas é aplicable para esa data. Por exemplo, a data do valor real de vendas por custo debería estar entre a data de inicio e a data de fin na lista de prezos. 
    - Se non hai ningunha lista de prezos que cubra esa data no valor real de vendas por custo, xa identificou o problema. Modificar as datas de inicio e fin da lista de prezos para asegurar que a lista de prezos cubra a data do valor real de vendas por custo. 
    - Se hai máis dunha lista de prezos que cubra a data no valor real de vendas por custo, xa identificou o problema. Pode corrixir isto editando as datas de inicio e fin das listas de prezos, de forma que haxa só unha lista de prezos que cubra a data do valor real de vendas por custo. 
    - Se só hai unha lista de prezos que cubra esa data do valor real de custo de tempo, vaia á seguinte verificación no documento.
Cando faga as correccións necesarias, cree novamente unha entrada de tempo, apróbea e verifique que o valor real de vendas por custo mostra un prezo válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Verificación 3: Hai un prezo na lista de prezos para as dimensions de prezos no valor real de vendas por custo?

Se concluíu correctamente as Verificacións 1 e 2, agora debe ter só unha lista de prezos é aplicable para a data do valor real de vendas por custo. Abra esta Lista de prezos do proxecto e vaia ao separador Prezos de rol. Asegúrese de que hai unha liña na grade para as dimensións de tempo no valor real de custo de tempo.

Se non hai ningunha fila na grade de prezos de rol para as dimensións de prezos no valor real de vendas por custo, xa identificou o problema. Cree unha liña na grade de prezos de Rol para as dimensións de prezos no valor real de vendas por custo. Cando termine, cree novamente unha entrada de tempo, apróbea e verifique que o valor real de vendas por custo mostra un prezo válido.
 
Se aínda non ve un prezo válido no valor real de vendas por custo despois de realizar as tres comprobacións anteriores, rexistre o tícket de asistencia.





[!INCLUDE[footer-include](../includes/footer-banner.md)]