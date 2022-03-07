---
title: Novidades de abril de 2021 - despregamento lite de Project Operations
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de abril de 2021 do despregamento lite de Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009394"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Novidades de abril de 2021 - despregamento lite de Project Operations

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

  - Project Operations en ambiente de Dataverse versión 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- Materiais sen fornecemento para proxectos. As principais capacidades son:
  - Estimación e fixación de prezos de materiais sen fornecemento durante o ciclo de vendas dun proxecto. Para obter máis información, consulte [Configurar taxas de custo e vendas para produtos de catálogo - lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Rastrexo do uso de materiais sen fornecemento durante a entrega do proxecto. Para obter máis información, consulte [Rexistrar o uso do material en proxectos e tarefas de proxecto](../../material/material-usage-log.md).
  - Facturación de custos de material sen fornecemento usado. Para obter máis información, consulte [Xestionar o traballo pendente de facturación - lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - As novas API en Dynamics 365 Dataverse permiten crear, actualizar e eliminar operacións con **Entidades de programación**. Para obter máis información, consulte [Usar as API de programación para realizar operacións con entidades de programación](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Actualizacións de calidade

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Facturación e prezos | 2224568 | Engadiuse lóxica para permitir as personalizacións que implican invocar o complemento de confirmación da factura. |
| Facturación e prezos | 2101098 | Mellorouse a lóxica dos campos predefinidos para a factura proforma: **Enderezo de facturación**, **Nome de facturación** e **Condicións de pagamento** agora son os predefinidos no rexistro de cliente do contrato do proxecto correspondente. |
| Facturación e prezos | 2021413 | Actualizáronse os campos **Custo real** e **Vendas** na entidade **Tarefa** para incluír valores de vendas de gastos non facturados e facturados en tarefas. |
| Facturación e prezos | 2182110 | Ao copiar un contrato de proxecto, o ID da liña de contrato rexenerase no contrato de proxecto de destino para garantir que sexa único. |
| Xestión de oportunidades | 2186741 | Engadíronse validacións para garantir que o campo **Orixe** e **Tipo de transacción** non se poden actualizar nos detalles da liña de oferta existente. |
| Xestión de oportunidades | 2191353 | Non se deben crear fitos nunha liña de contrato de tempo e material. |
| Xestión de oportunidades | 2216956 | Solucionáronse problemas con **Actualizar prezos**. |
| Planificación e rastrexo | 2182979 | Mellorouse a función de copia do proxecto para garantir que se copian as liñas de estimación de gastos do proxecto orixinal. |
| Planificación e rastrexo | 2184144 | Mellorouse a función de copia do proxecto para garantir que se copia o nome do posto do recurso do proxecto orixinal. |
| Planificación e rastrexo | 2184799 | Copia do proxecto: Axustouse o control para garantir que a data estimada de inicio non se poida cambiar mentres a copia estea en curso. |
| Planificación e rastrexo | 2185134 | Copia do proxecto: A data de inicio estimada do proxecto de destino establécese na data de hoxe. |
| Planificación e rastrexo | 2196373 | Copia do proxecto: Garantir que o xestor do proxecto e os rexistros dos membros do equipo non están duplicados no equipo do proxecto. |
| Planificación e rastrexo | 2211833 | Copia do proxecto: As atribucións de recursos cópianse da tarefa do proxecto de orixe ao proxecto de destino. |
| Planificación e rastrexo | 2186541 | Solucionáronse problemas na grade **Estimacións** ao agruparse por recurso. |
| Planificación e rastrexo | 2166906 | A categoría de transacción dunha tarefa debe copiarse na entidade **Atribución de recursos**. |
| Xestión de recursos | 2125362 | Solucionáronse problemas coa creación dun membro xenérico do equipo mediante un método de asignación baseado en horas. |
| Tempo e gasto | 2113603 | Solucionouse o problema relacionado coa personalización coa eliminación de atributos da páxina **Entrada de tempo**. Agora o sistema comproba se o atributo existe na páxina antes de acceder a eles mediante un script. |
| Tempo e gasto | 2204377 | As follas de control horario copiadas deben amosarse automaticamente cando selecciona **Copiar Semana** durante a entrada de tempo. |
| Tempo e gasto | 2209059 | O campo **Estado** pode editarse para entradas de tempo de Dynamics 365 Field Service. |
