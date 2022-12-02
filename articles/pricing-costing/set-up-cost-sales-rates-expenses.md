---
title: Configurar taxas de custo e vendas para os gastos
description: Este artigo ofrece información sobre como configurar as taxas de custo e vendas para categorías de transaccións e gastos.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c503230348750af246f6ee7a4af1176d7bf22ba4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911870"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Configurar taxas de custo e vendas para os gastos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pode configurar os prezos de custo e de venda para categorías de transaccións en Dynamics 365 Project Operations. Debido a que os prezos de custo e vendas están deseñados para gastos, cada categoría de transaccións que os inclúa tamén debe configurarse como categoría de gastos. Esta configuración garante a precisión na funcionalidade descendente. Os prezos de custo e vendas para as categorías de transaccións só poden figurar nunha moeda, que debe ser a moeda da cabeceira da lista de prezos.

Para configurar as taxas de custo e vendas para as categorías de transaccións, complete os seguintes pasos. 

1. Vaia a **Vendas** > **Clientes** > **Listas de prezos**.
2. Seleccione **Nova** para crear unha nova lista de prezos. 
3. En **Prezos de categoría**, no menú da subgrade, seleccione **Novo prezo de categoría**. 
4. Na páxina **Creación rápida**, introduza a categoría de transaccións e a unidade para a que está a crear o novo prezo.

A seguinte táboa mostra os campos do separador **Xeral** e a páxina **Creación rápida** dunha liña de prezos de categoría que debe ter en conta ao crear prezos de categoría nunha lista de prezos de vendas ou de custo.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| Categoría da transacción | Separador **Xeral** e páxinas de **Creación rápida** | Seleccione a categoría de transacción para a que está a crear un prezo de vendas ou de custo. | A categoría de transacción da estimación entrante ou o dato real para gasto compararase con esta liña para predefinir a taxa de custo ou vendas da categoría de transacción. |
| Programación de unidades | Separador **Xeral** e páxinas de **Creación rápida** | A programación ea unidade é a predefinida na programación de unidade da categoría de transacción. | Non hai ningún impacto descendente deste campo. |
| Unidade | Separador **Xeral** e páxinas de **Creación rápida** | Seleccione a unidade para a que se establecen as taxas. | A unidade da estimación entrante ou o dato real compárase coa unidade desta liña para predefinir a taxa na estimación de gasto ou o dato real. |
| Método de cálculo de prezos | Separador **Xeral** e páxinas de **Creación rápida** | Os valores posibles do campo **Método de fixación de prezos** son **Prezo por unidade**, **Ao custo** e **Sobreprezo sobre o custo**. | Durante a configuración de prezos, ao seleccionar **Prezo por unidade** bloquéase o campo **Porcentaxe** na liña de prezo da categoría. Se se selecciona **Ao custo**, os campos **Prezo** e **Porcentaxe** están bloqueados na lista de prezos de vendas. Ao seleccionar **Sobreprezo sobre o custo** bloquéase o campo **Prezo** da lista de prezos de vendas. Nunha liña de dato real entrante para gasto, método de fixación de prezos **Ao custo** ou **Sobreprezo sobre o custo** dá como resultado que a liña de vendas sen facturar correspondente teña asignado un prezo igual ao prezo do dato real de custo ou se calcule como un aumento sobre o prezo. |
| Prezo | Separador **Xeral** e páxinas de **Creación rápida** | Configure unha taxa de unidade para a categoría de transacción e a combinación de unidades. Por exemplo, a taxa de quilometraxe é 10 USD por milla e 8 USD por quilómetro. | A taxa de quilometraxe será a taxa por defecto no prezo de unidade ou no custo da estimación entrante ou da liña de dato real para unha clase de transacción de gastos.|
| Porcentaxe | Separador **Xeral** e páxinas de **Creación rápida** | Configure unha porcentaxe sobre o custo para a categoría de transacción e a combinación de unidades. Por exemplo, a taxa de venda do billete aéreo debería marcarse un 10 por cento sobre o custo do gasto en billetes aéreos. | Esta porcentaxe sobre o custo só é aplicable nunha lista de prezos de vendas cando o método de fixación de prezos e **Sobreprezo sobre o custo**. |
| Moeda | Separador **Xeral** e páxinas de **Creación rápida** | Por defecto, este valor procede da moeda da cabeceira da lista de prezos. No prezo da categoría de transacción, a moeda non se pode anular. | Esta moeda predefinida é o prezo de unidade da liña de dato real entrante para a clase de transacción de gastos para custo e vendas. |

## <a name="pricing-methods-for-expenses"></a>Métodos de fixación de prezos para gastos

Cando configura prezos de categoría que só son relevantes no contexto dos prezos de gastos, pode empregar un dos tres métodos de prezos seguintes:

- **Prezo por unidade**
- **Ao custo**
- **Sobreprezo sobre o custo**

### <a name="price-per-unit"></a>Prezo por unidade
Cando se selecciona este método de fixación de prezos nunha liña de prezos de categoría ligada a unha lista de prezos de vendas, os valores predefinidos da combinación de categoría e unidade tanto na estimación como no dato real. A estimación refírese ás liñas de estimación do proxecto para gastos, o detalle de liña de oferta e o detalle da liña de contrato para gastos.

### <a name="at-cost"></a>Ao custo
Cando se selecciona este método de fixación de prezos nunha liña de prezos de categoría ligada a unha lista de prezos de vendas, os valores predefinidos da combinación de categoría e unidade só para o dato real de gasto. Por exemplo, os datos reais de vendas non facturadas para a clase de transacción de gastos. O prezo de unidade establécese dato real de vendas sen facturar a partir do prezo de unidade do dato real de custo para ese gasto. O prezo por defecto baseado no custo non se define nas estimacións do proxecto para gastos ou nos detalles da liña de oferta e a liña de contrato para gastos.

### <a name="markup-over-cost"></a>Sobreprezo sobre o custo
Cando se selecciona este método de fixación de prezos nunha liña de prezos de categoría ligada a unha lista de prezos de vendas, os valores predefinidos da combinación de categoría e unidade só para un dato real de gasto. Por exemplo, os datos reais de vendas non facturadas para a clase de transacción de gastos. Este prezo de unidade establécese no dato real de vendas sen facturar ata un valor calculado a partir do prezo de unidade so dato real de custo dese gasto despois de que se aplique a porcentaxe de sobreprezo definida. O prezo por defecto baseado no custo non se define nas estimacións do proxecto para gastos ou nos detalles da liña de oferta e a liña de contrato para gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
