---
title: Configurar compoñentes imputables dunha liña de contrato baseado en proxecto
description: Este tema ofrece información sobre como engadir compoñentes imputables a liñas de contrato en Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d18e56f29457151e07636b67ff8d9b184bf5014ef0ceeef9bb9d322672be4335
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003454"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurar compoñentes imputables dunha liña de contrato baseado en proxecto

_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_

Unha liña de contrato baseado en proxecto ten compoñentes *incluídos* e compoñentes *imputables*.

Os compoñentes incluídos son compoñentes suxeitos a:

  - Método de facturación e divisións de clientes
  - Límites non superables 
  - Configuración de frecuencia de facturas definida na liña de contrato baseado en proxecto

Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**. O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de contrato:

  - Imputable
  - Non imputable

Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.

A imputabilidade defínese nas tarefas dunha liña de contrato de proxecto e aplícase a todas as clases de transaccións incluídas na liña. Se o campo **Incluír tarefas** dunha liña de contrato está en branco ou definido como **Todo o proxecto**, o separador **Tarefas imputables** non estará dispoñible.

A imputabilidade definida nos roles dunha liña de contrato de proxecto só se aplica á clase de transacción **Tempo**. Se o campo **Incluír tempo** dunha liña de contrato está en branco ou definido como **Non**, o separador **Roles imputables** non estará dispoñible.

A imputabilidade definida nas categorías de transacción dunha liña de contrato de proxecto só se aplica á clase de transacción **Gasto**. Se o campo **Incluír gastos** dunha liña de contrato está en branco ou definido como **Non**, o separador **Categorías imputables** non estará dispoñible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualizar unha tarefa do proxecto como imputable ou non imputable

Unha tarefa de proxecto pode ser imputable ou non imputable nunha liña de contrato específica, o que fai posible a seguinte configuración:

Se inclúe unha liña de contrato baseado en proxecto inclúe **Tempo** e unha tarefa determinada, **T1** asóciase a ela como imputable. Se hai unha segunda liña de contrato que inclúa **Gasto**, pode asociar a tarefa T1 á liña de contrato como non imputable. O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos son non imputables.

O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** da liña de contrato actualizando o campo **Tipo de facturación** na subgrade de tarefas da liña de contrato. Como alternativa, pode actualizar o campo **Tipo de facturación** na subgrade da tarefa Configuración de facturación dun proxecto que mostra as liñas de contrato asociadas a unha tarefa.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualizar un rol do proxecto como imputable ou non imputable

Un rol pode ser imputable ou non imputable nunha liña de contrato específica.

O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de contrato. Para iso, actualice o campo **Tipo de facturación** na subgrade **Roles imputables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualizar unha categoría de transacción como imputable ou non imputable

Unha categoría de transacción pode ser imputable ou non imputable nunha liña de contrato específica.

O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de contrato baseado en proxecto. Para iso, actualice o campo **Tipo de facturación** na subgrade **Categorías imputables**.

### <a name="resolve-chargeability"></a>Resolver a imputabiidade

Unha estimación ou dato real creado para tempo só se considera imputable se:

   - **Tempo** está incluído na liña de contrato.
   - **Rol** está configurado como imputable na liña de contrato.
   - **Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña do contrato.
 
 Se estas tres cousas son certas, a tarefa configúrase como imputable. 

Unha estimación ou dato real creado para gasto só se considera imputable se:

   - **Gasto** está incluído na liña de contrato
   - **Categoría de transacción** está configurado como imputable na liña de contrato
   - **Tarefas incluídas** está establecido como **Tarefa seleccionada** na liña do contrato.
  
 Se estas tres cousas son certas, a **Tarefa** configúrase como imputable. 

Unha estimación ou dato real creado para material só se considera imputable se:

   - **Materiais** está incluído na liña de contrato
   - **Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña do contrato

Se estas dous cousas son certas, a **Tarefa** configúrase como imputable. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inclúe tempo</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inclúe gasto</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Inclúe materiais</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tarefas incluídas</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rol</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categoría</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tarefa</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impacto na imputabilidade</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o proxecto </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: <strong>Imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: <strong>Imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: Imputable </p>
                <p>
Tipo de facturación no dato real de material: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: <strong>Non imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o proxecto </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: Imputable </p>
                <p>
Tipo de facturación no dato real de material: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o proxecto </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non dispoñible</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o proxecto </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: Imputable </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Si </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o proxecto </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Non dispoñible</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o proxecto </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: Imputable </p>
                <p>
Tipo de facturación no dato real de gasto: Imputable </p>
                <p>
Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Si </p>
            </td>
            <td width="78" valign="top">
                <p>
Si </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o proxecto </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Non se pode configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de gasto: <strong>Non imputable</strong>
                </p>
                <p>
Tipo de facturación no dato real de material: <strong>Non dispoñible</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
