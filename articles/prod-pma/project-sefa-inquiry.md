---
title: Lista de gastos de investigación de subvencións federais
description: Este tema ofrece información sobre a programación de gastos de investigación de subvencións federais.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288962"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d9093-103">Lista de gastos de investigación de subvencións federais</span><span class="sxs-lookup"><span data-stu-id="d9093-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9093-104">Segundo a Circular A-133 da Oficina de Xestión e Orzamentos, as axencias que reciben fondos federais están suxeitas a requisitos de auditoría, que tamén se coñecen como auditorías únicas.</span><span class="sxs-lookup"><span data-stu-id="d9093-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="d9093-105">O proceso de auditoría úsase para informar de forma recorrente sobre os ingresos e gastos das subvencións federais.</span><span class="sxs-lookup"><span data-stu-id="d9093-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="d9093-106">Unha parte do informe único de auditoría inclúe a programación de gastos de subvencións federais (SEFA).</span><span class="sxs-lookup"><span data-stu-id="d9093-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="d9093-107">A programación de gastos de investigación de subvencións federais inclúe o título e número do Catálogo de asistencia doméstica federal (CFDA), o número da subvención, o ano da subvención, o nome da axencia federal que proporciona os fondos e o nome da entidade intermediaria.</span><span class="sxs-lookup"><span data-stu-id="d9093-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="d9093-108">A investigación é por un período específico.</span><span class="sxs-lookup"><span data-stu-id="d9093-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="d9093-109">Normalmente, ese período é o mesmo que o período dos estados financeiros, que é un ano fiscal.</span><span class="sxs-lookup"><span data-stu-id="d9093-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="d9093-110">A consulta inclúe subvencións que teñen datas de proxección no intervalo de datas seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d9093-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="d9093-111">A columna **Axencia outorgante** na columna da investigación mostra o cliente da subvención ou, para unha subvención a través de intermediario, a axencia outorgante.</span><span class="sxs-lookup"><span data-stu-id="d9093-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="d9093-112">Para unha subvención a través de intermediario, a columna **Axencia intermediaria** mostra o cliente da subvención.</span><span class="sxs-lookup"><span data-stu-id="d9093-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="d9093-113">Se subvención non é través de intermediario, a columna **Axencia intermediaria** está en branco.</span><span class="sxs-lookup"><span data-stu-id="d9093-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="d9093-114">Configure os clústeres CFDA</span><span class="sxs-lookup"><span data-stu-id="d9093-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="d9093-115">Debe configurar os clústeres de CFDA que se poidan asociar aos números CFDA na programación de gastos de investigación de subvencións federais.</span><span class="sxs-lookup"><span data-stu-id="d9093-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d9093-116">Vaia a **Xestión e contabilidade de proxectos \> Configurar \> Subvencións \> Catálogo de clústeres de asistencia doméstica federal**.</span><span class="sxs-lookup"><span data-stu-id="d9093-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="d9093-117">Seleccione **Novo** para crear un clúster de CFDA.</span><span class="sxs-lookup"><span data-stu-id="d9093-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="d9093-118">Escriba o nome do clúster.</span><span class="sxs-lookup"><span data-stu-id="d9093-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="d9093-119">Seleccione **Gardar** para gardar as modificacións.</span><span class="sxs-lookup"><span data-stu-id="d9093-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="d9093-120">Configurar os números de CFDA</span><span class="sxs-lookup"><span data-stu-id="d9093-120">Set up CFDA numbers</span></span>

<span data-ttu-id="d9093-121">Debe configurar os números de CFDA que se poidan engadir ás subvencións e incluír na programación de gastos de investigación de subvencións federais.</span><span class="sxs-lookup"><span data-stu-id="d9093-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d9093-122">Vaia a **Xestión e contabilidade de proxectos \> Configurar \> Subvencións \> Catálogo de números de asistencia doméstica federal**.</span><span class="sxs-lookup"><span data-stu-id="d9093-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="d9093-123">Seleccione **Novo** para crear un número de CFDA.</span><span class="sxs-lookup"><span data-stu-id="d9093-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="d9093-124">Na columna **Número**, introduza o número de CFDA.</span><span class="sxs-lookup"><span data-stu-id="d9093-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="d9093-125">Prema a tecla **Separador**.</span><span class="sxs-lookup"><span data-stu-id="d9093-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="d9093-126">Na columna **Descrición**, introduza o título de CFDA.</span><span class="sxs-lookup"><span data-stu-id="d9093-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="d9093-127">Prema a tecla **Separador**.</span><span class="sxs-lookup"><span data-stu-id="d9093-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="d9093-128">Opcional: No campo **Clúster de programas**, engada o clúster de CFDA axeitado.</span><span class="sxs-lookup"><span data-stu-id="d9093-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="d9093-129">Seleccione **Gardar** para gardar as modificacións.</span><span class="sxs-lookup"><span data-stu-id="d9093-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d9093-130">Configurar subvencións para a programación de gastos de investigación de subvencións federais</span><span class="sxs-lookup"><span data-stu-id="d9093-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d9093-131">Vaia a **Xestión e contabilidade de proxectos \> Subvencións \> Subvencións** e seleccione unha subvención existente.</span><span class="sxs-lookup"><span data-stu-id="d9093-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="d9093-132">No separador rápido **Configurar**, no campo **Catálogo de asistencia doméstica federal**, atribúa o número CFDA.</span><span class="sxs-lookup"><span data-stu-id="d9093-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="d9093-133">O número CFDA da subvención determina o clúster de CFDA para a presentación de informes.</span><span class="sxs-lookup"><span data-stu-id="d9093-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="d9093-134">No separador rápido **Información de contacto**, introduza a información do outorgante seguindo estes pasos:</span><span class="sxs-lookup"><span data-stu-id="d9093-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="d9093-135">No campo **Cliente da subvención**, introduza o cliente responsable da subvención.</span><span class="sxs-lookup"><span data-stu-id="d9093-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="d9093-136">Para unha subvención existente, é posible que esta información xa estea introducida.</span><span class="sxs-lookup"><span data-stu-id="d9093-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="d9093-137">Indique se o cliente da subvención é o financiador.</span><span class="sxs-lookup"><span data-stu-id="d9093-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="d9093-138">Se o cliente da subvención é o financiador, deixe a caixa de verificación **Intermediario** sen marcar.</span><span class="sxs-lookup"><span data-stu-id="d9093-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="d9093-139">Se outro cliente é o financiador e o cliente da subvención é responsable do gasto e rastrexo do diñeiro, seleccione a caixa de verificación **Intermediario**.</span><span class="sxs-lookup"><span data-stu-id="d9093-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="d9093-140">Se seleccionou a caixa de verificación **Intermediario** no paso anterior, no campo **Axencia outorgante**, introduza o cliente que proporcionou a subvención.</span><span class="sxs-lookup"><span data-stu-id="d9093-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="d9093-141">A axencia outorgante e o cliente outorgante non poden ser o mesmo cliente.</span><span class="sxs-lookup"><span data-stu-id="d9093-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="d9093-142">Aquí ten un exemplo de subvención a través de intermediario:</span><span class="sxs-lookup"><span data-stu-id="d9093-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="d9093-143">O goberno federal financiou un proxecto de infraestrutura para un estado.</span><span class="sxs-lookup"><span data-stu-id="d9093-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="d9093-144">O goberno federal deu o diñeiro ao estado para gastalo.</span><span class="sxs-lookup"><span data-stu-id="d9093-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="d9093-145">Neste caso, o goberno federal é a axencia outorgante e o estado é o cliente da subvención.</span><span class="sxs-lookup"><span data-stu-id="d9093-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="d9093-146">Cando active a funcionalidade por primeira vez, introduciranse os números CFDA iniciais empregando os números existentes nas subvencións.</span><span class="sxs-lookup"><span data-stu-id="d9093-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="d9093-147">Excluír as subvencións dos informes SEFA en función do tipo de subvención</span><span class="sxs-lookup"><span data-stu-id="d9093-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="d9093-148">Vaia a **Xestión e contabilidade de proxectos \> Configurar \> Subvencións \> Tipos de subvencións**.</span><span class="sxs-lookup"><span data-stu-id="d9093-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="d9093-149">No separador rápido **Información predefinida**, seleccione a caixa de verificación **Excluír da programación de gastos de subvencións federais**.</span><span class="sxs-lookup"><span data-stu-id="d9093-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="d9093-150">Seleccione **Gardar** para gardar as modificacións.</span><span class="sxs-lookup"><span data-stu-id="d9093-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d9093-151">Execute a programación gastos de investigación de subvencións federais</span><span class="sxs-lookup"><span data-stu-id="d9093-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d9093-152">Vaia a **Xestión e contabilidade de proxectos \> Investigacións e informes \> Investigación de subvención \> Programación de gastos de subvencións federais**.</span><span class="sxs-lookup"><span data-stu-id="d9093-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="d9093-153">Na sección **Parámetros**, siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="d9093-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="d9093-154">No campo **Intervalo de datas**, seleccione o código para o intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="d9093-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="d9093-155">Alternativamente, nos campos **A partir da data** e **Ata a data**, defina o intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="d9093-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="d9093-156">Opcional: Para incluír só as transaccións facturadas como ingresos na investigación, configure a opción **Incluír só os ingresos facturados** en **Si**.</span><span class="sxs-lookup"><span data-stu-id="d9093-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="d9093-157">Columnas</span><span class="sxs-lookup"><span data-stu-id="d9093-157">Columns</span></span>

<span data-ttu-id="d9093-158">A programación de gastos de investigación de subvencións federais inclúe as seguintes columnas:</span><span class="sxs-lookup"><span data-stu-id="d9093-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="d9093-159">Nome do clúster do catálogo de asistencia doméstica federal</span><span class="sxs-lookup"><span data-stu-id="d9093-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="d9093-160">Axencia outorgante</span><span class="sxs-lookup"><span data-stu-id="d9093-160">Grantor agency</span></span>
- <span data-ttu-id="d9093-161">Axencia intermediaria</span><span class="sxs-lookup"><span data-stu-id="d9093-161">Pass-through agency</span></span>
- <span data-ttu-id="d9093-162">Nome da subvención</span><span class="sxs-lookup"><span data-stu-id="d9093-162">Grant name</span></span>
- <span data-ttu-id="d9093-163">ID da subvención</span><span class="sxs-lookup"><span data-stu-id="d9093-163">Grant ID</span></span>
- <span data-ttu-id="d9093-164">ID da solicitude de subvención</span><span class="sxs-lookup"><span data-stu-id="d9093-164">Grant application ID</span></span>
- <span data-ttu-id="d9093-165">Catálogo de asistencia doméstica federal</span><span class="sxs-lookup"><span data-stu-id="d9093-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="d9093-166">Recibos</span><span class="sxs-lookup"><span data-stu-id="d9093-166">Receipts</span></span>
- <span data-ttu-id="d9093-167">Gastos</span><span class="sxs-lookup"><span data-stu-id="d9093-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]