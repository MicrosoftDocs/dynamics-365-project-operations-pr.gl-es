---
title: Facturas corrixidas
description: Este tema fornece información sobre facturas corrixidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122386"
---
# <a name="corrected-invoices"></a>Facturas corrixidas

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Pódense editar as facturas confirmadas. Cando edite unha factura confirmada, créase un novo borrador de factura corrixida. Dado que se supón que desexa reverter todas as transaccións e cantidades da factura orixinal, a factura corrixida inclúe todas as transaccións da factura orixinal e todas as cantidades que hai en ela son cero (0).

Cando as transaccións non requiren corrección, pode eliminalas do borrador da factura correctora. Para inverter ou devolver só unha cantidade parcial, pode editar o campo Cantidade no detalle da liña. Se abre o detalle da liña de factura, pode ver a cantidade orixinal da factura. Pode editar a cantidade da factura actual de xeito que sexa inferior ou superior á cantidade da factura orixinal.

Cando se confirma unha factura correctora, invértese o datos real de vendas facturadas orixinais, e créase un novo dato real de vendas facturadas. Se a cantidade foi reducida, a diferenza fará que tamén se cree un novo dato real de vendas sen facturar. Por exemplo, se a vendas orixinal facturada foi de oito horas e o detalle da liña de factura corrixida ten unha cantidade reducida de seis horas, a liña de vendas facturadas orixinal invértese e créanse dous novos datos reais:

- Un dato real de vendas facturadas de seis horas.
- Un dato real de vendas sen facturar das dúas horas restantes. Esta transacción pódese facturar posteriormente ou marcarse como non imputable, dependendo das negociacións co cliente.
