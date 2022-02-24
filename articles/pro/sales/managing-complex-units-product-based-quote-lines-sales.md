---
title: Xestión de unidades complexas como por usuario, por mes para as liñas de oferta baseadas en produto - lite
description: Este tema ofrece información sobre a xestión de unidades complexas para liñas de oferta baseadas en produto.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272881"
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