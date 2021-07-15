---
title: Use as API de programación de proxectos para realizar operacións con entidades de programación
description: Este tema ofrece información e mostras para usar as API de programación de proxectos.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293225"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Use as API de programación de proxectos para realizar operacións con entidades de programación

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

> [!IMPORTANT] 
> Unha parte ou toda a funcionalidade sinalada neste tema está dispoñible como parte dunha versión preliminar. O contido e a funcionalidade están suxeitos a cambios. 

## <a name="scheduling-entities"></a>Entidades de programación

As API de programación de proxectos ofrecen a capacidade de realizar operacións de crear, actualizar e eliminar con **Entidades de programación**. Estas entidades xestiónanse a través do motor de programación en Project for the Web. Crear, actualizar e eliminar operacións con **Entidades de programación** estaban restrinxidos en versións anteriores de Dynamics 365 Project Operations.

A seguinte táboa ofrece unha lista completa das entidades de programación de proxectos.

| Nome da entidade  | Nome lóxico da entidade |
| --- | --- |
| Project | msdyn_project |
| Tarefa do proxecto  | msdyn_projecttask  |
| Dependencia da tarefa do proxecto  | msdyn_projecttaskdependency  |
| Atribución do recurso | msdyn_resourceassignment |
| Depósito do proxecto  | msdyn_projectbucket |
| Membro do equipo do proxecto | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet é un patrón de unidade de traballo que se pode empregar cando se deben procesar varias solicitudes que afectan á programación dentro dunha transacción.

## <a name="project-schedule-apis"></a>API de programación de proxectos

A continuación móstrase unha lista das API de programación de proxectos actuais.

- **msdyn_CreateProjectV1**: Esta API pódese usar para crear un proxecto. O proxecto e o depósito por defecto do proxecto créanse inmediatamente.
- **msdyn_CreateTeamMemberV1**: Esta API pódese usar para crear un membro do equipo do proxecto. O rexistro de membro do equipo créase inmediatamente.
- **msdyn_CreateOperationSetV1**: Esta API pode usarse para programar varias solicitudes que deben realizarse dentro dunha transacción.
- **msdyn_PSSCreateV1**: Esta API pódese usar para crear unha entidade. A entidade pode ser calquera das entidades de programación de proxectos que admitan a operación de creación.
- **msdyn_PSSUpdateV1**: Esta API pódese usar para actualizar unha entidade. A entidade pode ser calquera das entidades de programación de proxectos que admitan a operación de actualización.
- **msdyn_PSSDeleteV1**: Esta API pódese usar para eliminar unha entidade. A entidade pode ser calquera das entidades de programación de proxectos que admitan a operación de eliminación.
- **msdyn_ExecuteOperationSetV1**: Esta API úsase para executar todas as operacións dentro do conxunto de operacións determinado.

## <a name="using-project-schedule-apis-with-operationset"></a>Usando as API de programación de proxectos con OperationSet

Como os rexistros con **CreateProjectV1** e **CreateTeamMemberV1** créanse inmediatamente, estas API non se poden empregar en **OperationSet** directamente. Non obstante, pode usar a API para crear rexistros necesarios, crear un **OperationSet** e, a seguir, usar estes rexistros creados previamente no **OperationSet**.

## <a name="supported-operations"></a>Operacións compatibles

| Entidade de programación | Crear | Actualización | SUPR | Consideracións importantes |
| --- | --- | --- | --- | --- |
Tarefa do proxecto | Si | Si | Si | Nada |
| Dependencia da tarefa do proxecto | Si | Si | | Os rexistros de dependencia de tarefas do proxecto non se actualizan. Pola contra, pódese eliminar un rexistro antigo e pódese crear un novo rexistro. |
| Atribución do recurso | Si | Si | | Non se admiten operacións cos seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. Os rexistros de atribución de recursos non se actualizan. Pola contra, pódese eliminar o rexistro antigo e pódese crear un novo rexistro. |
| Depósito do proxecto | N/D | N/D | N/D | O depósito predefinido créase usando a API **CreateProjectV1**. |
| Membro do equipo do proxecto | Si | Si | Si | Para a operación de creación, use a API **CreateTeamMemberV1**. |
| Project | Si | Si | N/D | Non se admiten operacións cos seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**. |

Estas API pódense chamar con obxectos de entidade que inclúen campos personalizados.

A propiedade de ID é opcional. Se se proporciona, o sistema tenta usala e lanza unha excepción se non se pode usar. Se non se proporciona, o sistema xeraraa.

## <a name="restricted-fields"></a>Campos restrinxidos

As táboas seguintes definen os campos que están restrinxidos de **Crear** e **Editar.**

### <a name="project-task"></a>Tarefa do proxecto

| **Nome lóxico**                       | **Pode crear** | **Pode editar**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | non             | non               |
| msdyn_actualcost_base                  | non             | non               |
| msdyn_actualend                        | non             | non               |
| msdyn_actualsales                      | non             | non               |
| msdyn_actualsales_base                 | non             | non               |
| msdyn_actualstart                      | non             | non               |
| msdyn_costatcompleteestimate           | non             | non               |
| msdyn_costatcompleteestimate_base      | non             | non               |
| msdyn_costconsumptionpercentage        | non             | non               |
| msdyn_effortcompleted                  | non             | non               |
| msdyn_effortestimateatcomplete         | non             | non               |
| msdyn_iscritical                       | non             | non               |
| msdyn_iscriticalname                   | non             | non               |
| msdyn_ismanual                         | non             | non               |
| msdyn_ismanualname                     | non             | non               |
| msdyn_ismilestone                      | non             | non               |
| msdyn_ismilestonename                  | non             | non               |
| msdyn_LinkStatus                       | non             | non               |
| msdyn_linkstatusname                   | non             | non               |
| msdyn_msprojectclientid                | non             | non               |
| msdyn_plannedcost                      | non             | non               |
| msdyn_plannedcost_base                 | non             | non               |
| msdyn_plannedsales                     | non             | non               |
| msdyn_plannedsales_base                | non             | non               |
| msdyn_pluginprocessingdata             | non             | non               |
| msdyn_progress                         | non             | non (si para P4W) |
| msdyn_remainingcost                    | non             | non               |
| msdyn_remainingcost_base               | non             | non               |
| msdyn_remainingsales                   | non             | non               |
| msdyn_remainingsales_base              | non             | non               |
| msdyn_requestedhours                   | non             | non               |
| msdyn_resourcecategory                 | non             | non               |
| msdyn_resourcecategoryname             | non             | non               |
| msdyn_resourceorganizationalunitid     | non             | non               |
| msdyn_resourceorganizationalunitidname | non             | non               |
| msdyn_salesconsumptionpercentage       | non             | non               |
| msdyn_salesestimateatcomplete          | non             | non               |
| msdyn_salesestimateatcomplete_base     | non             | non               |
| msdyn_salesvariance                    | non             | non               |
| msdyn_salesvariance_base               | non             | non               |
| msdyn_scheduleddurationminutes         | non             | non               |
| msdyn_scheduledend                     | non             | non               |
| msdyn_scheduledstart                   | non             | non               |
| msdyn_schedulevariance                 | non             | non               |
| msdyn_skipupdateestimateline           | non             | non               |
| msdyn_skipupdateestimatelinename       | non             | non               |
| msdyn_summary                          | non             | non               |
| msdyn_varianceofcost                   | non             | non               |
| msdyn_varianceofcost_base              | non             | non               |

### <a name="project-task-dependency"></a>Dependencia da tarefa do proxecto

| **Nome lóxico**              | **Pode crear** | **Pode editar** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | non             | non           |
| msdyn_linktypename            | non             | non           |
| msdyn_predecessortask         | si            | non           |
| msdyn_predecessortaskname     | si            | non           |
| msdyn_project                 | si            | non           |
| msdyn_projectname             | si            | non           |
| msdyn_projecttaskdependencyid | si            | non           |
| msdyn_successortask           | si            | non           |
| msdyn_successortaskname       | si            | non           |

### <a name="resource-assignment"></a>Atribución do recurso

| **Nome lóxico**             | **Pode crear** | **Pode editar** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | si            | non           |
| msdyn_bookableresourceidname | si            | non           |
| msdyn_bookingstatusid        | non             | non           |
| msdyn_bookingstatusidname    | non             | non           |
| msdyn_committype             | non             | non           |
| msdyn_committypename         | non             | non           |
| msdyn_effort                 | non             | non           |
| msdyn_effortcompleted        | non             | non           |
| msdyn_effortremaining        | non             | non           |
| msdyn_finish                 | non             | non           |
| msdyn_plannedcost            | non             | non           |
| msdyn_plannedcost_base       | non             | non           |
| msdyn_plannedcostcontour     | non             | non           |
| msdyn_plannedsales           | non             | non           |
| msdyn_plannedsales_base      | non             | non           |
| msdyn_plannedsalescontour    | non             | non           |
| msdyn_plannedwork            | non             | non           |
| msdyn_projectid              | si            | non           |
| msdyn_projectidname          | non             | non           |
| msdyn_projectteamid          | non             | non           |
| msdyn_projectteamidname      | non             | non           |
| msdyn_start                  | non             | non           |
| msdyn_taskid                 | non             | non           |
| msdyn_taskidname             | non             | non           |
| msdyn_userresourceid         | non             | non           |

### <a name="project-team-member"></a>Membro do equipo do proxecto

| **Nome lóxico**                                 | **Pode crear** | **Pode editar** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | non             | non           |
| msdyn_creategenericteammemberwithrequirementname | non             | non           |
| msdyn_deletestatus                               | non             | non           |
| msdyn_deletestatusname                           | non             | non           |
| msdyn_effort                                     | non             | non           |
| msdyn_effortcompleted                            | non             | non           |
| msdyn_effortremaining                            | non             | non           |
| msdyn_finish                                     | non             | non           |
| msdyn_hardbookedhours                            | non             | non           |
| msdyn_hours                                      | non             | non           |
| msdyn_markedfordeletiontimer                     | non             | non           |
| msdyn_markedfordeletiontimestamp                 | non             | non           |
| msdyn_msprojectclientid                          | non             | non           |
| msdyn_percentage                                 | non             | non           |
| msdyn_requiredhours                              | non             | non           |
| msdyn_softbookedhours                            | non             | non           |
| msdyn_start                                      | non             | non           |

### <a name="project"></a>Project

| **Nome lóxico**                       | **Pode crear** | **Pode editar** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | non             | non           |
| msdyn_actualexpensecost_base           | non             | non           |
| msdyn_actuallaborcost                  | non             | non           |
| msdyn_actuallaborcost_base             | non             | non           |
| msdyn_actualsales                      | non             | non           |
| msdyn_actualsales_base                 | non             | non           |
| msdyn_contractlineproject              | si            | non           |
| msdyn_contractorganizationalunitid     | si            | non           |
| msdyn_contractorganizationalunitidname | si            | non           |
| msdyn_costconsumption                  | non             | non           |
| msdyn_costestimateatcomplete           | non             | non           |
| msdyn_costestimateatcomplete_base      | non             | non           |
| msdyn_costvariance                     | non             | non           |
| msdyn_costvariance_base                | non             | non           |
| msdyn_duration                         | non             | non           |
| msdyn_effort                           | non             | non           |
| msdyn_effortcompleted                  | non             | non           |
| msdyn_effortestimateatcompleteeac      | non             | non           |
| msdyn_effortremaining                  | non             | non           |
| msdyn_finish                           | si            | si          |
| msdyn_globalrevisiontoken              | non             | non           |
| msdyn_islinkedtomsprojectclient        | non             | non           |
| msdyn_islinkedtomsprojectclientname    | non             | non           |
| msdyn_linkeddocumenturl                | non             | non           |
| msdyn_msprojectdocument                | non             | non           |
| msdyn_msprojectdocumentname            | non             | non           |
| msdyn_plannedexpensecost               | non             | non           |
| msdyn_plannedexpensecost_base          | non             | non           |
| msdyn_plannedlaborcost                 | non             | non           |
| msdyn_plannedlaborcost_base            | non             | non           |
| msdyn_plannedsales                     | non             | non           |
| msdyn_plannedsales_base                | non             | non           |
| msdyn_progress                         | non             | non           |
| msdyn_remainingcost                    | non             | non           |
| msdyn_remainingcost_base               | non             | non           |
| msdyn_remainingsales                   | non             | non           |
| msdyn_remainingsales_base              | non             | non           |
| msdyn_replaylogheader                  | non             | non           |
| msdyn_salesconsumption                 | non             | non           |
| msdyn_salesestimateatcompleteeac       | non             | non           |
| msdyn_salesestimateatcompleteeac_base  | non             | non           |
| msdyn_salesvariance                    | non             | non           |
| msdyn_salesvariance_base               | non             | non           |
| msdyn_scheduleperformance              | non             | non           |
| msdyn_scheduleperformancename          | non             | non           |
| msdyn_schedulevariance                 | non             | non           |
| msdyn_taskearlieststart                | non             | non           |
| msdyn_teamsize                         | non             | non           |
| msdyn_teamsize_date                    | non             | non           |
| msdyn_teamsize_state                   | non             | non           |
| msdyn_totalactualcost                  | non             | non           |
| msdyn_totalactualcost_base             | non             | non           |
| msdyn_totalplannedcost                 | non             | non           |
| msdyn_totalplannedcost_base            | non             | non           |


## <a name="limitations-and-known-issues"></a>Limitacións e problemas coñecidos
A continuación móstrase unha lista de limitacións e problemas coñecidos:

- As API de programación de proxectos só as poden usar **Usuarios con licenza de Microsoft Project.** Non poden ser usadas por:
    - Usuarios da aplicación
    - Usuario do sistema
    - Usuarios de integración
    - Outros usuarios que non teñen a licenza requirida
- Cada **OperationSet** só pode ter un máximo de 100 operacións.
- Cada usuario só pode ter un máximo de 10 **OperationSets** abertos.
- Project Operations admite actualmente un máximo de 500 tarefas totais nun proxecto.
- O estado de fallo e os rexistros de fallos de **OperationSet** non están dispoñibles actualmente.
- [Límites en proxectos e tarefas](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Tratamento de erros

   - Para revisar os erros xerados a partir dos conxuntos de operacións, vaia a **Configuración** \> **Integración de programación** \> **Conxuntos de operacións**.
   - Para revisar os erros xerados desde o servizo de programación de proxectos, vaia a **Configuración** \> **Integración de programación** \> **Rexistros de erros de PSS**.

## <a name="sample-scenario"></a>Escenario de exemplo

Neste escenario, creará un proxecto, un membro do equipo, catro tarefas e dúas atribucións de recursos. A continuación, actualizará unha tarefa, actualizará o proxecto, eliminará unha tarefa, eliminará unha atribución de recursos e creará unha dependencia de tarefas.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Exemplos adicionais

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
