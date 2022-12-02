---
title: Confirmar facturas de fornecedor do proxecto
description: Este artigo explica como confirmar unha factura de fornecedor de proxecto en Microsoft Dynamics 365 Project Operations e describe o impacto financeiro de confirmar unha factura do fornecedor do proxecto.
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
# <a name="confirm-project-vendor-invoices"></a>Confirmar facturas de fornecedor do proxecto

**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento

Cando o parámetro **Requírese confirmación manual por PM** está activado, as facturas de fornecedores que se crean en Microsoft Dataverse teñen o estado de **Borrador**. As facturas de fornecedores que se crean deste xeito deben revisarse e confirmarse manualmente. Cando o parámetro **Requírese confirmación manual por PM** está desactivado, as facturas de fornecedores que se crean en Dataverse confírmanse automaticamente. Non son necesarias máis accións. 

Despois de verificar todas as liñas dunha factura de fornecedor en Dynamics 365 Project Operations, seleccione **Confirmar** para confirmar a factura do fornecedor.

Cando seleccione **Confirmar** nunha factura de fornecedor, ocorre o seguinte comportamento:

1. Actualízase o estado da factura do fornecedor a **Confirmada**.
1. A factura do fornecedor confirmada e os seus rexistros relacionados pasan a ser de só lectura e non se poden editar nin eliminar.
1. Se algún dato real de custo fai referencia á liña de factura do fornecedor como parte do proceso de busca de coincidencias, todos os datos reais de custo que están asociados á liña de factura do fornecedor de referencia reverteranse.
1. Os novos datos reais de custo créanse utilizando a información da liña de factura do fornecedor.
1. Xa non pode crear diarios de corrección, procesar os recordatorios de entradas de tempo ou cancelar a aprobación dos datos reais de tempo, gasto ou material orixinais que se reverteron.
1. En Dynamics 365 Finance, o valor de **Custo do proxecto** actualízase mediante o diario de integración do proxecto e a conta de integración de adquisicións *revértese* despois de publicar o diario de integración do proxecto.

> [!NOTE]
> Se algunha liña dunha factura de fornecedor ten un estado de verificación distinto de **Completa**, a factura do fornecedor non se pode confirmar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
