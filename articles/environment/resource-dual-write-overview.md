---
title: Integración de escrita dual de Project Operations
description: Este artigo ofrece unha visión xeral da integración da escrita dual de Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927970"
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
