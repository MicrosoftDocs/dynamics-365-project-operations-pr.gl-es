---
title: Novidades de febreiro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de febreiro de 2021 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029613"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de febreiro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

- Project Operations en ambiente de Dataverse 4.7.0.95
- Xestión e contabilidade de proxectos en ambientes de aplicacións de Dynamics 365 Finance versión 10.0.16 

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| **Facturación e prezos** | 2053736 | Agora pódese acceder aos detalles da liña de factura indo a **Factura** > **Información relacionada**. |
| **Facturación e prezos** | 2122613 | As accións **Activar** e **Desactivar** elimináronse das entidades de asociación de **Lista de prezos**. |
| **Facturación e prezos** | 2128606 | Resolveuse o problema con **ullReferenceException** no complemento **GetEstimatesForProject**. |
| **Despregamento e configuración** | 2139346 | Resolveuse o problema coa importación da solución **Dynamics365ProjectOperationsDualWrite** non xestionada. |
| **Despregamento e configuración** | 2140569 | A solución do proxecto non debe instalarse nos ambientes de Dataverse Teams. |
| **Despregamento e configuración** | 2086991 | Localización personalizada restrinxida dos recursos web. |
| **Xestión de oportunidades** | 2136794 | Mostrar a mensaxe de erro correcta cando fallan os procesos **Confirmar factura** ou **Marcar factura como pagada**. |
| **Xestión de oportunidades** | 2139330 | Cambiar o xestor de proxectos nun proxecto non debe restablecer a empresa propietaria ao valor predefinido. |
| **Xestión de oportunidades** | 2146376 | O importe do imposto corrixido nun dato real non imputable créase a partir da confirmación da factura. |
| **Planificación e rastrexo de proxectos** | 2099879 | O despregamento do ambiente de Dataverse debe crear unha categoría de transacción predefinida cunha ID estática e non xerar unha aleatoriamente por ambiente. |
| **Planificación e rastrexo de proxectos** | 2128577 | Corrixíronse os privilexios de usuario de Project Service para actualizar a categoría de transacción nunha atribución de recursos. |
| **Planificación e rastrexo de proxectos** | 2164035 | Solucionáronse problemas coa función **Copiar proxecto**. |
| **Entrada de tempo** | 2129161 | Aplícanse restricións máis estritas para garantir que os usuarios non poidan cambiar e actualizar unha entrada de tempo que se enviou ou aprobou. |
| **Entrada de tempo** | 2103572 | A aprobación do tempo para as entradas de tempo fóra do proxecto non debe buscar o rol de responsable de aprobación do proxecto. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance 

Para obter máis información sobre a xestión e contabilidade de proxectos en Dynamics 365 Finance, consulte [Novidades de xaneiro 2021 - Project Operations para escenarios baseados en recursos/sen fornecemento](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Actualizacións normativas

Para obter información sobre actualizacións normativas para aplicacións de finanzas e operacións, vexa [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Outra forma de aprender sobre as actualizacións normativas é iniciar sesión en Lifecycle Services (LCS) e ver as actualizacións regulamentarias planificadas mediante a ferramenta de busca de problemas. A busca de problemas permítelle buscar por país, tipo de funcionalidade e lanzamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]