---
title: Novidades de xullo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de xullo de 2022 de Microsoft Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403949"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de xullo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.44.0.22
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Despregamento e configuración | 2761472 | Trátase un erro de instalación de Project Operations. |
| Facturación e prezos | 2746940 | O nome da liña de subcontratación debe ter unha lonxitude máxima de 100 caracteres. |
| Facturación e prezos | 2739162 | Os clientes deben poder ver os botóns da fita na vista de grade de datos reais. |
| Planificación e rastrexo de proxectos | 2730318 | Validación actualizada para caracteres non admitidos no tema do proxecto. |
| Facturación e prezos | 2705361 | Os datos reais de vendas facturadas por fito deben incluírse nos campos de seguimento do proxecto. |
| Facturación e prezos | 2675880 | Evite que un proxecto se vincule a unha liña de contrato que non se basea no traballo. |
| Facturación e prezos | 2664396 | Se se garda unha lista de prezos de oferta sen unha oferta, debe haber un erro que indica que a oferta non pode estar baleira. |
| Facturación e prezos | 2184019 | O separador **Facturación baseada en tarefas** non se debe mostrar para proxectos que non teñan ningún contrato ou oferta de apoio. |
| Tempo e gasto | 2754459 | Cando o fluxo na nube de programación recorrente estea inactivo, mostra a faixa e evita o procesamento asíncrono. |
| Facturación e prezos | 2724391 | Lanzase unha excepción incorrecta cando a regra de facturación dividida do contrato do proxecto non ten un valor de cliente. |
| Facturación e prezos | 2708638 | Non se atopou o rexistro durante a busca mediante a busca de grade en Usos de materiais e aprobacións para usos de materiais.|
| Facturación e prezos | 2686977 | Evite a validación da liña de factura durante a creación da factura. |
| Facturación e prezos | 2683032 | A copia de roles e categorías imputables non supera os 5000 rexistros.|
| Facturación e prezos | 2673363 | O % de consumo de custos no proxecto está corrompido cando existen estimacións e datos reais de esforzo e gastos para un proxecto. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión e contabilidade de proxectos en Finance

Para obter información sobre as correccións incluídas nesta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) e vexa o [artigo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>As funcionalidades están activadas de forma predefinida na próxima versión

A seguinte táboa indica as funcións que están activadas por defecto na versión 10.0.29. A maioría das funcións que se activaron automaticamente pódense desactivar en [Xestión de funcionalidades](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, algunhas funcións que se activaron automaticamente poden eliminarse da xestión de funcionalidades e converterse en obrigatorias. Este cambio garante que os clientes estean a utilizar a funcionalidade actual, de xeito que as melloras poden incorporarse á funcionalidade actual a medida que se engaden. As funcionalidades nunca se activarán automaticamente en menos dun ano, a non ser que se determine que son esenciais.

| Nome da funcionalidade | Activar data | Funcionalidade engadida | Estado da funcionalidade | Módulo |
| --- | --- | --- |--- |--- |
| Activar o axuste da transacción horaria en función do cambio na asignación da regra de financiamento | 16 de setembro de 2022 | 7 de outubro de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Funcionalidade de reversión de facturas de prepagamento do pedido de compra do proxecto | 16 de setembro de 2022 | 6 de outubro de 2021 | Activado por defecto | Xestión e contabilidade de proxectos |
| Eliminar as liñas de proposta de factura coando se utiliza Project Operations para situacións baseadas en recursos/sen fornecemento | 16 de setembro de 2022 | 6 de outubro de 2021 | Activado por defecto | Xestión e contabilidade de proxectos |
| Axustar a contabilidade nunha transacción de proxecto contabilizada | 16 de setembro de 2022 | 10 de maio de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activar a configuración de contabilidade predefinida para o proxecto | 16 de setembro de 2022 | 19 de febreiro de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activar varias liñas de contrato para un proxecto | 16 de setembro de 2022 | 29 de xuño de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Facer que os diarios de horas do proxecto sexan de só lectura se o estado de aprobación actual non permite a edición | 16 de setembro de 2022 | 6 de outubro de 2021 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activar a sincronización das liñas de vendas das liñas de compra cando se actualicen as liñas de compra e o parámetro de xestión de cambios de pedidos de compra estea activado | 16 de setembro de 2022 | 7 de outubro de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Activar Project Operations en Dynamics 365 Customer Engagement | 16 de setembro de 2022 | 29 de xuño de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |
| Función de corrección de reversión de transaccións do proxecto | 16 de setembro de 2022 | 13 de xullo de 2020 | Activado por defecto | Xestión e contabilidade de proxectos |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funcións que se fan obrigatorias no próximo lanzamento

A seguinte táboa indica as funcións que son obrigatorias a partir da versión 10.0.29.

| Nome da funcionalidade | Activar data | Funcionalidade engadida | Estado da funcionalidade | Módulo |
| --- | --- | --- | --- | --- |
| Calcula o valor comprometido na fonte de financiamento sen redondear o tipo de cambio | 16 de setembro de 2022 | 14 de xuño de 2020 | Obrigatorio | Xestión e contabilidade de proxectos |
| Activar a publicación do axuste do proxecto coa mesma conta do libro maior que a transacción orixinal | 16 de setembro de 2022 | 14 de xuño de 2020 | Obrigatorio | Xestión e contabilidade de proxectos |
| Detalle do importe comprometido do contrato do proxecto | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatorio | Xestión e contabilidade de proxectos |
| Activar a clasificación por recurso durante a creación da proposta de factura do proxecto | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatorio | Xestión e contabilidade de proxectos |
