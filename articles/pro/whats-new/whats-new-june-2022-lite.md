---
title: 'Novidades de xuño de 2022: despregamento de Project Operations lite'
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de xuño de 2022 de Microsoft Dynamics 365 Project Operations despregamento lite.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959618"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novidades de xuño de 2022: despregamento de Project Operations lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.43.0.77

## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Subcontratación | 2708885 | Corrixiuse a mensaxe de erro que aparece cando un usuario crea un rexistro de cabeceira de reserva de recursos reservables onde non se enche ningún recurso reservable. |
| Planificación e rastrexo de proxectos | 2629441 | Corrixiuse a lóxica de activación do fluxo de traballo para axudar a evitar un bucle infinito cando se actualizan as tarefas do proxecto. |
| Tempo e gasto | 2641209 | As importacións de entradas de tempo de tarefas/reservas deben conservar unha referencia de recurso reservable. |
| Planificación e rastrexo de proxectos | 2651148 | A cabeceira do documento do proxecto debe estar protexida.|
| Planificación e rastrexo de proxectos | 2653145 | Engadíronse validacións para garantir que non se pode crear un rexistro de proxecto que teña caracteres non válidos no seu nome. |
| Tempo e gasto | 2654710 | Corrixiuse o filtrado no **Aprobacións** páxina. |
| Facturación e prezos | 2667805 | Engadíronse validacións para evitar que se creen reais de vendas facturadas se non existe o respaldo dos reais de vendas non facturados. |
| Facturación e prezos | 2668378 | Engadíronse validacións para evitar que se engada unha dimensión de prezos personalizado a menos que se enche un nome lóxico e un nome de campo. |
| Tempo e gasto | 2700428 | Mellorouse a lóxica de aprobacións para garantir que se poidan procesar outros conxuntos de aprobación para o proxecto aínda que un dos conxuntos de aprobación estea atascado en traballos do sistema. |
