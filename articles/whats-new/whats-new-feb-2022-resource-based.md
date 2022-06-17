---
title: Novidades de febreiro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de febreiro de 2022 de Project Operations para escenarios baseados en recursos ou non abastecidos.
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

- Operacións do proxecto en a Dataverse versión do entorno 4.28.0.120
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.24

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

- A partir desta versión, podes engadir ata 300 membros do equipo a un único proxecto. Anteriormente, o límite no número de membros do equipo era de 150. Para obter máis información, consulte [Límites do proxecto](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Actualizacións de mapas de dobre escritura de Project Operations

A seguinte lista mostra os mapas de dobre escritura que se modificaron ou engadiron na versión de febreiro de 2022 de Project Operations.

| Asignación de entidades | Versión actualizada | Comentarios |
| --- | --- | --- |
| Entidade de exportación de gastos do proxecto de integración de operacións do proxecto (msdyn\_ gastos) | 1.0.0.3 | Ampliado para a sincronización da actividade do proxecto a Dataverse. |

Para ver a lista e as versións actuais dos mapas de dobre escritura de Project Operations, consulte [Versións de mapas de dobre escritura de Project Operations](../environment/resource-dual-write-maps.md).

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, siga as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de Dual Write.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2415109 | O valor predeterminado no **Condicións de pagamento das operacións** campo debe ser o rexistro do cliente do contrato do proxecto e o rexistro da factura proforma. |
| Facturación e prezos | 2497369 | A corrección material debe seguir o valor da data no **Corrección** parámetros. |
| Facturación e prezos | 2498697 | Mellorouse a configuración de seguridade para **Recuperación de entrada de hora**. |
| Facturación e prezos | 2513824 | Para escenarios baseados en recursos, o ID da categoría de transacción non debe superar os 28 caracteres en Operacións do proxecto. |
| Facturación e prezos | 2517455 | O **Actualizar as transaccións da liña de factura** non se debe permitir que se active varias veces simultáneamente para a mesma factura. |
| Facturación e prezos | 2517465 | O **Desactivar os detalles da liña de factura** a acción está bloqueada porque non é compatible. |
| Facturación e prezos | 2556660 | Corrixiuse a comprobación de efectividade da data que se realiza na lista de prezos que se anexa ao rexistro de parámetros do proxecto. |
|   Xestión de oportunidades | 2369202 | Corrixida a lóxica de negocio que verifica que as listas de prezos que teñan datas de vixencia superpostas poidan unirse ao mesmo contrato do proxecto. |
|   Xestión de oportunidades | 2385965 | Corrixiuse o comportamento no **Clientes** ficha da **Contrato do proxecto** páxina cando seleccione **Garda e pecha**. |
| Tempo e gasto | 2538503 | Unha tarefa do proxecto debe estar dispoñible no **Reais do proxecto** entidade despois de publicar un informe de gastos. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión de proxectos e contabilidade en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durante a importación de notas de crédito do provedor, ocorre un erro. A mensaxe de erro indica: "A cantidade de retención non pode ser superior á cantidade neta restante". |
| Xestión e contabilidade de proxectos | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Se unha proposta de factura inclúe transaccións de tarifas de importe cero que sexan reais de vendas sen facturar, non se pode facturar. |
| Xestión e contabilidade de proxectos | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | O custo publicado non é correcto despois de que se actualice o prezo de compra e **Activar a xestión de cambios** está activado.|
| Xestión e contabilidade de proxectos | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | A estimación de contabilización dun proxecto de prezo fixo utiliza a moeda e o importe incorrectos no comprobante de estimación, mesmo cando o **Activa a moeda do contrato do proxecto para o cálculo da estimación** a función está activada. |
| Xestión e contabilidade de proxectos | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulación\_ Extensión** non debería facer unha chamada para activar o seguimento de cambios sen detectar excepcións para as entidades que teñen claves de configuración que non están activadas. |
| Xestión e contabilidade de proxectos | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | O traballo por lotes arranxase cando se publican varias revistas avanzadas e se produce un erro. |
| Viaxes e gasto | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Debido a un problema de liquidación relacionado cos avances en efectivo nos informes de gastos, o importe do imposto non está cuberto como parte do anticipo en efectivo. |
| Viaxes e gasto | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | A información do imposto sobre vendas non está incluída no **Gastos - Transaccións contabilizadas** informe. |
| Viaxes e gasto | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | O **Requírese recibos** a infracción da política de gastos mostra incorrectamente unha advertencia nos informes de gastos. |
| Viaxes e gasto | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Unha transacción de proxecto non inclúe impostos sobre vendas non recuperables no importe total das vendas cando a transacción é o resultado dun gasto de quilometraxe. |
| Viaxes e gasto | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Cando unha liña detallada ten impostos, non pode cambiar a data da liña de detalle e prodúcese un erro de estado do documento de orixe. |

## <a name="removed-and-deprecated-features"></a>Funcións eliminadas e obsoletas

O [Funcións eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) O artigo describe funcións que foron eliminadas ou obsoletas para Dynamics 365 Project Operations.

- Unha funcionalidade eliminada xa non está dispoñible no produto.
- Unha función obsoleta non está en desenvolvemento activo e é posible que se elimine nunha actualización futura.

Aparecerá un anuncio de desuso no [Funcións eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) artigo 12 meses antes de que se elimine calquera característica do produto.

Para os cambios que só afectan ao tempo de compilación, pero son compatibles con sistemas binarios con entornos de produción e sandbox, o tempo de desuso será inferior a 12 meses. Normalmente, estes cambios son actualizacións funcionais que se deben facer no compilador.
