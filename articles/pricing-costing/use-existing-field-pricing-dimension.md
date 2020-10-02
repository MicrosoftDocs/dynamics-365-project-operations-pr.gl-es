---
title: Campos de Project Operations como dimensións de prezos
description: Este tema fornece información sobre o uso dos campos como dimensións de prezos en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896414"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="6efac-103">Campos de Project Operations como dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="6efac-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="6efac-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="6efac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6efac-105">A entidade **Datos reais** ten moitos campos que se poden usar como dimensións de prezos para os prezos baseados en recursos.</span><span class="sxs-lookup"><span data-stu-id="6efac-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="6efac-106">Por exemplo, un campo común é **Recurso reservable**.</span><span class="sxs-lookup"><span data-stu-id="6efac-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="6efac-107">As empresas máis pequenas que teñen menos de 20-30 recursos facturables poden considerar que ter unha taxas de facturación e custos específicas para cada recurso é un enfoque máis sinxelo.</span><span class="sxs-lookup"><span data-stu-id="6efac-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="6efac-108">Non obstante, a medida que medra o persoal facturable, podería ser pouco realista manter as taxas específicas dos recursos.</span><span class="sxs-lookup"><span data-stu-id="6efac-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="6efac-109">O custo dos recursos e as taxas de facturación comezan a variar a medida que os recursos ascenden, gañan máis experiencia ou adquiren un conxunto diferente de habilidades.</span><span class="sxs-lookup"><span data-stu-id="6efac-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="6efac-110">Outro exemplo é o da categoría de transaccións.</span><span class="sxs-lookup"><span data-stu-id="6efac-110">Another example is that of transaction category.</span></span> <span data-ttu-id="6efac-111">Os clientes e implementadores utilizaron a categoría de transaccións para clasificar o traballo e usan o campo para prezo e custo en función da categoría de traballo.</span><span class="sxs-lookup"><span data-stu-id="6efac-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
