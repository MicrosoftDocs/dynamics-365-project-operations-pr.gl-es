---
title: Diario de integración en Project Operations
description: Este artigo ofrece información sobre como traballar co diario de Integration en Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541075"
---
# <a name="integration-journal-in-project-operations"></a>Diario de integración en Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

As entradas de tempo, tarifa e material crean transaccións de **Dato real** que representan a visión operativa do traballo realizado respecto a un proxecto. Dynamics 365 Project Operations ofrece aos contables unha ferramenta para revisar as transaccións e axustar os atributos de contabilidade segundo sexa necesario. Despois de completar a revisión e os axustes, as transaccións contabilízanse no libro auxiliar e o libro maior do proxecto. Un contable pode realizar estas actividades usando o diario de **Project Operations Integration** (**Dynamics 365 Finance** > **Xestión e contabilidade de proxectos** > **Diarios** > **Project Operations Integration**.

![Fluxo de diario de integración.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Crear rexistros no diario de Project Operations Integration

Os rexistros no diario de Project Operations Integration créanse mediante un proceso periódico, **Importar desde a táboa de transición**. Pode executar este proceso indo a **Dynamics 365 Finance** > **Xestión e contabilidade de proxectos** > **Periódico** > **Project Operations Integration** > **Importar desde a táboa de transición**. Pode executar o proceso de forma interactiva ou configuralo para que se execute en segundo plano segundo sexa necesario.

Cando se executa o proceso periódico, atoparanse os datos reais que aínda non se engadiron a Project Operations Integration. Créase unha liña de diario para cada transacción real.
O sistema agrupa as liñas de diario en diarios separados en función do valor seleccionado no campo **Unidade de período no diario de Project Operations Integration** (separador **Finance** > **Xestión e contabilidade de proxectos** > **Configuración** > **Parámetros de xestión e contabilidade de proxectos**, **Project Operations en Dynamics 365 Customer Engagement**). Os valores posibles para este campo inclúen:

  - **Días**: Os datos reais agrúpanse por data de transacción. Créase un diario separado para cada día.
  - **Meses**: Os datos reais agrúpanse por mes natural. Créase un diario separado para cada mes.
  - **Anos**: Os datos reais agrúpanse por ano natural. Créase un diario separado para cada ano.
  - **Todas**: Todas as transaccións reais están incluídas no mesmo diario de integración. Se o diario non está dispoñible cando se executa o proceso periódico, por exemplo, se o diario está en proceso de contabilizar transaccións, créase un novo diario.

As liñas de diario créanse en función dos datos reais do proxecto. A seguinte lista inclúe algunhas das regras por defecto e de transformación máis notables:

  - Cada transacción real do proxecto ten unha liña no diario de Project Operations Integration. O custo e as transaccións de vendas non facturadas para o tipo de facturación de tempo e material móstranse en liñas separadas.
  - O campo **Data** representa a data da transacción. O campo **Data de contabilidade** representa a data na que se rexistrou a transacción no libro maior. Se a data de contabilidade está nun [período financeiro pechado](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) e o parámetro **Establecer automaticamente a data de contabilidade para abrir o período do libro maior** está configurado no separador **Actividades financeiras** da páxina **Parámetros de xestión e contabilidade de proxectos**, o sistema axustará a data de contabilidade da transacción á primeira data do próximo período de libro maior aberto.
  - O campo **Vale** mostra o número do vale para cada transacción real. A secuencia numérica do vale defínese no separador **Secuencias numéricas**, na páxina **Parámetros de xestión e contabilidade de proxectos**. Cada liña ten asignado un novo número. Despois de contabilizar o vale, pode ver como se relacionan o custo e as transaccións de vendas sen facturar seleccionando **Vales relacionados** na páxina **Transacción de vale**.
  - O campo **Categoría** representa unha transacción do proxecto e os valores predefinidos baséanse na categoría de transacción para o dato real do proxecto relacionado.
    - Se **Categoría de transacción** está definida no dato real do proxecto real e existe unha **Categoría de proxecto** relacionada nunha entidade xurídica determinada, a categoría é por defecto esta categoría de proxecto.
    - Se **Categoría de transacción** non está definida no dato real do proxecto, o sistema usa o valor do campo **Valores predefinidos da categoría do proxecto** no separador **Project Operations en Dynamics 365 Customer Engagement** na páxina **Parámetros de xestión e contabilidade de proxectos**.
  - O campo **Recurso** representa o recurso do proxecto relacionado con esta transacción. O recurso úsase como referencia nas propostas de factura do proxecto aos clientes.
  - O campo **Taxa de cambio** é por defecto a **Taxa de cambio** establecida en Dynamics 365 Finance. Se falta a configuración da taxa de cambio, o proceso periódico **Importar desde a transición** non engadirá o rexistro a un diario e engadirase unha mensaxe de erro ao rexistro de execución do traballo.
  - O campo **Propiedade de liña** representa o tipo de facturación nos datos reais do proxecto. A asignación de propiedades de liña e o tipo de facturación defínense no separador **Project Operations en Dynamics 365 Customer Engagement** na páxina **Parámetros de xestión e contabilidade de proxectos**.

Só se poden actualizar os seguintes atributos de contabilidade nas liñas do diario de Project Operations Integration:

- **Grupo de impostos sobre vendas de facturación** e **Grupo de impostos sobre vendas individuais de facturación**
- **Dimensións financeiras** (usando a acción **Distribuír importes**)

Pódense eliminar as liñas de diario de integración. Con todo, as liñas non publicadas inseriranse no diario de novo despois de volver executar o proceso periódico **Importar desde a transición**.

### <a name="post-the-project-operations-integration-journal"></a>Contabilizar o diario de integración de Project Operations

Ao contabilizar diario de Integration, créanse transaccións de libro auxiliar e libro maior do proxecto. Estas úsanse na facturación posterior aos clientes, no recoñecemento de ingresos e na presentación de informes financeiros.

Pódese contabilizar o diario de integración de Project Operations seleccionado usando **Contabilizar** na páxina do diario de integración de Project Operations. Todos os diarios pódense publicar automaticamente executando un proceso en **Periódicos** > **Integración de Project Operations** > **Contabilizar diario de integración de Project Operations**.

A contabilización pódese realizar de forma interactiva ou por lotes. Teña en conta que todos os diarios que teñan máis de 100 liñas contabilizaranse automaticamente nun lote. Para un mellor rendemento cando os diarios que teñen moitas liñas se publican nun lote, active a funcionalidade **Contabilizar un diario de integración de Project Operations usando varias tarefas por lotes** na área de traballo **Xestión de funcionalidades**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Transferir todas as liñas que teñan erros de contabilización a un novo diario

> [!NOTE]
> Para usar esta capacidade, active a funcionalidade **Transferir todas as liñas con erros de contabilización a un novo diario de integración de Project Operations** na área de traballo **Xestión de funcionalidades**.

Esta funcionalidade axuda a mellorar a experiencia co diario de integración de Project Operations. Cando está activada, os problemas de sincronización de escrita dual e os problemas de configuración xa non impiden que se contabilicen diarios válidos. Durante a contabilización no diario de integración de Project Operations, o sistema valida todas as liñas do diario. Contabiliza todas as liñas que non teñen erros e crea un novo diario para todas as liñas que teñan erros de contabilización.

Para revisar os diarios que teñen liñas de erro de contabilización, vaia a **Xestión e contabilidade de proxectos** \> **Diarios** \> **Diario de integración de Project Operations** e filtre a lista de diarios usando o campo **Diario orixinal**. A seguinte ilustración mostra un exemplo onde as os diarios da páxina **Diario de integración de Project Operations** se filtraron deste xeito.

![Diario orixinal que se mostra na páxina do diario de integración de Project Operations.](./media/transferLines-originalJournal.png)

Se se configura un traballo por lotes periódico para publicar o diario de integración, tentarase de novo a contabilización e contabilizaranse os diarios se se solucionou o problema de sincronización. Os diarios restantes deberían ser investigados manualmente revisando os rexistros e tomando as medidas necesarias.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
