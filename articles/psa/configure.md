---
title: Configurar Project Service Automation
description: Pasos para configurar Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002831"
---
# <a name="configure-project-service"></a><span data-ttu-id="f8cd9-103">Configurar Project Service</span><span class="sxs-lookup"><span data-stu-id="f8cd9-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f8cd9-104">Para poder usar os recursos de automatización de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] para xestionar contas, proxectos e recursos, é necesario que complete uns pasos de configuración para garantir que a solución de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] coincida coas necesidades da súa organización.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="f8cd9-105">Siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="f8cd9-105">These steps include:</span></span>  
  
-   <span data-ttu-id="f8cd9-106">[Configurar unidades de hora](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="f8cd9-107">Configurar as unidades de tempo no catálogo de produtos que vai utilizar como base para a programación e facturación dos seus proxectos.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="f8cd9-108">[Configurar a moeda e as taxas de cambio](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="f8cd9-109">Definir moedas para utilizar cos seus proxectos.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="f8cd9-110">[Crear unidades organizativas](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="f8cd9-111">Configurar os grupos que utiliza a súa empresa para dividir o negocio, por xeografía, función da empresa ou outra división lóxica.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="f8cd9-112">[Configurar frecuencias da factura](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="f8cd9-113">Configurar períodos de tempo que desexa utilizar para facturar aos clientes.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="f8cd9-114">[Configurar categorías de transaccións](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="f8cd9-115">Configurar categorías de transacción nas que os consultores poden cobrar os seus gastos facturables e non facturables.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f8cd9-116">[Configurar categorías de gasto](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="f8cd9-117">Configurar as categorías nas que os consultores poden cobrar os seus gastos facturables e non facturables.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f8cd9-118">[Crear elementos do catálogo de produtos](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="f8cd9-119">Engadir os produtos que vende, como licenzas de software, ao catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="f8cd9-120">[Crear unha lista de prezos](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="f8cd9-121">Configurar listas de prezos diferentes, dependendo de canto quere cobrar aos clientes por cada rol que require o seu proxecto.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="f8cd9-122">[Configurar recursos reservables](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="f8cd9-123">Engadir os coñecementos, cualificacións, roles de recursos e outra información de recursos que necesitará para os seus proxectos.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f8cd9-124">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="f8cd9-124">See Also</span></span>  
 <span data-ttu-id="f8cd9-125">[Visión xeral de Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f8cd9-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="f8cd9-126">[Configurar Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="f8cd9-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="f8cd9-127">[Guía do xestor de contas](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f8cd9-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f8cd9-128">[Guía do xestor de proxectos](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f8cd9-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="f8cd9-129">[Guía para o xestor de recursos](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f8cd9-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="f8cd9-130">Guía de tempo, gasto e colaboración</span><span class="sxs-lookup"><span data-stu-id="f8cd9-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]