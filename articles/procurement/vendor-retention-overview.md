---
title: Visión xeral da retención de fornecedores
description: Este tema ofrece unha visión xeral das capacidades de retención de fornecedores.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588458"
---
# <a name="vendor-retention-overview"></a>Visión xeral da retención de fornecedores

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

A súa organización pode querer reter unha parte dos pagaentos aos fornecedores que traballan en proxectos para a súa organización. Por exemplo, antes de pagarlle ao fornecedor, é posible que queira asegurarse de que os artigos e servizos que proporcionaron cumpran as súas expectativas.

Cando negocie compras de proxectos con fornecedores, pode especificar as condiciones de retención de fornecedores que inclúan a porcentaxe ou a cantidade a reter. A medida que o fornecedor entrega artigos e servizos, vostede deduce a súa porcentaxe ou cantidade de retención especificada do seu pagamento ao fornecedor. Cando o proxecto estea rematado ou chegue a unha fase provisional como se especifica no contrato do fornecedor, liberará a cantidade retida e creará un pagamento ao fornecedor.

## <a name="vendor-retention-example"></a>Exemplo de retención de fornecedores

O seguinte exemplo mostra como se retén unha porcentaxe do importe da factura dun provedor en función da porcentaxe que se completa dun proxecto.

Contoso Robotics USA contratou co vendedor Fabrikam para impartir 100 horas de adestramento para o proxecto de renovación de equipos. O valor total do contrato é 30 000 USD cun prezo de compra acordado de 300 USD por hora.

A formación impartirase en tres fases co seguinte programa:

- Fase 1: 50 horas ou 50 por cento do proxecto
- Fase 2: 30 horas ou 80 por cento do proxecto en total
- Fase 3: 20 horas ou 100 por cento do proxecto

A seguinte táboa indica as condicións da retención.

| **Porcentaxe de unidades entregadas** | **Porcentaxe a reter** | **Porcentaxe a liberar** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100 % | 0 % | 100 % |

As transaccións dan lugar ás seguintes cantidades:

- Fase 1:
  - A cantidade a pagar é de 50 x 300 ou 15 000.
  - O 20 por cento do importe, ou 3000, retense e liberarase nunha fase posterior.
  - A cantidade que se paga ao fornencedor é de 12 000.
- Fase 2:
  - A cantidade a pagar é de 30 x 300 ou 9 000.
  - Retense o 10 por cento da cantidade, ou 900.
  - Libérase o 10 por cento dos 3000 que se retiveron na fase 1, ou 300.
  - A cantidade que se paga ao fornencedor é de 8 400. Esta cantidade é de 9000 menos as retencións de 900 máis aos 300 liberados da retención da fase 1.
- Fase 3:
  - A cantidade a pagar é de 20 x 300 ou 6000.
  - Non se retén ningunha cantidade.
  - A cantidade que se libera é de 3600. Esta cantidade consiste nos 3000 que se retiveron na fase 1, menos os 300 da fase 1 que se liberaron na fase 2, máis os 900 que se retiveron na fase 2.
  - A cantidade que se paga ao fornencedor é de 9600. Este importe consiste na cantidade retida de 3600 máis os 6000 para completar a fase 3.

O importe total pagado ao fornecedor despois de completadas as tres fases é de 30 000, que é o importe total do pedido de compra (15000 + 9000 + 6000).
