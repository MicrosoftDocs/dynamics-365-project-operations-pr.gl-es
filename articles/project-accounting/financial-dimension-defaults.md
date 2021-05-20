---
title: Valores predefinidos das dimensións financeiras
description: Este tema ofrece información sobre como configurar valores predefinidos de dimensións financeiras.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950127"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="ab61e-103">Valores predefinidos das dimensións financeiras</span><span class="sxs-lookup"><span data-stu-id="ab61e-103">Financial dimension defaults</span></span>

<span data-ttu-id="ab61e-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="ab61e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ab61e-105">Dynamics 365 Project Operations usa o marco [Dimensións financeiras](/dynamics365/finance/general-ledger/financial-dimensions) en Dynamics 365 Finance para proporcionar información adicional sobre as transaccións do libro maior e do libro auxiliar do proxecto.</span><span class="sxs-lookup"><span data-stu-id="ab61e-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="ab61e-106">As dimensións financeiras predefinidas pódense establecer nun cliente, fonte de financiamento do proxecto, fito, liña de contrato de proxecto ou proxecto.</span><span class="sxs-lookup"><span data-stu-id="ab61e-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="ab61e-107">Definir dimensións financeiras por defecto para un cliente</span><span class="sxs-lookup"><span data-stu-id="ab61e-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="ab61e-108">Os valores predefinidos das dimensións do cliente especifícanse en Finance.</span><span class="sxs-lookup"><span data-stu-id="ab61e-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="ab61e-109">Complete os seguintes pasos para establecer os valores predefinidos das dimensións.</span><span class="sxs-lookup"><span data-stu-id="ab61e-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="ab61e-110">Vaia a **Contas pendentes de cobro** > **Clientes** > **Todos os clientes**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="ab61e-111">Na páxina **Clientes**, no separador **Dimensións financeiras**, defina os valores das dimensións financeiras para un cliente específico.</span><span class="sxs-lookup"><span data-stu-id="ab61e-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="ab61e-112">Definir dimensións financeiras por defecto para contratos de proxecto</span><span class="sxs-lookup"><span data-stu-id="ab61e-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="ab61e-113">Os contratos de proxecto créanse e mantéñense en Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="ab61e-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="ab61e-114">Os atributos de contabilidade para os contratos de proxecto configúranse no módulo **Xestión e contabilidade de proxectos** en Finance.</span><span class="sxs-lookup"><span data-stu-id="ab61e-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="ab61e-115">Establecer dimensións financeiras para unha fonte de financiamento do proxecto</span><span class="sxs-lookup"><span data-stu-id="ab61e-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="ab61e-116">Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Contratos de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="ab61e-117">Seleccione o rexistro que desexa actualizar e no separador **Contrato de proxecto**, seleccione **Mostrar contabilidade predefinida**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="ab61e-118">Expanda **Información relacionada** e seleccione o separador **Fontes de financiamento**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="ab61e-119">Estableza os valores predefinidos das dimensións financeiras.</span><span class="sxs-lookup"><span data-stu-id="ab61e-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="ab61e-120">Teña en conta que as dimensións financeiras predefínense na conta do cliente.</span><span class="sxs-lookup"><span data-stu-id="ab61e-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="ab61e-121">Establecer dimensións financeiras para unha liña de contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="ab61e-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="ab61e-122">Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Contratos de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="ab61e-123">Seleccione o rexistro que desexa actualizar e no separador **Contrato de proxecto**, seleccione **Mostrar contabilidade predefinida**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="ab61e-124">Expanda **Información relacionada** e seleccione o separador **Liñas de contrato**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="ab61e-125">Estableza os valores predefinidos das dimensións financeiras.</span><span class="sxs-lookup"><span data-stu-id="ab61e-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="ab61e-126">Os valores predefinidos das dimensións financeiras son aplicables e só se poden empregar con liñas de contrato de prezo fixo (fito).</span><span class="sxs-lookup"><span data-stu-id="ab61e-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="ab61e-127">Estes valores predefinidos úsanse en transaccións en conta de proxectos e liñas de facturación relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ab61e-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="ab61e-128">Definir dimensións financeiras por defecto para proxectos</span><span class="sxs-lookup"><span data-stu-id="ab61e-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="ab61e-129">Os proxectos créanse e mantéñense en (CDS).</span><span class="sxs-lookup"><span data-stu-id="ab61e-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="ab61e-130">Os atributos de contabilidade para os proxectos configúranse no módulo **Xestión e contabilidade de proxectos** en Finance.</span><span class="sxs-lookup"><span data-stu-id="ab61e-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="ab61e-131">Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Todos os proxectos**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="ab61e-132">Seleccione o rexistro que desexa actualizar e no separador **Proxecto**, seleccione **Mostrar contabilidade predefinida**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="ab61e-133">Expanda **Información relacionada** e seleccione o separador **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="ab61e-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="ab61e-134">Estableza os valores predefinidos das dimensións financeiras.</span><span class="sxs-lookup"><span data-stu-id="ab61e-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="ab61e-135">Teña en conta que as dimensións financeiras predefínense na conta do cliente.</span><span class="sxs-lookup"><span data-stu-id="ab61e-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="ab61e-136">Se o proxecto está asociado a unha liña de contrato con varios clientes de contrato de proxecto, o cliente principal úsase para as dimensións financeiras predefinidas.</span><span class="sxs-lookup"><span data-stu-id="ab61e-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="ab61e-137">As dimensións financeiras predefinidas do proxecto úsanse para establecer os valores predefinidos da liña de diario para transaccións de tempo, gastos e taxas no **Diario de Project Operations Integration** e nas liñas de factura de proxecto relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ab61e-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]