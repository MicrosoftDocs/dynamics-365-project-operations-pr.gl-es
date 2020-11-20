---
title: Determinar o seu tipo de despregamento
description: Este tema ofrece información para axudarlle a determinar o tipo de despregamento correcto das operacións do proxecto para a súa empresa.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401216"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="6fc99-103">Determinar o seu tipo de despregamento</span><span class="sxs-lookup"><span data-stu-id="6fc99-103">Determine your deployment type</span></span>

<span data-ttu-id="6fc99-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="6fc99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6fc99-105">Despois de mercar a licenza, comece aquí para determinar o mellor modelo de despregamento de Dynamics 365 Project Operations usando o [Fluxo de instalación guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6fc99-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6fc99-106">Despois de completar o fluxo de instalación guiada, dirixiráselle ao portal de xestión correcto para completar a instalación.</span><span class="sxs-lookup"><span data-stu-id="6fc99-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6fc99-107">Vexa os detalles de despregamento para completar a instalación.</span><span class="sxs-lookup"><span data-stu-id="6fc99-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6fc99-108">Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6fc99-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6fc99-109">Project Operations inclúe as capacidades que se fornecen con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6fc99-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6fc99-110">Publicarase un camiño de actualización para estes clientes na onda 1 da versión de 2021.</span><span class="sxs-lookup"><span data-stu-id="6fc99-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6fc99-111">Clientes existentes de Dynamics 365 Finance empregando a xestión e a contabilidade do proxecto</span><span class="sxs-lookup"><span data-stu-id="6fc99-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6fc99-112">Os clientes existentes de Finance que empregan a funcionalidade de xestión e contabilidade de proxectos poden seguir empregándoa tal como está.</span><span class="sxs-lookup"><span data-stu-id="6fc99-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="6fc99-113">Consulte [Project Operations para situacións baseadas en recursos/sen fornecemento](#pma).</span><span class="sxs-lookup"><span data-stu-id="6fc99-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="6fc99-114">Tipos de despregamento</span><span class="sxs-lookup"><span data-stu-id="6fc99-114">Deployment types</span></span>
<span data-ttu-id="6fc99-115">Project Operations admite varias opcións de despregamento para adaptarse ás súas necesidades.</span><span class="sxs-lookup"><span data-stu-id="6fc99-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6fc99-116">Se vostede é un cliente novo ou existente de Dynamics 365, Project Operations pode atender ás súas necesidades.</span><span class="sxs-lookup"><span data-stu-id="6fc99-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6fc99-117">O noso [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations) axudaralle a determinar o despregamento correcto.</span><span class="sxs-lookup"><span data-stu-id="6fc99-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6fc99-118">Os resultados guiarano cara a un dos seguintes tipos de despregamento:</span><span class="sxs-lookup"><span data-stu-id="6fc99-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6fc99-119">Despregamento de Lite: acordo para facturación proforma</span><span class="sxs-lookup"><span data-stu-id="6fc99-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6fc99-120">Project Operations para escenarios baseados en recursos ou sen existencias</span><span class="sxs-lookup"><span data-stu-id="6fc99-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6fc99-121">Project Operations para situacións baseadas en recursos/sen fornecemento</span><span class="sxs-lookup"><span data-stu-id="6fc99-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6fc99-122">Project Operations admite situacións de pedidos de produción/con fornecemento e situacións baseadas en recursos/sen fornecemento no mesmo ambiente a través de configuracións a nivel de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="6fc99-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6fc99-123">Por exemplo, Contoso pode usar as capacidades de pedidos de fornecemento/produción na súa fábrica de Estados Unidos (entidade legal = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="6fc99-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="6fc99-124">Contoso pode usar as capacidades sen fornecemento/baseadas en recursos na súa instalación de servizo de Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="6fc99-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="6fc99-125">Despregamento de Lite: acordo para facturación proforma</span><span class="sxs-lookup"><span data-stu-id="6fc99-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="6fc99-126">O despregamento lite inclúe as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="6fc99-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6fc99-127">Proceso de vendas para proxectos que amplían as experiencias da aplicación Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="6fc99-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="6fc99-128">Planificación de proxectos mediante Microsoft Project para a web</span><span class="sxs-lookup"><span data-stu-id="6fc99-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6fc99-129">Prezos multidimensionais</span><span class="sxs-lookup"><span data-stu-id="6fc99-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6fc99-130">Xestión de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="6fc99-130">Unified resource management</span></span>
- <span data-ttu-id="6fc99-131">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="6fc99-131">Time tracking</span></span>
- <span data-ttu-id="6fc99-132">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="6fc99-132">Basic expense</span></span>
- <span data-ttu-id="6fc99-133">Facturación proforma e orientada ao cliente</span><span class="sxs-lookup"><span data-stu-id="6fc99-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="6fc99-134">Pasos de despregamento</span><span class="sxs-lookup"><span data-stu-id="6fc99-134">Deployment steps</span></span>
<span data-ttu-id="6fc99-135">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6fc99-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6fc99-136">Para este despregamento, consulte [Rexistro para subscricións de previsualización](lite-preview-subscription-sign-up.md) e [Fornecer a novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="6fc99-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="6fc99-137">Project Operations para escenarios baseados en recursos ou sen existencias</span><span class="sxs-lookup"><span data-stu-id="6fc99-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6fc99-138">Project Operations para situacións de recursos/sen fornecemento inclúe as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="6fc99-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="6fc99-139">Proceso de vendas para proxectos que amplían a aplicación Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="6fc99-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="6fc99-140">Planificación de proxectos mediante Microsoft Project para a web</span><span class="sxs-lookup"><span data-stu-id="6fc99-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6fc99-141">Prezos multidimensionais</span><span class="sxs-lookup"><span data-stu-id="6fc99-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6fc99-142">Xestión de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="6fc99-142">Unified resource management</span></span>
- <span data-ttu-id="6fc99-143">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="6fc99-143">Time tracking</span></span>
- <span data-ttu-id="6fc99-144">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="6fc99-144">Basic expense</span></span>
- <span data-ttu-id="6fc99-145">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="6fc99-145">Full expense</span></span>
- <span data-ttu-id="6fc99-146">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="6fc99-146">Receipt OCR</span></span>
- <span data-ttu-id="6fc99-147">Facturación proforma e orientada ao cliente</span><span class="sxs-lookup"><span data-stu-id="6fc99-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="6fc99-148">Recoñecemento de ingresos para proxectos</span><span class="sxs-lookup"><span data-stu-id="6fc99-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6fc99-149">Pasos de despregamento</span><span class="sxs-lookup"><span data-stu-id="6fc99-149">Deployment steps</span></span>
<span data-ttu-id="6fc99-150">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6fc99-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6fc99-151">Para este despregamento, consulte [Rexistro para subscricións de previsualización](resource-sign-up-preview-subscription.md) e [Fornecer a novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6fc99-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6fc99-152">Project Operations para situacións baseadas en recursos/sen fornecemento</span><span class="sxs-lookup"><span data-stu-id="6fc99-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6fc99-153">Planificación de proxectos mediante WBS</span><span class="sxs-lookup"><span data-stu-id="6fc99-153">Project planning using WBS</span></span>
- <span data-ttu-id="6fc99-154">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="6fc99-154">Resource Management</span></span>
- <span data-ttu-id="6fc99-155">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="6fc99-155">Time Tracking</span></span>
- <span data-ttu-id="6fc99-156">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="6fc99-156">Full Expense</span></span>
- <span data-ttu-id="6fc99-157">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="6fc99-157">Receipt OCR</span></span>
- <span data-ttu-id="6fc99-158">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="6fc99-158">Full Invoicing</span></span>
- <span data-ttu-id="6fc99-159">Recoñecemento de ingresos</span><span class="sxs-lookup"><span data-stu-id="6fc99-159">Revenue Recognition</span></span>
- <span data-ttu-id="6fc99-160">Pedidos de produción</span><span class="sxs-lookup"><span data-stu-id="6fc99-160">Production Orders</span></span>
- <span data-ttu-id="6fc99-161">Asistencia técnica para materiais</span><span class="sxs-lookup"><span data-stu-id="6fc99-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6fc99-162">Pasos de despregamento</span><span class="sxs-lookup"><span data-stu-id="6fc99-162">Deployment steps</span></span>
<span data-ttu-id="6fc99-163">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6fc99-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6fc99-164">Para este despregamento, consulte [Rexistro para subscricións de previsualización](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Fornecer a novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6fc99-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

