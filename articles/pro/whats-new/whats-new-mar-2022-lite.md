---
title: Novidades marzo 2022 - Despregamento de Project Operations lite
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de marzo de 2022 do despregamento de Project Operations lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934226"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novidades marzo 2022 - Despregamento de Project Operations lite

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.30.0.99

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

- Subcontratación: creación de facturas de fornecedor e coincidencia de experiencias

## <a name="quality-updates"></a>Actualizacións de calidade

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

## <a name="removed-and-deprecated-features"></a>Funcionalidades eliminadas e obsoletas

O artigo [Funcionalidades eliminadas ou obsoletas en Project Operations](../../whats-new/removed-depreciated-features-project.md) describe funcionalidades que se eliminaron ou quedaron obsoletas para Dynamics 365 Project Operations.

- Unha funcionalidade eliminada xa non está dispoñible no produto.
- Unha funcionalidade obsoleta non está en desenvolvemento activo e podería eliminarse nunha futura actualización.

Aparecerá un anuncio de obsolescencia no artigo [Funcionalidades eliminadas ou obsoletas en Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 meses antes de que se elimine calquera funcionalidade do produto.
