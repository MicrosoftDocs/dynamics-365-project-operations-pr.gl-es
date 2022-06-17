---
title: 'Orixes da transacción: vincula os datos reais á súa fonte'
description: Este artigo explica como se usa o concepto de orixe das transaccións para vincular datos reais aos rexistros orixinais de orixe, como a entrada de tempo, a entrada de gastos ou os rexistros de uso de material.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921300"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Orixes da transacción: vincula os datos reais á súa fonte

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os rexistros de orixe das transaccións créanse para vincular os datos reais á súa orixe, como as entradas de tempo, as entradas de gastos, os rexistros de uso de material e as facturas do proxecto.

O seguinte exemplo mostra o procesamento típico de entradas de tempo nun ciclo de vida dun proxecto de Project Operations.

> ![Tempo de procesamento completo en Operacións do proxecto.](media/basic-guide-17.png)
 
1. O envío dunha entrada de tempo fai que se creen dúas liñas de diario: unha para o custo e outra para as vendas non facturadas.
2. A aprobación eventual da entrada de tempo fai que se creen dous reais: un para o custo e outro para as vendas non facturadas.
3. Cando o usuario crea unha factura de proxecto, a transacción da liña de factura créase mediante datos de vendas non facturadas.
4. Cando se confirma a factura, créanse dous novos datos reais: unha reversión de vendas sen facturar e un dato real de vendas facturadas.

Cada evento deste fluxo de traballo de procesamento desencadea a creación de rexistros na entidade de orixe da transacción para axudar a construír un rastro das relacións entre estes rexistros que se crean a través da entrada de tempo, liña do diario, detalles reais e da liña de factura.

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
| GUID de factura de corrección      | Factura                  | GUID de dato real de novas vendas sen facturar    | Dato real                            |                          |


A seguinte ilustración mostra as ligazóns que se crean entre os datos reais e as súas fontes en varios eventos usando o exemplo de entradas de tempo en Operacións do proxecto.

> ![Como se vinculan os datos reais aos rexistros de orixe en Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
