---
title: Configurar a facturación de proxectos entre empresas
description: Este tema mostra como configurar a facturación de proxectos entre dúas empresas da súa organización.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288377"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="b434b-103">Configurar a facturación de proxectos entre empresas</span><span class="sxs-lookup"><span data-stu-id="b434b-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b434b-104">Este tema mostra como configurar a facturación de proxectos entre dúas empresas da súa organización.</span><span class="sxs-lookup"><span data-stu-id="b434b-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="b434b-105">Esta tarefa utiliza o conxunto de datos USSI.</span><span class="sxs-lookup"><span data-stu-id="b434b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b434b-106">No panel de navegación, vaia a **Módulos > Contas pendentes de pago > Fornecedores > Todos os fornecedores**.</span><span class="sxs-lookup"><span data-stu-id="b434b-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="b434b-107">Na lista **Todos os fornecedores**, busque e seleccione o rexistro desexado.</span><span class="sxs-lookup"><span data-stu-id="b434b-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="b434b-108">No panel Acción, seleccione **Xeral**.</span><span class="sxs-lookup"><span data-stu-id="b434b-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="b434b-109">Seleccione **Entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="b434b-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="b434b-110">Poña **Activar** en **Si** para permitir o comercio entre empresas.</span><span class="sxs-lookup"><span data-stu-id="b434b-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="b434b-111">No campo **Empresa de cliente**, introduza ou seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b434b-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="b434b-112">No campo **A miña conta**, introduza ou seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b434b-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="b434b-113">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="b434b-113">Select **Save**.</span></span>
9. <span data-ttu-id="b434b-114">Peche as páxinas para volver á páxina de inicio.</span><span class="sxs-lookup"><span data-stu-id="b434b-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="b434b-115">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración> Parámetros de xestión de proxectos e contabilidade**.</span><span class="sxs-lookup"><span data-stu-id="b434b-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="b434b-116">Prema o separador **Entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="b434b-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="b434b-117">Move o control deslizante a **Si** para activar a programación de recursos e as follas de control de tempo entre empresas.</span><span class="sxs-lookup"><span data-stu-id="b434b-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="b434b-118">Na lista, marque a fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="b434b-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="b434b-119">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="b434b-119">Select **New**.</span></span>
15. <span data-ttu-id="b434b-120">No campo **Entidade legal que toma prestado**, introduza ou seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b434b-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="b434b-121">Seleccione a caixa de verificación **Acumular ingresos**.</span><span class="sxs-lookup"><span data-stu-id="b434b-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="b434b-122">No campo **Categoría de folla de control de tempo predefinida**, introduza ou seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b434b-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="b434b-123">No campo **Categoría de gasto predefinida**, introduza ou seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b434b-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="b434b-124">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="b434b-124">Select **Save**.</span></span>
20. <span data-ttu-id="b434b-125">Peche a páxina.</span><span class="sxs-lookup"><span data-stu-id="b434b-125">Close the page.</span></span>
21. <span data-ttu-id="b434b-126">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Publicación > Configuración de publicación de libro maior**.</span><span class="sxs-lookup"><span data-stu-id="b434b-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="b434b-127">No campo **Tipos de contas de libro maior**, seleccione unha opción.</span><span class="sxs-lookup"><span data-stu-id="b434b-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="b434b-128">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="b434b-128">Select **New**.</span></span>
24. <span data-ttu-id="b434b-129">No campo **Conta principal** da nova fila, especifique os valores desexados.</span><span class="sxs-lookup"><span data-stu-id="b434b-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="b434b-130">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="b434b-130">Select **Save**.</span></span>
26. <span data-ttu-id="b434b-131">Peche a páxina.</span><span class="sxs-lookup"><span data-stu-id="b434b-131">Close the page.</span></span>
27. <span data-ttu-id="b434b-132">No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de transferencia**.</span><span class="sxs-lookup"><span data-stu-id="b434b-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="b434b-133">Seleccione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="b434b-133">Select **New**.</span></span>
29. <span data-ttu-id="b434b-134">No campo **Data de entrada en vigor**, introduza unha data.</span><span class="sxs-lookup"><span data-stu-id="b434b-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="b434b-135">No campo **Entidade legal que toma prestado**, introduza ou seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b434b-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="b434b-136">No campo **Modelo de prezo de transferencia**, seleccione unha opción.</span><span class="sxs-lookup"><span data-stu-id="b434b-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="b434b-137">No campo **Prezos**, introduza un número.</span><span class="sxs-lookup"><span data-stu-id="b434b-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="b434b-138">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="b434b-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]