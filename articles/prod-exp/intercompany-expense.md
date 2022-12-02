---
title: Gastos entre empresas
description: Este artigo ofrece información sobre como usar os gastos entre empresas para atribuír os gastos dun traballador á entidade legal para a que se realizou o traballo.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932386"
---
# <a name="intercompany-expenses"></a>Gastos entre empresas

Un traballador empregado por unha entidade legal nunha organización pode realizar traballos para outra entidade legal da mesma organización. Pode usar os gastos entre empresas para atribuír os gastos do traballador á entidade legal para a que se realizou o traballo. A entidade legal que emprega ao traballador denomínase entidade legal prestamista. A entidade legal pola que o traballador incorre en gastos chámase entidade xurídica prestameira. 

Antes de que un traballador poida crear e enviar gastos entre empresas, ten que activar as liñas de gastos entre empresas. Na entidade legal prestamista, na páxina **Parámetros de xestión de gastos**, seleccione **Permitir liñas de gasto entre empresas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Contabilización de impostos por gastos entre empresas

[!include [banner](../includes/banner.md)]

Antes de poder empregar no seu informe de gastos os grupos fiscais asociados á entidade legal prestamista (orixe) en lugar da entidade legal prestameira (destino), debe activar a funcionalidade na configuración do imposto sobre as vendas do libro maior. Cando o parámetro **Entidade legal para a contabilización de impostos entre empresas** está definido como **Orixe** e **Aplicar regras de tributación do imposto sobre as vendas** está fixado en **Non**, úsase a combinación de impostos para a entidade legal prestamista. Cando o mesmo parámetro está configurado en **Destino**, utilizarase a combinación fiscal para a entidade legal prestameira. Para as entidades legais dos Estados Unidos, cando o parámetro está establecido en **Orixe**, o campo **Imposto sobre as vendas pendente de cobro** tamén debe configurarse na nova páxina **Grupos de contabilización de libro maior**. O motor de contabilidade utilizará a información deste campo para a entrada contable relacionada cos impostos.   
O comportamento é coherente para as liñas de gastos contabilizadas con ou sen proxecto.  

## <a name="new-expense-expression-builder"></a>Novo creador de expresións de gastos

O novo creador de expresións de gastos aborda problemas cos escenarios de gastos entre empresas que utilizan proxectos. Esta funcionalidade garante que, cando crea un gasto entre empresas, a política de gastos se valide correctamente en relación co proxecto seleccionado na liña de gastos e que o informe de gastos se poida enviar con éxito.

Para que a funcionalidade de creador de expresións de gastos funcione, debe estar activada. Ademais, debe configurarse a política de gastos que ten un ID de proxecto.

Se xa configurou políticas que validan o ID do proxecto na liña de gastos, esas políticas deben retirarse. A seguir, pode activar a funcionalidade e volver configurar as políticas.

Para activar a funcionalidade, siga estes pasos.

1. Vaia a **Áreas de traballo** \> **Xestión de funcionalidades**.
2. Na lista, seleccione **Novo creador de expresións de gastos para abordar problemas cos escenarios de gastos entre empresas que utilizan proxectos**. Despois seleccione **Activar agora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
