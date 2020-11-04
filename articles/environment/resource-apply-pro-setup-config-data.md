---
title: Configure e aplique a configuración no Common Data Service para Project Operations
description: Este tema ofrece información sobre como configurar e aplicar os datos de configuración en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076005"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="6209a-103">Configure e aplique a configuración no Common Data Service para Project Operations</span><span class="sxs-lookup"><span data-stu-id="6209a-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="6209a-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="6209a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="6209a-105">Instale os datos de configuración</span><span class="sxs-lookup"><span data-stu-id="6209a-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="6209a-106">Descargue, desbloquee e descomprima o ficheiro [Paquete de datos de instalación e configuración](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="6209a-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="6209a-107">Vaia ao cartafol descomprimido e execute o ficheiro executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="6209a-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="6209a-108">Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="6209a-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración da configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="6209a-110">Na páxina 2 do asistente de CMT, seleccione **Microsoft 365** como o **Tipo de despregamento**.</span><span class="sxs-lookup"><span data-stu-id="6209a-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="6209a-111">Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.</span><span class="sxs-lookup"><span data-stu-id="6209a-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="6209a-112">Seleccione a rexión do seu arrendatario, introduza as súas credenciais e seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="6209a-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="6209a-114">Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="6209a-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="6209a-115">Na páxina 4, seleccione o ficheiro zip, *SampleSetupAndConfigData* do cartafol descomprimido.</span><span class="sxs-lookup"><span data-stu-id="6209a-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selección de ficheiro Zip](./media/3ZipFile.png)

![Seleccionar un ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="6209a-118">Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="6209a-118">After the zip file is selected, select **Import Data**.</span></span>

![Datos de importación](./media/5ImportData.png)

10. <span data-ttu-id="6209a-120">A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="6209a-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="6209a-121">Cando finalice a importación, saia do asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="6209a-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="6209a-122">Comprobe se a súa organización ten datos nas seguintes 19 entidades:</span><span class="sxs-lookup"><span data-stu-id="6209a-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="6209a-123">Moeda</span><span class="sxs-lookup"><span data-stu-id="6209a-123">Currency</span></span>
  - <span data-ttu-id="6209a-124">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="6209a-124">Organizational Unit</span></span>
  - <span data-ttu-id="6209a-125">Contacto</span><span class="sxs-lookup"><span data-stu-id="6209a-125">Contact</span></span>
  - <span data-ttu-id="6209a-126">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="6209a-126">Tax Group</span></span>
  - <span data-ttu-id="6209a-127">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="6209a-127">Customer Group</span></span>
  - <span data-ttu-id="6209a-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="6209a-128">Unit</span></span>
  - <span data-ttu-id="6209a-129">Grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="6209a-129">Unit Group</span></span>
  - <span data-ttu-id="6209a-130">Lista de prezos</span><span class="sxs-lookup"><span data-stu-id="6209a-130">Price List</span></span>
  - <span data-ttu-id="6209a-131">Lista de prezos do parámetro do proxecto</span><span class="sxs-lookup"><span data-stu-id="6209a-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="6209a-132">Frecuencia da factura</span><span class="sxs-lookup"><span data-stu-id="6209a-132">Invoice Frequency</span></span>
  - <span data-ttu-id="6209a-133">Categoría de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="6209a-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="6209a-134">Categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="6209a-134">Transaction Category</span></span>
  - <span data-ttu-id="6209a-135">Categoría de gasto</span><span class="sxs-lookup"><span data-stu-id="6209a-135">Expense Category</span></span>
  - <span data-ttu-id="6209a-136">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="6209a-136">Role Price</span></span>
  - <span data-ttu-id="6209a-137">Prezo da categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="6209a-137">Transaction Category Price</span></span>
  - <span data-ttu-id="6209a-138">Característica</span><span class="sxs-lookup"><span data-stu-id="6209a-138">Characteristic</span></span>
  - <span data-ttu-id="6209a-139">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="6209a-139">Bookable Resource</span></span>
  - <span data-ttu-id="6209a-140">Asociación de categorías de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="6209a-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="6209a-141">Característica de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="6209a-141">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="6209a-143">Actualiza as configuracións de Project Operations</span><span class="sxs-lookup"><span data-stu-id="6209a-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="6209a-144">Vaia ao ambiente de CE.</span><span class="sxs-lookup"><span data-stu-id="6209a-144">Navigate to the CE environment.</span></span> <span data-ttu-id="6209a-145">Podes atopalo abrindo o [Centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionando o ambiente e logo seleccionando **Ambiente aberto**.</span><span class="sxs-lookup"><span data-stu-id="6209a-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="6209a-147">Vaia a **Proxectos** > **Recursos** e logo seleccione **Novo** para crear un recurso reservable para o seu usuario.</span><span class="sxs-lookup"><span data-stu-id="6209a-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos reservables](./media/8BookableResources.png)

3. <span data-ttu-id="6209a-149">No separador **Xeral** , seleccione o seu usuario administrador.</span><span class="sxs-lookup"><span data-stu-id="6209a-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="6209a-150">Verifique que o fuso horario coincide co fuso no que se atopa.</span><span class="sxs-lookup"><span data-stu-id="6209a-150">Verify that the time zone matches the one you are in.</span></span> 

![Novo recurso reservable](./media/9NewBookableResource.png)

4. <span data-ttu-id="6209a-152">No separador **Programación** , no campo **Empresa** , escolla a empresa **USPM** e seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="6209a-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Separador de programación](./media/10SchedulingTab.png)

5. <span data-ttu-id="6209a-154">Prema o separador **Horas de traballo**.</span><span class="sxs-lookup"><span data-stu-id="6209a-154">Select the **Work hours** tab.</span></span>  

![Horas laborables](./media/11WorkHours.png)

6. <span data-ttu-id="6209a-156">Prema dúas veces en calquera valor do calendario e seleccione **Editar** > **Todos os eventos da serie**.</span><span class="sxs-lookup"><span data-stu-id="6209a-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendario de traballo](./media/12WorkCalendar.png)

7. <span data-ttu-id="6209a-158">Cambie as horas de traballo a un día de traballo de oito (8) horas, marque as fins de semana como días non laborables e asegúrese de que o fuso horario coincida co seu.</span><span class="sxs-lookup"><span data-stu-id="6209a-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="6209a-159">Seleccione **Gardar e pechar**.</span><span class="sxs-lookup"><span data-stu-id="6209a-159">Select **Save and close**.</span></span>

![Actualizar calendario](./media/13UpdateCalendar.png)

9. <span data-ttu-id="6209a-161">Vaia a **Configuración** > **Modelos de calendario** e seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="6209a-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de calendario](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="6209a-163">Insira un nome, seleccione o recurso do modelo que creou e logo seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="6209a-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Gardar modelo de calendario](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="6209a-165">Vaia a **Parámetros** e faga dobre clic no rexistro.</span><span class="sxs-lookup"><span data-stu-id="6209a-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parámetros do proxecto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="6209a-167">Actualice os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="6209a-167">Update the following fields:</span></span>

 - <span data-ttu-id="6209a-168">**Empresa predefinida** : USPM</span><span class="sxs-lookup"><span data-stu-id="6209a-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="6209a-169">**Unidade organizativa predefinida** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="6209a-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="6209a-170">**Frecuencia de facturas** : Sétimo e último día</span><span class="sxs-lookup"><span data-stu-id="6209a-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="6209a-171">**Modelo de horas de traballo** : Cambie ao modelo que creou.</span><span class="sxs-lookup"><span data-stu-id="6209a-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="6209a-172">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="6209a-172">Select **Save**.</span></span> 

![Parámetros do proxecto actualizados](./media/17UpdatedProjectParameters.png)
