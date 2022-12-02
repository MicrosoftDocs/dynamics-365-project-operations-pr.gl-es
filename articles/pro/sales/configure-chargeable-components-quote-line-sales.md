---
title: Configurar os compoñentes imputables dunha liña de oferta
description: Este artigo ofrece información sobre a configuración de compoñentes imputables e non imputables nunha liña de oferta baseada en proxecto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4829055f429546c7911a05a765bc28ae085afa1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930040"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurar os compoñentes imputables dunha liña de oferta 

_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_

Unha liña de oferta baseada en proxecto ten o concepto de compoñentes *incluídos* e compoñentes *imputables*.

Os compoñentes incluídos están suxeitos a:

  - Método de facturación e divisións de clientes
  - Límites non superables 
  - Configuración de frecuencia de facturas definida na liña de oferta baseada en proxecto

Un subconxunto dos compoñentes incluídos pódese marcar como imputable mediante o campo **Tipo de facturación**. O campo **Tipo de facturación** é un conxunto de opcións que permite os seguintes valores no contexto dunha liña de oferta:

  - Imputable
  - Non imputable

Os compoñentes imputables poden definirse en tarefas, roles e categorías de transacción.

A imputabilidade defínese nas tarefas dunha liña de oferta de proxecto e aplícase a todas as clases de transaccións incluídas nesa liña. Se o campo **Incluír tarefas** dunha liña de contrato está definido como **Todo o proxecto** ou se deixa en branco, o separador **Tarefas imputables** non está dispoñible.

A imputabilidade defínese nos roles dunha liña de oferta de proxecto só se aplica á clase de transacción **Tempo**. Se o campo **Incluír tempo** está definido como **Non** nunha liña de oferta de proxecto, o separador **Roles imputables** non está dispoñible.

A imputabilidade defínese nas categorías de transacción dunha liña de oferta de proxecto e só se aplica á clase de transacción **Gasto**. Se o campo **Incluír gastos** está definido como **Non** nunha liña de oferta de proxecto, o separador **Categorías imputables** non está dispoñible.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Actualizar unha tarefa de proxecto para que sexa imputable ou non imputable

Unha tarefa de proxecto pode ser imputable ou non imputable no contexto dunha liña de oferta baseada en proxecto específica, o que fai posible a seguinte configuración.

Se unha liña de oferta baseada en proxecto inclúe **Tempo** e a tarefa **T1**, a tarefa está asociada á liña de oferta como imputable. Se hai unha segunda liña de oferta que inclúa **Gasto**, pode asociar a tarefa **T1** á liña de oferta como non imputable. O resultado é que todo o tempo rexistrado na tarefa é imputable e todos os gastos rexistrados na tarefa son non imputables.

O tipo de facturación dunha tarefa pódese configurar no separador **Tarefas imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Tarefas da liña de oferta**. Como alternativa, pode actualizar o tipo de facturación para unha tarefa de proxecto no campo **Tipo de facturación** na subgrade na configuración de facturación de tarefas que mostra as liñas de oferta asociadas a unha tarefa.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizar un rol para que sexa imputable ou non imputable

Un rol pode ser imputable ou non imputable no contexto dunha liña de oferta específica baseada en proxecto.

O tipo de facturación dun rol pódese configurar no separador **Roles imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Roles imputables**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizar unha categoría de transacción para que sexa imputable ou non imputable

Unha categoría de transacción pode ser imputable ou non imputable nunha liña de oferta específica.

O tipo de facturación dunha transacción pódese configurar no separador **Categorías imputables** dunha liña de oferta baseada en proxecto actualizando o campo **Tipo de facturación** na subgrade **Categorías imputables**.

### <a name="resolve-chargeability"></a>Resolver a imputabiidade
Unha estimación ou dato real creado para tempo só se considerará imputable se:

   - **Tempo** está incluído na liña de oferta.
   - **Rol** está configurado como imputable na liña de oferta.
   - **Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta. 

Se estas tres cousas son certas, a **Tarefa** configúrase tamén como imputable. 

Unha estimación ou dato real creado para gasto só se considera imputable se: 

   - **Gasto** está incluído na liña de oferta.
   - **Categoría de transacción** está configurado como imputable na liña de oferta.
   - **Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.

Se estas tres cousas son certas, a **Tarefa** configúrase tamén como imputable. 

Unha estimación ou dato real creado para material só se considerará imputable se:

   - **Materiais** está incluído na liña de oferta.
   - **Tarefas incluídas** está establecido como **Tarefas seleccionadas** na liña de oferta.

Se estas dúas cousas son certas, a **Tarefa** debería configurarse tamén como imputable. 


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
Facturación nun dato real de tempo: Imputable </p>
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
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación nun dato real de tempo: Imputable </p>
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
