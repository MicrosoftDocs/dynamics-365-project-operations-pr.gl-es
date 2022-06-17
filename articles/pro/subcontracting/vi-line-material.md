---
title: Liñas de factura de fornecedor para produtos
description: Este artigo explica como rexistrar liñas de factura de provedores para produtos e usar os diferentes campos para rexistrar as compras de produtos dos provedores.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931374"
---
# <a name="vendor-invoice-lines-for-products"></a>Liñas de factura de fornecedor para produtos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha factura de provedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de provedores para produtos (tamén denominados materiais). Os xestores de proxectos poden usar liñas de factura de provedores para produtos para rexistrar os custos dos produtos que foron adquiridos nos proxectos.

As liñas de facturas de provedores para produtos poden ou non facer referencia a unha liña de subcontrato para materiais. Se unha liña de facturas de provedores para produtos fai referencia a un subcontrato, os xestores de proxectos poderán comparar e verificar os produtos que están a ser facturados pola liña de facturas de provedores co uso de produtos comprados que son rexistrados e aprobados polos xestores de proxectos.

A seguinte táboa ofrece información sobre os campos das liñas de factura de provedores dos produtos.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da liña de factura do provedor, para axudar coa identificación. | Este nome mostrarase como a primeira columna en todas as buscas baseadas nas liñas de factura de provedores. |
| Descripción | Unha breve descrición dos produtos que está a ser facturado polo provedor na liña de factura do provedor. | Nada |
| Subcontrato | O subcontrato no que se encargaron orixinalmente os produtos. | Cando se selecciona un subcontrato para a factura do provedor, todas as liñas da factura do provedor herdarán esa selección. Unha factura de provedor non pode ter liñas de factura de provedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontratación | A liña de subcontratación na que se encargaron os produtos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontrato nunha liña de factura de provedor para produtos, os valores predeterminados para o **Proxecto**, **·**, e **Produto** os campos introdúcense desde os campos correspondentes na liña de subcontratación. Se a liña de subcontratación seleccionada ten valores no **Proxecto**, **·**, e **Produto** campos, os valores dos campos correspondentes na liña de factura do provedor non poden diferir deses valores. |
| Data de transacción | A data na que se rexistrará no proxecto o custo real da liña de factura do provedor. | Nada|
| Clase de transacción | Cando se facturan os produtos, este campo debe establecerse como **Material**. | O valor **Material** indica que se está a utilizar a liña de factura do provedor para rexistrar o importe da factura dos materiais que foron adquiridos. |
| Project | O nome do proxecto no que se utilizaron os produtos que se están facturando. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto na que se utilizaron os produtos que se están facturando. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa do proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do provedor co produto comprado que se utiliza en calquera tarefa do proxecto. Se a liña de factura do provedor non fai referencia a unha liña de subcontrato e este campo se deixa en branco, o custo real que crea a liña de factura do provedor non se vinculará a ningún reais de vendas non facturados. Neste caso, se se configura a facturación baseada en tarefas, os custos non se poderán facturar ao cliente final. |
| Seleccionar produto | Seleccione se o produto que se está a facturar é un produto existente do catálogo ou un produto inscrito. | O valor predeterminado introdúcese desde a liña de subcontrato cando se selecciona unha liña de subcontrato. |
| Produto | Seleccione o produto do catálogo. Se o produto é un produto escrito, introduza o nome do produto. | Este campo úsase para introducir os prezos de compra predeterminados dos produtos existentes. |
| Cantidade | Introduza a cantidade de material que está a ser facturado polo provedor nesta liña de factura. | Nada |
| Grupo de unidades | Seleccione o grupo de unidades da unidade no que se expresa a cantidade que se está a facturar. | Nada |
| Unidade | O valor predeterminado é a unidade base do grupo de unidades seleccionado. Podes cambiar este valor para pagar en calquera unidade do grupo de unidades seleccionado. | A combinación de **Produto** e **Unidade** os valores empregaranse como valor predeterminado ou calculado para o **Prezo por unidade** campo na liña da factura do provedor. |
| Prezo por unidade | O prezo unitario predeterminado utiliza a combinación de **Produto** e **Unidade** valores da lista de prezos do proxecto aplicables á data de transacción da liña de factura do provedor. | Nada |
| Subtotal | Este campo de só lectura calcúlase como *Cantidade*&times;*Prezo por unidade*, se se introducen valores en ambos **Cantidade** campo e o **Prezo por unidade** campo. Se un ou os dous campos están en branco, pode introducir un valor neste campo. | Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Cantidade total | O importe total da liña de factura do provedor, incluídos os impostos. Este campo calcúlase como *Subtotal* + *Imposto sobre vendas*. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
