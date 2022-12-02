---
title: Usar as API de programación de proxectos con Power Automate
description: Este artigo ofrece un fluxo de mostra que utiliza as interfaces de programación de aplicacións (API) de programación de proxectos.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404454"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Usar as API de programación de proxectos con Power Automate

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Este artigo describe un fluxo de mostra que mostra como crear un plan de proxecto completo mediante o uso de Microsoft Power Automate, como crear un conxunto de operacións e como actualizar unha entidade. O exemplo mostra como crear un proxecto, un membro do equipo do proxecto, conxuntos de operacións, tarefas do proxecto e atribucións de recursos. Este artigo tamén explica como actualizar unha entidade e executar un conxunto de operacións.

A seguinte é unha lista completa dos pasos que se documentan no fluxo de mostra deste artigo:

1. [Crear un desencadeador de PowerApps](#1)
2. [Crear un proxecto](#2)
3. [Inicializar unha variable para o membro do equipo](#3)
4. [Crear un membro xenérico do equipo](#4)
5. [Crear un conxunto de opcións](#5)
6. [Crear unha depósito de proxecto](#6)
7. [Inicializar unha variable para o estado de ligazón](#7)
8. [Inicializar unha variable para o número de tarefas](#8)
9. [Inicializar unha variable para o ID de tarefas de proxecto](#9)
10. [Facer ata](#10)
11. [Establecer unha tarefa de proxecto](#11)
12. [Crear unha tarefa de proxecto](#12)
13. [Crear unha atribución de recursos](#13)
14. [Reducir unha variable](#14)
15. [Cambiar o nome dunha tarefa de proxecto.](#15)
16. [Executar un conxunto de opcións](#16)

## <a name="assumptions"></a>Suposicións

Este artigo asume que vostede ten un coñecemento básico da plataforma Dataverse, fluxos de nube e a interface de programación de aplicacións (API) de programación de proxectos. Para obter máis información, consulte a sección [Referencias](#references) máis adiante neste artigo.

## <a name="create-a-flow"></a>Crear un fluxo

### <a name="select-an-environment"></a>Seleccionar un ambiente

Pode crear o fluxo de Power Automate no seu ambiente.

1. Vaia a <https://flow.microsoft.com> e utilice as súas credenciais de administrador para iniciar sesión.
2. Na esquina superior dereita, seleccione **Ambientes**.
3. Na lista, seleccione o ambiente onde Dynamics 365 Project Operations está instalado.

### <a name="create-a-solution"></a>Crear unha solución

Siga estes pasos para crear un [fluxo baseado en solucións](/power-automate/overview-solution-flows). Ao crear un fluxo baseado en solucións, pode exportar máis facilmente o fluxo para utilizalo máis tarde.

1. No panel de navegación, seleccione **Solucións**.
2. Na páxina **Solucións**, seleccione **Nova solución**.
3. Na caixa de diálogo **Nova solución**, axuste os campos necesarios e seleccione **Crear**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Paso 1: Crear un desencadeador de PowerApps

1. Na páxina **Solucións**, seleccione a solución que creou e logo seleccione **Nova**.
2. No panel esquerdo, seleccione **Fluxos de nube** \> **Automatización** \> **Fluxo de nube** \> **Instantánea**.
3. No campo **Nome do fluxo**, introduza **Programar o fluxo de demostración da API**.
4. Na lista **Escoller como desencadear este fluxo**, seleccione **Power Apps**. Cando crea un desencadeador de Power Apps, a lóxica depende de vostede como autor. Neste artigo, deixe os parámetros de entrada en branco para fins de proba.
5. Seleccione **Crear**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Paso 2: Crear un proxecto

Siga estes pasos para crear un proxecto de mostra.

1. No fluxo que creou, seleccione **Novo paso**.

    ![Engadir un novo paso.](media/newstep.png)

2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **Executar unha acción desvinculada**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.

    ![Selección dunha operación.](media/chooseactiontab.png)

3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.

![Cambiar de nome un paso.](media/renamestep.png)

4. Cambie o nome do paso **Crear Proxecto**.
5. No campo **Nome da acción**, seleccione **msdyn\_CrearProxectoV1**.
6. No campo **msdyn\_subject**, seleccione **Engadir contido dinámico**.
7. No separador **Expresión**, no campo de función, introduza **Nome do proxecto - utcNow()**.
8. Seleccione **Aceptar**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Paso 3: Inicializar unha variable para o membro do equipo

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **inicializar variable**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Inicializar membro do equipo**.
5. No campo **Nome**, insira **TeamMemberAction**.
6. No campo **Tipo**, seleccione **Cadea**.
7. No campo **Valor**, introduza **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Paso 4: Crear un membro xenérico do equipo

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **Executar unha acción desvinculada**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Crear membro do equipo**.
5. Para o campo **Nome da acción**, seleccione **TeamMemberAction** na caixa de diálogo **Contido dinámico**.
6. No campo **Parámetros de acción**, introduza a seguinte información do parámetro.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Aquí ten unha explicación dos parámetros:

    - **\@\@odata.type** – O nome da entidade. Por exemplo, introduza **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – A clave principal do ID do equipo do proxecto. O valor é unha expresión do identificador único global (GUID).   O ID xérase a partir do separador de expresión.

    - **msdyn\_project\@odata.bind** – O ID de proxecto do proxecto propietario. O valor será o contido dinámico que proceda da resposta do paso "Crear proxecto". Asegúrese de introducir o camiño completo e engadir contido dinámico entre os parénteses. Son necesarias as comiñas. Por exemplo, introduza **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – O nome do membro do equipo. Por exemplo, introduza **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Paso 5: Crear un conxunto de operacións

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **Executar unha acción desvinculada**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Crear conxunto de operacións**.
5. No campo **Nome da acción**, seleccione a acción personalizada **msdyn\_CreateOperationSetV1** Dataverse.
6. No campo **Descrición**, insira **ScheduleAPIDemoOperationSet**.
7. No campo **Proxecto**, introduza **/msdyn\_projects(**.
8. Na caixa de diálogo **Contido dinámico**, seleccione **msdyn\_CreateProjectV1Response ProjectId**.
9. No campo **Proxecto**, introduza **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Paso 6: Crear un depósito de proxecto

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **engadir nova fila**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Crear depósito**.
5. No campo **Nome de táboa**, seleccione **Depósitos de proxecto**.
6. No campo **Nome**, insira **ScheduleAPIDemoBucket1**.
7. Para o campo **Proxecto**, seleccione **msdyn\_CreateProjectV1Response ProjectId** na caixa de diálogo **Contido dinámico**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Paso 7: Inicializar unha variable para o estado de ligazón

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **inicializar variable**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Init linkstatus**.
5. No campo **Nome**, insira **linkstatus**.
6. No campo **Tipo**, seleccione **Número enteiro**.
7. No campo **Valor**, introduza **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Paso 8: Inicializar unha variable para o número de tarefas

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **inicializar variable**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Iniciar número de tarefas**.
5. No campo **Nome**, insira **número de tarefas**.
6. No campo **Tipo**, seleccione **Número enteiro**.
7. No campo **Valor**, introduza **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Paso 9: Inicializar unha variable para o ID de tarefas de proxecto

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **inicializar variable**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Init ProjectTaskID**.
5. No campo **Nome**, insira **número de tarefas**.
6. No campo **Tipo**, seleccione **Cadea**.
7. Para o campo **Valor**, introduza **guid()** no xerador de expresións.

## <a name="step-10-do-until"></a><a id="10"></a>Paso 10: Facer ata

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **facer ata**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. Estableza o primeiro valor da instrución condicional á variable **número de tarefas** desde a caixa de diálogo **Contido dinámico**.
4. Estableza a condición en **menor que igual a**.
5. Estableza o segundo valor da declaración condicional en **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Paso 11: Establecer unha tarefa de proxecto

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **establecer variable**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Establecer tarefa de proxecto**.
5. No campo **Nome da acción**, seleccione **msdyn\_projecttaskid**.
6. Para o campo **Valor**, introduza **guid()** no xerador de expresións.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Paso 12: Crear unha tarefa de proxecto

Siga estes pasos para crear unha tarefa do proxecto que teña un ID único que pertenza ao proxecto actual e ao depósito do proxecto que creou.

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **Executar unha acción desvinculada**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Crear tarefa de proxecto**.
5. No campo **Nome da acción**, seleccione **msdyn\_PssCreateV1**.
6. No campo **Entidade**, introduza a seguinte información do parámetro.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Aquí ten unha explicación dos parámetros:

    - **\@\@odata.type** – O nome da entidade. Por exemplo, introduza **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – O ID único da tarefa. O valor debe establecerse nunha variable dinámica de **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – O ID de proxecto do proxecto propietario. O valor será o contido dinámico que proceda da resposta do paso "Crear proxecto". Asegúrese de introducir o camiño completo e engadir contido dinámico entre os parénteses. Son necesarias as comiñas. Por exemplo, introduza **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_tema** - Calquera nome da tarefa.
    - **msdyn\_projectbucket\@odata.bind** – O depósito do proxecto que contén as tarefas. O valor será o contido dinámico que proceda da resposta do paso "Crear depósito". Asegúrese de introducir o camiño completo e engadir contido dinámico entre os parénteses. Son necesarias as comiñas. Por exemplo, introduza **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Contido dinámico para a data de inicio. Por exemplo, mañá estará representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – A data de inicio programada Por exemplo, mañá estará representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Data de finalización programada. Seleccione unha data no futuro. Por exemplo, especifique **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – O estado da ligazón. Por exemplo, introduza **"192350000"**.

7. Para o campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Contido dinámico**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Paso 13: Crear unha atribución de recursos

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **Executar unha acción desvinculada**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Crear atribución**.
5. No campo **Nome da acción**, seleccione **msdyn\_PssCreateV1**.
6. No campo **Entidade**, introduza a seguinte información do parámetro.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Para o campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Contido dinámico**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Paso 14: Reducir unha variable

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **reducir variable**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No campo **Nome**, seleccione **número de tarefas**.
4. No campo **Valor**, introduza **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Paso 15: Cambiar de nome unha tarefa de proxecto

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **Executar unha acción desvinculada**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Cambiar nome de tarefa de proxecto**.
5. No campo **Nome da acción**, seleccione **msdyn\_PssUpdateV1**.
6. No campo **Entidade**, introduza a seguinte información do parámetro.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Para o campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Contido dinámico**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Paso 16: Executar un conxunto de operacións

1. No fluxo, seleccione **Novo paso**.
2. Na caixa de diálogo **Escoller unha operación**, no campo de busca, introduza **Executar unha acción desvinculada**. Despois, no separador **Accións**, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**), e logo seleccione **Cambiar nome**.
4. Cambie o nome do paso **Executar conxunto de operacións**.
5. No campo **Nome da acción**, seleccione **msdyn\_ExecuteOperationSetV1**.
6. Para o campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response OperationSetId** na caixa de diálogo **Contido dinámico**.

## <a name="references"></a>Referencias

- [Visión xeral de como integrar fluxos con Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Use as API de programación de proxectos para realizar operacións con entidades de programación](schedule-api-preview.md)
- [Visión xeral dos fluxos de nube - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Visión xeral dos fluxos baseados en solucións - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
