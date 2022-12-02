---
title: Crear e confirmar diarios de entradas
description: Este artigo fornece información sobre como crear e confirmar os diarios de entradas en Microsoft Dynamics 365 Project Operations.
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

Os diarios de entradas utilízanse para rexistrar datos reais directamente en Microsoft Dynamics 365 Project Operations. Cando utiliza os diarios de entradas, non ten que introducir rexistros de tempo, gasto e uso de material en Project Operations.

Un único diario de entradas permítelle crear varias liñas de diario. Cando se confirma o diario, unha liña do diario de entradas rexistra o dato real para os seguintes detalles:

- O custo ou os ingresos, dependendo do tipo de transacción seleccionado.
- A clase da transacción seleccionada. As clases dispoñibles son **Tempo**, **Gasto**, **Material**, **Retención**, **Fito** e **Imposto**.
- O proxecto e/ou unha tarefa que se selecciona na liña de diario.

Siga estes pasos para crear un diario de entradas en Project Operations.

1. Vaia a **Vendas** \> **Transaccións** \> **Diarios**.
2. Na páxina de lista **Diarios de entradas**, no panel de Acción, seleccione **Novo** para crear un diario.
3. Na páxina **Novo diario**, no separador **Descrición**, introduza unha descrición do diario.
4. Asegúrese de que o campo **Tipo de diario** campo está configurado como **Entrada** e, a seguir, seleccione **Gardar**. Despois de gardar o novo diario de entradas, o separador **Liñas de diario** debe aparecer na páxina do diario.
5. No separador **Liñas de diario**, na barra de ferramentas situada enriba da grade, seleccione **Nova** para crear unha liña de diario de entradas.
6. Na caixa de diálogo **Creación rápida** para crear unha liña de diario de entradas, configure os campos como se describe na seguinte táboa.

    | Campo | Descripción | Impacto funcional |
    | --- | --- | --- |
    | Clase de transacción | A liña de diario pódese clasificar nunha das seis clases de transacción: **Tempo**, **Gasto**, **Material**, **Retención**, **Fito** ou **Imposto**. | A clase de transacción **Imposto** quedou obsoleta en Project Operations. <br> Se crea unha clase de transacción **Imposto**, non se procesará mediante facturación nin cálculos de custos ou ingresos. **Fito** é unha clase de transacción só con ingresos. <br>A transacción **Retención** representa un anticipo que se recibiu dun cliente. Debe crearse sempre como un par de liñas de diario de vendas facturadas e vendas non facturadas. |
    | Tipo de transacción | Os tipos de transacción **Custo**, **Vendas entre organizacións** e **Custo da unidade de recursos** deben utilizarse para rexistrar o custo.<br> Os tipos de transaccións **Vendas non facturadas** e **Vendas facturadas** deben utilizarse para rexistrar os ingresos. | A clase de transacción **Retención** só funciona cos tipos de transacción **Vendas non facturadas** e **Vendas facturadas**.<br> A clase de transacción **Fito** só funciona co tipo de transacción **Vendas facturadas**. <br>Os tipos de transacción **Vendas entre organizacións** e **Custo de unidade de recursos** só son aplicables á clase de transacción **Tempo** e só están dispoñibles nos diarios de entradas no escenario de despregamento Lite e non cando se desprega Project Operations nos escenarios de recursos/sen fornecemento. |
    | Seleccionar produto | Cando a clase de transacción **Material** está seleccionada, este campo permítelle especificar se a transacción de material para a que está a crear a liña de diario é un produto existente ou un produto fóra de catálogo. | Se selecciona **Produto fóra de catálogo**, pode introducir un nome para o produto. |
    | Produto | Unha referencia ao produto do catálogo. | |
    | Descripción | Unha descrición da liña de diario para facilitar a súa identificación. | Para as liñas de diario de vendas non facturadas, o valor empregarase como descrición cando se creen os detalles da liña de factura. |
    | Descrición externa | Unha descrición da liña de diario que se pode usar para compartir con partes interesadas externas. | Para as liñas de diario de vendas non facturadas, o valor empregarase como descrición externa cando se creen os detalles da liña de factura. Tamén pode aparecer na factura que se envía ao cliente. |
    | Tipo de facturación | Un valor que indica se a liña de diario se contará como un compoñente imputable, gratuíto ou non imputable no proxecto. | Nun fluxo típico, o tipo de facturación derívase dos termos acordados que se establecen no contrato. Non obstante, cando rexistra unha liña de diario, pode introducir un valor neste campo. |
    | Data do documento | Use unha data na que se produciu a transacción. | |
    | Data de inicio | Use a data na que se produciu a transacción. | Este campo úsase para comparar coa data de creación da factura para as transaccións do tipo **Vendas non facturadas**. Esta comparación axudaralle a decidir se a transacción ten data futura ou pasada. Só se engadirán á factura as transaccións con datas pasadas. |
    | Data de fin | Use a data na que se produciu a transacción. | |
    | Data da contabilidade | Use a data na que se rexistrará o impacto contable. | |
    | Cliente da liña de contrato | Por defecto, se a liña de contrato só ten un cliente, este campo establécese para o cliente na liña de contrato cando se garda a liña de diario. Se a liña de contrato ten varios clientes, seleccione o cliente correcto na liña de contrato. | Se o sistema non pode determinar o cliente da liña de contrato na liña do diario, e se está en branco no dato real de tipo **Vendas non facturadas** que se crea a partir da liña do diario, o dato real non se facturará. |
    | Project | Seleccione o proxecto para rexistrar o dato real. | En función do proxecto seleccionado, a clase de transacción e a tarefa seleccionados, o sistema tentará determinar o contrato, a liña de contrato e o cliente da liña de contrato. |
    | Tarefa | Seleccione a tarefa para rexistrar o dato real. | Se asociou tarefas con liñas de contrato durante a configuración do contrato, o sistema utilizará a tarefa seleccionada, xunto cun proxecto e unha clase de transacción, para determinar o contrato, a liña de contrato e o cliente da liña de contrato. |
    | Categoría da transacción | Seleccione a categoría de transacción para rexistrar o dato real. | Para os gastos, a categoría de transacción seleccionada determina o prezo predeterminado que se introducirá na liña de diario cando se garde. |
    | Rol | Este campo é relevante para as liñas de diario de tempo. Seleccione o rol do recurso que pasou tempo no proxecto e/ou tarefa. | Para as liñas de diario de tempo, se usa a configuración predefinida para a entrada de custos e taxas de facturación de recursos predefinidos, o rol seleccionado utilízase xunto coa unidade de recursos para determinar o prezo predefinido que se introducirá na liña de diario cando se garda. Se utiliza unha configuración personalizada para a entrada de prezos predefinidos, debe revisar esa configuración para determinar se o **Rol** se utiliza para introducir os valores de prezos predefinidos. |
    | Subcontrato | Se a liña de diario representa a capacidade subcontratada, ou gastos ou materiais subcontratados, seleccione o subcontrato correspondente. | Cando se rexistran liñas do diario de custos, o subcontrato seleccionado determinará a lista de prezos que se utiliza para introducir o custo unitario predeterminado. |
    | Liña de subcontrato | Se a liña de diario representa a capacidade subcontratada, ou gastos ou materiais subcontratados, seleccione o a liña de subcontrato correspondente. | Cando se rexistran liñas de diario de custo, a liña de subcontratación seleccionada asegurarase de que os cálculos de capacidade dispoñibles na liña de subcontratación se calculen correctamente. |
    | Método do importe | Por defecto, este campo establécese en **Multiplicar cantidade por prezo**. Cando se utilice este método, o importe calcularase como *Cantidade* × *Prezo*. O outro método compatible é **Prezo fixo**. Cando se utiliza este método, o prezo establecerase na cantidade e a cantidade non se utilizará no cálculo. | |
    | Programación de unidades e unidade | Conxuntamente, a programación de unidades e a unidade identifican a unidade da cantidade. | A combinación da unidade e a categoría de transacción úsase para introducir prezos predefinidos para gastos. Na configuración predeterminada de Project Operations, a combinación da unidade, rol e unidade de recursos úsase para introducir prezos predefinidos para tempo. Se ten unha configuración personalizada para a entrada de prezos predefinidos, utilizarase xunto coa unidade. A combinación do produto e a unidade utilízase para introducir os prezos por defecto dos materiais. |
    | Cantidade | Introduza a cantidade. | |
    | Prezo | Se o prezo se deixa en branco cando se crea a liña de diario, utilizaranse os valores pertinentes para introducir os prezos predefinidos, dependendo da clase de transacción. Se se introduce un prezo cando se crea a liña de diario, utilizarase ese prezo. | |
    | Impostos | Introduza calquera cantidade de impostos. | En función do importe do imposto que se introduza, o importe ampliado calcularase como *Cantidade* + *Imposto*. |

## <a name="confirm-an-entry-journal"></a>Confirmar un diario de entradas

Despois de introducir todas as liñas do diario nun diario de entradas, pode confirmalo. Este proceso rexistrará cada liña de diario como datos reais dos proxectos apropiados.

Despois de confirmar un diario, xa non pode editalo nin ningunha das súas liñas.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Datos reais creados pola confirmación do diario de entradas

Hai algunhas diferenzas fundamentais entre os datos reais que se crean mediante a confirmación do diario de entradas e os datos reais que se crean durante a aprobación dos rexistros de uso de tempo, gastos e materiais e a confirmación da factura en Project Operations:

- Os diarios de entradas non usan conexións de transacción para vincular o dato real de custo co dato real de vendas non facturadas. Os datos reais que se crean cando se aproban os rexistros de uso de tempo, gasto e material sempre usan conexións de transacción para vincular os datos reais de custo e vendas non facturadas.
- Os diarios de entradas non usan orixes de transacción para vincular o dato real de custo e os datos reais de vendas non facturadas con calquera rexistro de orixe. Os datos reais que se crean cando se aproban os rexistros de uso de tempo, gasto e material sempre usan orixes de transacción para vincular os datos reais de custo e vendas non facturadas coa entrada de tempo de orixe.
- Cando se facturan os datos reais de vendas non facturadas que se crean mediante a confirmación do diario de entradas, os datos reais de vendas facturadas que se crean durante a confirmación da factura vincúlanse aos reais de vendas non facturadas, de xeito similar aos datos reais de vendas non facturadas que se crean cando o se aproban os rexistros de tempo, gasto e uso de material.
- As liñas de diario de entradas que se crean para o tempo introducido por recursos entre organizacións non causan datos reais dos tipos **Custo de unidades de recursos** e **Vendas entre organizacións** que se crearán automaticamente. Estes datos reais débense crear manualmente. Este comportamento difire do comportamento das entradas de tempo que son rexistradas por recursos entre organizacións. Nese caso, cando se aproba o tempo, a aplicación crea automaticamente datos reais de tipo **Custo** no proxecto e datos reais dos tipos **Custo de unidade de recursos** e **Vendas entre organizacións** na división propietaria do empregado. Despois usa conexións de transacción para vincular eses datos reais e orixes de transacción para vinculalos á entrada de tempo de orixe.
- Cando se confirman os diarios de entradas, crean datos reais. Non obstante, os diarios de corrección non se poden usar para corrixir eses datos reais. Este comportamento difire do comportamento dos datos reais que se crean cando se aproban os rexistros de tempo, gasto e uso de material. Nese caso, a aplicación permítelle utilizar os diarios de corrección para corrixir os datos reais e corrixir os erros, sempre que aínda non se facturasen. Se xa se facturaron, aínda pode corrixir un dato real se procesa un crédito completo dese dato real ao cliente.

> [!NOTE]
> Os diarios de entradas non aplican regras predefinidas estritas. Polo tanto, use estes diarios de entradas o menos posible e teña coidado para asegurarse de non crear datos financeiros corruptos no seu sistema. Sempre que poida, utilice os rexistros de tempo, gasto e uso de material, a configuración de fitos e retencións nos contratos do proxecto e o proceso de confirmación da factura do proxecto en lugar dos diarios de entradas para crear datos reais.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
