---
title: Novidades de agosto de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de agosto de 2021 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cd5a7e74fc90c6138cd672ff6109b59a8d2ae916
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323459"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de agosto de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

*Aplícase a: Project Operations para situacións baseadas en recursos/sen fornecemento*

Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

   - Project Operations no ambiente de Microsoft Dataverse versión 4.13.0.152.
   - Xestión e contabilidade de proxectos en ambiente de Dynamics 365 Finance versión 10.0.20.

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- **Conxuntos de aprobacións**: A aprobación reúne as solicitudes de aprobación do tempo, gastos ou uso de material do grupo en subconxuntos de operacións máis pequenos. Esta agrupación permite procesar as aprobacións por proxecto, nunha orde específica por proxecto e permite reintentar e secuenciar. Agrupar as solicitudes mellora a fiabilidade e rastrexabilidade do procesamento de aprobacións para grandes volumes de aprobacións. Para obter máis información, consulte [Conxuntos de aprobacións](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. 

Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse solución e a versión da solución de Finance. É posible que certas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na páxina **Escrita dual** na columna **Versión**. Active unha nova versión do mapa seleccionando **Versións do mapa de táboas**, seleccionando a última versión e logo gardando a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema ao iniciar o mapa, siga as instrucións da sección [Problema de columnas da táboa que faltan nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) na guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Facturación e prezos | 2295625 | O nome do fito debe copiarse da programación da factura ao detalle da liña de factura. |
| Facturación e prezos | 2316323 | O desconto non debe ser editable nunha factura proforma en Project Operations para escenarios baseados en recursos. |
|   Xestión de oportunidades | 2338619 | As regras de negocio **Oportunidade** e **Oferta** deben invocarse só nas páxinas. |
| Xestión de recursos | 2316523 | Ao usar **Enviar solicitude** dun requisito de recurso que ten un rol asociado non debería mostrarse un erro. |
| Xestión de recursos | 2326885 | A creación dun requisito de recursos a través dun proxecto non debería mostrar un erro. |
| Tempo e gasto | 2335584 | Fluxos de tarefas obsoletos na entrada de tempo. |
| Tempo e gasto | 2336884 | O botón de entrada de tempo **Copiar semana** debe funcionar para máis que o usuario actual. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Viaxes e gasto | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | As cantidades de transaccións de fornecedores e impostos sobre as vendas incorrectas contabilízanse cando se cree un gasto a partir dunha transacción con tarxeta de crédito. |
| Viaxes e gasto | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | A liquidación incorrecta son as liñas creadas cando se xera o diario de pagamentos. |
| Viaxes e gasto | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | As cantidades de transaccións de impostos sobre as vendas incorrectas contabilízanse cando se cree un gasto a partir dunha transacción con tarxeta de crédito. |
| Viaxes e gasto | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | A eliminación dunha liña de gasto pode levar moito tempo. |
| Contabilidade de proxectos | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | O sistema non admite a configuración de secuencias de números continuos cando contabiliza unha estimación despois de aplicar KB 4619395. |
| Contabilidade de proxectos | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | É posible que a contabilización de facturas do fornecedor falle coa mensaxe de erro "As transaccións do vale non se saldan de acordo con 17/05/2021. (divisa de contabilidade: 0,00 - divisa de informes: 0,01)" |
