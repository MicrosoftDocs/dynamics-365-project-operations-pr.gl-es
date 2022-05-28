---
title: Novidades marzo 2022 - Despregamento de Project Operations lite
description: Este tema ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de marzo de 2022 da implantación de Project Operations lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583748"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novidades marzo 2022 - Despregamento de Project Operations lite

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este tema aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.30.0.99

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

- Subcontratación: creación de facturas de provedores e experiencias de emparellamento

## <a name="quality-updates"></a>Actualizacións de calidade

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

## <a name="removed-and-deprecated-features"></a>Funcións eliminadas e obsoletas

O [Funcións eliminadas ou obsoletas en Project Operations](../../whats-new/removed-depreciated-features-project.md) o tema describe as funcións que foron eliminadas ou obsoletas Dynamics 365 Project Operations.

- Unha funcionalidade eliminada xa non está dispoñible no produto.
- Unha función obsoleta non está en desenvolvemento activo e é posible que se elimine nunha actualización futura.

Aparecerá un anuncio de desuso no [Funcións eliminadas ou obsoletas en Project Operations](../../whats-new/removed-depreciated-features-project.md) tema 12 meses antes de que se elimine calquera característica do produto.
