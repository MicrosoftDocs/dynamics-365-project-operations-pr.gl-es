---
title: Visión xeral de liñas de oferta baseada en proxecto
description: Este tema ofrece información sobre como liñas de oferta baseada en proxecto para o traballo do proxecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181855"
---
# <a name="project-based-quote-lines-overview"></a>Visión xeral de liñas de oferta baseada en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

As liñas de oferta baseada en proxecto están deseñadas para axudar a estimar o traballo do proxecto nun compromiso. A estrutura dunha liña de oferta baseada en proxecto amplíase para as estimacións do proxecto cos seguintes conceptos:

- Método de facturación
- Asignación de proxectos
- Clases de transaccións incluídas
- Límite non superable
- Configuración de imputabilidade.
- Estimación mediante detalles da liña de oferta
- Clientes da liña de oferta

A seguinte táboa ofrece información sobre os campos do separador **Xeral** da liña de oferta baseada en proxecto. Estes campos axudan a establecer as bases para unha estimación detallada e completa do traballo do proxecto.

| **Campo** | **Descrición** | **Impacto descendente** |
| --- | --- | --- |
| Nome | O nome da liña de oferta que debería axudarlle a identificar o compoñente discreto da oferta que se estima. | Copiado á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Método de facturación | Nunha oferta creada a partir dunha oportunidade, este valor copiase desde campo correspondente na liña de oferta. Este campo inclúe os dous modelos de contratación principais admitidos por Dynamics 365 Project Operations:</br>- Prezo fixo</br>- Tempo e material.| Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Project | Use este campo opcional para identificar o proxecto que se usará para entregar o traballo neste compromiso. Cando un proxecto está asignado a unha liña de oferta, axuda a configurar tarefas imputables e tamén a traer unha estimación baseada no proxecto á liña de oferta como detalles da liña de oferta. Cando un proxecto non está asignado a unha liña de oferta baseada en proxecto, a estimación debe crearse manualmente creando cada detalle da liña de oferta. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Incluír tempo | O indicador **Si**/**Non** indica se as transaccións de tempo ou os custos laborais do proxecto seleccionado se incluirán na estimación nesta liña de oferta. O valor **Non** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado non se incluirán na estimación nesta liña de oferta. O valor **Si** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado se incluirán na estimación nesta liña de oferta. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Incluír gasto | O indicador **Si**/**Non** indica se os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta. O valor **Non** indica que os custos de gastos do proxecto seleccionado non se incluirán na estimación nesta liña de oferta. O valor **Si** indica que os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Incluír taxa | O indicador **Si**/**Non** indica se as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta. O valor **Non** indica que as taxas do proxecto seleccionado non se incluirán na estimación nesta liña de oferta. O valor **Si** indica que as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Cantidade ofertada | Esta é a cantidade que se ofertará ao cliente por todo o traballo previsto nesta liña de oferta baseada en proxecto. Nunha oferta creada a partir dunha oportunidade, este valor copiase desde o campo **Orzamento do cliente** correspondente na liña de oportunidade. Cando a liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de oferta. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Imposto estimado | Este é un campo editable para que o usuario poida engadir o importe do imposto estimado na liña de oferta. Cando unha liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de oferta. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Importe da oferta despois de impostos | Este campo é o importe da liña de oferta despois do imposto e é só de lectura. O importe deste campo calcúlase como *Importe da oferta + Imposto*. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Límite non superable | Este campo é editable e só está dispoñible en liñas de oferta baseada en proxecto que teñan un método de facturación de **Tempo e material**. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |
| Orzamento do cliente | Este campo é editable e cópiase desde o campo correspondente na liña de oferta se a oferta se creou a partir dunha oportunidade. | Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regras de validación para campos do separador Xeral das liñas de oferta baseada en proxecto

**Regra 1**: Unha determinada clase de transacción no proxecto seleccionado só se pode incluír nunha liña de oferta baseada en proxecto dunha oferta.

**Regra 2**: Se unha oportunidade ten varias ofertas, pode haber liñas de oferta de diferentes ofertas que fan referencia ao mesmo proxecto e inclúen a mesma clase de transacción.

**Regra 3**: Se as ofertas non pertencen á mesma oportunidade, non poden incluír o mesmo proxecto e clase de transacción.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Oportunidade</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Oferta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Liña de oferta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
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
                    <strong>Incluír</strong>
                </p>
                <p>
                    <strong>taxa</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Válido/Non válido</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Motivo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 1. O tempo, o gasto e as taxas do proxecto P1 inclúense nas dúas liñas de oferta, QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 1. O tempo e as taxas do proxecto P1 inclúense nas dúas liñas de oferta, QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
O tempo e as taxas do proxecto P1 están incluídos en QL1.
O gasto no proxecto P1 está incluído en QL2.
Non hai superposición no que se inclúe en cada liña de oferta, polo que é válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Non válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracción da regra n.º 1. anterior </p>
                <p>
Q1 inclúe o tempo, os gastos e as taxas para todo o proxecto P1.
                </p>
                <p>
QL2 inclúe tempo, gastos e taxas para todo o proxecto P1 e superponse co incluído en Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Segundo a regra n.º 2, Q1 e Q2 son dúas ofertas da mesma oportunidade, polo que ambas poden estimar para os mesmos compoñentes dun proxecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 en Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Segundo a regra n.º 3, Q1 e Q2 son dúas ofertas de diferentes oportunidades, polo que non poden estimar para os mesmos compoñentes do mesmo proxecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Non válido </p>
            </td>
        </tr>
    </tbody>
</table>

