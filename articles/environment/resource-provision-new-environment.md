---
title: Fornecer un novo ambiente
description: Este tema ofrece información sobre como fornecer un novo ambiente de Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642967"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="250b6-103">Fornecer un novo ambiente</span><span class="sxs-lookup"><span data-stu-id="250b6-103">Provision a new environment</span></span>

<span data-ttu-id="250b6-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="250b6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="250b6-105">Este tema ofrece información sobre como proporcionar un novo ambiente de Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.</span><span class="sxs-lookup"><span data-stu-id="250b6-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="250b6-106">Activar o fornecemento automatizado de Project Operations nun proxecto de LCS</span><span class="sxs-lookup"><span data-stu-id="250b6-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="250b6-107">Siga os pasos seguintes para activar o fluxo de fornecemento automatizado de Project Operations para o seu proxecto de LCS.</span><span class="sxs-lookup"><span data-stu-id="250b6-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="250b6-108">Vaia a [LCS](https://lcs.dynamics.com/v2) e seleccione o mosaico **Xestión da funcionalidade de previsualización**.</span><span class="sxs-lookup"><span data-stu-id="250b6-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="250b6-109">Na lista **Funcionalidade de previsualización**, seleccione **Funcionalidade Project Operations** e, a seguir, seleccione **Funcionalidade de previsualización activada** para activar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="250b6-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="250b6-110">Este paso só se realiza unha vez por proxecto de LCS.</span><span class="sxs-lookup"><span data-stu-id="250b6-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="250b6-111">Fornecer un ambiente de Project Operations</span><span class="sxs-lookup"><span data-stu-id="250b6-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="250b6-112">Abra un novo despregamento de Dynamics 365 Finance [ambiente de demostración](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ou [ambiente de illamento de procesos/produción](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="250b6-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="250b6-113">Consulte o asistente de **Fornecemento de ambientes**.</span><span class="sxs-lookup"><span data-stu-id="250b6-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="250b6-114">Asegúrese de que a versión da aplicación seleccionada sexa 10.0.13 ou superior.</span><span class="sxs-lookup"><span data-stu-id="250b6-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="250b6-115">Para fornecer Project Operations, en **Configuración avanzada**, seleccione **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="250b6-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="250b6-116">Active a **Configuración de Common Data Service** seleccionando **Si** e logo introduza información nos campos obrigatorios:</span><span class="sxs-lookup"><span data-stu-id="250b6-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="250b6-117">Nome</span><span class="sxs-lookup"><span data-stu-id="250b6-117">Name</span></span>
  - <span data-ttu-id="250b6-118">Rexión</span><span class="sxs-lookup"><span data-stu-id="250b6-118">Region</span></span>
  - <span data-ttu-id="250b6-119">Linguaxe</span><span class="sxs-lookup"><span data-stu-id="250b6-119">Language</span></span>
  - <span data-ttu-id="250b6-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="250b6-120">Currency</span></span>
 
5. <span data-ttu-id="250b6-121">No campo **Modelo de Common Data Service**, seleccione **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="250b6-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="250b6-122">Seleccionar o tipo de ambiente para o seu despregamento.</span><span class="sxs-lookup"><span data-stu-id="250b6-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="250b6-123">Unha proba baseada en subscrición permitiralle despregar un ambiente de CDS durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="250b6-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configuración de despregamento](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="250b6-125">Seleccione **Acepto** para aceptar os termos do servizo e logo seleccione **Feito** para volver á configuración de despregamento.</span><span class="sxs-lookup"><span data-stu-id="250b6-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentimento de despregamento](./media/2DeploymentConsent.png)

7. <span data-ttu-id="250b6-127">Complete os restantes campos obrigatorios no asistente e confirme o despregamento.</span><span class="sxs-lookup"><span data-stu-id="250b6-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="250b6-128">O tempo de subministración do ambiente varía segundo o tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="250b6-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="250b6-129">A subministración pode levar ata seis horas.</span><span class="sxs-lookup"><span data-stu-id="250b6-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="250b6-130">Despois de completar correctamente o despregamento, o ambiente mostrarase como **Despregado**.</span><span class="sxs-lookup"><span data-stu-id="250b6-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="250b6-131">Para confirmar que o ambiente se implantou correctamente, seleccione **Iniciar sesión** e inicie sesión no ambiente para confirmar.</span><span class="sxs-lookup"><span data-stu-id="250b6-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalles do ambiente de ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="250b6-133">Aplicar datos de demostración de Project Operations Finance (paso opcional)</span><span class="sxs-lookup"><span data-stu-id="250b6-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="250b6-134">Aplique os datos de demostración de Project Operations Finance á versión de servizo 10.0.13 do ambiente aloxado na nube como se describe [neste artigo](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="250b6-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="250b6-135">Aplicar actualizacións ao ambiente de Finance</span><span class="sxs-lookup"><span data-stu-id="250b6-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="250b6-136">Project Operations require un ambiente de Finance coa versión da aplicación **10.0.13 (10.0.569.20009)** ou superior.</span><span class="sxs-lookup"><span data-stu-id="250b6-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="250b6-137">É posible que teña que aplicar actualizacións de calidade ao seu ambiente de Finance para recibir esta versión.</span><span class="sxs-lookup"><span data-stu-id="250b6-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="250b6-138">En LCS, na páxina **Detalles do ambiente**, na sección **Actualizacións dispoñibles**, seleccione **Ver actualización**.</span><span class="sxs-lookup"><span data-stu-id="250b6-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Ver actualizacións](./media/5ViewUpdates.png)

2. <span data-ttu-id="250b6-140">Na páxina **Actualizacións binarias**, seleccione **Gardar paquete.**</span><span class="sxs-lookup"><span data-stu-id="250b6-140">On the **Binary updates** page, select **Save package.**</span></span>

![Gardar paquete](./media/6SavePackage.png)

3. <span data-ttu-id="250b6-142">Prema **Seleccionar todos** e logo seleccione **Gardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="250b6-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar e gardar actualizacións](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="250b6-144">Introduza un nome e unha descrición do paquete e seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="250b6-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="250b6-145">Dependendo da conexión a Internet, este proceso pode levar algún tempo.</span><span class="sxs-lookup"><span data-stu-id="250b6-145">Depending on the internet connection, this process might take some time.</span></span>

![Cargar o paquete á biblioteca de activos](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="250b6-147">Despois de gardar o paquete, seleccione **Feito** e garde este paquete na biblioteca de activos do seu proxecto de LCS.</span><span class="sxs-lookup"><span data-stu-id="250b6-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="250b6-148">Gardar e validar o paquete pode levar uns 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="250b6-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="250b6-149">Para aplicar a actualización, navegue ata a páxina **Detalles do ambiente** páxina en LCS e seleccione **Manter** > **Aplicar actualizacións**.</span><span class="sxs-lookup"><span data-stu-id="250b6-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Manter ambientes](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="250b6-151">Na lista de actualizacións seleccione o paquete que creou e seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="250b6-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar actualizacións](./media/10ApplyUpdates.png)

<span data-ttu-id="250b6-153">O servizo do ambiente levará algún tempo.</span><span class="sxs-lookup"><span data-stu-id="250b6-153">Environment servicing will take some time.</span></span> <span data-ttu-id="250b6-154">Despois de completalo, o ambiente volverá a un estado despregado.</span><span class="sxs-lookup"><span data-stu-id="250b6-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ambiente despregado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="250b6-156">Establecer unha conexión de escrita dual</span><span class="sxs-lookup"><span data-stu-id="250b6-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="250b6-157">No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="250b6-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="250b6-158">En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións**.</span><span class="sxs-lookup"><span data-stu-id="250b6-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="250b6-159">Despois de completar a ligazón, seleccione **Ligazón a CDS para aplicacións** de novo.</span><span class="sxs-lookup"><span data-stu-id="250b6-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="250b6-160">Redixiráselle a escrita dual en Finance.</span><span class="sxs-lookup"><span data-stu-id="250b6-160">You will be redirected to Dual Write in Finance.</span></span>

![Ligazón a CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="250b6-162">Seleccione **Aplicar solución** para acceder ás entidades que serán asignadas na integración.</span><span class="sxs-lookup"><span data-stu-id="250b6-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar solucións](./media/13ApplySolutions.png)

5. <span data-ttu-id="250b6-164">Seleccione ambas solucións, **Mapa de entidade de escrita dual de Dynamics 365 Finance and Operations** e **Mapas de entidades de escrita dual de Dynamics 365 Project Operations** e, a seguir, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="250b6-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar solucións](./media/14ConfirmSolutions.png)

<span data-ttu-id="250b6-166">Despois de aplicar as solucións, as entidades de escrita dual aplícanse ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="250b6-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicación de solucións](./media/15ApplyingSolutions.png)

<span data-ttu-id="250b6-168">Despois de aplicar as entidades, todas as asignacións dispoñibles aparecen no ambiente.</span><span class="sxs-lookup"><span data-stu-id="250b6-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapas de escrita dual](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="250b6-170">Actualice as entidades de datos despois da actualización</span><span class="sxs-lookup"><span data-stu-id="250b6-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="250b6-171">En Finance, vaia á área de traballo **Xestión de datos**.</span><span class="sxs-lookup"><span data-stu-id="250b6-171">In Finance, go to the **Data management** workspace.</span></span>

![Área de traballo de xestión de datos](./media/16DataManagement.png)

2. <span data-ttu-id="250b6-173">Seleccione o mosaico **Parámetros marco**.</span><span class="sxs-lookup"><span data-stu-id="250b6-173">Select the **Framework parameters** tile.</span></span>

![Parámetros do marco](./media/17FrameworkParameters.png)

3. <span data-ttu-id="250b6-175">Na páxina **Configuración de entidades**, seleccione **Actualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="250b6-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualizar lista de entidades](./media/18RefreshEntityList.png)

<span data-ttu-id="250b6-177">A actualización tardará aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="250b6-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="250b6-178">Recibirá unha alerta cando remate.</span><span class="sxs-lookup"><span data-stu-id="250b6-178">You will receive an alert when it is complete.</span></span>

![Actualizar confirmación](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="250b6-180">Executar mapas de escrita dual en Project Operations</span><span class="sxs-lookup"><span data-stu-id="250b6-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="250b6-181">No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="250b6-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="250b6-182">En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións.**</span><span class="sxs-lookup"><span data-stu-id="250b6-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="250b6-183">Despois de seleccionar a ligazón, redirixiráselle á lista de entidades nas asignacións.</span><span class="sxs-lookup"><span data-stu-id="250b6-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="250b6-184">Inicie os mapas segundo se describe na seguinte táboa.</span><span class="sxs-lookup"><span data-stu-id="250b6-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="250b6-185">Asegúrese de seguir a secuencia como aparece na lista.</span><span class="sxs-lookup"><span data-stu-id="250b6-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="250b6-186">**Asignación de entidades**</span><span class="sxs-lookup"><span data-stu-id="250b6-186">**Entity Map**</span></span> | <span data-ttu-id="250b6-187">**Actualizar entidade**</span><span class="sxs-lookup"><span data-stu-id="250b6-187">**Refresh entity**</span></span> | <span data-ttu-id="250b6-188">**Sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="250b6-188">**Initial sync**</span></span> | <span data-ttu-id="250b6-189">**Padrón para a sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="250b6-189">**Master for initial sync**</span></span> | <span data-ttu-id="250b6-190">**Executar requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="250b6-190">**Run prerequisites**</span></span> | <span data-ttu-id="250b6-191">**Sincronización inicial de requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="250b6-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="250b6-192">**Roles de recursos do proxecto para todas as empresas (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="250b6-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="250b6-193">No</span><span class="sxs-lookup"><span data-stu-id="250b6-193">No</span></span> | <span data-ttu-id="250b6-194">Si</span><span class="sxs-lookup"><span data-stu-id="250b6-194">Yes</span></span> | <span data-ttu-id="250b6-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="250b6-195">Common Data Service</span></span> | <span data-ttu-id="250b6-196">No</span><span class="sxs-lookup"><span data-stu-id="250b6-196">No</span></span> | <span data-ttu-id="250b6-197">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-197">N\A</span></span> |
| <span data-ttu-id="250b6-198">**Entidades legais (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="250b6-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="250b6-199">No</span><span class="sxs-lookup"><span data-stu-id="250b6-199">No</span></span> | <span data-ttu-id="250b6-200">Si</span><span class="sxs-lookup"><span data-stu-id="250b6-200">Yes</span></span> | <span data-ttu-id="250b6-201">Aplicacións de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="250b6-201">Finance and Operations apps</span></span> | <span data-ttu-id="250b6-202">No</span><span class="sxs-lookup"><span data-stu-id="250b6-202">No</span></span> | <span data-ttu-id="250b6-203">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-203">N\A</span></span> |
| <span data-ttu-id="250b6-204">**Libro maior (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="250b6-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="250b6-205">No</span><span class="sxs-lookup"><span data-stu-id="250b6-205">No</span></span> | <span data-ttu-id="250b6-206">Si</span><span class="sxs-lookup"><span data-stu-id="250b6-206">Yes</span></span> | <span data-ttu-id="250b6-207">Aplicacións de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="250b6-207">Finance and Operations apps</span></span> | <span data-ttu-id="250b6-208">Si</span><span class="sxs-lookup"><span data-stu-id="250b6-208">Yes</span></span> | <span data-ttu-id="250b6-209">Si, aplicacións de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="250b6-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="250b6-210">**Datos reais de integración de Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="250b6-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="250b6-211">No</span><span class="sxs-lookup"><span data-stu-id="250b6-211">No</span></span> | <span data-ttu-id="250b6-212">No</span><span class="sxs-lookup"><span data-stu-id="250b6-212">No</span></span> | <span data-ttu-id="250b6-213">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-213">N\A</span></span> | <span data-ttu-id="250b6-214">Si</span><span class="sxs-lookup"><span data-stu-id="250b6-214">Yes</span></span> | <span data-ttu-id="250b6-215">No</span><span class="sxs-lookup"><span data-stu-id="250b6-215">No</span></span> |
| <span data-ttu-id="250b6-216">**Liñas de contrato de proxecto (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="250b6-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="250b6-217">No</span><span class="sxs-lookup"><span data-stu-id="250b6-217">No</span></span> | <span data-ttu-id="250b6-218">No</span><span class="sxs-lookup"><span data-stu-id="250b6-218">No</span></span> | <span data-ttu-id="250b6-219">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-219">N\A</span></span> | <span data-ttu-id="250b6-220">No</span><span class="sxs-lookup"><span data-stu-id="250b6-220">No</span></span> | <span data-ttu-id="250b6-221">No</span><span class="sxs-lookup"><span data-stu-id="250b6-221">No</span></span> |
| <span data-ttu-id="250b6-222">**Entidade de integración para as relacións de transaccións do proxecto (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="250b6-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="250b6-223">No</span><span class="sxs-lookup"><span data-stu-id="250b6-223">No</span></span> | <span data-ttu-id="250b6-224">No</span><span class="sxs-lookup"><span data-stu-id="250b6-224">No</span></span> | <span data-ttu-id="250b6-225">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-225">N\A</span></span> | <span data-ttu-id="250b6-226">No</span><span class="sxs-lookup"><span data-stu-id="250b6-226">No</span></span> | <span data-ttu-id="250b6-227">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-227">N\A</span></span> |
| <span data-ttu-id="250b6-228">**Fitos da liña de contrato de integración de Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="250b6-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="250b6-229">No</span><span class="sxs-lookup"><span data-stu-id="250b6-229">No</span></span> | <span data-ttu-id="250b6-230">No</span><span class="sxs-lookup"><span data-stu-id="250b6-230">No</span></span> | <span data-ttu-id="250b6-231">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-231">N\A</span></span> | <span data-ttu-id="250b6-232">No</span><span class="sxs-lookup"><span data-stu-id="250b6-232">No</span></span> | <span data-ttu-id="250b6-233">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-233">N\A</span></span> |
| <span data-ttu-id="250b6-234">**Entidade de integración de Project Operations para estimacións de gastos (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="250b6-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="250b6-235">No</span><span class="sxs-lookup"><span data-stu-id="250b6-235">No</span></span> | <span data-ttu-id="250b6-236">No</span><span class="sxs-lookup"><span data-stu-id="250b6-236">No</span></span> | <span data-ttu-id="250b6-237">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-237">N\A</span></span> | <span data-ttu-id="250b6-238">No</span><span class="sxs-lookup"><span data-stu-id="250b6-238">No</span></span> | <span data-ttu-id="250b6-239">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-239">N\A</span></span> |
| <span data-ttu-id="250b6-240">**Entidade de exportación de categorías de gastos de proxecto de integración de Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="250b6-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="250b6-241">No</span><span class="sxs-lookup"><span data-stu-id="250b6-241">No</span></span> | <span data-ttu-id="250b6-242">No</span><span class="sxs-lookup"><span data-stu-id="250b6-242">No</span></span> | <span data-ttu-id="250b6-243">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-243">N\A</span></span> | <span data-ttu-id="250b6-244">No</span><span class="sxs-lookup"><span data-stu-id="250b6-244">No</span></span> | <span data-ttu-id="250b6-245">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-245">N\A</span></span> |
| <span data-ttu-id="250b6-246">**Entidade de exportación de gastos de proxecto de integración de Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="250b6-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="250b6-247">Si</span><span class="sxs-lookup"><span data-stu-id="250b6-247">Yes</span></span> | <span data-ttu-id="250b6-248">No</span><span class="sxs-lookup"><span data-stu-id="250b6-248">No</span></span> | <span data-ttu-id="250b6-249">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-249">N\A</span></span> | <span data-ttu-id="250b6-250">No</span><span class="sxs-lookup"><span data-stu-id="250b6-250">No</span></span> | <span data-ttu-id="250b6-251">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-251">N\A</span></span> |
| <span data-ttu-id="250b6-252">**Entidade de integración de Project Operations para estimacións de horas (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="250b6-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="250b6-253">Si</span><span class="sxs-lookup"><span data-stu-id="250b6-253">Yes</span></span> | <span data-ttu-id="250b6-254">No</span><span class="sxs-lookup"><span data-stu-id="250b6-254">No</span></span> | <span data-ttu-id="250b6-255">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-255">N\A</span></span> | <span data-ttu-id="250b6-256">No</span><span class="sxs-lookup"><span data-stu-id="250b6-256">No</span></span> | <span data-ttu-id="250b6-257">N\A</span><span class="sxs-lookup"><span data-stu-id="250b6-257">N\A</span></span> |


4. <span data-ttu-id="250b6-258">Para actualizar a entidade, seleccione o nome do mapa e logo seleccione **Actualizar entidades**.</span><span class="sxs-lookup"><span data-stu-id="250b6-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualizar mapa](./media/20RefreshMapping.png)

5. <span data-ttu-id="250b6-260">Ao finalizar a actualización, execute o mapa.</span><span class="sxs-lookup"><span data-stu-id="250b6-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="250b6-261">Antes de activar o seguinte mapa, verifique que o mapa da táboa estea en estado de **Execución**.</span><span class="sxs-lookup"><span data-stu-id="250b6-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="250b6-262">A execución de mapas cun maior número de requisitos previos pode levar moito tempo.</span><span class="sxs-lookup"><span data-stu-id="250b6-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="250b6-263">Para executar un mapa con requisitos previos, active o conmutador **Mostrar mapas de entidades relacionadas**.</span><span class="sxs-lookup"><span data-stu-id="250b6-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="250b6-264">Se a táboa indica **Sincronización inicial de requisitos previos** é **Non**, verifique que o indicador **Sincronización inicial** está **Desactivado** en todos os mapas de requisitos previos antes de executalo.</span><span class="sxs-lookup"><span data-stu-id="250b6-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar mapa](./media/21RunMap.png)

6. <span data-ttu-id="250b6-266">Valide que todos os mapas relacionados co proxecto están en estado de execución.</span><span class="sxs-lookup"><span data-stu-id="250b6-266">Validate all project related maps are in the running state.</span></span>

![Todos os mapas en execución](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="250b6-268">Aplicar os datos de configuración en CDS para Project Operations (opcional)</span><span class="sxs-lookup"><span data-stu-id="250b6-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="250b6-269">Se aplicou datos de demostración ao ambiente de Finance, consulte [Configurar e aplicar os datos de configuración en Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar datos de demostración ao ambiente de CDS.</span><span class="sxs-lookup"><span data-stu-id="250b6-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="250b6-270">O seu ambiente de Project Operations agora está subministrado e configurado.</span><span class="sxs-lookup"><span data-stu-id="250b6-270">Your Project Operations environment is now provisioned and configured.</span></span> 
