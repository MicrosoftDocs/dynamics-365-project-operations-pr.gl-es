---
title: Novidades de maio de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de Microsoft de maio de 2022 Dynamics 365 Project Operations para escenarios baseados en recursos/non abastecidos.
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

- Operacións do proxecto en a Dataverse versión do entorno 4.42.0.70
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, siga as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade
### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión de recursos | 2634019 | Mensaxes de erro melloradas para validacións empresariais ao engadir membros xenéricos do equipo como recursos. |
| Planificación e rastrexo de proxectos | 2648515 | Actualizacións restrinxidas de **propietario**, **·**, e **estado** en entidades de programación. |
| Facturación e prezos | 2653167 | O **Estimacións** o separador decimal de grade debe seguir a configuración do formato **Opcións persoais**. |
| Facturación e prezos| 2662251 | Valores no **Unidade corrixida** e **Grupo de unidades** campos predeterminados ao crear rexistros en estimacións de materiais. |
| Facturación e prezos| 2571408 | Os reais de vendas non facturados están selados cun ID de factura proforma ao crear un borrador de factura. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión de proxectos e contabilidade en Dynamics 365 Finance

Para obter información sobre as correccións de erros que se inclúen nesta actualización, inicie sesión en Microsoft Dynamics Servizos de ciclo de vida (LCS) e consulte [Artigo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
