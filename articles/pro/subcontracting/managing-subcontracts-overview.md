---
title: Xestión de subcontratos en Project Operations
description: Este tema ofrece unha visión xeral do proceso de xestión de subcontratos de extremo a extremo normalmente en organizacións baseadas en proxectos.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323594"
---
# <a name="subcontract-management-in-project-operations"></a>Xestión de subcontratos en Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este tema ofrece unha visión xeral do proceso de xestión de subcontratos de extremo a extremo en organizacións baseadas en proxectos. A subcontratación de servizos normalmente segue o fluxo do proceso de negocio que se mostra no seguinte diagrama.

![Fluxo do proceso de subcontratación](../media/SubcontractingProcessFlow.png)

A seguinte lista proporciona unha descrición paso a paso do proceso de subcontratación.

1. O xestor do proxecto crea un subcontrato cun provedor. De xeito predefinido, as listas de prezos que se xuntan ao rexistro do fornecedor úsanse para o subcontrato. A conta do fornecedor ten un tipo de relación de **Fornecedor** ou **Provedor**.
2. O xestor do proxecto pode detallar todas as compras como partidas na subcontrata. As liñas de subcontrato poden ser por tempo, gastos ou produtos. A clase de transacción da liña de subcontrato determina para que serve a liña.
3. O xestor de contas do fornecedor e o xestor de proxectos poden repetir o subcontrato. Os prezos poden axustarse nas listas de prezos de compra que se xuntan ao subcontrato.
4. Neste momento ou máis tarde no proceso, se a liña de subcontrato é por tempo, o xestor de contas do fornecedor asocia contactos de fornecedor con cada liña de subcontrato. Esta asociación proporciona información ao xestor do proxecto que está a traballar no subcontrato. Cando un contacto de fornecedor está asociado a unha liña de subcontrato, o sistema crea automaticamente un recurso reservable a partir do contacto, se aínda non existe un recurso reservable.
5. O método de facturación en cada liña de subcontrato pode ser **Prezo fixo** ou **Tempo e material**. Para as liñas de subcontrato a prezo fixo, configúrase un programa de facturas baseado en fitos.
6.  Despois de establecer o subcontrato e completar a negociación, confírmase. Non se poden editar os subcontratos confirmados pero se hai cambios, pódese "reabrir para editar" un subcontrato, que axusta o estado de **Confirmado** a **Borrador** e a negociación pódese reabrir. 
7.  Ao crear un membro do equipo xenérico nun proxecto, o membro do equipo pode asociarse a unha liña de subcontrato. Isto indica a necesidade de dotar de persoal ao equipo xenérico con capacidade de subcontratista.
8.  Os membros do equipo nomeados pódense crear directamente nun proxecto ou ben reservalos empregando as experiencias de programación de recursos. Se un membro do equipo do proxecto designado é un traballador por contrato, é posible asocialo a unha liña de subcontrato. Isto reducirá a capacidade dispoñible nunha liña de subcontrato.
9.  Os recursos dos subcontratistas poden rexistrar o tempo, os gastos e o uso de material en proxectos e tarefas do proxecto e despois sometelos a aprobación. Isto é similar para os empregados. Ao rexistrar o tempo, un traballador por contrato pode seleccionar un subcontrato e unha liña de subcontrato específicos.
10. Despois da aprobación, o tempo aprobado polos subcontratos rexistrará os custos do proxecto en función do prezo de compra do traballador contratado ou do rol que desempeñou no proxecto.
11. As facturas de fornecedor e os elementos de liña da factura do fornecedor pódense rexistrar no sistema para o traballo realizado polos recursos do fornecedor ou os produtos entregados polo fornecedor. As liñas de factura do fornecedor deben ser específicas para un proxecto e para unha clase de transacción de tempo, gasto, produto/material, fito ou taxa. Opcionalmente, as liñas de factura do fornecedor poden facer referencia a unha liña de subcontrato.
12. O sistema asociará automaticamente todos os custos reais que coincidan coa liña de subcontrato e o proxecto á factura do fornecedor. Isto facilitará un proceso de verificación e coincidencia a tres bandas.
13. O xestor do proxecto pode entón revisar os datos reais do proxecto que coinciden automaticamente, eliminar ou engadir outros datos reais de custo do proxecto e completar o proceso de verificación.
14. Ao completar o proceso de verificación en todas as liñas marcarase a factura do fornecedor como **Lista para o pagamento**. Nesta fase, a factura e as liñas do fornecedor pódense transferir a un sistema de contabilidade ou contas pendentes de pago para procesar o pagamento ao vendedor. Os custos do proxecto rexistrados previamente reverteranse e os custos reais da liña de factura do fornecedor rexistraranse no proxecto.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Liñas de subcontrato baseadas en cantidade e liñas de subcontrato baseadas en traballo

Unha liña de subcontrato pode estar baseada na cantidade ou no traballo. 

Cando unha liña de subcontrato está **baseada en cantidade**, a cantidade que se compra na liña de subcontrato por tempo, gasto ou material pode usarse en calquera proxecto.

Cando unha liña de subcontrato está **baseada no traballo**, a liña de subcontrato asígnase a un corpo de traballo representado por un nó no plan do proxecto. O valor da liña de subcontrato é a suma de todos os compoñentes necesarios para entregar ese corpo de traballo. Estes modélanse como detalles da liña de subcontrato e poden ser unha colección de tempo, gastos ou materiais. Para unha liña de subcontrato baseada en traballo, a liña de subcontrato tamén está dedicada a un único proxecto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

