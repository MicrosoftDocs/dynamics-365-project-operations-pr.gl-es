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
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121171"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="db5cd-103">Fornecer un novo ambiente</span><span class="sxs-lookup"><span data-stu-id="db5cd-103">Provision a new environment</span></span>

<span data-ttu-id="db5cd-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="db5cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="db5cd-105">Este tema ofrece información sobre como fornecer un novo ambiente de Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.</span><span class="sxs-lookup"><span data-stu-id="db5cd-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="db5cd-106">Activar o fornecemento automatizado de Project Operations nun proxecto de LCS</span><span class="sxs-lookup"><span data-stu-id="db5cd-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="db5cd-107">Siga os pasos seguintes para activar o fluxo de fornecemento automatizado de Project Operations para o seu proxecto de LCS.</span><span class="sxs-lookup"><span data-stu-id="db5cd-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="db5cd-108">Vaia a [LCS](https://lcs.dynamics.com/v2) e seleccione o mosaico **Xestión da funcionalidade de previsualización**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="db5cd-109">Na lista **Funcionalidade de previsualización**, seleccione **Funcionalidade Project Operations** e, a seguir, seleccione **Funcionalidade de previsualización activada** para activar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="db5cd-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="db5cd-110">Este paso só se realiza unha vez por proxecto de LCS.</span><span class="sxs-lookup"><span data-stu-id="db5cd-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="db5cd-111">Fornecer un ambiente de Project Operations</span><span class="sxs-lookup"><span data-stu-id="db5cd-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="db5cd-112">Abra un novo despregamento de Dynamics 365 Finance [ambiente de demostración](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ou [ambiente de illamento de procesos/produción](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="db5cd-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="db5cd-113">Consulte o asistente de **Fornecemento de ambientes**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="db5cd-114">Asegúrese de que a versión da aplicación seleccionada sexa 10.0.13 ou superior.</span><span class="sxs-lookup"><span data-stu-id="db5cd-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="db5cd-115">Para fornecer Project Operations, en **Configuración avanzada**, seleccione **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="db5cd-116">Active a **Configuración de Common Data Service** seleccionando **Si** e logo introduza información nos campos obrigatorios:</span><span class="sxs-lookup"><span data-stu-id="db5cd-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="db5cd-117">Nome</span><span class="sxs-lookup"><span data-stu-id="db5cd-117">Name</span></span>
  - <span data-ttu-id="db5cd-118">Rexión</span><span class="sxs-lookup"><span data-stu-id="db5cd-118">Region</span></span>
  - <span data-ttu-id="db5cd-119">Linguaxe</span><span class="sxs-lookup"><span data-stu-id="db5cd-119">Language</span></span>
  - <span data-ttu-id="db5cd-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="db5cd-120">Currency</span></span>
 
5. <span data-ttu-id="db5cd-121">No campo **Modelo de Common Data Service**, seleccione **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="db5cd-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="db5cd-122">Seleccionar o tipo de ambiente para o seu despregamento.</span><span class="sxs-lookup"><span data-stu-id="db5cd-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="db5cd-123">Unha proba baseada en subscrición permitiralle despregar un ambiente de CDS durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="db5cd-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configuración de despregamento](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="db5cd-125">Seleccione **Acepto** para aceptar os termos do servizo e logo seleccione **Feito** para volver á configuración de despregamento.</span><span class="sxs-lookup"><span data-stu-id="db5cd-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentimento de despregamento](./media/2DeploymentConsent.png)

7. <span data-ttu-id="db5cd-127">Complete os restantes campos obrigatorios no asistente e confirme o despregamento.</span><span class="sxs-lookup"><span data-stu-id="db5cd-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="db5cd-128">O tempo de subministración do ambiente varía segundo o tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="db5cd-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="db5cd-129">A subministración pode levar ata seis horas.</span><span class="sxs-lookup"><span data-stu-id="db5cd-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="db5cd-130">Despois de completar correctamente o despregamento, o ambiente mostrarase como **Despregado**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="db5cd-131">Para confirmar que o ambiente se implantou correctamente, seleccione **Iniciar sesión** e inicie sesión no ambiente para confirmar.</span><span class="sxs-lookup"><span data-stu-id="db5cd-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalles do ambiente de ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="db5cd-133">Aplicar datos de demostración de Project Operations Finance (paso opcional)</span><span class="sxs-lookup"><span data-stu-id="db5cd-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="db5cd-134">Aplique os datos de demostración de Project Operations Finance á versión de servizo 10.0.13 do ambiente aloxado na nube como se describe [neste artigo](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="db5cd-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="db5cd-135">Aplicar actualizacións ao ambiente de Finance</span><span class="sxs-lookup"><span data-stu-id="db5cd-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="db5cd-136">Project Operations require un ambiente de Finance coa versión da aplicación **10.0.13 (10.0.569.20009)** ou superior.</span><span class="sxs-lookup"><span data-stu-id="db5cd-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="db5cd-137">É posible que teña que aplicar actualizacións de calidade ao seu ambiente de Finance para recibir esta versión.</span><span class="sxs-lookup"><span data-stu-id="db5cd-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="db5cd-138">En LCS, na páxina **Detalles do ambiente**, na sección **Actualizacións dispoñibles**, seleccione **Ver actualización**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Ver actualizacións](./media/5ViewUpdates.png)

2. <span data-ttu-id="db5cd-140">Na páxina **Actualizacións binarias**, seleccione **Gardar paquete.**</span><span class="sxs-lookup"><span data-stu-id="db5cd-140">On the **Binary updates** page, select **Save package.**</span></span>

![Gardar paquete](./media/6SavePackage.png)

3. <span data-ttu-id="db5cd-142">Prema **Seleccionar todos** e logo seleccione **Gardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar e gardar actualizacións](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="db5cd-144">Introduza un nome e unha descrición do paquete e seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="db5cd-145">Dependendo da conexión a Internet, este proceso pode levar algún tempo.</span><span class="sxs-lookup"><span data-stu-id="db5cd-145">Depending on the internet connection, this process might take some time.</span></span>

![Cargar o paquete á biblioteca de activos](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="db5cd-147">Despois de gardar o paquete, seleccione **Feito** e garde este paquete na biblioteca de activos do seu proxecto de LCS.</span><span class="sxs-lookup"><span data-stu-id="db5cd-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="db5cd-148">Gardar e validar o paquete pode levar uns 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="db5cd-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="db5cd-149">Para aplicar a actualización, navegue ata a páxina **Detalles do ambiente** páxina en LCS e seleccione **Manter** > **Aplicar actualizacións**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Manter ambientes](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="db5cd-151">Na lista de actualizacións seleccione o paquete que creou e seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar actualizacións](./media/10ApplyUpdates.png)

<span data-ttu-id="db5cd-153">O servizo do ambiente levará algún tempo.</span><span class="sxs-lookup"><span data-stu-id="db5cd-153">Environment servicing will take some time.</span></span> <span data-ttu-id="db5cd-154">Despois de completalo, o ambiente volverá a un estado despregado.</span><span class="sxs-lookup"><span data-stu-id="db5cd-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ambiente despregado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="db5cd-156">Establecer unha conexión de escrita dual</span><span class="sxs-lookup"><span data-stu-id="db5cd-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="db5cd-157">No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="db5cd-158">En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="db5cd-159">Despois de completar a ligazón, seleccione **Ligazón a CDS para aplicacións** de novo.</span><span class="sxs-lookup"><span data-stu-id="db5cd-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="db5cd-160">Redixiráselle a escrita dual en Finance.</span><span class="sxs-lookup"><span data-stu-id="db5cd-160">You will be redirected to Dual Write in Finance.</span></span>

![Ligazón a CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="db5cd-162">Seleccione **Aplicar solución** para acceder ás entidades que serán asignadas na integración.</span><span class="sxs-lookup"><span data-stu-id="db5cd-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar solucións](./media/13ApplySolutions.png)

5. <span data-ttu-id="db5cd-164">Seleccione ambas solucións, **Mapa de entidades de escrita dual de Dynamics 365 Finance and Operations** e **Mapas de entidades de escrita dual de Dynamics 365 Project Operations** e, a seguir, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar solucións](./media/14ConfirmSolutions.png)

<span data-ttu-id="db5cd-166">Despois de aplicar as solucións, as entidades de escrita dual aplícanse ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="db5cd-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicación de solucións](./media/15ApplyingSolutions.png)

<span data-ttu-id="db5cd-168">Despois de aplicar as entidades, todas as asignacións dispoñibles aparecen no ambiente.</span><span class="sxs-lookup"><span data-stu-id="db5cd-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapas de escrita dual](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="db5cd-170">Actualice as entidades de datos despois da actualización</span><span class="sxs-lookup"><span data-stu-id="db5cd-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="db5cd-171">En Finance, vaia á área de traballo **Xestión de datos**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-171">In Finance, go to the **Data management** workspace.</span></span>

![Área de traballo de xestión de datos](./media/16DataManagement.png)

2. <span data-ttu-id="db5cd-173">Seleccione o mosaico **Parámetros marco**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-173">Select the **Framework parameters** tile.</span></span>

![Parámetros do marco](./media/17FrameworkParameters.png)

3. <span data-ttu-id="db5cd-175">Na páxina **Configuración de entidades**, seleccione **Actualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualizar lista de entidades](./media/18RefreshEntityList.png)

<span data-ttu-id="db5cd-177">A actualización tardará aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="db5cd-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="db5cd-178">Recibirá unha alerta cando remate.</span><span class="sxs-lookup"><span data-stu-id="db5cd-178">You will receive an alert when it is complete.</span></span>

![Actualizar confirmación](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="db5cd-180">Executar mapas de escrita dual en Project Operations</span><span class="sxs-lookup"><span data-stu-id="db5cd-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="db5cd-181">No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="db5cd-182">En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións.**</span><span class="sxs-lookup"><span data-stu-id="db5cd-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="db5cd-183">Despois de seleccionar a ligazón, redirixiráselle á lista de entidades nas asignacións.</span><span class="sxs-lookup"><span data-stu-id="db5cd-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="db5cd-184">Inicie os mapas segundo se describe na seguinte táboa.</span><span class="sxs-lookup"><span data-stu-id="db5cd-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="db5cd-185">Asegúrese de seguir a secuencia como aparece na lista.</span><span class="sxs-lookup"><span data-stu-id="db5cd-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="db5cd-186">**Asignación de entidades**</span><span class="sxs-lookup"><span data-stu-id="db5cd-186">**Entity Map**</span></span> | <span data-ttu-id="db5cd-187">**Actualizar entidade**</span><span class="sxs-lookup"><span data-stu-id="db5cd-187">**Refresh entity**</span></span> | <span data-ttu-id="db5cd-188">**Sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="db5cd-188">**Initial sync**</span></span> | <span data-ttu-id="db5cd-189">**Padrón para a sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="db5cd-189">**Master for initial sync**</span></span> | <span data-ttu-id="db5cd-190">**Executar requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="db5cd-190">**Run prerequisites**</span></span> | <span data-ttu-id="db5cd-191">**Sincronización inicial de requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="db5cd-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="db5cd-192">**Roles de recursos do proxecto para todas as empresas (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="db5cd-193">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-193">No</span></span> | <span data-ttu-id="db5cd-194">Si</span><span class="sxs-lookup"><span data-stu-id="db5cd-194">Yes</span></span> | <span data-ttu-id="db5cd-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="db5cd-195">Common Data Service</span></span> | <span data-ttu-id="db5cd-196">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-196">No</span></span> | <span data-ttu-id="db5cd-197">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-197">N\A</span></span> |
| <span data-ttu-id="db5cd-198">**Entidades legais (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="db5cd-199">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-199">No</span></span> | <span data-ttu-id="db5cd-200">Si</span><span class="sxs-lookup"><span data-stu-id="db5cd-200">Yes</span></span> | <span data-ttu-id="db5cd-201">Aplicacións de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="db5cd-201">Finance and Operations apps</span></span> | <span data-ttu-id="db5cd-202">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-202">No</span></span> | <span data-ttu-id="db5cd-203">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-203">N\A</span></span> |
| <span data-ttu-id="db5cd-204">**Datos reais de integración de Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="db5cd-205">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-205">No</span></span> | <span data-ttu-id="db5cd-206">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-206">No</span></span> | <span data-ttu-id="db5cd-207">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-207">N\A</span></span> | <span data-ttu-id="db5cd-208">Si</span><span class="sxs-lookup"><span data-stu-id="db5cd-208">Yes</span></span> | <span data-ttu-id="db5cd-209">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-209">No</span></span> |
| <span data-ttu-id="db5cd-210">**Liñas de contrato de proxecto (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="db5cd-211">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-211">No</span></span> | <span data-ttu-id="db5cd-212">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-212">No</span></span> | <span data-ttu-id="db5cd-213">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-213">N\A</span></span> | <span data-ttu-id="db5cd-214">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-214">No</span></span> | <span data-ttu-id="db5cd-215">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-215">No</span></span> |
| <span data-ttu-id="db5cd-216">**Entidade de integración para as relacións de transaccións do proxecto (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="db5cd-217">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-217">No</span></span> | <span data-ttu-id="db5cd-218">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-218">No</span></span> | <span data-ttu-id="db5cd-219">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-219">N\A</span></span> | <span data-ttu-id="db5cd-220">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-220">No</span></span> | <span data-ttu-id="db5cd-221">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-221">N\A</span></span> |
| <span data-ttu-id="db5cd-222">**Fitos da liña de contrato de integración de Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="db5cd-223">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-223">No</span></span> | <span data-ttu-id="db5cd-224">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-224">No</span></span> | <span data-ttu-id="db5cd-225">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-225">N\A</span></span> | <span data-ttu-id="db5cd-226">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-226">No</span></span> | <span data-ttu-id="db5cd-227">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-227">N\A</span></span> |
| <span data-ttu-id="db5cd-228">**Entidade de integración de Project Operations para estimacións de gastos (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="db5cd-229">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-229">No</span></span> | <span data-ttu-id="db5cd-230">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-230">No</span></span> | <span data-ttu-id="db5cd-231">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-231">N\A</span></span> | <span data-ttu-id="db5cd-232">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-232">No</span></span> | <span data-ttu-id="db5cd-233">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-233">N\A</span></span> |
| <span data-ttu-id="db5cd-234">**Entidade de exportación de categorías de gastos de proxecto de integración de Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="db5cd-235">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-235">No</span></span> | <span data-ttu-id="db5cd-236">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-236">No</span></span> | <span data-ttu-id="db5cd-237">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-237">N\A</span></span> | <span data-ttu-id="db5cd-238">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-238">No</span></span> | <span data-ttu-id="db5cd-239">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-239">N\A</span></span> |
| <span data-ttu-id="db5cd-240">**Entidade de exportación de gastos de proxecto de integración de Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="db5cd-241">Si</span><span class="sxs-lookup"><span data-stu-id="db5cd-241">Yes</span></span> | <span data-ttu-id="db5cd-242">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-242">No</span></span> | <span data-ttu-id="db5cd-243">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-243">N\A</span></span> | <span data-ttu-id="db5cd-244">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-244">No</span></span> | <span data-ttu-id="db5cd-245">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-245">N\A</span></span> |
| <span data-ttu-id="db5cd-246">**Entidade de integración de Project Operations para estimacións de horas (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="db5cd-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="db5cd-247">Si</span><span class="sxs-lookup"><span data-stu-id="db5cd-247">Yes</span></span> | <span data-ttu-id="db5cd-248">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-248">No</span></span> | <span data-ttu-id="db5cd-249">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-249">N\A</span></span> | <span data-ttu-id="db5cd-250">No</span><span class="sxs-lookup"><span data-stu-id="db5cd-250">No</span></span> | <span data-ttu-id="db5cd-251">N\A</span><span class="sxs-lookup"><span data-stu-id="db5cd-251">N\A</span></span> |


4. <span data-ttu-id="db5cd-252">Para actualizar a entidade, seleccione o nome do mapa e logo seleccione **Actualizar entidades**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualizar mapa](./media/20RefreshMapping.png)

5. <span data-ttu-id="db5cd-254">Ao finalizar a actualización, execute o mapa.</span><span class="sxs-lookup"><span data-stu-id="db5cd-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="db5cd-255">Antes de activar o seguinte mapa, verifique que o mapa da táboa estea en estado de **Execución**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="db5cd-256">A execución de mapas cun maior número de requisitos previos pode levar moito tempo.</span><span class="sxs-lookup"><span data-stu-id="db5cd-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="db5cd-257">Para executar un mapa con requisitos previos, active o conmutador **Mostrar mapas de entidades relacionadas**.</span><span class="sxs-lookup"><span data-stu-id="db5cd-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="db5cd-258">Se a táboa indica **Sincronización inicial de requisitos previos** é **Non**, verifique que o indicador **Sincronización inicial** está **Desactivado** en todos os mapas de requisitos previos antes de executalo.</span><span class="sxs-lookup"><span data-stu-id="db5cd-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar mapa](./media/21RunMap.png)

6. <span data-ttu-id="db5cd-260">Valide que todos os mapas relacionados co proxecto están en estado de execución.</span><span class="sxs-lookup"><span data-stu-id="db5cd-260">Validate all project related maps are in the running state.</span></span>

![Todos os mapas en execución](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="db5cd-262">Aplicar os datos de configuración en CDS para Project Operations (opcional)</span><span class="sxs-lookup"><span data-stu-id="db5cd-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="db5cd-263">Se aplicou datos de demostración ao ambiente de Finance, consulte [Configurar e aplicar os datos de configuración en Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar datos de demostración ao ambiente de CDS.</span><span class="sxs-lookup"><span data-stu-id="db5cd-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="db5cd-264">O seu ambiente de Project Operations agora está subministrado e configurado.</span><span class="sxs-lookup"><span data-stu-id="db5cd-264">Your Project Operations environment is now provisioned and configured.</span></span> 
