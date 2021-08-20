---
title: Ligar datos reais cos rexistros orixinais
description: Este tema explica como ligar datos reais a rexistros orixinais como entrada de tempo, entrada de gastos ou rexistros de uso de material.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991754"
---
# <a name="link-actuals-to-original-records"></a>Ligar datos reais cos rexistros orixinais

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


En Dynamics 365 Project Operations, unha *transacción comercial* é un concepto abstracto que non está representada por unha entidade. Non obstante, algúns campos e procesos comúns en entidades están deseñados para empregar o concepto de transaccións comerciais. As seguintes entidades usan este concepto:

- Detalles da liña de oferta
- Detalles da liña de contrato
- Liñas de estimación
- Liñas de diario
- Valores reais

Destas entidades, **Detalles de liña de oferta**, **Detalles de liña de contrato** e **Liñas de estimación** asígnanse á fase de estimación no ciclo de vida do proxecto. As entidades **Liñas de diario** e **Datos reais** asígnanse á fase de execución no ciclo de vida do proxecto.

Project Operations recoñece rexistros nestas cinco entidades como transaccións comerciais. A única distinción é que os rexistros das entidades que se asignan á fase de estimación considéranse previsións financeiras, mentres que os rexistros de entidades que se asignan á fase de execución considéranse feitos financeiros que xa se produciron.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptos exclusivos das transaccións comerciais
Os conceptos seguintes son exclusivos do concepto de transaccións comerciais:

- Tipo de transacción
- Clase de transacción
- Orixe da transacción
- Conexión da transacción

### <a name="transaction-type"></a>Tipo de transacción

O tipo de transacción representa o momento e o contexto do impacto financeiro nun proxecto. Isto está representado por un conxunto de opcións que ten os seguintes valores admitidos en Project Operations:

  - Custo
  - Contrato do proxecto
  - Vendas sen facturar
  - Vendas facturadas
  - Vendas entre organizacións
  - Custo da unidade de recursos

### <a name="transaction-class"></a>Clase de transacción

A clase de transacción representa os diferentes tipos de custos nos que se incorre nos proxectos. Isto está representado por un conxunto de opcións que ten os seguintes valores admitidos en Project Operations:

  - Tempo
  - Gasto
  - Material
  - Cota
  - Fito
  - Impostos

**Fito** utilízase normalmente pola lóxica de negocio para a facturación con prezos fixos en Project Operations.

### <a name="transaction-origin"></a>Orixe da transacción

**Orixe da transacción** é unha entidade que almacena a orixe de cada transacción comercial. Cando se inicia un proxecto, cada transacción comercial dará lugar a outra transacción comercial que á súa vez creará outra, etc. A entidade de orixe da transacción está deseñada para almacenar datos sobre a orixe de cada transacción para axudar aos informes e á trazabilidade. 

### <a name="transaction-connection"></a>Conexión da transacción

**Conexión de transacción** é unha entidade que almacena a relación entre dúas transaccións comerciais similares, como os datos reais de custo e as vendas relacionadas ou as inversións de transaccións desencadeadas por actividades de facturación como a confirmación de facturas ou as correccións de facturas.

En conxunto, **Orixe de transacción** e **Conexión de transacción** axudan a rastrexar as relacións entre as transaccións comerciais e as accións que deron lugar a unha transacción comercial específica.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplo: Como funciona Orixe de transacción con Conexión de transacción

O seguinte exemplo mostra o procesamento típico de entradas de tempo nun ciclo de vida dun proxecto de Project Operations.

> ![Entradas de tempo de procesamento nun ciclo de vida de Project Service.](media/basic-guide-17.png)
 
1. O envío dunha entrada de tempo crea dúas liñas de diario: unha liña para o custo e outra liña para as vendas sen facturar.
2. A aprobación posterior da entrada de tempo crea de dous datos reais: un dato real para o custo e un dato real para as vendas sen facturar.
3. Cando se crea unha nova factura de proxecto, a transacción da liña de factura créase mediante datos de vendas non facturadas. 
4. Cando se confirma a factura, créanse dous novos datos reais: un dato real de reversión de vendas sen facturar e un dato real de vendas facturadas.

Cada un destes eventos crea un rexistro nas entidades **Orixe de transacción** e **Conexión de transacción**. Estes novos rexistros axudan a construír un historial de relacións entre os rexistros que se crean en entrada de tempo, liña do diario, datos reais e detalles da liña de factura.

Na seguinte táboa móstranse os rexistros da entidade de **Orixe da transacción** para o fluxo de traballo.

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

Na seguinte táboa móstranse os rexistros da entidade de **Conexión da transacción** para o fluxo de traballo.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
