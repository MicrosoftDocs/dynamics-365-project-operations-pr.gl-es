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
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="10b16-103">Desenvolver modelos de proxecto con Copiar proxecto</span><span class="sxs-lookup"><span data-stu-id="10b16-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="10b16-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="10b16-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="10b16-105">Dynamics 365 Project Operations admite a capacidade de copiar un proxecto e devolver as tarefas aos recursos xenéricos que representan o rol.</span><span class="sxs-lookup"><span data-stu-id="10b16-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="10b16-106">Os clientes poden usar esta funcionalidade para crear modelos básicos de proxectos.</span><span class="sxs-lookup"><span data-stu-id="10b16-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="10b16-107">Cando selecciona **Copiar proxecto**, actualízase o estado do proxecto de destino.</span><span class="sxs-lookup"><span data-stu-id="10b16-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="10b16-108">Use **Motivo para o estado** para determinar cando finaliza a acción de copia.</span><span class="sxs-lookup"><span data-stu-id="10b16-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="10b16-109">Ao seleccionar **Copiar proxecto** tamén actualiza a data de inicio do proxecto á data de inicio actual se non se detecta ningunha data de destino na entidade de proxecto de destino.</span><span class="sxs-lookup"><span data-stu-id="10b16-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="10b16-110">Acción personalizada Copiar proxecto</span><span class="sxs-lookup"><span data-stu-id="10b16-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="10b16-111">Nome</span><span class="sxs-lookup"><span data-stu-id="10b16-111">Name</span></span> 

<span data-ttu-id="10b16-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="10b16-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="10b16-113">Parámetros de entrada</span><span class="sxs-lookup"><span data-stu-id="10b16-113">Input parameters</span></span>
<span data-ttu-id="10b16-114">Hai tres parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="10b16-114">There are three input parameters:</span></span>

| <span data-ttu-id="10b16-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="10b16-115">Parameter</span></span>          | <span data-ttu-id="10b16-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="10b16-116">Type</span></span>   | <span data-ttu-id="10b16-117">Valores</span><span class="sxs-lookup"><span data-stu-id="10b16-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="10b16-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="10b16-118">ProjectCopyOption</span></span>  | <span data-ttu-id="10b16-119">String</span><span class="sxs-lookup"><span data-stu-id="10b16-119">String</span></span> | <span data-ttu-id="10b16-120">**{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="10b16-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="10b16-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="10b16-121">SourceProject</span></span>      | <span data-ttu-id="10b16-122">Referencia de entidade</span><span class="sxs-lookup"><span data-stu-id="10b16-122">Entity Reference</span></span> | <span data-ttu-id="10b16-123">Proxecto de orixe</span><span class="sxs-lookup"><span data-stu-id="10b16-123">Source Project</span></span> |
| <span data-ttu-id="10b16-124">Destino</span><span class="sxs-lookup"><span data-stu-id="10b16-124">Target</span></span>             | <span data-ttu-id="10b16-125">Referencia de entidade</span><span class="sxs-lookup"><span data-stu-id="10b16-125">Entity Reference</span></span> | <span data-ttu-id="10b16-126">Proxecto de destino</span><span class="sxs-lookup"><span data-stu-id="10b16-126">Target Project</span></span> |


- <span data-ttu-id="10b16-127">**{"clearTeamsAndAssignments":true}**: O comportamento predefinido para o proxecto para a web, e eliminará todas as atribucións e membros do equipo.</span><span class="sxs-lookup"><span data-stu-id="10b16-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="10b16-128">**{"removeNamedResources":true}** O comportamento predefinido para Project Operations e reverterá as atribucións a recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="10b16-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="10b16-129">Para ver máis valores predefinidos para accións, consulte [Usar accións da API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="10b16-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="10b16-130">Especificar campos para copiar</span><span class="sxs-lookup"><span data-stu-id="10b16-130">Specify fields to copy</span></span> 
<span data-ttu-id="10b16-131">Cando se chama a acción, **Copiar proxecto** verá a vista do proxecto **Copiar as columnas do proxecto** para determinar que campos se copian cando se copia o proxecto.</span><span class="sxs-lookup"><span data-stu-id="10b16-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
