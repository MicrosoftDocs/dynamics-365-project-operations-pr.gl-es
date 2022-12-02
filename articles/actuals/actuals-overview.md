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

Os datos reais representan o progreso financeiro e programado revisado e aprobado nun proxecto. Créanse cando se aproban as entradas de tempo, gasto e uso de material, as entradas do diario e as facturas.

> [!IMPORTANT]
> Os datos reais non deben editarse nin eliminarse do sistema. En caso contrario, a integridade financeira e calquera integración con outros sistemas financeiros e contables poderían verse afectadas negativamente. Microsoft Dynamics 365 Project Operations permítelle utilizar a inversión e a substitución de datos reais para editar os datos reais en varios puntos do ciclo de vida do proceso de negocio dos seus proxectos.

## <a name="recording-actuals-based-on-project-events"></a>Rexistro de datos reais baseados en eventos de proxecto

Project Operations rexistra as transaccións financeiras que se producen durante o ciclo de vida da interacción dun proxecto como datos reais. A creación de datos reais en varios eventos do ciclo de vida varía, dependendo de se o compromiso do proxecto utiliza o modelo de facturación de tempo e materiais ou o modelo de facturación de prezo fixo, e se está na fase de prevenda ou se é un proxecto interno.

Os artigos seguintes explican o impacto na táboa Datos reais en varios eventos para diferentes variacións:

- [Impacto dos datos reais nunha interacción de tempo e materiais](ActualsonTM.md)
- [Impacto dos datos reais nunha interacción de prezo fixo](ActualonFP.md)
- [Impacto dos datos reais durante a fase de prevenda dunha interacción](ActualonPreSales.md)
- [Impacto dos datos reais para un proxecto interno](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
