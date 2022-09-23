---
title: Use as API de programación de proxectos para realizar operacións con entidades de programación
description: Este artigo ofrece información e mostras para usar as API de programación do proxecto.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541122"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Use as API de programación de proxectos para realizar operacións con entidades de programación

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


**Entidades de programación**

As API de programación de proxectos ofrecen a capacidade de realizar operacións de crear, actualizar e eliminar con **Entidades de programación**. Estas entidades xestiónanse a través do motor de programación en Project for the Web. Crear, actualizar e eliminar operacións con **Entidades de programación** estaban restrinxidos en versións anteriores de Dynamics 365 Project Operations.

A seguinte táboa ofrece unha lista completa das entidades de programación de proxectos.

| **Nome de entidade**         | **Nome lóxico da entidade**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarefa do proxecto            | msdyn_projecttask           |
| Dependencia da tarefa do proxecto | msdyn_projecttaskdependency |
| Atribución do recurso     | msdyn_resourceassignment    |
| Depósito do proxecto          | msdyn_projectbucket         |
| Membro do equipo do proxecto     | msdyn_projectteam           |
| Listas de verificación do proxecto      | msdyn_projectchecklist      |
| Etiqueta do proxecto           | msdyn_projectlabel          |
| Tarefa do proxecto para etiquetar   | msdyn_projecttasktolabel    |
| Sprint do proxecto          | msdyn_projectsprint         |

**OperationSet**

OperationSet é un patrón de unidade de traballo que se pode empregar cando se deben procesar varias solicitudes que afectan á programación dentro dunha transacción.

**API de programación de proxectos**

A continuación móstrase unha lista das API de programación de proxectos actuais.

| **API**                                 | Descripción                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Esta API úsase para crear un proxecto. O proxecto e o conxunto de proxectos predeterminados créanse inmediatamente.                         |
| **msdyn_CreateTeamMemberV1**            | Esta API úsase para crear un membro do equipo do proxecto. O rexistro de membro do equipo créase inmediatamente.                                  |
| **msdyn_CreateOperationSetV1**          | Esta API úsase para programar varias solicitudes que deben realizarse nunha transacción.                                        |
| **msdyn_PssCreateV1**                   | Esta API úsase para crear unha entidade. A entidade pode ser calquera das entidades de programación de proxectos que admitan a operación de creación. |
| **msdyn_PssUpdateV1**                   | Esta API úsase para actualizar unha entidade. A entidade pode ser calquera das entidades de programación do proxecto que admitan a operación de actualización  |
| **msdyn_PssDeleteV1**                   | Esta API úsase para eliminar unha entidade. A entidade pode ser calquera das entidades de programación de proxectos que admitan a operación de eliminación. |
| **msdyn_ExecuteOperationSetV1**         | Esta API úsase para executar todas as operacións dentro do conxunto de operacións dado.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Esta API úsase para actualizar un contorno de traballo planificado da asignación de recursos.                                                        |



**Usando as API de programación de proxectos con OperationSet**

Como os rexistros con **CreateProjectV1** e **CreateTeamMemberV1** créanse inmediatamente, estas API non se poden empregar en **OperationSet** directamente. Non obstante, pode usar a API para crear rexistros necesarios, crear un **OperationSet** e, a seguir, usar estes rexistros creados previamente no **OperationSet**.

**Operacións compatibles**

| **Entidade de programación**   | **Crear** | **Actualización** | **SUPR** | **Consideracións importantes**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tarefa do proxecto            | Si        | Si        | Si        | O **Progreso**, **completado**, e **EsforzoRestante** os campos pódense editar en Project for the Web, pero non se poden editar en Project Operations.                                                                                                                                                                                             |
| Dependencia da tarefa do proxecto | Si        | No         | Si        | Os rexistros de dependencia de tarefas do proxecto non se actualizan. Pola contra, pódese eliminar un rexistro antigo e crear un rexistro novo.                                                                                                                                                                                                                                 |
| Atribución do recurso     | Si        | Si\*      | Si        | Non se admiten operacións cos seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. Os rexistros de atribución de recursos non se actualizan. Pola contra, pódese eliminar o rexistro antigo e crear un novo rexistro. Forneceuse unha API separada para actualizar os contornos de asignación de recursos. |
| Depósito do proxecto          | Si        | Si        | Si        | O depósito predeterminado créase usando o **CrearProxectoV1** API. A compatibilidade para crear e eliminar grupos de proxectos engadiuse na actualización 16.                                                                                                                                                                                                   |
| Membro do equipo do proxecto     | Si        | Si        | Si        | Para a operación de creación, use a API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Si        | Si        |            | Non se admiten operacións cos seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.                                                                                       |
| Listas de verificación do proxecto      | Si        | Si        | Si        |                                                                                                                                                                                                                                                                                                                                                         |
| Etiqueta do proxecto           | No         | Si        | No         | Os nomes das etiquetas pódense cambiar. Esta función só está dispoñible para Project for the Web                                                                                                                                                                                                                                                                      |
| Tarefa do proxecto para etiquetar   | Si        | No         | Si        | Esta función só está dispoñible para Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint do proxecto          | Si        | Si        | Si        | O **Comeza** campo debe ter unha data anterior á **Remate** campo. Os sprints para o mesmo proxecto non poden superpoñerse entre si. Esta función só está dispoñible para Project for the Web                                                                                                                                                                    |




A propiedade de ID é opcional. Se se proporciona, o sistema tenta usala e lanza unha excepción se non se pode usar. Se non se proporciona, o sistema xeraraa.

**Limitacións e problemas coñecidos**

A continuación móstrase unha lista de limitacións e problemas coñecidos:

-   As API de Project Schedule só poden ser usadas por **Usuarios con licenza de Microsoft Project**. Non poden ser usadas por:
    -   Usuarios da aplicación
    -   Usuario do sistema
    -   Usuarios de integración
    -   Outros usuarios que non teñen a licenza requirida
-   Cada **OperationSet** só pode ter un máximo de 100 operacións.
-   Cada usuario só pode ter un máximo de 10 **OperationSets** abertos.
-   Project Operations admite actualmente un máximo de 500 tarefas totais nun proxecto.
-   Cada operación de actualización de contorno de asignación de recursos conta como unha única operación.
-   Cada lista de contornos actualizados pode conter un máximo de 100 intervalos de tempo.
-   O estado de fallo e os rexistros de fallos de **OperationSet** non están dispoñibles actualmente.
-   Hai un máximo de 400 sprints por proxecto.
-   [Límites e límites en proxectos e tarefas](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Actualmente, as etiquetas só están dispoñibles para Project for the Web.

**Tratamento de erros**

-   Para revisar os erros xerados a partir dos conxuntos de operacións, vaia a **Configuración** \> **Integración de programación** \> **Conxuntos de operacións**.
-   Para revisar os erros xerados desde o servizo de programación de proxectos, vaia a **Configuración** \> **Integración de programación** \> **Rexistros de erros de PSS**.

**Edición de contornos de asignación de recursos**

A diferenza de todas as outras API de programación de proxectos que actualizan unha entidade, a API de contorno de asignación de recursos é a única responsable das actualizacións dun só campo, msdyn_plannedwork, nunha única entidade, msydn_resourceassignment.

O modo de programación dado é:

-   **unidades fixas**
-   O calendario do proxecto é de 9-5 p. é de 9-5 pst, luns, martes, xoves, venres (SEN TRABALLO OS MÉRCORES)
-   E o calendario de recursos é de 9-1p PST de luns a venres

Este traballo é dunha semana, catro horas ao día. Isto débese a que o calendario de recursos é de 9-1 PST, ou catro horas ao día.

| &nbsp;     | Tarefa | Data de inicio | Data de fin  | Cantidade | 13/06/2022 | 14/06/2022 | 15/06/2022 | 16/06/2022 | 17/06/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 traballador |  T1  | 13/06/2022  | 17/06/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Por exemplo, se quere que o traballador só traballe tres horas ao día esta semana e permita unha hora para outras tarefas.

#### <a name="updatedcontours-sample-payload"></a>Carga útil de mostra de UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Esta é a asignación despois de que se execute a API Update Contour Schedule.

| &nbsp;     | Tarefa | Data de inicio | Data de fin  | Cantidade | 13/06/2022 | 14/06/2022 | 15/06/2022 | 16/06/2022 | 17/06/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 traballador | T1   | 13/06/2022  | 17/06/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Escenario de exemplo**

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

** Mostras adicionais

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
