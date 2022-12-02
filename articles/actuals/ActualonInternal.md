---
title: Impacto dos datos reais para un proxecto interno
description: Este artigo ofrece información sobre o impacto na táboa Datos reais en varios eventos para un proxecto interno en Microsoft Dynamics 365 Project Operations.
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
# <a name="actuals-impact-for-an-internal-project"></a>Impacto dos datos reais para un proxecto interno

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A seguinte táboa enumera os datos reais dos diferentes tipos de transaccións que se crean en varios eventos nunha interacción de proxecto interno.

| Evento | Dato real de custo | Exemplo |
|---|---|---|
| Créase o tempo. | Non aplicable | <p>Bob Kozack, da unidade organizativa de Fabrikam US que ten un custo de 100 dólares estadounidenses (100 USD) por hora, está a traballar nun proxecto que se chama "Instalación de brazos en Adatum". Este proxecto está asignado a un método de facturación de prezo fixo na liña de contrato. Aquí ten unha mostra de entrada de tempo de Bob Kozak:</p><p>Bob Kozack - 8 horas</p> |
| Envíase o tempo. | Non aplicable | Créase unha liña de diario de custo para a entrada de tempo. A taxa de custo predefinida introdúcese na entrada do diario. |
| A entrada de tempo recupérase antes de ser aprobada. | Non aplicable | |
| O tempo apróbase. | Créase un dato real de custo. | <p>Novo dato real que se crea:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD</li></ul> |
| Cancelarase a aprobación de tempo. | <p>Actualízase o estado de axuste do dato real de custo orixinal a **Axustado**.</p><p>Créase un dato real de custo reversión que ten un estado de axuste de **Non axustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD, *Axustado*</li></ul><p>Novo dato real que se crea para reverter o impacto financeiro previo:</p><ul><li>**Dato real de custo:** Bob Kozack, (8 horas), (800 USD), *Non axustable*</li></ul> |
| A entrada de tempo recupérase despois de ser aprobada. | <p>Actualízase o estado de axuste do dato real de custo orixinal a **Axustado**.</p><p>Créase un dato real de custo reversión que ten un estado de axuste de **Non axustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Dato real de custo:** Bob Kozack, 8 horas, 800 USD, *Axustado*</li></ul><p>Novo dato real que se crea para reverter o impacto financeiro previo:</p><ul><li>**Dato real de custo:** Bob Kozack, (8 horas), (800 USD), *Non axustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
