---
title: Desenvolver modelos de proxecto con Copiar proxecto
description: Este tema ofrece información sobre como crear modelos de proxecto usando a acción personalizada Copiar proxecto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642406"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolver modelos de proxecto con Copiar proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations admite a capacidade de copiar un proxecto e devolver as tarefas aos recursos xenéricos que representan o rol. Os clientes poden usar esta funcionalidade para crear modelos básicos de proxectos.

Cando selecciona **Copiar proxecto**, actualízase o estado do proxecto de destino. Use **Motivo para o estado** para determinar cando finaliza a acción de copia. Ao seleccionar **Copiar proxecto** tamén actualiza a data de inicio do proxecto á data de inicio actual se non se detecta ningunha data de destino na entidade de proxecto de destino.

## <a name="copy-project-custom-action"></a>Acción personalizada Copiar proxecto 

### <a name="name"></a>Nome 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parámetros de entrada
Hai tres parámetros de entrada:

| Parámetro          | Tipo   | Valores                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referencia de entidade | Proxecto de orixe |
| Destino             | Referencia de entidade | Proxecto de destino |


- **{"clearTeamsAndAssignments":true}**: O comportamento predefinido para o proxecto para a web, e eliminará todas as atribucións e membros do equipo.
- **{"removeNamedResources":true}** O comportamento predefinido para Project Operations e reverterá as atribucións a recursos xenéricos.

Para ver máis valores predefinidos para accións, consulte [Usar accións da API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especificar campos para copiar 
Cando se chama a acción, **Copiar proxecto** verá a vista do proxecto **Copiar as columnas do proxecto** para determinar que campos se copian cando se copia o proxecto.
