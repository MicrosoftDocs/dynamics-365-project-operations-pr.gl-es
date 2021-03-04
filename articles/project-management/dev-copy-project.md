---
title: Desenvolver modelos de proxecto con Copiar proxecto
description: Este tema ofrece información sobre como crear modelos de proxecto usando a acción personalizada Copiar proxecto.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045007"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="41394-103">Desenvolver modelos de proxecto con Copiar proxecto</span><span class="sxs-lookup"><span data-stu-id="41394-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="41394-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="41394-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="41394-105">Dynamics 365 Project Operations admite a capacidade de copiar un proxecto e devolver as tarefas aos recursos xenéricos que representan o rol.</span><span class="sxs-lookup"><span data-stu-id="41394-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="41394-106">Os clientes poden usar esta funcionalidade para crear modelos básicos de proxectos.</span><span class="sxs-lookup"><span data-stu-id="41394-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="41394-107">Cando selecciona **Copiar proxecto**, actualízase o estado do proxecto de destino.</span><span class="sxs-lookup"><span data-stu-id="41394-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="41394-108">Use **Motivo para o estado** para determinar cando finaliza a acción de copia.</span><span class="sxs-lookup"><span data-stu-id="41394-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="41394-109">Ao seleccionar **Copiar proxecto** tamén actualiza a data de inicio do proxecto á data de inicio actual se non se detecta ningunha data de destino na entidade de proxecto de destino.</span><span class="sxs-lookup"><span data-stu-id="41394-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="41394-110">Acción personalizada Copiar proxecto</span><span class="sxs-lookup"><span data-stu-id="41394-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="41394-111">Nome</span><span class="sxs-lookup"><span data-stu-id="41394-111">Name</span></span> 

<span data-ttu-id="41394-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="41394-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="41394-113">Parámetros de entrada</span><span class="sxs-lookup"><span data-stu-id="41394-113">Input parameters</span></span>
<span data-ttu-id="41394-114">Hai tres parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="41394-114">There are three input parameters:</span></span>

| <span data-ttu-id="41394-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="41394-115">Parameter</span></span>          | <span data-ttu-id="41394-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="41394-116">Type</span></span>   | <span data-ttu-id="41394-117">Valores</span><span class="sxs-lookup"><span data-stu-id="41394-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="41394-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="41394-118">ProjectCopyOption</span></span>  | <span data-ttu-id="41394-119">String</span><span class="sxs-lookup"><span data-stu-id="41394-119">String</span></span> | <span data-ttu-id="41394-120">**{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="41394-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="41394-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="41394-121">SourceProject</span></span>      | <span data-ttu-id="41394-122">Referencia de entidade</span><span class="sxs-lookup"><span data-stu-id="41394-122">Entity Reference</span></span> | <span data-ttu-id="41394-123">Proxecto de orixe</span><span class="sxs-lookup"><span data-stu-id="41394-123">Source Project</span></span> |
| <span data-ttu-id="41394-124">Destino</span><span class="sxs-lookup"><span data-stu-id="41394-124">Target</span></span>             | <span data-ttu-id="41394-125">Referencia de entidade</span><span class="sxs-lookup"><span data-stu-id="41394-125">Entity Reference</span></span> | <span data-ttu-id="41394-126">Proxecto de destino</span><span class="sxs-lookup"><span data-stu-id="41394-126">Target Project</span></span> |


- <span data-ttu-id="41394-127">**{"clearTeamsAndAssignments":true}**: O comportamento predefinido para o proxecto para a web, e eliminará todas as atribucións e membros do equipo.</span><span class="sxs-lookup"><span data-stu-id="41394-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="41394-128">**{"removeNamedResources":true}** O comportamento predefinido para Project Operations e reverterá as atribucións a recursos xenéricos.</span><span class="sxs-lookup"><span data-stu-id="41394-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="41394-129">Para ver máis valores predefinidos para accións, consulte [Usar accións da API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="41394-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="41394-130">Especificar campos para copiar</span><span class="sxs-lookup"><span data-stu-id="41394-130">Specify fields to copy</span></span> 
<span data-ttu-id="41394-131">Cando se chama a acción, **Copiar proxecto** verá a vista do proxecto **Copiar as columnas do proxecto** para determinar que campos se copian cando se copia o proxecto.</span><span class="sxs-lookup"><span data-stu-id="41394-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="41394-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="41394-132">Example</span></span>
<span data-ttu-id="41394-133">O seguinte exemplo mostra como chamar á acción personalizada **CopyProject** co grupo de parámetros **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="41394-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
