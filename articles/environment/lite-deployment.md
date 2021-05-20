---
title: Despregar Project Operations - lite
description: Este tema ofrece información sobre como instalar o despregamento de Project Operations lite - de oferta a facturación proforma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950262"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="91498-103">Despregar Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="91498-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="91498-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="91498-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="91498-105">Project Operations admite varios modelos de despregamento.</span><span class="sxs-lookup"><span data-stu-id="91498-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="91498-106">Para determinar o mellor modelo de despregamento, consulte [Tipos de despregamento](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="91498-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="91498-107">Este despregamento, o despregamento Lite - de oferta a facturación proforma, ten como resultado **Common Data Service-só despregamento de Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="91498-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="91498-108">Instalar Project Operations nun novo ambiente de CDS</span><span class="sxs-lookup"><span data-stu-id="91498-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="91498-109">Instalar nun ambiente de CDS existente</span><span class="sxs-lookup"><span data-stu-id="91498-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="91498-110">Instalar Project Operations nun novo ambiente de CDS</span><span class="sxs-lookup"><span data-stu-id="91498-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="91498-111">Como [Administrador global ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, cree un novo ambiente de CDS no [Centro de administración de PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="91498-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="91498-112">Asegúrese de que **Base de datos de CDS** e **Dynamics 365 Apps** están activados.</span><span class="sxs-lookup"><span data-stu-id="91498-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="91498-113">Para obter información, consulte [Crear e xestionar ambientes no centro de administración de Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="91498-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="91498-114">Seleccione **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="91498-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="91498-115">Instalar Project Operations nun ambiente de CDS existente</span><span class="sxs-lookup"><span data-stu-id="91498-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="91498-116">Como o [Administrador global ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, localice o ambiente no [Centro de administración de PowerPlatform](https://admin.powerplatform.com) onde desexa instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="91498-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="91498-117">Instale **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="91498-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="91498-118">Para obter máis información, consulte [Xestionar aplicacións de Dynamics 365](/power-platform/admin/manage-apps)</span><span class="sxs-lookup"><span data-stu-id="91498-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]