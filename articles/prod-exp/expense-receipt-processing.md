---
title: Procesamento de recibos de gastos
description: Este tema ofrece información sobre o procesamento de recoñecemento óptico de caracteres (OCR) para recibos. Esta funcionalidade está deseñada para mellorar a experiencia do usuario ao crear informes de gastos en Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993504"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="10d43-104">Procesamento de recibos de gastos</span><span class="sxs-lookup"><span data-stu-id="10d43-104">Expense receipt processing</span></span>

<span data-ttu-id="10d43-105">A entrada de gastos mellorouse mediante a introdución do procesamento de recoñecemento óptico de caracteres (OCR) para recibos.</span><span class="sxs-lookup"><span data-stu-id="10d43-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="10d43-106">Esta funcionalidade está deseñada para mellorar a experiencia do usuario ao crear informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="10d43-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="10d43-107">Funcionalidades clave</span><span class="sxs-lookup"><span data-stu-id="10d43-107">Key features</span></span>

- <span data-ttu-id="10d43-108">O nome do comerciante, a data e o importe total extráense dos recibos.</span><span class="sxs-lookup"><span data-stu-id="10d43-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="10d43-109">A funcionalidade tenta emparellar os recibos non anexados coas transaccións de gastos non anexadas.</span><span class="sxs-lookup"><span data-stu-id="10d43-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="10d43-110">Os usuarios poden crear transaccións de gastos introducidas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="10d43-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="10d43-111">Exemplos de uso</span><span class="sxs-lookup"><span data-stu-id="10d43-111">Usage examples</span></span>

<span data-ttu-id="10d43-112">Para anexar automaticamente recibos que inclúan transaccións con tarxeta de crédito cando se crea un informe de gastos, faga o seguinte:</span><span class="sxs-lookup"><span data-stu-id="10d43-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="10d43-113">Abra a área de traballo **Xestión de gastos**.</span><span class="sxs-lookup"><span data-stu-id="10d43-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="10d43-114">No separador **Recibos**, comprobe que existen recibos non anexados.</span><span class="sxs-lookup"><span data-stu-id="10d43-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="10d43-115">Tamén pode cargar recibos no separador **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="10d43-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="10d43-116">No separador **Gastos**, comprobe que existen gastos non anexados.</span><span class="sxs-lookup"><span data-stu-id="10d43-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="10d43-117">Normalmente, o administrador de gastos importa estes gastos do provedor da tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="10d43-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="10d43-118">Seleccione **Novo informe de gastos**.</span><span class="sxs-lookup"><span data-stu-id="10d43-118">Select **New expense report**.</span></span> <span data-ttu-id="10d43-119">Teña en conta que agora tamén pode incluír gastos e recibos tamén cando crea un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="10d43-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="10d43-120">Se engade tanto gastos como recibos, activarase a correspondencia automática dos recibos cos gastos.</span><span class="sxs-lookup"><span data-stu-id="10d43-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="10d43-121">Para crear un gasto ou emparellar un gasto desde un recibo, faga o seguinte:</span><span class="sxs-lookup"><span data-stu-id="10d43-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="10d43-122">Nun informe de gastos, no separador **Recibos**, anexe un recibo seleccionando **Engadir recibos**.</span><span class="sxs-lookup"><span data-stu-id="10d43-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="10d43-123">Debaixo da imaxe cargada do recibo, observe as opcións **Crear** e **Emparellar**.</span><span class="sxs-lookup"><span data-stu-id="10d43-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="10d43-124">Seleccione **Crear** para crear unha transacción de gastos introducida manualmente e encher os valores que se extraen do recibo.</span><span class="sxs-lookup"><span data-stu-id="10d43-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="10d43-125">Se selecciona **Emparellar**, o sistema tenta emparellar un gasto existente co recibo.</span><span class="sxs-lookup"><span data-stu-id="10d43-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="10d43-126">Instalación</span><span class="sxs-lookup"><span data-stu-id="10d43-126">Installation</span></span>

<span data-ttu-id="10d43-127">Esta funcionalidade funciona en combinación coa funcionalidade **Reinvención dos informes de gastos** para axudar a simplificar a experiencia dos gastos.</span><span class="sxs-lookup"><span data-stu-id="10d43-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="10d43-128">Esta función só está dispoñible para ambientes de nivel 2+, que son Illamento de procesos e Produción.</span><span class="sxs-lookup"><span data-stu-id="10d43-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="10d43-129">Para utilizar estas capacidades avanzadas de gastos, instale o complemento Servizo de xestión de gastos para Microsoft Dynamics 365 Finance e active as funcionalidades na súa instancia.</span><span class="sxs-lookup"><span data-stu-id="10d43-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="10d43-130">Pode acceder ao complemento desde o seu proxecto en Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="10d43-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="10d43-131">Inicie sesión en LCS e abra o ambiente desexado.</span><span class="sxs-lookup"><span data-stu-id="10d43-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="10d43-132">Vaia a **Detalles completos**.</span><span class="sxs-lookup"><span data-stu-id="10d43-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="10d43-133">Seleccione **Manter** ou desprácese ata o separador rápido **Complementos de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="10d43-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="10d43-134">Seleccione **Instala un novo complemento**.</span><span class="sxs-lookup"><span data-stu-id="10d43-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="10d43-135">Seleccione **Servizo de xestión de gastos**.</span><span class="sxs-lookup"><span data-stu-id="10d43-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="10d43-136">Siga a guía de instalación e acepte os termos e condicións.</span><span class="sxs-lookup"><span data-stu-id="10d43-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="10d43-137">Seleccionar **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="10d43-137">Select **Install**.</span></span>

<span data-ttu-id="10d43-138">Na área de traballo **Xestión de funcionalidades**, active as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="10d43-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="10d43-139">Os informes de gastos reinventáronse</span><span class="sxs-lookup"><span data-stu-id="10d43-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="10d43-140">Emparellar automaticamente e crear gastos a partir do recibo</span><span class="sxs-lookup"><span data-stu-id="10d43-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="10d43-141">Ao activar estas funcionalidades, prodúcense as seguintes accións:</span><span class="sxs-lookup"><span data-stu-id="10d43-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="10d43-142">A área de traballo **Xestión de gastos** existente substitúese pola nova área de traballo.</span><span class="sxs-lookup"><span data-stu-id="10d43-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="10d43-143">Engádese un novo elemento de menú para a visibilidade do campo de gastos.</span><span class="sxs-lookup"><span data-stu-id="10d43-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="10d43-144">Aínda pode abrir a páxina **Informes de gastos** anterior indo a **Xestión de gastos > Os meus gastos > Informes de gastos**.</span><span class="sxs-lookup"><span data-stu-id="10d43-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="10d43-145">Os fluxos de traballo e as aprobacións aínda o levarán á páxina de informes de gastos existente.</span><span class="sxs-lookup"><span data-stu-id="10d43-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="10d43-146">Os recibos procesaranse mediante Microsoft Azure Cognitive Services e os metadatos extraeranse e engadiranse.</span><span class="sxs-lookup"><span data-stu-id="10d43-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="10d43-147">Engádese unha opción que lle permite crear un informe de gastos que inclúe recibos non anexados emparellados.</span><span class="sxs-lookup"><span data-stu-id="10d43-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="10d43-148">Unha opción que se engade aos informes de gastos permítelle crear unha liña de gasto a partir dun recibo ou tentar emparellar un recibo existente cunha liña de gasto existente.</span><span class="sxs-lookup"><span data-stu-id="10d43-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="10d43-149">Para obter máis información sobre a funcionalidade de reinvención dos informes de gastos, consulte [Reinvención dos informes de gastos](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="10d43-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="10d43-150">Preguntas máis frecuentes</span><span class="sxs-lookup"><span data-stu-id="10d43-150">Frequently asked questions</span></span>

<span data-ttu-id="10d43-151">**Usa Microsoft os meus datos para os seus modelos?**</span><span class="sxs-lookup"><span data-stu-id="10d43-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="10d43-152">Non, Microsoft creou un modelo xeral de aprendizaxe automático para o seu servizo de procesamento de recibos.</span><span class="sxs-lookup"><span data-stu-id="10d43-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="10d43-153">Este modelo non está baseado nos recibos que vostede cargue.</span><span class="sxs-lookup"><span data-stu-id="10d43-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="10d43-154">**Onde está dispoñible e se procesa esta funcionalidade?**</span><span class="sxs-lookup"><span data-stu-id="10d43-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="10d43-155">Actualmente, está dispoñible nos Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="10d43-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="10d43-156">**Onde van os meus recibos?**</span><span class="sxs-lookup"><span data-stu-id="10d43-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="10d43-157">Finanzas contactará con Cognitive Services para extraer os datos do campo.</span><span class="sxs-lookup"><span data-stu-id="10d43-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="10d43-158">Cognitive Services conservará unha copia do seu recibo ata 24 horas mentres se produce o procesamento.</span><span class="sxs-lookup"><span data-stu-id="10d43-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="10d43-159">Unha vez finalizado o procesamento, Cognitive Services eliminará o recibo.</span><span class="sxs-lookup"><span data-stu-id="10d43-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="10d43-160">Os recibos aínda se gardan en Finanzas.</span><span class="sxs-lookup"><span data-stu-id="10d43-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="10d43-161">Para obter máis información, consulte [Activar a comprensión de recibos coa nova capacidade de recoñecemento de formularios](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="10d43-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]