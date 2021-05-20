---
title: Engadir unha subscrición a Azure a un proxecto de LCS
description: Este tema ofrece información sobre como conectar a súa subscrición a Azure a un proxecto LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880536"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="31a27-103">Engadir unha subscrición a Azure a un proxecto de LCS</span><span class="sxs-lookup"><span data-stu-id="31a27-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="31a27-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="31a27-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="31a27-105">Os ambientes aloxados na nube deben despregarse mediante unha subscrición a Azure existente.</span><span class="sxs-lookup"><span data-stu-id="31a27-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="31a27-106">Este tema explica como conectar a súa subscrición a Azure existente a un proxecto LCS.</span><span class="sxs-lookup"><span data-stu-id="31a27-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="31a27-107">Outorgar o consentimento de administrador</span><span class="sxs-lookup"><span data-stu-id="31a27-107">Grant admin consent</span></span>

1. <span data-ttu-id="31a27-108">No seu proxecto LCS, na sección **Ambientes**, seleccione **Configuración de Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="31a27-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Configuración de Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="31a27-110">Na páxina **Configuración do proxecto**, no separador **Conectores de Azure**, seleccione **Autorizar**.</span><span class="sxs-lookup"><span data-stu-id="31a27-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="31a27-111">Isto permite despregar ambientes neste proxecto.</span><span class="sxs-lookup"><span data-stu-id="31a27-111">This allows environments to be deployed to this project.</span></span>

![Conectores de Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="31a27-113">Seleccione **Autorizar** de novo para proporcionar o consentimento do administrador.</span><span class="sxs-lookup"><span data-stu-id="31a27-113">Select **Authorize** again to provide admin consent.</span></span>

![Outorgar o consentimento de administrador](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="31a27-115">Acepte a solicitude de permisos.</span><span class="sxs-lookup"><span data-stu-id="31a27-115">Accept the permissions request.</span></span>

![Aceptar a solicitude de permisos](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="31a27-117">A autorización xa está completa.</span><span class="sxs-lookup"><span data-stu-id="31a27-117">The authorization is now complete.</span></span> 

![Autorización realizada correctamente](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="31a27-119">Proporcionar acceso a Dynamics Deployment Services para a súa subscrición a Azure</span><span class="sxs-lookup"><span data-stu-id="31a27-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="31a27-120">Vaia a [Facturación de Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e seleccione a súa subscrición.</span><span class="sxs-lookup"><span data-stu-id="31a27-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="31a27-121">Dynamics Deployment Services precisa acceder a esta subscrición para poder despregar ambientes.</span><span class="sxs-lookup"><span data-stu-id="31a27-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalles da subscrición a Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="31a27-123">Seleccione **Control de acceso (IAM)** no panel de navegación e logo seleccione **Engadir atribución de roles**.</span><span class="sxs-lookup"><span data-stu-id="31a27-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="31a27-124">No control deslizante do lado dereito, seleccione **Rol de colaborador** e na lista que aparece busque e seleccione **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="31a27-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="31a27-125">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="31a27-125">Select **Save**.</span></span>

![Acceso á subscrición](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="31a27-127">Engadir un conector de subscrición a un proxecto LCS</span><span class="sxs-lookup"><span data-stu-id="31a27-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="31a27-128">No seu proxecto LCS, na páxina **Configuración de Microsoft Azure**, seleccione **Engadir** para engadir un novo conector.</span><span class="sxs-lookup"><span data-stu-id="31a27-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="31a27-129">Introduza o seu ID de subscrición a Azure.</span><span class="sxs-lookup"><span data-stu-id="31a27-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="31a27-130">Pode atopar o seu ID de subscrición a Azure no [Portal de Azure](https://ms.portal.azure.com/), en **Configuración** na parte inferior esquerda da pantalla.</span><span class="sxs-lookup"><span data-stu-id="31a27-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="31a27-131">No campo **Configurar para usar Azure Resource Manager**, seleccione **Si**.</span><span class="sxs-lookup"><span data-stu-id="31a27-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="31a27-132">Asegúrese de que o dominio do arrendatario AAD da subscrición a Azure coincida coa subscrición a Azure que posúe o dominio que está a usar e seleccione **Seguinte**.</span><span class="sxs-lookup"><span data-stu-id="31a27-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="31a27-133">Na pantalla **Configuración de Microsoft Azure**, seleccione **Seguinte** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="31a27-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="31a27-134">Se recibe un erro nesta pantalla, volva á sección [Proporcionar acceso a Dynamics Deployment Services para a subscrición a Azure](#provide) neste tema e asegúrese de que completou todos os pasos.</span><span class="sxs-lookup"><span data-stu-id="31a27-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="31a27-135">Descargue o certificado de xestión de Azure a un cartafol local do seu ordenador.</span><span class="sxs-lookup"><span data-stu-id="31a27-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="31a27-136">Solicite ao administrador da subscrición a Azure que cargue o certificado no Azure Management Portal seleccionando a subscrición e dirixíndose a **Configuración** > **Certificados de xestión**.</span><span class="sxs-lookup"><span data-stu-id="31a27-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="31a27-137">Este certificado permite a LCS comunicarse con Azure no seu nome.</span><span class="sxs-lookup"><span data-stu-id="31a27-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="31a27-138">Podes omitir este paso se o seu usuario ten acceso á subscrición.</span><span class="sxs-lookup"><span data-stu-id="31a27-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="31a27-139">Seleccione **Seguinte**.</span><span class="sxs-lookup"><span data-stu-id="31a27-139">Select  **Next**.</span></span>
8. <span data-ttu-id="31a27-140">Seleccione a rexión de Azure na que desexa despregar e seleccione un centro de datos que estea preto do lugar onde desexa usar este sistema.</span><span class="sxs-lookup"><span data-stu-id="31a27-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="31a27-141">Seleccione **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="31a27-141">Select  **Connect**.</span></span>

<span data-ttu-id="31a27-142">Conectou correctamente a súa subscrición a Azure.</span><span class="sxs-lookup"><span data-stu-id="31a27-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="31a27-143">Agora pode despregar ambientes aloxados na nube de Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="31a27-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
