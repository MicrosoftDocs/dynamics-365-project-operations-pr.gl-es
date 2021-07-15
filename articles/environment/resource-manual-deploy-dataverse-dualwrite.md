---
title: Despregar manualmente a aplicación Project Operations Dataverse con soporte de escrita dual
description: Este tema explica como despregar manualmente a aplicación Project Operations Dataverse para que admita a escrita dual.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274006"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="a6367-103">Despregar manualmente a aplicación Project Operations Dataverse con soporte de escrita dual</span><span class="sxs-lookup"><span data-stu-id="a6367-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="a6367-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="a6367-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a6367-105">Este tema explica como despregar manualmente Microsoft Dynamics 365 Project Operations en Microsoft Dataverse para que admita a escrita dual.</span><span class="sxs-lookup"><span data-stu-id="a6367-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="a6367-106">Project Operations detecta a configuración do ambiente e engade soporte adicional para a escritura dual se se cumpren os requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="a6367-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="a6367-107">Durante o despregamento a través de Microsoft Dynamics Lifecycle Services (LCS), se seguiu as instrucións deste tema, podes omitir o despregamento da integración de Microsoft Power Platform (anteriormente coñecida como o ambiente de Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="a6367-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="a6367-108">O proceso de despregamento de Project Operations en Dataverse para que admita a escrita dual ten catro pasos principais:</span><span class="sxs-lookup"><span data-stu-id="a6367-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="a6367-109">[Cree un novo ambiente en Dataverse que admita a escrita dual](#create).</span><span class="sxs-lookup"><span data-stu-id="a6367-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="a6367-110">[Engada requisitos previos de escrita dual ao ambiente](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="a6367-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="a6367-111">[Engada a aplicación Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="a6367-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="a6367-112">[Ligue os seus ambientes](#link).</span><span class="sxs-lookup"><span data-stu-id="a6367-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="a6367-113">Crear un novo ambiente en Dataverse que admita a escrita dual</span><span class="sxs-lookup"><span data-stu-id="a6367-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="a6367-114">Para completar este procedemento, debe iniciar sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="a6367-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="a6367-115">Abra o [centro de administración de Power Platform](https://admin.powerplatform.com) e inicie sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="a6367-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="a6367-116">Cree un novo ambiente e noméeo.</span><span class="sxs-lookup"><span data-stu-id="a6367-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="a6367-117">Seleccione o tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="a6367-117">Select the environment type.</span></span> <span data-ttu-id="a6367-118">Se se rexistrou para a oferta de proba, seleccione **Proba (baseada en subscrición)**.</span><span class="sxs-lookup"><span data-stu-id="a6367-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="a6367-119">Confirme a rexión de despregamento.</span><span class="sxs-lookup"><span data-stu-id="a6367-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="a6367-120">Active a opción **Crear unha base de datos para este ambiente**.</span><span class="sxs-lookup"><span data-stu-id="a6367-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="a6367-121">Confirme o idioma e, a seguir, confirme que a moeda coincide coa moeda para as súas aplicacións de Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6367-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="a6367-122">Active a opción **Aplicacións de Dynamics 365** e confirme que o campo **Despregar automaticamente estas aplicacións** está definido como **Ningunha**.</span><span class="sxs-lookup"><span data-stu-id="a6367-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="a6367-123">Engada un grupo de seguranza, se é necesario un grupo de seguranza.</span><span class="sxs-lookup"><span data-stu-id="a6367-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="a6367-124">Seleccione **Gardar** para crear o ambiente.</span><span class="sxs-lookup"><span data-stu-id="a6367-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="a6367-125">Agarde a que se complete o despregamento e o ambiente chegue ao estado **Listo**.</span><span class="sxs-lookup"><span data-stu-id="a6367-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="a6367-126">Engadir requisitos previos de escrita dual ao ambiente</span><span class="sxs-lookup"><span data-stu-id="a6367-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="a6367-127">A compatibilidade coa escrita dual inclúe campos adicionais que se engaden a entidades clave, como a entidade **Empresa**.</span><span class="sxs-lookup"><span data-stu-id="a6367-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="a6367-128">Se está engadindo compatibilidade con escrita dual a un ambiente existente, pode que teña que actualizar os datos para activar a compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="a6367-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="a6367-129">Para obter información sobre como facer o bootstrap dos datos, consulte [Facer bootstrap dos datos da empresa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="a6367-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="a6367-130">Para obter máis información sobre a escrita dual, consulte [Requisitos do sistema de escrita dual](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="a6367-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="a6367-131">Complete este procedemento para engadir os requisitos previos de escrita dual ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="a6367-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="a6367-132">Abra o ambiente que acaba de crear e logo vaia a **Recurso** \> **Aplicacións de Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a6367-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="a6367-133">Seleccione **Solución principal de escrita dual** na lista de aplicacións e instálea.</span><span class="sxs-lookup"><span data-stu-id="a6367-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="a6367-134">Agarde ata que finalice a instalación.</span><span class="sxs-lookup"><span data-stu-id="a6367-134">Wait until the installation is completed.</span></span> <span data-ttu-id="a6367-135">Logo seleccione **Solución de orquestración de escrita dual** na lista de aplicacións e instálea.</span><span class="sxs-lookup"><span data-stu-id="a6367-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="a6367-136">Engadir a aplicación Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="a6367-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="a6367-137">Só pode completar este procedemento se completou os procedementos anteriores antes de instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a6367-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="a6367-138">Durante a instalación, o sistema analiza a configuración do ambiente e engade compatibilidade con escrita dual se é necesario.</span><span class="sxs-lookup"><span data-stu-id="a6367-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="a6367-139">Abra o ambiente que creou antes e logo vaia a **Recurso** \> **Aplicacións de Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a6367-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="a6367-140">Seleccione **Microsoft Dynamics 365 Project Operations** na lista de aplicacións e instálea.</span><span class="sxs-lookup"><span data-stu-id="a6367-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="a6367-141">Ligar os seus ambientes</span><span class="sxs-lookup"><span data-stu-id="a6367-141">Link your environments</span></span>

<span data-ttu-id="a6367-142">Despois do despregamento de Dataverse, pode configurar a ligazón nas súas aplicacións de Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6367-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="a6367-143">Siga os pasos indicados en [Usar asistente de escrita dual para ligar os seus ambientes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="a6367-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
