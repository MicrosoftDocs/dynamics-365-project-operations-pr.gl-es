---
title: Traballar con liñas de contrato baseado en proxecto
description: Este tema ofrece información sobre as liñas de contrato baseado en proxecto.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990044"
---
# <a name="work-with-projectbased-contract-lines"></a>Traballar con liñas de contrato baseado en proxecto

As liñas de contrato baseado en proxecto en Dynamics 365 Project Operations están deseñadas para manter os acordos de estimación e facturación de compoñentes específicos do traballo do proxecto nun compromiso. A estrutura dunha liña de contrato baseado en proxecto amplíase para estimacións de proxecto e escenarios de facturación cos seguintes conceptos:

- Método de facturación
- Asignación de tarefas e proxectos
- Clases de transaccións incluídas
- Límite non superable
- Configuración de imputabilidade.
- Estimacións utilizando os detalles da liña do contrato
- Cliente da liña de contrato

Os seguintes campos están incluídos no separador **Xeral** das liñas de contrato baseado en proxecto. Estes campos axudan a establecer a base para unha estimación detallada e completa e os arranxos de facturación do traballo baseado en proxecto.

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| **Nome** | O nome da liña de contrato que identifica o compoñente discreto do contrato que se está a estimar. Para un contrato de proxecto creado a partir dunha oferta, este valor cópiase a partir dun valor correspondente da liña de oferta baseada en proxecto. | Este valor de campo cópiase na liña de factura do proxecto que se crea a partir desta liña de contrato cando se crea a factura. |
| **Método de facturación** | Nun contrato de proxecto creado a partir dunha oferta, este valor cópiase a partir do campo correspondente da liña de oferta. Este é un conxunto de opcións que representa os dous principais modelos de contratación admitidos por Project Operations:</br>- **Prezo fixo**</br>- **Hora e material** | Baseado no método de facturación da liña de contrato referenciada, procesarase a transacción real. Se a liña de contrato á que fai referencia o dato real ten un método de facturación de tempo e material, e créanse un custo e un rexistro de dato real de vendas non facturadas. Se a liña de contrato referenciada polo dato real ten un método de facturación de prezo fixo, só se crea un dato real de custo. |
| **Project** | Use este campo para identificar o proxecto que se usará para entregar o traballo neste compromiso. | O valor deste campo úsase xunto cos dos campos **Tarefas incluídas** e **Clases de transaccións incluídas** para resolver a referencia da liña de contrato nun dato real ou un rexistro de liña estimado. |
| **Incluír tempo** | Unha bandeira indica se se inclúen nesta liña de contrato as transaccións de tempo ou os custos laborais do proxecto seleccionado. O valor **Non** indica que as transaccións de tempo ou os custos laborais non se incluirán nesta liña de contrato. O valor **Si** indica que o farán. | Este valor de campo úsase xunto co proxecto para resolver a referencia da liña de contrato nun dato real ou un rexistro de liña de estimación. |
| **Incluír gasto** | Unha bandeira indica se se incluirán nesta liña de contrato os custos de gastos do proxecto seleccionado. O valor **Non** indica que o custo de gasto non se incluirá nesta liña de contrato. O valor **Si** indica que o farán. | Este valor de campo úsase xunto co proxecto para resolver a referencia da liña de contrato nun dato real ou un rexistro de liña de estimación. |
| **Incluír taxa** | Unha bandeira indica se se incluirán nesta liña de contrato as taxas do proxecto seleccionado. O valor **Non** indica que as taxas non se incluirán nesta liña de contrato. O valor **Si** indica que o farán. | Este valor de campo úsase xunto co proxecto para resolver a referencia da liña de contrato nun dato real ou un rexistro de liña de estimación. |
| **Importe contratado** | Nunha liña de contrato de prezo fixo, este é o valor acordado que se facturará ao cliente por todos os compoñentes de traballo asociados a esta liña de contrato. Nunha liña de contrato de tempo e material, este importe é un valor estimado do que se facturará ao cliente por todos os compoñentes de traballo asociados a esta liña de contrato. Nun contrato de proxecto que se crea a partir dunha oferta, este valor cópiase a partir do campo correspondente da liña de oferta. Cando unha liña de contrato baseado en proxecto ten detalles de liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de contrato. | Cando a liña de contrato ten detalles de liña, este valor pode modificarse cambiando os importes nos detalles da liña. Nunha liña de contrato de prezo fixo, este valor úsase para xerar o importe antes de impostos sobre os fitos periódicos de facturación. |
| **Imposto estimado** | O usuario pode editar este campo para introducir o importe do imposto estimado na liña de contrato. Cando unha liña de contrato baseado en proxecto ten detalles de liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de contrato. | Cando a liña de contrato ten detalles de liña, este valor pode modificarse cambiando os importes do imposto nos detalles da liña. Nunha liña de contrato de prezo fixo, este valor úsase para xerar impostos sobre os fitos periódicos de facturación. |
| **Importe contratado despois de impostos** | O importe la liña de contrato despois de impostos. Este campo é de só lectura e calcúlase como **Importe contratado + Imposto**. | Nunha liña de contrato de prezo fixo, este valor úsase para xerar fitos periódicos de facturación. |
| **Límite non superable** | O usuario pode editar este campo e só está dispoñible en liñas de contrato baseado en proxecto que teñen un método de facturación de tempo e material. | O usuario pode editar este campo. Cando un dato real de tempo ou gasto fai referencia a esta liña de contrato por tempo e material, o importe real avalíase fronte ao límite non superable nesta liña de contrato despois de contabilizar os importes xa gastados e comprometidos. |
| **Orzamento do cliente** | Este campo é editable e cópiase do campo correspondente na liña de oferta, se o contrato se creou a partir dunha oferta. | Este campo só se usa para obter información e non ten ningunha importancia descendente. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regra de validación das opcións do separador Xeral das liñas de contrato baseado en proxecto

Regra: Un proxecto e unha clase de transacción determinada só se poden incluír nunha liña de contrato baseado en proxecto nun contrato.

| Contrato | Liña de contrato | Project | Incluír tempo | Incluír gasto | Incluír taxa | Válido/non válido | Razón                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Si          | Si             | Si         | Non válido       | Infrinxe a regra. O tempo, o gasto e as taxas do proxecto P1 inclúense en ambas liñas de contrato, CL1 e CL2.                                                                                       |
| C1       | CL2           | P1      | Si          | Si             | Si         | Non válido       | Infrinxe a regra. O tempo, o gasto e as taxas do proxecto P1 inclúense en ambas liñas de contrato, CL1 e CL2.                                                                                       |
| C1       | CL1           | P1      | Si          | No              | Si         | Non válido       | Infrinxe a regra. O tempo e as taxas do proxecto P1 inclúense en ambas liñas de contrato, CL1 e CL2.                                                                                                   |
| C1       | CL2           | P1      | Si          | Si             | Si         | Non válido       | Infrinxe a regra. O tempo e as taxas do proxecto P1 inclúense en ambas liñas de contrato, CL1 e CL2.                                                                                                   |
| C1       | CL1           | P1      | Si          | No              | Si         | Válido           | O tempo e as taxas do proxecto P1 están incluídos en CL1. O gasto no proxecto P1 está incluído en CL2. </br>   Non hai solapamento no que se inclúe en cada liña de contrato e, polo tanto, é válido.  |
| C1       | CL2           | P1      | No           | Si             | No          | Válido           | O tempo e as taxas do proxecto P1 están incluídos en CL1. O gasto no proxecto P1 está incluído en CL2. </br>   Non hai solapamento no que se inclúe en cada liña de contrato e, polo tanto, é válido.  |
| C1       | CL1           | P1      | Si          | Si             | Si         | Non válido       | Infrinxe a regra. O tempo, os gastos e as taxas do proxecto P1 inclúense nas liñas de dous contratos.                                                                                               |
| CL2      | CL2           | P1      | Si          | Si             | Si         | Non válido       | Infrinxe a regra. O tempo, os gastos e as taxas do proxecto P1 inclúense nas liñas de dous contratos.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]