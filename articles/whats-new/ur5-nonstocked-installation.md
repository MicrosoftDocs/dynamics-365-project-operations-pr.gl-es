---
title: Actualizar Project Operations no seu ambiente de Finance
description: Este tema ofrece información sobre como actualizar Project Operations no seu ambiente de Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816623"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="c1ca8-103">Actualizar Project Operations no seu ambiente de Finance</span><span class="sxs-lookup"><span data-stu-id="c1ca8-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="c1ca8-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="c1ca8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="c1ca8-105">Este tema ofrece información sobre como actualizar Dynamics 365 Project Operations no seu ambiente de Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="c1ca8-106">Hai tres procedementos necesarios para actualizar Project Operations á actualización 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="c1ca8-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="c1ca8-107">Importar o paquete ao seu proxecto de previsualización</span><span class="sxs-lookup"><span data-stu-id="c1ca8-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="c1ca8-108">Aplicar a actualización</span><span class="sxs-lookup"><span data-stu-id="c1ca8-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="c1ca8-109">Actualizar o seu ambiente de Dataverse</span><span class="sxs-lookup"><span data-stu-id="c1ca8-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="c1ca8-110">Importar o paquete ao seu proxecto de LCS</span><span class="sxs-lookup"><span data-stu-id="c1ca8-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="c1ca8-111">Iniciar sesión en [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como propietario do proxecto ou xestor do ambiente.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="c1ca8-112">Na lista de proxectos, seleccione o seu proxecto de LCS.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="c1ca8-113">Na páxina **Proxecto**, no grupo **Ambientes**, abra o ambiente que desexe actualizar.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="c1ca8-114">Verifique que o ambiente se está a executar.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-114">Verify that the environment is running.</span></span> <span data-ttu-id="c1ca8-115">Se non se inicia, inicie o ambiente.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="c1ca8-116">Na sección **Nova versión** en **Actualizacións dispoñibles**, seleccione **Ver actualización** para 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Botón de ver actualización](media/view-update.png)

6. <span data-ttu-id="c1ca8-118">Na páxina **Actualizacións binarias**, seleccione **Gardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="c1ca8-119">Na páxina **Revisar e gardar actualizacións**, seleccione **Gardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="c1ca8-120">No panel **Gardar paquete na biblioteca de activos** que se abre, introduza o nome do paquete e logo seleccione **Gardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="c1ca8-121">Cando LCS remate de gardar o paquete, actívase o botón **Feito**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="c1ca8-122">Seleccione **Feito**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-122">Select **Done**.</span></span> <span data-ttu-id="c1ca8-123">LCS verificará o paquete.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-123">LCS will verify the package.</span></span> <span data-ttu-id="c1ca8-124">A verificación pode levar uns minutos ou ata unha hora.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="c1ca8-125">Aplicar a actualización do paquete</span><span class="sxs-lookup"><span data-stu-id="c1ca8-125">Apply the package update</span></span>

1. <span data-ttu-id="c1ca8-126">En LCS, na páxina **Detalles do ambiente**, seleccione **Manter** > **Aplicar actualizacións**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="c1ca8-127">Na lista, seleccione o paquete que gardou anteriormente e logo seleccione **Solicitar**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="c1ca8-128">Seleccione **Si** para confirmar que desexa despregar o paquete.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Caixa de diálogo de confirmar o despregamento do paquete](media/confirm-package-deployment.png)

4. <span data-ttu-id="c1ca8-130">Seleccione **Si** para confirmar que desexa actualizar a aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Caixa de diálogo de confirmar a actualización da aplicación](media/confirm-application-update.png)

<span data-ttu-id="c1ca8-132">Comezará o despregamento e a actualización da aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="c1ca8-133">Na páxina **Detalles do ambiente**, na esquina superior dereita, o estado do ambiente actualizarase a **Mantemento**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="c1ca8-134">En aproximadamente dúas horas, a actualización estará completa.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="c1ca8-135">A información da versión da aplicación actualizarase a **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** e o estado do ambiente actualizarase a **Despregado**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="c1ca8-136">Actualizar o seu ambiente de Dataverse</span><span class="sxs-lookup"><span data-stu-id="c1ca8-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="c1ca8-137">Inicie sesión no [Centro de administración de Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="c1ca8-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="c1ca8-138">Na lista, busque e abra o ambiente que utilizou para instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="c1ca8-139">Na páxina **Ambientes**, seleccione **Recurso** > **Aplicacións de Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="c1ca8-140">Na lista, localice **Microsoft Dynamics 365 Project Operations**, e na columna **Estado**, seleccione **Actualización dispoñible**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="c1ca8-141">Seleccione a caixa de verificación **Acepto as condicións do servizo** e logo seleccione **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="c1ca8-142">Instalarase a versión máis recente da solución.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="c1ca8-143">Despois de completar a instalación, terá instalada a versión 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="c1ca8-144">Configurar novas funcionalidades</span><span class="sxs-lookup"><span data-stu-id="c1ca8-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="c1ca8-145">Activar a asignación de escrita dual</span><span class="sxs-lookup"><span data-stu-id="c1ca8-145">Enable dual-write mapping</span></span>

<span data-ttu-id="c1ca8-146">Despois de completar a actualización nos ambiente de Finance e Dataverse, pode activar as asignacións de escritura dual requiridas.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="c1ca8-147">Complete os seguintes procedementos para activar as asignacións de escritura dual.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="c1ca8-148">Actualice a configuración de seguridade no ambiente de Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="c1ca8-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="c1ca8-149">Actualizar entidades de datos</span><span class="sxs-lookup"><span data-stu-id="c1ca8-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="c1ca8-150">Actualizar e executar as asignacións de escritura dual</span><span class="sxs-lookup"><span data-stu-id="c1ca8-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="c1ca8-151">Actualizar a configuración de seguridade no ambiente de Dataverse</span><span class="sxs-lookup"><span data-stu-id="c1ca8-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="c1ca8-152">As seguintes actualizacións dos privilexios de seguridade para entidades son necesarias como parte da actualización a UR5.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="c1ca8-153">No seu ambiente de Dataverse, vaia a **Configuración**, e no grupo **Sistema**, seleccione **Seguridade**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Configuración de ambientes de Dataverse](media/Picture21.png)

2. <span data-ttu-id="c1ca8-155">Seleccionar **Roles de seguranza**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="c1ca8-156">Na lista de roles, seleccione **usuario de aplicación de escritura dual** e seleccione o separador **Entidades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="c1ca8-157">Comprobe que o rol ten os permisos de **Ler** e **Anexar a** para:</span><span class="sxs-lookup"><span data-stu-id="c1ca8-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="c1ca8-158">**Tipo de taxa de cambio de divisas**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="c1ca8-159">**Gráfica de contas**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="c1ca8-160">**Calendario fiscal**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="c1ca8-161">**Libro maior**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-161">**Ledger**</span></span>

5. <span data-ttu-id="c1ca8-162">Despois de actualizar o rol de seguranza, vaia a **Configuración** > **Seguridade** > **Equipos**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="c1ca8-163">Verifique que o rol **usuario de aplicación de escritura dual** se aplicou ao equipo.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="c1ca8-164">Actualizar as entidades de datos desde a actualización</span><span class="sxs-lookup"><span data-stu-id="c1ca8-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="c1ca8-165">No seu ambiente de Finance, abra a área de traballo **Xestión de datos** e logo abra a páxina **Parámetros marco**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="c1ca8-166">No separador **Configuración da entidade**, seleccione **Actualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="c1ca8-167">Seleccione **Pechar** para confirmar a actualización da entidade.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="c1ca8-168">Este proceso pode tardar aproximadamente 20 minutos en completarse.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="c1ca8-169">Recibirá unha notificación cando remate a actualización.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="c1ca8-170">Actualizar asignacións de escrita dual</span><span class="sxs-lookup"><span data-stu-id="c1ca8-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="c1ca8-171">Na área de traballo **Xestión de datos**, seleccione **Escritura dual**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="c1ca8-172">Seleccione **Aplicar solucións**, seleccione ambas solucións da lista e logo seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="c1ca8-173">Na páxina **Escritura dual**, seleccione os seguintes mapas da táboa e logo seleccione **Parar**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="c1ca8-174">**Datos reais de integración de Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="c1ca8-175">**Categorías de gastos do proxecto de integración de Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="c1ca8-176">**Entidade de exportación de gastos do proxecto de datos reais de integración de Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="c1ca8-177">Na páxina **Versión do mapa de táboas**, aplique unha nova versión do mapa a cada unha das tres entidades.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="c1ca8-178">Na páxina **Escritura dual**, seleccione executar para reiniciar os mapas.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="c1ca8-179">Na lista de mapas, seleccione o papa de **Libro maior (msdyn_ledgers)** con todos os requisitos previos e seleccione a caixa de verificación **Sincronización inicial**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="c1ca8-180">No campo **Padrón para a sincronización inicial**, seleccione **aplicacións de Finance and Operations** e logo seleccione **Executar**.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sincronización de mapa de libro maior](media/DW6.png)
 
