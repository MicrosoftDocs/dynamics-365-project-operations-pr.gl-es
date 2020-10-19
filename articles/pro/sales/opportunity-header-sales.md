---
title: Cabeceira de oportunidade
description: Este tema ofrece información sobre a información xeral sobre acordos baseados en proxecto e as liñas de oportunidade baseada en proxecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906159"
---
# <a name="opportunity-header"></a>Cabeceira de oportunidade

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

A cabeceira Oportunidade recolle a información xeral sobre un acordo baseado en proxecto que se aplica a todas as liñas da oportunidade baseada en proxecto.

As oportunidades baseadas en proxecto en Dynamics 365 Project Operations son extensións de oportunidades en Dynamics 365 Sales. Estas extensións proporcionan unha funcionalidade adicional específica e necesaria para oportunidades baseadas en proxecto. Estas extensións poden incluír novos campos e accións de banda dispoñibles en oportunidades baseadas en proxecto. Pode atopar que algúns campos, funcionalidade e lóxica predefinida que están dispoñibles en Vendas non están dispoñibles en Project Operations.

A seguinte táboa inclúe os campos dunha oportunidade baseada en proxecto que son exclusivos de Project Operations ou teñen algúns cambios importantes no comportamento das oportunidades en vendas.

| **Campo** | **Localización** | **Relevancia, finalidade e orientación** | **Impacto descendente** |
| --- | --- | --- | --- |
| Tipo | Separador Xeral (oculto) | Este campo de conxunto de opcións ten as seguintes opcións:</br>- Baseado en traballo (dispoñible só con Project Operations)</br>- Baseado en elementos (dispoñible só cando Project Operations e Sales están instaladas)</br>- Baseado en mantemento de servizo (dispoñible cando se instala Field Service) | Cando usa Project Operations, este valor de campo configúrase automaticamente en **Baseado en traballo**, que clasifica a oportunidade como baseada en proxecto. A oportunidade debe estar baseada en proxecto para activar todas as extensións e funcionalidades específicas do proxecto no proceso de vendas descendentes para este acordo. |
| Contacto | Separador Xeral | Referencia ao contacto principal do cliente para este acordo. | |
| Conta | Separador Xeral | Referencia á empresa ou ao rexistro da conta do cliente. | |
| Xestor de contas | Separador Xeral | O nome do xestor de contas desta oportunidade baseada en proxecto. | O xestor de contas é o responsable de xestionar a relación co cliente a través durante a realización deste proxecto. Baseada no rexistro de recursos reservables ligado ao xestor de contas, a unidade de contratación está predefinida. |
| Unidade de contratación | Separador Xeral | A unidade de organización que se encarga da entrega do proxecto ou proxectos asociados a este acordo. | A unidade de contratación é a división da empresa que completará os proxectos despois de pechar o acordo. Cada unidade de contratación ten unha moeda e esta moeda úsase para informar dos custos estimados e reais incorridos durante o proxecto. |

Para todos os demais campos e seccións do separador **Resumo** da oportunidade, consulte [Crear ou editar oportunidades (vendas e plataforma común de vendas)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
