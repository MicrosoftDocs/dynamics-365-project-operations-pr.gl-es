---
title: Tipos de fases de proxecto
description: Neste tema se proporciona información sobre as fases do proxecto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148101"
---
# <a name="project-stage-types"></a><span data-ttu-id="8c4ad-103">Tipos de fases de proxecto</span><span class="sxs-lookup"><span data-stu-id="8c4ad-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8c4ad-104">As fases do proxecto están deseñadas para reflectir o estado do proxecto a medida que progresa.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="8c4ad-105">Pódense utilizar as personalizacións para actualizar automaticamente as fases con fluxos de proceso de negocio, Power Automate ou extensións de complementos.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="8c4ad-106">No BPF por defecto defínense as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="8c4ad-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="8c4ad-107">Nova</span><span class="sxs-lookup"><span data-stu-id="8c4ad-107">New</span></span>
- <span data-ttu-id="8c4ad-108">Oferta</span><span class="sxs-lookup"><span data-stu-id="8c4ad-108">Quote</span></span>
- <span data-ttu-id="8c4ad-109">Planificar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-109">Plan</span></span>
- <span data-ttu-id="8c4ad-110">Entregar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-110">Deliver</span></span>
- <span data-ttu-id="8c4ad-111">Completar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-111">Complete</span></span>
- <span data-ttu-id="8c4ad-112">Pechar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="8c4ad-113">Novo</span><span class="sxs-lookup"><span data-stu-id="8c4ad-113">New</span></span>

<span data-ttu-id="8c4ad-114">Ao crear un proxecto, a fase do proxecto defínese como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="8c4ad-115">Se o proxecto se creou a partir dun modelo, pode que teña datos de programación, estimación e equipo.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="8c4ad-116">Se non, é só un esquema do proxecto e deben introducirse os compoñentes restantes.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="8c4ad-117">Oferta</span><span class="sxs-lookup"><span data-stu-id="8c4ad-117">Quote</span></span>

<span data-ttu-id="8c4ad-118">Cando asocia un proxecto a unha oferta ou cando crea un proxecto a partir dunha oferta, a fase de proxecto está definida en **Oferta**, e as datas de inicio e fin estimadas tamén se actualizan.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="8c4ad-119">Mentres o proxecto está na fase de **Oferta**, o separador **Vendas** da páxina **Entidade do proxecto** mostra detalles da oferta.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="8c4ad-120">Planificar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-120">Plan</span></span>

<span data-ttu-id="8c4ad-121">Cando gaña unha oferta asociada a un proxecto, e o proxecto se move á fase **Contrato**, a fase do proxecto actualízase a **Planificar**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="8c4ad-122">Mentres o proxecto está na fase **Planificar**, a páxina **Entidade do proxecto** mostra detalles do contrato.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="8c4ad-123">Entregar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-123">Deliver</span></span>

<span data-ttu-id="8c4ad-124">Cando o plan do proxecto estea finalizado e vostede estea listo para iniciar o proxecto, o xestor de proxectos debería actualizar a fase do proxecto a **Entregar** para demostrar que o proxecto comezou.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="8c4ad-125">Finalizar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-125">Complete</span></span> 

<span data-ttu-id="8c4ad-126">Cando o traballo para o proxecto estea rematado, o xestor de proxectos pode actualizar a fase a **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="8c4ad-127">Ao actualizar a fase do proxecto a **Finalizar**, o xestor de proxectos indica que o traballo está finalizado ao 100 por cento, pero que o proxecto se mantén aberto para que se poida rexistrar calquera entrada de tempo ou gasto pendente.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="8c4ad-128">Pechar</span><span class="sxs-lookup"><span data-stu-id="8c4ad-128">Close</span></span>

<span data-ttu-id="8c4ad-129">Cando todas as transaccións do proxecto estean rexistradas, o xestor de proxectos pode actualizar a fase a **Pechar**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="8c4ad-130">Nese momento, non se poden rexistrar transaccións e o proxecto configúrase como só de lectura.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
