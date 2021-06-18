---
title: Crear e aplicar os termos de retención do pagamento do fornecedor
description: Este tema ofrece información sobre como configurar e manter os termos de retención para os pagamentos do fornecedor.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006322"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="d27c2-103">Crear e aplicar os termos de retención do pagamento do fornecedor</span><span class="sxs-lookup"><span data-stu-id="d27c2-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="d27c2-104">Configurar as condicións de retención de pagamentos do fornecedor para un proxecto é útil cando a súa organización quere reter parte dos pagamentos realizados a un fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="d27c2-105">Por exemplo, cando quere reter o pagamento a un fornecedor ata que os produtos entregados cumpran as súas expectativas.</span><span class="sxs-lookup"><span data-stu-id="d27c2-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="d27c2-106">Pódense especificar as condicións de retención do pagamento do fornecedor cando negocie un contrato de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="d27c2-107">Crear os termos de retención do pagamento do fornecedor</span><span class="sxs-lookup"><span data-stu-id="d27c2-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="d27c2-108">Pode introducir a porcentaxe de pagamento do fornecedor para a retención e a porcentaxe das cantidades retidas anteriormente que se liberarán.</span><span class="sxs-lookup"><span data-stu-id="d27c2-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="d27c2-109">As cantidades retéñense automaticamente nas facturas do fornecedor ata que o contrato alcanza o estado especificado de finalización.</span><span class="sxs-lookup"><span data-stu-id="d27c2-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="d27c2-110">Despois de configurar os termos de retención, pode aplicalos a calquera proxecto dese fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="d27c2-111">Utilice os seguintes pasos para configurar e manter os termos de retención dos pagamentos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="d27c2-112">Vaia a **Xestión e contabilidade de proxectos** > **Retención** > **Condicións de retención do pagamento do fornecedor**.</span><span class="sxs-lookup"><span data-stu-id="d27c2-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="d27c2-113">Seleccione **Novo** para engadir un novo termo de retención do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="d27c2-114">O valor de **ID da regra** introdúcese automaticamente para o novo termo.</span><span class="sxs-lookup"><span data-stu-id="d27c2-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="d27c2-115">Introduza unha breve descrición no campo **Descrición** e no separador rápido **Termos**, seleccione **Engadir liña** para introducir valores de termo para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d27c2-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="d27c2-116">**Porcentaxe de unidades entregadas**: Introduza unha porcentaxe de finalización para o termo.</span><span class="sxs-lookup"><span data-stu-id="d27c2-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="d27c2-117">As cantidades retéñense automaticamente nas facturas do fornecedor ata que a fase de finalización do proxecto sexa igual á porcentaxe especificada.</span><span class="sxs-lookup"><span data-stu-id="d27c2-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="d27c2-118">Por exemplo, se introduce 50,00, as cantidades retéñense ata que o proxecto se complete nun 50 por cento.</span><span class="sxs-lookup"><span data-stu-id="d27c2-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="d27c2-119">**Porcentaxe para reter**: Insira unha porcentaxe do importe da factura do fornecedor que se reterá.</span><span class="sxs-lookup"><span data-stu-id="d27c2-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="d27c2-120">Por exemplo, se introduce 10,00, reterase o 10 por cento do importe da factura dun fornecedor ata que o proxecto alcance a porcentaxe de finalización establecida no campo **Porcentaxe de unidades entregadas**.</span><span class="sxs-lookup"><span data-stu-id="d27c2-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="d27c2-121">**Porcentaxe para liberar**: Seleccione **Engadir liña** para introducir unha porcentaxe de cantidades retidas anteriormente que se liberarán para o nivel seleccionado de finalización do proxecto.</span><span class="sxs-lookup"><span data-stu-id="d27c2-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="d27c2-122">Se ten máis dun fito para os diferentes niveis de finalización do proxecto, escriba unha liña de termo de retención do fornecedor separada para cada regra de retención.</span><span class="sxs-lookup"><span data-stu-id="d27c2-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="d27c2-123">Cada liña pode especificar unha porcentaxe de retención diferente e unha porcentaxe de liberación diferente para cada nivel designado de finalización do proxecto.</span><span class="sxs-lookup"><span data-stu-id="d27c2-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="d27c2-124">Despois de crear os termos de retención para un fornecedor, pode aplicar os termos a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="d27c2-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="d27c2-125">Aplicar os termos de retención do fornecedor a un proxecto</span><span class="sxs-lookup"><span data-stu-id="d27c2-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="d27c2-126">Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Todos os proxectos** e abra un proxecto desde a páxina da lista de proxectos.</span><span class="sxs-lookup"><span data-stu-id="d27c2-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="d27c2-127">No separador rápido **Acordos de fornecedores**, seleccione **Engadir liña**.</span><span class="sxs-lookup"><span data-stu-id="d27c2-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="d27c2-128">No campo **Código de conta**, seleccione unha das seguintes opcións:</span><span class="sxs-lookup"><span data-stu-id="d27c2-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="d27c2-129">**Táboa**: Os termos de retención do fornecedor aplícanse a un único fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="d27c2-130">**Grupo**: Os termos de retención do fornecedor aplícanse a todos os fornecedores dun grupo de fornecedores.</span><span class="sxs-lookup"><span data-stu-id="d27c2-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="d27c2-131">**Todos**: Os termos de retención do fornecedor aplícanse a todos os fornecedores.</span><span class="sxs-lookup"><span data-stu-id="d27c2-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="d27c2-132">No campo **Fornecedor/grupo de fornecedores**, seleccione o fornecedor ou grupo de fornecedores ao que se aplican os termos de retención do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="d27c2-133">Se seleccionou **Todos** no paso anterior, este campo non está dispoñible.</span><span class="sxs-lookup"><span data-stu-id="d27c2-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="d27c2-134">No campo **Termos de retención do fornecedor**, seleccione os termos de retención que creou no procedemento anterior.</span><span class="sxs-lookup"><span data-stu-id="d27c2-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="d27c2-135">Se o proxecto tamén ten configurados os termos de pagar ao recibir o pagamento (PWP) para o fornecedor, escriba a porcentaxe limiar para o proxecto no campo **Porcentaxe de limiar de PWP**.</span><span class="sxs-lookup"><span data-stu-id="d27c2-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="d27c2-136">Os termos de retención do fornecedor tamén se mostran nos pedidos de compra que cree para o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d27c2-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]