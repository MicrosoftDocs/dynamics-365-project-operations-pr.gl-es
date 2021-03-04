---
title: Aplicar datos de instalación e configuración da demostración - lite
description: Este tema ofrece información sobre como aplicar os datos de instalación e configuración da demostración para Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089117"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="25f30-103">Aplicar a configuración de demostración e os datos de configuración para Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="25f30-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="25f30-104">_\*\*Despregamento de Lite - oferta para facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="25f30-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="25f30-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25f30-105">Prerequisites</span></span>

<span data-ttu-id="25f30-106">Antes de comezar a configuración, debe ter un ambiente de Common Data Service (CDS) subministrado para Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="25f30-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="25f30-107">Instrucións</span><span class="sxs-lookup"><span data-stu-id="25f30-107">Instructions</span></span>

1. <span data-ttu-id="25f30-108">Descargue o [Paquete de datos mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="25f30-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="25f30-109">Vaia ao cartafol *ProjOpsDemoDataSetupAndMaster - Integrated CMT* e execute o ficheiro executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="25f30-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="25f30-110">Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="25f30-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migración da configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="25f30-112">Na páxina 2 do asistente de CMT, seleccione **Microsoft 365** como o **Tipo de despregamento**.</span><span class="sxs-lookup"><span data-stu-id="25f30-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="25f30-113">Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.</span><span class="sxs-lookup"><span data-stu-id="25f30-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="25f30-114">Seleccione a rexión do seu arrendatario, introduza as súas credenciais e logo seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="25f30-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="25f30-116">Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e logo seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="25f30-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="25f30-117">Na páxina 4, seleccione o ficheiro zip *MasterAndSetupData* desde o cartafol desempaquetado, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="25f30-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Ficheiro ZIP](./media/3ZipFile.png)

   ![Seleccionar un ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="25f30-120">Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="25f30-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="25f30-122">A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="25f30-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="25f30-123">Cando finalice, saia do asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="25f30-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="25f30-124">Comprobe se a súa organización ten datos nas seguintes 20 entidades:</span><span class="sxs-lookup"><span data-stu-id="25f30-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="25f30-125">Moeda</span><span class="sxs-lookup"><span data-stu-id="25f30-125">Currency</span></span>
    -   <span data-ttu-id="25f30-126">Conta</span><span class="sxs-lookup"><span data-stu-id="25f30-126">Account</span></span>
    -   <span data-ttu-id="25f30-127">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="25f30-127">Organizational Unit</span></span>
    -   <span data-ttu-id="25f30-128">Contacto</span><span class="sxs-lookup"><span data-stu-id="25f30-128">Contact</span></span>
    -   <span data-ttu-id="25f30-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="25f30-129">Unit</span></span>
    -   <span data-ttu-id="25f30-130">Grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="25f30-130">Unit Group</span></span>
    -   <span data-ttu-id="25f30-131">Lista de prezos</span><span class="sxs-lookup"><span data-stu-id="25f30-131">Price List</span></span>
    -   <span data-ttu-id="25f30-132">Lista de prezos do parámetro do proxecto</span><span class="sxs-lookup"><span data-stu-id="25f30-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="25f30-133">Frecuencia da factura</span><span class="sxs-lookup"><span data-stu-id="25f30-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="25f30-134">Categoría de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="25f30-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="25f30-135">Categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="25f30-135">Transaction Category</span></span>
    -   <span data-ttu-id="25f30-136">Categoría de gasto</span><span class="sxs-lookup"><span data-stu-id="25f30-136">Expense Category</span></span>
    -   <span data-ttu-id="25f30-137">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="25f30-137">Role Price</span></span>
    -   <span data-ttu-id="25f30-138">Prezo da categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="25f30-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="25f30-139">Característica</span><span class="sxs-lookup"><span data-stu-id="25f30-139">Characteristic</span></span>
    -   <span data-ttu-id="25f30-140">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="25f30-140">Bookable Resource</span></span>
    -   <span data-ttu-id="25f30-141">Asociación de categorías de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="25f30-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="25f30-142">Característica de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="25f30-142">Bookable Resource Characteristic</span></span>

    ![Completar importación](./media/6CompleteImport.png)
