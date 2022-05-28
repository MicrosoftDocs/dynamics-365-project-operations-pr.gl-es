---
title: Desenvolver modelos de proxecto con Copiar proxecto
description: Este tema ofrece información sobre como crear modelos de proxecto usando a acción personalizada Copiar proxecto.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590896"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolver modelos de proxecto con Copiar proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations admite a capacidade de copiar un proxecto e devolver as tarefas aos recursos xenéricos que representan o rol. Os clientes poden usar esta funcionalidade para crear modelos básicos de proxectos.

Cando selecciona **Copiar proxecto**, actualízase o estado do proxecto de destino. Use **Motivo para o estado** para determinar cando finaliza a acción de copia. Ao seleccionar **Copiar proxecto** tamén actualiza a data de inicio do proxecto á data de inicio actual se non se detecta ningunha data de destino na entidade de proxecto de destino.

## <a name="copy-project-custom-action"></a>Acción personalizada Copiar proxecto

### <a name="name"></a>Nome 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Parámetros de entrada

Hai tres parámetros de entrada:

- **SubstituírNamedResources** ou **ClearTeamsAndAssignments** – Establece só unha das opcións. Non configure os dous.

    - **\{"ReplaceNamedResources": verdadeiro\}** – O comportamento predeterminado para as operacións do proxecto. Calquera recurso nomeado substitúese por recursos xenéricos.
    - **\{"ClearTeamsAndAssignments":true\}** – O comportamento predeterminado para Project for the Web. Elimínanse todas as tarefas e membros do equipo.

- **Proxecto fonte** – A referencia da entidade do proxecto orixe do que se copiará. Este parámetro non pode ser nulo.
- **Obxectivo** – A referencia da entidade do proxecto de destino para copiar. Este parámetro non pode ser nulo.

A seguinte táboa ofrece un resumo dos tres parámetros.

| Parámetro                | Tipo             | Valor                 |
|--------------------------|------------------|-----------------------|
| SubstituírNamedResources    | Boolean          | **Verdade** ou **Falso** |
| ClearTeamsAndAssignments | Boolean          | **Verdade** ou **Falso** |
| SourceProject            | Referencia de entidade | O proxecto fonte    |
| Destino                   | Referencia de entidade | O proxecto obxectivo    |

Para obter máis valores predeterminados das accións, consulte [Usa accións da API web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validacións

Realízanse as seguintes validacións.

1. Null verifica e recupera os proxectos orixe e destino para confirmar a existencia de ambos os proxectos na organización.
2. O sistema valida que o proxecto de destino é válido para copiar verificando as seguintes condicións:

    - Non hai ningunha actividade previa no proxecto (incluída a selección do **Tarefas** pestana), e o proxecto é recén creado.
    - Non hai ningunha copia anterior, non se solicitou ningunha importación neste proxecto e o proxecto non ten un **Fallou** estado.

3. A operación non se chama usando HTTP.

## <a name="specify-fields-to-copy"></a>Especificar campos para copiar

Cando se chama a acción, **Copiar proxecto** verá a vista do proxecto **Copiar as columnas do proxecto** para determinar que campos se copian cando se copia o proxecto.

### <a name="example"></a>Exemplo

O seguinte exemplo mostra como chamar a **CopyProjectV3** acción personalizada co **removeNamedResources** conxunto de parámetros.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
