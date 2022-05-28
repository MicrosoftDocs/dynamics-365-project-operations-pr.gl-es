---
title: Novidades de marzo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este tema ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de marzo de 2022 de Project Operations para escenarios baseados en recursos ou non almacenados.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600740"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de marzo de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

*Aplícase a: Project Operations para situacións baseadas en recursos/sen fornecemento*

Este tema aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.30.0.99
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.25

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

Os viáticos agora admítense no novo e reimaxinado espazo de traballo de gastos modernos. As empresas que usan dietas poden activar esta función para ofrecer aos usuarios un xeito sinxelo de enviar e recibir o reembolso dos seus gastos diarios. Para obter máis información, consulte [Gastos diarios](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte lista mostra os mapas de dobre escritura que se modificaron ou engadiron na versión de marzo de 2022 de Project Operations.

| **Asignación de entidades** | **Versión actualizada** | **Comentarios** |
| --- | --- | --- |
| Entidade de exportación de liña de factura do provedor do proxecto de integración de operacións do proxecto msdyn\_ liñas de facturas do provedor do proxecto | 1.0.0.3 | Actualizáronse as asignacións para aliñarse coa entidade da liña de factura do provedor en Dataverse. <br>Non active a versión de mapeo 1.0.0.4. Estará listo para usar en combinación coa versión 10.0.26 do entorno financeiro na próxima actualización mensual. |

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, siga as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Tempo e gasto | 2388011 | Mostra os comentarios de rexeitamento aos remitentes de entradas de tempo durante a aprobación masiva. |
| Planificación e rastrexo de proxectos | 2495294 | Os detalles do proxecto non deben ser editables no **Detalles da tarefa** páxina. |
| Facturación e prezos | 2499605 | Os fitos de contrato que se crean a partir de fitos de cotización están marcados incorrectamente como de só lectura. |
| Planificación e rastrexo de proxectos | 2506050 | O conxunto de operacións permanece pendente durante unha hora se non hai cambios que gardar. O conxunto márcase entón falsamente como **Fallou**, mentres que debería completarse inmediatamente. |
| Facturación e prezos | 2507401 | As unidades de contratación predeterminadas introdúcense incorrectamente nos proxectos por mor dunha caché incorrecta. |
| Facturación e prezos | 2541660 | **Validación de creación de pedidos de venda** en escritura dual só debe ser para pedidos baseados en proxectos. |
| Facturación e prezos | 2552745 | O imposto non se divide entre os clientes que configuraron regras de facturación dividida. |
| Facturación e prezos | 2558859 | Mensaxes de erro melloradas cando se configuran as dimensións de prezos. |
| Facturación e prezos | 2558933 | **Importar desde as estimacións do proxecto** falla cando **msdyn\_ proxecto** engádese como dimensión de prezos. |
| Facturación e prezos | 2559101 | A eliminación de parámetros do proxecto non está bloqueada e causa problemas. |
|   Xestión de oportunidades | 2570390 | O complemento de escritura dual obriga a que o tipo de conta se faga en cotizacións, pedidos e oportunidades **Cliente**, aínda que ese tipo de conta non sexa correcto. |
| Facturación e prezos | 2586097 | Os custos reais facturados divididos non se inverten cando un proxecto se elimina dunha liña de contrato do proxecto. |
| Facturación e prezos | 2589619 | O imposto sobre o material rexistrado propágase aos reais de vendas non facturados e á factura. |
|   Xestión de oportunidades | 2594015 | Non se pode pechar unha cotización como gañada para os clientes que o teñan **Rede 60** Termos de pago. |
| Planificación e rastrexo de proxectos | 2595841 | En Proxecto para a web, os usuarios reciben unha mensaxe de erro sobre unha falta **msdyn\_ inicio real** cando crean unha nova solicitude de recurso. |
| Tempo e gasto | 2602511 | O **Rexeitado por** campo para entradas de tempo mostra **Sistema** en lugar dun usuario nomeado como o rexeitamento. |
| Tempo e gasto | 2602528 | Un aprobador de proxectos pode aprobar o tempo de proxectos nos que non figuren como aprobadores. |
| Facturación e prezos | 2608550 | Pódese confirmar unha factura de corrección aínda que non haxa cambios na orixinal. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión de proxectos e contabilidade en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Hai un desaxuste entre as operacións financeiras e do proxecto na duración permitida **ID de categoría** campo. |
| Xestión e contabilidade de proxectos | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Os proxectos de prezos fixos non se poden eliminar cando o **Facturación a conta** campo está configurado en **Perdas e ganancias** e o **Porcentaxe completada** utilízase o principio. |
| Xestión e contabilidade de proxectos | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Introdúcese un grupo de impostos sobre vendas predeterminado incorrecto desde a configuración do proxecto nas liñas de gasto do diario de integración de Operacións do proxecto. |
| Xestión e contabilidade de proxectos | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Non pode editar as dimensións da cabeceira da proposta de factura do proxecto nunha implementación integrada con Project Operations. |
| Xestión e contabilidade de proxectos | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Non se deben integrar as facturas de provedores entre empresas Dataverse. |
| Xestión e contabilidade de proxectos | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Hai un desaxuste na moeda dos saldos dos clientes e na moeda de informes. |
| Xestión e contabilidade de proxectos | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Pode publicar unha factura de proxecto aínda que o cliente estea en espera para todas as facturas. |
| Xestión e contabilidade de proxectos | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | O **Elimina todas as liñas** Falta o botón nas propostas de factura do proxecto que teñen o **Cabeceira** e **Liñas** vistas. |
| Xestión e contabilidade de proxectos | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Cando publica unha factura de provedor, prodúcese o seguinte erro: "A data contable da factura debe estar no mesmo exercicio contable que a orde de compra relacionada. Execute o proceso de fin de ano da orde de compra ou cambie a data ao exercicio contable actual". |
| Viaxes e gasto | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | O custo comprometido dun proxecto non se libera despois de que se libera o custo comprometido da solicitude de viaxe. |
| Viaxes e gasto | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | O seguinte erro prodúcese ao enviar un informe de gastos: "Rastrexo de pila: a empresa non existe". |
| Viaxes e gasto | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | O predeterminado **ID do proxecto** non se inscribe nos informes de gastos cando o **Require actividade para o diario** o parámetro está seleccionado no proxecto. |
| Viaxes e gasto | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | O **Gastos de publicación** o botón non funciona correctamente en Operacións do proxecto para escenarios de recursos/non abastecidos. |
| Viaxes e gasto | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Hai un problema con **Tarifa por milla** para un informe de gastos de quilometraxe que inclúa os pasaxeiros. |
| Viaxes e gasto | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | As taxas de quilometraxe dos gastos dos empregados non se suman correctamente cando se usan dous tipos de vehículos diferentes **Niveles de taxa de quilometraxe** categoría de gasto. |
| Viaxes e gasto | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | A busca de **Proxecto** o campo dunha liña de solicitude de viaxe non devolve a lista correcta de proxectos. |
| Viaxes e gasto | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Quilometraxe en revisión** mostra unha advertencia nos informes de gastos. |
| Viaxes e gasto | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | O servizo de recoñecemento óptico de caracteres (OCR) de recibos non funciona debido a un problema co URL do servizo OCR de gastos. |
| Viaxes e gasto | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Cando o **Capacidade de detallar os gastos recorrentes rapidamente** función está activada, os importes nas liñas de detalle dos informes de gastos cambian os importes cada vez que o **Detallar** ábrese a páxina. |
| Viaxes e gasto | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Non pode eliminar un informe de gastos cando a lista provisional ten máis dun aprobador. |

## <a name="removed-and-deprecated-features"></a>Funcións eliminadas e obsoletas

O [Funcións eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) o tema describe funcións que foron eliminadas ou obsoletas para Dynamics 365 Project Operations.

- Unha funcionalidade eliminada xa non está dispoñible no produto.
- Unha función obsoleta non está en desenvolvemento activo e é posible que se elimine nunha actualización futura.

Aparecerá un anuncio de desuso no [Funcións eliminadas ou obsoletas en Project Operations](removed-depreciated-features-project.md) tema 12 meses antes de que se elimine calquera característica do produto.

Para os cambios que só afectan ao tempo de compilación, pero son compatibles con sistemas binarios con entornos de produción e sandbox, o tempo de desuso será inferior a 12 meses. Normalmente, estes cambios son actualizacións funcionais que se deben facer no compilador.
