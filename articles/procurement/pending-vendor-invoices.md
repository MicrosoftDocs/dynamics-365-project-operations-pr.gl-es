---
title: Comprar materiais sen fornecemento ou categorías de adquisición usando unha factura pendente de fornecedor
description: Este artigo explica como rexistrar as facturas pendentes do fornecedor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921990"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Comprar materiais sen fornecemento ou categorías de adquisición usando unha factura pendente de fornecedor

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Cando unha empresa adquire materiais sen fornecemento ou categorías de adquisición para un proxecto, os custos pódense rexistrar de inmediato no proxecto. 

Por exemplo, Contoso Robotics US está a realizar un proxecto de renovación de equipos e precisa licenzas de software. Estas licenzas adquírense a un fornecedor externo.  Usando Dynamics 365 Finance, o empregado de contas pendentes de pago rexistra un documento de factura pendente do fornecedor e atribúe os custos da licenza directamente ao proxecto de renovación de equipos. 

> [!IMPORTANT]
> Antes de empregar a funcionalidade descrita neste artigo, revise e aplique as configuracións necesarias. Para obter máis información, consulte [Activa materiais sen fornecemento e facturas pendentes do fornecedor](configure-materials-nonstocked.md) e [Usar categorías de adquisición con pedidos de compra de proxectos e facturas de fornecedores pendentes](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Enviar unha factura pendente fornecedor relacionada co proxecto 

As facturas pendentes do fornecedor poden rexistrarse na páxina **Facturas pendentes do fornecedor** (**Contas pendentes de pago** > **Facturas** > **Facturas pendentes do fornecedor**). Complete os seguintes pasos para publicar unha factura pendente do fornecedor relacionada co proxecto:

1. Vaia a **Contas pendentes de pago** > **Facturas** e seleccione **Nova**. 
1. No campo **Conta de factura**, seleccione un fornecedor e, a seguir, no campo **Número**, introduza a identificación da factura do fornecedor.
1. Engada unha liña á factura do fornecedor e logo, no campo **Número de artigo**, seleccione o artigo sen fornecemento comprado ao fornecedor. Alternativamente, no campo **Categoría de adquisición**, seleccione a categoría de adquisición que se comprou ao fornecedor.   
1. Engada a cantidade que se comprou. O sistema enche o prezo unitario en función da configuración do prezo do elemento sen fornecemento. 
1. Verifique o importe total e outros detalles requiridos na liña.
1. Nos detalles da liña, no separador **Proxecto**, seleccione o ID do proxecto no que se rexistrará este elemento.
1. Opcional: Seleccione o número de actividade e actualice a categoría do proxecto e a propiedade da liña.
1. Contabilice a factura pendente do fornecedor. Cando se contabiliza a factura, o sistema rexistra a seguinte información:
    
    - O importe do saldo do fornecedor.
    - O importe do imposto de vendas.
    - O custo contra o proxecto rexístrase na conta de integración de adquisicións.
    - Transacción de custo real do proxecto en Dataverse.  Esta transacción procésase mediante o [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Ao contabilizar este diario móvese o importe da conta de integración de adquisicións á conta de custos do proxecto. 
    - Compras que se facturan ao cliente do proxecto mediante o método de facturación de tempo e materiais. Ademais, créanse transaccións de facturación non facturadas para as compras en Dataverse. Lista de prezos de produtos en Dataverse úsase para os prezos e importes de venda para a transacción de vendas sen facturar.
