---
title: Análise de ofertas de proxecto
description: Este tema fornece información sobre a análise de ofertas de proxecto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751327"
---
# <a name="analysis-of-project-quotes"></a>Análise de ofertas de proxecto

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
