---
title: Novidades de setembro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de setembro de 2021 de Project Operations para escenarios baseados en recursos ou non almacenados.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923370"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de setembro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

*Aplícase a: Project Operations para situacións baseadas en recursos/sen fornecemento*

Este artigo aplícase ao seguinte Dynamics 365 Project Operations compoñentes e versións:

   - Project Operations no ambiente de Microsoft Dataverse versión 4.14.0.99.
   - Xestión de proxectos e contabilidade no entorno Dynamics 365 Finance versión 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse solución e a versión da solución de Finance. É posible que certas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na páxina **Escrita dual** na columna **Versión**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema ao iniciar o mapa, siga as instrucións da sección [Problema de columnas da táboa que faltan nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Tempo e gasto | 1811407 | Axustouse o rol de seguranza do responsable de aprobacións do proxecto para aprobacións de entradas de gastos. |
| Tempo e gasto | 1811438 | Axustouse o rol de seguranza do responsable de aprobacións do proxecto para a cancelación de aprobacións de entradas de tempo. |
| Tempo e gasto | 2370126 | Actualizáronse as iconas de **Tarefa do proxecto** e **Rol** na entidade **Entrada de tempo**. |
| Tempo e gasto | 2379879 | Corrixiuse a función **Copiar semana** na entrada de tempo cando se usa Dynamics 365 para teléfono. |
| Facturación e prezos | 2371906 | O importe total da factura Proforma non debe ser axustable en Project Operations para despregamentos baseados en recursos. |
| Facturación e prezos | 2385802 | Corrixiuse o erro que se producía con horas reais negativas cando se actualizaban os totais do proxecto. |
| Facturación e prezos | 2389675 | Mellorouse o comportamento de confirmación da factura proforma. A entidade de traballos de longa duración debe ter en conta a actividade necesaria para escribir resultados de confirmación para contabilidade. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión de proxectos e contabilidade en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Viaxes e gasto | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os importes das transaccións do fornecedor e do imposto sobre as vendas que se rexistran a partir dun gasto creado a partir dunha transacción con tarxeta de crédito son incorrectos. |
| Viaxes e gasto | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Créanse liñas de liquidación incorrectas cando se xera o diario de pagamentos. |
| Viaxes e gasto | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os importes das transaccións do imposto sobre as vendas que se rexistran a partir dun gasto creado a partir dunha transacción con tarxeta de crédito son incorrectos. |
| Viaxes e gasto | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | A eliminación dunha liña de gasto pode levar moito tempo. |
| Contabilidade de proxectos | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Despois de aplicar KB 4619395, cambiar a secuencia numérica a **Continua** non se admite e cando contabiliza unha estimación, prodúcese o seguinte erro: "O sistema non admite a configuración "continua" da secuencia numérica Proj_X". |
| Contabilidade de proxectos | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | A contabilizacón dunha factura de fornecedor pode fallar coa seguinte mensaxe de erro: "As transaccións do vale non se saldan segundo o 17/05/2021. (divisa de contabilidade: 0,00 - divisa de informes: 0,01)". |
