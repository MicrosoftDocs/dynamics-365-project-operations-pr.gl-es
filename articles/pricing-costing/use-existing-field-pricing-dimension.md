---
title: Campos de Project Operations como dimensións de prezos
description: Este tema fornece información sobre o uso de campos como dimensións de prezos en Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004484"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="ad3fe-103">Campos de Project Operations como dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="ad3fe-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="ad3fe-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="ad3fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ad3fe-105">A entidade **Datos reais** ten moitos campos que se poden usar como dimensións de prezos para os prezos baseados en recursos.</span><span class="sxs-lookup"><span data-stu-id="ad3fe-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="ad3fe-106">Por exemplo, un campo común é **Recurso reservable**.</span><span class="sxs-lookup"><span data-stu-id="ad3fe-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="ad3fe-107">As empresas máis pequenas que teñen menos de 20-30 recursos facturables poden considerar que ter unha taxas de facturación e custos específicas para cada recurso é un enfoque máis sinxelo.</span><span class="sxs-lookup"><span data-stu-id="ad3fe-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="ad3fe-108">Non obstante, a medida que medra o persoal facturable, podería ser pouco realista manter as taxas específicas dos recursos.</span><span class="sxs-lookup"><span data-stu-id="ad3fe-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="ad3fe-109">O custo dos recursos e as taxas de facturación comezan a variar a medida que os recursos ascenden, gañan máis experiencia ou adquiren un conxunto diferente de habilidades.</span><span class="sxs-lookup"><span data-stu-id="ad3fe-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="ad3fe-110">Outro exemplo é o da categoría de transaccións.</span><span class="sxs-lookup"><span data-stu-id="ad3fe-110">Another example is that of transaction category.</span></span> <span data-ttu-id="ad3fe-111">Os clientes e implementadores utilizaron a categoría de transaccións para clasificar o traballo e usan o campo para prezo e custo en función da categoría de traballo.</span><span class="sxs-lookup"><span data-stu-id="ad3fe-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]