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

Este artigo describe un fluxo de mostra que mostra como crear un plan de proxecto completo mediante o uso Microsoft Power Automate, como crear un conxunto de operacións e como actualizar unha entidade. O exemplo mostra como crear un proxecto, un membro do equipo do proxecto, conxuntos de operacións, tarefas do proxecto e asignacións de recursos. Este artigo tamén explica como actualizar unha entidade e executar un conxunto de operacións.

A seguinte é unha lista completa dos pasos que se documentan no fluxo de mostra deste artigo:

1. [Crear un PowerApps disparador](#1)
2. [Crear un proxecto](#2)
3. [Inicializa unha variable para o membro do equipo](#3)
4. [Crea un membro xenérico do equipo](#4)
5. [Crear un conxunto de operacións](#5)
6. [Crear un depósito de proxecto](#6)
7. [Inicializa unha variable para o estado da ligazón](#7)
8. [Inicializa unha variable para o número de tarefas](#8)
9. [Inicialice unha variable para o ID da tarefa do proxecto](#9)
10. [Fai ata](#10)
11. [Establecer unha tarefa do proxecto](#11)
12. [Crear unha tarefa do proxecto](#12)
13. [Crear unha asignación de recursos](#13)
14. [Disminución dunha variable](#14)
15. [Cambiar o nome dunha tarefa do proxecto](#15)
16. [Executar un conxunto de operacións](#16)

## <a name="assumptions"></a>Suposicións

Este artigo asume que tes un coñecemento básico do Dataverse plataforma, fluxos de nube e a interface de programación de aplicacións (API) de programación de proxectos. Para obter máis información, consulte o [Referencias](#references) sección máis adiante neste artigo.

## <a name="create-a-flow"></a>Crear un fluxo

### <a name="select-an-environment"></a>Seleccionar un ambiente

Podes crear o Power Automate fluír no seu entorno.

1. Ir a<https://flow.microsoft.com>, e use as súas credenciais de administrador para iniciar sesión.
2. Na esquina superior dereita, selecciona **Ambientes**.
3. Na lista, seleccione o ambiente onde Dynamics 365 Project Operations está instalado.

### <a name="create-a-solution"></a>Crear unha solución

Siga estes pasos para crear un [fluxo consciente da solución](/power-automate/overview-solution-flows). Ao crear un fluxo consciente da solución, pode exportar máis facilmente o fluxo para utilizalo máis tarde.

1. No panel de navegación, seleccione **Solucións**.
2. No **Solucións** páxina, seleccione **Nova solución**.
3. No **Nova solución** caixa de diálogo, configure os campos necesarios e, a continuación, seleccione **Crear**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Paso 1: Crear un PowerApps disparador

1. No **Solucións** páxina, seleccione a solución que creou e, a continuación, seleccione **Novo**.
2. No panel esquerdo, seleccione **Fluxos de nubes** \> **Automatización** \> **Fluxo de nubes** \> **Instantánea**.
3. No **Nome do fluxo** campo, ingrese **Programar o fluxo de demostración da API**.
4. No **Escolle como activar este fluxo** lista, seleccione **Power Apps**. Cando creas un Power Apps disparador, a lóxica depende de ti como autor. Neste artigo, deixe os parámetros de entrada en branco para fins de proba.
5. Seleccione **Crear**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Paso 2: Crear un proxecto

Siga estes pasos para crear un proxecto de mostra.

1. No fluxo que creaches, selecciona **Novo paso**.

    ![Engadindo un novo paso.](media/newstep.png)

2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **realizar accións non vinculadas**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.

    ![Selección dunha operación.](media/chooseactiontab.png)

3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.

![Cambiar o nome dun paso.](media/renamestep.png)

4. Cambia o nome do paso **Crear Proxecto**.
5. No **Nome da acción** campo, seleccione **msdyn\_ CrearProxectoV1**.
6. Baixo a **msdyn\_ tema** campo, seleccione **Engade contido dinámico**.
7. No **Expresión** pestana, no campo de función, introduza **Nome do proxecto - utcNow()**.
8. Seleccione **Aceptar**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Paso 3: inicializa unha variable para o membro do equipo

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **inicializar a variable**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Membro do equipo de inicio**.
5. No **Nome** campo, ingrese **TeamMemberAction**.
6. No **Tipo** campo, seleccione **Corda**.
7. No **Valor** campo, ingrese **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Paso 4: crea un membro xenérico do equipo

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **realizar accións non vinculadas**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Crear membro do equipo**.
5. Para o **Nome da acción** campo, seleccione **TeamMemberAction** no **Contido dinámico** caixa de diálogo.
6. No **Parámetros de acción** campo, introduza a seguinte información do parámetro.

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

    Aquí tes unha explicación dos parámetros:

    - **\@\@ odata.type** - O nome da entidade. Por exemplo, introduza **"Microsoft.Dynamics.CRM.msdyn\_ equipo do proxecto"**.
    - **msdyn\_ projectteamid** – A clave principal do ID do equipo do proxecto. O valor é unha expresión de identificador único global (GUID).   O ID xérase a partir da pestana Expresión.

    - **msdyn\_ proxecto\@ odata.bind** – O ID do proxecto propietario. O valor será o contido dinámico que proceda da resposta do paso "Crear proxecto". Asegúrate de introducir o camiño completo e engadir contido dinámico entre os parénteses. Son necesarias as comiñas. Por exemplo, introduza **"/msdyn\_ proxectos (ENGADIR CONTIDO DINÁMICO)"**.
    - **msdyn\_ nome** – O nome do membro do equipo. Por exemplo, introduza **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Paso 5: crear un conxunto de operacións

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **realizar accións non vinculadas**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Crear conxunto de operacións**.
5. No **Nome da acción** campo, seleccione o **msdyn\_ CreateOperationSetV1** Dataverse acción personalizada.
6. No **Descrición** campo, ingrese **ScheduleAPIDemoOperationSet**.
7. No **Proxecto** campo, ingrese **/msdyn\_ proxectos (**.
8. No **Contido dinámico** caixa de diálogo, seleccione **msdyn\_ CreateProjectV1Response ProjectId**.
9. No **Proxecto** campo, ingrese **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Paso 6: crea un depósito de proxecto

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **engadir unha nova fila**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Crear cubo**.
5. No **Nome da táboa** campo, seleccione **Cubos do proxecto**.
6. No **Nome** campo, ingrese **ScheduleAPIDemoBucket1**.
7. Para o **Proxecto** campo, seleccione **msdyn\_ CreateProjectV1Response ProjectId** no **Contido dinámico** caixa de diálogo.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Paso 7: inicializa unha variable para o estado da ligazón

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **inicializar a variable**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Iniciar o estado da ligazón**.
5. No **Nome** campo, ingrese **estado da ligazón**.
6. No **Tipo** campo, seleccione **Número enteiro**.
7. No **Valor** campo, ingrese **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Paso 8: inicializa unha variable para o número de tarefas

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **inicializar a variable**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Init Número de tarefas**.
5. No **Nome** campo, ingrese **número de tarefas**.
6. No **Tipo** campo, seleccione **Número enteiro**.
7. No **Valor** campo, ingrese **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Paso 9: inicializa unha variable para o ID da tarefa do proxecto

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **inicializar a variable**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Iniciar ProjectTaskID**.
5. No **Nome** campo, ingrese **número de tarefas**.
6. No **Tipo** campo, seleccione **Corda**.
7. Para o **Valor** campo, ingrese **guid()** no constructor de expresións.

## <a name="step-10-do-until"></a><a id="10"></a> Paso 10: Fai ata

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **facer ata**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. Establece o primeiro valor da instrución condicional a **número de tarefas** variable desde o **Contido dinámico** caixa de diálogo.
4. Establece a condición en **menor que igual a**.
5. Establece o segundo valor da instrución condicional en **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Paso 11: Establece unha tarefa do proxecto

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **establecer variable**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No novo paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Establecer tarefa do proxecto**.
5. No **Nome** campo, seleccione **msdyn\_ projecttaskid**.
6. Para o **Valor** campo, ingrese **guid()** no constructor de expresións.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Paso 12: crea unha tarefa do proxecto

Siga estes pasos para crear unha tarefa do proxecto que teña un ID único que pertenza ao proxecto actual e ao depósito do proxecto que creou.

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **realizar accións non vinculadas**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Crear tarefa do proxecto**.
5. No **Nome da acción** campo, seleccione **msdyn\_ PssCreateV1**.
6. No **Entidade** campo, introduza a seguinte información do parámetro.

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

    Aquí tes unha explicación dos parámetros:

    - **\@\@ odata.type** - O nome da entidade. Por exemplo, introduza **"Microsoft.Dynamics.CRM.msdyn\_ tarefa do proxecto"**.
    - **msdyn\_ projecttaskid** – O ID único da tarefa. O valor debe establecerse nunha variable dinámica de **msdyn\_ projecttaskid**.
    - **msdyn\_ proxecto\@ odata.bind** – O ID do proxecto propietario. O valor será o contido dinámico que proceda da resposta do paso "Crear proxecto". Asegúrate de introducir o camiño completo e engadir contido dinámico entre os parénteses. Son necesarias as comiñas. Por exemplo, introduza **"/msdyn\_ proxectos (ENGADIR CONTIDO DINÁMICO)"**.
    - **msdyn\_ tema** - Calquera nome da tarefa.
    - **msdyn\_ projectbucket\@ odata.bind** – O depósito do proxecto que contén as tarefas. O valor será o contido dinámico que procede da resposta do paso "Crear depósito". Asegúrate de introducir o camiño completo e engadir contido dinámico entre os parénteses. Son necesarias as comiñas. Por exemplo, introduza **"/msdyn\_ projectbuckets(ENGADIR CONTIDO DINÁMICO)"**.
    - **msdyn\_ comezar** – Contido dinámico para a data de inicio. Por exemplo, mañá estará representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_ inicio programado** - Data de inicio prevista. Por exemplo, mañá estará representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_ axenda** - Data de finalización prevista. Seleccione unha data no futuro. Por exemplo, especifique **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** - O estado da ligazón. Por exemplo, introduza **"192350000"**.

7. Para o **OperationSetId** campo, seleccione **msdyn\_ CreateOperationSetV1Response** no **Contido dinámico** caixa de diálogo.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Paso 13: crea unha asignación de recursos

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **realizar accións non vinculadas**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Crear tarefa**.
5. No **Nome da acción** campo, seleccione **msdyn\_ PssCreateV1**.
6. No **Entidade** campo, introduza a seguinte información do parámetro.

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

7. Para o **OperationSetId** campo, seleccione **msdyn\_ CreateOperationSetV1Response** no **Contido dinámico** caixa de diálogo.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Paso 14: Disminución dunha variable

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **variable de decremento**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No **Nome** campo, seleccione **número de tarefas**.
4. No **Valor** campo, ingrese **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Paso 15: renomear unha tarefa do proxecto

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **realizar accións non vinculadas**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Cambiar o nome da tarefa do proxecto**.
5. No **Nome da acción** campo, seleccione **msdyn\_ PssUpdateV1**.
6. No **Entidade** campo, introduza a seguinte información do parámetro.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Para o **OperationSetId** campo, seleccione **msdyn\_ CreateOperationSetV1Response** no **Contido dinámico** caixa de diálogo.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Paso 16: executa un conxunto de operacións

1. No fluxo, seleccione **Novo paso**.
2. No **Escolle unha operación** caixa de diálogo, no campo de busca, introduza **realizar accións non vinculadas**. Despois, no **Accións** ficha, seleccione a operación na lista de resultados.
3. No paso, seleccione os puntos suspensivos (**...**) e, a continuación, seleccione **Cambiar o nome**.
4. Cambia o nome do paso **Executar conxunto de operacións**.
5. No **Nome da acción** campo, seleccione **msdyn\_ ExecuteOperationSetV1**.
6. Para o **OperationSetId** campo, seleccione **msdyn\_ CreateOperationSetV1Response OperationSetId** no **Contido dinámico** caixa de diálogo.

## <a name="references"></a>Referencias

- [Visión xeral de como integrar fluxos con Dataverse -Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Use as API de programación de proxectos para realizar operacións con entidades de programación](schedule-api-preview.md)
- [Visión xeral dos fluxos da nube -Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Visión xeral dos fluxos conscientes da solución -Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
