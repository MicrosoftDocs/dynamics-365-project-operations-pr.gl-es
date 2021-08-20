---
title: Estimar unha estimación a unha liña de contrato baseado en proxecto - lite
description: Este tema ofrece información sobre a estimación dunha liña de contrato baseado en proxecto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 747a1abe5630cac3dc074eba3a469d8d858c5ef244b59e26921e35afa61645df
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999089"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimar unha estimación a unha liña de contrato baseado en proxecto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Dynamics 365 Project Operations, unha liña de contrato baseado en proxecto ten detalles que axudan a estimar o custo e os ingresos potenciais do traballo implicado para entregar a liña de contrato.

Para estimar unha liña de contrato baseado en proxecto, vaia ao separador **Detalle da liña de contrato** na **Liña de contrato** baseado en proxecto.  Hai dúas formas de crear unha estimación nunha liña de contrato baseado en proxecto:

   - Cree unha estimación directamente na liña de contrato engadindo manualmente os detalles da liña de contrato.
   - Cree un proxecto e un plan de proxecto e, a seguir, asocie o proxecto e as tarefas á liña de contrato de proxecto. Isto activa o proceso mediante o cal pode importar a estimación do plan de proxecto á liña de contrato en función dos compoñentes incluídos na liña de contrato.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Crear unha estimación directamente nunha liña de contrato baseado en proxecto

Para crear unha estimación directamente nunha liña de contrato baseada en proxecto, siga estes pasos:

1. Vaia á liña do contrato e seleccione o separador **Detalle da liña do contrato**. As liñas que cree neste separador resúmense e móstranse como **Valor contratado** para esta **Liña de contrato**. 
2. Na subgrade **Detalles de liña de contrato**, seleccione **Novo detalle de liña de contrato**. Ábrese unha barra de desprazamento de creación rápida. Os seguintes campos están dispoñibles na páxina **Detalles de liña de contrato**.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| **Descrición** | **Creación rápida** | Unha descrición da estimación específica. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Clase de transacción** | **Creación rápida** | Esta é unha lista de clases de transacción incluída no separador **Xeral** da liña de contrato baseada en proxecto. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Seleccionar produto** | **Creación rápida** | Aplícase cando a clase de transacción é **Material**. Pode especificar se esta liña de estimación é para un produto **Existente** (catálogo) ou un produto **Fóra de catálogo**. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Produto** | **Creación rápida** | O ID do produto do catálogo de produtos. Este campo só está activado cando selecciona **Produto existente** no campo **Seleccionar produto**. O ID úsase para recuperar o prezo de venda da lista de prezos do proxecto no contrato. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Produto fóra de catálogo** | **Creación rápida** | Un campo de texto para introducir o nome do produto. Este campo só está activado cando selecciona **Fóra de catálogo** no campo **Seleccionar produto**.| Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Rol** | **Creación rápida** | O rol da persoa que realiza este traballo ou incorre neste gasto. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente.|
| **Categoría** | **Creación rápida** | A categoría do traballo ou gasto. |Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente.|
| **Data de inicio** | **Creación rápida** | Data de inicio do traballo. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Data de fin** | **Creación rápida** | Data de finalización do traballo. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Unidade de recursos** | **Creación rápida** | A unidade de recursos que incorre neste custo e proporciona o recurso para traballar nel. |Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente e se utiliza na recuperación do prezo de custo. |
| **Programa de unidades** | **Creación rápida** | O grupo de unidades do traballo, produto ou gasto. As unidades pertencen a un programa de unidades ou a un grupo de unidades. Por exemplo, *millas* e *quilómetros (km)* son unidades que pertencen a un grupo de unidades que describen a distancia. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Unidade** | **Creación rápida** | A unidade de traballo, produto ou gasto. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Importe** | **Creación rápida** | A cantidade de traballo, produto ou gasto. | Este valor é por defecto o detalle da liña de contrato relacionado para o custo que se crea automaticamente. |
| **Prezo por unidade** | **Creación rápida** | A taxa de facturación do rol que está a realizar o traballo, o prezo unitario do produto ou o prezo de venda do produto ou a categoría de gasto. Este campo está predefinido para **Tempo** segundo a combinación de valores de dimensión de prezos na liña de prezo do rol da lista de prezos do proxecto que está vixente na data de inicio. Para **Gastos**, o valor predefinido deste campo é o da configuración de prezos para a categoría de transacción da lista de prezos de proxecto que é efectiva para a data de inicio. Se o método de fixación de prezos para a categoría de transaccións non é **prezo por unidade**, non é o predefinido, e este campo déixase en branco. Para produtos, o valor predefinido deste campo baséase na liña **Elemento de lista de prezos** da lista de prezos do proxecto que está vixente na data de inicio.| A taxa de custo do rol que está a realizar o traballo, ou o custo por unidade da categoría de gasto ou o custo unitario do produto. Este campo está predefinido para **Tempo** segundo a combinación de valores de dimensión de prezos na liña de prezo da lista de prezos de custo anexo á unidade de contratación que está vixente na data de inicio. Para gastos, o valor predefinido deste campo baséase na liña de prezo de categoría de lista de prezos de custo para a unidade contratante que é efectiva para a data de inicio. Se o método de fixación de prezos para a categoría de transaccións non é prezo por unidade, non é o predefinido, e este campo déixase en branco. Para produtos, o valor predefinido deste campo baséase na liña **Elemento de lista de prezos** da lista de prezos de custo anexa á unidade de contratación que está vixente na data de inicio.|
| **Imposto estimado** | **Creación rápida** | O imposto estimado por este traballo ou gasto. | O imposto estimado por este traballo ou gasto. |
| **Importe** | **Creación rápida** | Pode engadir o valor neste campo se os campos **Cantidade** e **Prezo** quedan en branco. Se se enchen **Cantidade** e **Prezo**, o campo **Cantidade** é de só lectura e calcúlase como **(Cantidade \* Prezo unitario) + Imposto**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Actualizar os prezos nos detalles da liña do contrato

Se cambia os prezos na lista de prezos da proxecto que se anexa ao contrato ou na lista de prezos de custo da unidade contratante, pode actualizar os prezos nos detalles da liña de contrato individual para reflectir o cambio. Na páxina **Contrato**, seleccione **Calcular de novo**. Aparece un aviso para informarlle de que se restablecen os prezos de todas as liñas de contrato deste contrato. Seleccione **Si** para actualizar os prezos tanto de venda como dos detalles da liña de contrato.

## <a name="access-contract-line-details-for-cost"></a>Acceder aos detalles de liña de contrato para custo

No separador **Detalles de liña de contrato**, seleccione unha fila na grade para mostrar accións na barra de ferramentas da subgrade. A primeira acción na barra de ferramentas da subgrade é **Abrir detalle de custo**. Para ver a taxa de custo e o importe relacionados para este detalle de liña de contrato, seleccione **Abrir detalle de custo**. 

> [!NOTE]
> Cambiar os valores da empresa de recursos, da unidade de recursos, da cantidade, das datas, do rol ou dos valores da categoría no detalle da liña de contrato para **Custo** tamén cambia os valores correspondentes no detalle da liña de contrato para **Vendas**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moeda nos detalles da liña de contrato para custo e vendas

O detalle da liña de contrato para **Vendas** define a moeda por defecto da lista de prezos de proxecto que é efectiva para a data de inicio do detalle da liña de contrato.

O detalle da liña de contrato para **Custo** define a moeda por defecto da lista de prezos da unidade contratante do contrato que é efectiva para a data de inicio do detalle da liña de contrato para **Custo**.

Os cálculos de rendibilidade converten os importes dos detalles da liña de contrato para **Custo** e **Vendas** na moeda base do ambiente para informar das marxes xerais reais e estimadas do contrato.

> [!NOTE]
> Os erros de redondeo de moeda e as marxes modificadas poden producirse debido á falta de tipos de cambio con data efectiva. Utilice estes cálculos só nos contratos de proxecto, xa que son aproximacións e non son para informes legais ou doutro tipo que requiran maior precisión de redondeo e coñecemento da efectividade da data para os tipos de cambio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
