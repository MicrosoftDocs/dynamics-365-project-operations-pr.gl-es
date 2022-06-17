---
title: Liñas de factura de fornecedor para categorías de gasto
description: Este artigo explica como rexistrar liñas de facturas de provedores para categorías de gastos.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925874"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Liñas de factura de fornecedor para categorías de gasto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha factura de provedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de provedores para categorías de gastos. Os xestores de proxectos poden usar liñas de factura de provedores para categorías de gastos para rexistrar os custos dos servizos que se adquiren como categorías de gastos.

As liñas de factura de provedores para categorías de gastos poden facer referencia ou non a unha liña de subcontrato para categorías de gastos. Se unha liña de factura de provedor para categorías de gastos fai referencia a un subcontrato, os xestores de proxectos poderán comparar e verificar os gastos que están a ser facturados pola liña de facturas de provedores cos gastos rexistrados nestas categorías de gastos e aprobados polos xestores de proxecto no proxecto.

A seguinte táboa ofrece información sobre os campos das liñas de factura de provedores para as categorías de gastos.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da liña de factura do provedor, para axudar coa identificación. | Este nome mostrarase como a primeira columna en todas as buscas baseadas nas liñas de factura de provedores. |
| Descripción | Unha breve descrición dos servizos que está a ser facturado polo provedor na liña de factura do provedor. | Nada |
| Subcontrato | O subcontrato polo que se encargaron orixinalmente os servizos. | Cando se selecciona un subcontrato para a factura do provedor, todas as liñas da factura do provedor herdarán esa selección. Unha factura de provedor non pode ter liñas de factura de provedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontratación | A liña de subcontratación na que se encargaron os servizos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontrato nunha liña de factura de provedor para categorías de gastos, os valores predeterminados para o **Proxecto**, **·**, e **Categoría de transacción** os campos introdúcense desde os campos correspondentes na liña de subcontratación. Se a liña de subcontratación seleccionada ten valores no **Proxecto**, **do proxecto**, e **Categoría de transacción** campos, os valores dos campos correspondentes na liña de factura do provedor non poden diferir deses valores. |
| Data de transacción | A data na que se rexistrará no proxecto o custo real da liña de factura do provedor. |Nada |
| Clase de transacción | Seleccione **Gasto** para rexistrar unha factura de provedor para unha categoría de gasto. | O valor **Gasto** indica que se está a utilizar a liña de factura do provedor para rexistrar o importe da factura dos servizos que foron adquiridos como categorías de gasto. |
| Project | O nome do proxecto no que se utilizaron os servizos que se están facturando. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto na que se utilizaron os servizos que se están facturando. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa do proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do provedor cos gastos que se rexistran en calquera tarefa do proxecto. Se a liña de factura do provedor non fai referencia a unha liña de subcontrato e este campo se deixa en branco, o custo real que crea a liña de factura do provedor non se vinculará a ningún reais de vendas non facturados. Neste caso, se se configura a facturación baseada en tarefas, é posible que os custos non se poidan facturar ao cliente final. |
| Categoría da transacción | A categoría de transacción que se está a facturar. Debe crearse unha categoría de gasto correspondente para a categoría de transacción seleccionada. | A combinación de **Categoría de transacción** e **Unidade** os valores empregaranse como valor predeterminado ou calculado para o **Prezo por unidade** campo na liña da factura do provedor. |
| Cantidade | Introduza a cantidade que está a ser facturada polo provedor na liña de factura. |Nada|
| Grupo de unidades | Introdúcese un valor predeterminado en función do grupo de unidades da categoría de transacción seleccionada. | Nada |
| Unidade | O valor predeterminado é a unidade base do grupo de unidades seleccionado. Podes cambiar este valor para mercar en calquera unidade do grupo de unidades. | A combinación de **Categoría de transacción** e **Unidade** os valores empregaranse como valor predeterminado ou calculado para o **Prezo por unidade** campo na liña da factura do provedor. |
| Prezo por unidade | O prezo unitario predeterminado utiliza a combinación de **Categoría de transacción** e **Unidade** valores da lista de prezos do proxecto aplicables á data de transacción da liña de factura do provedor. | Se o prezo para a lista de prezos do proxecto aplicable está configurado nunha unidade que é diferente da unidade da liña de factura do provedor, o sistema utiliza a conversión de unidade para calcular o prezo por unidade. |
| Subtotal | Este campo de só lectura calcúlase como *Cantidade*&times;*Prezo por unidade*, se se introducen valores en ambos **Cantidade** campo e o **Prezo por unidade** campo. Se un ou os dous campos están en branco, pode introducir un valor neste campo.| Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Cantidade total | O importe total da liña de factura do provedor, incluídos os impostos. Este campo calcúlase como *Subtotal* + *Imposto sobre vendas*. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
