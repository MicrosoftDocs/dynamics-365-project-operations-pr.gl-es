---
title: Novidades de xullo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de xullo de 2022 de Microsoft Dynamics 365 Project Operations para escenarios baseados en recursos/non abastecidos.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183894"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de xullo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.44.0.22
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Executa sempre a versión máis recente do mapa no teu ambiente e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, sigue as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Despregamento e configuración | 2761472 | Xestiónase un erro de instalación de Project Operations. |
| Facturación e prezos | 2746940 | O nome da liña de subcontrato debe ter unha lonxitude máxima de 100 caracteres. |
| Facturación e prezos | 2739162 | Os clientes deben poder ver os botóns da cinta na vista da grade real. |
| Planificación e rastrexo de proxectos | 2730318 | Validación actualizada para caracteres non admitidos no tema do proxecto. |
| Facturación e prezos | 2705361 | Os reais de vendas facturadas por Milestone deben incluírse nos campos de seguimento do proxecto. |
| Facturación e prezos | 2675880 | Evitar que un proxecto se vincule a unha liña de contrato que non se basea no traballo. |
| Facturación e prezos | 2664396 | Se se garda unha lista de prezos de cotización sen cotización, debe haber un erro que indica que a cotización non pode estar baleira. |
| Facturación e prezos | 2184019 | O **Facturación baseada en tarefas** non se debe mostrar a pestana para proxectos que non teñan ningún contrato ou cotización de apoio. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión de proxectos e contabilidade en Finanzas

Para obter información sobre as correccións de erros que se inclúen nesta actualización, inicie sesión en Microsoft Dynamics Servizos de ciclo de vida (LCS) e consulte [Artigo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>As funcións están activadas de forma predeterminada na próxima versión

A seguinte táboa enumera as funcións que están activadas por defecto na versión 10.0.29. A maioría das funcións que se activaron automaticamente pódense desactivar en [Xestión de características](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, algunhas funcións que se activaron automaticamente poden eliminarse da xestión de funcións e converterse en obrigatorias. Este cambio garante que os clientes estean a utilizar a funcionalidade actual, de xeito que as melloras poden incorporarse á funcionalidade actual a medida que se engaden. As funcións nunca se activarán automaticamente en menos dun ano, a non ser que se determine que son esenciais.

| Nome da característica | Activar data | Función engadida | Estado da característica | Módulo |
| --- | --- | --- |--- |--- |
| Activa o axuste da transacción horaria en función do cambio na asignación da regra de financiamento | 16 de setembro de 2022 | 7 de outubro de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Función de reversión de facturas de prepago da orde de compra do proxecto | 16 de setembro de 2022 | 6 de outubro de 2021 | Activado por defecto | Xestión e contabilidade de proxectos |
| Elimine as liñas de proposta de factura cando se utilice Project Operations para escenarios baseados en recursos ou non almacenados | 16 de setembro de 2022 | 6 de outubro de 2021 | Activado por defecto | Xestión e contabilidade de proxectos |
| Axustar a contabilidade nunha transacción de proxecto publicada | 16 de setembro de 2022 | 10 de maio de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activa a configuración de contabilidade predeterminada para o proxecto | 16 de setembro de 2022 | 19 de febreiro de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activar varias liñas de contrato para un proxecto | 16 de setembro de 2022 | 29 de xuño de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Fai que as revistas Project Hour sexan só de lectura se o estado de aprobación actual non permite a edición | 16 de setembro de 2022 | 6 de outubro de 2021 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activa a sincronización das liñas de vendas das liñas de compra cando se actualicen as liñas de compra e o parámetro de xestión de cambios de pedidos de compra estea activado | 16 de setembro de 2022 | 7 de outubro de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activa as operacións do proxecto en Dynamics 365 Customer Engagement | 16 de setembro de 2022 | 29 de xuño de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Función de corrección de reversión de transaccións do proxecto | 16 de setembro de 2022 | 13 de xullo de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funcións que se fan obrigatorias no próximo lanzamento

A seguinte táboa enumera as funcións que son obrigatorias a partir da versión 10.0.29.

| Nome da característica | Activar data | Función engadida | Estado da característica | Módulo |
| --- | --- | --- | --- | --- |
| Calcula o valor comprometido na fonte de financiamento sen redondear o tipo de cambio | 16 de setembro de 2022 | 14 de xuño de 2020 | Obrigatorio | Xestión e contabilidade de proxectos |
| Activa a publicación do axuste do proxecto coa mesma conta do libro maior que a transacción orixinal | 16 de setembro de 2022 | 14 de xuño de 2020 | Obrigatorio | Xestión e contabilidade de proxectos |
| Detalle do importe comprometido do contrato do proxecto | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatorio | Xestión e contabilidade de proxectos |
| Activa a clasificación por recurso durante a creación da proposta de factura do proxecto | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatorio | Xestión e contabilidade de proxectos |
