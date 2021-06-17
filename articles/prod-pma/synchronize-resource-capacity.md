---
title: Sincronizar capacidade de recursos
description: Este tema ofrece información sobre como sincronizar a capacidade dun recurso entre calendarios e proxectos.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997509"
---
# <a name="synchronize-resource-capacity"></a>Sincronizar capacidade de recursos

[!include [banner](../includes/banner.md)]

Os procesos de sincronización de recursos axudan a garantir que a información do calendario e do calendario base chega á programación de recursos do proxecto. Se se cambia o calendario, os procesos realizan as actualizacións necesarias para a programación dos recursos do proxecto. Os procesos tamén axudan a mellorar o rendemento, porque a información dos recursos do calendario está sincronizada con antelación. Polo tanto, as actualizacións da información de programación de recursos prodúcense con maior rapidez. Recomendámoslle que programe os procesos como un lote en vez de un á vez. En caso contrario, existe o risco de que alguén esqueza as datas incluídas na última sincronización da información. Se non se utilizan datas inclusivas, poden producirse lagoas durante a sincronización de datas.

![Sincronización do calendario](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar agrupamentos de capacidade de recursos

O proceso de sincronización está deseñado para sincronizar toda a información do calendario de recursos. Esta información inclúe información do calendario base sobre calquera cambio na táboa de capacidade do calendario dos recursos do proxecto. Se se engaden novos recursos no proxecto, a sincronización axuda a garantir que a información actualizada do calendario está dispoñible. Esta sincronización pódese facer en calquera momento.

Recomendámoslle que use un lote. As opcións están dispoñibles durante a sincronización das reservas de capacidade.

1. Seleccione **Xestión de proxectos e contabilidade** &gt; **Periódico** &gt; **Sincronización de capacidade** &gt; **Sincronizar agrupamentos de capacidade de recursos**.
2. Configure as opcións na táboa seguinte.

    | Opción      | Descripción |
    |-------------|-------------|
    | Código do período | Opcionalmente, seleccione o código do intervalo de datas do libro maior para establecer as datas de inicio e finalización do proceso de sincronización para os agrupamentos de capacidade de recursos. |
    | Data de inicio  | Introduza a data de inicio do proceso de sincronización para os agrupamentos de capacidade de recursos. |
    | Data de finalización    | Introduza a data de finalización do proceso de sincronización para os agrupamentos de capacidade de recursos. |

[![Proceso de sincronización](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]