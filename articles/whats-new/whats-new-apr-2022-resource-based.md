---
title: Novidades de abril de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de abril de 2022 de Microsoft Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110882"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de abril de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.41.0.45
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.26

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As categorías de adquisición pódense usar con pedidos de compra de proxectos e facturas de fornecedores pendentes. Para obter máis información, consulte [Usar categorías de adquisición con pedidos de compra de proxectos e facturas de fornecedores pendentes](../procurement/configure-procurement-categories.md)

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte táboa mostra os mapas de escrita dual que foron modificados ou engadidos na versión de Project Operations de marzo de 2022.

| Asignación de entidades | Versión actualizada | Comentarios |
| -------------- | ------------------- | ------------|
| Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Este mapa admite o uso de categorías de adquisición con pedidos de compra de proxectos e facturas de fornecedores pendentes. |

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| ------------ | ---------------- | -------------- |
| Tempo e gasto | 2573900 | A funcionalidade **Aprobación Moderna** debe estar activada por defecto. |
| Facturación e prezos | 2603313 | Corrixiuse un erro de rexistro duplicado que impedía que se engadisen liñas de oferta e contrato que tiñan un produto. |
| Despregamento e configuración | 2611368 | Os clientes deben poder engadir ata cinco entidades personalizadas á solución mediante o deseñador de aplicacións moderno. |
| Tempo e gasto | 2628285 | Solucionouse un problema que afectaba á posibilidade de establecer a categoría de recurso correcta durante a importación da entrada de tempo. |
|   Xestión de oportunidades| 2628815 | Actualice o límite de caracteres da descrición detallada da liña de oferta para que coincida co límite de caracteres do asunto da tarefa, de xeito que a importación teña éxito para as tarefas nas que o asunto supere os 100 caracteres. |
| Tempo e gasto| 2629547 | O campo **Enviado por** de aprobacións do proxecto debe sinalar ao usuario que enviou o rexistro. |
| Tempo e gasto| 2629865 | O campo **Copiar categoría** sobre tarefas cando se copian proxectos. |
| Tempo e gasto| 2636463 | Arranxáronse os filtros das aprobacións nos formularios de aprobacións modernos. |
| Planificación e rastrexo de proxectos | 2648300 | Solucionouse un problema que impedía que se cambiase o propietario do proxecto. |
| Facturación e prezos | 2563000 | Non se deben permitir liñas de diario para unha venda non facturada na que a moeda difire da moeda do contrato. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

Para obter información sobre as correccións incluídas nesta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) e vexa o [artigo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
