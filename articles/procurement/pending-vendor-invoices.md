---
title: Comprar materiais sen fornecemento usando unha factura pendente de fornecedor
description: Este tema explica como rexistrar as facturas pendentes do fornecedor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547287"
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
    - Transacción de custo real do proxecto en Dataverse.  Esta transacción procésase mediante o [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Ao contabilizar este diario móvese o importe da conta de integración de adquisicións á conta de custos do proxecto. 
    - Compras que se facturan ao cliente do proxecto mediante o método de facturación de tempo e materiais. Ademais, créanse transaccións de facturación non facturadas para as compras en Dataverse. Lista de prezos de produtos en Dataverse úsase para os prezos e importes de venda para a transacción de vendas sen facturar.
