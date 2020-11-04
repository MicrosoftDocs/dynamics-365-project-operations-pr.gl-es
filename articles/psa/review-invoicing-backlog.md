---
title: Revisar os traballos pendentes de facturación en proxectos e contratos de proxectos
description: Este tema fornece información sobre como revisar o traballo pendente de facturación de tempo, gasto e produtos e como marcalos como listos para a facturación.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076341"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="7fff5-103">Revisar os traballos pendentes de facturación en proxectos e contratos de proxectos</span><span class="sxs-lookup"><span data-stu-id="7fff5-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7fff5-104">Cando unha transacción está lista para crear e procesar unha factura, a operación debería marcarse como **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="7fff5-105">Este tema describe os tipos de transaccións que se poden crear.</span><span class="sxs-lookup"><span data-stu-id="7fff5-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="7fff5-106">Revisar o traballo pendente de facturación de tempo e material</span><span class="sxs-lookup"><span data-stu-id="7fff5-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="7fff5-107">Cando se presenta e aproba unha entrada de tempo ou gasto para un proxecto, PSA crea un dato real de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7fff5-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="7fff5-108">Se a combinación do proxecto e a clase de transacción están asignadas a unha liña de contrato para un proxecto de tempo e materiais, créanse dous datos reais cando se aproba a entrada:</span><span class="sxs-lookup"><span data-stu-id="7fff5-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="7fff5-109">Dato real de custo</span><span class="sxs-lookup"><span data-stu-id="7fff5-109">Cost actual</span></span> 
- <span data-ttu-id="7fff5-110">Dato real de vendas sen facturar</span><span class="sxs-lookup"><span data-stu-id="7fff5-110">Unbilled sales actual</span></span>

<span data-ttu-id="7fff5-111">Os datos reais de vendas sen facturar representan o traballo pendente de facturación e hai que establecer o seu estado de facturación en **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="7fff5-112">Cando se crea unha factura do proxecto, os datos reais de vendas sen facturar que están marcados como **Listo para facturar** cópianse como detalles da liña de factura.</span><span class="sxs-lookup"><span data-stu-id="7fff5-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="7fff5-113">Para revisar o calendario de facturación de tempo e materiais, vaia a **Vendas** \> **Facturación** \> **Traballo pendente de facturación de tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="7fff5-114">Seleccione todos os datos reais de vendas sen facturar listas para ser facturadas e logo seleccione **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="7fff5-115">O estado de facturación destes datos reais cambia a **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Traballo pendente de facturación de tempo e material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="7fff5-117">Revisar o traballo pendente de facturación de produtos</span><span class="sxs-lookup"><span data-stu-id="7fff5-117">Review the product billing backlog</span></span>

<span data-ttu-id="7fff5-118">En PSA, cando un contrato de proxecto ten liñas de contrato baseadas en produtos, considéranse esas liñas para facturar sempre que se cree unha factura para o contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="7fff5-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="7fff5-119">Calquera produto que teña liñas de contrato que están marcadas como **Listo para facturar** cópiase na factura do proxecto como liñas de factura do proxecto.</span><span class="sxs-lookup"><span data-stu-id="7fff5-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="7fff5-120">Para revisar o traballo pendente de facturación de produtos, vaia a **Vendas** \> **Facturación de produtos** \> **Traballo pendente de facturación de produtos**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="7fff5-121">Seleccione todas liñas de contrato baseadas en produtos que están listas para ser facturadas e logo seleccione **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="7fff5-122">O estado de facturación destas liñas cambia a **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Traballo pendente de facturación de produtos](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="7fff5-124">Revisar os fitos de facturación de contratos de prezo fixo</span><span class="sxs-lookup"><span data-stu-id="7fff5-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="7fff5-125">Cada liña de contrato de proxecto que teña un método de facturación de prezo fixo debe definir os fitos do contrato.</span><span class="sxs-lookup"><span data-stu-id="7fff5-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="7fff5-126">Estes fitos do contrato pódense facturar só se están marcados como **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="7fff5-127">Para revisar os fitos de facturación, vaia a **Vendas** \> **Facturación** \> **Fitos de prezo fixo**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="7fff5-128">Seleccione todos os fitos listos para ser facturados e logo seleccione **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="7fff5-129">O estado de facturación destes fitos cambia a **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="7fff5-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Fitos de prezo fixo](media/FPBacklog.png)
