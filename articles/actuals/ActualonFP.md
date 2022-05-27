---
title: Os datos reais afectan a un compromiso de prezo fixo
description: Este tema ofrece información sobre o impacto na táboa Reais en varios eventos durante o ciclo de vida dun compromiso de prezo fixo en Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579226"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Os datos reais afectan a un compromiso de prezo fixo

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A seguinte táboa enumera os datos reais dos diferentes tipos de transaccións que se crean en varios eventos nun compromiso de prezo fixo.

| Evento | Dato real de custo | Dato real de vendas sen facturar | Vendas facturadas reais | Exemplo |
|---|---|---|---|---|
| O tempo créase. | Non aplicable | Non aplicable | Non aplicable | <p>Bob Kozack, da unidade organizativa de Fabrikam US que ten un custo de 100 dólares estadounidenses (100 USD) por hora, está a traballar nun proxecto que se chama "Instalación de brazos en Adatum". Este proxecto está asignado a un método de facturación de prezo fixo na liña de contrato. Aquí tes unha entrada de tempo de mostra de Bob Kozak:</p><p>Bob Kozack - 8 horas</p> |
| O tempo é enviado. | Non aplicable | Non aplicable | Non aplicable | Créase unha liña de diario de custos para a entrada de tempo. A taxa de custo predeterminada introdúcese na entrada do diario. |
| A entrada de tempo lémbrase antes de ser aprobada. | Non aplicable | Non aplicable | Non aplicable | |
| O tempo está aprobado. | Créase un custo real. | Non aplicable | Non aplicable | <p>Novo real que se crea:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800</li></ul> |
| A aprobación horaria está cancelada. | <p>Actualízase o estado de axuste do custo orixinal real **Axustado**.</p><p>Créase un custo real de reversión que ten un estado de axuste de **Inaxustable**.</p> | Non aplicable | Non aplicable | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul> |
| A entrada de hora lémbrase despois de ser aprobada. | <p>Actualízase o estado de axuste do custo orixinal real **Axustado**.</p><p>Créase un custo real de reversión que ten un estado de axuste de **Inaxustable**.</p> | Non aplicable | Non aplicable | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul> |
| O contrato está confirmado. | <p>Actualízase o estado de axuste dos antigos custos reais **Axustado**.</p><p>Créanse os custos reais de reversión que teñen un estado de axuste de **Inaxustable**.</p><p>Os novos custos reais créanse despois de que se reavalien as regras contractuais.</p> | Non aplicable | Non aplicable | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul><p>Novo real que se crea para o impacto financeiro reavaliado:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800</li></ul> |
| Créase unha factura. | Non aplicable | Non aplicable | Non aplicable | |
| A factura confírmase cun fito. | Non aplicable | Non aplicable | Créanse novos datos reais de vendas facturadas baseados en fitos. | <p>Reais existentes que permanecen sen cambios:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800</li></ul><p>Novo real que se crea para rexistrar os valores de vendas facturados:</p><ul><li>**Vendas facturadas reais:** Milestone, USD 5,000</li></ul> |
| A factura corríxese para acreditar o fito. | Non aplicable | Non aplicable | Créanse os datos reais de vendas facturados por reversión. | <p>Reais existentes que permanecen sen cambios:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, 800 USD</li></ul><p>Reais existentes que se actualizan:</p><ul><li>**Vendas facturadas reais:** Milestone, USD 5,000, *Axustado*</li></ul><p>Novo real que se crea para revertir os valores de vendas facturados anteriores:</p><ul><li>**Vendas facturadas reais:** Milestone (5.000 USD), *Inaxustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
