---
title: Rexistros de programación de proxectos
description: Este artigo ofrece información e mostras que lle axudarán a utilizar os rexistros de programación de proxectos para rastrexar os erros relacionados co servizo de programación de proxectos e as API de programación de proxectos.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923693"
---
# <a name="project-scheduling-logs"></a>Rexistros de programación de proxectos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento, despregamento de Lite: facturación proforma_, _Project for the Web_

Microsoft Dynamics 365 Project Operations usa [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) como o seu principal motor de programación. En lugar de usar as interfaces de programación de aplicacións (API) estándar de Microsoft Dataverse Web, Project Operations usa as novas API de programación de proxectos para crear, actualizar e eliminar tarefas do proxecto, atribucións de recursos, dependencias de tarefas, depósitos de proxectos e membros dos equipos do proxecto. Non obstante, cando as operacións de creación, actualización ou eliminación se executan mediante programación en entidades de estrutura de subdivisión do traballo (WBS), poden producirse erros. Para rastrexar estes erros e o historial de operacións, implementáronse dous novos rexistros administrativos: **Conxunto de operacións** e **Servizo de Programación de Proxectos (PSS)**. Para acceder a estes rexistros, vaia a **Configuración** \> **Integración de programación**.

A seguinte ilustración mostra o modelo de datos para os rexistros de programación de proxectos.

![Modelo de datos para os rexistros de programación de proxectos.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Rexistro de conxunto de operacións

O rexistro do conxunto de operacións fai un seguimento da execución dun conxunto de operacións que se usa para executar unha ou varias operacións de creación, actualización ou eliminación nun lote en proxectos, tarefas do proxecto, asignacións de recursos, dependencias de tarefas, depósitos de proxectos ou membros do equipo do proxecto. O campo **Operación en estado** campo mostra o estado xeral do conxunto de operacións. Os detalles da carga útil do conxunto de operacións recóllense nos rexistros de Detalles do conxunto de operacións relacionados.

### <a name="operation-set"></a>Conxunto de operacións

A táboa seguinte mostra os campos que están relacionados coa entidade **Conxunto de operacións**.

| Nome do esquema            | Descripción                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | A data/hora na que o conxunto de operacións se completou o fallou.                                                | CompletedOn            |
| msdyn_correlationid   | O valor de **correlationId** da solicitude.                                                                  | CorrelationId          |
| msdyn_description     | Descrición do conxunto de operacións.                                                                        | Descripción            |
| msdyn_executedon      | A data/hora na que se executou o rexistro.                                                                       | Data de execución            |
| msdyn_operationsetId  | O identificador único das instancias da entidade.                                                                   | OperationSet           |
| msdyn_Project         | O proxecto que está relacionado co conxunto de operacións.                                                            | Project                |
| msdyn_projectid       | O valor de **projectId** da solicitude.                                                                      | ProjectId (obsoleto) |
| msdyn_projectName     | Non aplicable.                                                                                              | Non aplicable         |
| msdyn_PSSErrorLog     | O identificador único do rexistro de erros do servizo de programación de proxectos que está asociado co conxunto de operacións. | Rexistro de erros de PSS          |
| msdyn_PSSErrorLogName | Non aplicable.                                                                                              | Non aplicable         |
| msdyn_status          | O estado do conxunto de operacións.                                                                             | Progresión                 |
| msdyn_statusName      | Non aplicable.                                                                                              | Non aplicable         |
| msdyn_useraadid       | ID de obxecto de Azure Active Directory (Azure AD) do usuario ao que pertence a solicitude.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalles do conxunto de operacións

A táboa seguinte mostra os campos que están relacionados coa entidade **Detalles do conxunto de operacións**.

| Nome do esquema                 | Descripción                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Os campos de Dataverse serializados para a solicitude.                                            | CdsPayload            |
| msdyn_entityname           | Nome da entidade para a solicitude.                                                     | EntityName            |
| msdyn_httpverb             | O método da solicitude.                                                                         | HTTPVerb (obsoleto) |
| msdyn_httpverbName         | Non aplicable.                                                                             | Non aplicable        |
| msdyn_operationset         | O identificador único do conxunto de operacións ao que pertence este rexistro.                      | OperationSet          |
| msdyn_operationsetdetailId | O identificador único das instancias da entidade.                                                  | Detalle de OperationSet   |
| msdyn_operationsetName     | Non aplicable.                                                                             | Non aplicable        |
| msdyn_operationtype        | O tipo de operación do detalle do conxunto de operacións.                                             | OperationType         |
| msdyn_operationtypeName    | Non aplicable.                                                                             | Non aplicable        |
| msdyn_psspayload           | Os campos serializados do servizo de programación de proxectos para a solicitude.                           | PssPayload            |
| msdyn_recordid             | O identificador do rexistro da solicitude.                                                       | ID de rexistro             |
| msdyn_requestnumber        | Un número xerado automaticamente que identifica a orde na que se recibiron as solicitudes. | Número de solicitude        |

## <a name="project-scheduling-service-error-logs"></a>Rexistros de erros do servizo de programación de proxectos

Os rexistros de erros do servizo de programación de proxectos capturan os fallos que se producen cando o servizo de programación de proxectos tenta a operación **Gardar** ou **Abrir**. Hai tres escenarios compatibles nos que se xeran estes rexistros:

- As accións iniciadas polo usuario fallan gravemente (por exemplo, non se pode crear unha tarefa por falta de privilexios).
- O servizo de programación de proxectos non pode crear, actualizar, eliminar nin realizar ningunha outra operación en cascada nunha entidade mediante programación.
- O usuario experimenta erros cando un rexistro non se abre (por exemplo, cando se abre un proxecto ou se actualiza a información dun membro do equipo).

### <a name="project-scheduling-service-log"></a>Rexistro do servizo de programación de proxectos

A táboa seguinte mostra os campos que se inclúen no rexistro do servizo de programación de proxectos.

| Nome do esquema          | Descripción                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Montón de chamadas da excepción.                                               | Montón de chamadas     |
| msdyn_correlationid | O ID de correlación do erro.                                               | CorrelationId  |
| msdyn_errorcode     | Un campo que se usa para almacenar o código de erro Dataverse ou o código de erro HTTP. | Código de erro     |
| msdyn_HelpLink      | Unha ligazón á documentación de axuda.                                       | Ligazón de axuda      |
| msdyn_log           | O rexistro do servizo de programación de proxectos.                                   | Rexistro            |
| msdyn_project       | O proxecto que está asociado ao rexistro de erros.                             | Project        |
| msdyn_projectName   | O nome do proxecto manterase se a carga útil do conxunto de operacións persiste. | Non aplicable |
| msdyn_psserrorlogId | O identificador único das instancias da entidade.                                     | Rexistro de erros de PSS  |
| msdyn_SessionId     | O ID de sesión do proxecto.                                                        | ID de sesión     |

## <a name="error-log-cleanup"></a>Limpeza do rexistro de erros

Por defecto, tanto os rexistros de erros do servizo de programación de proxectos como o rexistro de conxunto de operacións pódense limpar cada 90 días. Eliminaranse os rexistros de erros con máis de 90 días. Non obstante, cambiando o valor do campo **msdyn_StateOperationSetAge** na páxina **Parámetros do proxecto**, os administradores poden axustar o intervalo de limpeza para que estea entre 1 e 120 días. Existen varios métodos para cambiar este valor:

- Personalice a entidade **Parámetro do proxecto** creando unha páxina personalizada e engadindo o campo **Antigüidade dos conxuntos de operacións obsoletos**.
- Use o código de cliente que use o [Kit de desenvolvemento de software WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Usa o código do SDK de servizo que utiliza o método SDK Xrm **updateRecord** (referencia de API de cliente) en aplicacións baseadas en modelos. Power Apps inclúe unha descrición e os parámetros admitidos para o método **updateRecord**.

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
