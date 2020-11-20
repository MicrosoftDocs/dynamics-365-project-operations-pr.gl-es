---
title: Emparellar un recibo cun gasto mediante OCR
description: Este tema ofrece información sobre o procesamento de recoñecemento óptico de caracteres (OCR) para recibos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124321"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="6f78f-103">Emparellar un recibo cun gasto mediante OCR</span><span class="sxs-lookup"><span data-stu-id="6f78f-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="6f78f-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="6f78f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6f78f-105">A entrada de gastos mellorouse mediante a introdución do procesamento de recoñecemento óptico de caracteres (OCR) para recibos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="6f78f-106">Esta funcionalidade está deseñada para mellorar a experiencia do usuario ao crear informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="6f78f-107">Funcionalidades clave</span><span class="sxs-lookup"><span data-stu-id="6f78f-107">Key features</span></span>

- <span data-ttu-id="6f78f-108">O sistema extrae o nome do comerciante, a data e o importe total dos recibos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="6f78f-109">O sistema tentará emparellar os recibos non anexados coas transaccións de gastos non anexadas.</span><span class="sxs-lookup"><span data-stu-id="6f78f-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="6f78f-110">Pode crear transaccións de gastos introducidas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="6f78f-111">Anexar recibos a un informe de gastos</span><span class="sxs-lookup"><span data-stu-id="6f78f-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="6f78f-112">Para anexar automaticamente recibos que inclúan transaccións con tarxeta de crédito cando se crea un informe de gastos, complete os seguintes pasos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="6f78f-113">Abra a área de traballo **Xestión de gastos**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="6f78f-114">No separador **Recibos**, comprobe que existen recibos non anexados.</span><span class="sxs-lookup"><span data-stu-id="6f78f-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="6f78f-115">Tamén pode cargar recibos no separador **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="6f78f-116">No separador **Gastos**, comprobe que existen gastos non anexados.</span><span class="sxs-lookup"><span data-stu-id="6f78f-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="6f78f-117">Normalmente, o administrador de gastos importa estes gastos do provedor da tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="6f78f-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="6f78f-118">Seleccione **Novo informe de gastos**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-118">Select **New expense report**.</span></span> <span data-ttu-id="6f78f-119">Teña en conta que agora tamén pode incluír gastos e recibos tamén cando crea un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="6f78f-120">Se engade tanto gastos como recibos, activarase a correspondencia automática dos recibos cos gastos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="6f78f-121">Crear ou emparellar recibos cun informe de gastos</span><span class="sxs-lookup"><span data-stu-id="6f78f-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="6f78f-122">Para crear un gasto ou emparellar un gasto desde un recibo, complete os seguintes pasos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="6f78f-123">Nun informe de gastos, no separador **Recibos**, anexe un recibo seleccionando **Engadir recibos**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="6f78f-124">Debaixo da imaxe cargada do recibo, observe as opcións **Crear** e **Emparellar**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="6f78f-125">Seleccione **Crear** para crear unha transacción de gastos introducida manualmente e encher os valores que se extraen do recibo.</span><span class="sxs-lookup"><span data-stu-id="6f78f-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="6f78f-126">Se selecciona **Emparellar**, o sistema tenta emparellar un gasto existente co recibo.</span><span class="sxs-lookup"><span data-stu-id="6f78f-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="6f78f-127">Instalación</span><span class="sxs-lookup"><span data-stu-id="6f78f-127">Installation</span></span>

<span data-ttu-id="6f78f-128">Para utilizar estas capacidades avanzadas de gastos, instale o complemento Servizo de xestión de gastos para Microsoft Dynamics 365 Finance e active as funcionalidades na súa instancia.</span><span class="sxs-lookup"><span data-stu-id="6f78f-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="6f78f-129">Pode acceder ao complemento desde o seu proxecto en Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6f78f-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="6f78f-130">Inicie sesión en LCS e abra o ambiente desexado.</span><span class="sxs-lookup"><span data-stu-id="6f78f-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="6f78f-131">Vaia a **Detalles completos**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="6f78f-132">Seleccione **Manter** ou desprácese ata o separador rápido **Complementos de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="6f78f-133">Seleccione **Instala un novo complemento**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="6f78f-134">Seleccione **Servizo de xestión de gastos**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="6f78f-135">Siga a guía de instalación e acepte os termos e condicións.</span><span class="sxs-lookup"><span data-stu-id="6f78f-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="6f78f-136">Seleccionar **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-136">Select **Install**.</span></span>

<span data-ttu-id="6f78f-137">Na área de traballo **Xestión de funcionalidades**, active as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="6f78f-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="6f78f-138">Os informes de gastos reinventáronse</span><span class="sxs-lookup"><span data-stu-id="6f78f-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="6f78f-139">Emparellar automaticamente e crear gastos a partir do recibo</span><span class="sxs-lookup"><span data-stu-id="6f78f-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="6f78f-140">Ao activar estas funcionalidades, prodúcense as seguintes accións:</span><span class="sxs-lookup"><span data-stu-id="6f78f-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="6f78f-141">A área de traballo **Xestión de gastos** existente substitúese pola nova área de traballo.</span><span class="sxs-lookup"><span data-stu-id="6f78f-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="6f78f-142">Engádese un novo elemento de menú para a visibilidade do campo de gastos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="6f78f-143">Aínda pode abrir a páxina **Informes de gastos** anterior indo a **Xestión de gastos > Os meus gastos > Informes de gastos**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="6f78f-144">Os fluxos de traballo e as aprobacións aínda o levarán á páxina de informes de gastos existente.</span><span class="sxs-lookup"><span data-stu-id="6f78f-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="6f78f-145">Os recibos procesaranse mediante Microsoft Azure Cognitive Services e os metadatos extraeranse e engadiranse.</span><span class="sxs-lookup"><span data-stu-id="6f78f-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="6f78f-146">Engádese unha opción que lle permite crear un informe de gastos que inclúe recibos non anexados emparellados.</span><span class="sxs-lookup"><span data-stu-id="6f78f-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="6f78f-147">Unha opción que se engade aos informes de gastos permítelle crear unha liña de gasto a partir dun recibo ou tentar emparellar un recibo existente cunha liña de gasto existente.</span><span class="sxs-lookup"><span data-stu-id="6f78f-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6f78f-148">Preguntas máis frecuentes</span><span class="sxs-lookup"><span data-stu-id="6f78f-148">Frequently asked questions</span></span>

<span data-ttu-id="6f78f-149">**Usa Microsoft os meus datos para os seus modelos?**</span><span class="sxs-lookup"><span data-stu-id="6f78f-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="6f78f-150">Non, Microsoft creou un modelo xeral de aprendizaxe automático para o seu servizo de procesamento de recibos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="6f78f-151">Este modelo non está baseado nos recibos que vostede cargue.</span><span class="sxs-lookup"><span data-stu-id="6f78f-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="6f78f-152">**Onde está dispoñible e se procesa esta funcionalidade?**</span><span class="sxs-lookup"><span data-stu-id="6f78f-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="6f78f-153">Actualmente, está dispoñible nos Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="6f78f-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="6f78f-154">**Onde van os meus recibos?**</span><span class="sxs-lookup"><span data-stu-id="6f78f-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="6f78f-155">Finanzas contactará con Cognitive Services para extraer os datos do campo.</span><span class="sxs-lookup"><span data-stu-id="6f78f-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="6f78f-156">Cognitive Services conservará unha copia do seu recibo ata 24 horas mentres se produce o procesamento.</span><span class="sxs-lookup"><span data-stu-id="6f78f-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="6f78f-157">Unha vez finalizado o procesamento, Cognitive Services eliminará o recibo.</span><span class="sxs-lookup"><span data-stu-id="6f78f-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="6f78f-158">Os recibos aínda se gardan en Finanzas.</span><span class="sxs-lookup"><span data-stu-id="6f78f-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="6f78f-159">Para obter máis información, consulte [Activar a comprensión de recibos coa nova capacidade de recoñecemento de formularios](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="6f78f-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
