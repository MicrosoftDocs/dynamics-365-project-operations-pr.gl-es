---
title: Prezos do catálogo de produtos
description: Este tema fornece información sobre como funcionan os prezos do catálogo de produtos en Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3fb9b51d58cbe3b0db6dad902461b90ac04cc42f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151206"
---
# <a name="product-catalog-pricing"></a>Prezos do catálogo de produtos 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


As entidades listas de prezos e elemento de lista de prezos admiten os prezos do catálogo de produtos. Na súa maior parte, esta funcionalidade úsase para liñas baseadas en catálogo en ofertas de proxecto e contratos de proxecto.

Para liñas baseadas en proxectos, un contrato representa o acordo despois gañalo. Debido a que o proceso de negociación normalmente precede á ganancia, o prezo que se anexa á oferta cópiase sempre tal como está nunha lista de prezos nova e anexa ao contrato. Esta nova lista de prezos non se pode cambiar fóra do ámbito do contrato. Esta limitación axuda a protexer a tarxeta de tarifas que se negociaba fronte a calquera cambio de prezo que se produza na lista de prezos.

Os produtos deben configurarse de xeito que teñan listas de custos e prezos por defecto no catálogo de produtos. Debe usar o prezo da lista, o custo estándar e o custo actual para configurar o custo predeterminado e os prezos da lista. Os prezos da lista por defecto úsanse nunha liña de presupostos ou nunha liña de contratos de proxecto só cando o sistema non atopa unha liña de prezos para ese produto na lista de prezos do produto para a oferta ou contrato de proxecto.

O prezo de custo das liñas de catálogo de produtos pódese cambiar entre ofertas. Esta capacidade é importante, porque se non rastrexa con precisión os custos, non pode determinar os beneficios operativos nas compromisos do proxecto. Por defecto, o custo estándar do produto utilízase como prezo de custo Non obstante, o prezo de custo por defecto pódese actualizar na liña de oferta se hai un prezo de custo diferente para esa oferta.

## <a name="price-list-items"></a>Elementos da lista de prezos

Pode engadir produtos dun catálogo de produtos a diferentes listas de prezos. As liñas de lista prezos dos produtos fan referencia sempre a unha unidade específica. Os prezos dun produto dos elementos da lista de prezos pódense configurar como cantidade de moeda. Alternativamente, pódese configurar en función do prezo da lista, do custo actual ou do custo estándar.

PSA admite varias opcións de redondeo cando os prezos están configurados en función do prezo de lista, do custo estándar ou do custo actual. Ademais de aproveitar múltiples métodos de prezos e opcións de redondeo, pode asociar listas de descontos con elementos da lista de prezos. 

> ![Engadir produtos dun catálogo a diferentes listas de prezos.](media/basic-guide-16.png)

Ao crear unha nova lista de prezos personalizados para unha oferta, seleccione **Crear prezos personalizados** na páxina **Oferta de proxecto**, PSA fai unha copia da lista de prezos e o campo **Entidade** da cabeceira da nova lista de prezos establécese en **Entidade de vendas** O nome da nova lista de prezos engádese co nome da oferta e unha marca de tempo. Tamén pode usar o nome da nova lista de prezos e o nome da oferta en fluxos de traballo personalizados para activar revisións e aprobacións adicionais para ofertas que usan prezos personalizados.

 
## <a name="default-product-price-list"></a>Lista de prezos de produtos predefinida
Cada rexistro de clientes ten un campo **Lista de prezos por defecto**, onde pode especificar unha lista de prezos que coincida coa moeda do cliente. En PSA, este valor por defecto non se introduce automaticamente neste campo. Cando existe un acordo de prezos personalizado cun cliente específico, pode usar este campo para asociar unha lista de prezos a ese cliente.

As entidades Oportunidade, Oferta e Contrato de proxecto usan a seguinte orde para introducir listas de prezos de produtos por defecto. A mesma orde úsase para listas de prezos de proxecto.

1.  Oferta
2.  Oportunidade
3.  Cliente
4.  Configuración global para PSA

Por defecto, o campo **Produto** da liña de oferta indica todos os produtos activos na lista de prezos do produto. Se un produto foi inactivado ou se é un produto borrador, non aparece na lista, aínda que estea na lista de prezos. 

As liñas de catálogo de produtos engádense como liñas de factura na primeira factura que se crea para un contrato de proxecto. Nun borrador de factura, pódense eliminar esas liñas de factura. Nese caso, as liñas aparecerán nunha factura posterior ata a facturación ou ata que a factura se envíe ao cliente. En PSA, non pode facturar unha cantidade parcial dunha liña de factura de produto. Cando se facturan as liñas de produto do contrato do proxecto, créanse datos reais. Non obstante, eses datos reais non están ligados á entidade de proxecto relacionada. Noutras palabras, as liñas de contrato de proxecto baseadas en produtos son independentes de calquera uso baseado en proxectos. PSA non rastrexa o consumo de material nos proxectos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]