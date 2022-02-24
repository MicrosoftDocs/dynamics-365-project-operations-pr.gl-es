---
title: Configurar políticas de gasto
description: Pode configurar as políticas de gastos que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes en Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271261"
---
# <a name="set-up-expense-policies"></a>Configurar políticas de gasto

Pode definir as políticas que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes.         
A aplicación de políticas de gastos pode axudarlle a xestionar os gastos de xeito eficaz.         

Por exemplo, pode establecer unha política de gastos de hotel en Nova York, na que se afirma que o gasto por noite non pode superar os 250 USD.       
Se un traballador presenta un informe de gastos ou unha solicitude de viaxe na que a tarifa da habitación supera esta cantidade, o sistema notificará        
ao traballador que se superou o importe da política para o gasto. Pode configurar a mensaxe que recibirá o traballador cando        
defina a política.      
        
Pode definir tres tipos de políticas:         
        
- Advertencia – Permite ao traballador presentar un informe de gastos ou unha solicitude de viaxe pero o gasto marcarase para todos os responsables de aprobacións        
  e para informes posteriores.        

- Erro – Esixe ao traballador que revise o gasto para cumprir coa política antes de enviar o informe de gastos ou a solicitude de viaxe.       
 
 - Xustificación – Require que o traballador ou un xestor introduza unha xustificación por superar o importe da política antes de enviar o informe de gastos ou a solicitude de viaxe.        

## <a name="policy-tips"></a>Consellos sobre políticas
Aquí ten algunhas suxestións que poden axudarlle á hora de crear novas políticas para a xestión de gastos. 
* As políticas teñen data de entrada en vigor e non entrarán en vigor se a política se crea cunha data posterior á data na que se produciu o gasto. Por exemplo, se está a crear unha nova política hoxe para aplicar un gasto máximo de comida de 50 $, os gastos existentes introducidos ata onte non se compararán con esta política.
* Ao crear unha política para unha categoría de gastos que se poida detallar, considere engadir unha condición para o tipo de liña de gasto. É posible que algunhas políticas como esixir un recibo non teñan sentido para as liñas detalladas e só se deben aplicar á liña de cabeceira ou a unha liña non detallada. 
* As políticas de xestión de gastos avalíanse por defecto con respecto á entidade de orixe. Para os escenarios entre empresas, pode definir a política que se avaliará coa entidade de destino (entidade prestameira). Para executar as políticas contra a entidade de destino, active a funcionalidade "Avaliar a política de gastos fronte á entidade legal prestameira" na área de traballo **Xestión de funcionalidades**.

## <a name="when-to-evaluate-policies"></a>Cando avaliar as políticas

Nos parámetros de xestión de gastos, hai unha opción para avaliar as políticas de xestión de gastos cando se garda unha liña ou cando se envía un informe de gastos. Se elixe avaliar cando se garda unha liña, isto garante que os usuarios terán unha visibilidade previa do que deben facer para completar o seu informe de gastos á vez. Se non o fai, pode atrasar a avaliación da política e aforrar tempo se fai que a validación ocorra ao final, durante o envío ao fluxo de traballo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]