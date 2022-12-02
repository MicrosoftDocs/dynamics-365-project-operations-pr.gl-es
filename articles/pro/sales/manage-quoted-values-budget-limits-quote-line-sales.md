---
title: Visión xeral de liñas de oferta baseada en proxecto
description: Este artigo ofrece información sobre como liñas de oferta baseada en proxecto para o traballo do proxecto.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 90c5affa25b113476e43f0bbbadd5c9615f9c05c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934456"
---
# <a name="project-based-quote-lines-overview"></a>Visión xeral de liñas de oferta baseada en proxecto 

_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_

As liñas de oferta baseada en proxecto están deseñadas para axudar a estimar o traballo do proxecto nun compromiso. A estrutura dunha liña de oferta baseada en proxecto amplíase para as estimacións do proxecto cos seguintes conceptos:

- Método de facturación
- Asignación de tarefas e proxectos
- Clases de transaccións incluídas
- Límite non superable
- Configuración de imputabilidade.
- Estimación mediante detalles da liña de oferta
- Clientes da liña de oferta

A seguinte táboa ofrece información sobre os campos do separador **Xeral** da liña de oferta baseada en proxecto. Estes campos axudan a establecer as bases para unha estimación detallada e completa do traballo do proxecto.

| **Campo** | **Descrición** | **Impacto descendente** |
| --- | --- | --- |
| Nome | O nome da liña de oferta que lle axuda a identificar o compoñente discreto da oferta que se está a estimar. | Copiado á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Método de facturación | Nunha oferta creada a partir dunha oportunidade, este valor copiase desde campo correspondente na liña de oferta. Este campo inclúe os dous principais modelos de contratación admitidos por Dynamics 365 Project Operations:</br>- Prezo fixo</br>- Tempo e material.| Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Project | Use este campo opcional para identificar o proxecto que se usará para entregar o traballo neste compromiso. Cando un proxecto está asignado a unha liña de oferta, axuda a configurar tarefas imputables e tamén a traer unha estimación baseada no proxecto á liña de oferta como detalles da liña de oferta. Cando un proxecto non está asignado a unha liña de oferta baseada en proxecto, a estimación debe crearse manualmente creando cada detalle da liña de oferta. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.|
| Tarefas incluídas | Indica se esta liña de oferta se usa para todas ou algunhas das tarefas do proxecto seleccionado. Este campo ten os seguintes valores posibles:</br>- Todas as tarefas do proxecto</br>- Só tarefas do proxecto seleccionadas</br>Un valor en branco neste campo equivale á opción **Todas as tarefas do proxecto**. | Cando **Só tarefas do proxecto seleccionadas** está seleccionado na páxina do proxecto, o separador **Configuración de facturación de tarefas** permítelle seleccionar tarefas específicas para asocialas a esta liña de oferta. Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Incluír tempo | Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta as transaccións de tempo ou os custos laborais do proxecto seleccionado. O valor **Non** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado non se incluirán na estimación nesta liña de oferta. O valor **Si** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado se incluirán na estimación nesta liña de oferta. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Incluír gasto | Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta os custos de gasto do proxecto seleccionado. O valor **Non** indica que os custos de gastos do proxecto seleccionado non se incluirán na estimación nesta liña de oferta. O valor **Si** indica que os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Incluír material | Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta os custos de material do proxecto seleccionado. Un valor **Non** indica que os custos de material non se incluirán na estimación deste contrato. Un valor **Si** indica que os custos de material non se incluirán na estimación deste contrato. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Incluír taxa | Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta as taxas do proxecto seleccionado. O valor **Non** indica que as taxas do proxecto seleccionado non se incluirán na estimación nesta liña de oferta. O valor **Si** indica que as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Cantidade ofertada | Esta é a cantidade que se lle ofrecerá ao cliente por todo o traballo previsto nesta liña de oferta baseada en proxecto. Nunha oferta creada a partir dunha oportunidade, este valor copiase desde o campo **Orzamento do cliente** correspondente na liña de oportunidade. Cando a liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de oferta. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Imposto estimado | Este é un campo editable para que o usuario poida engadir o importe do imposto estimado na liña de oferta. Cando unha liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de oferta. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Importe da oferta despois de impostos | Este campo é o importe da liña de oferta despois do imposto e é só de lectura. O importe deste campo calcúlase como *Importe da oferta + Imposto*. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Límite non superable | Este campo é editable e só está dispoñible en liñas de oferta baseada en proxecto que teñan un método de facturación de **Tempo e material**. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Orzamento do cliente | Este campo é editable e cópiase desde o campo correspondente na liña de oferta se a oferta se creou a partir dunha oportunidade. | Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regras de validación para campos do separador Xeral das liñas de oferta baseada en proxecto

**Regra 1**: Se o campo **Tarefas incluídas** está en branco ou se está definido como **Todas as tarefas do proxecto**, inclúese un proxecto na liña de oferta.

**Regra 2**: Se o campo **Tarefas incluídas** campo está en branco ou se está definido como **Todas as tarefas do proxecto**, un proxecto e unha clase de transacción determinada só se poden incluír nunha liña de oferta baseada en proxecto dunha oferta.

**Regra 3**: Se o campo **Tarefas incluídas** campo está en branco ou se está definido como **Só as tarefas do proxecto seleccionadas**, un proxecto e unha clase de transacción determinada só se poden incluír en varias liñas de oferta baseada en proxecto dunha oferta.

**Regra 4**: Se unha oportunidade ten varias ofertas, pode haber liñas de oferta de diferentes ofertas que fan referencia ao mesmo proxecto e inclúen a mesma clase de transacción.

**Regra 5**: Se as ofertas non pertencen á mesma oportunidade, non poden incluír o mesmo proxecto e clase de transacción.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Oportunidade</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Oferta</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Liña de oferta</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Tarefas incluídas</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Incluír tempo</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Incluír gasto</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Incluír material</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Incluír</strong>
                </p>
                <p>
                    <strong>Cota</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Válido/Non válido</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Motivo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 2. O tempo, o gasto e as taxas do proxecto P1 inclúense nas liñas de oferta QL1 e QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 2. O tempo, o material e as taxas do proxecto P1 inclúense nas liñas de oferta QL1 e QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
O tempo, o material e as taxas do proxecto P1 inclúense en QL1 <br>
O gasto no proxecto P1 está incluído en QL2 <br>
Non hai superposición no incluído en cada liña de oferta e, polo tanto, é válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En branco </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 2 </p>
                <p>
Q1 inclúe tempo, material, gastos e taxas nun subconxunto de tarefas do proxecto P1. </p>
                <p>
QL2 inclúe tempo, gastos e taxas para todo o proxecto P1 e, polo tanto, solápase co incluído en Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Segundo a regra n.º 3 </p>
                <p>
Q1 inclúe tempo, material, gastos e taxas nun subconxunto de tarefas do proxecto P1.
                </p>
                <p>
QL2 inclúe tempo, material, gastos e taxas nun subconxunto de tarefas do proxecto P1.
                </p>
                <p>
A única validación adicional arredor do subconxunto de tarefas en QL1, que é diferente do subconxunto de tarefas en QL2 para garantir que non haxa superposición. O sistema faino cando as tarefas están asociadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Só tarefas seleccionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do proxecto ou en branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Segundo a regra n.º 5, Q1 e Q2 son dúas ofertas na mesma oportunidade, polo que ambas poden estimar para os mesmos compoñentes dun proxecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do proxecto ou en branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do proxecto ou en branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Segundo a regra n.º 4, Q1 e Q2 son dúas ofertas en oportunidades diferentes, polo que non poden estimar para os mesmos compoñentes dun proxecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do proxecto ou en branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Si </p>
            </td>
            <td width="46" valign="top">
                <p>
Si </p>
            </td>
            <td width="43" valign="top">
                <p>
Si </p>
            </td>
            <td width="41" valign="top">
                <p>
Si </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
