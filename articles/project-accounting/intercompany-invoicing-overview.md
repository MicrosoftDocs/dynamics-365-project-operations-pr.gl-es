---
title: Visión xeral da facturación entre empresas
description: Este tema ofrece información e exemplos sobre a facturación entre empresas para proxectos.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287326"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="5e825-103">Visión xeral da facturación entre empresas</span><span class="sxs-lookup"><span data-stu-id="5e825-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="5e825-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="5e825-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5e825-105">A súa organización pode ter varias divisións, filiais e outras persoas xurídicas que se transfiren produtos e servizos entre si para proxectos.</span><span class="sxs-lookup"><span data-stu-id="5e825-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="5e825-106">A entidade legal que presta o servizo ou fornece o produto chámase *entidade legal prestamista*.</span><span class="sxs-lookup"><span data-stu-id="5e825-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="5e825-107">A entidade legal que recibe o servizo ou produto chámase *entidade legal prestameira*.</span><span class="sxs-lookup"><span data-stu-id="5e825-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="5e825-108">A seguinte ilustración mostra un escenario típico no que dúas entidades legais, Contoso Robotics USA (a entidade legal en prestameira) e Contoso Robotics UK (a entidade legal prestamista), comparten recursos para entregar un proxecto ao cliente, Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="5e825-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="5e825-109">Para este escenario, Contoso Robotics USA está contratada para entregar o traballo a Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="5e825-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Facturación entre empresas](./media/IntercompanyScenario.png) 

<span data-ttu-id="5e825-111">Dynamics 365 Project Operations usa o seguinte fluxo para procesar transaccións entre empresas:</span><span class="sxs-lookup"><span data-stu-id="5e825-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="5e825-112">Os recursos da entidade legal prestameira rexistran as transaccións de tempo ou gasto entre empresas reservando o tempo e os gastos contra proxectos da entidade legal prestameira.</span><span class="sxs-lookup"><span data-stu-id="5e825-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="5e825-113">Os custos de tempo e gasto rexístranse na empresa prestameira empregando a lista de prezos de custo unitarios da empresa prestameira.</span><span class="sxs-lookup"><span data-stu-id="5e825-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="5e825-114">As transaccións de vendas sen facturar entre empresas rexístranse na empresa prestameira empregando a lista de prezos de custo unitarios da empresa prestameira.</span><span class="sxs-lookup"><span data-stu-id="5e825-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="5e825-115">Os ingresos non facturados rexístranse na empresa prestameira mediante a lista de prezos de venda do contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e825-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="5e825-116">Pódese facturar ao cliente cando se rexistran ingresos non facturados.</span><span class="sxs-lookup"><span data-stu-id="5e825-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="5e825-117">O cliente non ten que esperar a que remate o procesamento de facturas entre empresas.</span><span class="sxs-lookup"><span data-stu-id="5e825-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="5e825-118">As facturas de clientes entre empresas créanse periodicamente na empresa prestamista.</span><span class="sxs-lookup"><span data-stu-id="5e825-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="5e825-119">As facturas créanse manualmente ou mediante un proceso automatizado periódico.</span><span class="sxs-lookup"><span data-stu-id="5e825-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="5e825-120">Pódese crear unha única factura por cada entidade xurídica prestameira ou pódense crear facturas separadas por proxecto.</span><span class="sxs-lookup"><span data-stu-id="5e825-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="5e825-121">Cando a factura de cliente entre empresas se contabiliza na entidade legal prestamista, a factura de fornecedor pendente correspondente créase na entidade legal prestameira.</span><span class="sxs-lookup"><span data-stu-id="5e825-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="5e825-122">Os custos da factura do fornecedor pendente rexistraranse no subprograma do proxecto cando se contabilice a factura.</span><span class="sxs-lookup"><span data-stu-id="5e825-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="5e825-123">O seguinte diagrama ilustra a facturación entre empresas relacionada con eventos de contabilidade e anotacións esperadas no libro maior xeral.</span><span class="sxs-lookup"><span data-stu-id="5e825-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Fluxo entre empresas](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="5e825-125">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5e825-125">Additional resources</span></span>

- [<span data-ttu-id="5e825-126">Configurar a facturación entre empresas</span><span class="sxs-lookup"><span data-stu-id="5e825-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="5e825-127">Rexistrar transaccións entre empresas</span><span class="sxs-lookup"><span data-stu-id="5e825-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="5e825-128">Crear facturas entre empresas de clientes e fornecedores</span><span class="sxs-lookup"><span data-stu-id="5e825-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]