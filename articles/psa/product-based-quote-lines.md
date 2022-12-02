---
title: Liñas de oferta baseadas en produtos
description: Este artigo fornece información sobre liñas de oferta baseadas en produtos.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a5385e1bb0f18a7cc1d23f4e46c86d8340ba951d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922680"
---
# <a name="product-based-quote-lines"></a>Liñas de oferta baseadas en produtos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Pode crear liñas de oferta baseadas en produtos Dynamics 365 Project Service Automation. As liñas de oferta baseadas en produtos poden ser liñas "fóra de catálogo" ou poden ser elementos do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Os produtos dun catálogo de produtos de Dynamics 365 teñen unha unidade por defecto e un grupo de unidades. Se varios produtos comparten o mesmo conxunto de atributos, pode crear unha familia de produtos que tamén teña eses atributos. Todos os produtos dunha familia de produtos herdan o mesmo conxunto de atributos.

Por exemplo, unha empresa vende licenzas de subscrición para unha variedade de software. Todo o software de subscrición ten os dous atributos seguintes:

- Número de usuarios 
- Duración da subscrición (en meses)

Un bo xeito de manter este tipo de catálogo é crear unha familia de produtos que leva o nome **Software de subscrición**, e iso ten **Número de usuarios** e **Duración da subscrición** como atributos. Pode engadir produtos individuais, como **Dynamics 365 Sales** ou **Dynamics 365 Field Service** á familia de produtos **Software de subscrición**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Engadir elementos do catálogo de produtos a unha oferta de proxecto

As páxinas de oferta de proxecto e contrato de proxecto teñen seccións para dous tipos de liñas: liñas baseadas en proxectos e liñas baseadas en produtos. Para liñas baseadas en produtos, Dynamics 365 úsase para engadir elementos dun catálogo de produtos a unha oferta. A lista despregable na liña de oferta ou liña de contrato de proxecto inclúe todos os produtos e unidades da lista de prezos de produtos que se anexa á oferta ou contrato de proxecto. Tamén pode engadir produtos que non forman parte da lista de prezos da oferta.

Ademais, pode seleccionar produtos doutras listas de prezos ou pode seleccionar os produtos directamente do catálogo de produtos. Cando selecciona produtos directamente dun catálogo de produtos, utilízase a lista de prezos por defecto dese produto para obter o prezo de venda do produto. Se non se establece unha lista de prezos por defecto, o prezo será de 0 (cero).

Se unha liña de oferta está baseada nun catálogo de produtos, pode anular o prezo de venda directamente na liña de oferta. Teña en conta que unha liña de oferta en Dynamics 365 ten un campo **Prezos**. Hai dous valores dispoñibles:

- Anular prezos  
- Usar predefinido

Se definiu este campo en **Anular prezos**, Dynamics 365 non establece un prezo por defecto. Debe introducir un prezo para o produto na liña de oferta. Se definiu este campo como **Usar predefinido**, Dynamics 365 usa o prezo de venda predefinido e bloquea o campo para evitar a edición.

Despois de instalar PSA, os prezos de venda por defecto introdúcense nas liñas baseadas en produtos nunha oferta. O campo **Prezos** defínese como **Anular prezos** para que poida editar o prezo por defecto nas liñas de oferta.

> ![Establecer anular prezos.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Factores de cantidade para produtos

PSA usa factores de cantidade para apoiar a venda de produtos baseados en subscrición. Para os produtos baseados en subscrición, a cantidade na liña de oferta ou contrato de proxecto exprésase como o número de meses de usuario.

Normalmente, o prezo do software de subscrición almacénase no catálogo como o prezo por usuario ao mes. Non obstante, pode usar outras descricións de tempo no seu lugar. Durante o proceso de vendas, o prezo na liña de oferta adoita ser o prezo por usuario, por mes que foi negociado e descontado polo axente de vendas de TI. Cada acordo ten un número diferente de usuarios e un número diferente de meses de subscrición. A cantidade que se utiliza para calcular a cantidade da liña de oferta é un produto do número de usuarios e do número de meses de subscrición.

Para apoiar este tipo de venda, PSA introduciu o concepto de factores de cantidade. Os factores de cantidade dependen dos atributos do produto en Dynamics 365. Ao configurar propiedades específicas para un produto, PSA permítelle marcar un subconxunto destas propiedades ou de todas as propiedades como factores de cantidade.

PSA valida que só as propiedades numéricas ou propiedades de produto que teñen un tipo de datos numéricos estean marcadas como factores de cantidade. Cando un produto para o que se configuran os factores de cantidade se engade a unha liña de presupostos, o campo **Cantidade** na liña de oferta convértese nun campo de só lectura. Despois de introducir valores para as propiedades do produto que son factores de cantidade, PSA calcula a cantidade da liña de oferta.

Por exemplo, Dynamics 365 pode ter as seguintes propiedades: 

- **N.º de usuarios** - O número de usuarios 
- **Nº de meses** - O número de meses de subscrición
- **SKU de produto** 

As propiedades **N.º de Usuarios** e **N.º de meses** pódense marcar como factores de cantidade editando as propiedades da liña de produtos. 

> ![Marcado de n.º de usuarios e n.º de meses como factores de calidade.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
