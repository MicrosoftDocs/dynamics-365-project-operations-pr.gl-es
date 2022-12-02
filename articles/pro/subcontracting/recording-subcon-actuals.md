---
title: Rexistro de tempo, gastos e uso de material para compoñentes subcontratados
description: Este artigo explica como Microsoft Dynamics 365 Project Operations fai un seguimento do tempo, dos gastos e do uso de material rexistrados en proxectos de compoñentes subcontratados.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522511"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Rexistro de tempo, gastos e uso de material en proxectos para compoñentes subcontratados

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Este artigo explica como Microsoft Dynamics 365 Project Operations fai un seguimento do tempo, dos gastos e do uso de material rexistrados en proxectos de compoñentes subcontratados.

## <a name="costing-for-subcontractor-time-on-projects"></a>Custo do tempo do subcontratista nos proxectos
En Project Operations, os traballadores por contrato poden rexistrar o tempo nos proxectos dun xeito similar ao dos empregados. Ao introducir o tempo en proxectos e/ou tarefas de proxecto, un traballador por contrato pode seleccionar un subcontrato e unha liña de subcontrato específicos.

Cando se aprobe o tempo enviado polos traballadores por contrato, o custo do proxecto rexístrase utilizando a taxa de custo unitario que se establece para ese recurso de traballador contratado na sección **Prezos de rol** da lista de prezos de compra do subcontrato.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Costes de gastos subcontratados en proxectos
Ao introducir os gastos incorridos en proxectos, pode seleccionar un subcontrato e unha liña de subcontrato na entrada de gasto. 

Cando se aprobe e envíe esta entrada de tempo, o custo do gasto rexístrase no proxecto segundo o custo unitario que se establece para esa categoría de transacción na sección **Prezos de categoría** da lista de prezos de compra do subcontrato.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Costes de materiais subcontratados en proxectos
Ao introducir o uso de material en proxectos, pode seleccionar un subcontrato e unha liña de subcontrato no rexistro de uso de material. Cando se aprobe e envíe o rexistro de uso de material, o custo do material rexístrase no proxecto segundo o custo unitario que se establece para ese produto na sección **Elemento de lista de prezos** da lista de prezos do subcontrato.

Tamén se pode rexistrar o uso de material para produtos fóra de catálogo en proxectos. Este tipo de uso de material tamén se pode vincular a un subcontrato e unha liña de subcontrato. Ao rexistrar o uso de material para produtos fóra de catálogo, cómpre introducir o custo unitario do produto fóra de catálogo. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
