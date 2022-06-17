---
title: Datos reais
description: Este artigo ofrece información sobre como traballar con datos reais en Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924796"
---
# <a name="actuals"></a>Datos reais

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os datos reais representan o progreso financeiro e programado revisado e aprobado nun proxecto. Créanse cando se aproban as entradas de tempo, gastos e uso de material, as entradas de diario e as facturas.

> [!IMPORTANT]
> Os datos reais non deben editarse nin eliminarse do sistema. En caso contrario, a integridade financeira e calquera integración con outros sistemas financeiros e contables poderían verse afectadas negativamente. Microsoft Dynamics 365 Project Operations permítelle utilizar a reversión e a substitución de datos reais para editar os datos reais en varios puntos do ciclo de vida do proceso empresarial dos seus proxectos.

## <a name="recording-actuals-based-on-project-events"></a>Rexistro de datos reais baseados en eventos de proxecto

As operacións do proxecto rexistran as transaccións financeiras que se producen durante o ciclo de vida do compromiso do proxecto como reais. A creación de datos reais en varios eventos do ciclo de vida varía, dependendo de se o compromiso do proxecto utiliza o modelo de facturación de tempo e materiais ou o modelo de facturación de prezo fixo, e se está en fase de prevenda ou se trata dun proxecto interno.

Os artigos seguintes explican o impacto na táboa Reais en varios eventos para diferentes variacións:

- [Impacto real nun compromiso de tempo e materiais](ActualsonTM.md)
- [Os datos reais afectan a un compromiso de prezo fixo](ActualonFP.md)
- [Impacto real durante a fase previa á venda dun compromiso](ActualonPreSales.md)
- [Impacto real dun proxecto interno](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
