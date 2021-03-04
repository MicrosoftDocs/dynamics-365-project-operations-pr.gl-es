---
title: Planifique o seu traballo en Microsoft Project co complemento Project Service
description: Este tema fornece información sobre como usar o complemento Microsoft Project para Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145941"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planifique o seu traballo en Microsoft Project co complemento Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] facilita a planificación de proxectos, incluíndo estimacións. Pode definir o traballo de forma que os custos, esforzo e o valor de vendas estea limpo cando se envía a proposta final.  

Pode instalar [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] e realizar as tarefas de planificación no ambiente coñecido de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilice as sólidas capacidades de planificación e xestión de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e despois actualice o seu plan de proxecto en Project Service Automation.  

> [!IMPORTANT]
> - Para utilizar a funcionalidade de xestión de documentos de SharePoint en para almacenar os seus ficheiros de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para proxectos de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o seu administrador de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] terá que activar a xestión de documentos. 
> - O [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] só é compatible con [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Descargar e instalar o complemento  
 Teña a información de inicio de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] preparada. Necesitará esta información para conectarse desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Desde o centro de descargas, descargue o complemento para a súa versión admitida de Project Service [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ou [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Seleccione ligazón de descarga.  

3.  Cando conclúa a descarga, seleccione **Si** para instalar o complemento.  

## <a name="configure-the-add-in"></a>Configurar o complemento  

1. Abra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e seleccione o separador **Project Service**.  

2. Seleccione **Conectar**.  

3. Introduza a información de inicio de sesión e seleccione **Iniciar sesión**.  

   Agora pode empezar a usar o suplemento.  

## <a name="read-from-a-template"></a>Ler a partir dun modelo  
 Lea desde un modelo creado en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copiado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para iniciar a a planificación do proxecto. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crear un modelo de proxecto (Project Service Automation)](../psa/create-project-template.md)  

1.  No separador **Project Service**, seleccione **Ler** > **Modelo de proxecto de Project Service Automation**.  

2.  Elixa un modelo de proxecto da lista e, a seguir, seleccione **Abrir**.  

    > [!NOTE]
    >  Por defecto, as tarefas que se copian desde o modelo en Project están definidas como programadas manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Atribuír roles de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a recursos de proxecto  

1.  Abra un proxecto e seleccione a fita **Tarefa**.  

2. Seleccione o menú **Gráfica de Gantt** e, a seguir, escolla **Folla de Recursos**.  

3. Na Folla de Recursos, seleccione o menú despregable **Rol de recurso de Project Service** e escolla un rol de Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Déalle recursos a seu proxecto  

1.  No separador Project Service, seleccione unha fila e seleccione **Localizar Recursos**.  

2.  Na pantalla **Reservar recurso**, seleccione o recurso que desexa utilizar para o proxecto.  

3.  Seleccione **Reservar** e, a seguir, seleccione **Aceptar**.  

## <a name="publish-your-project"></a>Publicar o proxecto  
Cando a planificación do proxecto estea concluída, o seguinte paso é importar e publicar o proxecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

O proxecto importarase en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Aplícase o proceso de xeración de prezos e equipo. Abra o proxecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para ver que o equipo, as estimacións do proxecto e estrutura de subdivisión do traballo xa se xeraron. A táboa seguinte mostra onde buscar os resultados.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gráfica Gantt**   | Impórtase na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pantalla **Estrutura de subdivisión do traballo**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Folla de recursos** |   Importacións na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pantalla **Membros do Equipo de proxecto**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Utilización de uso**    |    Impórtase na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pantalla **Estimacións de Proxecto**.     |

**Para importar e publicar o seu proxecto**  
1. No separador **Project Service**, vaia a **Publicar** > **Novo proxecto de Project Service Automation**.  

2. Na caixa de diálogo **Publicar nun novo proxecto en Project Service**, introduza o **Nome do proxecto** e seleccione o **Cliente**.  

3. Tamén pode seleccionar **Ligar o plan do proxecto a Project Service Automation** para ligar o ficheiro do plan do proxecto a Project Service Automation.  

4. Seleccione **Publicar**.  

   Ligar o ficheiro do Proxecto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] converte o ficheiro do proxecto en principal e define a estrutura de subdivisión do traballo en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a só de lectura.  Para modificar a planificación do proxecto é necesario facelas en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicalas como actualizacións en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar un proxecto que se importou  
 Para modificar un plan de proxecto que se importou a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ten dúas opcións:  

- Abra o ficheiro principal e edíteo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desligar o ficheiro principal e editalo directamente en Project Service. Por defecto, un proxecto que se cargou desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] está bloqueado e só se pode editar en Project. Para editar o ficheiro en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o ficheiro ten que estar desligado.  

### <a name="edit-in-pn_microsoft_project"></a>Editar en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. No menú principal, vaia a **Project Service** > **Proxectos**.  

2. Na lista de proxectos, abra o que creou en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleccione **Abrir en MS Project** na fita. Abrirase o ficheiro principal ligado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desligar un ficheiro e editalo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. No menú principal, vaia a **Project Service** > **Proxectos**.  

2. Na lista de proxectos, abra o que creou en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleccione **Desligar de MS Project** na fita.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Cargar un ficheiro de proxecto a SharePoint ou Grupos de Office  
 Pode cargar o ficheiro de proxecto en SharePoint e localizalo nos Documentos Asociados para o seu proxecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Cómpre que o seu administrador configure a xestión de documentos de SharePoint e que o active para a entidade de proxecto. 

 Pode tamén cargar o ficheiro de Project file en [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se ten Grupos de Office configurados.

### <a name="upload-a-file-for-sharepoint"></a>Cargar un ficheiro para SharePoint  

1. No menú principal, vaia a **Project Service** > **Cargar**.  

2. Seleccione **Documentos de proxecto Project Service Automation**.  

3. Na caixa de diálogo **Activar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Si** ou **Non**.  

   - Se selecciona **Si**, poderá seleccionar o botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation e iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e cargar o ficheiro de proxecto desde a biblioteca de documentos de SharePoint.  

   - Se selecciona **Non**, a ligazón para **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** non funcionará.  

4. O ficheiro de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode encontrarse en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], en **Documentos** para o proxecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

### <a name="upload-a-file-for-office-groups"></a>Cargar un ficheiro a Grupos de Office  

1. No menú principal, vaia a **Project Service** > **Cargar**.  

2. Seleccione **Documentos de proxecto Project Service Automation**.  

3. Na caixa de diálogo **Activar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Si** ou **Non**.  

   - Se selecciona **Si**, poderá seleccionar o botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation e iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e cargar o ficheiro de proxecto desde a biblioteca de documentos de SharePoint.  

   - Se selecciona **Non**, a ligazón para **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** non funcionará.  

4. O ficheiro de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode encontrarse en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], en **Documentos** para o proxecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

## <a name="publish--your-project-as-a-template"></a>Publicar o proxecto como modelo  
 Pode gardar o seu proxecto e reutilizalo se o garda como modelo de proxecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Os modelos de proxecto son plans de proxecto reutilizables en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Para obter máis información, consulte [Crear un modelo de proxecto (Project Service Automation)](../psa/create-project-template.md). 

1. No separador **Project Service**, vaia a **Publicar** > **Novo modelo de proxecto de Project Service Automation**.  

2. Na caixa de diálogo **Publicar nun novo modelo de proxecto en Project Service**, introduza o **Nome do modelo de proxecto**.  

3. Tamén pode seleccionar **Ligar o plan do proxecto a Project Service Automation** para ligar o ficheiro do proxecto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Seleccione **Publicar**.  

Ligar o ficheiro do Proxecto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] converte o ficheiro do proxecto en principal e define a estrutura de subdivisión do traballo no modelo de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a só de lectura.  Para modificar a planificación do proxecto é necesario facelas en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicalas como actualizacións en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Ler unha programación cargada de recursos

Ao ler un proxecto desde Project Service Automation, o calendario do recurso non está sincronizado co cliente de escritorio. Se hai diferenzas na duración, esforzo ou fin da tarefa, é probablemente porque os recursos e o cliente de escritorio non teñen o mesmo calendario de modelo de horas de traballo aplicado ao proxecto.


## <a name="data-synchronization"></a>Sincronización de datos
As táboas desta sección proporcionan información sobre a sincronización de datos de entidade entre Project Service Automation e o complemento de escritorio Microsoft Project.

### <a name="project-task-entity-table"></a>Táboa de entidades de tarefa do proxecto
A seguinte táboa describe como se sincronizan os datos da entidade de tarefa de proxecto entre Project Service Automation e o complemento de escritorio Microsoft Project.

| **Entidade** | **Campo** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Tarefa do proxecto | Data de vencemento | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Esforzo estimado | Sincronizado | Non sincronizado |
| Tarefa do proxecto | ID do cliente de MS Project | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Tarefa primaria | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Project | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Tarefa do proxecto | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Nome da tarefa do proxecto | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Unidade de recursos (desfasado en v3.0) | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Duración programada | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Data de inicio | Sincronizado | Non sincronizado |
| Tarefa do proxecto | Identificador de WBS | Sincronizado | Non sincronizado |

### <a name="team-member-entity-table"></a>Táboa de entidades de membro do equipo
A seguinte táboa describe como se sincronizan os datos da entidade de membro do equipo entre Project Service Automation e o complemento de escritorio Microsoft Project.

| **Entidade** | **Campo** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Membro do equipo | ID do cliente de MS Project | Sincronizado | Non sincronizado |
| Membro do equipo | Nome da posición | Sincronizado | Non sincronizado |
| Membro do equipo | proxecto | Sincronizado | Sincronizado |
| Membro do equipo | Equipo do proxecto | Sincronizado | Sincronizado |
| Membro do equipo | Unidade de recursos | Non sincronizado | Sincronizado |
| Membro do equipo | Rol | Non sincronizado | Sincronizado |
| Membro do equipo | Horario laboral | Non sincronizado | Non sincronizado |

### <a name="resource-assignment-entity-table"></a>Táboa de entidades de atribución de recursos
A seguinte táboa describe como se sincronizan os datos da entidade de atribución de recursos entre Project Service Automation e o complemento de escritorio Microsoft Project.

| **Entidade** | **Campo** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Atribución do recurso | Data de inicio | Sincronizado | Non sincronizado |
| Atribución do recurso | horas | Sincronizado | Non sincronizado |
| Atribución do recurso | ID do cliente de MS Project | Sincronizado | Non sincronizado |
| Atribución do recurso | Traballo planificado | Sincronizado | Non sincronizado |
| Atribución do recurso | Project | Sincronizado | Non sincronizado |
| Atribución do recurso | Equipo do proxecto | Sincronizado | Non sincronizado |
| Atribución do recurso | Atribución do recurso | Sincronizado | Non sincronizado |
| Atribución do recurso | Tarefa | Sincronizado | Non sincronizado |
| Atribución do recurso | Até o presente | Sincronizado | Non sincronizado |

### <a name="project-task-dependencies-entity-table"></a>Táboa de entidades de dependencias da tarefa do proxecto
A seguinte táboa describe como se sincronizan os datos da entidade de dependencias da tarefa de proxecto entre Project Service Automation e o complemento de escritorio Microsoft Project.

| **Entidade** | **Campo** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Dependencias da tarefa do proxecto | Dependencia da tarefa do proxecto | Sincronizado | Non sincronizado |
| Dependencias da tarefa do proxecto | Tipo de ligazón | Sincronizado | Non sincronizado |
| Dependencias da tarefa do proxecto | Tarefa predecesora | Sincronizado | Non sincronizado |
| Dependencias da tarefa do proxecto | Project | Sincronizado | Non sincronizado |
| Dependencias da tarefa do proxecto | Tarefa sucesora | Sincronizado | Non sincronizado |

### <a name="additional-resources"></a>Recursos adicionais
 [Guía do xestor de proxectos](../psa/project-manager-guide.md)