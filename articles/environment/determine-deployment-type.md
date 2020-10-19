---
title: Tipos de despregamento
description: Este tema ofrece información para axudarlle a determinar o tipo de despregamento correcto das operacións do proxecto para a súa empresa.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948858"
---
# <a name="deployment-types"></a><span data-ttu-id="d5b47-103">Tipos de despregamento</span><span class="sxs-lookup"><span data-stu-id="d5b47-103">Deployment types</span></span>

<span data-ttu-id="d5b47-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="d5b47-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5b47-105">Despois de mercar a licenza, comece aquí para determinar o mellor modelo de despregamento de Dynamics 365 Project Operations usando o [Fluxo de instalación guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d5b47-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="d5b47-106">Despois de completar o fluxo de instalación guiada, dirixiráselle ao portal de xestión correcto para completar a instalación.</span><span class="sxs-lookup"><span data-stu-id="d5b47-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="d5b47-107">Vexa os detalles de despregamento a seguir para completar a instalación.</span><span class="sxs-lookup"><span data-stu-id="d5b47-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="d5b47-108">Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d5b47-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="d5b47-109">Project Operations inclúe as capacidades que se fornecen con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d5b47-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="d5b47-110">No futuro publicarase unha ruta de actualización para estes clientes.</span><span class="sxs-lookup"><span data-stu-id="d5b47-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="d5b47-111">Clientes existentes de Dynamics 365 Finance empregando a xestión e a contabilidade do proxecto</span><span class="sxs-lookup"><span data-stu-id="d5b47-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="d5b47-112">Os clientes existentes de Finance que empregan a funcionalidade de xestión e contabilidade de proxectos poden seguir usando isto tal como está.</span><span class="sxs-lookup"><span data-stu-id="d5b47-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="d5b47-113">Consulte [Project Operations para situacións baseadas en recursos/sen fornecemento](#pma).</span><span class="sxs-lookup"><span data-stu-id="d5b47-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="d5b47-114">Project Operations admite varias opcións de despregamento para adaptarse ás súas necesidades.</span><span class="sxs-lookup"><span data-stu-id="d5b47-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="d5b47-115">Se vostede é un cliente novo ou existente de Dynamics 365, Project Operations pode atender ás súas necesidades.</span><span class="sxs-lookup"><span data-stu-id="d5b47-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="d5b47-116">O noso [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations) axudaralle a determinar o despregamento correcto.</span><span class="sxs-lookup"><span data-stu-id="d5b47-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="d5b47-117">Os resultados guiarano cara a un dos seguintes tipos de despregamento:</span><span class="sxs-lookup"><span data-stu-id="d5b47-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="d5b47-118">Despregamento de Lite: acordo para facturación proforma</span><span class="sxs-lookup"><span data-stu-id="d5b47-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="d5b47-119">Project Operations para escenarios baseados en recursos ou sen existencias</span><span class="sxs-lookup"><span data-stu-id="d5b47-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="d5b47-120">Project Operations para situacións baseadas en recursos/sen fornecemento</span><span class="sxs-lookup"><span data-stu-id="d5b47-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="d5b47-121">Project Operations admite situacións de pedidos de produción/con fornecemento e situacións baseadas en recursos/sen fornecemento no mesmo ambiente a través de configuracións a nivel de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="d5b47-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="d5b47-122">Por exemplo, Contoso pode aproveitar as capacidades de pedidos de produción/con forncemento nas súas instalacións de fabricación de Estados Unidos (entidade legal = Contoso Manufacturing United States) e as capacidades baseadas en recursos/sen fornecemento na súa instalación de servizos de Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="d5b47-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="d5b47-123"><a name="lite"><a/>Despregamento de Lite: acordo para facturación proforma</span><span class="sxs-lookup"><span data-stu-id="d5b47-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="d5b47-124">O despregamento lite inclúe as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="d5b47-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="d5b47-125">Planificación de proxectos mediante Microsoft Project para a web</span><span class="sxs-lookup"><span data-stu-id="d5b47-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d5b47-126">Prezos multidimensionais</span><span class="sxs-lookup"><span data-stu-id="d5b47-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d5b47-127">Xestión de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="d5b47-127">Unified Resource Management</span></span>
- <span data-ttu-id="d5b47-128">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="d5b47-128">Time Tracking</span></span>
- <span data-ttu-id="d5b47-129">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="d5b47-129">Basic Expense</span></span>
- <span data-ttu-id="d5b47-130">Proposta de factura</span><span class="sxs-lookup"><span data-stu-id="d5b47-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="d5b47-131">Pasos de despregamento:</span><span class="sxs-lookup"><span data-stu-id="d5b47-131">Deployment steps:</span></span>
<span data-ttu-id="d5b47-132">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d5b47-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d5b47-133">Para este despregamento, consulte [Rexistro para subscricións de previsualización](lite-preview-subscription-sign-up.md) e [Fornecer a novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="d5b47-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="d5b47-134"><a name="integrated"><a/>Project Operations para escenarios baseados en recursos ou sen existencias</span><span class="sxs-lookup"><span data-stu-id="d5b47-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="d5b47-135">Project Operations para situacións de recursos/sen fornecemento inclúe as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="d5b47-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="d5b47-136">Planificación de proxectos mediante Microsoft Project para a web</span><span class="sxs-lookup"><span data-stu-id="d5b47-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d5b47-137">Prezos multidimensionais</span><span class="sxs-lookup"><span data-stu-id="d5b47-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d5b47-138">Xestión de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="d5b47-138">Unified Resource Management</span></span>
- <span data-ttu-id="d5b47-139">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="d5b47-139">Time Tracking</span></span>
- <span data-ttu-id="d5b47-140">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="d5b47-140">Basic Expense</span></span>
- <span data-ttu-id="d5b47-141">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="d5b47-141">Full Expense</span></span>
- <span data-ttu-id="d5b47-142">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="d5b47-142">Receipt OCR</span></span>
- <span data-ttu-id="d5b47-143">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="d5b47-143">Full Invoicing</span></span>
- <span data-ttu-id="d5b47-144">Recoñecemento de ingresos</span><span class="sxs-lookup"><span data-stu-id="d5b47-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="d5b47-145">Pasos de despregamento:</span><span class="sxs-lookup"><span data-stu-id="d5b47-145">Deployment steps:</span></span>
<span data-ttu-id="d5b47-146">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d5b47-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d5b47-147">Para este despregamento, consulte [Rexistro para subscricións de previsualización](resource-sign-up-preview-subscription.md) e [Fornecer a novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d5b47-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="d5b47-148">Project Operations para situacións baseadas en recursos/sen fornecemento</span><span class="sxs-lookup"><span data-stu-id="d5b47-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="d5b47-149">Planificación de proxectos mediante WBS</span><span class="sxs-lookup"><span data-stu-id="d5b47-149">Project planning using WBS</span></span>
- <span data-ttu-id="d5b47-150">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="d5b47-150">Resource Management</span></span>
- <span data-ttu-id="d5b47-151">Rastrexo de tempo</span><span class="sxs-lookup"><span data-stu-id="d5b47-151">Time Tracking</span></span>
- <span data-ttu-id="d5b47-152">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="d5b47-152">Full Expense</span></span>
- <span data-ttu-id="d5b47-153">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="d5b47-153">Receipt OCR</span></span>
- <span data-ttu-id="d5b47-154">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="d5b47-154">Full Invoicing</span></span>
- <span data-ttu-id="d5b47-155">Recoñecemento de ingresos</span><span class="sxs-lookup"><span data-stu-id="d5b47-155">Revenue Recognition</span></span>
- <span data-ttu-id="d5b47-156">Pedidos de produción</span><span class="sxs-lookup"><span data-stu-id="d5b47-156">Production Orders</span></span>
- <span data-ttu-id="d5b47-157">Asistencia técnica para materiais</span><span class="sxs-lookup"><span data-stu-id="d5b47-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="d5b47-158">Pasos de despregamento:</span><span class="sxs-lookup"><span data-stu-id="d5b47-158">Deployment steps:</span></span>
<span data-ttu-id="d5b47-159">Determine o mellor modelo de despregamento de Project Operations usando o [Cuestionario de despregamento](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d5b47-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d5b47-160">Para este despregamento, consulte [Rexistro para subscricións de previsualización](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Fornecer a novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d5b47-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



