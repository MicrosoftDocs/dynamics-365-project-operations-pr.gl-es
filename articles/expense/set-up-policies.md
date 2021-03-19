---
title: Definir políticas de gastos
description: Pode definir as políticas de gastos que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276076"
---
# <a name="define-expense-policies"></a>Definir políticas de gastos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pode definir as políticas que deben seguir os seus traballadores ao introducir e enviar informes de gastos e solicitudes de viaxes.         
A aplicación de políticas de gastos pode axudarlle a xestionar os gastos de xeito eficaz.         

Por exemplo, pode establecer unha política de gastos de hotel en Nova York, na que se afirma que o gasto por noite non pode superar os 250 USD.       
Se un traballador presenta un informe de gastos ou unha solicitude de viaxe na que a tarifa da habitación supera esta cantidade, o sistema notificará         
ao traballador que se superou o importe da política para o gasto. Pode configurar a mensaxe que recibirá o traballador cando        
defina a política.      
        
Pode definir tres tipos de políticas:         
        
- **Advertencia**: Permite ao traballador presentar un informe de gastos ou unha solicitude de viaxe pero o gasto marcarase para todos os responsables de aprobacións         
  e para informes posteriores.        

- **Erro**: Esixe ao traballador que revise o gasto para cumprir coa política antes de enviar o informe de gastos ou a solicitude de viaxe.        
 
 - **Xustificación**: Require que o traballador ou un xestor introduza unha xustificación por superar o importe da política antes de enviar o informe de gastos ou a solicitude de viaxe.        

## <a name="policy-tips"></a>Consellos sobre políticas
Aquí ten algunhas suxestións que poden axudarlle á hora de crear novas políticas para a xestión de gastos: 

- As políticas teñen data de entrada en vigor, o que significa que unha política non entrará en vigor se se crea cunha data posterior á data na que se produciu o gasto. Por exemplo, vostede crea unha nova política hoxe para aplicar un gasto máximo de comida de 50 $. Os gastos existentes introducidos ata onte non se comprobarán con esta política.
- Ao crear unha política para unha categoría de gastos que se poida detallar, considere engadir unha condición para o tipo de liña de gasto. Algunhas políticas, como esixir un recibo, poden non ter sentido para as liñas detalladas. Nesta situación, a política só se aplica á liña de cabeceira ou a unha liña non detallada. 
- As políticas de xestión de gastos avalíanse por defecto con respecto á entidade de orixe. Para os escenarios entre empresas, pode definir a política que se avaliará coa entidade de destino (entidade prestameira). Para executar as políticas contra a entidade de destino, active a funcionalidade **Avaliar a política de gastos fronte á persoa xurídica prestameira** na área de traballo **Xestión de funcionalidades**.

## <a name="when-to-evaluate-policies"></a>Cando avaliar as políticas

Nos parámetros de xestión de gastos, pode seleccionar avaliar as políticas de xestión de gastos cando se garda unha liña ou cando se envía un informe de gastos. Se elixe avaliar cando se garda unha liña, os usuarios terán unha visibilidade previa do que deben facer para completar o seu informe de gastos á vez. Se non o fai, pode atrasar a avaliación da política e aforrar tempo validándoa ao final, durante o envío ao fluxo de traballo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]