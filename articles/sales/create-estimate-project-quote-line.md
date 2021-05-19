---
title: Estimar unha liña de oferta de proxecto
description: Este tema ofrece información sobre como crear unha estimación nunha liña de oferta de proxecto.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858786"
---
# <a name="estimate-a-project-quote-line"></a>Estimar unha liña de oferta de proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Unha liña de oferta baseada en proxecto ten detalles que axudan a estimar o custo e os ingresos potenciais do traballo implicado para entregar a liña de oferta.

Para estimar unha liña de oferta baseada en proxecto, na liña de oferta, seleccione o separador **Detalle de liña de oferta**. Hai dúas formas de crear unha estimación nunha liña de oferta baseada en proxecto:

   - Crear manualmente a estimación directamente na liña de oferta empregando os detalles da liña de oferta. 
   - Cree un proxecto e un plan de proxecto e, a seguir, asocie o proxecto e as tarefas do proxecto á liña de oferta. Activarase o proceso para importar as estimacións do plan do proxecto á liña de oferta en función da información que proporcionou.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Crear estimacións directamente nunha liña de oferta baseada en proxecto

Para crear estimacións directamente nunha liña de oferta baseada en proxecto, siga estes pasos:

1. Para crear unha estimación nunha liña de oferta baseada en proxecto, seleccione o separador **Detalle da liña de oferta**. O elementos de liña que cree neste separador resumirá o valor ofertado para esta liña de oferta. 
2. Para crear detalles da liña de oferta, seleccione **Novo detalle de liña de oferta** na subgrade **Detalles de liña de oferta**. Abrirase un control deslizante de creación rápida. Os seguintes campos da páxina **Liña de oferta**.

| **Campo** | **Localización** | **Descrición** | **Impacto descendente** |
| --- | --- | --- | --- |
| Descripción | Creación rápida | Unha descrición da estimación específica. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Clase de transacción | Creación rápida | Esta lista despregable proporciona as clases de transaccións incluídas no separador **Xeral** da liña de oferta baseada en proxecto.  | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Seleccionar produto | Creación rápida | Aplícase cando a clase de transacción é **Material**. Pode seleccionar para especificar que esta liña de estimación é para un produto **Existente** (catálogo) ou un produto **Fóra de catálogo**. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Produto | Creación rápida | O ID do produto do catálogo de produtos. Este campo só está activado cando selecciona **Existente** no campo **Seleccionar produto**. O ID úsase para recuperar o prezo de venda da lista de prezos do proxecto na oferta. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Produto fóra de catálogo | Creación rápida | Unha caixa de texto para escribir o nome do produto. Este campo só está activado cando selecciona **Fóra de catálogo** no campo **Seleccionar produto**.| Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Rol | Creación rápida | O rol da persoa que realizará este traballo ou incorrerá neste gasto. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Categoría | Creación rápida | A categoría do traballo ou gasto. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Data de inicio | Creación rápida | Data de inicio do traballo. | Este campo é por defecto o detalle da liña de oferta para o custo que se crea automaticamente. |
| Data de finalización | Creación rápida | Data de finalización do traballo. | Este campo é por defecto o detalle da liña de oferta para o custo que se crea automaticamente. |
| Empresa de recursos | Creación rápida | A empresa ou entidade legal de recursos que incorre neste custo e proporciona o recurso para traballar nel. | O valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente e se utiliza na recuperación do prezo de custo. |
| Unidade de recursos | Creación rápida | A unidade de recursos que incorre neste custo e proporciona o recurso para traballar nel. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente e se utiliza na recuperación do prezo de custo. |
| Programa de unidades | Creación rápida | O grupo de unidades do traballo, produto ou gasto. As unidades pertencen a un programa de unidades ou a un grupo de unidades. Por exemplo, millas e quilómetros (km) son unidades que pertencen a un grupo de unidades que describe a distancia. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Unidade | Creación rápida | A unidade do traballo, produto ou gasto. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Importe | Creación rápida | A cantidade de traballo, produto ou gasto. | Este valor é por defecto o detalle da liña de oferta relacionado para o custo que se crea automaticamente. |
| Prezo por unidade | Creación rápida |A taxa de facturación do rol que está a realizar o traballo, o prezo unitario do produto ou o prezo de venda do produto ou a categoría de gasto. O valor por defecto para **Tempo** baséase na combinación de valores de dimensión de prezos na liña de prezo do rol da lista de prezos do proxecto que está vixente na data de inicio. Para **Gastos**, o valor predefinido é o da configuración de prezos para a categoría de transacción da lista de prezos de proxecto que é efectiva para a data de inicio. Se o método de fixación de prezos para a categoría de transaccións non é prezo por unidade, non é o predefinido, e este campo déixase en branco. Para produtos, o valor predefinido deste campo baséase na liña **Elemento de lista de prezos** da lista de prezos do proxecto que está vixente na data de inicio.| A taxa de custo do rol que está a realizar o traballo, o custo por unidade da categoría de gasto ou o custo unitario do produto. O valor predefinido para **Tempo** baséase na combinación de valores de dimensión de prezos na liña de prezo da lista de prezos de custo anexo á unidade de contratación que está vixente na data de inicio. Para gastos, o valor por defecto baséase na liña de prezo de categoría da lista de prezos de custo anexa á unidade de contratación que está vixente na data de inicio. Se o método de fixación de prezos para a categoría de transacción non é o prezo por unidade, non hai valor predefinido e este campo queda en branco. Para produtos, o valor predefinido deste campo baséase na liña **Elemento de lista de prezos** da lista de prezos de custo anexa á unidade de contratación que está vixente na data de inicio.|
| Imposto estimado | Creación rápida | Pode introducir manualmente o imposto estimado por este traballo ou gasto. | Non hai ningún impacto descendente para este campo. |
| Importe | Creación rápida | Pode introducir información manualmente neste campo se os campos **Cantidade** e **Prezo** se deixan en branco. Se estes campos non están en branco, este campo convértese en de só lectura e calcúlase como (Cantidade \* Prezo unitario) + Imposto. | Non hai ningún impacto descendente para este campo. |

## <a name="update-prices-on-quote-line-details"></a>Actualizar os prezos nos detalles da liña de oferta

Se cambiou os prezos na lista de prezos do proxecto que se xunta á oferta ou na lista de prezos de custo da unidade de contratación, pode seleccionar **Recalcular** na páxina **Oferta**, para actualizar os prezos nos detalles da liña de oferta individual para reflectir este cambio. Cando selecciona **Recalcular** aparece un aviso que informa de que se restablecerán os prezos dos detalles da liña de oferta para todas as liñas de oferta desta oferta. Seleccione **Si** para actualizar os prezos dos detalles da liña de oferta de vendas e custo.

## <a name="access-quote-line-details-for-cost"></a>Acceder aos detalles da liña de oferta para custo

Para acceder aos detalles da liña de oferta para o custo, siga estes pasos:

1. No separador **Detalles da liña de oferta**, seleccione unha fila na grade para activar as accións na barra de ferramentas da subgrade. 
2. Seleccione **Abrir detalle de custo** para ver a taxa de custo relacionada e o importe desta liña de oferta.

> [!NOTE]
> Ao cambiar a unidade de recursos, a cantidade, as datas, o rol ou os valores da categoría no detalle da liña de oferta para custo cambiaranse os valores correspondentes nos detalles da liña de oferta para vendas.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moeda nos detalles da liña de oferta para custo e vendas

A moeda no detalle da liña de oferta para os valores predefinidos de venda da lista de prezos do proxecto que está vixente na data de inicio do detalle da liña de oferta.

A moeda no detalle da liña de oferta para os valores predefinidos de custo da lista de prezos da unidade de contratación da oferta que está vixente na data de inicio do detalle da liña de oferta para custo.

> [!NOTE]
> Os cálculos de rendibilidade converten o importe dos detalles da liña de oferta para custo e vendas na moeda base do ambiente para informar da marxe global estimada na oferta. Os erros de redondeo de moeda e as marxes modificadas poden producirse debido á falta de tipos de cambio con data efectiva. Utilice estes cálculos só nas ofertas de proxecto, xa que son aproximacións e non son para informes legais ou doutro tipo que requiran maior precisión de redondeo e coñecemento da efectividade da data para os tipos de cambio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]