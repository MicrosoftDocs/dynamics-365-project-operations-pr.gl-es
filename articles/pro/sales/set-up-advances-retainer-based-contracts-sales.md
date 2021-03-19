---
title: Contratos baseados en adiantos e retencións
description: Este tema ofrece información sobre modelos de contratación baseados en retencións e adiantos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e098d25a3e96adf2a1b8e43a19da3a14f446fba9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272341"
---
# <a name="advances-and-retainer-based-contracts"></a>Contratos baseados en adiantos e retencións


_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations admite contratos baseados en retencións. Un contrato baseado en retencións é un conxunto negociado de pagamentos distribuídos igualmente para os que se facturará ao cliente durante un proxecto. Este tipo de contrato úsase normalmente para modelos de facturación baseados no tempo e no material ou no consumo, onde é necesario ofrecerlle ao cliente unha programación previsible de facturación e pagamento. Os datos reais de ingresos acumulados cada período concílianse co pagamento recibido do cliente ao comezo do período. De acordo co concepto de modelo de facturación de tempo e material, os valores de ingresos acumulados en cada período poden variar cos custos incorridos. Se os ingresos acumulados son superiores á cantidade recibida ao comezo do período, a empresa de entrega do proxecto podería:

- Facture ao cliente só o exceso 
- Aprazar a conciliación dos ingresos ao seguinte período de facturación e facer unha factura final ao final do proxecto por todos os ingresos non conciliados restantes

A principal diferenza entre un modelo de contratación baseado en retencións e un modelo de contrato de prezo fixo en Project Operations é que, no modelo de contrato de prezo fixo, o importe da factura non está vinculado nin está ligado aos custos incorridos. A facturación segue un enfoque baseado en fitos que se axusta aos custos incorridos nese período. Nun contrato baseado en retencións, os ingresos que se poden facturar rexístranse en función do método de facturación da liña de contrato. Cando o método de facturación é tempo e material, os ingresos facturables están ligados aos custos incorridos nun período determinado e poden variar dun período a outro. Non obstante, ao cliente só se lle factura polo importa da retención periódica. O sistema utiliza outra factura ao final do período para conciliar os ingresos facturables rexistrados durante o período co importe polo que se facturou ao cliente ao comezo do período.

A vantaxe deste método é que os custos do cliente fanse previsibles na programación de retencións a diferenza dun modelo de tempo e material típico. A organización que entrega o proxecto tamén ten un espazo para cubrir o risco de recuperar os custos ocasionados por calquera incremento no alcance que un modelo de prezo fixo non lles permitiría.

Ademais dunha programación baseada en retencións periódicas, Project Operations pode rexistrar un adianto unha soa vez dun cliente e concilialo cos diferentes compoñentes do custo do proxecto.

A retención en Project Operations non está dispoñible para o seu uso ata que non se factura ao cliente. Isto está indicado nos seguintes campos da subgrade para adiantos e retencións.

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| Importe dispoñible | O importe que está dispoñible para o seu uso no rexistro de retención ou adianto. | Ata que non se facture o adianto ou retención, non estará dispoñible para o seu uso, o que significa que o importe dispoñible será cero. |
| Importe usado | O importe que xa se utiliza na retención ou o adianto. | Un adianto ou retención pódese conciliar parcialmente nunha factura cos custos reais, que terán marcada algunha parte como xa usada ou consumida. O resto do importe do adianto ou retención está dispoñible para conciliar nunha factura futura cos custos reais. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]