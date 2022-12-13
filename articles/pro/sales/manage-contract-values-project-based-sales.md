---
title: Visión xeral das liñas de contrato do proxecto
description: Este artigo ofrece información sobre como traballar coas liñas de contrato do proxecto en Operacións do proxecto.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5a529233692a39b0674417cd4ea225e40243086
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824624"
---
# <a name="project-contract-lines-overview"></a>Visión xeral das liñas de contrato do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As liñas de contrato baseado en proxecto en Dynamics 365 Project Operations están deseñadas para manter os acordos de estimación e facturación de compoñentes específicos do traballo do proxecto nun compromiso. A estrutura dunha liña de contrato baseado en proxecto amplíase para estimacións de proxecto e escenarios de facturación cos seguintes conceptos:

- Método de facturación
- Asignación de tarefas e proxectos
- Clases de transaccións incluídas
- Límite non superable
- Configuración de imputabilidade.
- Estimacións utilizando os detalles da liña do contrato
- Cliente da liña de contrato

A seguinte táboa inclúe os campos do separador **Xeral** de liñas de contrato baseado en proxecto que axudan a establecer as bases para unha estimación detallada e completa e arranxos de facturación para o traballo baseado en proxecto.

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| **Nome** | Nome da liña de contrato. Isto identifica o compoñente discreto do contrato que se está a estimar. Para un contrato de proxecto creado a partir dunha oferta, este valor cópiase a partir dun valor correspondente da liña de oferta baseada en proxecto. | O nome copiado á liña de factura do proxecto que se crea a partir desta liña de contrato cando se crea a factura. |
| **Método de facturación** | Nun contrato de proxecto creado a partir dunha oferta, este valor cópiase a partir do campo correspondente da liña de oferta. Este é un conxunto de opcións que representa os dous principais modelos de contratación admitidos por Project Operations:</br>- **Prezo fixo**</br>- **Hora e material** | Baseado no método de facturación da liña de contrato referenciada, procesarase a transacción real. Se a liña de contrato á que fai referencia o dato real ten un método de facturación de tempo e material, e créanse rexistros de datos reais de custo e vendas non facturadas. Se a liña de contrato referenciada polo dato real ten un método de facturación de prezo fixo, só se crea un dato real de custo. |
| **Project** | Use este campo para identificar o proxecto que se usará para entregar o traballo neste compromiso. | Este valor usarase xunto con **Tarefas incluídas** e **Clases de transaccións incluídas** para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado. |
| **Tarefas incluídas** | Indica se esta liña de contrato inclúe todas as tarefas de proxecto para o proxecto seleccionado ou só un subconxunto das tarefas. Este é un conxunto de opcións que ten os seguintes valores posibles:</br>- **Todas as tarefas do proxecto**</br>- **Só as tarefas de proxecto seleccionadas**. Un valor en branco neste campo é igual a seleccionar **Todas as tarefas do proxecto**. | Se está seleccionado **Só tarefas seleccionadas**, pode seleccionar tarefas específicas e asocialas a esta liña de contrato no separador **Configuración de facturación de tarefas** na páxina **Proxecto**. O valor utilizarase xunto coas clases **Proxecto** e **Transacción incluída** para resolver a referencia da liña de contrato nun dato real ou un rexistro de liña estimado. |
| **Incluír tempo** | Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato as transaccións de tempo ou os custos laborais do proxecto seleccionado. O valor **Non** indica que as transaccións de tempo ou o custo laboral non se incluirán nesta liña de contrato. O valor **Si** indica que o farán. | Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado. |
| **Incluír gasto** | Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato os custos de gasto do proxecto seleccionado. O valor **Non** indica que o custo de gasto non se incluirá nesta liña de contrato. O valor **Si** indica que o farán. | Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado. |
| **Incluír materiais** | Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato os custos de material do proxecto seleccionado. Un valor **Non** indica que os custos de material non se incluirán nesta liña de contrato. O valor **Si** indica que o farán. | Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado. |
| **Incluír taxa** | Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato as taxas de gasto do proxecto seleccionado. O valor **Non** indica que as taxas non se incluirán nesta liña de contrato. O valor **Si** indica que o farán. | Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado. |
| **Importe contratado** | Nunha liña de contrato de prezo fixo, este importe é o valor acordado que se facturará ao cliente por todos os compoñentes de traballo asociados a esta liña de contrato. Nunha liña de contrato de tempo e material, este importe é un valor estimado do que se facturará ao cliente por todos os compoñentes de traballo asociados a esta liña de contrato. Nun contrato de proxecto que se crea a partir dunha oferta, este valor cópiase a partir do campo correspondente da liña de oferta. Cando unha liña de contrato baseado en proxecto ten detalles de liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de contrato. | Cando a liña de contrato ten detalles de liña, este valor pode modificarse cambiando os importes nos detalles da liña. Nunha liña de contrato de prezo fixo, este valor úsase para xerar o importe antes de impostos sobre os fitos periódicos de facturación. |
| **Imposto estimado** | O usuario pode editar este campo para introducir o importe do imposto estimado na liña de contrato. Cando unha liña de contrato baseado en proxecto ten detalles de liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de contrato. | Cando a liña de contrato ten detalles de liña, este valor pode modificarse cambiando os importes do imposto nos detalles da liña. Nunha liña de contrato de prezo fixo, este valor úsase para xerar o imposto sobre os fitos periódicos de facturación. |
| **Importe contratado despois de impostos** | O importe la liña de contrato despois de impostos. Este campo é de só lectura e calcúlase como **Importe contratado + Imposto**. | Nunha liña de contrato de prezo fixo, este valor úsase para xerar fitos periódicos de facturación. |
| **Límite non superable** | O usuario pode editar este campo e só está dispoñible en liñas de contrato baseado en proxecto que teñen un método de facturación de tempo e material establecido. | O usuario pode editar este campo. Cando un dato real de tempo e material fai referencia a esta liña de contrato por tempo e material, o importe real avalíase fronte ao límite non superable na liña de contrato. Esta avaliación complétase despois de contabilizar as cantidades xa gastadas e contabilizadas. |
| **Orzamento do cliente** | Este campo é editable e cópiase do campo correspondente na liña de oferta se o contrato se creou a partir dunha oferta. | Este campo só se usa para obter información e non ten ningunha importancia descendente. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regras de validación das opcións do separador Xeral das liñas de contrato baseado en proxecto

Regra 1: Se o campo **Tarefas incluídas** está en branco ou definido como **Todas as tarefas do proxecto**, todas as tarefas do proxecto están incluídas na liña de contrato.

Regra 2: Cando o campo **Tarefas incluídas** está en branco ou está definido de xeito explícito en **Todas as tarefas do proxecto**, un proxecto e unha determinada clase de transaccións só se poden incluír nunha liña de contrato baseado en proxecto dun contrato.

Regra 3: Cando o campo **Tarefas incluídas** está definido en **Só as tarefas do proxecto seleccionadas**, un proxecto e unha determinada clase de transaccións poden incluírse en varias liñas de contrato baseado en proxecto dun contrato.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contrato</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Liña de contrato</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Tarefas incluídas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluír tempo</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluír gasto</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Incluír materiais</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Incluír</strong>
                </p>
                <p>
                    <strong>Cota</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Válido/Non válido</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Motivo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 2. O tempo, os gastos, os materiais e as taxas do proxecto P1 inclúense nas dúas liñas de contrato CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 2. O tempo, os materiais e as taxas do proxecto P1 inclúense nas dúas liñas de contrato CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
O tempo, os materiais e as taxas do proxecto P1 inclúense en CL1.
                </p>
                <ul>
                    <li>
O gasto no proxecto P1 está incluído en CL2.
                    </li>
                </ul>
                <p>
Non hai superposición no incluído en cada liña de contrato e, polo tanto, é válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En branco </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 2 </p>
                <p>
C1 inclúe tempo, materiais, gastos e taxas nun subconxunto de tarefas do proxecto P1.
                </p>
                <p>
CL2 inclúe o tempo, os materiais, os gastos e as taxas para todo o proxecto P1 e, polo tanto, superponse co incluído en C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Segundo a regra n.º 3 </p>
                <p>
C1 inclúe tempo, gastos, materiais e taxas nun subconxunto de tarefas do proxecto P1.
                </p>
                <p>
CL2 inclúe tempo, gastos, materiais e taxas nun subconxunto de tarefas do proxecto P1.
                </p>
                <p>
A única validación adicional arredor do subconxunto de tarefas en CL1 é diferente do subconxunto de tarefas en CL2 para garantir que non haxa superposicións alí. O sistema faino cando as tarefas están asociadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="48" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
            <td width="42" valign="top">
                <p>
Si </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
