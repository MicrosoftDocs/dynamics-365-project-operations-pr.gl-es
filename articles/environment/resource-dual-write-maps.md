---
title: Versións do mapa de escrita dual de Project Operations
description: Este tema ofrece a lista de mapas de escrita dual necesarios para Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938980"
---
# <a name="project-operations-dual-write-map-versions"></a>Versións do mapa de escrita dual de Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Usando Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento require que un conxunto de mapas de escrita dual se executen no ambiente. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Mapas de requisitos previos: solución de orquestración de escrita dual

Os seguintes mapas son requisitos previos para a solución de Project Operations. Asegúrese de executar os mapas que aparecen na seguinte táboa e os mapas de táboa relacionados no seu ambiente.

| Asignación de táboas | Sincronización inicial |
| --- | --- |
| Libro maior (msdyn_ledgers) | Require a sincronización inicial para o mapa da táboa e todos os requisitos previos. O padrón para a sincronización inicial é as aplicacións de Finance and Operations. |
| Entidades legais (cdm_companies) | Non é necesario. O sistema enche esta entidade automaticamente cando os ambientes están ligados mediante escrita dual. |
| Clientes V3 (contas) | Non é necesario para o aprovisionamento. |
| Fornecedores V2 (msdyn_vendors) | Non é necesario para o aprovisionamento. |

1. Na lista de mapas, seleccione o papa de libro maior **(msdyn\_ledgers)** con todos os requisitos previos e seleccione a caixa de verificación **Sincronización inicial**. No campo **Padrón para a sincronización inicial**, seleccione **Aplicacións de Finance and Operations** tanto para o mapa de libro maior como para todos os mapas de requisitos previos. Seleccione **Executar**.

![Sincronización de mapa de libro maior](media/DW6.png)

1. Siga os mesmos pasos para todos os mapas de táboa restantes que aparecen na táboa anterior. Non seleccione a caixa de verificación **Sincronización inicial** ao executar eses mapas.

## <a name="project-operations-dual-write-maps"></a>Mapas de escrita dual en Project Operations

Os seguintes mapas son necesarios para a solución de Project Operations.

| **Asignación de entidades** | **Última versión** | **Sincronización inicial** |
| --- | --- | --- |
| Entidade de integración para as relacións de transaccións do proxecto (msdyn\_transactionconnections) | 1.0.0.0 | Non é necesario para o aprovisionamento. |
| Cabeceiras de contrato de proxecto (pedidos de vendas) | 1.0.0.1 | Non é necesario para o aprovisionamento. |
| Liñas de contrato de proxecto (salesorderdetails) | 1.0.0.0 | Non é necesario para o aprovisionamento. |
| Orixe de financiamento do proxecto (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Non é necesario para o aprovisionamento. |
| Táboa de integración de Project Operations para estimacións de material (msdyn\_estimatelines) | 1.0.0.0 | Non é necesario para o aprovisionamento. |
| Propostas de factura de proxecto V2 (facturas) | 1.0.0.2 | Non é necesario para o aprovisionamento. |
| Datos reais de integración de Project Operations (msdyn_actuals) | 1.0.0.14 | Non é necesario para o aprovisionamento. |
| Fitos da liña de contrato de integración de Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Non é necesario para o aprovisionamento. |
| Entidade de integración de Project Operations para estimacións de gastos (msdyn_estimateslines) | 1.0.0.2 | Non é necesario para o aprovisionamento. |
| Entidade de integración de Project Operations para estimacións de horas (msdyn_resourceassignments) | 1.0.0.5 | Non é necesario para o aprovisionamento. |
| Entidade de exportación de categorías de gastos de proxecto de integración de Project Operations (msdyn_expensecategories) | 1.0.0.2 | Non é necesario para o aprovisionamento. |
| Entidade de exportación de gastos de proxecto de integración de Project Operations (msdyn_expenses) | 1.0.0.2 | Non é necesario para o aprovisionamento. |
| Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Non é necesario para o aprovisionamento. |
| Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Non é necesario para o aprovisionamento. |
| Roles de recursos do proxecto para todas as empresas (bookableresourcecategories) | 1.0.0.1 | É necesaria unha sincronización inicial para que o mapa de táboas sincronice os roles de recursos de xestor de proxectos e membros do equipo que se introducen no ambiente de Dynamics 365 Dataverse durante o aprovisionamento. Dataverse é a orixe principal para a sincronización inicial. |
| Tarefas do proxecto (msdyn_projecttasks) | 1.0.0.4 | Non é necesario para o aprovisionamento. |
| Categorías de transacción de proxecto (msdyn_transactioncategories) | 1.0.0.0 | Non é necesario para o aprovisionamento. |
| Proxectos V2 (msdyn_projects) | 1.0.0.1 | Non é necesario para o aprovisionamento. |

Realice os seguintes pasos para executar os mapas que se mostran.

1. Active os roles de recursos do proxecto para o mapa da táboa de **todas as empresas (bookableresourcecategories)** xa que este mapa require a sincronización inicial. No campo **Padrón para a sincronización inicial**, seleccione **Common Data Service**. 

 ![Sincronización do mapa da táboa de roles de recursos](media/6ResourceInitialSync.jpg)

 Agarde a que o estado do mapa sexa **En execución** antes de pasar ao seguinte paso.

2. Seleccione todos os mapas necesarios restantes. Podes filtralos na lista de mapas de escrita dual usando a palabra clave **Proxecto** na busca da esquina superior dereita. Pode seleccionar todos os mapas e despois executalos. Para obter máis información, consulte [Xestionar varios mapas de táboa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Asegúrese de activar e executar tamén os mapas de entidade relacionados.

### <a name="project-operations-dual-write-map-versions"></a>Versións do mapa de escrita dual de Project Operations

Execute sempre a versión máis recente do mapa no seu ambiente. É posible que certas funcionalidades e capacidades non funcionen correctamente se existe algunha das seguintes condicións:

- Un mapa non está activado.
- A versión máis recente do mapa non está activada. 
- Os mapas de táboas relacionados non están activados.

Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Pode activar unha nova versión do mapa seleccionando **Versións do mapa de táboa**, seleccionando a versión máis recente e logo gardar a versión seleccionada. Se personalizou un mapa de táboa listo para usar, necesitará volver aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
