---
title: Configurar categorías de proxecto
description: Neste tema se proporciona información sobre a configuración das categorías de proxectos.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131926"
---
# <a name="configure-project-categories"></a><span data-ttu-id="fd5e0-103">Configurar categorías de proxecto</span><span class="sxs-lookup"><span data-stu-id="fd5e0-103">Configure project categories</span></span>

<span data-ttu-id="fd5e0-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="fd5e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fd5e0-105">Project Operations ofrece capacidades robustas para categorizar ingresos e gastos en proxectos.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="fd5e0-106">As categorías ofrecen a capacidade de informar e analizar as transaccións do proxecto e impulsar a contabilización no libro maior.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="fd5e0-107">O seguinte diagrama ilustra a correlación entre categorías de transaccións, as categorías compartidas e as categorías de proxectos.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="fd5e0-108">As categorías de transaccións son a agrupación básica para as transaccións do proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="fd5e0-109">Dentro desa agrupación, hai un conxunto de categorías compartidas que se poden compartir entre aplicacións e módulos.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="fd5e0-110">Afondando aínda máis nos aspectos específicos, as categorías de proxectos son o nivel máis granular de categorías.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="fd5e0-111">As categorías de proxectos son específicas para a entidade legal, o módulo e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-111">Project categories are specific to legal entity, module, and application.</span></span>

![Correlación entre categorías de transaccións, as categorías compartidas e as categorías de proxectos](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="fd5e0-113">Categorías de transaccións</span><span class="sxs-lookup"><span data-stu-id="fd5e0-113">Transaction categories</span></span>

<span data-ttu-id="fd5e0-114">As categorías de transaccións representan a agrupación básica para as transaccións do proxecto e non son específicas do tipo de empresa ou transacción.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="fd5e0-115">Por exemplo, Contoso Robotics usa as categorías de Deseño, Viaxe, Instalación e Transacción de servizos para agrupar as transaccións do proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="fd5e0-116">As categorías de transaccións defínense no módulo Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="fd5e0-117">Vaia a **Configuración** \> **Categorías de transaccións** para abrir o formulario.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="fd5e0-118">Cree unha nova categoría de transaccións seleccionando **Nova** ou seleccionando **Importar desde Excel**.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="fd5e0-119">Categorías compartidas</span><span class="sxs-lookup"><span data-stu-id="fd5e0-119">Shared categories</span></span>

<span data-ttu-id="fd5e0-120">Dynamics 365 utiliza o concepto de categorías compartidas para clasificar os gastos en diferentes aplicacións, como Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="fd5e0-121">Para cada categoría de transacción creada, Project Operations crea automaticamente catro categorías compartidas relacionadas: Horas, Gasto, Taxas e Elemento.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="fd5e0-122">Pode revisar e axustar as categorías compartidas indo a **Xestión de proxectos e contabilidade** \> **Configuración** \> **Categorías** \> **Categorías compartidas**.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="fd5e0-123">Categorías do proxecto</span><span class="sxs-lookup"><span data-stu-id="fd5e0-123">Project categories</span></span>

<span data-ttu-id="fd5e0-124">As categorías do proxecto representan o nivel máis granular da configuración de categorías e deben ser configuradas por separado e para cada empresa por un contable do proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="fd5e0-125">Vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Categorías** \> **Categorías de proxectos**.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="fd5e0-126">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-126">Select **New**.</span></span>
3. <span data-ttu-id="fd5e0-127">Seleccione a **ID de categoría** da categoría compartida que creou na sección anterior.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="fd5e0-128">Project Operations permite usar só as categorías compartidas asociadas a categorías de transaccións.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="fd5e0-129">Seleccionar un grupo de categorías</span><span class="sxs-lookup"><span data-stu-id="fd5e0-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="fd5e0-130">Grupos de categorías</span><span class="sxs-lookup"><span data-stu-id="fd5e0-130">Category groups</span></span>

<span data-ttu-id="fd5e0-131">Os grupos de categorías úsanse para compartir propiedades, principalmente publicar perfís, entre categorías de proxectos relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="fd5e0-132">Debe haber polo menos un grupo de categorías para cada tipo de transacción e cada categoría de proxecto ten asignado un grupo.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="fd5e0-133">As especificacións de contabilización en Project Operations están definidas polas regras do perfil de custos e ingresos do proxecto, as categorías de proxectos e os grupos de categorías.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="fd5e0-134">Pode configurar grupos de categorías indo a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Categorías** \> **Grupos de categorías**.</span><span class="sxs-lookup"><span data-stu-id="fd5e0-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
