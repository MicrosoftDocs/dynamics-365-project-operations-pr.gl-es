---
title: Novidades de agosto de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de agosto de 2022 de Microsoft Dynamics 365 Project Operations para escenarios baseados en recursos/non abastecidos.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403854"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de agosto de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.45.0.53
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, sigue as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
|   Xestión de oportunidades | 2762089 | Xestión de erros ao pechar o contrato como perdido se o gardado automático está desactivado na organización.|
|Planificación e rastrexo de proxectos | 2767841 | Actualizacións de telemetría Entidade do proxecto Crear ou actualizar escenarios.|
|Facturación e prezos | 2771072 | Manexo de excepcións de referencia nula ao gañar cotización.|
|Facturación e prezos | 2844181 |Fallo ao conseguir un identificador de correlación e bloqueo da creación dunha factura.|
|Facturación e prezos | 2852836 | Faltan datos reais entre empresas para os gastos entre empresas creados e aprobados en CE.|


### <a name="project-management-and-accounting-in-finance"></a>Xestión de proxectos e contabilidade en Finanzas

Para obter información sobre as correccións de erros que se inclúen nesta actualización, inicie sesión en Microsoft Dynamics Servizos de ciclo de vida (LCS) e consulte [Artigo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
