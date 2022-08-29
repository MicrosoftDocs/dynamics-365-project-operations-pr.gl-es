---
title: Detalles da cabeceira para facturas de fornecedores
description: Este artigo explica a funcionalidade que se proporciona na cabeceira da factura do provedor en Microsoft Dynamics 365 Project Operations.
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

Este artigo explica a funcionalidade que se proporciona na cabeceira da factura do provedor en Microsoft Dynamics 365 Project Operations.

A medida que os xestores de proxectos planifican e executan proxectos, poden contratar subcontratistas e comprar produtos e servizos a provedores. Durante a execución dun proxecto, os custos incorren en servizos, materiais e categorías de gastos que se adquiren mediante subcontratos con provedores. Os provedores facturan estes custos aos proxectos creando facturas de provedores.

A seguinte táboa ofrece información sobre os campos das cabeceiras das facturas de provedores en Operacións do proxecto.

| Campo | Descripción | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da factura do provedor. | En todas as listas despregábeis de facturas de provedores, o nome da factura de provedores aparece na primeira columna para axudarche a identificar a factura de provedores. Por defecto, cando se crea unha factura de provedor a partir dun subcontrato, o **Nome** campo da factura do provedor establécese nun valor que consiste no nome do subcontrato máis a data actual. |
| Descripción | Unha breve descrición dos servizos e produtos que se están facturando na factura do provedor. | Nada |
| Fornecedor | O nome da empresa que está a facturar os produtos e servizos. Esta empresa debe ser un rexistro de conta que teña un tipo de relación **Vendedor** ou **Provedor**. | <p>En función do provedor seleccionado, os valores predeterminados introdúcense automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de prezos</li><li>Condicións de pagamento</li><li>Enderezo de pago</li></ul> |
| Subcontrato | Unha referencia ao subcontrato para a factura do provedor. | <p>En función do subcontrato seleccionado, os valores predeterminados introdúcense automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de prezos</li><li>Condicións de pagamento</li><li>Enderezo de pago</li></ul><p>O subcontrato que se selecciona na cabeceira da factura do provedor introdúcese de forma predeterminada nas liñas da factura do provedor e non se pode cambiar alí.</p> |
| Datos da factura | A data dos custos reais que se crearán cando se confirme a factura do provedor. | A data da factura tamén se usa para seleccionar a lista de prezos de compra correcta das listas de prezos anexas ao provedor relacionado ou dos parámetros do proxecto. |
| Motivo para o estado | O estado da factura do provedor. | <p>O estado determina onde está a factura do provedor no proceso comercial e se se pode editar. Estes son algúns dos valores dispoñibles:</p><ul><li>**Borrador** – A factura do provedor pódese editar.</li><li>**Confirmado** – Verificouse e confirmouse a factura do provedor. As facturas de provedores neste estado non se poden editar nin eliminar.</li><li>**En proceso** – Está a revisar a factura do provedor. As facturas de provedores neste estado pódense editar, pero non se poden eliminar.</li><li>**Cancelado** – Cancelouse a factura do provedor. As facturas de provedores neste estado non se poden editar nin eliminar.</li></ul> |
| Moeda | Moeda na que está a facturar o provedor dos produtos e servizos da factura do provedor. | Nunha factura do provedor que fai referencia a un subcontrato, a moeda do subcontrato introdúcese de forma predeterminada como a moeda da factura do provedor. Nunha factura do provedor que non fai referencia a un subcontrato, o valor predeterminado introdúcese desde o rexistro da conta do provedor e pódese cambiar. Despois de gardar unha factura de provedor, a moeda xa non se pode editar. |
| Unidade de contratación | A división da empresa que se encarga de recibir os servizos e/ou produtos do provedor. | Nada |
| Condicións de pagamento | Condicións de pagamento das facturas de provedores que se emitan. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | As condicións de pago dun subcontrato cópianse en todas as facturas de provedores relacionadas co subcontrato. As condicións de pago pódense actualizar se a factura do provedor ten o estado de **Borrador**. |
| Enderezo de pago | O enderezo do fornecedor ao que se deben enviar os pagamentos. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | O enderezo de pago dun subcontrato cópiase como enderezo de pago a todas as facturas de provedores que se crean para ese subcontrato. O enderezo de pago pódese actualizar se a factura do provedor ten o estado de **Borrador**. |
| Subtotal | Se a factura do provedor non ten liñas, introduza o subtotal da factura antes de impostos. Se a factura do provedor ten liñas, este campo é de só lectura. Neste caso, o importe que se mostra é o subtotal de todas as liñas da factura do provedor. | Nada |
| Imposto total | Se a factura do provedor non ten liñas, introduza os impostos totais do subcontrato. Se a factura do provedor ten liñas, este campo é de só lectura. Neste caso, o importe que se mostra é a suma dos importes fiscais de todas as liñas da factura do provedor. | Nada |
| Cantidade total | Este campo calculado mostra o importe total da factura do provedor despois de incluír os impostos. | Nada |

> [!NOTE]
> Os seguintes campos dunha factura de provedor non se poden cambiar despois de gardar a factura de provedor: **Vendedor**, **·**, **·**, **de contratación**, e **Termos de pago**. Se é necesario realizar algún cambio nestes campos nunha factura de provedor, debes eliminar a factura de provedor e crear unha nova factura de provedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
