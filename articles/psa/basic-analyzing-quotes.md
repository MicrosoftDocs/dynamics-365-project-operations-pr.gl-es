---
title: Análise de ofertas de proxecto
description: Este tema fornece información sobre a análise de ofertas de proxecto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291257"
---
# <a name="analysis-of-project-quotes"></a>Análise de ofertas de proxecto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analiza as ofertas de proxectos para estimar a rendibilidade. Tamén analiza o axuste da oferta ás expectativas dos clientes sobre a data de entrega ou a data de finalización e sobre o orzamento.

## <a name="profitability-analysis"></a>Análise da rendibilidade

Project Service Automation analiza a rendibilidade empregando a marxe bruta e a marxe bruta axustada.

- A marxe bruta calcúlase mediante a seguinte fórmula:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- A marxe bruta axustada calcúlase mediante a seguinte fórmula:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Se os valores da marxe bruta e da marxe bruta axustada difiren por unha ampla marxe, gran parte do traballo da oferta clasifícase como non impoñible.

## <a name="analysis-of-customer-expectations"></a>Análise das expectativas do cliente

Pode analizar ofertas e xerar gráficos para as expectativas dos clientes sobre a programación e o orzamento se introduce valores para os seguintes campos:

- O campo **Data de entrega solicitada** no encabezado da oferta.
- O campo **Orzamento do cliente** para cada liña da oferta (para liñas baseadas en proxectos e liñas baseadas en produtos).

A análise das expectativas dos clientes sobre a programación realízase comparando a última data final do detalle da liña de oferta coa data de entrega solicitada en todas as liñas de oferta da oferta.

A análise das expectativas dos clientes sobre o orzamento realízase comparando a suma do orzamento total do cliente co importe ofertado en todas as liñas da oferta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]