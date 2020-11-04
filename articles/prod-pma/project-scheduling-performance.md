---
title: Rendemento de programación de recursos de proxecto
description: Este tema ofrece información sobre como mellorar o rendemento da programación de recursos para un gran número de proxectos.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076115"
---
# <a name="project-resource-scheduling-performance"></a>Rendemento de programación de recursos de proxecto

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Os problemas de rendemento relacionados coa programación de recursos poden ocorrer cando o número de proxectos alcanza os miles. Para mellorar o rendemento da programación de recursos, está dispoñible unha función que permite aos usuarios reducir o tempo que tardan en lanzar o formulario de dispoñibilidade de recursos. En concreto, isto elimina o proceso de sincronización acumulativa de recursos e usa a táboa **ResProjectResource** para acelerar a busca de recursos. Teña en conta que a táboa **Resrollup** deixará de usarse.

> [!IMPORTANT]
> Se existe unha dependencia do proceso de sincronización de acumulación de recursos ou da táboa **ResProjectResource** , non use esta función.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Activar a mellora do rendemento da programación de recursos
Para activar a mellora do rendemento da programación de recursos, complete os seguintes pasos.

1. Vaia a **Xestión de funcionalidades** > **Todas** e na lista de funcionalidades, localice **Activar a función de mellora do rendemento da programación de recursos do proxecto**.
2. Seleccione **Activar agora**.

> [!NOTE]
> Se non atopa a función na lista, seleccione **Comprobar se hai actualizacións** para actualizar a lista.

3. Actualice o explorador e despois vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Recursos do proxecto** > **Sincronizar a capacidade dos calendarios de recursos en todas as empresas**.
4. Axuste **Eliminar os rexistros de capacidade existentes** en **Si** para eliminar datos anteriores. Se quere xerar datos incrementais, configúreo en **Non**.
5. No campo **Código do período** , seleccione o período no que se deben xerar os datos. Se selecciona un código de período, non é preciso definir unha data de inicio e finalización.
6. Se deixa o campo **Código do período** en branco, seleccione datas específicas de inicio e finalización para xerar datos.
7. Seleccione **Aceptar**.

 > [!NOTE]
 > Isto distribuirá datos xerais á táboa **ResCalendarCapacity** entre todas as empresas do seu ambiente, polo que o traballo por lotes só precisa executarse nunha entidade legal. Os datos deste traballo por lotes son necesarios para calcular a capacidade do recurso a través do calendario asociado.

8. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Recursos do proxecto** > **Poboar recursos do proxecto en todas as empresas** e logo seleccione **Aceptar**. Este é o script de actualización de datos para datos xerais nas táboas **ResProjectResource** , **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**. Os valores para o campo **PSAPRojSchedRole.RootActivity**. Se non se executa, recibirá un aviso cando intente executar operacións de programación de recursos.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Desactivar a mellora do rendemento da programación de recursos

1. Vaia a **Xestión de funcionalidades** > **Todas** e busque **Activar a función de mellora do rendemento da programación de recursos do proxecto**.
2. Seleccione a funcionalidade e logo seleccione o botón **Desactivar**.
3. Actualice o explorador.
4. Vaia a **Xestión de proxectos e contabilidade** > **Periódico** > **Sincronización de capacidade** > **Sincronizar agrupamentos de capacidade de recursos**.
5. Na paxina **Sincronización de acumulación de capacidade** , axuste **Eliminar os rexistros de capacidade existentes** en **Si** para eliminar datos anteriores. Se quere xerar datos incrementais, configúreo en **Non**.
6. No campo **Código do período** , seleccione o período no que se deben xerar os datos. Se selecciona un código de período, non é preciso definir unha data de inicio e finalización.
7. Se deixa o campo **Código do período** en branco, seleccione datas específicas de inicio e finalización para xerar datos.
8. Seleccione **Aceptar**.

> [!NOTE]
> Isto distribuirá datos xerais á táboa **ResRollup** entre todas as empresas do seu ambiente, polo que o traballo por lotes só precisa executarse nunha entidade legal. Este traballo por lotes é necesario para todas as vistas de **Dispoñibilidade de recursos**. Se non se executa este traballo por lotes, os datos de **Resrollup** os datos xeraranse sobre a marcha, o que pode levar algún tempo.
