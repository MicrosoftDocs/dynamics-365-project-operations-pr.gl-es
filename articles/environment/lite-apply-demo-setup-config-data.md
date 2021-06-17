---
title: Aplicar datos de instalación e configuración da demostración - lite
description: Este tema ofrece información sobre como aplicar os datos de instalación e configuración da demostración para Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997149"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="3dd7b-103">Aplicar a configuración de demostración e os datos de configuración para Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="3dd7b-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="3dd7b-104">_\*\*Despregamento de Lite - oferta para facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="3dd7b-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="3dd7b-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3dd7b-105">Prerequisites</span></span>

<span data-ttu-id="3dd7b-106">Antes de comezar a configuración, debe ter un ambiente de Common Data Service (CDS) subministrado para Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="3dd7b-107">Instrucións</span><span class="sxs-lookup"><span data-stu-id="3dd7b-107">Instructions</span></span>

1. <span data-ttu-id="3dd7b-108">Descargue o [Paquete de datos mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="3dd7b-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="3dd7b-109">Desprácese ata o cartafol *ProjOpsSampleSetupData - CE only CMT* e execute o ficheiro executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="3dd7b-110">Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migración da configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="3dd7b-112">Na páxina 2 do asistente de CMT, seleccione **Microsoft 365** como o **Tipo de despregamento**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="3dd7b-113">Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="3dd7b-114">Seleccione a rexión do seu arrendatario, introduza as súas credenciais e logo seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="3dd7b-116">Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e logo seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="3dd7b-117">Na páxina 4, seleccione o ficheiro zip *SampleSetupAndConfigData* dende o cartafol desempaquetado, *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Ficheiro ZIP](./media/3ZipFile.png)

   ![Seleccionar un ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="3dd7b-120">Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="3dd7b-122">A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="3dd7b-123">Cando finalice, saia do asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="3dd7b-124">Comprobe se a súa organización ten datos nas seguintes 18 entidades:</span><span class="sxs-lookup"><span data-stu-id="3dd7b-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="3dd7b-125">Moeda</span><span class="sxs-lookup"><span data-stu-id="3dd7b-125">Currency</span></span>
    -   <span data-ttu-id="3dd7b-126">Conta</span><span class="sxs-lookup"><span data-stu-id="3dd7b-126">Account</span></span>
    -   <span data-ttu-id="3dd7b-127">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="3dd7b-127">Organizational Unit</span></span>
    -   <span data-ttu-id="3dd7b-128">Contacto</span><span class="sxs-lookup"><span data-stu-id="3dd7b-128">Contact</span></span>
    -   <span data-ttu-id="3dd7b-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="3dd7b-129">Unit</span></span>
    -   <span data-ttu-id="3dd7b-130">Grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="3dd7b-130">Unit Group</span></span>
    -   <span data-ttu-id="3dd7b-131">Lista de prezos</span><span class="sxs-lookup"><span data-stu-id="3dd7b-131">Price List</span></span>
    -   <span data-ttu-id="3dd7b-132">Lista de prezos do parámetro do proxecto</span><span class="sxs-lookup"><span data-stu-id="3dd7b-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="3dd7b-133">Frecuencia da factura</span><span class="sxs-lookup"><span data-stu-id="3dd7b-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="3dd7b-134">Categoría de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="3dd7b-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="3dd7b-135">Categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="3dd7b-135">Transaction Category</span></span>
    -   <span data-ttu-id="3dd7b-136">Categoría de gasto</span><span class="sxs-lookup"><span data-stu-id="3dd7b-136">Expense Category</span></span>
    -   <span data-ttu-id="3dd7b-137">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="3dd7b-137">Role Price</span></span>
    -   <span data-ttu-id="3dd7b-138">Prezo da categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="3dd7b-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="3dd7b-139">Característica</span><span class="sxs-lookup"><span data-stu-id="3dd7b-139">Characteristic</span></span>
    -   <span data-ttu-id="3dd7b-140">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="3dd7b-140">Bookable Resource</span></span>
    -   <span data-ttu-id="3dd7b-141">Asociación de categorías de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="3dd7b-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="3dd7b-142">Característica de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="3dd7b-142">Bookable Resource Characteristic</span></span>

    ![Completar importación](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
