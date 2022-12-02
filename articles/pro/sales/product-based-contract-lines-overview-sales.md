---
title: Visión xeral de liñas de contrato baseado en produto - lite
description: Este artigo fornece información sobre liñas de contrato baseado en produtos.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919874"
---
# <a name="product-based-contract-lines-overview---lite"></a>Visión xeral de liñas de contrato baseado en produto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Pode crear liñas de contrato baseado en produtos en Dynamics 365 Project Operations. As liñas de contrato baseado en produtos poden ser liñas creadas manualmente ou poden ser elementos do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Os produtos do catálogo de produtos teñen unha unidade por defecto e un grupo de unidades. Se varios produtos comparten o mesmo conxunto de atributos, pode crear unha familia de produtos que tamén teña eses atributos. Todos os produtos dunha familia de produtos herdan o mesmo conxunto de atributos.

Por exemplo, unha empresa vende licenzas de subscrición para diferentes tipos de software. Todo o software de subscrición ten os dous atributos seguintes:

- Número de usuarios
- Duración da subscrición (en meses)

Para manter este tipo de catálogo, cree unha familia de produtos con nome **Software de subscrición**. Engada os atributos **Número de usuarios** e **Duración da subscrición** á familia de produtos. A seguir, engada produtos individuais á familia de produtos **Software de subscrición**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Engadir elementos do catálogo de produtos a un contrato de proxecto

Os contratos de proxecto e contrato de proxecto teñen seccións para dous tipos de liñas: liñas baseadas en proxectos e liñas baseadas en produtos. As liñas baseadas en produtos inclúen todos os produtos e unidades da lista de prezos do contrato. Poden engadirse produtos que non forman parte da lista de prezos de produtos do contrato.

Pode seleccionar produtos doutras listas de prezos ou directamente do catálogo de produtos. Cando selecciona produtos directamente dun catálogo de produtos, utilízase a lista de prezos por defecto dese produto para o prezo de venda do produto. Se non se establece unha lista de prezos por defecto, o prezo será de 0 (cero).

Se unha liña de contrato está baseada nun catálogo de produtos, pode anular o prezo de venda directamente na liña. Unha liña de contrato ten o campo **Prezos** cos dous valores:

- **Anular prezos**
- **Usar predefinido**

Se definiu o campo **Prezos** en **Anular prezos**, non se establece un prezo por defecto. Introduza un prezo do produto da liña de contrato. Se configura o campo en **Usar predefinido**, úsase o prezo de venda predefinido e o campo non se pode editar.

Despois de instalar Project Operations, os prezos de venda por defecto introdúcense nas liñas baseadas en produtos nun contrato. O campo **Prezos** defínese como **Anular prezos** para que poida editar o prezo por defecto nas liñas de contrato. Trátase dunha anulación específica de Project Operations para o comportamento das liñas baseadas en produto en Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]