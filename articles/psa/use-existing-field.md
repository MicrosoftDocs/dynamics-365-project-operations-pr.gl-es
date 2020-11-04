---
title: Usar un campo existente en Project Service como dimensión de prezos
description: Este tema fornece información sobre o uso dos campos existentes de Project Service como dimensións de prezos.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076210"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="9e3e3-103">Usar un campo existente en Project Service como dimensión de prezos</span><span class="sxs-lookup"><span data-stu-id="9e3e3-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="9e3e3-104">Project Service Automation (PSA) ten moitos campos na entidade **Datos reais** que poden usarse como dimensións de prezos para prezos baseados en recursos en organizacións de proxectos.</span><span class="sxs-lookup"><span data-stu-id="9e3e3-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="9e3e3-105">Por exemplo, un campo común é **Recurso reservable**.</span><span class="sxs-lookup"><span data-stu-id="9e3e3-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="9e3e3-106">As empresas máis pequenas que teñen menos de 20-30 recursos facturables poden considerar que ter unha taxas de facturación e custos específicas para cada recurso é un enfoque máis sinxelo.</span><span class="sxs-lookup"><span data-stu-id="9e3e3-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="9e3e3-107">Non obstante, a medida que a forza de traballo facturable medra, isto podería resultar irreal, xa que as taxas de custos e facturación dos recursos comezan a variar a medida que os recursos ascenden, gañan máis experiencia ou adquiren diferentes conxuntos de habilidades.</span><span class="sxs-lookup"><span data-stu-id="9e3e3-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="9e3e3-108">Debido a que este enfoque aínda funciona para empresas de certo tamaño, consulte o tema [Usar un recurso reservable como dimensión de prezos](bookable-resource-pricing-dimension.md) para comprender como se pode usar un campo de Project Service existente como dimensión de prezos.</span><span class="sxs-lookup"><span data-stu-id="9e3e3-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="9e3e3-109">Outro exemplo é o da categoría de transaccións.</span><span class="sxs-lookup"><span data-stu-id="9e3e3-109">Another example is that of transaction category.</span></span> <span data-ttu-id="9e3e3-110">Os clientes e implementadores utilizaron a categoría de transaccións en PSA para clasificar o traballo e usan o campo para prezo e custo en función da categoría de traballo.</span><span class="sxs-lookup"><span data-stu-id="9e3e3-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="9e3e3-111">Para obter máis información, consulte [Usar a categoría de transaccións como dimensión de prezos](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="9e3e3-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
