---
title: Facturación entre empresas
description: Este artigo ofrece información e exemplos sobre a facturación entre empresas para proxectos.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1debf8f67b7dbe7752075c6f8e5f2cdd37a3ae
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002774"
---
# <a name="intercompany-invoicing"></a>Facturación entre empresas

[!include [banner](../includes/banner.md)]

Este artigo ofrece información e exemplos sobre a facturación entre empresas para proxectos.

A súa organización pode ter varias divisións, filiais e outras persoas xurídicas que se transfiren produtos e servizos entre si para proxectos. A persoa xurídica que presta o servizo ou proporciona o produto chámase *persoa xurídica prestamista* e a persoa xurídica que recibe o servizo ou produto chámase *persoa xurídica prestameira*. 

A seguinte ilustración mostra un escenario típico onde dúas persoas xurídicas, SI FR (a persoa xurídica prestameira) e SI EUA (a persoa xurídica prestamista), comparten recursos para entregar un proxecto ao cliente A. Para este escenario, SI FR está contratada para entregar o traballo ao cliente A. 

[![Exemplo de facturación entre empresas](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

O obxectivo é facer máis flexible e poderoso o control de custos, o recoñecemento de ingresos, os impostos e o prezo de transferencia para transaccións de proxectos entre empresas. Ademais, ofrécense as seguintes capacidades:

-   Crear facturas de clientes contra un proxecto nunha persoa xurídica prestameira usando follas de control horario entre empresas, gastos e facturas de fornecedores nunha persoa xurídica prestamista.
-   Apoiar cálculos fiscais e custos indirectos.
-   Aprazar o recoñecemento de ingresos nunha persoa xurídica prestamista e cando unha persoa xurídica prestameira debe recoñecer o custo.
-   Acumular ingresos de traballo en proceso (WIP) na persoa xurídica prestamista.
-   Establecer prezos de transferencia que se poden basear en varios modelos de prezos. Aquí van algúns exemplos:
    -   **Cantidade** - A cantidade que ingresa no campo **Prezos** é o custo real por cantidade ou unidade.
    -   **Importe dos cargos** - O prezo/custo por transacción máis o importe dos cargos que introduce no campo **Prezos**.
    -   **Porcentaxe de cargos** - O prezo de transferencia é o prezo/custo por transacción multiplicado pola porcentaxe de cargos que introduce no campo **Prezos**.
    -   **Porcentaxe do prezo de venda** - A porcentaxe do prezo de venda que se transfire á persoa xurídica prestamista.
    -   **Cantidade inferior ao prezo de venda** - A cantidade que a persoa xurídica prestameira retén dos prezos de venda antes da transferencia á persoa xurídica prestamista.
    -   **Proporción de contribución** - O número que introduce no campo **Prezos** é a proporción de contribución, que se expresa como porcentaxe do prezo de venda.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Exemplo 1: Configurar parámetros para a facturación entre empresas
Neste exemplo, USSI é unha persoa xurídica prestamista e os seus recursos comunican tempo contra a persoa xurídica prestameira, FRSI, que posúe o contrato co cliente final. As horas e gastos que comunican os empregados de USSI pódense incluír na factura do proxecto que xera FRSI. Ademais, hai unha terceira fonte de transaccións que pode orixinarse desde a persoa xurídica prestamista (USSI neste exemplo) cando ofrece servizos de fornecedores compartidos a filiais (como FRSI) e despois transfire eses custos a proxectos dentro desas filiais. Finanzas cumprimenta todos os documentos de facturas e os cálculos de impostos correspondentes. 

Para este exemplo, FRSI debe ser un cliente da persoa xurídica USSI e USSI debe ser un fornecedor da persoa xurídica FRSI. A seguir, pode establecer unha relación entre empresas entre as dúas persoas xurídicas. O seguinte procedemento amosa como configurar os parámetros para que ambas as persoas xurídicas poidan participar na facturación entre empresas.

1. Configure FRSI como cliente na persoa xurídica USSI e configure USSI como fornecedor na persoa xurídica FRSI. Hai tres puntos de entrada para os pasos que son necesarios para esta tarefa.

   | Paso |                                                       Punto de entrada                                                        |                                                                                                                                                                                               Descripción                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | En USSI, prema <strong>Contas pendentes de cobro</strong> &gt; <strong>Clientes</strong> &gt; <strong>Todos os clientes</strong>. |                                                                                                                                                                  Cree un novo rexistro de cliente para FRSI e seleccione o grupo de clientes.                                                                                                                                                                  |
   |  N   |    En FRSI, prema <strong>Contas pendentes de pago</strong> &gt; <strong>Fornecedores</strong> &gt; <strong>Todos os fornecedores</strong>.     |                                                                                                                                                                    Cree un novo rexistro de fornecedor para USSI e seleccione o grupo de fornecedores.                                                                                                                                                                    |
   |  C   |                                  En FRSI, abra o rexistro de fornecedor que acaba de crear.                                  | No panel Acción, no separador <strong>Xeral</strong>, no grupo <strong>Configurar</strong>, prema <strong>Entre empresas</strong>. Na páxina <strong>Entre empresas</strong>, no separador <strong>Relación comercial</strong>, poña o control deslizante <strong>Activo</strong> en <strong>Si</strong>. No campo <strong>Empresa de cliente</strong>, seleccione o rexistro de cliente que creou no paso A. |


2. Prema **Xestión de proxectos e contabilidade** &gt; **Configurar** &gt; **Parámetros de xestión de proxectos e contabilidade** e prema o separador **Entre empresas**. A forma de configurar os parámetros depende de se vostede é a persoa xurídica prestameira ou a persoa xurídica prestamista.
   -   Se vostede é a persoa xurídica prestameira, seleccione a categoría de contratación que se debería empregar para que coincida coas facturas do fornecedor, que se xeran automaticamente.
   -   Se vostede é a persoa xurídica prestamista, seleccione unha categoría de proxecto predefinida para cada tipo de transacción para cada entidade prestameira. As categorías de proxectos úsanse para a configuración de impostos cando a categoría facturada en transaccións entre empresas só existe na persoa xurídica prestameira. Pode optar por acumular ingresos por transaccións entre empresas. Esta acumulación realízase cando se contabilizan as transaccións e, despois, invértese cando se publica a factura entre empresas.

3. Prema **Xestión de proxectos e contabilidade** &gt; **Configurar** &gt; **Prezos** &gt; **Prezo de transferencia**.
4. Seleccione unha moeda, un tipo de transacción e un modelo de prezo de transferencia. A moeda que se usa na factura é a moeda que está configurada no rexistro do cliente para a persoa xurídica prestameira na persoa xurídica prestamista. A moeda úsase para facer coincidir as entradas da táboa de prezos de transferencia.
5. Prema **Libro maior xeral** &gt; **Configuración de publicación** &gt; **Contabilidade entre empresas**, e configure unha relación para USSI e FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Exemplo 2: Crear e publicar unha folla de control horario entre empresas
USSI, a persoa xurídica prestamista, debe crear e publicar a folla de control horario para un proxecto de FRSI, a persoa xurídica prestameira. Hai dous puntos de entrada para os pasos que son necesarios para esta tarefa.

| Paso | Punto de entrada                                                                       | Descripción                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Xestión de proxectos e contabilidade** &gt; **Follas de control horario** &gt; **Todas as follas de control horario** | Cree unha folla de control horario nova Na liña da folla de control horario, no campo **Persoa xurídica**, seleccione **FRSI**. No campo **ID do proxecto**, seleccione o proxecto en FRSI. Introduza as horas de cada día da semana. |
| N    | Páxina **Folla de control horario**                                                                | Despois de executarse o fluxo de traballo, publique a folla de control horario e anote o número do vale.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Exemplo 3: Crear e publicar unha factura de fornecedor entre empresas
USSI, a persoa xurídica prestamista, debe crear e publicar factura de fornecedor entre empresas para un proxecto de FRSI, a persoa xurídica prestameira. Esta factura do fornecedor representa a man de obra e os gastos subcontratados que realizaron os fornecedores aos que paga USSI. Hai dous puntos de entrada para os pasos que son necesarios para esta tarefa.

| Paso | Punto de entrada                                                                                      | Descripción                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Contas pendentes de pago** &gt; **Facturas** &gt; **Abrir facturas de fornecedor** &gt; **Nova factura de fornecedor** | Cree unha nova factura de fornecedor e introduza os servizos que se adquiriron en nome do proxecto de FRSI.                                                                                                                                                                                  |
| N    | A páxina **Factura de fornecedor**                                                                      | Introduza liñas que representen os servizos subcontratados en nome de FRSI. No separador rápido **Detalles da liña**, no separador **Proxecto** para a liña de factura, no campo **Empresa do proxecto**, introduza **FRSI**. Introduza o proxecto e a información correspondente. A seguir, publique a factura do fornecedor. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Exemplo 4: Crear e publicar a factura entre empresas
USSI, a persoa xurídica prestamista, debe crear e publicar a factura entre empresas. Hai dous puntos de entrada para os pasos que son necesarios para esta tarefa.

| Paso | Punto de entrada                                                                                             | Descripción                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Xestión de proxectos e contabilidade** &gt; **Facturas do proxecto** &gt; **Factura de cliente entre empresas**  | Prema **Nova** para abrir a páxina **Crear factura entre empresas**.                                                                                  |
| N    | **Xestión de proxectos e contabilidade** &gt; **Facturas do proxecto** &gt; **Facturas de cliente entre empresas** | Na páxina **Crear factura entre empresas**, introduza a persoa xurídica, especifique a transacción que se debería incluír e prema **Buscar**. |
| C    | **Xestión de proxectos e contabilidade** &gt; **Facturas do proxecto** &gt; **Facturas de cliente entre empresas** | Seleccione as transaccións que desexa facturar ou prema **Seleccionar todas** para facturar todas as transaccións da lista e prema en **Aceptar**.                  |
| D    | A páxina **Factura entre empresas**                                                                       | Amósase a proposta de factura de cliente entre empresas.                                                                                             |
| E    | A páxina **Factura entre empresas**                                                                       | Prema **Publicar**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Exemplo 5: Publicar a factura do fornecedor e facturar ao cliente
Cando a persoa xurídica prestamista, USSI, publica a factura de cliente entre empresas, créase unha factura de fornecedor pendente equivalente na entidade xurídica prestameira, FRSI. Despois de publicar esta factura do fornecedor, FRSI tamén factura ao cliente do proxecto as horas que introduciu USSI. Hai tres puntos de entrada para os pasos que son necesarios para esta tarefa.

| Paso | Punto de entrada                                                                                        | Descripción                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Contas pendentes de pago** &gt; **Facturas** &gt; **Facturas pendentes do fornecedor**                            | Revise a factura para comprobar que se inclúen os valores da folla de control horario e logo publique a factura do fornecedor.                  |
| N    | **Xestión de proxectos e contabilidade** &gt; **Facturas do proxecto** &gt; **Propostas de facturas do proxecto** | Cree unha nova factura de proxecto e comprobe que aparecen as transaccións horarias que se publicaron.            |
| C    | A páxina **Factura de proxecto**                                                                       | Seleccione a factura do proxecto e prema **Ver detalles** para revisar o custo e o importe das vendas. A seguir, publique a factura. |


Para obter máis información, consulte [Configurar a facturación de proxectos entre empresas](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]