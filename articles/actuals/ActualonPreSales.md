---
title: Impacto real durante a fase previa á venda dun compromiso
description: Este tema ofrece información sobre o impacto na táboa Reais en varios eventos mentres un compromiso está en fase de prevenda en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577234"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impacto real durante a fase previa á venda dun compromiso

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A seguinte táboa enumera os datos reais dos diferentes tipos de transaccións que se crean en varios eventos durante a fase previa á venda dun compromiso do proxecto.

| Evento | Dato real de custo | Exemplo |
|---|---|---|
| O tempo créase. | Non aplicable | <p>Bob Kozack, da unidade organizativa de Fabrikam US que ten un custo de 100 dólares estadounidenses (100 USD) por hora, está a traballar nun proxecto que se chama "Instalación de brazos en Adatum". Este proxecto está asignado a un método de facturación de prezo fixo na liña de contrato. Aquí tes unha entrada de tempo de mostra de Bob Kozak:</p><p>Bob Kozack - 8 horas</p> |
| O tempo é enviado. | Non aplicable | Créase unha liña de diario de custos para a entrada de tempo. A taxa de custo predeterminada introdúcese na entrada do diario. |
| A entrada de tempo lémbrase antes de ser aprobada. | Non aplicable | |
| O tempo está aprobado. | Créase un custo real. | <p>Novo real que se crea:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800</li></ul> |
| A aprobación horaria está cancelada. | <p>Actualízase o estado de axuste do custo orixinal real **Axustado**.</p><p>Créase un custo real de reversión que ten un estado de axuste de **Inaxustable**.</p> | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul> |
| A entrada de hora lémbrase despois de ser aprobada. | <p>Actualízase o estado de axuste do custo orixinal real **Axustado**.</p><p>Créase un custo real de reversión que ten un estado de axuste de **Inaxustable**.</p> | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul> |
| Gañouse a cotización e créase un contrato. | <p>Actualízase o estado de axuste dos antigos custos reais **Axustado**.</p><p>Créanse os custos reais de reversión que teñen un estado de axuste de **Inaxustable**.</p><p>Os novos custos reais créanse despois de que se reavalien as regras contractuais.</p> | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul><p>Novos datos reais que se crean para o impacto financeiro reavaliado cando se gaña a cotización e se crea o contrato:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800</li><li>**Vendas reais non facturadas:** Bob Kozack, 8 horas, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
