---
title: Crear e confirmar diarios de entradas
description: Este artigo ofrece información sobre como crear e confirmar diarios de entrada en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912330"
---
# <a name="create-and-confirm-entry-journals"></a>Crear e confirmar diarios de entradas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Usa os diarios de entrada para rexistrar datos reais directamente en Microsoft Dynamics 365 Project Operations. Cando utilizas os diarios de entrada, non tes que introducir rexistros de uso de tempo, gasto e material en Operacións do proxecto.

Un único diario de entrada permítelle crear varias liñas de diario. Cando se confirma o diario, unha liña do diario de entrada rexistra o real para os seguintes detalles:

- O custo ou ingresos, dependendo do tipo de transacción seleccionado.
- A clase de transacción seleccionada. As clases dispoñibles son **Tempo**, **·**, **·**, **·**, **·**, e **Imposto**.
- O proxecto e/ou unha tarefa que se selecciona na liña do xornal.

Siga estes pasos para crear un diario de entrada en Project Operations.

1. Ir a **Vendas** \> **Transaccións** \> **Xornais**.
2. No **Xornais de entrada** páxina de lista, no Panel de accións, seleccione **Novo** para crear un diario.
3. No **Novo xornal** páxina, na **Descrición** campo, introduza unha descrición da revista.
4. Asegúrese de que o **Tipo de revista** campo está configurado en **Entrada** e, a continuación, seleccione **Gardar**. Despois de gardar o novo diario de entrada, a **Liñas do xornal** debe aparecer na páxina do xornal.
5. No **Liñas do xornal** pestana, na barra de ferramentas situada enriba da grade, seleccione **Novo** para crear unha liña de diario de entrada.
6. No **Creación rápida** caixa de diálogo para crear unha liña de diario de entrada, configure os campos como se describe na seguinte táboa.

    | Campo | Descripción | Impacto funcional |
    | --- | --- | --- |
    | Clase de transacción | A liña do diario pódese clasificar nunha das seis clases de transacción: **Tempo**, **·**, **·**, **·**, **·**, ou **Imposto**. | O **Imposto** a clase de transacción quedou en desuso en Project Operations. <br> Se creas un **Imposto** clase de transacción, non se procesará mediante facturación nin cálculos de custos ou ingresos. **Fito** é unha clase de transacción de só ingresos. <br>O **Retén** clase de transacción representa un anticipo que se recibiu dun cliente. Debe crearse sempre como un par de liñas de diario de vendas facturadas e vendas non facturadas. |
    | Tipo de transacción | O **Custo**, **Interorg**, e **Custo unitario de recursos** os tipos de transacción deben utilizarse para rexistrar o custo.<br> O **Vendas non facturadas** e **Vendas facturadas** Os tipos de transacción deben utilizarse para rexistrar os ingresos. | O **Retén** a clase de transacción só funciona co **Vendas non facturadas** e **Vendas facturadas** tipos de transacción.<br> O **Fito** a clase de transacción só funciona co **Vendas facturadas** tipo de transacción. <br>O **Vendas Interorg** e **Custo unitario de recursos** os tipos de transacción só son aplicables ao **Tempo** clase de transacción e estes só están dispoñibles nos diarios de entrada no escenario de despregamento Lite e non cando se implementan Operacións do proxecto nos escenarios de recursos/non almacenados. |
    | Seleccionar produto | Cando o **Material** está seleccionada a clase de transacción, este campo permítelle especificar se a transacción de material para a que está a crear a liña de diario é un produto existente ou un produto de escritura. | Se seleccionas **Produto de escritura**, pode introducir un nome para o produto. |
    | Produto | Unha referencia ao produto do catálogo. | |
    | Descripción | Unha descrición da liña do xornal para facilitar a súa identificación. | Para as liñas de diario de vendas non facturadas, o valor empregarase como descrición cando se creen os detalles da liña de factura. |
    | Descrición externa | Unha descrición da liña do xornal que se pode usar para compartir con partes interesadas externas. | Para as liñas de diario de vendas non facturadas, o valor empregarase como descrición externa cando se creen os detalles da liña de factura. Tamén pode aparecer na factura que se envía ao cliente. |
    | Tipo de facturación | Un valor que indica se a liña do xornal se contará como un compoñente cobrable, complementario ou non cobrable no proxecto. | Nun fluxo típico, o tipo de facturación derívase dos termos acordados que se establecen no contrato. Non obstante, cando grava unha liña de diario, pode introducir un valor neste campo. |
    | Data do documento | Usa unha data na que se produciu a transacción. | |
    | Data de inicio | Use a data na que se produciu a transacción. | Este campo úsase para comparar coa data de creación da factura para as transaccións do **Vendas non facturadas** tipo. Esta comparación axudarache a decidir se a transacción ten data futura ou pasada. Só se engadirán á factura as transaccións con datas anteriores. |
    | Data de fin | Use a data na que se produciu a transacción. | |
    | Data da contabilidade | Use a data na que se rexistrará o impacto contable. | |
    | Cliente liña de contrato | Por defecto, se a liña de contrato só ten un cliente, este campo establécese para o cliente na liña de contrato cando se garda a liña de diario. Se a liña de contrato ten varios clientes, seleccione o cliente correcto na liña de contrato. | Se o sistema non pode determinar o cliente da liña de contrato na liña do diario, e se está en branco no real do **Vendas non facturadas** tipo que se crea a partir da liña do diario, o real non se facturará. |
    | Project | Seleccione o proxecto para gravar o real. | En función do proxecto, clase de transacción e tarefa seleccionados, o sistema tentará determinar o contrato, a liña de contrato e o cliente da liña de contrato. |
    | Tarefa | Seleccione a tarefa para gravar o real. | Se asociaches tarefas con liñas de contrato durante a configuración do contrato, o sistema utilizará a tarefa seleccionada, xunto cun proxecto e unha clase de transacción, para determinar o contrato, a liña de contrato e o cliente da liña de contrato. |
    | Categoría da transacción | Seleccione a categoría de transacción para gravar o real. | Para os gastos, a categoría de transacción seleccionada determina o prezo predeterminado que se introducirá na liña do diario cando se garda. |
    | Rol | Este campo é relevante para as liñas do diario de tempo. Seleccione o papel do recurso que pasou tempo no proxecto e/ou tarefa. | Para as liñas de diario de tempo, se usa a configuración predeterminada para a entrada de custos de recursos predeterminados e tarifas de facturación, o rol seleccionado utilízase xunto coa unidade de recursos para determinar o prezo predeterminado que se introducirá na liña de diario cando está gardado. Se usa unha configuración personalizada para a entrada de prezos predeterminados, debe revisar esa configuración para determinar se o **Papel** úsase para introducir os valores de prezos predeterminados. |
    | Subcontrato | Se a liña do diario representa a capacidade subcontratada, ou gastos ou materiais subcontratados, seleccione o subcontrato correspondente. | Cando se rexistran liñas de diario de custos, o subcontrato seleccionado determinará a lista de prezos que se utiliza para introducir o custo unitario predeterminado. |
    | Liña de subcontratación | Se a liña do diario representa a capacidade subcontratada, ou gastos ou materiais subcontratados, seleccione a liña de subcontratación correspondente. | Cando se rexistran liñas de diario de custos, a liña de subcontratación seleccionada asegurarase de que os cálculos de capacidade dispoñibles na liña de subcontratación se calculen correctamente. |
    | Método do importe | De forma predeterminada, este campo está configurado como **Multiplica a cantidade polo prezo**. Cando se utilice este método, o importe calcularase como *Cantidade* ×*Prezo*. O outro método compatible é **Prezo fixo**. Cando se utiliza este método, o prezo establecerase na cantidade e a cantidade non se utilizará no cálculo. | |
    | Horario e Unidade da Unidade | Xuntos, o programa unitario e a unidade identifican a unidade da cantidade. | A combinación da unidade e a categoría de transacción úsase para introducir os prezos predeterminados dos gastos. Na configuración predeterminada de Operacións do proxecto, a combinación da unidade, función e unidade de recursos úsase para introducir prezos predeterminados para o tempo. Se tes unha configuración personalizada para a entrada de prezos predeterminados, utilizarase xunto coa unidade. A combinación do produto e da unidade úsase para introducir os prezos predeterminados dos materiais. |
    | Cantidade | Introduza a cantidade. | |
    | Prezo | Se o prezo se deixa en branco cando se crea a liña do diario, utilizaranse os valores relevantes para introducir os prezos predeterminados, dependendo da clase de transacción. Se se introduce un prezo cando se crea a liña do diario, utilizarase ese prezo. | |
    | Impostos | Introduza calquera cantidade de impostos. | En función do importe do imposto que se consigna, o importe ampliado calcularase como *Cantidade* + *Imposto*. |

## <a name="confirm-an-entry-journal"></a>Confirmar un diario de entrada

Despois de introducir todas as liñas do diario nun diario de entrada, podes confirmalo. Este proceso rexistrará cada liña do xornal como reais dos proxectos apropiados.

Despois de confirmar unha revista, xa non podes editala nin ningunha das súas liñas.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Datos reais creados pola confirmación do diario de entrada

Existen algunhas diferenzas clave entre os datos reais que se crean mediante a confirmación do diario de entrada e os reais que se crean durante a aprobación dos rexistros de uso de tempo, gastos e materiais e a confirmación da factura en Operacións do proxecto:

- Os diarios de entrada non usan conexións de transacción para vincular o custo real coas vendas reais non facturadas. Os datos reais que se crean cando se aproban os rexistros de uso de tempo, gasto e material sempre usan conexións de transaccións para vincular os custos e as vendas sen facturar.
- Os diarios de entrada non usan as orixes das transaccións para vincular o custo real e os reais de vendas non facturados con ningún rexistro de orixe. Os datos reais que se crean cando se aproban os rexistros de uso de tempo, gasto e material sempre usan orixes de transacción para vincular os custos e as vendas non facturadas coa entrada de tempo de orixe.
- Cando se facturan os reais de vendas non facturados que se crean mediante a confirmación do diario de entrada, os reais de vendas facturados que se crean durante a confirmación da factura vencellan aos reais de vendas non facturados, dun xeito similar aos reais de vendas non facturados que se crean cando o tempo, os gastos e Os rexistros de uso do material están aprobados.
- As liñas do diario de entrada que se crean para o tempo introducido por recursos interorganizativos non causan reais do **Custo unitario de recursos** e **Vendas Interorg** tipos que se crearán automaticamente. Estes datos reais deben ser creados manualmente. Este comportamento difire do comportamento das entradas de tempo que son rexistradas por recursos interorganizativos. Nese caso, cando se aproba o tempo, a aplicación crea automaticamente os datos reais **Custo** escriba o proxecto e os datos reais do **Custo unitario de recursos** e **Vendas Interorg** tipos na división propietaria do empregado. Despois utiliza conexións de transacción para vincular eses datos reais e orixes de transacción para vinculalos á entrada de tempo de orixe.
- Cando se confirman os diarios de entrada, crean datos reais. Non obstante, os diarios de corrección non se poden usar para corrixir eses datos reais. Este comportamento difire do comportamento dos datos reais que se crean cando se aproban os rexistros de uso de tempo, gasto e material. Nese caso, a aplicación permítelle utilizar os diarios de corrección para corrixir os datos reais e corrixir os erros, sempre que aínda non se facturaron. Se xa foron facturados, aínda pode corrixir un real se procesa un crédito completo deste real ao cliente.

> [!NOTE]
> Os diarios de entrada non aplican regras predeterminadas estritas. Polo tanto, use estes Diarios de entrada o menos posible e teña coidado e coidado para asegurarse de non crear datos financeiros corruptos no seu sistema. Sempre que poidas, utiliza os rexistros de uso de tempo, gasto e material, a configuración de fitos e retencións nos contratos do proxecto e o proceso de confirmación da factura do proxecto en lugar dos diarios de entrada para crear datos reais.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
