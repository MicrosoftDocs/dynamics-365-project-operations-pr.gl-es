---
title: Gastos entre empresas
description: Un traballador empregado por unha entidade legal nunha organización pode realizar traballos para outra entidade legal da mesma organización. Nesta situación, pode utilizar a función de gasto entre empresas para atribuír os gastos do traballador á entidade legal para a que se realizou o traballo.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076283"
---
# <a name="intercompany-expenses"></a>Gastos entre empresas

[!include [banner](../includes/banner.md)]

Un traballador empregado por unha entidade legal nunha organización pode realizar traballos para outra entidade legal da mesma organización. Nesta situación, pode utilizar a función de gasto entre empresas para atribuír os gastos do traballador á entidade legal para a que se realizou o traballo. A entidade legal que emprega ao traballador denomínase entidade legal prestamista. A entidade legal pola que o traballador incorre en gastos chámase entidade xurídica prestameira. 

Antes de que un traballador poida crear e enviar gastos por traballos que se realicen para unha entidade legal diferente, na entidade legal prestamista, na páxina **Parámetros de xestión de gastos** , seleccione a opción **Permitir liñas de gasto entre empresas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Contabilización de impostos por gastos entre empresas

[!include [banner](../includes/banner.md)]

Se desexa usar grupos fiscais asociados á entidade legal prestamista (orixe) no canto da entidade legal prestameira (destino) no seu informe de gastos, deberá configuralo no imposto sobre vendas do libro maior. Cando o parámetro do libro maior **Entidade para a contabilización de impostos entre empresas** está establecido en **Orixe** e **Aplicar normas de tributación do imposto sobre as vendas** está establecido en **Non** , empregarase a combinación fiscal para a entidade legal prestamista. Cando o mesmo parámetro está configurado en **Destino** , utilizarase a combinación fiscal para a entidade legal prestameira. Para as entidades legais dos Estados Unidos, cando o parámetro está establecido en **Orixe** , o campo **Imposto sobre as vendas pendente de cobro** tamén debe configurarse na nova páxina **Grupos de contabilización de libro maior**. O motor de contabilidade utilizará a información deste campo para a entrada contable relacionada cos impostos.   
O comportamento é coherente para as liñas de gastos contabilizadas con ou sen proxecto.  
