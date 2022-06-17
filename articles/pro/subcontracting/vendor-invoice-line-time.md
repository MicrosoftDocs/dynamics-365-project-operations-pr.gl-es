---
title: Liñas de factura de fornecedor para tempo
description: Este artigo explica como rexistrar as liñas de facturas de provedores para os custos de tempo que realizan os subcontratistas.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927540"
---
# <a name="vendor-invoice-lines-for-time"></a>Liñas de factura de fornecedor para tempo

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha factura de provedor en Microsoft Dynamics 365 Project Operations pode ter liñas de factura de provedores por tempo. Os xestores de proxectos poden usar as liñas de factura de provedores para rexistrar os custos do tempo dos subcontratistas nos proxectos.

As liñas de factura de provedores para o tempo poden ou non facer referencia a unha liña de subcontrato para o tempo. Se unha liña de factura de provedor para o tempo fai referencia a un subcontrato, os xestores do proxecto poderán comparar e verificar o tempo que está a ser facturado pola liña de factura do provedor en función do tempo rexistrado polos subcontratistas e aprobado polos xestores do proxecto no proxecto.

A seguinte táboa ofrece información sobre os campos das liñas de factura de provedores para o tempo.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da liña de factura do provedor, para axudar coa identificación. | Este nome mostrarase como a primeira columna en todas as buscas baseadas nas liñas de factura de provedores. |
| Descripción | Unha breve descrición dos servizos que está a ser facturado polo provedor na liña de factura do provedor. | Nada |
| Subcontrato | O subcontrato polo que se encargaron orixinalmente os servizos. | Cando se selecciona un subcontrato para a factura do provedor, todas as liñas da factura do provedor herdarán esa selección. Unha factura de provedor non pode ter liñas de factura de provedor que fagan referencia a diferentes subcontratos. |
| Liña de subcontratación | A liña de subcontratación na que se encargaron os servizos. A lista de liñas de subcontratación que se poden seleccionar está limitada ás liñas do subcontrato seleccionado. | Cando se selecciona unha liña de subcontrato nunha liña de factura de provedor para o tempo, os valores predeterminados para o **Proxecto**, **·**, e **Recurso reservable** os campos introdúcense desde os campos correspondentes na liña de subcontratación. Se a liña de subcontratación seleccionada ten valores no **Proxecto**, **·**, e **Reservable** campos, os valores dos campos correspondentes na liña de factura do provedor non poden diferir deses valores. |
| Data de transacción | A data na que se rexistrará no proxecto o custo real da liña de factura do provedor. | Nada |
| Clase de transacción | O valor predefinido é **Tempo**. | O valor **Tempo** indica que se está a utilizar a liña de factura do provedor para rexistrar o importe da factura do tempo do subcontratista. |
| Project | O nome do proxecto no que se utilizaron os servizos que se están facturando. | Este campo é obrigatorio e non se pode deixar en branco. |
| Tarefa | O nome da tarefa do proxecto na que se utilizaron os servizos que se están facturando. Este campo só está dispoñible se se selecciona un proxecto. A selección dunha tarefa do proxecto é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do provedor co tempo que rexistran os recursos do subcontratista en calquera tarefa do proxecto. Se a liña de factura do provedor non fai referencia a unha liña de subcontrato e este campo se deixa en branco, o custo real que crea a liña de factura do provedor non se vinculará a ningún reais de vendas non facturados. Neste caso, se se configura a facturación baseada en tarefas, é posible que os custos non se poidan facturar ao cliente final. |
| Rol | O papel dos recursos de subcontratación cuxo tempo se está a facturar. | Este campo especifica a función que desempeñan os recursos de subcontratación cuxo tempo se factura na factura do provedor. |
| Recurso reservable | O nome do subcontratista cuxo tempo se está a facturar. A selección dun recurso reservable é opcional. | Se este campo se deixa en branco, o xestor do proxecto pode relacionar a liña de factura do provedor coa hora que rexistra calquera recurso que pertenza ao provedor na liña de factura do provedor. |
| Cantidade | Introduza o número de horas de tempo que está a ser facturado polo provedor na liña de factura. |Nada |
| Grupo de unidades | O valor predeterminado é **Grupo de unidades de tempo** e non se pode cambiar. | Nada |
| Unidade | O valor predeterminado é a unidade base de horas do grupo de unidades de tempo. Podes cambiar este valor para mercar en calquera unidade do grupo de unidades de tempo, como o día ou a semana. | A combinación de **Papel** e **Unidade** os valores empregaranse como valor predeterminado ou calculado para o **Prezo por unidade** campo na liña da factura do provedor. |
| Prezo por unidade | O prezo unitario predeterminado utiliza a combinación de **Papel** e **Unidade** valores da lista de prezos do proxecto aplicables á data de transacción da liña de factura do provedor. | Se o prezo para a lista de prezos do proxecto aplicable está configurado nunha unidade que é diferente da unidade da liña de factura do provedor, o sistema utiliza a conversión de unidade para calcular o prezo por unidade. |
| Subtotal | Este campo de só lectura calcúlase como *Cantidade*&times;*Prezo por unidade*, se se introducen valores en ambos **Cantidade** campo e o **Prezo por unidade** campo. Se un ou os dous campos están en branco, pode introducir un valor neste campo. | Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. | Nada |
| Cantidade total | O importe total da liña de factura do provedor, incluídos os impostos. Este campo calcúlase como *Subtotal* + *Imposto sobre vendas*. | Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
