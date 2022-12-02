---
title: Novidades de febreiro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de febreiro de 2022 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932984"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de febreiro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

*Aplícase a: Project Operations para situacións baseadas en recursos/sen fornecemento*

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.28.0.120
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.24

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

- A partir desta versión, pode engadir ata 300 membros do equipo a un único proxecto. Anteriormente, o límite do número de membros do equipo era de 150. Para obter máis información, consulte [Límites de proxecto](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte lista mostra os mapas de escrita dual que foron modificados ou engadidos na versión de Project Operations de febreiro de 2022.

| Asignación de entidades | Versión actualizada | Comentarios |
| --- | --- | --- |
| Entidade de exportación de gastos de proxecto de integración de Project Operations (msdyn\_expenses) | 1.0.0.3 | Ampliado para a sincronización da actividade do proxecto con Dataverse. |

Para obter a lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2415109 | O valor predefinido no campo **Condicións de pagamento de operacións** debe ser o rexistro do cliente do contrato do proxecto e o rexistro da factura proforma. |
| Facturación e prezos | 2497369 | A corrección de material debe seguir o valor da data nos parámetros de **Corrección**. |
| Facturación e prezos | 2498697 | Mellorouse a configuración de seguridade para **Recuperación de entrada de hora**. |
| Facturación e prezos | 2513824 | Para escenarios baseados en recursos, o ID da categoría de transacción non debe superar os 28 caracteres en Project Operations. |
| Facturación e prezos | 2517455 | Non se debe permitir que se active a acción **Actualizar transaccións de liña de factura** varias veces simultaneamente para a mesma factura. |
| Facturación e prezos | 2517465 | A acción **Desactivar os detalles da liña de factura** está bloqueada porque non é compatible. |
| Facturación e prezos | 2556660 | Arranxouse a comprobación de efectividade da data que se realiza na lista de prezos que se anexa ao rexistro de parámetros do proxecto. |
|   Xestión de oportunidades | 2369202 | Corrixiuse a lóxica de negocio que verifica que as listas de prezos que teñan datas de vixencia superpostas poidan unirse ao mesmo contrato do proxecto. |
|   Xestión de oportunidades | 2385965 | Corrixiuse o comportamento no separador **Clientes** da páxina **Contrato do proxecto** cando selecciona **Gardar e pechar**. |
| Tempo e gasto | 2538503 | Unha tarefa do proxecto debe estar dispoñible na entidade **Datos reais do proxecto** despois de contabilizar un informe de gastos. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durante a importación de notas de crédito do fornecedor, ocorre un erro. A mensaxe de erro indica: "A cantidade de retención non pode ser superior á cantidade neta restante". |
| Xestión e contabilidade de proxectos | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Se unha proposta de factura inclúe transaccións de tarifas de importe cero que sexan datos reais de vendas sen facturar, non se pode facturar. |
| Xestión e contabilidade de proxectos | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | O custo publicado non é correcto despois de que se actualice o prezo de compra e se active **Activar a xestión de cambios**.|
| Xestión e contabilidade de proxectos | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | A estimación de contabilización dun proxecto de prezo fixo utiliza a moeda e o importe incorrectos no vale de estimación, mesmo cando a funcionalidade **Activar a moeda do contrato do proxecto para o cálculo da estimación** está activada. |
| Xestión e contabilidade de proxectos | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extensión** non debería facer unha chamada para activar o seguimento de cambios sen detectar excepcións para entidades que teñen claves de configuración que non están activadas. |
| Xestión e contabilidade de proxectos | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | O traballo por lotes arranxase cando se publican varios diarios avanzados e se produce un erro. |
| Viaxes e gasto | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Debido a un problema de liquidación relacionado cos avances en efectivo nos informes de gastos, o importe do imposto non está cuberto como parte do adianto de efectivo. |
| Viaxes e gasto | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | A información do imposto sobre as vendas non está incluída no **Gasto - Transaccións contabilizadas** informe. |
| Viaxes e gasto | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | A violación de política de gastos **Requírense recibos** mostra incorrectamente unha advertencia nos informes de gastos. |
| Viaxes e gasto | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Unha transacción de proxecto non inclúe impostos sobre vendas non recuperables no importe total das vendas cando a transacción é o resultado dun gasto de quilometraxe. |
| Viaxes e gasto | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Cando unha liña detallada ten impostos, non pode cambiar a data da liña de detalle e prodúcese un erro de estado do documento de orixe. |

## <a name="removed-and-deprecated-features"></a>Funcionalidades eliminadas e obsoletas

O artigo [Funcionalidades eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) describe funcionalidades que se eliminaron ou quedaron obsoletas para Dynamics 365 Project Operations.

- Unha funcionalidade eliminada xa non está dispoñible no produto.
- Unha funcionalidade obsoleta non está en desenvolvemento activo e podería eliminarse nunha futura actualización.

Aparecerá un anuncio de obsolescencia no artigo [Funcionalidades eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) 12 meses antes de que se elimine calquera funcionalidade do produto.

Para os cambios que só afectan ao tempo de compilación, pero son compatibles con sistemas binarios con ambientes de proba e produción, o tempo de obsolescencia será inferior a 12 meses. Normalmente, estes cambios son actualizacións funcionais que se deben facer no compilador.
