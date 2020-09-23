---
title: Novidades ou cambios na versión 3.x onda 1 2020 de Project Service Automation
description: Este tema fornece información sobre as novidades e as modificacións na versión 3 onda 1 2020 de Project Service Automation.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751381"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novidades ou cambios na versión 3 onda 1 2020 de Project Service Automation
O tema resalta as principais consideracións da actualización ao pasar á última versión de Project Service Automation (PSA) versión 3.x onda 1 2020.

## <a name="time-entry"></a>Entrada de tempo
A experiencia de entrada de tempo ampliouse para ofrecer capacidades para ampliar a entrada de tempo a máis escenarios de clientes. Isto inclúe a capacidade de engadir tipos de entrada, que agora favorecen un comportamento específico baseado no nome do esquema de campo **Configuración de entrada de hora**, amosado como **Orixe de tempo**.

### <a name="upgrade-consideration"></a>Consideración sobre a actualización
Para apoiar esta funcionalidade, os roles dentro de PSA actualizáronse para incluír novos privilexios. Estes privilexios conceden acceso de lectura á nova entidade, **Configuración de entrada de hora**.

Os usuarios que requiran a capacidade de rexistro de tempo deben recibir o rol de usuario **Usuario de entrada de tempo** ademais dos roles existentes. Este papel inclúe a nova funcionalidade e garante que a entrada de tempo seguirá funcionando.

### <a name="currently-extended-time-entry-changes"></a>Cambios de entrada de tempo ampliado actualmente
Para minimizar o impacto para os usuarios actuais de entrada de tempo, este cambio de rol é o único requisito básico necesario para continuar utilizando a entrada de tempo. Se creou vistas personalizadas ou experiencias de entrada de tempo independentes, ten que configurar os campos de **Configuración de entrada de tempo** co valor de PSA correcto.
