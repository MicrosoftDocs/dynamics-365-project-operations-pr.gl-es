---
title: Xestionar unidades complexas para liñas de contrato baseado en produto - lite
description: Este tema ofrece información sobre como apoiar a venda de produtos baseados en subscrición.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177374"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Xestionar unidades complexas para liñas de contrato baseado en produto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Dynamics 365 Project Operations usa factores de cantidade para apoiar a venda de produtos baseados en subscrición. Para os produtos baseados en subscrición, a cantidade na liña de contrato ou de contrato de proxecto exprésase como o número de meses de usuario.

O prezo do software de subscrición almacénase no catálogo como o prezo por usuario ao mes. Durante o proceso de vendas, o prezo na liña de contrato adoita ser o prezo por usuario, por mes que foi negociado e descontado polo axente de vendas. Cada acordo ten un número diferente de usuarios e un número diferente de meses de subscrición. A cantidade que se utiliza para calcular a cantidade da liña de contrato é un produto do número de usuarios e do número de meses de subscrición.

Para apoiar este tipo de venda, Project Operations admite o concepto de *factores de cantidade*. Os factores de cantidade dependen dos atributos do produto. Ao configurar propiedades específicas para un produto, pode marcar un subconxunto destas propiedades ou de todas as propiedades como factores de cantidade.

Project Operations valida que só as propiedades numéricas ou propiedades de produto que teñen un tipo de datos numéricos estean marcadas como factores de cantidade. Cando un produto con factores de cantidade configurados se engade a unha liña de contrato, o campo **Cantidade** convértese en só de lectura. Despois de introducir valores para as propiedades do produto que son factores de cantidade, Project Operations calcula a cantidade da liña de contrato.

Por exemplo, Dynamics 365 Sales pode ter as seguintes propiedades:

- **N.º de usuarios**: O número de usuarios.
- **Nº de meses**: O número de meses de subscrición.
- **SKU do produto**: A unidade de mantemento de stock (SKU) do produto.

As propiedades **N.º de Usuarios** e **N.º de meses** pódense marcar como factores de cantidade editando as propiedades da liña de produtos.

Para crear factores de cantidade a partir das propiedades do produto, complete os seguintes pasos.

1. En **Project Operations**, seleccione **Produtos de vendas**.
2. Abra o produto para o que precisa configurar factores de cantidade. Asegúrese de que o produto xa ten propiedades configuradas.
3. Na páxina **Información do proxecto**, seleccione o separador **Factores de cantidade**.
4. Na subgrade, seleccione **+ Novo cálculo de campo**.
5. Introduza o nome do **Factor de cantidade** e seleccione o valor da propiedade que se asigna ao cálculo de campo.
6. Garde e peche o formulario.
7. Repita os pasos 2-6 para todas as propiedades que xuntas constituirán a cantidade da liña de contrato baseado en produto.

Con factores de cantidade configurados, cando o usuario crea unha liña de contrato para este produto, a cantidade da liña de contrato está bloqueada. A cantidade calcúlase como produto dos valores da propiedade para esa liña de contrato.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]