---
title: Campos de Project Operations como dimensións de prezos
description: Este tema fornece información sobre o uso de campos como dimensións de prezos en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274636"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="68489-103">Campos de Project Operations como dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="68489-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="68489-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="68489-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="68489-105">A entidade **Datos reais** ten moitos campos que se poden usar como dimensións de prezos para os prezos baseados en recursos.</span><span class="sxs-lookup"><span data-stu-id="68489-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="68489-106">Por exemplo, un campo común é **Recurso reservable**.</span><span class="sxs-lookup"><span data-stu-id="68489-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="68489-107">As empresas máis pequenas que teñen menos de 20-30 recursos facturables poden considerar que ter unha taxas de facturación e custos específicas para cada recurso é un enfoque máis sinxelo.</span><span class="sxs-lookup"><span data-stu-id="68489-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="68489-108">Non obstante, a medida que medra o persoal facturable, podería ser pouco realista manter as taxas específicas dos recursos.</span><span class="sxs-lookup"><span data-stu-id="68489-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="68489-109">O custo dos recursos e as taxas de facturación comezan a variar a medida que os recursos ascenden, gañan máis experiencia ou adquiren un conxunto diferente de habilidades.</span><span class="sxs-lookup"><span data-stu-id="68489-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="68489-110">Outro exemplo é o da categoría de transaccións.</span><span class="sxs-lookup"><span data-stu-id="68489-110">Another example is that of transaction category.</span></span> <span data-ttu-id="68489-111">Os clientes e implementadores utilizaron a categoría de transaccións para clasificar o traballo e usan o campo para prezo e custo en función da categoría de traballo.</span><span class="sxs-lookup"><span data-stu-id="68489-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]