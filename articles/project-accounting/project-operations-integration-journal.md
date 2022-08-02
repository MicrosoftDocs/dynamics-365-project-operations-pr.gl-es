---
title: Diario de integración en Project Operations
description: Este artigo ofrece información sobre como traballar co diario de integración en Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106273"
---
# <a name="integration-journal-in-project-operations"></a>Diario de integración en Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Crear entradas de tempo, gasto, taxa e material **Real** transaccións que representan a visión operativa do traballo realizado nun proxecto. Dynamics 365 Project Operations ofrece aos contables unha ferramenta para revisar as transaccións e axustar os atributos de contabilidade segundo sexa necesario. Despois de completar a revisión e os axustes, as transaccións contabilízanse no libro auxiliar e o libro maior do proxecto. Un contable pode realizar estas actividades usando o **Integración das operacións do proxecto** diario (**Dynamics 365 Finance** > **Xestión de proxectos e contabilidade** > **Xornais** > **Integración das operacións do proxecto** xornal.

![Fluxo de diario de integración.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Crear rexistros no diario de Project Operations Integration

Os rexistros no diario de Project Operations Integration créanse mediante un proceso periódico, **Importar desde a táboa de transición**. Podes executar este proceso indo a **Dynamics 365 Finance** > **Xestión de proxectos e contabilidade** > **Periódico** > **Integración das operacións do proxecto** > **Importar desde a táboa de preparación**. Pode executar o proceso de forma interactiva ou configuralo para que se execute en segundo plano segundo sexa necesario.

Cando se executa o proceso periódico, atoparanse os datos reais que aínda non se engadiron a Project Operations Integration. Créase unha liña de diario para cada transacción real.
O sistema agrupa as liñas de diarios en diarios separados en función do valor seleccionado no **Unidade de período sobre Xornada de Integración de Operacións do Proxecto** campo (**Finanzas** > **Xestión de proxectos e contabilidade** > **Montar** > **Xestión de proxectos e parámetros contables**, **do proxecto en Dynamics 365 Customer Engagement** ficha). Os valores posibles para este campo inclúen:

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
    - Se **Categoría de transacción** non está definido no Proxecto real, o sistema usa o valor do proxecto **Valores predeterminados da categoría do proxecto** campo no **Operacións do proxecto en Dynamics 365 Customer Engagement** ficha na **Xestión de proxectos e parámetros contables** páxina.
  - O campo **Recurso** representa o recurso do proxecto relacionado con esta transacción. O recurso úsase como referencia nas propostas de factura do proxecto aos clientes.
  - O **Taxa de cambio** campo predeterminado de **Tipo de cambio da moeda** establecido en Dynamics 365 Finance. Se falta a configuración da taxa de cambio, o proceso periódico **Importar desde a transición** non engadirá o rexistro a un diario e engadirase unha mensaxe de erro ao rexistro de execución do traballo.
  - O campo **Propiedade de liña** representa o tipo de facturación nos datos reais do proxecto. A propiedade da liña e a asignación do tipo de facturación defínense no **Operacións do proxecto en Dynamics 365 Customer Engagement** ficha na **Xestión de proxectos e parámetros contables** páxina.

Só se poden actualizar os seguintes atributos de contabilidade nas liñas do diario de Project Operations Integration:

- **Grupo de impostos sobre vendas de facturación** e **Grupo de impostos sobre vendas individuais de facturación**
- **Dimensións financeiras** (usando a acción **Distribuír importes**)

As liñas do diario de integración pódense eliminar. Non obstante, todas as liñas non publicadas inseriranse de novo no diario despois de volver executar o **Importar desde a posta en escena** proceso periódico.

### <a name="post-the-project-operations-integration-journal"></a>Publicar o diario de integración de Project Operations

Ao contabilizar diario de Integration, créanse transaccións de libro auxiliar e libro maior do proxecto. Estas úsanse na facturación posterior aos clientes, no recoñecemento de ingresos e na presentación de informes financeiros.

Pódese publicar o diario de integración de Project Operations seleccionado usando **Publicación** na páxina do diario de integración de Operacións do proxecto. Todas as revistas pódense publicar automaticamente executando un proceso en **Periódicos** > **Integración das operacións do proxecto** > **Diario de integración de operacións posteriores ao proxecto**.

A publicación pódese realizar de forma interactiva ou por lotes. Teña en conta que todas as revistas que teñan máis de 100 liñas publicaranse automaticamente nun lote. Para un mellor rendemento cando as revistas que teñen moitas liñas se publican nun lote, habilite a opción **Publicar un diario de integración de operacións do proxecto usando varias tarefas por lotes** característica no **Xestión de características** espazo de traballo. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Transferir todas as liñas que teñan erros de publicación a unha nova revista

> [!NOTE]
> Para usar esta capacidade, habilite o **Transfire todas as liñas con erros de publicación a un novo diario de integración de Project Operations** característica no **Xestión de características** espazo de traballo.

Durante a publicación no diario de integración de Operacións do proxecto, o sistema valida todas as liñas do diario. O sistema publica todas as liñas que non teñen erros e crea un novo diario para todas as liñas que teñan erros de publicación. Para revisar as revistas que teñen liñas de erro de publicación, vai a **Xestión de proxectos e contabilidade** > **Xornais** > **Diario de integración de operacións de proxectos**, e filtra as revistas usando o **Xornal orixinal** campo.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
