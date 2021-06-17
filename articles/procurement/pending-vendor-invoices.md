---
title: Comprar materiais sen fornecemento usando unha factura pendente de fornecedor
description: Este tema explica como rexistrar as facturas pendentes do fornecedor.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993789"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="fc7b0-103">Comprar materiais sen fornecemento usando unha factura pendente de fornecedor</span><span class="sxs-lookup"><span data-stu-id="fc7b0-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="fc7b0-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="fc7b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fc7b0-105">Cando unha empresa adquire materiais sen fornecemento para un proxecto, os custos pódense rexistrar de inmediato no proxecto.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="fc7b0-106">Por exemplo, Contoso Robotics US está a realizar un proxecto de renovación de equipos e precisa licenzas de software.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="fc7b0-107">Estas licenzas adquírense a un fornecedor externo.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="fc7b0-108">Usando Dynamics 365 Finance, o empregado de contas pendentes de pago rexistra un documento de factura pendente do fornecedor e atribúe os custos da licenza directamente ao proxecto de renovación de equipos.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="fc7b0-109">Antes de empregar a funcionalidade descrita neste tema, revise e aplique as configuracións necesarias.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="fc7b0-110">Para obter máis información, consulte [Activa materiais sen fornecemento e facturas pendentes do fornecedor](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="fc7b0-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="fc7b0-111">Enviar unha factura pendente fornecedor relacionada co proxecto</span><span class="sxs-lookup"><span data-stu-id="fc7b0-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="fc7b0-112">As facturas pendentes do fornecedor poden rexistrarse na páxina **Facturas pendentes do fornecedor** (**Contas pendentes de pago** > **Facturas** > **Facturas pendentes do fornecedor**).</span><span class="sxs-lookup"><span data-stu-id="fc7b0-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="fc7b0-113">Complete os seguintes pasos para publicar unha factura pendente do fornecedor relacionada co proxecto:</span><span class="sxs-lookup"><span data-stu-id="fc7b0-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="fc7b0-114">Vaia a **Contas pendentes de pago** > **Facturas** e seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="fc7b0-115">No campo **Conta de factura**, seleccione un fornecedor e no campo **Número**, introduza a identificación da factura do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="fc7b0-116">Engada unha liña á factura do fornecedor e no campo **Número de elemento**, seleccione o elemento sen fornecemento comprado ao fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fc7b0-117">As liñas de factura do fornecedor baseadas nunha categoría de adquisición non se poden rexistrar no proxecto.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="fc7b0-118">Engada a cantidade comprada.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-118">Add the quantity purchased.</span></span> <span data-ttu-id="fc7b0-119">O sistema encherá o prezo unitario en función da configuración do prezo do elemento sen fornecemento.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="fc7b0-120">Verifique o importe total e outros detalles requiridos na liña.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="fc7b0-121">Nos detalles da liña, no separador **Proxecto**, seleccione o ID do proxecto no que se rexistrará este elemento.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="fc7b0-122">Opcionalmente, seleccione o número de actividade e actualice a categoría do proxecto e a propiedade da liña.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="fc7b0-123">Contabilice a factura pendente do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-123">Post pending vendor invoice.</span></span> <span data-ttu-id="fc7b0-124">Cando se contabiliza a factura, o sistema rexistra:</span><span class="sxs-lookup"><span data-stu-id="fc7b0-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="fc7b0-125">O importe do saldo do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="fc7b0-126">O importe do imposto de vendas.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-126">The sales tax amount.</span></span>
    - <span data-ttu-id="fc7b0-127">O custo contra o proxecto rexístrase na conta de integración de adquisicións.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="fc7b0-128">A transacción real do proxecto en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="fc7b0-129">Esta transacción procésase mediante o [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="fc7b0-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="fc7b0-130">Ao contabilizar este diario móvese o importe da conta de integración de adquisicións á conta de custos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="fc7b0-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
