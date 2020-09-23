---
title: Transaccións comerciais
description: Este tema fornece información sobre as transaccións comerciais.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f059d9ec-878d-40c1-bd00-a8966bdf4e29
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe93ec07e9eed0af02c62d08f18a0b2aaeff7996
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751484"
---
# <a name="business-transactions"></a>Transaccións comerciais

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En Dynamics 365 Project Service Automation, *transacción comercial* é un concepto abstracto que non representa ningunha entidade. Non obstante, algúns campos e procesos comúns en entidades están deseñados para empregar o concepto de transaccións comerciais. As seguintes entidades usan esta abstracción:

- Detalles da liña de oferta
- Detalles da liña de contrato
- Liñas de estimación
- Liñas de diario
- Valores reais

Destas entidades, os detalles da liña de oferta, os detalles da liña de contrato e as liñas de estimación asígnanse á fase de estimación no ciclo de vida do proxecto. As entidades de liñas de diario e datos reais asígnanse á fase de execución no ciclo de vida do proxecto.

PSA trata os rexistros nestas cinco entidades como transaccións comerciais. A única distinción é que os rexistros de entidades que se asignan á fase de estimación considéranse previsións financeiras, mentres que os rexistros de entidades que se asignan á fase de execución considéranse feitos financeiros que xa se produciron.

Para obter máis información, consulte [Estimacións](estimates.md) e [Datos reais](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptos exclusivos das transaccións comerciais
Os conceptos seguintes son exclusivos do concepto de transaccións comerciais:

- Tipo de transacción
- Clase de transacción
- Orixe da transacción
- Conexión da transacción

### <a name="transaction-type"></a>Tipo de transacción

O tipo de transacción representa o momento e o contexto do impacto financeiro nun proxecto. Está representado por un conxunto de opcións que ten os seguintes valores admitidos en PSA:
- Custo
- Contrato do proxecto
- Vendas sen facturar
- Vendas facturadas
- Vendas entre organizacións
- Custo da unidade de recursos

### <a name="transaction-class"></a>Clase de transacción

A clase de transacción representa os diferentes tipos de custos nos que se incorre nos proxectos. Está representado por un conxunto de opcións que ten os seguintes valores admitidos en PSA:

- Time
- Gasto
- Material
- Tarifa
- Fito
- Imposto

O valor **Fito** é utilizado normalmente pola lóxica de negocio para a facturación con prezos fixos en PSA.

### <a name="transaction-origin"></a>Orixe da transacción

A orixe da transacción é unha entidade que almacena a orixe de cada transacción comercial. Cando a execución do proxecto estea en marcha, cada transacción comercial dará lugar a outra transacción comercial que á súa vez creará outra e así sucesivamente. A entidade de orixe da transacción foi deseñada para almacenar datos sobre a orixe de cada transacción para axudar na elaboración de informes e a rastrexabilidade. 

### <a name="transaction-connection"></a>Conexión da transacción

A conexión de transacción é unha entidade que almacena a relación entre dúas transaccións comerciais similares, como os datos reais de custo e as vendas relacionadas ou as inversións de transaccións desencadeadas por actividades de facturación como a confirmación de facturas ou a corrección de facturas.

En conxunto, as entidades Orixe de transacción e Conexión de transacción axudan a rastrexar as relacións entre as transaccións comerciais e as accións que deron lugar á creación dunha transacción comercial específica.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplo: Como funciona Orixe de transacción con Conexión de transacción

O seguinte exemplo mostra o procesamento típico de entradas de tempo nun ciclo de vida dun proxecto de PSA.

> ![Entradas de tempo de procesamento nun ciclo de vida de Project Service](media/basic-guide-17.png)
 
1. O envío dunha entrada de tempo provoca a creación de dúas liñas de diario: unha para o custo e outra para as vendas sen facturar.
2. A aprobación posterior da entrada de tempo provoca a creación de dous datos reais: un para o custo e outro para as vendas sen facturar.
3. Cando o usuario crea unha factura de proxecto, a transacción da liña de factura créase mediante datos de vendas non facturadas. 
4. Cando se confirma a factura, créanse dous novos datos reais: unha reversión de vendas sen facturar e un dato real de vendas facturadas.

Cada un destes eventos desencadea a creación de rexistros nas entidades Orixe da transacción e Conexión da transacción para axudar a construír un rastro de relacións entre estes rexistros que se crean na entrada de tempo, a liña de diario, os datos reais e os detalles da liña de factura.

Na seguinte táboa móstranse os rexistros da entidade de Orixe da transacción para o fluxo de traballo anterior.

| Evento                        | Orixe                   | Tipo de orixe                       | Transacción                       | Tipo de transacción         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Envío de entrada de tempo        | GUID de rexistro de entrada de tempo   | Entrada de tempo                        | GUID de rexistro de liña de diario (custo)   | Liña de diario             |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de rexistro de liña de diario (vendas)  | Liña de diario                      |                          |
| Aprobación de tempo                | GUID de rexistro de liña de diario | Liña de diario                      | GUID de rexistro de vendas sen facturar        | Real                   |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de rexistro de vendas sen facturar        | Real                            |                          |
| GUID de rexistro de liña de diario     | Liña de diario             | GUID de rexistro de datos reais de custo           | Real                            |                          |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de rexistro de datos reais de custo           | Real                            |                          |
| Creación de facturas             | GUID de rexistro de entrada de tempo   | Entrada de tempo                        | GUID de transacción da liña de factura     | Transacción da liña de factura |
| GUID de rexistro de liña de diario     | Liña de diario             | GUID de transacción da liña de factura     | Transacción da liña de factura          |                          |
| Confirmación de factura         | GUID de liña de factura        | Liña de factura                      | GUID de rexistro de vendas facturadas          | Real                   |
| GUID de factura                 | Factura                  | GUID de rexistro de vendas facturadas          | Real                            |                          |
| GUID de detalle da liña de factura     | Detalle da liña da factura      | GUID de rexistro de vendas facturadas          | Real                            |                          |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de rexistro de vendas facturadas          | Real                            |                          |
| GUID de rexistro de liña de diario     | Liña de diario             | GUID de rexistro de vendas facturadas          | Real                            |                          |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de inversión de vendas sen facturar      | Real                            |                          |
| GUID de rexistro de liña de diario     | Liña de diario             | GUID de inversión de vendas sen facturar      | Real                            |                          |
| Corrección de borrador de factura     | GUID de ILD antiga             | Transacción da liña de factura          | GUID de ILD de corrección               | Transacción da liña de factura |
| GUID de IL antiga                  | Liña de factura             | GUID de ILD de corrección               | Transacción da liña de factura          |                          |
| GUID de factura antiga             | Factura                  | GUID de ILD de corrección               | Transacción da liña de factura          |                          |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de ILD de corrección               | Transacción da liña de factura          |                          |
| GUID de rexistro de liña de diario     | Liña de diario             | GUID de ILD de corrección               | Transacción da liña de factura          |                          |
| Corrección de factura confirmada | GUID de ILD antiga             | Transacción da liña de factura          | GUID de datos real de vendas facturadas revertidas | Real                   |
| GUID de IL antiga                  | Liña de factura             | GUID de datos real de vendas facturadas revertidas | Real                            |                          |
| GUID de factura antiga             | Factura                  | GUID de datos real de vendas facturadas revertidas | Real                            |                          |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de datos real de vendas facturadas revertidas | Real                            |                          |
| GUID de rexistro de liña de diario     | Liña de diario             | GUID de datos real de vendas facturadas revertidas | Real                            |                          |
| GUID de ILD antiga                 | Transacción da liña de factura | GUID de dato real de novas vendas sen facturar    | Real                            |                          |
| GUID de IL antiga                  | Liña de factura             | GUID de dato real de novas vendas sen facturar    | Real                            |                          |
| GUID de factura antiga             | Factura                  | GUID de dato real de novas vendas sen facturar    | Real                            |                          |
| GUID de rexistro de entrada de tempo       | Entrada de tempo               | GUID de dato real de novas vendas sen facturar    | Real                            |                          |
| GUID de rexistro de liña de diario     | Liña de diario             | GUID de dato real de novas vendas sen facturar    | Real                            |                          |
| GUID de ILD de corrección          | Transacción da liña de factura | GUID de dato real de novas vendas sen facturar    | Real                            |                          |
| GUID de IL de corrección           | Liña de factura             | GUID de dato real de novas vendas sen facturar    | Real                            |                          |
| GUID de factura de corrección      | Factura                  | GUID de dato real de novas vendas sen facturar    | Real                            |                          |

Na seguinte táboa móstranse os rexistros da entidade de Conexión da transacción para o fluxo de traballo anterior.

| Evento                          | Transacción 1                 | Rol de transacción 1 | Tipo de transacción 1           | Transacción 2                | Rol de transacción 2 | Tipo de transacción 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Envío de entrada de tempo          | GUID de liña de diario (vendas)     | Vendas sen facturar     | msdyn_journalline            | GUID de liña de diario (custo)     | Custo               | msdyn_journalline  |
| Aprobación de tempo                  | GUID de dato real de vendas sen facturar  | Vendas sen facturar     | msdyn_actual                 | GUID de dato real de custo (custo)       | Custo               | msdyn_actual       |
| Creación de facturas               | GUID de detalle da liña de factura      | Vendas facturadas       | msdyn_invoicelinetransaction | GUID de dato real de vendas sen facturar   | Vendas sen facturar     | msdyn_actual       |
| Confirmación de factura           | GUID de dato real de reversión         | Reversión          | msdyn_actual                 | GUID de vendas sen facturar orixinais | Orixinal           | msdyn_actual       |
| GUID de vendas facturadas              | Vendas facturadas                  | msdyn_actual       | GUID de dato real de vendas sen facturar   | Vendas sen facturar               | msdyn_actual       |                    |
| Corrección de borrador de factura       | GUID de transacción da liña de factura | Substitución          | msdyn_invoicelinetransaction | GUID de vendas facturadas            | Orixinal           | msdyn_actual       |
| Confirmar corrección de factura     | GUID de reversión de vendas facturadas    | Reversión          | msdyn_actual                 | GUID de vendas facturadas            | Orixinal           | msdyn_actual       |
| GUID de dato real de novas vendas sen facturar | Substitución                     | msdyn_actual       | GUID de vendas facturadas            | Orixinal                     | msdyn_actual       |                    |
