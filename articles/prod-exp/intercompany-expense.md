---
title: Gastos entre empresas
description: Este tema ofrece información sobre como usar os gastos entre empresas para atribuír os gastos dun traballador á entidade legal para a que se realizou o traballo.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005069"
---
# <a name="intercompany-expenses"></a>Gastos entre empresas

Un traballador empregado por unha entidade legal nunha organización pode realizar traballos para outra entidade legal da mesma organización. Pode usar os gastos entre empresas para atribuír os gastos do traballador á entidade legal para a que se realizou o traballo. A entidade legal que emprega ao traballador denomínase entidade legal prestamista. A entidade legal pola que o traballador incorre en gastos chámase entidade xurídica prestameira. 

Antes de que un traballador poida crear e enviar gastos entre empresas, ten que activar as liñas de gastos entre empresas. Na entidade legal prestamista, na páxina **Parámetros de xestión de gastos**, seleccione **Permitir liñas de gasto entre empresas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Contabilización de impostos por gastos entre empresas

[!include [banner](../includes/banner.md)]

Antes de poder empregar no seu informe de gastos os grupos fiscais asociados á entidade legal prestamista (orixe) en lugar da entidade legal prestameira (destino), debe activar a funcionalidade na configuración do imposto sobre as vendas do libro maior. Cando o parámetro **Entidade legal para a contabilización de impostos entre empresas** está definido como **Orixe** e **Aplicar regras de tributación do imposto sobre as vendas** está fixado en **Non**, úsase a combinación de impostos para a entidade legal prestamista. Cando o mesmo parámetro está configurado en **Destino**, utilizarase a combinación fiscal para a entidade legal prestameira. Para as entidades legais dos Estados Unidos, cando o parámetro está establecido en **Orixe**, o campo **Imposto sobre as vendas pendente de cobro** tamén debe configurarse na nova páxina **Grupos de contabilización de libro maior**. O motor de contabilidade utilizará a información deste campo para a entrada contable relacionada cos impostos.   
O comportamento é coherente para as liñas de gastos contabilizadas con ou sen proxecto.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]