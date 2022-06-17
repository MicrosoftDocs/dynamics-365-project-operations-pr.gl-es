---
title: Impacto real dun proxecto interno
description: Este artigo ofrece información sobre o impacto na táboa Reais en varios eventos para un proxecto interno en Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921346"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impacto real dun proxecto interno

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A seguinte táboa enumera os datos reais dos diferentes tipos de transaccións que se crean en varios eventos nun compromiso interno do proxecto.

| Evento | Dato real de custo | Exemplo |
|---|---|---|
| O tempo créase. | Non aplicable | <p>Bob Kozack, da unidade organizativa de Fabrikam US que ten un custo de 100 dólares estadounidenses (100 USD) por hora, está a traballar nun proxecto que se chama "Instalación de brazos en Adatum". Este proxecto está asignado a un método de facturación de prezo fixo na liña de contrato. Aquí tes unha entrada de tempo de mostra de Bob Kozak:</p><p>Bob Kozack - 8 horas</p> |
| O tempo é enviado. | Non aplicable | Créase unha liña de diario de custos para a entrada de tempo. A taxa de custo predeterminada introdúcese na entrada do diario. |
| A entrada de tempo lémbrase antes de ser aprobada. | Non aplicable | |
| O tempo está aprobado. | Créase un custo real. | <p>Novo real que se crea:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800</li></ul> |
| Cancelarase a aprobación horaria. | <p>Actualízase o estado de axuste do custo orixinal real **Axustado**.</p><p>Créase un custo real de reversión que ten un estado de axuste de **Inaxustable**.</p> | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul> |
| A entrada de hora lémbrase despois de ser aprobada. | <p>Actualízase o estado de axuste do custo orixinal real **Axustado**.</p><p>Créase un custo real de reversión que ten un estado de axuste de **Inaxustable**.</p> | <p>Reais existentes que se actualizan:</p><ul><li>**Custo real:** Bob Kozack, 8 horas, USD 800, *Axustado*</li></ul><p>Novo real que se crea para revertir o impacto financeiro anterior:</p><ul><li>**Custo real:** Bob Kozack, (8 h), (USD 800), *Inaxustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
