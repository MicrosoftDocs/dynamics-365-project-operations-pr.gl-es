---
title: Configurar e aplicar datos de configuración en Common Data Service
description: Este tema ofrece información sobre como configurar e aplicar os datos de configuración en Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642226"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="21bf9-103">Configurar e aplicar datos de configuración en Common Data Service</span><span class="sxs-lookup"><span data-stu-id="21bf9-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="21bf9-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="21bf9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="21bf9-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="21bf9-105">Prerequisites</span></span>

<span data-ttu-id="21bf9-106">Antes de comezar a configurar datos en Common Data Service (CDS), deben cumprirse os seguintes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="21bf9-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="21bf9-107">Proporcionar un ambiente de CDS e un ambiente de Dynamics 365 Finance ambiente para Project Operations.</span><span class="sxs-lookup"><span data-stu-id="21bf9-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="21bf9-108">A información da entidade legal de Dynamics 365 Finance compártese co ambiente de CDS.</span><span class="sxs-lookup"><span data-stu-id="21bf9-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="21bf9-109">Isto significa que a entidade **Empresa** en CDS ten os seguintes rexistros da empresa:</span><span class="sxs-lookup"><span data-stu-id="21bf9-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="21bf9-110">THPM</span><span class="sxs-lookup"><span data-stu-id="21bf9-110">THPM</span></span>
  - <span data-ttu-id="21bf9-111">USPM</span><span class="sxs-lookup"><span data-stu-id="21bf9-111">USPM</span></span>
  - <span data-ttu-id="21bf9-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="21bf9-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="21bf9-113">Instale os datos de configuración</span><span class="sxs-lookup"><span data-stu-id="21bf9-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="21bf9-114">Descargue, desbloquee e descomprima o ficheiro [Paquete de datos de instalación e configuración](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="21bf9-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="21bf9-115">Vaia ao cartafol descomprimido e execute o ficheiro executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="21bf9-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="21bf9-116">Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración da configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="21bf9-118">Na páxina 2 do asistente de CMT, seleccione **Microsoft 365** como o **Tipo de despregamento**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="21bf9-119">Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="21bf9-120">Seleccione a rexión do seu arrendatario, introduza as súas credenciais e seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="21bf9-122">Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="21bf9-123">Na páxina 4, seleccione o ficheiro zip, *SampleSetupAndConfigData* do cartafol descomprimido.</span><span class="sxs-lookup"><span data-stu-id="21bf9-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selección de ficheiro Zip](./media/3ZipFile.png)

![Seleccionar un ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="21bf9-126">Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-126">After the zip file is selected, select **Import Data**.</span></span>

![Datos de importación](./media/5ImportData.png)

10. <span data-ttu-id="21bf9-128">A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="21bf9-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="21bf9-129">Cando finalice a importación, saia do asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="21bf9-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="21bf9-130">Comprobe se a súa organización ten datos nas seguintes 19 entidades:</span><span class="sxs-lookup"><span data-stu-id="21bf9-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="21bf9-131">Moeda</span><span class="sxs-lookup"><span data-stu-id="21bf9-131">Currency</span></span>
  - <span data-ttu-id="21bf9-132">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="21bf9-132">Organizational Unit</span></span>
  - <span data-ttu-id="21bf9-133">Contacto</span><span class="sxs-lookup"><span data-stu-id="21bf9-133">Contact</span></span>
  - <span data-ttu-id="21bf9-134">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="21bf9-134">Tax Group</span></span>
  - <span data-ttu-id="21bf9-135">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="21bf9-135">Customer Group</span></span>
  - <span data-ttu-id="21bf9-136">Unidade</span><span class="sxs-lookup"><span data-stu-id="21bf9-136">Unit</span></span>
  - <span data-ttu-id="21bf9-137">Grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="21bf9-137">Unit Group</span></span>
  - <span data-ttu-id="21bf9-138">Lista de prezos</span><span class="sxs-lookup"><span data-stu-id="21bf9-138">Price List</span></span>
  - <span data-ttu-id="21bf9-139">Lista de prezos do parámetro do proxecto</span><span class="sxs-lookup"><span data-stu-id="21bf9-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="21bf9-140">Frecuencia da factura</span><span class="sxs-lookup"><span data-stu-id="21bf9-140">Invoice Frequency</span></span>
  - <span data-ttu-id="21bf9-141">Categoría de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="21bf9-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="21bf9-142">Categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="21bf9-142">Transaction Category</span></span>
  - <span data-ttu-id="21bf9-143">Categoría de gasto</span><span class="sxs-lookup"><span data-stu-id="21bf9-143">Expense Category</span></span>
  - <span data-ttu-id="21bf9-144">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="21bf9-144">Role Price</span></span>
  - <span data-ttu-id="21bf9-145">Prezo da categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="21bf9-145">Transaction Category Price</span></span>
  - <span data-ttu-id="21bf9-146">Característica</span><span class="sxs-lookup"><span data-stu-id="21bf9-146">Characteristic</span></span>
  - <span data-ttu-id="21bf9-147">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="21bf9-147">Bookable Resource</span></span>
  - <span data-ttu-id="21bf9-148">Asociación de categorías de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="21bf9-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="21bf9-149">Característica de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="21bf9-149">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="21bf9-151">Actualiza as configuracións de Project Operations</span><span class="sxs-lookup"><span data-stu-id="21bf9-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="21bf9-152">Vaia ao ambiente de CE.</span><span class="sxs-lookup"><span data-stu-id="21bf9-152">Navigate to the CE environment.</span></span> <span data-ttu-id="21bf9-153">Podes atopalo abrindo o [Centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionando o ambiente e logo seleccionando **Ambiente aberto**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="21bf9-155">Vaia a **Proxectos** > **Recursos** e logo seleccione **Novo** para crear un recurso reservable para o seu usuario.</span><span class="sxs-lookup"><span data-stu-id="21bf9-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos reservables](./media/8BookableResources.png)

3. <span data-ttu-id="21bf9-157">No separador **Xeral**, seleccione o seu usuario administrador.</span><span class="sxs-lookup"><span data-stu-id="21bf9-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="21bf9-158">Verifique que o fuso horario coincide co fuso no que se atopa.</span><span class="sxs-lookup"><span data-stu-id="21bf9-158">Verify that the time zone matches the one you are in.</span></span> 

![Novo recurso reservable](./media/9NewBookableResource.png)

4. <span data-ttu-id="21bf9-160">No separador **Programación**, no campo **Empresa**, escolla a empresa **USPM** e seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Separador de programación](./media/10SchedulingTab.png)

5. <span data-ttu-id="21bf9-162">Prema o separador **Horas de traballo**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-162">Select the **Work hours** tab.</span></span>  

![Horas laborables](./media/11WorkHours.png)

6. <span data-ttu-id="21bf9-164">Prema dúas veces en calquera valor do calendario e seleccione **Editar** > **Todos os eventos da serie**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendario de traballo](./media/12WorkCalendar.png)

7. <span data-ttu-id="21bf9-166">Cambie as horas de traballo a un día de traballo de oito (8) horas, marque as fins de semana como días non laborables e asegúrese de que o fuso horario coincida co seu.</span><span class="sxs-lookup"><span data-stu-id="21bf9-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="21bf9-167">Seleccione **Gardar e pechar**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-167">Select **Save and close**.</span></span>

![Actualizar calendario](./media/13UpdateCalendar.png)

9. <span data-ttu-id="21bf9-169">Vaia a **Configuración** > **Modelos de calendario** e seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de calendario](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="21bf9-171">Insira un nome, seleccione o recurso do modelo que creou e logo seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Gardar modelo de calendario](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="21bf9-173">Vaia a **Parámetros** e faga dobre clic no rexistro.</span><span class="sxs-lookup"><span data-stu-id="21bf9-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parámetros do proxecto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="21bf9-175">Actualice os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="21bf9-175">Update the following fields:</span></span>

 - <span data-ttu-id="21bf9-176">**Empresa predefinida**: USPM</span><span class="sxs-lookup"><span data-stu-id="21bf9-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="21bf9-177">**Unidade organizativa predefinida**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="21bf9-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="21bf9-178">**Frecuencia de facturas**: Sétimo e último día</span><span class="sxs-lookup"><span data-stu-id="21bf9-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="21bf9-179">**Modelo de horas de traballo**: Cambie ao modelo que creou.</span><span class="sxs-lookup"><span data-stu-id="21bf9-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="21bf9-180">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="21bf9-180">Select **Save**.</span></span> 

![Parámetros do proxecto actualizados](./media/17UpdatedProjectParameters.png)
