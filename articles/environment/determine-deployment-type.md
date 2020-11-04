---
title: Determinar o seu tipo de despregamento
description: Este tema ofrece información para axudarlle a determinar o tipo de despregamento correcto das operacións do proxecto para a súa empresa.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076136"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="f8678-103">Determinar o seu tipo de despregamento</span><span class="sxs-lookup"><span data-stu-id="f8678-103">Determine your deployment type</span></span>

<span data-ttu-id="f8678-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="f8678-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8678-105">Despois de mercar a licenza, comece aquí para determinar o mellor modelo de despregamento de Dynamics 365 Project Operations usando o [Fluxo de instalación guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f8678-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="f8678-106">Despois de completar o fluxo de instalación guiada, dirixiráselle ao portal de xestión correcto para completar a instalación.</span><span class="sxs-lookup"><span data-stu-id="f8678-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="f8678-107">Vexa os detalles de despregamento para completar a instalación.</span><span class="sxs-lookup"><span data-stu-id="f8678-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="f8678-108">Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f8678-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="f8678-109">Project Operations inclúe as capacidades que se fornecen con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f8678-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="f8678-110">No futuro publicarase unha ruta de actualización para estes clientes.</span><span class="sxs-lookup"><span data-stu-id="f8678-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="f8678-111">Clientes existentes de Dynamics 365 Finance empregando a xestión e a contabilidade do proxecto</span><span class="sxs-lookup"><span data-stu-id="f8678-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="f8678-112">Os clientes existentes de Finance que empregan a funcionalidade de xestión e contabilidade de proxectos poden seguir usando isto tal como está.</span><span class="sxs-lookup"><span data-stu-id="f8678-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="f8678-113">Consulte [Project Operations para situacións baseadas en recursos/sen fornecemento](#pma).</span><span class="sxs-lookup"><span data-stu-id="f8678-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="f8678-114">Tipos de despregamento</span><span class="sxs-lookup"><span data-stu-id="f8678-114">Deployment types</span></span>
<span data-ttu-id="f8678-115">Project Operations admite varias opcións de despregamento para adaptarse ás súas necesidades.</span><span class="sxs-lookup"><span data-stu-id="f8678-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="f8678-116">Se vostede é un cliente novo ou existente de Dynamics 365, Project Operations pode atender ás súas necesidades.</span><span class="sxs-lookup"><span data-stu-id="f8678-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="f8678-117">O noso [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations) axudaralle a determinar o despregamento correcto.</span><span class="sxs-lookup"><span data-stu-id="f8678-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="f8678-118">Os resultados guiarano cara a un dos seguintes tipos de despregamento:</span><span class="sxs-lookup"><span data-stu-id="f8678-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="f8678-119">Despregamento de Lite: acordo para facturación proforma</span><span class="sxs-lookup"><span data-stu-id="f8678-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="f8678-120">Project Operations para escenarios baseados en recursos ou sen existencias</span><span class="sxs-lookup"><span data-stu-id="f8678-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="f8678-121">Project Operations para situacións baseadas en recursos/sen fornecemento</span><span class="sxs-lookup"><span data-stu-id="f8678-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="f8678-122">Project Operations admite situacións de pedidos de produción/con fornecemento e situacións baseadas en recursos/sen fornecemento no mesmo ambiente a través de configuracións a nivel de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="f8678-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="f8678-123">Por exemplo, Contoso pode usar as capacidades de pedidos de fornecemento/produción na súa fábrica de Estados Unidos (entidade legal = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="f8678-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="f8678-124">Contoso pode usar as capacidades sen fornecemento/baseadas en recursos na súa instalación de servizo de Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="f8678-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="f8678-125">Despregamento de Lite: acordo para facturación proforma</span><span class="sxs-lookup"><span data-stu-id="f8678-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="f8678-126">O despregamento lite inclúe as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="f8678-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="f8678-127">Planificación de proxectos mediante Microsoft Project para a web</span><span class="sxs-lookup"><span data-stu-id="f8678-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f8678-128">Prezos multidimensionais</span><span class="sxs-lookup"><span data-stu-id="f8678-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f8678-129">Xestión de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="f8678-129">Unified Resource Management</span></span>
- <span data-ttu-id="f8678-130">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="f8678-130">Time Tracking</span></span>
- <span data-ttu-id="f8678-131">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="f8678-131">Basic Expense</span></span>
- <span data-ttu-id="f8678-132">Proposta de factura</span><span class="sxs-lookup"><span data-stu-id="f8678-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f8678-133">Pasos de despregamento</span><span class="sxs-lookup"><span data-stu-id="f8678-133">Deployment steps</span></span>
<span data-ttu-id="f8678-134">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f8678-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f8678-135">Para este despregamento, consulte [Rexistro para subscricións de previsualización](lite-preview-subscription-sign-up.md) e [Fornecer a novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="f8678-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="f8678-136">Project Operations para escenarios baseados en recursos ou sen existencias</span><span class="sxs-lookup"><span data-stu-id="f8678-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="f8678-137">Project Operations para situacións de recursos/sen fornecemento inclúe as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="f8678-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="f8678-138">Planificación de proxectos mediante Microsoft Project para a web</span><span class="sxs-lookup"><span data-stu-id="f8678-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f8678-139">Prezos multidimensionais</span><span class="sxs-lookup"><span data-stu-id="f8678-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f8678-140">Xestión de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="f8678-140">Unified Resource Management</span></span>
- <span data-ttu-id="f8678-141">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="f8678-141">Time Tracking</span></span>
- <span data-ttu-id="f8678-142">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="f8678-142">Basic Expense</span></span>
- <span data-ttu-id="f8678-143">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="f8678-143">Full Expense</span></span>
- <span data-ttu-id="f8678-144">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="f8678-144">Receipt OCR</span></span>
- <span data-ttu-id="f8678-145">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="f8678-145">Full Invoicing</span></span>
- <span data-ttu-id="f8678-146">Recoñecemento de ingresos</span><span class="sxs-lookup"><span data-stu-id="f8678-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f8678-147">Pasos de despregamento</span><span class="sxs-lookup"><span data-stu-id="f8678-147">Deployment steps</span></span>
<span data-ttu-id="f8678-148">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f8678-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f8678-149">Para este despregamento, consulte [Rexistro para subscricións de previsualización](resource-sign-up-preview-subscription.md) e [Fornecer a novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="f8678-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="f8678-150">Project Operations para situacións baseadas en recursos/sen fornecemento</span><span class="sxs-lookup"><span data-stu-id="f8678-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="f8678-151">Planificación de proxectos mediante WBS</span><span class="sxs-lookup"><span data-stu-id="f8678-151">Project planning using WBS</span></span>
- <span data-ttu-id="f8678-152">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="f8678-152">Resource Management</span></span>
- <span data-ttu-id="f8678-153">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="f8678-153">Time Tracking</span></span>
- <span data-ttu-id="f8678-154">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="f8678-154">Full Expense</span></span>
- <span data-ttu-id="f8678-155">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="f8678-155">Receipt OCR</span></span>
- <span data-ttu-id="f8678-156">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="f8678-156">Full Invoicing</span></span>
- <span data-ttu-id="f8678-157">Recoñecemento de ingresos</span><span class="sxs-lookup"><span data-stu-id="f8678-157">Revenue Recognition</span></span>
- <span data-ttu-id="f8678-158">Pedidos de produción</span><span class="sxs-lookup"><span data-stu-id="f8678-158">Production Orders</span></span>
- <span data-ttu-id="f8678-159">Asistencia técnica para materiais</span><span class="sxs-lookup"><span data-stu-id="f8678-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f8678-160">Pasos de despregamento</span><span class="sxs-lookup"><span data-stu-id="f8678-160">Deployment steps</span></span>
<span data-ttu-id="f8678-161">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f8678-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f8678-162">Para este despregamento, consulte [Rexistro para subscricións de previsualización](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Fornecer a novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f8678-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

