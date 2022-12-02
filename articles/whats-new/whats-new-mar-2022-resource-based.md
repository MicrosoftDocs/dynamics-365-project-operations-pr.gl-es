---
title: Novidades de marzo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de marzo de 2022 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910904"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de marzo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

*Aplícase a: Project Operations para situacións baseadas en recursos/sen fornecemento*

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.30.0.99
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.25

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As dietas agora admítense na nova e reinventada área de traballo de gastos moderna. As empresas que usan dietas poden activar esta funcionalidade para ofrecer aos usuarios un xeito sinxelo de enviar e recibir o reembolso dos seus gastos de dietas. Para obter máis información, consulte [Gastos de dietas](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte lista mostra os mapas de escrita dual que foron modificados ou engadidos na versión de Project Operations de marzo de 2022.

| **Asignación de entidades** | **Versión actualizada** | **Comentarios** |
| --- | --- | --- |
| Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Actualizáronse as asignacións para aliñarse coa entidade da liña de factura do fornecedor en Dataverse. <br>Non active a versión de asignación 1.0.0.4. Estará lista para usar en combinación coa versión 10.0.26 do ambiente de Finance na próxima actualización mensual. |

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Tempo e gasto | 2388011 | Mostre os comentarios de rexeitamento aos remitentes de entradas de tempo durante a aprobación masiva. |
| Planificación e rastrexo de proxectos | 2495294 | Os detalles do proxecto non deben ser editables na páxina **Detalles da tarefa**. |
| Facturación e prezos | 2499605 | Os fitos de contrato que se crean a partir de fitos de cotización están marcados incorrectamente como de só lectura. |
| Planificación e rastrexo de proxectos | 2506050 | O conxunto de operacións permanece pendente durante unha hora se non hai cambios que gardar. O conxunto márcase entón falsamente como **Erro**, mentres que debería completarse inmediatamente. |
| Facturación e prezos | 2507401 | As unidades de contratación predefinidas introdúcense incorrectamente nos proxectos por mor dunha caché incorrecta. |
| Facturación e prezos | 2541660 | **Validación de creación de pedidos de vendas** en escrita dual só debe ser para pedidos baseados en proxectos. |
| Facturación e prezos | 2552745 | O imposto non se divide entre os clientes que configuraron regras de facturación dividida. |
| Facturación e prezos | 2558859 | Mensaxes de erro melloradas cando se configuran as dimensións de prezos. |
| Facturación e prezos | 2558933 | **Importar desde as estimacións do proxecto** falla cando **msdyn\_proxecto** se engade como dimensión de prezos. |
| Facturación e prezos | 2559101 | A eliminación de parámetros do proxecto non está bloqueada e causa problemas. |
|   Xestión de oportunidades | 2570390 | O complemento de escrita dual obriga a que o tipo de conta se faga en cotizacións, pedidos e oportunidades sexa **Cliente**, aínda que ese tipo de conta non sexa correcto. |
| Facturación e prezos | 2586097 | Os datos reais de custo facturado dividido non se inverten cando se elimina un proxecto dunha liña de contrato do proxecto. |
| Facturación e prezos | 2589619 | O imposto sobre o material fóra de catálogo propágase aos reais de vendas non facturados e á factura. |
|   Xestión de oportunidades | 2594015 | Non se pode pechar unha cotización como gañada para os clientes que o teñan condicións de pagamento **Net60**. |
| Planificación e rastrexo de proxectos | 2595841 | En Project for the Web, os usuarios reciben unha mensaxe de erro sobre un **msdyn\_actualstart** que falta cando crean unha nova solicitude de recurso. |
| Tempo e gasto | 2602511 | O campo **Rexeitado por** mostra o campo para as entradas de tempo **Sistema** en lugar dun usuario nomeado como o rexeitador. |
| Tempo e gasto | 2602528 | Un responsable de aprobación de proxectos pode aprobar o tempo de proxectos nos que non figure como responsable de aprobación. |
| Facturación e prezos | 2608550 | Pódese confirmar unha factura de corrección aínda que non haxa cambios na orixinal. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Hai un desaxuste entre Finance e Project Operations na duración permitida do campo **ID de categoría**. |
| Xestión e contabilidade de proxectos | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Os proxectos de prezos fixos non se poden eliminar cando o campo **Facturación en conta** está configurado como **Perdas e ganancias** e utilízase o principio de **Porcentaxe completada**. |
| Xestión e contabilidade de proxectos | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Introdúcese un grupo de impostos sobre vendas predefinido incorrecto desde a configuración do proxecto nas liñas de gasto do diario de integración de Project Operations. |
| Xestión e contabilidade de proxectos | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Non pode editar as dimensións da cabeceira da proposta de factura do proxecto nun despregamento integrado con Project Operations. |
| Xestión e contabilidade de proxectos | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | As facturas de fornecedores entre empresas non deben integrarse con Dataverse. |
| Xestión e contabilidade de proxectos | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Hai unha falta de coincidencia na moeda dos saldos dos clientes e na moeda de informes. |
| Xestión e contabilidade de proxectos | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Pode contabilizar unha factura de proxecto aínda que o cliente estea en espera para todas as facturas. |
| Xestión e contabilidade de proxectos | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | O botón **Eliminar todas as liñas** nas propostas de factura do proxecto que teñen as vistas de **Cabeceira** e **Liñas**. |
| Xestión e contabilidade de proxectos | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Cando contabiliza unha factura de fornecedor, prodúcese o seguinte erro: "A data contable da factura debe estar no mesmo exercicio contable que o pedido de compra relacionada. Execute o proceso de fin de ano da orde de compra ou cambie a data ao exercicio contable actual". |
| Viaxes e gasto | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | O custo comprometido para un proxecto non se libera despois de que se libere o custo comprometido da solicitude de viaxe. |
| Viaxes e gasto | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | O seguinte erro ocorre cando envía un informe de gastos "Rastrexo de pila: a empresa non existe". |
| Viaxes e gasto | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | O **ID do proxecto** predefinido non se introduce nos informes de gastos cando o parámetro **Require actividade para o diario** está seleccionado no proxecto. |
| Viaxes e gasto | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | O botón **Contabilizar gastos** non funciona correctamente en Project Operations para situacións de recursos/sen fornecemento. |
| Viaxes e gasto | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Hai un problema con **Tarifa por quilómetro** para un informe de gastos de quilometraxe que inclúa os pasaxeiros. |
| Viaxes e gasto | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | As taxas de quilometraxe dos gastos dos empregados non se suman correctamente cando se usan dous tipos de vehículos diferentes na categoría de gasto **Niveis de taxa de quilometraxe**. |
| Viaxes e gasto | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | A busca para o campo **Proxecto** dunha liña de solicitude de viaxe non devolve a lista correcta de proxectos. |
| Viaxes e gasto | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Quilometraxe en revisión** mostra unha advertencia nos informes de gastos. |
| Viaxes e gasto | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | O servizo de recoñecemento óptico de caracteres (OCR) de recibos non funciona debido a un problema co URL do servizo OCR de gastos. |
| Viaxes e gasto | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Cando a funcionalidade **Capacidade de detallar os gastos recorrentes rapidamente** está activada, os importes nas liñas de itemización nos informes de gastos cambian cada vez que o se abre a páxina **Itemizar**. |
| Viaxes e gasto | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Non pode eliminar un informe de gastos cando a lista provisional ten máis dun responsable de aprobación. |

## <a name="removed-and-deprecated-features"></a>Funcionalidades eliminadas e obsoletas

O artigo [Funcionalidades eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) describe funcionalidades que se eliminaron ou quedaron obsoletas para Dynamics 365 Project Operations.

- Unha funcionalidade eliminada xa non está dispoñible no produto.
- Unha funcionalidade obsoleta non está en desenvolvemento activo e podería eliminarse nunha futura actualización.

Aparecerá un anuncio de obsolescencia no artigo [Funcionalidades eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) 12 meses antes de que se elimine calquera funcionalidade do produto.

Para os cambios que só afectan ao tempo de compilación, pero son compatibles con sistemas binarios con ambientes de proba e produción, o tempo de obsolescencia será inferior a 12 meses. Normalmente, estes cambios son actualizacións funcionais que se deben facer no compilador.
