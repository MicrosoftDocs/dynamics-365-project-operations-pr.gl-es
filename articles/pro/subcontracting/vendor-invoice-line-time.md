---
title: Liñas de factura de fornecedor para tempo
description: Este artigo explica como rexistrar as liñas de facturas de fornecedor para os custos de tempo que introducen os subcontratistas.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262010"
---
# <a name="vendor-invoice-lines-for-time"></a>Liñas de factura de fornecedor para tempo

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha factura de fornecedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de fornecedor para tempo. Os xestores de proxectos poden usar as liñas de factura de fornecedor para rexistrar os custos de tempo dos subcontratistas nos proxectos.

As liñas de factura de fornecedor para o tempo poden ou non facer referencia a unha liña de subcontrato para o tempo. Se unha liña de factura de fornecedor para o tempo fai referencia a un subcontrato, os xestores de proxectos poderán comparar e verificar o tempo que está a ser facturado pola liña de factura do fornecedor en función do tempo rexistrado polos subcontratistas e aprobado polos xestores de proxectos no proxecto.

A táboa seguinte fornece información acerca dos campos das liñas de factura do fornecedor para tempo.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome la liña da factura do fornecedor, para axudar na identificación. | Este nome amosarase como a primeira columna en todas as buscas baseadas en liñas de factura do fornecedor. |
| Descripción | Unha breve descrición dos servizos e produtos que vai facturar o fornecedor na liña de factura do fornecedor. | Nada |
| Subcontrato | O subcontrato no que se pediron orixinalmente os servizos. | Cando se selecciona un subcontrato para a factura do fornecedor, todas as liñas da factura do fornecedor herdarán esa selección. Unha factura de fornecedor non pode ter liñas de factura de fornecedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontrato | A liña de subcontratación no que se pediron os servizos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontrato nunha liña de factura de fornecedor para o tempo, os valores predeterminados para os campos **Proxecto**, **Rol** e **Recurso reservable** introdúcense desde os campos correspondentes na liña de subcontratación. Se a liña de subcontratación seleccionada ten valores nos campos **Proxecto**, **Rol** e **Reservable**, os valores dos campos correspondentes na liña de factura do fornecedor non poden diferir deses valores. |
| Data de transacción | A data na que se rexistrará no proxecto o dato real de custo da liña de factura do fornecedor. | Nada |
| Clase de transacción | O valor predefinido é **Tempo**. | O valor **Tempo** indica que se está a utilizar a liña de factura do fornecedor para rexistrar o importe da factura do tempo do subcontratista. |
| Project | O nome do proxecto no que se usaron os servizos que se van facturar. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto no que se usaron os servizos que se van facturar. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa de proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do fornecedor co tempo que rexistran os recursos do subcontratista en calquera tarefa do proxecto. Se a liña de factura do fornecedor non fai referencia a unha liña de subcontratación e este campo se deixa en branco, o dato real de custo que crea a liña de factura do fornecedor non se vinculará a ningún dato de vendas non facturado. Neste caso, se se configura a facturación baseada en tarefas, é posible que os custos non se poidan facturar ao cliente final. |
| Rol | O rol dos recursos de subcontrato cuxo tempo se está a facturar. | Este campo especifica o rol que desempeñan os recursos de subcontratación cuxo tempo se factura na factura do fornecedor. |
| Recurso reservable | O nome do subcontratista cuxo tempo se está a facturar. A selección dun recurso reservable é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do fornecedor co tempo que rexistra calquera recurso que pertenza ao fornecedor na liña de factura do fornecedor. |
| Cantidade | Introduza o número de horas de tempo que van facturar o fornecedor na liña de factura do fornecedor. |Nada |
| Grupo de unidades | O valor predefinido é **Grupo de unidades de tempo** e non se pode cambiar. | Nada |
| Unidade | O valor predefinido é a unidade base de horas do grupo de unidades de tempo. Pode cambiar este valor para mercar en calquera unidade do grupo de unidades de tempo, como o día ou a semana. | A combinación dos valores de **Rol** e **Unidade** usarase como valor predefinido ou computado para o campo **Prezo unitario** da liña de factura de fornecedor. |
| Prezo por unidade | O prezo unitario predefinido usa a combinación dos valores de **Rol** e **Unidade** da lista de prezos do proxecto que é aplicable para a data da transacción da liña de factura de fornecedor. | Se o prezo para a lista de prezos do proxecto aplicable está configurado nunha unidade diferente á unidade da liña de factura de fornecedor, o sistema utiliza a conversión unitaria para calcular o prezo por unidade. |
| Subtotal | Este campo de só lectura calcúlase como *Cantidade* &times; *Prezo unitario*, se os valores se introducen nos campos **Cantidade** e **Prezo unitario**. Se un ou ambos campos están en branco, pode introducir un valor neste campo. | Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Importe total | O importe total da liña de factura do fornecedor, incluídos os impostos. Este campo calcúlase como *Subtotal* + *Imposto sobre as vendas*. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
