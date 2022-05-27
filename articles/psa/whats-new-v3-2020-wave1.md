---
title: Novidades ou cambios na versión 3.x onda 1 2020 de Project Service Automation
description: Este tema fornece información sobre as novidades e as modificacións na versión 3 onda 1 2020 de Project Service Automation.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577878"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novidades ou cambios na versión 3 onda 1 2020 de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

O tema resalta as principais consideracións da actualización ao pasar á última versión de Project Service Automation (PSA) versión 3.x onda 1 2020.

## <a name="time-entry"></a>Entrada de tempo
A experiencia de entrada de tempo ampliouse para ofrecer capacidades para ampliar a entrada de tempo a máis escenarios de clientes. Isto inclúe a capacidade de engadir tipos de entrada, que agora favorecen un comportamento específico baseado no nome do esquema de campo **Configuración de entrada de hora**, amosado como **Orixe de tempo**. Engadiuse unha nova solución, chamada Time, Expense, Statusing, and Approvals (TESA) para permitir esta funcionalidade.

### <a name="upgrade-consideration"></a>Consideración sobre a actualización
Para apoiar esta funcionalidade, os roles dentro de PSA actualizáronse para incluír novos privilexios. Estes privilexios conceden acceso de lectura á nova entidade, **Configuración de entrada de hora**.

Os usuarios que requiran a capacidade de rexistro de tempo deben recibir o rol de usuario **Usuario de entrada de tempo** ademais dos roles existentes. Este papel inclúe a nova funcionalidade e garante que a entrada de tempo seguirá funcionando.

Ademais, se ten módulos de aplicación personalizados que inclúan todos os formularios para a entidade de entrada de tempo, deberá eliminar o **Formulario de creación rápida da entradas de tempo de TESA** desde o módulo.

### <a name="currently-extended-time-entry-changes"></a>Cambios de entrada de tempo ampliado actualmente
Para minimizar o impacto para os usuarios actuais de entrada de tempo, este cambio de rol é o único requisito básico necesario para continuar utilizando a entrada de tempo. Se creou vistas personalizadas ou experiencias de entrada de tempo independentes, ten que configurar os campos de **Configuración de entrada de tempo** co valor de PSA correcto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
