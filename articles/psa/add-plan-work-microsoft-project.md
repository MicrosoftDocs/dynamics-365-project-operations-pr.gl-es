---
title: Utilizar o complemento Project Service para planificar o traballo en Microsoft Project | MicrosoftDocs
description: Este tema fornece información sobre como engadir, configurar e usar o complemento Microsoft Project para Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129676"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="e2f58-103">Utilice o complemento de Project Service Automation para planificar o seu traballo en Project Microsoft</span><span class="sxs-lookup"><span data-stu-id="e2f58-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="e2f58-104">facilita a planificación de proxectos, incluíndo estimacións.</span><span class="sxs-lookup"><span data-stu-id="e2f58-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="e2f58-105">Pode definir o traballo de forma que os custos, esforzo e o valor de vendas estea limpo cando se envía a proposta final.</span><span class="sxs-lookup"><span data-stu-id="e2f58-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="e2f58-106">Agora pode instalar [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] e realizar as tarefas de planificación no ambiente coñecido de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="e2f58-107">Utilice as sólidas capacidades de planificación e xestión de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e despois actualice o seu plan de proxecto en Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e2f58-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="e2f58-108">Para utilizar a funcionalidade de xestión de documentos de SharePoint en para almacenar os seus ficheiros de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para proxectos de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o seu administrador de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] terá que activar a xestión de documentos.</span><span class="sxs-lookup"><span data-stu-id="e2f58-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="e2f58-109">O [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] só é compatible con [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="e2f58-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="e2f58-110">Descargar e instalar o complemento</span><span class="sxs-lookup"><span data-stu-id="e2f58-110">Download and install the add-in</span></span>  
 <span data-ttu-id="e2f58-111">Teña a información de inicio de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] preparada.</span><span class="sxs-lookup"><span data-stu-id="e2f58-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="e2f58-112">Necesitará esta información para conectarse desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="e2f58-113">Desde o centro de descargas, descargue o complemento para a súa versión admitida de Project Service [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ou [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="e2f58-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="e2f58-114">Prema na ligazón de descarga.</span><span class="sxs-lookup"><span data-stu-id="e2f58-114">Click the download link.</span></span>  

3.  <span data-ttu-id="e2f58-115">Cando conclúa a descarga, prema **Si** para instalar o complemento.</span><span class="sxs-lookup"><span data-stu-id="e2f58-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="e2f58-116">Configurar o complemento</span><span class="sxs-lookup"><span data-stu-id="e2f58-116">Configure the add-in</span></span>  

1. <span data-ttu-id="e2f58-117">Abra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e prema no separador **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="e2f58-118">Prema **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="e2f58-119">Introduza a información de inicio de sesión e prema en **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="e2f58-120">Agora pode empezar a usar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="e2f58-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="e2f58-121">Ler a partir dun modelo</span><span class="sxs-lookup"><span data-stu-id="e2f58-121">Read from a template</span></span>  
 <span data-ttu-id="e2f58-122">Lea desde un modelo creado en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copiado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para iniciar a a planificación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="e2f58-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e2f58-123">[Crear un modelo de proxecto (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="e2f58-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="e2f58-124">No separador **Project Service**, prema en **Ler** > **Modelo de proxecto de Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="e2f58-125">Elixa un modelo de proxecto da lista e, a seguir, prema en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="e2f58-126">Por defecto, as tarefas que se copian desde o modelo en Project están definidas como programadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="e2f58-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="e2f58-127">Atribuír roles de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a recursos de proxecto</span><span class="sxs-lookup"><span data-stu-id="e2f58-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="e2f58-128">Abra un proxecto e prema na fita **Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="e2f58-129">Prema no menú **Gráfica de Gantt** e, a seguir, escolla **Folla de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="e2f58-130">Na Folla de Recursos, prema o menú despregable **Rol de recurso de Project Service** e escolla un rol de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e2f58-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="e2f58-131">Déalle recursos a seu proxecto</span><span class="sxs-lookup"><span data-stu-id="e2f58-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="e2f58-132">No separador Project Service, seleccione unha fila e prema **Localizar Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="e2f58-133">Na pantalla **Reservar recurso**, seleccione o recurso que desexa utilizar para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="e2f58-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="e2f58-134">Prema **Reservar** e, a seguir, prema **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="e2f58-135">Publicar o proxecto</span><span class="sxs-lookup"><span data-stu-id="e2f58-135">Publish your project</span></span>  
<span data-ttu-id="e2f58-136">Cando a planificación do proxecto estea concluída, o seguinte paso é importar e publicar o proxecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="e2f58-137">O proxecto importarase en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="e2f58-138">Aplícase o proceso de xeración de prezos e equipo.</span><span class="sxs-lookup"><span data-stu-id="e2f58-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="e2f58-139">Abra o proxecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para ver que o equipo, estimación do proxecto e estrutura de subdivisión do traballo xa se xerou.</span><span class="sxs-lookup"><span data-stu-id="e2f58-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="e2f58-140">A táboa seguinte mostra onde buscar os resultados:</span><span class="sxs-lookup"><span data-stu-id="e2f58-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="e2f58-141">**Gráfica Gantt**</span><span class="sxs-lookup"><span data-stu-id="e2f58-141">**Gantt Chart**</span></span>   | <span data-ttu-id="e2f58-142">Impórtase na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pantalla **Estrutura de subdivisión do traballo**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="e2f58-143">**Folla de recursos**</span><span class="sxs-lookup"><span data-stu-id="e2f58-143">**Resource Sheet**</span></span> |   <span data-ttu-id="e2f58-144">Importacións na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pantalla **Membros do Equipo de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="e2f58-145">**Utilización de uso**</span><span class="sxs-lookup"><span data-stu-id="e2f58-145">**Use Usage**</span></span>    |    <span data-ttu-id="e2f58-146">Impórtase na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pantalla **Estimacións de Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="e2f58-147">**Para importar e publicar o seu proxecto**</span><span class="sxs-lookup"><span data-stu-id="e2f58-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="e2f58-148">No separador **Project Service**, prema en **Publicar** > **Novo proxecto de Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="e2f58-149">Na caixa de diálogo **Publicar nun novo proxecto en Project Service**, introduza o **Nome do proxecto** e seleccione o **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="e2f58-150">Tamén pode marcar **Ligar o plan do proxecto a Project Service Automation** para ligar o ficheiro do plan do proxecto a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e2f58-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="e2f58-151">Prema **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-151">Click **Publish**.</span></span>  

   <span data-ttu-id="e2f58-152">Ligar o ficheiro do Proxecto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] converte o ficheiro do proxecto en principal e define a estrutura de subdivisión do traballo en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a só de lectura.</span><span class="sxs-lookup"><span data-stu-id="e2f58-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="e2f58-153">Para modificar a planificación do proxecto é necesario facelas en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicalas como actualizacións en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="e2f58-154">Editar un proxecto que se importou</span><span class="sxs-lookup"><span data-stu-id="e2f58-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="e2f58-155">Para modificar un plan de proxecto que se importou a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ten dúas opcións:</span><span class="sxs-lookup"><span data-stu-id="e2f58-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="e2f58-156">Abra o ficheiro principal e edíteo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="e2f58-157">Desligar o ficheiro principal e editalo directamente en Project Service.</span><span class="sxs-lookup"><span data-stu-id="e2f58-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="e2f58-158">Por defecto, un proxecto que se cargou desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] está bloqueado e só se pode editar en Project.</span><span class="sxs-lookup"><span data-stu-id="e2f58-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="e2f58-159">Para editar o ficheiro en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o ficheiro ten que estar desligado.</span><span class="sxs-lookup"><span data-stu-id="e2f58-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="e2f58-160">Editar en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="e2f58-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="e2f58-161">No menú principal, prema en **Project Service** > **Proxectos**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="e2f58-162">Na lista de proxectos, abra o que creou en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="e2f58-163">Prema **Abrir en MS Project** na fita.</span><span class="sxs-lookup"><span data-stu-id="e2f58-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="e2f58-164">Abrirase o ficheiro principal ligado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="e2f58-165">Desligar un ficheiro e editalo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="e2f58-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="e2f58-166">No menú principal, prema en **Project Service** > **Proxectos**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="e2f58-167">Na lista de proxectos, abra o que creou en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="e2f58-168">Prema **Desligar de MS Project** na fita.</span><span class="sxs-lookup"><span data-stu-id="e2f58-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="e2f58-169">Cargar un ficheiro de proxecto a SharePoint ou Grupos de Office</span><span class="sxs-lookup"><span data-stu-id="e2f58-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="e2f58-170">Pode cargar o ficheiro de proxecto en SharePoint e localizalo nos Documentos Asociados para o seu proxecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="e2f58-171">Cómpre que o seu administrador configure a xestión de documentos de SharePoint e que o active para a entidade de proxecto.</span><span class="sxs-lookup"><span data-stu-id="e2f58-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="e2f58-172">Pode tamén cargar o ficheiro de Project file en [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se ten Grupos de Office configurados.</span><span class="sxs-lookup"><span data-stu-id="e2f58-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="e2f58-173">Cargar un ficheiro para SharePoint</span><span class="sxs-lookup"><span data-stu-id="e2f58-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="e2f58-174">No menú principal, prema en **Project Service** > **Cargar**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="e2f58-175">Seleccione **Documentos de proxecto Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="e2f58-176">Na caixa de diálogo **Activar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Si** ou **Non**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="e2f58-177">Se preme en **Si**, poderá seleccionar o botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation, iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e cargar o ficheiro de proxecto desde a biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e2f58-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="e2f58-178">Se preme en **Non** non funciona a ligazón para o botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="e2f58-179">O ficheiro de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode encontrarse en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], en **Documentos** para o proxecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.</span><span class="sxs-lookup"><span data-stu-id="e2f58-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="e2f58-180">Cargar un ficheiro a Grupos de Office</span><span class="sxs-lookup"><span data-stu-id="e2f58-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="e2f58-181">No menú principal, prema en **Project Service** > **Cargar**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="e2f58-182">Seleccione **Documentos de proxecto Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="e2f58-183">Na caixa de diálogo **Activar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Si** ou **Non**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="e2f58-184">Se preme en **Si**, poderá seleccionar o botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation, iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e cargar o ficheiro de proxecto desde a biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e2f58-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="e2f58-185">Se preme en **Non** non funciona a ligazón para o botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="e2f58-186">O ficheiro de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode encontrarse en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], en **Documentos** para o proxecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.</span><span class="sxs-lookup"><span data-stu-id="e2f58-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="e2f58-187">Publicar o proxecto como modelo</span><span class="sxs-lookup"><span data-stu-id="e2f58-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="e2f58-188">Pode gardar o seu proxecto e reutilizalo se o garda como modelo de proxecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="e2f58-189">Os modelos de proxecto son plans de proxecto reutilizables en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e2f58-190">[Crear un modelo de proxecto (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="e2f58-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="e2f58-191">No separador **Project Service**, prema en **Publicar** > **Novo modelo de proxecto de Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="e2f58-192">Na caixa de diálogo **Publicar nun novo modelo de proxecto en Project Service**, introduza o **Nome do modelo de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="e2f58-193">Tamén pode marcar **Ligar o plan do proxecto a Project Service Automation** para ligar o ficheiro do proxecto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="e2f58-194">Prema **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="e2f58-194">Click **Publish**.</span></span>  

<span data-ttu-id="e2f58-195">Ligar o ficheiro do Proxecto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] converte o ficheiro do proxecto en principal e define a estrutura de subdivisión do traballo no modelo de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a só de lectura.</span><span class="sxs-lookup"><span data-stu-id="e2f58-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="e2f58-196">Para modificar a planificación do proxecto é necesario facelas en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicalas como actualizacións en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f58-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="e2f58-197">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="e2f58-197">See Also</span></span>  
 [<span data-ttu-id="e2f58-198">Guía do xestor de proxectos</span><span class="sxs-lookup"><span data-stu-id="e2f58-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
