---
title: Novidades de marzo de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de marzo de 2021 de Project Operations para escenarios baseados en recursos ou non almacenados.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932938"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de marzo de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase ao seguinte Dynamics 365 Project Operations compoñentes e versións:

- Project Operations en ambiente de Dataverse versión 4.8.0.91 
- Xestión de proxectos e contabilidade no entorno Dynamics 365 Finance versión 10.0.16 

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse


| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Facturación e prezos | 2133873 | Corrixiuse a visualización do símbolo de moeda de **Prezo de venda unitario** na grade **Estimacións de gastos**. |
| Facturación e prezos | 2174616 | Cando se gaña unha oferta, faise referencia á lista de prezos personalizada do contrato nos detalles da liña do contrato que se copian da oferta. |
| Xestión de oportunidades | 2167475 | Importe fixo do imposto na factura de corrección que orixinou unha entrada real non facturada. |
| Xestión de oportunidades | 2176285 | Non se debe copiar o importe do imposto desde os detalles da liña de contrato de vendas/oferta ata os detalles da liña de contrato/oferta. |
| Xestión de oportunidades | 2188079 | Non se debe crear a regra de facturación dividida para contratos que non estean baseados en traballo. |
| Planificación e rastrexo | 2125274 | Actualizouse o atributo **Mapa de escritura dual do proxecto** para **Asignación de datas de inicio do proxecto** des **msdyn\_taskearlieststart** a **msdyn\_actualstart**. |
| Planificación e rastrexo | 2138853 | Actualizouse a función de copia do proxecto para garantir que as liñas de estimación de gastos que fan referencia ás tarefas se copian no proxecto de destino. |
| Planificación e rastrexo | 2154306 | Solucionáronse problemas coa eliminación de estimacións de gastos en Project Operations para situacións baseadas en recursos. |
| Planificación e rastrexo | 2173259 | Actualizouse a función de copia do proxecto para asegurarse de que non amosa a mensaxe de erro **Copiando WBS** en determinadas situacións. |
| Tempo e gasto | 2148910 | Solucionouse un problema de visualización coa páxina **Editar entrada** na grade **Entrada de tempo**. |
| Tempo e gasto | 2159798 | Reforzáronse os controis para garantir que non se poidan editar as entradas de gastos aprobadas. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión de proxectos e contabilidade en Dynamics 365 Finance

Para obter máis información, consulte [Novidades de xaneiro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Actualizacións normativas

Para obter información acerca das actualizacións regulamentarias para as aplicacións Finance and Operations, consulte [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Outra forma de aprender sobre as actualizacións normativas é iniciar sesión en LCS e ver as actualizacións regulamentarias planificadas mediante a ferramenta de busca de problemas. A busca de problemas permítelle buscar por país, tipo de funcionalidade e lanzamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]