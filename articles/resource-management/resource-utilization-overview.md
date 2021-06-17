---
title: Visión xeral da utilización de recursos
description: Este tema fornece información sobre a utilización de recursos en Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000794"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="5873b-103">Visión xeral da utilización de recursos</span><span class="sxs-lookup"><span data-stu-id="5873b-103">Resource utilization overview</span></span>

<span data-ttu-id="5873b-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="5873b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5873b-105">Os recursos poden ter unha utilización facturable obxectivo.</span><span class="sxs-lookup"><span data-stu-id="5873b-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="5873b-106">Esta utilización obxectivo defínese como un atributo no rol predefinido dun recurso ou establécese no rexistro do recurso reservable individual.</span><span class="sxs-lookup"><span data-stu-id="5873b-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="5873b-107">Os cálculos de utilización baséanse nas horas reais que os recursos comunicaron mediante entradas de tempo aprobadas.</span><span class="sxs-lookup"><span data-stu-id="5873b-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="5873b-108">Para o cálculo da utilización úsanse as seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="5873b-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="5873b-109">Utilización facturable = (Horas reais imputables) ÷ (Capacidade do recurso).</span><span class="sxs-lookup"><span data-stu-id="5873b-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="5873b-110">Utilización non facturable = Tempo real con ID de tipo de facturación = Non imputable, Gratuíto ou Non dispoñible ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5873b-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="5873b-111">Interno = Tempo real sen contrato de vendas ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5873b-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="5873b-112">Capacidade do recurso = Horas laborables do recurso - Fóra de oficina - Días non laborables</span><span class="sxs-lookup"><span data-stu-id="5873b-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="5873b-113">Podes atopar a vista **Utilización de recursos** no panel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="5873b-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="5873b-114">Cada cela da grade representa a porcentaxe de utilización facturable do recurso nun período, como un día, unha semana ou un mes.</span><span class="sxs-lookup"><span data-stu-id="5873b-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="5873b-115">Para o color das celas úsanse as seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="5873b-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="5873b-116">**Verde**: utilización facturable > = utilización de destino de recursos</span><span class="sxs-lookup"><span data-stu-id="5873b-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="5873b-117">**Amarelo**: utilización de destino – 20 < = utilización facturable < utilización de destino</span><span class="sxs-lookup"><span data-stu-id="5873b-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="5873b-118">**Vermello**: utilización facturable < utilization de destino – 20</span><span class="sxs-lookup"><span data-stu-id="5873b-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="5873b-119">Debido a que a vista **Utilización de recursos** está baseada no panel de programación, pode empregar as capacidades de filtrado do panel de programación para filtrar os seus resultados.</span><span class="sxs-lookup"><span data-stu-id="5873b-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="5873b-120">A grade require que estableza unha utilización obxectivo no rol ou o recurso individual.</span><span class="sxs-lookup"><span data-stu-id="5873b-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="5873b-121">Para configurar isto, vaia a **Recursos** > **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="5873b-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="5873b-122">Ademais, debe atribuírse un rol predefinido a cada recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="5873b-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="5873b-123">Vaia a **Recursos** > **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="5873b-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="5873b-124">No separador **Project Service**, verifique se está definido un rol de recurso e que o campo **É predefinido** está configurado en **Si**.</span><span class="sxs-lookup"><span data-stu-id="5873b-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="5873b-125">Pode engadir roles adicionais cando **É predefinido** = **Non**.</span><span class="sxs-lookup"><span data-stu-id="5873b-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="5873b-126">O rol cando **É predefinido** = **Si** úsase para avaliar a utilización do recurso fronte ao obxectivo para ese rol.</span><span class="sxs-lookup"><span data-stu-id="5873b-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="5873b-127">No separador **Project Service**, tamén pode configurar unha utilización obxectivo individual para o recurso.</span><span class="sxs-lookup"><span data-stu-id="5873b-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="5873b-128">A seguir, o cálculo de utilización usa esa utilización obxectivo para avaliar o obxectivo do recurso no canto do obxectivo do rol predefinido do recurso.</span><span class="sxs-lookup"><span data-stu-id="5873b-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="5873b-129">A utilización móstrase só para un recurso só se ese recurso ten un tempo imputable acordado durante o período que se amosa na grade.</span><span class="sxs-lookup"><span data-stu-id="5873b-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]