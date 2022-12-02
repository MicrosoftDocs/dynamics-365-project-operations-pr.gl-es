---
title: Detalles da cabeceira para facturas de fornecedores
description: Este artigo explica a funcionalidade que se proporciona na cabeceira da factura do fornecedor en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261651"
---
# <a name="header-details-for-vendor-invoices"></a>Detalles da cabeceira para facturas de fornecedores

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo explica a funcionalidade que se proporciona na cabeceira da factura do fornecedor en Microsoft Dynamics 365 Project Operations.

Cando un xestor de proxectos planifica e executa proxectos, podería empregar subcontratistas e mercar produtos e servizos a fornecedores. Durante a execución dun proxecto, os custos incórrense en servizos, materiais e categorías de gastos que se adquiren mediante subcontratos con fornecedores. Os fornecedores facturan estes custos aos proxectos creando facturas de provedores.

A seguinte táboa ofrece información sobre os campos nas cabeceiras de factura de fornecedor en Project Operations.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da factura do fornecedor. | En todas as listas despregables de facturas de fornecedor, o nome da factura do fornecedor aparece na primeira columna para axudarlle a identificar a factura do fornecedor. Por defecto, cando se crea unha factura de fornecedor a partir dun subcontrato, o campo **Nome** da factura do fornecedor establécese nun valor que consiste no nome do subcontrato máis a data actual. |
| Descripción | Unha breve descrición dos servizos e produtos que se van facturar na factura do fornecedor. | Nada |
| Fornecedor | O nome da empresa á que se van facturar os produtos e servizos. Esta empresa debe ser un rexistro de conta ten un tipo de relación de **Fornecedor** ou **Provedor**. | <p>En función do fornecedor seleccionado, os valores predefinidos introdúcense automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de prezos</li><li>Condicións de pagamento</li><li>Enderezo de pagamento</li></ul> |
| Subcontrato | Unha referencia ao subcontrato para a factura do fornecedor. | <p>En función do subcontrato seleccionado, os valores predefinidos introdúcense automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de prezos</li><li>Condicións de pagamento</li><li>Enderezo de pagamento</li></ul><p>O subcontrato que se selecciona na cabeceira da factura do fornecedor introdúcese de forma predeterminada nas liñas da factura do fornecedor e non se pode cambiar alí.</p> |
| Data da factura | A data dos datos reais de custos que se crearán cando se confirme a factura do fornecedor. | A data da factura úsase tamén para seleccionar a lista de prezos de compra correcta entre as listas de prezos que se xuntan ao fornecedor relacionado ou entre os parámetros do proxecto. |
| Motivo para o estado | O estado da factura do fornecedor | <p>O estado determina onde se atopa a factura do fornecedor no proceso comercial e se se pode editar. Estes son algúns dos valores dispoñibles:</p><ul><li>**Borrador** – A factura do fornecedor pódese editar.</li><li>**Confirmada** – Verificouse e confirmouse a factura do fornecedor. As facturas de fornecedor neste estado non se poden editar nin eliminar.</li><li>**En proceso** – A factura do fornecedor está a revisarse. As facturas de fornecedor neste estado pódense editar, pero non se poden eliminar.</li><li>**Cancelada** – Cancelouse a factura do fornecedor. As facturas de fornecedor neste estado non se poden editar nin eliminar.</li></ul> |
| Moeda | Moeda na que está a facturar o fornecedor dos produtos e servizos da factura do fornecedor. | Nunha factura do fornecedor que fai referencia a un subcontrato, a moeda do subcontrato introdúcese de forma predeterminada como a moeda da factura do fornecedor. Nunha factura do fornecedor que non fai referencia a un subcontrato, o valor predeterminado introdúcese desde o rexistro da conta do fornecedor e pódese cambiar. Despois de gardar unha factura de fornecedor, a moeda xa non se pode editar. |
| Unidade de contratación | A división da empresa que se encarga de recibir os servizos e/ou produtos do fornecedor. | Nada |
| Condicións de pagamento | As condicións de pagamento das facturas do fornecedor que se emiten. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | As condicións de pagamento do subcontrato cópianse en todas as facturas do fornecedor relacionadas co subcontrato. As condicións de pagamento pódense actualizar se a factura do fornecedor ten un estado de **Borrador**. |
| Enderezo de pagamento | O enderezo do fornecedor ao que se deben enviar os pagamentos. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | O enderezo de pagamento dun subcontrato cópiase como o enderezo de pagamento a todas as facturas do fornecedor que se crean para ese subcontrato. O enderezo de pagamento pódese actualizar se a factura do fornecedor ten un estado de **Borrador**. |
| Subtotal | Se a factura do fornecedor non ten liñas, introduza o subtotal da factura antes de impostos. Se a factura do fornecedor ten liñas, este campo só será de lectura. Neste caso, a cantidade que se mostra é a cantidade subtotal de todas as liñas da factura do fornecedor. | Nada |
| Imposto total | Se a factura do fornecedor non ten liñas, introduza os impostos totais do subcontrato. Se a factura do fornecedor ten liñas, este campo só será de lectura. Neste caso, a cantidade que se mostra é a suma das cantidades de impostos de todas as liñas da factura do fornecedor. | Nada |
| Importe total | Este campo calculado mostra o importe total da factura do fornecedor despois de incluír os impostos. | Nada |

> [!NOTE]
> Os seguintes campos dunha factura de fornecedor non se poden cambiar despois de gardar a factura de fornecedor: **Fornecedor**, **Subcontrato**, **Moeda**, **Unidade de contratación**, e **Condicións de pagamento**. Se é necesario realizar algún cambio nestes campos nunha factura de fornecedor, debe eliminar a factura de fornecedor e crear unha nova factura de fornecedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
