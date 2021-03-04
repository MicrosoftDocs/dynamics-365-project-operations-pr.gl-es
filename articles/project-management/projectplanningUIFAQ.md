---
title: Resolver problemas de traballo na grade de tarefas
description: Este tema ofrece a información de solución de problemas necesaria cando se traballa na grade de tarefas.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031535"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="ca4e2-103">Resolver problemas de traballo na grade de tarefas</span><span class="sxs-lookup"><span data-stu-id="ca4e2-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="ca4e2-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="ca4e2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca4e2-105">Este tema describe como solucionar problemas que pode atopar ao traballar coa xestión de custos.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="ca4e2-106">Activar cookies</span><span class="sxs-lookup"><span data-stu-id="ca4e2-106">Enable cookies</span></span>

<span data-ttu-id="ca4e2-107">Project Operations require que se activen as cookies de terceiros para renderizar a estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="ca4e2-108">Cando as cookies de terceiros non estean activadas, no canto de ver tarefas, verá unha páxina en branco cando seleccione o separador **Tarefas** guía na páxina **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Separador en branco cando as cookies de terceiros non están activadas](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="ca4e2-110">Outros métodos</span><span class="sxs-lookup"><span data-stu-id="ca4e2-110">Workaround</span></span>
<span data-ttu-id="ca4e2-111">Para os navegadores Microsoft Edge ou Google Chrome, os seguintes procedementos describen como actualizar a configuración do seu explorador para activar as cookies de terceiros.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="ca4e2-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ca4e2-112">Microsoft Edge</span></span>

1. <span data-ttu-id="ca4e2-113">Abra o explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="ca4e2-114">Na esquina superior dereita, seleccione a icona de **puntos suspensivos** (...) e seleccione **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="ca4e2-115">En **Cookies e permisos do sitio**, seleccione **Cookies e datos do sitio**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="ca4e2-116">Desactive **Bloquear cookies de terceiros**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="ca4e2-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="ca4e2-117">Google Chrome</span></span>

1. <span data-ttu-id="ca4e2-118">Abra o explorador Chrome.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="ca4e2-119">Na esquina superior dereita, seleccione os tres puntos verticais e logo seleccione **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="ca4e2-120">En **Privacidade e seguridade**, seleccione **Cookies e outros datos do sitio**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="ca4e2-121">Seleccione **Permitir todas as cookies**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca4e2-122">Se bloquea as cookies de terceiros, bloquearanse todas as cookies e os datos doutros sitios, aínda que o sitio estea permitido na súa lista de excepcións.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="ca4e2-123">Extremo de PEX</span><span class="sxs-lookup"><span data-stu-id="ca4e2-123">PEX Endpoint</span></span>

<span data-ttu-id="ca4e2-124">Project Operations requiren que un parámetro do proxecto faga referencia ao extremo de PEX.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="ca4e2-125">Este extremo é necesario para comunicarse co servizo usado para renderizar a estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="ca4e2-126">Se o parámetro non está activado, recibirá o erro "O parámetro do proxecto non é válido".</span><span class="sxs-lookup"><span data-stu-id="ca4e2-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="ca4e2-127">Outros métodos</span><span class="sxs-lookup"><span data-stu-id="ca4e2-127">Workaround</span></span>
 ![Campo Extremo PEX no parámetro do proxecto](media/projectparameter.png)

1. <span data-ttu-id="ca4e2-129">Engada o campo **Extremo PEX** á páxina **Parámetros do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="ca4e2-130">Actualice o campo co valor seguinte: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="ca4e2-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="ca4e2-131">Elimine o campo da páxina **Parámetros do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="ca4e2-132">Privilexios para o proxecto para a web</span><span class="sxs-lookup"><span data-stu-id="ca4e2-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="ca4e2-133">Project Operations depende dun servizo de programación externo.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="ca4e2-134">O servizo require que un usuario teña varios roles atribuídos para ler e escribir a entidades relacionadas coa estrutura de subdivisión do traballo.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="ca4e2-135">Estas entidades inclúen tarefas do proxecto, atribucións de recursos e dependencias de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="ca4e2-136">Se un usuario non pode renderizar a estrutura de subdivisión do traballo cando vai ao separador **Tarefas**, probablemente sexa porque o proxecto para Project Operations non se activou.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="ca4e2-137">Un usuario pode recibir un erro de rol de seguranza ou un erro relacionado cunha denegación de acceso.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="ca4e2-138">Outros métodos</span><span class="sxs-lookup"><span data-stu-id="ca4e2-138">Workaround</span></span>

1. <span data-ttu-id="ca4e2-139">Vaia a **Configuración > Seguridade > Usuarios > Usuarios da aplicación**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Lector de aplicacións](media/applicationuser.jpg)
   
2. <span data-ttu-id="ca4e2-141">Prema dúas veces no rexistro de usuario da aplicación para verificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ca4e2-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="ca4e2-142">O usuario ten acceso ao proxecto.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-142">The user has access to the project.</span></span> <span data-ttu-id="ca4e2-143">Esta verificación normalmente faise asegurándose de que o usuario ten o rol de seguranza **Xestor de proxectos**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="ca4e2-144">O usuario da aplicación Microsoft Project existe e está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="ca4e2-145">Se este usuario non existe, pode crear un novo rexistro de usuario.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="ca4e2-146">Seleccione **Novos usuarios**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-146">Select **New Users**.</span></span> <span data-ttu-id="ca4e2-147">Cambie o formulario de entrada a **Usuario da aplicación** e, a seguir, engada o **ID de aplicación**.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detalles do usuario da aplicación](media/applicationuserdetails.jpg)

4. <span data-ttu-id="ca4e2-149">Verifique que ao usuario se lle asignou a licenza correcta e que o servizo está activado nos detalles dos plans de servizo da licenza.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="ca4e2-150">Verifique que o usuario pode abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="ca4e2-151">Verifique a través dos parámetros do proxecto que o sistema apunta ao extremo correcto do proxecto.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="ca4e2-152">Verifique que se crea o usuario da aplicación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="ca4e2-153">Aplique ao usuario os seguintes roles de seguranza:</span><span class="sxs-lookup"><span data-stu-id="ca4e2-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="ca4e2-154">Usuario de Dataverse</span><span class="sxs-lookup"><span data-stu-id="ca4e2-154">Dataverse User</span></span>
  - <span data-ttu-id="ca4e2-155">Sistema de Project Operations</span><span class="sxs-lookup"><span data-stu-id="ca4e2-155">Project Operations System</span></span>
  - <span data-ttu-id="ca4e2-156">Sistema do proxecto</span><span class="sxs-lookup"><span data-stu-id="ca4e2-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="ca4e2-157">Erro ao actualizar a estrutura de subdivisión do traballo</span><span class="sxs-lookup"><span data-stu-id="ca4e2-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="ca4e2-158">Cando se fai unha ou máis actualizacións na estrutura de subdivisión do traballo, os cambios finalmente fallan e non se gardan.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="ca4e2-159">Prodúcese un erro na grade de programación indicando que "Non se puideron gardar os cambios recentes que fixo".</span><span class="sxs-lookup"><span data-stu-id="ca4e2-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="ca4e2-160">Outros métodos</span><span class="sxs-lookup"><span data-stu-id="ca4e2-160">Workaround</span></span>

1. <span data-ttu-id="ca4e2-161">Verifique que ao usuario se lle asignou a licenza correcta e que o servizo está activado nos detalles dos plans de servizo da licenza.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="ca4e2-162">Verifique que o usuario pode abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="ca4e2-163">Verifique que o sistema apunta ao extremo correcto do proxecto.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="ca4e2-164">Verifique que se creou o usuario da aplicación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="ca4e2-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="ca4e2-165">Aplique ao usuario os seguintes roles de seguranza:</span><span class="sxs-lookup"><span data-stu-id="ca4e2-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="ca4e2-166">Usuario de Dataverse ou usuario de base</span><span class="sxs-lookup"><span data-stu-id="ca4e2-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="ca4e2-167">Sistema de Project Operations</span><span class="sxs-lookup"><span data-stu-id="ca4e2-167">Project Operations System</span></span>
  - <span data-ttu-id="ca4e2-168">Sistema do proxecto</span><span class="sxs-lookup"><span data-stu-id="ca4e2-168">Project System</span></span>
  - <span data-ttu-id="ca4e2-169">Sistema de escritura dual de Project Operations (Este rol é necesario se está a despregar o escenario baseado en recursos/sen fornecemento de Project Operations).</span><span class="sxs-lookup"><span data-stu-id="ca4e2-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
