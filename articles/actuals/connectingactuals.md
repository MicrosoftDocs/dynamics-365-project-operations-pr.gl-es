---
title: Conexións de transaccións - Ligar datos reais de diferentes tipos de transaccións
description: Este artigo explica como se usa unha conexión de transacción para vincular datos reais de diferentes tipos para axudar a rastrexar a rendibilidade, os traballo pendentes de facturación e os cálculos dos ingresos facturados e non facturados.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926084"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Conexións de transaccións - Ligar datos reais de diferentes tipos de transaccións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os rexistros de conexión de transacción créanse para vincular datos reais de diferentes tipos a medida que o tempo, o gasto ou o uso do material se move no seu ciclo de vida desde a fase de oferta ou prevenda ata a fase do contrato, aprobacións e/ou retiradas, facturación e, potencialmente, a facturación de crédito ou de corrección.

O seguinte exemplo mostra o procesamento típico de entradas de tempo nun ciclo de vida dun proxecto de Project Operations.

> ![Procesamento de entradas de tempo en Project Operations.](media/basic-guide-17.png)

O procesamento de entradas de tempo nun ciclo de vida dun proxecto de Project Operations sigue estes pasos: 

1. O envío dunha entrada de tempo provoca a creación de dúas liñas de diario: unha para o custo e outra para as vendas sen facturar. 
2. A aprobación posterior da entrada de tempo provoca a creación de dous datos reais: un para o custo e outro para as vendas sen facturar. Estes dous datos reais están ligados mediante conexións de transacción.
3. Cando o usuario crea unha factura de proxecto, a transacción da liña de factura créase mediante datos de vendas non facturadas.
4. Cando se confirma a factura, créanse dous novos datos reais: unha reversión de vendas sen facturar e un dato real de vendas facturadas. A reversión de vendas non facturadas e as vendas reais non facturadas orixinais conéctanse mediante conexións de reversión de transacción. Os datos reais de vendas facturadas e vendas non facturadas orixinais tamén están conectados para mostrar os vínculos entre o que antes eran traballos pendentes ou traballos en curso (WIP) co que agora é ingresos facturados.   

Cada evento no fluxo de traballo de procesamento desencadea a creación de rexistros na táboa **Conexión de transacción**. Isto axuda a construír un rastrexo de relacións entre os rexistros que se crean en entrada de tempo, liña do diario, dato real e detalles da liña de factura.

Na seguinte táboa móstranse os rexistros da entidade de **Conexión da transacción** para o fluxo de traballo anterior.

|Evento                   |Transacción 1                 |Rol de transacción 1 |Tipo de transacción 1       |Transacción 2          |Rol de transacción 2 |Tipo de transacción 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Envío de entrada de tempo   |GUID de liña de diario (vendas)     |Vendas sen facturar |msdyn_journalline            |GUID de liña de diario (custo)     |Custo            |msdyn_journalline  |
|Aprobación de tempo           |GUID de dato real de vendas sen facturar  |Vendas sen facturar |msdyn_actual                 |GUID de dato real de custo (custo)       |Custo            |msdyn_actual       |
|Creación de facturas        |GUID de detalle da liña de factura      |Vendas facturadas   |msdyn_invoicelinetransaction |GUID de dato real de vendas sen facturar   |Vendas sen facturar  |msdyn_actual       |
|Confirmación de factura    |GUID de dato real de reversión         |Reversión      |msdyn_actual                 |GUID de vendas sen facturar orixinais |Orixinal        |msdyn_actual       |
|                        |GUID de vendas facturadas             |Vendas facturadas   |msdyn_actual                 |GUID de dato real de vendas sen facturar   |Vendas sen facturar  |msdyn_actual       |
|Corrección de borrador de factura |GUID de transacción da liña de factura|Substitución      |msdyn_invoicelinetransaction |GUID de vendas facturadas            |Orixinal        |msdyn_actual       |
|Confirmar corrección de factura|GUID de reversión de vendas facturadas  |Reversión      |msdyn_actual                 |GUID de vendas facturadas            |Orixinal        |msdyn_actual       |
|                        |Nova GUID de vendas non facturadas |Substitución            |msdyn_actual                 |GUID de vendas facturadas            |Orixinal        |msdyn_actual       |


A seguinte ilustración mostra as ligazóns que se crean entre diferentes tipos de datos reais en varios eventos usando o exemplo de entradas de tempo en Project Operations.

> ![Como os datos reais de diferentes tipos están ligados entre si en Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
