---
title: Novidades de xuño de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de xuño de 2022 de Microsoft Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031329"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de xuño de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.43.0.77 ou 4.43.0.119
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte táboa mostra os mapas de escrita dual que foron modificados ou engadidos na versión de Project Operations de xuño de 2022.

| Asignación de entidades | Versión actualizada | Comentarios |
| --- | --- | --- |
| Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | O campo herdado quedou obsoleto e asignouse ao novo campo para o seguimento do estado da factura do fornecedor. |

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

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
| Subcontratación | 2677485 | Actualizouse a versión de destino do mapa de escrita dual das liñas de factura do fornecedor. |
| Tempo e gasto | 2700428 | Mellorouse a lóxica de aprobacións para garantir que se poidan procesar outros conxuntos de aprobacións para o proxecto aínda que un dos conxuntos de aprobacións estea atascado en traballos do sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión e contabilidade de proxectos en Finance

Para obter información sobre as correccións incluídas nesta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) e vexa o [artigo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
