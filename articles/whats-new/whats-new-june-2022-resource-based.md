---
title: Novidades de xuño de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de xuño de 2022 de Microsoft Dynamics 365 Project Operations para escenarios baseados en recursos/non abastecidos.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959632"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de xuño de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.43.0.77
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte táboa mostra os mapas de dobre escritura que se modificaron ou engadiron na versión de xuño de 2022 de Project Operations.

| Asignación de entidades | Versión actualizada | Comentarios |
| --- | --- | --- |
| Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | O campo heredado quedou en desuso e mapeouse co novo campo para o seguimento do estado da factura do provedor. |

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, siga as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

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
| Subcontratación | 2677485 | Actualizouse a versión de destino do mapa de dobre escritura das liñas de factura do provedor. |
| Tempo e gasto | 2700428 | Mellorouse a lóxica de aprobacións para garantir que se poidan procesar outros conxuntos de aprobación para o proxecto aínda que un dos conxuntos de aprobación estea atascado en traballos do sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión de proxectos e contabilidade en Finanzas

Para obter información sobre as correccións de erros que se inclúen nesta actualización, inicie sesión en Microsoft Dynamics Servizos de ciclo de vida (LCS) e consulte [Artigo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
