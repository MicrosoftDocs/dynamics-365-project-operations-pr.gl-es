---
title: Visión xeral de liñas de oferta baseada en produto - lite
description: Este tema ofrece información sobre o traballo con liñas de oferta baseada en produto.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994449"
---
# <a name="product-based-quote-lines-overview---lite"></a>Visión xeral de liñas de oferta baseada en produto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Pode crear liñas de oferta baseadas en produtos Dynamics 365 Project Operations. As liñas de oferta baseadas en produtos poden engadirse manualmente ou poden ser elementos do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Cada produto do catálogo de produtos ten unha unidade e un grupo de unidades por defecto. Se varios produtos comparten o mesmo conxunto de atributos, pode crear unha familia de produtos que comparta eses atributos. 

Por exemplo, unha empresa vende licenzas de subscrición para diferentes tipos de software. Todo o software de subscrición ten os dous atributos seguintes:

- Número de usuarios
- Unha duración da subscrición medida en meses

Para manter este tipo de catálogo, cree unha familia de produtos que leva o nome **Software de subscrición** e engada o número de usuarios e a duración da subscrición como atributos. A seguir, pode engadir produtos individuais á familia de produtos de **Software de subscrición**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Engadir elementos do catálogo de produtos a unha oferta de proxecto

As páxinas **Oferta de proxecto** e **Contrato de proxecto** teñen seccións para liñas baseadas en proxecto e liñas baseadas en produto. Para liñas baseadas en produto, a lista despregable na liña de oferta ou liña de contrato de proxecto inclúe todos os produtos e unidades da lista de prezos de produtos. Tamén pode engadir produtos que non forman parte da lista de prezos de produtos.

Ademais, pode seleccionar produtos doutras listas de prezos ou directamente do catálogo de produtos. Cando selecciona produtos directamente dun catálogo de produtos, utilízase a lista de prezos por defecto dese produto para obter o prezo de venda do produto. Se non se establece unha lista de prezos por defecto, o prezo será de cero (0).

Cando unha liña de oferta está baseada nun catálogo de produtos, pode anular o prezo de venda directamente na liña de oferta. Unha liña de oferta no campo **Prezos** con dous valores dispoñibles:

- **Anular prezos**
- **Utilizar predefinido**

Se selecciona **Anular prezos**, o prezo por defecto non está definido. En lugar diso, debe introducir un prezo para o produto na liña de oferta. Se selecciona **Usar predefinido**, úsase o prezo de venda por defecto e o campo está bloqueado para a súa edición.

Os prezos de venda por defecto introdúcense nas liñas baseadas en produtos dunha oferta. O campo **Prezos** defínese como **Anular prezos** para que poida editar o prezo por defecto nas liñas de oferta. Trátase dunha anulación específica de Project Operations do comportamento das liñas baseadas en produto en Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]