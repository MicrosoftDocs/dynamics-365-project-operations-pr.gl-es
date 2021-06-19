---
title: Visión xeral do recoñecemento de ingresos
description: Este tema fornece información sobre o recoñecemento de ingresos en Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013754"
---
# <a name="revenue-recognition-overview"></a>Visión xeral do recoñecemento de ingresos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

En Dynamics 365 Project Operations, os principios de recoñecemento de ingresos varían en función do método de facturación seleccionado para un proxecto ou parte do proxecto. Este tema fornece información sobre o recoñecemento de ingresos en Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transaccións contabilizadas mediante o método de facturación de tempo e material

- O custo e o recoñecemento de ingresos están conectados. O custo da transacción e as vendas non facturadas contabilízanse mediante o [diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).
- O custo do proxecto e o perfil de ingresos determinan se as transaccións de vendas non facturadas se contabilizan no libro maior. Se **Acumular ingresos** está seleccionado, o sistema usa as contas **Valor das vendas WIP** e **Valor das vendas de ingresos acumulados** durante a contabilización. O seguinte é un exemplo deste método.  

  | Tipo de transacción | Débito/crédito | Importe  |
  | --- | --- | --- |
  | Valor de vendas WIP | Débito | 100 |
  | Valos de vendas de ingresos acumulados | Crédito | 100 |

- Os ingresos se recoñecen durante a facturación. O sistema usa a conta **Ingresos facturados** durante a contabilización. O seguinte é un exemplo deste método.  

  | Tipo de transacción | Débito/crédito | Importe  |
  | --- | --- | --- |
  | Saldo de cliente | Débito | 120 |
  | Imposto de vendas pendente de pago | Crédito | 20 |
  | Ingresos facturados | Crédito | 100 |

- Se se acumularon ingresos cando se contabilizan as vendas non facturadas, o sistema reverterá os ingresos acumulados na facturación.

  | Tipo de transacción | Débito/crédito | Importe  |
  | --- | --- | --- |
  | Valor de vendas WIP | Crédito | 100 |
  | Valos de vendas de ingresos acumulados | Débito | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transaccións contabilizadas mediante o método de facturación de prezo fixo

- O custo e o recoñecemento de ingresos están separados. O custo da transacción contabilízase mediante o [diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Non se crean transaccións de vendas sen facturar.
- Os ingresos pódense recoñecer durante a facturación se o custo do proxecto e o perfil de ingresos teñen **Principio empregado para os cálculos de finalización do proxecto** definido como **Sen WIP**. Use este método só para proxectos sinxelos a curto prazo.
- Os ingresos pódense recoñecer empregando estimacións de ingresos a prezos fixos, co método **Contrato completado** ou **Recoñecemento de ingresos por conclusión porcentual**.

## <a name="additional-resources"></a>Recursos adicionais
[Configurar a contabilidade para artigo de proxectos facturables](../project-accounting/configure-accounting-billable-projects.md)

[Proxectos de estimación de ingresos a prezo fixo](rev-rec-percentage-completion-method.md)

[Xestionar estimacións de ingresos](rev-rec-completed-contract-method.md)

[Métodos de custo para completar](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]