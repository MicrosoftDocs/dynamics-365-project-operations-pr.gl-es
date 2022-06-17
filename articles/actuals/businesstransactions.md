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

En Microsoft Dynamics 365 Project Operations, *comercial* é un concepto abstracto que non está representado por ningunha entidade. Non obstante, algúns campos e procesos comúns en entidades están deseñados para empregar o concepto de transaccións comerciais. As seguintes entidades usan esta abstracción:

- Detalles da liña de oferta
- Detalles da liña de contrato
- Liñas de estimación
- Liñas de diario
- Valores reais

Destas entidades, os detalles da liña de cotización, os detalles da liña de contrato e as liñas de estimación están asignados ao *fase de estimación* no ciclo de vida do proxecto. As liñas do Diario e as entidades Reais están mapeadas ao *fase de execución* no ciclo de vida do proxecto.

Project Operations trata os rexistros destas cinco entidades como transaccións comerciais. A única distinción é que se consideran os rexistros das entidades que se asignan á fase de estimación (detalles da liña de cotización, detalles da liña de contrato e liñas de estimación).*previsións financeiras*, mentres que se consideran rexistros nas entidades que se asignan á fase de execución (liñas de diario e reais).*feitos financeiros* que xa ocorreron.

Para obter máis información, consulte [Estimacións](../project-management/estimating-projects-overview.md) e [Datos reais](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptos exclusivos das transaccións comerciais

Os conceptos seguintes son exclusivos do concepto de transaccións comerciais:

- Tipo de transacción
- Clase de transacción
- Orixe da transacción
- Conexión da transacción

### <a name="transaction-type"></a>Tipo de transacción

O tipo de transacción representa o momento e o contexto do impacto financeiro nun proxecto. Está definido por un conxunto de opcións que ten os seguintes valores admitidos en Operacións do proxecto:

- Custo
- Contrato do proxecto
- Vendas sen facturar
- Vendas facturadas
- Vendas entre organizacións
- Custo da unidade de recursos

### <a name="transaction-class"></a>Clase de transacción

A clase de transacción representa os diferentes tipos de custos nos que se incorre nos proxectos. Está definido por un conxunto de opcións que ten os seguintes valores admitidos en Operacións do proxecto:

- Tempo
- Gasto
- Material
- Cota
- Fito
- Impostos

> [!NOTE]
> O **Fito** O valor adoita ser usado pola lóxica empresarial para a facturación a prezos fixos en Operacións do proxecto.

### <a name="transaction-origin"></a>Orixe da transacción

A orixe da transacción é unha entidade que almacena a orixe de cada transacción comercial para axudar aos informes e a rastrexabilidade. Cando comeza a execución do proxecto, cada transacción comercial crea outra transacción comercial que, á súa vez, creará outra transacción comercial, etc.

### <a name="transaction-connection"></a>Conexión de transacción

A conexión de transacción é unha entidade que almacena a relación entre dúas transaccións comerciais similares, como custos e vendas reais relacionadas ou reversións de transaccións que se desencadean por actividades de facturación como a confirmación de facturas ou as correccións de facturas.

Xuntos, as entidades Orixe da transacción e conexión da transacción axúdanche a rastrexar as relacións entre as transaccións comerciais e as accións que provocaron a creación dunha transacción comercial específica.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
