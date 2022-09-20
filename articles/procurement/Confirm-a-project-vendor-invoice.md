---
title: Confirme as facturas do provedor do proxecto
description: Este artigo explica como confirmar unha factura do provedor do proxecto en Microsoft Dynamics 365 Project Operations e describe o impacto financeiro de confirmar unha factura do provedor do proxecto.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475462"
---
# <a name="confirm-project-vendor-invoices"></a>Confirme as facturas do provedor do proxecto

**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento

Cando o **Requírese confirmación manual por PM** o parámetro está activado, as facturas de provedores que se crean en Microsoft Dataverse ter **Borrador** estado. As facturas de provedores que se crean deste xeito deben revisarse e confirmarse manualmente. Cando o **Requírese confirmación manual por PM** o parámetro está desactivado, as facturas de provedores que se crean en Dataverse confírmanse automaticamente. Non é necesaria ningunha acción adicional. 

Despois de verificar todas as liñas dunha factura de provedor Dynamics 365 Project Operations, seleccione **Confirmar** para confirmar a factura do provedor.

Cando selecciones **Confirmar** nunha factura de provedor, ocorre o seguinte comportamento:

1. O estado da factura do provedor actualízase a **Confirmado**.
1. A factura do provedor confirmada e os seus rexistros relacionados pasan a ser de só lectura e non se poden editar nin eliminar.
1. Se algún custo real fai referencia á liña de factura do provedor como parte do proceso de coincidencia, todos os custos reais que están asociados á liña de factura do provedor referenciado invertéranse.
1. Os novos custos reais créanse utilizando a información da liña de factura do provedor.
1. Xa non pode crear diarios de corrección, procesar recordatorios de entradas horarias nin cancelar a aprobación do tempo orixinal, os gastos ou os datos reais do material que se reverteron.
1. En Dynamics 365 Finance, o **Custo do proxecto** o valor actualízase mediante o diario de integración do proxecto e a conta de integración de Adquisicións *invertida* despois de publicar o diario de integración do proxecto.

> [!NOTE]
> Se algunha liña dunha factura de provedor ten un estado de verificación distinto de **Completa**, a factura do provedor non se pode confirmar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
