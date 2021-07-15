---
title: Novidades de xuño de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de xuño de 2021 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 28890238f9debb96786a31f66dd9a219f88a5338
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293135"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de xuño de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

- Project Operations no ambiente de Dynamics 365 Dataverse versión 4.11.0.156 ou 4.11.0.164.
- Xestión e contabilidade de proxectos en ambientes de aplicacións de Finance and Operations versión 10.0.19.

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- Posibilidade de eliminar [Liñas de proposta de factura do proxecto para escenarios de axuste](../invoicing/correct-project-invoice-proposals.md).
- As liñas de gastos detalladas reflicten os nomes das subcategorías no informe de gastos [Novo deseño dos informes de gastos: novas funcionalidades](../expense/expense-reports-reimagined.md#new-features).
- O método de pagamento está dispoñible no novo panel de gastos cando se crea un novo gasto.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. 

Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e activar todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de aplicacións de Finance and Operations. É posible que certas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na páxina **Escrita dual** na columna **Versión**. Active unha nova versión do mapa seleccionando **Versións do mapa de táboas**, seleccionando a última versión e logo gardando a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema ao iniciar o mapa, siga as instrucións da sección [Problema de columnas da táboa que faltan nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Facturación e prezos | 2281417 | Solucionouse o problema relativo ao fallo da acción de creación automática de facturas a través da programación de facturas. |
| Facturación e prezos | 2287835 | Rendemento mellorado na confirmación da factura. |
| Xestión de oportunidades | 2222555 | A imputabilidade de estimacións de material debe copiarse correctamente na liña de oferta cando se usa **Importar desde a estimación do proxecto**. |
| Xestión de oportunidades | 2223427 | Agora permítense personalizacións para a acción **GenerateRetainersFromRetainerScheduleOptions**. |
| Xestión de oportunidades | 2277528 | Cálculo do valor do fito de facturación fixa para liñas de contratos de proxecto con varios clientes. |
| Planificación e rastrexo de proxectos | 2226110 | Solucionouse o problema intermitente coa función **Xerar requisito** na grade **Equipo do proxecto** cuadrícula. |
| Planificación e rastrexo de proxectos | 2208109 | Os usuarios non poden crear un proxecto nunha moeda con tarefas relacionadas noutra moeda. |
| Planificación e rastrexo de proxectos | 2258228 | Actualizouse a lista de campos que se poden modificar coas entidades de **Programación** que utilizan a API de programación. |
| Planificación e rastrexo de proxectos | 2293989 | Os axustes rexionais e de idioma correctos deben pasar á grade **Tarefas do proxecto**. |
| Xestión de recursos | 2220493 | Arranxouse a experiencia do usuario na grade **Tarefa** cando se marca rapidamente unha solicitude de recurso como completa. |
| Xestión de recursos | 2330496 | Arranxouse o problema de carga do **Panel de programación**. (A actualización de calidade está dispoñible na versión 4.11.0.164) |
| Tempo e gasto | 2194431 | A grade **Entrada de tempo** debe cumprir o comezo da semana como se establece na **Configuración do sistema**. |
| Tempo e gasto | 2277311 | Despois de eliminar o valor dunha cela na grade **Entrada de tempo**, o cursor permanece na grade. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notas do formulario** e **Configuración do formulario** non é visible na **Configuración da xestión de proxectos** nas entidades legais de Finance integradas con Project Operations. |
| Xestión e contabilidade de proxectos | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | A descrición predefinida do IVE está en branco cando o **Tipo de contabilización** = **Imposto sobre as vendas** para vales de factura do proxecto. |
| Xestión e contabilidade de proxectos | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Contabilízanse transaccións dobres cando se usa a facturación baseada en tarefas en Dataverse coa integración de Project Operations. |
| Xestión e contabilidade de proxectos | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | A porcentaxe completa no recoñecemento de ingresos é incorrecta mentres se usa a integración de Project Operations. |
| Xestión e contabilidade de proxectos | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | A acumulación de ingresos duplícase nunha factura de fornecedor pendente nun escenario integrado de Project Operations. |
| Xestión e contabilidade de proxectos | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Non se pode contabilizar o diario de integración cando a regra do perfil de ingresos está establecida en configuración de **Grupo**. |
| Xestión e contabilidade de proxectos | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Non se pode contabilizar unha factura de compra para pedidos de proxecto que teñan liñas con varias unidades de medida. |
| Xestión e contabilidade de proxectos | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | A dimensión financeira predefinida nun proxecto non se pode actualizar mediante a entidade de datos **V2** dos proxectos. |
| Xestión e contabilidade de proxectos | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | O proceso por lotes para crear estimacións do proxecto tarda demasiado tempo en completarse. |
| Xestión e contabilidade de proxectos | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | A eliminación dun contrato tamén elimina o enderezo asociado ao cliente. |
| Viaxes e gasto | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | A condición do fluxo de traballo de aprobación do informe de gastos non se avalía correctamente. |
| Viaxes e gasto | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | A política de informe de gastos non avalía correctamente o ID do proxecto. |
| Viaxes e gasto | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | A acción **Dividir a persoal para transaccións de gastos entre empresas** non funciona correctamente. |
| Viaxes e gasto | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | As xustificacións da liña de informe de gastos elimínanse accidentalmente cando se eliminan certas solicitudes de viaxe. Isto ocorre cando o recID do informe de gastos e a solicitude de viaxe son os mesmos. |
| Viaxes e gasto | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Hai un problema na aplicación móbil Expense cando o campo **ID do proxecto** é obrigatorio nas políticas de informe de gastos. |
| Viaxes e gasto | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Non se poden editar os gastos entre empresas asociados a un proxecto. Pola contra, aparece a seguinte mensaxe de erro: "Referencia de obxecto non establecida nunha instancia dun obxecto." |
| Viaxes e gasto | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Despois de que se publique o informe de gastos, a moeda e o importe equivocados aparecerán no libro bancario secundario. |
| Viaxes e gasto | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Realizáronse melloras na funcionalidade *Eliminar as transaccións con tarxeta de crédito*.  |
| Viaxes e gasto | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | O imposto sobre as vendas incluído nun informe de gastos non se calcula de forma coherente cando se especifica unha moeda de información diferente nunha entidade legal. |
| Viaxes e gasto | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | O rendemento vese afectado ao engadir un novo gasto de viaxe en efectivo. |
| Viaxes e gasto | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | As regras da política de gastos non se activan nun informe de gastos. |
| Viaxes e gasto | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Cargar unha nova categoría compartida mediante o marco de xestión de datos elimina todas as subcategorías para todas as categorías compartidas. |
| Viaxes e gasto | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Cando crea unha liña de gasto e selecciona unha categoría, aparece a seguinte mensaxe de erro: "A combinación do grupo de impostos sobre vendas DOM e grupo de impostos sobre vendas de artigos STD non é válida." |
| Viaxes e gasto | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Hai problemas de sincronización na aplicación para móbil Expense. |
