---
title: Rexistros de programación de proxectos
description: Este tema ofrece información e mostras que che axudarán a utilizar os rexistros de programación de proxectos para rastrexar os fallos relacionados co servizo de programación de proxectos e as API de programación de proxectos.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589516"
---
# <a name="project-scheduling-logs"></a>Rexistros de programación de proxectos

_**Aplícase a:** Operacións do proxecto para escenarios baseados en recursos/non abastecidos, implementación Lite: tramitación de facturación proforma_, _para a Web_

Microsoft Dynamics 365 Project Operations usos [Proxecto para a Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) como o seu principal motor de programación. En lugar de usar o estándar Microsoft Dataverse Interfaces de programación de aplicacións web (API), Project Operations usa as novas API de programación de proxectos para crear, actualizar e eliminar tarefas do proxecto, asignacións de recursos, dependencias de tarefas, depósitos de proxectos e membros dos equipos do proxecto. Non obstante, cando as operacións de creación, actualización ou eliminación se executan mediante programación en entidades de estrutura de descomposición do traballo (WBS), poden producirse erros. Para rastrexar estes erros e o historial de operacións, implementáronse dous novos rexistros administrativos: **Conxunto de operacións** e **Servizo de programación de proxectos (PSS)**. Para acceder a estes rexistros, vai a **Configuración** \> **Integración de horarios**.

A seguinte ilustración mostra o modelo de datos para os rexistros de programación do proxecto.

![Modelo de datos para os rexistros de programación do proxecto.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operación Establecer rexistro

O rexistro do conxunto de operacións fai un seguimento da execución dun conxunto de operacións que se usa para executar unha ou varias operacións de creación, actualización ou eliminación nun lote en proxectos, tarefas do proxecto, asignacións de recursos, dependencias de tarefas, depósitos de proxectos ou membros do equipo do proxecto. O **Operación en estado** campo mostra o estado xeral do conxunto de operacións. Os detalles da carga útil do conxunto de operacións recóllense nos rexistros de Detalles do conxunto de operacións relacionados.

### <a name="operation-set"></a>Conxunto de operacións

A seguinte táboa mostra os campos relacionados co **Conxunto de operacións** entidade.

| SchemaName            | Descripción                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | A data/hora na que se completou ou fallou a operación definida.                                                | CompletedOn            |
| msdyn_correlationid   | O **ID de correlación** valor da solicitude.                                                                  | CorrelationId          |
| msdyn_description     | A descrición do conxunto de operacións.                                                                        | Descripción            |
| msdyn_executedon      | A data/hora na que se executou o rexistro.                                                                       | Data de execución            |
| msdyn_operationsetId  | O identificador único das instancias da entidade.                                                                   | OperationSet           |
| msdyn_Project         | O proxecto que está relacionado co conxunto de operacións.                                                            | Project                |
| msdyn_projectid       | O **projectId** valor da solicitude.                                                                      | ProjectId (obsoleto) |
| msdyn_projectName     | Non aplicable.                                                                                              | Non aplicable         |
| msdyn_PSSErrorLog     | O identificador único do rexistro de erros de Project Scheduling Service que está asociado co conxunto de operacións. | Rexistro de erros de PSS          |
| msdyn_PSSErrorLogName | Non aplicable.                                                                                              | Non aplicable         |
| msdyn_status          | O estado do conxunto de operacións.                                                                             | Progresión                 |
| msdyn_statusName      | Non aplicable.                                                                                              | Non aplicable         |
| msdyn_useraadid       | O Azure Active Directory (Azure AD) ID de obxecto do usuario ao que pertence a solicitude.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalle do conxunto de operacións

A seguinte táboa mostra os campos relacionados co **Detalle do conxunto de operacións** entidade.

| SchemaName                 | Descripción                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | O serializado Dataverse campos para a solicitude.                                            | CdsPayload            |
| msdyn_entityname           | O nome da entidade para a solicitude.                                                     | EntityName            |
| msdyn_httpverb             | O método de solicitude.                                                                         | HTTPVerb (obsoleto) |
| msdyn_httpverbName         | Non aplicable.                                                                             | Non aplicable        |
| msdyn_operationset         | O identificador único do conxunto de operacións ao que pertence o rexistro.                      | OperationSet          |
| msdyn_operationsetdetailId | O identificador único das instancias da entidade.                                                  | Detalle de OperationSet   |
| msdyn_operationsetName     | Non aplicable.                                                                             | Non aplicable        |
| msdyn_operationtype        | O tipo de operación do detalle do conxunto de operacións.                                             | OperationType         |
| msdyn_operationtypeName    | Non aplicable.                                                                             | Non aplicable        |
| msdyn_psspayload           | Os campos serializados do Servizo de programación de proxectos para a solicitude.                           | PssPayload            |
| msdyn_recordid             | O identificador do rexistro da solicitude.                                                       | ID de rexistro             |
| msdyn_requestnumber        | Un número xerado automaticamente que identifica a orde na que se recibiron as solicitudes. | Número de solicitude        |

## <a name="project-scheduling-service-error-logs"></a>Rexistros de erros do servizo de programación de proxectos

Os rexistros de erros de Project Scheduling Service capturan os fallos que se producen cando o Project Scheduling Service tenta a **Gardar** ou **Aberto** operación. Hai tres escenarios compatibles nos que se xeran estes rexistros:

- As accións iniciadas polo usuario fallan gravemente (por exemplo, non se pode crear unha tarefa por falta de privilexios).
- O servizo de programación de proxectos non pode crear, actualizar, eliminar nin realizar ningunha outra operación en cascada nunha entidade mediante programación.
- O usuario experimenta erros cando un rexistro non se abre (por exemplo, cando se abre un proxecto ou se actualiza a información dun membro do equipo).

### <a name="project-scheduling-service-log"></a>Rexistro do servizo de programación de proxectos

A seguinte táboa mostra os campos que están incluídos no rexistro do servizo de programación de proxectos.

| SchemaName          | Descripción                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Montón de chamadas da excepción.                                               | Montón de chamadas     |
| msdyn_correlationid | O ID de correlación do erro.                                               | CorrelationId  |
| msdyn_errorcode     | Un campo que se usa para almacenar Dataverse código de erro ou código de erro HTTP. | Código de erro     |
| msdyn_HelpLink      | Unha ligazón á documentación de axuda pública.                                       | Ligazón de axuda      |
| msdyn_log           | O rexistro do Servizo de Programación de Proxectos.                                   | Rexistro            |
| msdyn_project       | O proxecto asociado ao rexistro de erros.                             | Project        |
| msdyn_projectName   | O nome do proxecto se manterase a carga útil do conxunto de operacións. | Non aplicable |
| msdyn_psserrorlogId | O identificador único das instancias da entidade.                                     | Rexistro de erros de PSS  |
| msdyn_SessionId     | ID da sesión do proxecto.                                                        | ID de sesión     |

## <a name="error-log-cleanup"></a>Erro na limpeza do rexistro

De forma predeterminada, tanto os rexistros de erros do servizo de programación de proxectos como o rexistro do conxunto de operacións pódense limpar cada 90 días. Eliminaranse os rexistros que teñan máis de 90 días. Non obstante, ao cambiar o valor do **msdyn_StateOperationSetAge** campo no **Parámetros do proxecto** páxina, os administradores poden axustar o intervalo de limpeza para que estea entre 1 e 120 días. Existen varios métodos para cambiar este valor:

- Personaliza o **Parámetro do proxecto** entidade creando unha páxina personalizada e engadindo o **Operacións obsoletas Establecer idade** campo.
- Use o código de cliente que use o [Kit de desenvolvemento de software WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Usa o código do SDK do servizo que utiliza o SDK Xrm **updateRecord** método (referencia de API de cliente) en aplicacións basadas en modelos. Power Apps inclúe unha descrición e os parámetros admitidos para o **updateRecord** método.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
