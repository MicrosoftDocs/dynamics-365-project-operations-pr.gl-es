---
title: 'Novidades de xuño de 2022: despregamento de Project Operations lite'
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de xuño de 2022 do despregamento lite de Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031191"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novidades de xuño de 2022: despregamento de Project Operations lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.43.0.77 ou 4.43.0.119

## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Subcontratación | 2708885 | Corrixiuse a mensaxe de erro que aparece cando un usuario crea un rexistro de cabeceira de reserva de recursos reservables onde non se enche ningún recurso reservable. |
| Planificación e rastrexo de proxectos | 2629441 | Corrixiuse a lóxica de activación do fluxo de traballo para axudar a evitar un bucle infinito cando se actualizan as tarefas do proxecto. |
| Tempo e gasto | 2641209 | As importacións de entradas de tempo desde tarefas/reservas deben conservar unha referencia de recurso reservable. |
| Planificación e rastrexo de proxectos | 2651148 | A cabeceira do documento do proxecto debe estar protexida.|
| Planificación e rastrexo de proxectos | 2653145 | Engadíronse validacións para garantir que non se pode crear un rexistro de proxecto que teña caracteres non válidos no seu nome. |
| Tempo e gasto | 2654710 | Corrixiuse o filtrado na páxina **Aprobacións**. |
| Facturación e prezos | 2667805 | Engadíronse validacións para evitar que se creen datos reais de vendas facturadas se non existe o respaldo dos datos reais de vendas non facturadas. |
| Facturación e prezos | 2668378 | Engadíronse validacións para evitar que se engada unha dimensión de prezos personalizada a menos que se encha un nome lóxico e un nome de campo. |
| Tempo e gasto | 2700428 | Mellorouse a lóxica de aprobacións para garantir que se poidan procesar outros conxuntos de aprobacións para o proxecto aínda que un dos conxuntos de aprobacións estea atascado en traballos do sistema. |
