---
title: Liñas de factura de fornecedor para produtos
description: Este artigo explica como rexistrar liñas de factura do fornecedor para produtos e usar os diferentes campos para rexistrar compras de produtos de fornecedores.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261556"
---
# <a name="vendor-invoice-lines-for-products"></a>Liñas de factura de fornecedor para produtos

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha factura de fornecedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de fornecedor para produtos (tamén denominados materiais). Os xestores de proxectos poden usar as liñas de factura de fornecedor para produtos para rexistrar os custos dos produtos que se compraron nos proxectos.

As liñas de factura de fornecedor para produtos poden ou non facer referencia a unha liña de subcontrato para materiais. Se unha liña de factura de fornecedor para produtos fai referencia a un subcontrato, os xestores de proxectos poderán comparar e verificar os produtos que están a ser facturados pola liña de factura do fornecedor en función uso dos produtos comprados rexistrados e aprobados polos xestores de proxectos.

A táboa seguinte fornece información acerca dos campos das liñas de factura do fornecedor para produtos.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome la liña da factura do fornecedor, para axudar na identificación. | Este nome amosarase como a primeira columna en todas as buscas baseadas en liñas de factura do fornecedor. |
| Descripción | Unha breve descrición dos produtos que vai facturar o fornecedor na liña de factura do fornecedor. | Nada |
| Subcontrato | O subcontrato no que se pediron orixinalmente os produtos. | Cando se selecciona un subcontrato para a factura do fornecedor, todas as liñas da factura do fornecedor herdarán esa selección. Unha factura de fornecedor non pode ter liñas de factura de fornecedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontratación | A liña de subcontrato no que se pediron os produtos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontrato nunha liña de factura de fornecedor para produtos, os valores predeterminados para os campos **Proxecto**, **Tarefa** e **Produto** introdúcense desde os campos correspondentes na liña de subcontratación. Se a liña de subcontratación seleccionada ten valores nos campos **Proxecto**, **Tarefa** e **Produto**, os valores dos campos correspondentes na liña de factura do fornecedor non poden diferir deses valores. |
| Data de transacción | A data na que se rexistrará no proxecto o dato real de custo da liña de factura do fornecedor. | Nada|
| Clase de transacción | Cando se facturan os produtos, este campo debe establecerse como **Material**. | O valor **Material** indica que se está a utilizar a liña de factura do fornecedor para rexistrar o importe da factura dos materiais que foron adquiridos. |
| Project | O nome do proxecto no que se usaron os produtos que se van facturar. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto no que se usaron os produtos que se van facturar. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa de proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do fornecedor cos produtos comprados que se utilizan en calquera tarefa do proxecto. Se a liña de factura do fornecedor non fai referencia a unha liña de subcontratación e este campo se deixa en branco, o dato real de custo que crea a liña de factura do fornecedor non se vinculará a ningún dato de vendas non facturado. Neste caso, se se configura a facturación baseada en tarefas, os custos non se poderán facturar ao cliente final. |
| Seleccionar produto | Seleccione se o produto que se vai facturar existe no catálogo ou se é un produto fóra de catálogo. | O valor predeterminado introdúcese desde a liña de subcontratación cando se selecciona unha liña de subcontratación. |
| Produto | Seleccione o produto do catálogo. Se o produto é un produto fóra de catálogo, introduza o nome do produto. | Este campo úsase para introducir os prezos de compra predefinidos dos produtos existentes. |
| Cantidade | Introduza a cantidade de material que está a ser facturada polo fornecedor nesta liña de factura. | Nada |
| Grupo de unidades | Seleccione o grupo de unidades da unidade na que se expresa a cantidade que se está a facturar. | Nada |
| Unidade | O valor predefinido é a unidade base do grupo de unidades que está seleccionado. Pode cambiar este valor para pagar en calquera unidade do grupo de unidades seleccionado. | A combinación dos valores de **Produto** e **Unidade** usarase como valor predefinido ou computado para o campo **Prezo unitario** da liña de factura de fornecedor. |
| Prezo por unidade | O prezo unitario predefinido usa a combinación dos valores de **Produto** e **Unidade** da lista de prezos do proxecto que é aplicable para a data da transacción da liña de factura de fornecedor. | Nada |
| Subtotal | Este campo de só lectura calcúlase como *Cantidade* &times; *Prezo unitario*, se os valores se introducen nos campos **Cantidade** e **Prezo unitario**. Se un ou ambos campos están en branco, pode introducir un valor neste campo. | Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Importe total | O importe total da liña de factura do fornecedor, incluídos os impostos. Este campo calcúlase como *Subtotal* + *Imposto sobre as vendas*. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
