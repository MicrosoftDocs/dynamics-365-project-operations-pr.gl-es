---
title: Aplicar datos de instalación e configuración da demostración
description: Este tema ofrece información sobre como aplicar os datos de instalación e configuración da demostración para Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075997"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="13cc4-103">Aplique os datos de instalación e configuración da demostración para o despregamento de Project Operations lite: oferta para facturación proforma</span><span class="sxs-lookup"><span data-stu-id="13cc4-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="13cc4-104">_\*\*Despregamento de Lite - oferta para facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="13cc4-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="13cc4-105">Descargue o [Paquete de datos mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="13cc4-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="13cc4-106">Vaia ao cartafol *ProjOpsDemoDataSetupAndMaster - Integrated CMT* e execute o ficheiro executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="13cc4-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="13cc4-107">Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="13cc4-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración da configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="13cc4-109">Na páxina 2 do asistente de CMT, seleccione **Microsoft 365** como o **Tipo de despregamento**.</span><span class="sxs-lookup"><span data-stu-id="13cc4-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="13cc4-110">Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.</span><span class="sxs-lookup"><span data-stu-id="13cc4-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="13cc4-111">Seleccione a rexión do seu arrendatario, introduza as súas credenciais e logo seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="13cc4-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="13cc4-113">Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e logo seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="13cc4-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="13cc4-114">Na páxina 4, seleccione o ficheiro zip *MasterAndSetupData* desde o cartafol desempaquetado, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="13cc4-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Ficheiro ZIP](./media/3ZipFile.png)

![Seleccionar un ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="13cc4-117">Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="13cc4-117">After the zip file is selected, select **Import Data**.</span></span>

![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="13cc4-119">A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="13cc4-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="13cc4-120">Cando finalice, saia do asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="13cc4-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="13cc4-121">Comprobe se a súa organización ten datos nas seguintes 20 entidades:</span><span class="sxs-lookup"><span data-stu-id="13cc4-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="13cc4-122">Moeda</span><span class="sxs-lookup"><span data-stu-id="13cc4-122">Currency</span></span>
- <span data-ttu-id="13cc4-123">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="13cc4-123">Organizational Unit</span></span>
- <span data-ttu-id="13cc4-124">Contacto</span><span class="sxs-lookup"><span data-stu-id="13cc4-124">Contact</span></span>
- <span data-ttu-id="13cc4-125">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="13cc4-125">Tax Group</span></span>
- <span data-ttu-id="13cc4-126">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="13cc4-126">Customer Group</span></span>
- <span data-ttu-id="13cc4-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="13cc4-127">Unit</span></span>
- <span data-ttu-id="13cc4-128">Grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="13cc4-128">Unit Group</span></span>
- <span data-ttu-id="13cc4-129">Lista de prezos</span><span class="sxs-lookup"><span data-stu-id="13cc4-129">Price List</span></span>
- <span data-ttu-id="13cc4-130">Lista de prezos do parámetro do proxecto</span><span class="sxs-lookup"><span data-stu-id="13cc4-130">Project Parameter Price List</span></span>
- <span data-ttu-id="13cc4-131">Frecuencia da factura</span><span class="sxs-lookup"><span data-stu-id="13cc4-131">Invoice Frequency</span></span>
- <span data-ttu-id="13cc4-132">Detalle da frecuencia da factura</span><span class="sxs-lookup"><span data-stu-id="13cc4-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="13cc4-133">Categoría de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="13cc4-133">Bookable Resource Category</span></span>
- <span data-ttu-id="13cc4-134">Categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="13cc4-134">Transaction Category</span></span>
- <span data-ttu-id="13cc4-135">Categoría de gasto</span><span class="sxs-lookup"><span data-stu-id="13cc4-135">Expense Category</span></span>
- <span data-ttu-id="13cc4-136">Prezo do rol</span><span class="sxs-lookup"><span data-stu-id="13cc4-136">Role Price</span></span>
- <span data-ttu-id="13cc4-137">Prezo da categoría da transacción</span><span class="sxs-lookup"><span data-stu-id="13cc4-137">Transaction Category Price</span></span>
- <span data-ttu-id="13cc4-138">Característica</span><span class="sxs-lookup"><span data-stu-id="13cc4-138">Characteristic</span></span>
- <span data-ttu-id="13cc4-139">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="13cc4-139">Bookable Resource</span></span>
- <span data-ttu-id="13cc4-140">Asociación de categorías de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="13cc4-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="13cc4-141">Característica de recursos reservables</span><span class="sxs-lookup"><span data-stu-id="13cc4-141">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)
