---
title: Adquira materiais ou categorías de aprovisionamento non almacenados mediante unha factura de provedor pendente
description: Este artigo explica como rexistrar facturas de provedores pendentes.
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
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Adquira materiais ou categorías de aprovisionamento non almacenados mediante unha factura de provedor pendente

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Como unha empresa adquire materiais non abastecidos ou categorías de adquisición para un proxecto, os custos pódense rexistrar inmediatamente contra o proxecto. 

Por exemplo, Contoso Robotics US está a realizar un proxecto de renovación de equipos e precisa licenzas de software. Estas licenzas adquírense a un fornecedor externo.  Usando Dynamics 365 Finance, o empregado de contas a pagar rexistra un documento de factura do provedor pendente e atribúe os custos da licenza directamente ao proxecto de renovación do equipo. 

> [!IMPORTANT]
> Antes de utilizar a funcionalidade descrita neste artigo, revise e aplique as configuracións necesarias. Para obter máis información, consulte [Activa os materiais non abastecidos e as facturas de provedores pendentes](configure-materials-nonstocked.md) e [Use categorías de adquisición con pedidos de compra de proxectos e facturas de provedores pendentes](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Enviar unha factura pendente fornecedor relacionada co proxecto 

As facturas pendentes do fornecedor poden rexistrarse na páxina **Facturas pendentes do fornecedor** (**Contas pendentes de pago** > **Facturas** > **Facturas pendentes do fornecedor**). Complete os seguintes pasos para publicar unha factura pendente do fornecedor relacionada co proxecto:

1. Ir a **Contas por pagar** > **Facturas**, e seleccione **Novo**. 
1. No **Conta de factura** campo, seleccione un provedor e, a continuación, no campo **Número** campo, introduza a identificación da factura do provedor.
1. Engade unha liña á factura do provedor e, a continuación, no **Número de artigo** campo, seleccione o artigo non almacenado que foi adquirido ao provedor. Alternativamente, no **Categoría de contratación** campo, seleccione a categoría de adquisición que se comprou ao provedor.   
1. Engade a cantidade que foi comprada. O sistema enche o prezo unitario, en función da configuración do prezo do artigo non almacenado. 
1. Verifique o importe total e outros detalles requiridos na liña.
1. Nos detalles da liña, no **Proxecto** ficha, seleccione o ID do proxecto no que se gravará este elemento.
1. Opcional: seleccione o número de actividade e actualice a categoría do proxecto e a propiedade da liña.
1. Publicar a factura do provedor pendente. Cando se publica a factura, o sistema rexistra a seguinte información:
    
    - O importe do saldo do fornecedor.
    - O importe do imposto de vendas.
    - O custo contra o proxecto rexístrase na conta de integración de adquisicións.
    - Transacción de custo real do proxecto en Dataverse.  Esta transacción procésase mediante o [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Ao contabilizar este diario móvese o importe da conta de integración de adquisicións á conta de custos do proxecto. 
    - Compras que se facturan ao cliente do proxecto mediante o método de facturación de tempo e materiais. Ademais, créanse transaccións de facturación non facturadas para as compras en Dataverse. Lista de prezos de produtos en Dataverse úsase para os prezos e importes de venda para a transacción de vendas sen facturar.
