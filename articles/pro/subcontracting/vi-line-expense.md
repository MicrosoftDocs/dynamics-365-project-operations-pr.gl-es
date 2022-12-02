---
title: Liñas de factura de fornecedor para categorías de gasto
description: Este artigo explica como rexistrar liñas de factura de fornecedor para categorías de gastos.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261680"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Liñas de factura de fornecedor para categorías de gasto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha factura de fornecedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de fornecedor para categorías de gasto. Os xestores de proxectos poden usar liñas de factura de fornecedor para categorías de gastos para rexistrar os custos dos servizos que se adquiren como categorías de gastos.

As liñas de factura de fornecedor para categorías de gasto poden ou non facer referencia a unha liña de subcontrato para as categorías de gasto. Se unha liña de factura de fornecedor para categorías de gasto fai referencia a un subcontrato, os xestores de proxectos poderán comparar e verificar os gastos que están a ser facturados pola liña de factura do fornecedor en función dos gastos rexistrados nestas categorías de gasto e aprobados polos xestores de proxectos no proxecto.

A táboa seguinte fornece información acerca dos campos das liñas de factura do fornecedor para categorías de gasto.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome la liña da factura do fornecedor, para axudar na identificación. | Este nome amosarase como a primeira columna en todas as buscas baseadas en liñas de factura do fornecedor. |
| Descripción | Unha breve descrición dos servizos e produtos que vai facturar o fornecedor na liña de factura do fornecedor. | Nada |
| Subcontrato | O subcontrato no que se pediron orixinalmente os servizos. | Cando se selecciona un subcontrato para a factura do fornecedor, todas as liñas da factura do fornecedor herdarán esa selección. Unha factura de fornecedor non pode ter liñas de factura de fornecedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontratación | A liña de subcontratación no que se pediron os servizos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontrato nunha liña de factura de fornecedor para categorías de gasto, os valores predeterminados para os campos **Proxecto**, **Tarefa** e **Categoría de transacción** introdúcense desde os campos correspondentes na liña de subcontratación. Se a liña de subcontratación seleccionada ten valores nos campos **Proxecto**, **Tarefa de proxecto** e **Categoría de transacción**, os valores dos campos correspondentes na liña de factura do fornecedor non poden diferir deses valores. |
| Data de transacción | A data na que se rexistrará no proxecto o dato real de custo da liña de factura do fornecedor. |Nada |
| Clase de transacción | Seleccione **Gasto** para rexistrar unha factura de fornecedor para unha categoría de gasto. | O valor **Gasto** indica que se está a utilizar a liña de factura do fornecedor para rexistrar o importe da factura dos servizos que foron adquiridos como categorías de gasto. |
| Project | O nome do proxecto no que se usaron os servizos que se van facturar. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto no que se usaron os servizos que se van facturar. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa de proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do fornecedor cos gastos que están rexistrados en calquera tarefa do proxecto. Se a liña de factura do fornecedor non fai referencia a unha liña de subcontratación e este campo se deixa en branco, o dato real de custo que crea a liña de factura do fornecedor non se vinculará a ningún dato de vendas non facturado. Neste caso, se se configura a facturación baseada en tarefas, é posible que os custos non se poidan facturar ao cliente final. |
| Categoría da transacción | A categoría de transacción que se está a facturar. Debe crearse unha categoría de gasto correspondente para a categoría de transacción seleccionada. | A combinación dos valores de **Categoría de transacción** e **Unidade** usarase como valor predefinido ou computado para o campo **Prezo unitario** da liña de factura de fornecedor. |
| Cantidade | Introduza a cantidade que está a ser facturada polo fornecedor na liña de factura. |Nada|
| Grupo de unidades | Introdúcese un valor predefinido en función do grupo de unidades predefinido configurado para a categoría de transacción seleccionada. | Nada |
| Unidade | O valor predefinido é a unidade base do grupo de unidades que está seleccionado. Pode cambiar este valor para mercar calquera unidade do grupo de unidades. | A combinación dos valores de **Categoría de transacción** e **Unidade** usarase como valor predefinido ou computado para o campo **Prezo unitario** da liña de factura de fornecedor. |
| Prezo por unidade | O prezo unitario predefinido usa a combinación dos valores de **Categoría de transacción** e **Unidade** da lista de prezos do proxecto que é aplicable para a data da transacción da liña de factura de fornecedor. | Se o prezo para a lista de prezos do proxecto aplicable está configurado nunha unidade diferente á unidade da liña de factura de fornecedor, o sistema utiliza a conversión unitaria para calcular o prezo por unidade. |
| Subtotal | Este campo de só lectura calcúlase como *Cantidade* &times; *Prezo unitario*, se os valores se introducen nos campos **Cantidade** e **Prezo unitario**. Se un ou ambos campos están en branco, pode introducir un valor neste campo.| Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Importe total | O importe total da liña de factura do fornecedor, incluídos os impostos. Este campo calcúlase como *Subtotal* + *Imposto sobre as vendas*. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
