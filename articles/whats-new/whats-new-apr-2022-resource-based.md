---
title: Novidades de abril de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de Microsoft de abril de 2022 Dynamics 365 Project Operations para escenarios baseados en recursos/non abastecidos.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912376"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de abril de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.41.0.45
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.26

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As categorías de adquisición pódense utilizar en pedidos de compra de proxectos e facturas de provedores pendentes. Para obter máis información, consulte [Use categorías de adquisición con pedidos de compra de proxectos e facturas de provedores pendentes](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte táboa mostra os mapas de dobre escritura que se modificaron ou engadiron na versión de marzo de 2022 de Project Operations.

| Asignación de entidades | Versión actualizada | Comentarios |
| -------------- | ------------------- | ------------|
| Entidade de exportación de liña de factura do provedor do proxecto de integración de operacións do proxecto msdyn\_ liñas de facturas do provedor do proxecto | 1.0.0.4 | Este mapa admite o uso de categorías de adquisición con pedidos de compra e facturas de provedores pendentes. |

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, siga as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| ------------ | ---------------- | -------------- |
| Tempo e gasto | 2573900 | O **Aprobación Moderna** a función debe estar activada por defecto. |
| Facturación e prezos | 2603313 | Corrixiuse un erro de rexistro duplicado que impedía que se engadesen liñas de cotización e contrato que tiñan un produto. |
| Implantación e configuración | 2611368 | Os clientes deben poder engadir ata cinco entidades personalizadas á solución mediante o deseñador de aplicacións moderno. |
| Tempo e gasto | 2628285 | Solucionouse un problema que afectaba á posibilidade de establecer a categoría de recurso correcta durante a importación da entrada de tempo. |
|   Xestión de oportunidades| 2628815 | Actualiza o límite de caracteres da descrición detallada da liña de comiñas para que coincida co límite de caracteres do asunto da tarefa, para que a importación se realice correctamente para as tarefas nas que o asunto supere os 100 caracteres. |
| Tempo e gasto| 2629547 | O **Enviado por** O campo de aprobación do proxecto debe sinalar o usuario que presentou o rexistro. |
| Tempo e gasto| 2629865 | O **Categoría de copia** campo sobre tarefas cando se copian proxectos. |
| Tempo e gasto| 2636463 | Arranxáronse os filtros das aprobacións nos formularios de aprobacións modernos. |
| Planificación e rastrexo de proxectos | 2648300 | Solucionouse un problema que impedía que se cambiase o propietario do proxecto. |
| Facturación e prezos | 2563000 | Non se deben permitir liñas de diario para unha venda sen facturar na que a moeda difire da moeda do contrato. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión de proxectos e contabilidade en Dynamics 365 Finance

Para obter información sobre as correccións de erros que se inclúen nesta actualización, inicie sesión en Microsoft Dynamics Servizos de ciclo de vida (LCS) e consulte [Artigo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
