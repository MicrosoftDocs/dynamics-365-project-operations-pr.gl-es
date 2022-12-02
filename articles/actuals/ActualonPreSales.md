---
title: Impacto dos datos reais durante a fase de prevenda dunha interacción
description: Este artigo ofrece información sobre o impacto na táboa Datos reais en varios eventos mentres unha interacción está na fase de prevenda en Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922358"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impacto dos datos reais durante a fase de prevenda dunha interacción

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A seguinte táboa enumera os datos reais dos diferentes tipos de transaccións que se crean en varios eventos durante a fase de prevenda dunha interacción de proxecto.

| Evento | Dato real de custo | Exemplo |
|---|---|---|
| Créase o tempo. | Non aplicable | <p>Bob Kozack, da unidade organizativa de Fabrikam US que ten un custo de 100 dólares estadounidenses (100 USD) por hora, está a traballar nun proxecto que se chama "Instalación de brazos en Adatum". Este proxecto está asignado a un método de facturación de prezo fixo na liña de contrato. Aquí ten unha mostra de entrada de tempo de Bob Kozak:</p><p>Bob Kozack - 8 horas</p> |
| Envíase o tempo. | Non aplicable | Créase unha liña de diario de custo para a entrada de tempo. A taxa de custo predefinida introdúcese na entrada do diario. |
| A entrada de tempo recupérase antes de ser aprobada. | Non aplicable | |
| O tempo apróbase. | Créase un dato real de custo. | <p>Novo dato real que se crea:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD</li></ul> |
| Cancelase a aprobación de tempo. | <p>Actualízase o estado de axuste do dato real de custo orixinal a **Axustado**.</p><p>Créase un dato real de custo reversión que ten un estado de axuste de **Non axustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD, *Axustado*</li></ul><p>Novo dato real que se crea para reverter o impacto financeiro previo:</p><ul><li>**Dato real de custo:** Bob Kozack, (8 horas), (800 USD), *Non axustable*</li></ul> |
| A entrada de tempo recupérase despois de ser aprobada. | <p>Actualízase o estado de axuste do dato real de custo orixinal a **Axustado**.</p><p>Créase un dato real de custo reversión que ten un estado de axuste de **Non axustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD, *Axustado*</li></ul><p>Novo dato real que se crea para reverter o impacto financeiro previo:</p><ul><li>**Dato real de custo:** Bob Kozack, (8 horas), (800 USD), *Non axustable*</li></ul> |
| Gáñase a oferta e créase un contrato. | <p>Actualízase o estado de axuste dos datos reais de custo antigos a **Axustado**.</p><p>Créanse datos reais de custo de reversión que teñen un estado de axuste de **Non axustable**.</p><p>Os novos datos reais de custo créanse despois de que se reavalien as regras contractuais.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD, *Axustado*</li></ul><p>Novo dato real que se crea para reverter o impacto financeiro previo:</p><ul><li>**Dato real de custo:** Bob Kozack, (8 horas), (800 USD), *Non axustable*</li></ul><p>Novos datos reais que se crean para o impacto financeiro reavaliado cando se gaña a oferta e se crea o contrato:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD</li><li>**Dato real de vendas non facturadas:** Bob Kozack, 8 horas, 1600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
