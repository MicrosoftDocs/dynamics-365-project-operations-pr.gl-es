---
title: Visión xeral do recoñecemento de ingresos
description: Este tema fornece información sobre o recoñecemento de ingresos en Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368024"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="83411-103">Visión xeral do recoñecemento de ingresos</span><span class="sxs-lookup"><span data-stu-id="83411-103">Revenue recognition overview</span></span>

<span data-ttu-id="83411-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="83411-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="83411-105">En Dynamics 365 Project Operations, os principios de recoñecemento de ingresos varían en función do método de facturación seleccionado para un proxecto ou parte do proxecto.</span><span class="sxs-lookup"><span data-stu-id="83411-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="83411-106">Este tema fornece información sobre o recoñecemento de ingresos en Project Operations.</span><span class="sxs-lookup"><span data-stu-id="83411-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="83411-107">Transaccións contabilizadas mediante o método de facturación de tempo e material</span><span class="sxs-lookup"><span data-stu-id="83411-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="83411-108">O custo e o recoñecemento de ingresos están conectados.</span><span class="sxs-lookup"><span data-stu-id="83411-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="83411-109">O custo da transacción e as vendas non facturadas contabilízanse mediante o [diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="83411-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="83411-110">O custo do proxecto e o perfil de ingresos determinan se as transaccións de vendas non facturadas se contabilizan no libro maior.</span><span class="sxs-lookup"><span data-stu-id="83411-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="83411-111">Se **Acumular ingresos** está seleccionado, o sistema usa as contas **Valor das vendas WIP** e **Valor das vendas de ingresos acumulados** durante a contabilización.</span><span class="sxs-lookup"><span data-stu-id="83411-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="83411-112">O seguinte é un exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="83411-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="83411-113">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="83411-113">Transaction type</span></span> | <span data-ttu-id="83411-114">Débito/crédito</span><span class="sxs-lookup"><span data-stu-id="83411-114">Debit/Credit</span></span> | <span data-ttu-id="83411-115">Importe </span><span class="sxs-lookup"><span data-stu-id="83411-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="83411-116">Valor de vendas WIP</span><span class="sxs-lookup"><span data-stu-id="83411-116">WIP Sales value</span></span> | <span data-ttu-id="83411-117">Débito</span><span class="sxs-lookup"><span data-stu-id="83411-117">Debit</span></span> | <span data-ttu-id="83411-118">100</span><span class="sxs-lookup"><span data-stu-id="83411-118">100</span></span> |
  | <span data-ttu-id="83411-119">Valos de vendas de ingresos acumulados</span><span class="sxs-lookup"><span data-stu-id="83411-119">Accrued revenue sales value</span></span> | <span data-ttu-id="83411-120">Crédito</span><span class="sxs-lookup"><span data-stu-id="83411-120">Credit</span></span> | <span data-ttu-id="83411-121">100</span><span class="sxs-lookup"><span data-stu-id="83411-121">100</span></span> |

- <span data-ttu-id="83411-122">Os ingresos se recoñecen durante a facturación.</span><span class="sxs-lookup"><span data-stu-id="83411-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="83411-123">O sistema usa a conta **Ingresos facturados** durante a contabilización.</span><span class="sxs-lookup"><span data-stu-id="83411-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="83411-124">O seguinte é un exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="83411-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="83411-125">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="83411-125">Transaction type</span></span> | <span data-ttu-id="83411-126">Débito/crédito</span><span class="sxs-lookup"><span data-stu-id="83411-126">Debit/Credit</span></span> | <span data-ttu-id="83411-127">Importe </span><span class="sxs-lookup"><span data-stu-id="83411-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="83411-128">Saldo de cliente</span><span class="sxs-lookup"><span data-stu-id="83411-128">Customer balance</span></span> | <span data-ttu-id="83411-129">Débito</span><span class="sxs-lookup"><span data-stu-id="83411-129">Debit</span></span> | <span data-ttu-id="83411-130">120</span><span class="sxs-lookup"><span data-stu-id="83411-130">120</span></span> |
  | <span data-ttu-id="83411-131">Imposto de vendas pendente de pago</span><span class="sxs-lookup"><span data-stu-id="83411-131">Sales tax payable</span></span> | <span data-ttu-id="83411-132">Crédito</span><span class="sxs-lookup"><span data-stu-id="83411-132">Credit</span></span> | <span data-ttu-id="83411-133">20</span><span class="sxs-lookup"><span data-stu-id="83411-133">20</span></span> |
  | <span data-ttu-id="83411-134">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="83411-134">Invoiced Revenue</span></span> | <span data-ttu-id="83411-135">Crédito</span><span class="sxs-lookup"><span data-stu-id="83411-135">Credit</span></span> | <span data-ttu-id="83411-136">100</span><span class="sxs-lookup"><span data-stu-id="83411-136">100</span></span> |

- <span data-ttu-id="83411-137">Se se acumularon ingresos cando se contabilizan as vendas non facturadas, o sistema reverterá os ingresos acumulados na facturación.</span><span class="sxs-lookup"><span data-stu-id="83411-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="83411-138">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="83411-138">Transaction type</span></span> | <span data-ttu-id="83411-139">Débito/crédito</span><span class="sxs-lookup"><span data-stu-id="83411-139">Debit/Credit</span></span> | <span data-ttu-id="83411-140">Importe </span><span class="sxs-lookup"><span data-stu-id="83411-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="83411-141">Valor de vendas WIP</span><span class="sxs-lookup"><span data-stu-id="83411-141">WIP Sales value</span></span> | <span data-ttu-id="83411-142">Crédito</span><span class="sxs-lookup"><span data-stu-id="83411-142">Credit</span></span> | <span data-ttu-id="83411-143">100</span><span class="sxs-lookup"><span data-stu-id="83411-143">100</span></span> |
  | <span data-ttu-id="83411-144">Valos de vendas de ingresos acumulados</span><span class="sxs-lookup"><span data-stu-id="83411-144">Accrued revenue sales value</span></span> | <span data-ttu-id="83411-145">Débito</span><span class="sxs-lookup"><span data-stu-id="83411-145">Debit</span></span> | <span data-ttu-id="83411-146">100</span><span class="sxs-lookup"><span data-stu-id="83411-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="83411-147">Transaccións contabilizadas mediante o método de facturación de prezo fixo</span><span class="sxs-lookup"><span data-stu-id="83411-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="83411-148">O custo e o recoñecemento de ingresos están separados.</span><span class="sxs-lookup"><span data-stu-id="83411-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="83411-149">O custo da transacción contabilízase mediante o [diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="83411-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="83411-150">Non se crean transaccións de vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="83411-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="83411-151">Os ingresos pódense recoñecer durante a facturación se o custo do proxecto e o perfil de ingresos teñen **Principio empregado para os cálculos de finalización do proxecto** definido como **Sen WIP**.</span><span class="sxs-lookup"><span data-stu-id="83411-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="83411-152">Use este método só para proxectos sinxelos a curto prazo.</span><span class="sxs-lookup"><span data-stu-id="83411-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="83411-153">Os ingresos pódense recoñecer empregando estimacións de ingresos a prezos fixos, co método **Contrato completado** ou **Recoñecemento de ingresos por conclusión porcentual**.</span><span class="sxs-lookup"><span data-stu-id="83411-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83411-154">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="83411-154">Additional resources</span></span>
[<span data-ttu-id="83411-155">Configurar a contabilidade para artigo de proxectos facturables</span><span class="sxs-lookup"><span data-stu-id="83411-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="83411-156">Proxectos de estimación de ingresos a prezo fixo</span><span class="sxs-lookup"><span data-stu-id="83411-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="83411-157">Xestionar estimacións de ingresos</span><span class="sxs-lookup"><span data-stu-id="83411-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="83411-158">Métodos de custo para completar</span><span class="sxs-lookup"><span data-stu-id="83411-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]