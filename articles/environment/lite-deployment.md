---
title: Despregar Project Operations Lite - de oferta a facturación proforma
description: Este tema ofrece información sobre como instalar o despregamento de Project Operations lite - de oferta a facturación proforma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948856"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="e54c2-103">Despregar Project Operations Lite - de oferta a facturación proforma</span><span class="sxs-lookup"><span data-stu-id="e54c2-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="e54c2-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="e54c2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e54c2-105">Project Operations admite varios modelos de despregamento.</span><span class="sxs-lookup"><span data-stu-id="e54c2-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="e54c2-106">Para determinar o mellor modelo de despregamento, consulte [Tipos de despregamento](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="e54c2-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="e54c2-107">Este despregamento, o despregamento Lite - de oferta a facturación proforma, ten como resultado **Common Data Service-só despregamento de Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="e54c2-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="e54c2-108">Instalar Project Operations nun novo ambiente de CDS</span><span class="sxs-lookup"><span data-stu-id="e54c2-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="e54c2-109">Instalar nun ambiente de CDS existente</span><span class="sxs-lookup"><span data-stu-id="e54c2-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="e54c2-110">Instalar Project Operations nun novo ambiente de CDS</span><span class="sxs-lookup"><span data-stu-id="e54c2-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="e54c2-111">Como [Administrador global ou Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, cree un novo ambiente de CDS no [Centro de administración de PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="e54c2-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="e54c2-112">Asegúrese de que **Base de datos de CDS** e **Dynamics 365 Apps** están activados.</span><span class="sxs-lookup"><span data-stu-id="e54c2-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="e54c2-113">Para obter información, consulte [Crear e xestionar ambientes no centro de administración de Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="e54c2-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="e54c2-114">Seleccione **Microsoft Dynamics 365 Project Operations** na lista de despregamento de aplicacións de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e54c2-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="e54c2-115">Instalar Project Operations nun ambiente de CDS existente</span><span class="sxs-lookup"><span data-stu-id="e54c2-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="e54c2-116">Como o [Administrador global ou Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) cunha licenza de Project Operations, localice o ambiente no [Centro de administración de PowerPlatform](https://admin.powerplatform.com) onde desexa instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e54c2-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="e54c2-117">Instale **Microsoft Dynamics 365 Project Operations** desde a lista de despregamento de aplicacións de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e54c2-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="e54c2-118">Para obter máis información, consulte [Xestionar aplicacións de Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps)</span><span class="sxs-lookup"><span data-stu-id="e54c2-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


