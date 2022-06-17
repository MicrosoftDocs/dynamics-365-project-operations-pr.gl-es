---
title: Rexistro de tempo, gastos e uso de material para compoñentes subcontratados
description: Este artigo explica como Microsoft fai un seguimento do tempo, dos gastos e do uso de material rexistrado en proxectos de compoñentes subcontratados Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927648"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Rexistro de tempo, gastos e uso de material en proxectos para compoñentes subcontratados

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo explica como Microsoft fai un seguimento do tempo, dos gastos e do uso de material rexistrado en proxectos de compoñentes subcontratados Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Custo do tempo do subcontratista nos proxectos
En Operacións de Proxectos, os traballadores por contrato poden rexistrar o tempo nos proxectos dun xeito similar ao dos empregados. Ao introducir o tempo de proxectos e/ou tarefas do proxecto, un traballador contratado pode seleccionar un subcontrato e unha liña de subcontrato específicos.

Cando se aprobe o tempo entregado polos traballadores contratados, o custo do proxecto rexístrase utilizando a taxa de custo unitario que se establece para ese recurso contratado no **Prezos dos roles** sección da lista de prezos de compra do subcontrato.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Custo dos gastos subcontratados dos proxectos
Ao introducir os gastos realizados en proxectos, pode seleccionar unha liña de subcontrato e subcontrato na entrada de gasto. 

Cando se presenta e aprobe esta entrada de gasto, o custo do gasto rexístrase no proxecto en función do custo unitario que se establece para esa categoría de transacción no **Prezos das categorías** sección da lista de prezos de compra do subcontrato.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Custo dos materiais subcontratados nos proxectos
Ao introducir o uso de material en proxectos, pode seleccionar unha liña de subcontrato e subcontrato no rexistro de uso de material. Cando se envía e aproba o rexistro de uso do material, o custo do material rexístrase no proxecto en función do custo unitario configurado para ese produto no **Elementos da lista de prezos** sección da lista de prezos de subcontratación.

Tamén se pode rexistrar o uso de material para produtos de escritura en proxectos. Este tipo de uso de material tamén se pode vincular a unha liña de subcontratación e subcontratación. Ao rexistrar o uso de material para produtos de escritura, cómpre introducir o custo unitario do produto de escritura. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
