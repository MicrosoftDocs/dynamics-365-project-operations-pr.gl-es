---
title: Xestión de unidades complexas como por usuario, por mes para as liñas de oferta baseadas en produto - lite
description: Este artigo ofrece información sobre a xestión de unidades complexas para as liñas de cotización baseadas en produtos.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929902"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Xestión de unidades complexas como por usuario, por mes para as liñas de oferta baseadas en produto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Dynamics 365 Project Operations usa factores de cantidade para apoiar a venda de produtos baseados en subscrición. Para os produtos baseados en subscrición, a cantidade na liña de oferta ou contrato de proxecto exprésase como o número de meses de usuario.

Normalmente, o prezo do software de subscrición almacénase no catálogo como o prezo por usuario ao mes. Durante o proceso de vendas, o prezo na liña de oferta adoita ser o prezo por usuario, por mes que foi negociado e descontado polo axente de vendas de TI. Cada acordo ten un número diferente de usuarios e un número diferente de meses de subscrición. A cantidade que se utiliza para calcular a liña de oferta é un produto do número de usuarios e do número de meses de subscrición.

Para apoiar este tipo de venda, Project Operations introduciu o concepto de factores de cantidade. Os factores de cantidade dependen dos atributos do produto en Dynamics 365. Ao configurar propiedades específicas para un produto, Project Operations permítelle marcar un subconxunto ou todas as propiedades como factores de cantidade.

Project Operations valida que só as propiedades numéricas ou propiedades de produto que teñen un tipo de datos numéricos estean marcadas como factores de cantidade. Cando engade un produto con factores de cantidade a unha liña de oferta, o campo **Cantidade** convértese en só de lectura. Despois de introducir valores para as propiedades do produto que son factores de cantidade, Project Operations calcula a cantidade da liña de oferta.

Por exemplo, Dynamics 365 Sales pode ter as seguintes propiedades:

- **N.º de usuarios**: O número de usuarios
- **Nº de meses**: O número de meses de subscrición
- **SKU de produto**

Pode marcar as propiedades **N.º de Usuarios** e **N.º de meses** como factores de cantidade editando as propiedades da liña de produtos.

Para crear factores de cantidade a partir das propiedades do produto, siga estes pasos:

1. No panel de navegación esquerdo de Project Operations, vaia a **Vendas** > **Produtos**.
2. Abra o produto para o que precisa configurar os factores de cantidade. Asegúrese de que o produto xa ten propiedades configuradas.
3. Na páxina **Información do proxecto** do produto, seleccione o separador **Factores de cantidade**.
4. Na subgrade, seleccione **+ Novo cálculo de campo**.
5. Introduza o nome do factor de cantidade e seleccione o valor da propiedade que se asigna ao cálculo de campo.
6. Garde e peche o formulario. Repita estes pasos para todas as propiedades que se empregarán para calcular a cantidade da liña de oferta baseada en produto.

Cando cree unha liña de oferta baseada en produto, bloquearase a cantidade da liña de oferta. A cantidade calcularase como produto dos valores da propiedade que introduciu para esa liña de oferta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]