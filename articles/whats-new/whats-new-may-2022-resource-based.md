---
title: Novidades de maio de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de maio de 2022 de Microsoft Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921392"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de maio de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.42.0.70
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade
### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión de recursos | 2634019 | Mensaxes de erro melloradas para validacións empresariais ao engadir membros xenéricos do equipo como recursos. |
| Planificación e rastrexo de proxectos | 2648515 | Actualizacións restrinxidas de **ownerid**, **state** e **status** en entidades de programación. |
| Facturación e prezos | 2653167 | O separador decimal da grade **Estimacións** debe seguir a configuración do formato en **Opcións persoais**. |
| Facturación e prezos| 2662251 | Os valores dos campos **Unidade corrixida** e **Grupo de unidades** son os predefinidos ao crear rexistros en estimacións de materiais. |
| Facturación e prezos| 2571408 | Os datos reais de vendas sen facturar están marcados cun ID de factura proforma ao crear un borrador de factura. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

Para obter información sobre as correccións incluídas nesta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) e vexa o [artigo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
