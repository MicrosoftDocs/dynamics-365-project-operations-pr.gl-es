---
title: Liñas de factura de fornecedor para fitos
description: Este artigo explica como crear liñas de factura de fornecedor para fitos nun subcontrato.
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

Unha factura de fornecedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de fornecedor para fitos que se definen nunha liña de subcontrato. Os xestores de proxectos poden usar liñas de facturas de fornecedor para fitos para rexistrar os custos dos servizos que se adquiren como custos baseados en fitos que se incorren nos servizos ou produtos que se adquiren para o proxecto.

As liñas de factura de fornecedor para fitos sempre deben facer referencia a unha liña de subcontrato que teña un método de facturación de prezo fixo. Cando unha liña de factura de fornecedor para fitos fai referencia a unha liña de subcontrato, os xestores de proxectos poderán comparar e verificar os custos subxacentes de tempo, gastos ou materiais que fan referencia a esa liña de subcontratación contra o fito que está a ser facturado polo fornecedor.

A táboa seguinte fornece información acerca dos campos das liñas de factura do fornecedor para fitos.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome la liña da factura do fornecedor, para axudar na identificación. | Este nome amosarase como a primeira columna en todas as buscas baseadas en liñas de factura do fornecedor. |
| Descripción | Unha breve descrición dos servizos e produtos que vai facturar o fornecedor na liña de factura do fornecedor. | Nada |
| Subcontrato | O subcontrato no que se pediron orixinalmente os servizos. | Cando se selecciona un subcontrato para a factura do fornecedor, todas as liñas da factura do fornecedor herdarán esa selección. Unha factura de fornecedor non pode ter liñas de factura de fornecedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontratación | A liña de subcontratación no que se pediron os servizos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontratación nunha liña de factura de fornecedor para os fitos, os campos **Rol** e **Categoría de transacción** e os campos relacionados co produto, son irrelevantes e non están dispoñibles. Os campos **Cantidade**, **Unidade** e **Grupo de unidades** tampouco son relevantes para as liñas de facturas de fornecedor baseadas en fitos. |
| Data de transacción | A data na que se rexistrará no proxecto o dato real de custo da liña de factura do fornecedor. | Nada |
| Clase de transacción | Seleccione **Fito** para rexistrar unha factura de fornecedor para un fito completado que se definiu nunha liña de subcontratación. | Nada |
| Fito | Seleccione o fito que se define na liña de subcontratación relacionada que está marcada como **Listo para facturar**. | Os fitos de liña de subcontratación que teñen un estado de **Listo para facturar** se poden seleccionar nunha liña de factura de fornecedor. |
| Project | O nome do proxecto no que se usaron os servizos que se van facturar. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto no que se usaron os servizos que se van facturar. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa de proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do fornecedor coa clase de transaccións da liña de subcontratación seleccionada que está rexistrada en calquera tarefa do proxecto. Se a liña de factura do fornecedor non fai referencia a unha liña de subcontratación e este campo se deixa en branco, o dato real de custo que crea a liña de factura do fornecedor non se vinculará a ningún dato de vendas non facturado. Neste caso, se se configura a facturación baseada en tarefas, é posible que os custos non se poidan facturar ao cliente final. |
| Cantidade do fito | Introduza o valor do fito que se define na liña de subcontratación que está lista para facturar | Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Importe total | O importe total da liña de factura do fornecedor, incluídos os impostos. Este campo calcúlase cono *Importe de fito* + *Imposto sobre as vendas*. | Nada |

> [!NOTE]
> Cando se crea unha liña de factura de fornecedor que fai referencia a un fito da liña de subcontratación, o estado do fito de subcontrato actualízase a **Creouse a factura do fornecedor**. Despois, cando se confirma esa factura do fornecedor, actualízase o estado do fito da liña de subcontratación a **Factura do fornecedor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
