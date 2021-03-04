---
title: Estimación dunha liña de oferta baseada en proxecto
description: Este tema ofrece información sobre como crear unha estimación nunha liña de oferta baseada en proxecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 56892a134c0c739958f7f939214930631dea7420
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180370"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimación dunha liña de oferta baseada en proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Unha liña de oferta baseada en proxecto ten detalles que axudan a estimar o custo e os ingresos potenciais do traballo implicado para entregar a liña de oferta.

Para estimar unha liña de oferta baseada en proxecto, na liña de oferta baseada en proxecto, seleccione o separador **Detalle da liña de oferta**. Hai dúas formas de crear unha estimación nunha liña de oferta baseada en proxecto:

- Crear manualmente a estimación directamente na liña de oferta empregando os detalles da liña de oferta 
- Cree un proxecto e un plan de proxecto e, a seguir, asocie o proxecto e as tarefas do proxecto á liña de oferta. Activarase o proceso para importar as estimacións do plan do proxecto á liña de oferta en función da información que proporcionou.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Crear estimacións directamente nunha liña de oferta baseada en proxecto

Para crear unha estimación nunha liña de oferta baseada en proxecto, seleccione o separador **Detalle da liña de oferta**. O elementos de liña que cree neste separador resumirá o valor ofertado para esta liña de oferta. 

Para crear detalles da liña de oferta, seleccione **+ Novo detalle de liña de oferta** na subgrade **Detalles de liña de oferta**. Abrirase un control deslizante de creación rápida. Os campos seguintes no formulario **Liña de oferta**:

| **Campo** | **Localización** | **Descrición** | **Impacto descendente** |
| --- | --- | --- | --- |
| Descripción | Creación rápida | Unha descrición da estimación específica. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Clase de transacción | Creación rápida | Esta lista despregable proporciona as clases de transaccións incluídas no separador **Xeral** da liña de oferta baseada en proxecto.  | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Rol | Creación rápida | A persoa que realizará este traballo ou incorrerá neste gasto. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Categoría | Creación rápida | Categoría do traballo ou gasto. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Data de inicio | Creación rápida | Data de inicio do traballo. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Data de finalización | Creación rápida | Data de finalización do traballo. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Unidade de recursos | Creación rápida | Unidade de recursos que incorrerá neste custo e proporcionará o recurso para traballar nel. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. Este campo tamén se usa na recuperación do prezo de custo. |
| Programa de unidades | Creación rápida | Grupo de unidades do traballo ou gasto. As unidades pertencen a un programa de unidades ou a un grupo de unidades. Por exemplo, as millas e quilómetros son unidades que pertencen a un grupo de unidades que describe a distancia. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Unidade | Creación rápida | Unidad do traballo ou gasto. | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Importe | Creación rápida | Cantidade do traballo ou gasto | Este campo é por defecto o detalle da liña de oferta relacionada para o custo que se crea automaticamente. |
| Prezo por unidade | Creación rápida | Taxa de facturación do rol que está a realizar o traballo ou o prezo de venda da categoría de gastos. Por defecto, este campo e Tempo baseándose na combinación de rol e unidade de recursos na lista de prezos do proxecto que estea vixente para a data de inicio. Para gastos, este campo é por defecto a configuración do prezo para a categoría de transaccións na lista de prezos do proxecto que estea vixente para a data de inicio. Se o método de fixación de prezos para a categoría de transaccións non é prezo por unidade, non é o predefinido, e este campo déixase en branco. | Taxa de custo do rol que está a realizar o traballo ou o custo por unidade da categoría de gastos. Por defecto, este campo e Tempo baseándose combinación de rol e unidade de recursos no prezo da unidade de contratación da lista de prezos da oferta que estea vixente para a data de inicio. Para gastos, este campo é por defecto a configuración do prezo para a categoría de transaccións na lista de prezo de custo da unidade de contratación que estea vixente para a data de inicio. Se o método de fixación de prezos para a categoría de transaccións non é prezo por unidade, non é o predefinido, e este campo déixase en branco. |
| Imposto estimado | Creación rápida | Pode introducir manualmente o imposto estimado por este traballo ou gasto. | Non hai ningún impacto descendente deste campo. |
| Importe  | Creación rápida | Pode introducir información manualmente neste campo se os campos **Cantidade** e **Prezo** se deixan en branco. Se estes campos non están en branco, este campo convértese en de só lectura e calcúlase como (Cantidade \* Prezo unitario) + Imposto. | Non hai ningún impacto descendente deste campo. |

## <a name="update-prices-on-quote-line-details"></a>Actualizar os prezos nos detalles da liña de oferta

Se cambiou os prezos na lista de prezos do proxecto que se xunta á oferta ou na lista de prezos de custo da unidade de contratación, pode seleccionar **Recalcular** na páxina **Oferta**, para actualizar os prezos nos detalles da liña de oferta individual para reflectir este cambio. Cando selecciona **Recalcular**, aparece unha advertencia que informa de que se restablecerán os prezos nos detalles da liña de oferta para todas as liñas de oferta desta oferta. Seleccione **Si** para actualizar os prezos dos detalles da liña de oferta de vendas e custo.

## <a name="access-quote-line-details-for-cost"></a>Acceder aos detalles da liña de oferta para custo

No separador **Detalles de liña de oferta**, seleccione unha fila na grade para activar algunhas accións na barra de ferramentas da subgrade. A primeira acción na barra de ferramentas da subgrade cando se selecciona un detalle de liña de oferta é **Abrir detalle de custo**. Seleccione **Abrir detalle de custo** para ver a taxa de custo relacionada e o importe desta liña de oferta.

> [!NOTE]
> Ao cambiar a unidade de recursos, a cantidade, as datas, o rol ou os valores da categoría no detalle da liña de oferta para custo cambiaranse os valores correspondentes nos detalles da liña de oferta para vendas.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moeda nos detalles da liña de oferta para custo e vendas

A moeda no detalle da liña de oferta para vendas é por defecto a da lista de prezos do proxecto que estea vixente para a data de inicio do detalle da liña de oferta.

A moeda no detalle da liña de oferta para custo é por defecto a da lista de prezos da unidade de contratación da oferta que estea vixente para a data de inicio do detalle da liña de oferta para custo.

Os cálculos de rendibilidade converten o importe dos detalles da liña de oferta para custo e vendas na moeda base do ambiente para informar da marxe global estimada na oferta.

Isto podería producir erros de redondeo de divisas e cambios de marxes debido á falta de taxas de cambio vixentes. Use estes cálculos nas ofertas do proxecto só como aproximacións e non informes legais ou doutro tipo que requiran maior precisión de redondeo e coñecemento da vixencia das datas para as taxas de cambio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]