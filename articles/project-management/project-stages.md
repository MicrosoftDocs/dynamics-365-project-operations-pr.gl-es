---
title: Fases do proxecto
description: Este tema ofrece información sobre as fases do proxecto dispoñibles en Microsoft Dynamics Project Operations.
author: ruhercul
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
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996924"
---
# <a name="project-stages"></a><span data-ttu-id="edefe-103">Fases do proxecto</span><span class="sxs-lookup"><span data-stu-id="edefe-103">Project stages</span></span>

<span data-ttu-id="edefe-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="edefe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="edefe-105">As fases do proxecto están deseñadas para reflectir o estado do proxecto a medida que progresa.</span><span class="sxs-lookup"><span data-stu-id="edefe-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="edefe-106">Pódense utilizar as personalizacións para actualizar automaticamente as fases con fluxos de proceso de negocio, Power Automate ou extensións de complementos.</span><span class="sxs-lookup"><span data-stu-id="edefe-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="edefe-107">No fluxo do proceso de negocio por defecto defínense as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="edefe-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="edefe-108">Nova</span><span class="sxs-lookup"><span data-stu-id="edefe-108">New</span></span>
- <span data-ttu-id="edefe-109">Oferta</span><span class="sxs-lookup"><span data-stu-id="edefe-109">Quote</span></span>
- <span data-ttu-id="edefe-110">Plan</span><span class="sxs-lookup"><span data-stu-id="edefe-110">Plan</span></span>
- <span data-ttu-id="edefe-111">Entregar</span><span class="sxs-lookup"><span data-stu-id="edefe-111">Deliver</span></span>
- <span data-ttu-id="edefe-112">Completado</span><span class="sxs-lookup"><span data-stu-id="edefe-112">Complete</span></span>
- <span data-ttu-id="edefe-113">Pechar</span><span class="sxs-lookup"><span data-stu-id="edefe-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="edefe-114">Nova</span><span class="sxs-lookup"><span data-stu-id="edefe-114">New</span></span>

<span data-ttu-id="edefe-115">Ao crear un proxecto, a fase do proxecto defínese como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="edefe-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="edefe-116">Se o proxecto se creou a partir dun modelo, pode que teña datos de programación, estimación e equipo.</span><span class="sxs-lookup"><span data-stu-id="edefe-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="edefe-117">Se non, é un esquema do proxecto e deben introducirse os compoñentes restantes.</span><span class="sxs-lookup"><span data-stu-id="edefe-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="edefe-118">Oferta</span><span class="sxs-lookup"><span data-stu-id="edefe-118">Quote</span></span>

<span data-ttu-id="edefe-119">Cando asocia un proxecto a unha oferta ou cando crea un proxecto a partir dunha oferta, a fase de proxecto está definida en **Oferta**, e as datas de inicio e fin estimadas tamén se actualizan.</span><span class="sxs-lookup"><span data-stu-id="edefe-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="edefe-120">Mentres o proxecto está na fase de **Oferta**, o separador **Vendas** da páxina **Entidade do proxecto** mostra detalles da oferta.</span><span class="sxs-lookup"><span data-stu-id="edefe-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="edefe-121">Planificar</span><span class="sxs-lookup"><span data-stu-id="edefe-121">Plan</span></span>

<span data-ttu-id="edefe-122">Cando gaña unha oferta asociada a un proxecto, e o proxecto se move á fase **Contrato**, a fase do proxecto actualízase a **Planificar**.</span><span class="sxs-lookup"><span data-stu-id="edefe-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="edefe-123">Mentres o proxecto está na fase **Planificar**, a páxina **Entidade do proxecto** mostra detalles do contrato.</span><span class="sxs-lookup"><span data-stu-id="edefe-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="edefe-124">Entregar</span><span class="sxs-lookup"><span data-stu-id="edefe-124">Deliver</span></span>

<span data-ttu-id="edefe-125">Cando o plan do proxecto estea finalizado e vostede estea listo para iniciar o proxecto, o xestor de proxectos debería actualizar a fase do proxecto a **Entregar** para demostrar que o proxecto comezou.</span><span class="sxs-lookup"><span data-stu-id="edefe-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="edefe-126">Finalizar</span><span class="sxs-lookup"><span data-stu-id="edefe-126">Complete</span></span> 

<span data-ttu-id="edefe-127">Cando o traballo para o proxecto estea rematado, o xestor de proxectos pode actualizar a fase a **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="edefe-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="edefe-128">Ao actualizar a fase do proxecto a **Finalizar**, o xestor de proxectos indica que o traballo está finalizado ao 100 por cento, pero que o proxecto se mantén aberto para que se poida rexistrar calquera entrada de tempo ou gasto pendente.</span><span class="sxs-lookup"><span data-stu-id="edefe-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="edefe-129">Pechar</span><span class="sxs-lookup"><span data-stu-id="edefe-129">Close</span></span>

<span data-ttu-id="edefe-130">Cando todas as transaccións do proxecto estean rexistradas, o xestor de proxectos pode actualizar a fase a **Pechar**.</span><span class="sxs-lookup"><span data-stu-id="edefe-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="edefe-131">Nese momento, non se poden rexistrar transaccións e o proxecto configúrase como só de lectura.</span><span class="sxs-lookup"><span data-stu-id="edefe-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]