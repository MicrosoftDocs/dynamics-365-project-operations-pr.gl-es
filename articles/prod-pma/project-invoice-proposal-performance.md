---
title: Rendemento de proposta de factura de proxecto
description: Este artigo ofrece información sobre melloras de rendemento nas propostas de facturas de proxectos.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927188"
---
# <a name="project-invoice-proposal-performance"></a>Rendemento de proposta de factura de proxecto

[!include [banner](../includes/banner.md)]

Cando crea unha nova proposta de factura, é posible que teña problemas de rendemento a medida que aumenta o número de proxectos e subproxectos. Para mellorar o rendemento, está dispoñible unha función que reduce o tempo necesario para crear unha nova proposta de factura para as transaccións do proxecto contabilizadas.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Activar a mellora do rendemento das propostas de factura do proxecto
Para activar a función de mellora do rendemento das propostas de factura do proxecto, complete os seguintes pasos.

1.  Vaia a **Xestión de funcionalidades** > **Todo**. Na lista de funcionalidades, localice **Mellora do rendemento das propostas de factura do proxecto**.
2.  Seleccione **Activar agora**.
3.  Actualice o explorador e cree unha nova proposta de factura.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Desactivar a mellora do rendemento das propostas de factura do proxecto
Complete os seguintes pasos para desactivar a mellora do rendemento das propostas de factura do proxecto.

1.  Vaia a **Xestión de funcionalidades** > **Todo**. Na lista de funcionalidades, localice **Mellora do rendemento das propostas de factura do proxecto**.
2.  Seleccione **Desactivar**.
3.  Actualice o explorador.

> [!NOTE]
> O rendemento da proposta de factura non se pode aplicar cando se activan as regras de facturación.
> 
> Durante o proceso por lotes para crear propostas de factura, o número de subtarefas dividirá as tarefas a un número máximo en función do número de contratos con transaccións facturables, independentemente do que introducise. Por exemplo, se introduce **3** para o número de subtarefas para a creación de propostas de factura por lotes e só hai dous contratos con transaccións facturables, só se crean dúas subtarefas.
