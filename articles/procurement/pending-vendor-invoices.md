---
title: Comprar materiais sen fornecemento usando unha factura pendente de fornecedor
description: Este tema explica como rexistrar as facturas pendentes do fornecedor.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009034"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Comprar materiais sen fornecemento usando unha factura pendente de fornecedor

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Cando unha empresa adquire materiais sen fornecemento para un proxecto, os custos pódense rexistrar de inmediato no proxecto. 

Por exemplo, Contoso Robotics US está a realizar un proxecto de renovación de equipos e precisa licenzas de software. Estas licenzas adquírense a un fornecedor externo.  Usando Dynamics 365 Finance, o empregado de contas pendentes de pago rexistra un documento de factura pendente do fornecedor e atribúe os custos da licenza directamente ao proxecto de renovación de equipos. 

> [!IMPORTANT]
> Antes de empregar a funcionalidade descrita neste tema, revise e aplique as configuracións necesarias. Para obter máis información, consulte [Activa materiais sen fornecemento e facturas pendentes do fornecedor](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Enviar unha factura pendente fornecedor relacionada co proxecto 

As facturas pendentes do fornecedor poden rexistrarse na páxina **Facturas pendentes do fornecedor** (**Contas pendentes de pago** > **Facturas** > **Facturas pendentes do fornecedor**). Complete os seguintes pasos para publicar unha factura pendente do fornecedor relacionada co proxecto:

1. Vaia a **Contas pendentes de pago** > **Facturas** e seleccione **Nova**. 
2. No campo **Conta de factura**, seleccione un fornecedor e no campo **Número**, introduza a identificación da factura do fornecedor.
3. Engada unha liña á factura do fornecedor e no campo **Número de elemento**, seleccione o elemento sen fornecemento comprado ao fornecedor. 

    > [!NOTE]
    > As liñas de factura do fornecedor baseadas nunha categoría de adquisición non se poden rexistrar no proxecto. 
    
5. Engada a cantidade comprada. O sistema encherá o prezo unitario en función da configuración do prezo do elemento sen fornecemento. 
6. Verifique o importe total e outros detalles requiridos na liña.
7. Nos detalles da liña, no separador **Proxecto**, seleccione o ID do proxecto no que se rexistrará este elemento.
8. Opcionalmente, seleccione o número de actividade e actualice a categoría do proxecto e a propiedade da liña.
9. Contabilice a factura pendente do fornecedor. Cando se contabiliza a factura, o sistema rexistra:
    
    - O importe do saldo do fornecedor.
    - O importe do imposto de vendas.
    - O custo contra o proxecto rexístrase na conta de integración de adquisicións.
    - A transacción real do proxecto en Dataverse. Esta transacción procésase mediante o [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Ao contabilizar este diario móvese o importe da conta de integración de adquisicións á conta de custos do proxecto.
