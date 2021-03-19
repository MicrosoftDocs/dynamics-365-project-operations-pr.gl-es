---
title: Revisar os traballos pendentes de facturación en proxectos e contratos de proxectos
description: Este tema fornece información sobre como revisar o traballo pendente de facturación de tempo, gasto e produtos e como marcalos como listos para a facturación.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282781"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Revisar os traballos pendentes de facturación en proxectos e contratos de proxectos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Cando unha transacción está lista para crear e procesar unha factura, a operación debería marcarse como **Listo para facturar**. Este tema describe os tipos de transaccións que se poden crear.

## <a name="review-the-time-and-material-billing-backlog"></a>Revisar o traballo pendente de facturación de tempo e material

Cando se presenta e aproba unha entrada de tempo ou gasto para un proxecto, PSA crea un dato real de proxecto. Se a combinación do proxecto e a clase de transacción están asignadas a unha liña de contrato para un proxecto de tempo e materiais, créanse dous datos reais cando se aproba a entrada:

- Dato real de custo 
- Dato real de vendas sen facturar

Os datos reais de vendas sen facturar representan o traballo pendente de facturación e hai que establecer o seu estado de facturación en **Listo para facturar**. Cando se crea unha factura do proxecto, os datos reais de vendas sen facturar que están marcados como **Listo para facturar** cópianse como detalles da liña de factura.

Para revisar o calendario de facturación de tempo e materiais, vaia a **Vendas** \> **Facturación** \> **Traballo pendente de facturación de tempo e material**. Seleccione todos os datos reais de vendas sen facturar listas para ser facturadas e logo seleccione **Listo para facturar**. O estado de facturación destes datos reais cambia a **Listo para facturar**.

![Traballo pendente de facturación de tempo e material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Revisar o traballo pendente de facturación de produtos

En PSA, cando un contrato de proxecto ten liñas de contrato baseadas en produtos, considéranse esas liñas para facturar sempre que se cree unha factura para o contrato de proxecto. Calquera produto que teña liñas de contrato que están marcadas como **Listo para facturar** cópiase na factura do proxecto como liñas de factura do proxecto.

Para revisar o traballo pendente de facturación de produtos, vaia a **Vendas** \> **Facturación de produtos** \> **Traballo pendente de facturación de produtos**. Seleccione todas liñas de contrato baseadas en produtos que están listas para ser facturadas e logo seleccione **Listo para facturar**. O estado de facturación destas liñas cambia a **Listo para facturar**.

![Traballo pendente de facturación de produtos](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Revisar os fitos de facturación de contratos de prezo fixo

Cada liña de contrato de proxecto que teña un método de facturación de prezo fixo debe definir os fitos do contrato. Estes fitos do contrato pódense facturar só se están marcados como **Listo para facturar**. 

Para revisar os fitos de facturación, vaia a **Vendas** \> **Facturación** \> **Fitos de prezo fixo**. Seleccione todos os fitos listos para ser facturados e logo seleccione **Listo para facturar**. O estado de facturación destes fitos cambia a **Listo para facturar**.

![Fitos de prezo fixo](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]