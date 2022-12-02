---
title: Transaccións empresariais en Project Operations
description: Este artigo ofrece unha visión xeral do concepto de transaccións comerciais en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923278"
---
# <a name="business-transactions-in-project-operations"></a>Transaccións empresariais en Project Operations

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

En Microsoft Dynamics 365 Project Operations, *transacción comercial* é un concepto abstracto que non representa ningunha entidade. Non obstante, algúns campos e procesos comúns en entidades están deseñados para empregar o concepto de transaccións comerciais. As seguintes entidades usan esta abstracción:

- Detalles da liña de oferta
- Detalles da liña de contrato
- Liñas de estimación
- Liñas de diario
- Valores reais

Destas entidades, Detalles de liña de oferta, Detalles de liña de contrato e Liñas de estimación asígnanse á *fase de estimación* no ciclo de vida do proxecto. As entidades Liñas de diario e Datos reais asígnanse á *fase de execución* no ciclo de vida do proxecto.

Project Operations trata rexistros nestas cinco entidades como transaccións comerciais. A única distinción é que os rexistros das entidades que se asignan á fase de estimación (detalles de liña de oferta, detalles de liña de contrato e detalles de estimación) considéranse *previsións financeiras*, mentres que os rexistros de entidades que se asignan á fase de execución (liñas de diario e datos reais) considéranse *feitos financeiros* que xa se produciron.

Para obter máis información, consulte [Estimacións](../project-management/estimating-projects-overview.md) e [Datos reais](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptos exclusivos das transaccións comerciais

Os conceptos seguintes son exclusivos do concepto de transaccións comerciais:

- Tipo de transacción
- Clase de transacción
- Orixe da transacción
- Conexión da transacción

### <a name="transaction-type"></a>Tipo de transacción

O tipo de transacción representa o momento e o contexto do impacto financeiro nun proxecto. Isto defínese por un conxunto de opcións que ten os seguintes valores admitidos en Project Operations:

- Custo
- Contrato do proxecto
- Vendas sen facturar
- Vendas facturadas
- Vendas entre organizacións
- Custo da unidade de recursos

### <a name="transaction-class"></a>Clase de transacción

A clase de transacción representa os diferentes tipos de custos nos que se incorre nos proxectos. Isto defínese por un conxunto de opcións que ten os seguintes valores admitidos en Project Operations:

- Tempo
- Gasto
- Material
- Cota
- Fito
- Impostos

> [!NOTE]
> O valor de **Fito** utilízase normalmente pola lóxica de negocio para a facturación con prezos fixos en Project Operations.

### <a name="transaction-origin"></a>Orixe da transacción

A orixe da transacción é unha entidade que almacena a orixe de cada transacción comercial para axudar aos informes e á trazabilidade. Cando a execución do proxecto comeza, cada transacción comercial crea a outra transacción comercial que, á súa vez, creará outra transacción comercial e así sucesivamente.

### <a name="transaction-connection"></a>Conexión de transacción

A conexión de transacción é unha entidade que almacena a relación entre dúas transaccións comerciais similares, como os datos reais de custo e as vendas relacionadas ou as inversións de transaccións que se desencadean por actividades de facturación como a confirmación de facturas ou as correccións de facturas.

En conxunto, as entidades Orixe de transacción e Conexión de transacción axudan a rastrexar as relacións entre as transaccións comerciais e as accións que provocaron que se crease unha operación comercial específica.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
