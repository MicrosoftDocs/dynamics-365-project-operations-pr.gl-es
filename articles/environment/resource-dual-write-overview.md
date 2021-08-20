---
title: Integración de escrita dual de Project Operations
description: Este tema ofrece unha visión xeral da integración da escrita dual de Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007909"
---
# <a name="project-operations-dual-write-integration-overview"></a>Visión xeral da integración de escrita dual de Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Project Operations usa as [capacidades de escrita dual](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar datos entre Microsoft Dataverse e Dynamics 365 Finance.

A seguinte ilustración mostra como se sincronizan os datos como parte desta integración entre Dataverse e Finance.

![Visión xeral dos fluxos de datos de Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations en Dataverse ofrece unha interface de usuario moderna (IU) e unha fácil extensibilidade sen código/de código baixo utilizando as capacidades de Power Platform. Xestores de proxectos, xestores de recursos, membros do equipo do proxecto e outras persoas de atención ao cliente realizan as súas actividades en Project Operations en Dataverse.

Project Operations en Finance ofrece asistencia para recoñecemento de ingresos e contabilidade de proxectos. Project Operations conéctase ao marco financeiro de Finance para o cálculo do imposto sobre as vendas, as taxas de cambio de divisas, a información de dimensións financeiras e moito máis. As experiencias do contable do proxecto baséanse principalmente en Finance.

A integración de Project Operations consiste na seguinte integración de compoñentes:


- [Integración de datos de instalación e configuración de Project Operations](resource-dual-write-setup-integration.md) 
- [Estimacións e datos reais do proxecto](resource-dual-write-estimates-actuals.md)
- [Facturas do proxecto](resource-dual-write-project-invoice.md)
- [Xestión de gastos](resource-dual-write-expense.md)
- [Factura do fornecedor](resource-dual-write-vendor-invoice.md)
