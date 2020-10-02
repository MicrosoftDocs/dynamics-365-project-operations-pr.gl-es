---
title: Facturas corrixidas
description: Este tema fornece información sobre facturas corrixidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898079"
---
# <a name="corrected-invoices"></a>Facturas corrixidas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pódense editar as facturas confirmadas. Cando edite unha factura confirmada, créase un novo borrador de factura corrixida. Dado que se supón que desexa reverter todas as transaccións e cantidades da factura orixinal, a factura corrixida inclúe todas as transaccións da factura orixinal e todas as cantidades que hai en ela son cero (0).

Cando as transaccións non requiren corrección, pode eliminalas do borrador da factura correctora. Para inverter ou devolver só unha cantidade parcial, pode editar o campo Cantidade no detalle da liña. Se abre o detalle da liña de factura, pode ver a cantidade orixinal da factura. Pode editar a cantidade da factura actual de xeito que sexa inferior ou superior á cantidade da factura orixinal.

Cando se confirma unha factura correctora, invértese o datos real de vendas facturadas orixinais, e créase un novo dato real de vendas facturadas. Se a cantidade foi reducida, a diferenza fará que tamén se cree un novo dato real de vendas sen facturar. Por exemplo, se a vendas orixinal facturada foi de oito horas e o detalle da liña de factura corrixida ten unha cantidade reducida de seis horas, a liña de vendas facturadas orixinal invértese e créanse dous novos datos reais:

- Un dato real de vendas facturadas de seis horas.
- Un dato real de vendas sen facturar das dúas horas restantes. Esta transacción pódese facturar posteriormente ou marcarse como non imputable, dependendo das negociacións co cliente.
