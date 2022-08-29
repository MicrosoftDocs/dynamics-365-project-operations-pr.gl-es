---
title: Liñas de factura de fornecedor para fitos
description: Este artigo explica como crear liñas de factura de provedores para fitos nun subcontrato.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9260993"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Liñas de factura de fornecedor para fitos

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha factura de provedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de provedores para fitos que se definen nunha liña de subcontrato. Os xestores de proxectos poden usar liñas de facturas de provedores para fitos para rexistrar os custos dos servizos que se adquiren como custos baseados en fitos que se incorren nos servizos ou produtos que se adquiren para o proxecto.

As liñas de factura de provedores para fitos sempre deben facer referencia a unha liña de subcontrato que teña un método de facturación de prezo fixo. Cando unha liña de factura de provedor para fitos fai referencia a unha liña de subcontrato, os xestores de proxecto poderán comparar e verificar os custos subxacentes de tempo, gastos ou materiais que fan referencia a esa liña de subcontrato co fito que está a ser facturado polo provedor.

A seguinte táboa ofrece información sobre os campos das liñas de factura de provedores para os fitos.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da liña de factura do provedor, para axudar coa identificación. | Este nome mostrarase como a primeira columna en todas as buscas baseadas nas liñas de factura de provedores. |
| Descripción | Unha breve descrición dos servizos que está a ser facturado polo provedor na liña de factura do provedor. | Nada |
| Subcontrato | O subcontrato polo que se encargaron orixinalmente os servizos. | Cando se selecciona un subcontrato para a factura do provedor, todas as liñas da factura do provedor herdarán esa selección. Unha factura de provedor non pode ter liñas de factura de provedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontratación | A liña de subcontratación na que se encargaron os servizos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontrato nunha liña de factura de provedor para os fitos, o **Papel** e **Categoría de transacción** campos e campos relacionados co produto, son irrelevantes e non están dispoñibles. O **Cantidade**, **·**, e **Grupo de unidades** Os campos tampouco son relevantes para as liñas de facturas de provedores baseadas en fitos. |
| Data de transacción | A data na que se rexistrará no proxecto o custo real da liña de factura do provedor. | Nada |
| Clase de transacción | Seleccione **Fito** para rexistrar unha factura de provedor para un fito completado que se definiu nunha liña de subcontrato. | Nada |
| Fito | Seleccione o fito que se define na liña de subcontratación relacionada que está marcada como **Listo para facturar**. | Fitos da liña de subcontratación que teñen un estado de **Listo para facturar** pódese seleccionar nunha liña de factura de provedor. |
| Project | O nome do proxecto no que se utilizaron os servizos que se están facturando. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto na que se utilizaron os servizos que se están facturando. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa do proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do provedor coa clase de transaccións da liña de subcontratación relacionada que se rexistra en calquera tarefa do proxecto. Se a liña de factura do provedor non fai referencia a unha liña de subcontrato e este campo se deixa en branco, o custo real que crea a liña de factura do provedor non se vinculará a ningún dato de vendas non facturado. Neste caso, se se configura a facturación baseada en tarefas, é posible que non se poidan facturar os custos ao cliente final. |
| Cantidade do fito | Introduza o valor do fito que se define na liña de subcontrato que está lista para ser facturada. | Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Cantidade total | O importe total da liña de factura do provedor, incluídos os impostos. Este campo calcúlase como *Importe do fito* + *Imposto sobre vendas*. | Nada |

> [!NOTE]
> Cando se crea unha liña de factura de provedor que fai referencia a un hito da liña de subcontrato, o estado do fito de subcontrato actualízase a **Creouse a factura do provedor**. Despois, cando se confirma esa factura do provedor, actualízase o estado do fito da liña de subcontrato **Factura do provedor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
