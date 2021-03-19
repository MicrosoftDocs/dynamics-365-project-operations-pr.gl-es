---
title: Crear e confirmar diarios de corrección
description: Este tema fornece información sobre como crear e confirmar un diario de corrección.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8ca35d1e66cbacaf65b7cd43493e3588f213788e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276931"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="ea044-103">Crear e confirmar diarios de corrección</span><span class="sxs-lookup"><span data-stu-id="ea044-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="ea044-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="ea044-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea044-105">De cando en vez pode introducirse unha entrada de tempo ou gasto incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="ea044-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="ea044-106">Por exemplo, un consultor pode seleccionar a data incorrecta ao crear unha entrada de tempo ou pode traspor os números ao ingresar un gasto.</span><span class="sxs-lookup"><span data-stu-id="ea044-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="ea044-107">Se un consultor non pode realizar as actualizacións das entradas enviadas, un administrador pode corrixir directamente a entrada para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="ea044-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="ea044-108">Para completar os procedementos neste tema, necesitará permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="ea044-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="ea044-109">Corrixir as entradas de tempo aprobadas</span><span class="sxs-lookup"><span data-stu-id="ea044-109">Correct approved time entries</span></span>     

<span data-ttu-id="ea044-110">Realice os seguintes pasos para corrixir as entradas de tempo individuais ou múltiples para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="ea044-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="ea044-111">Na zona **Vendas**, seleccione **Transaccións** e logo seleccione **Tempo aprobado**.</span><span class="sxs-lookup"><span data-stu-id="ea044-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="ea044-112">Na lista **Tempo aprobado**, localice e seleccione unha ou varias entradas de tempo aprobadas para corrixir.</span><span class="sxs-lookup"><span data-stu-id="ea044-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="ea044-113">Pode usar o filtro para localizar entradas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ea044-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="ea044-114">Por exemplo, pode filtrar un ID de proxecto e seleccionar todas as entradas de tempo aprobadas con ese ID de proxecto.</span><span class="sxs-lookup"><span data-stu-id="ea044-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="ea044-115">Seleccione **Corrixir entradas**.</span><span class="sxs-lookup"><span data-stu-id="ea044-115">Select **Correct entries**.</span></span> <span data-ttu-id="ea044-116">Créase automaticamente un novo diario de corrección, co tipo asignado **Corrección de tempo**.</span><span class="sxs-lookup"><span data-stu-id="ea044-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="ea044-117">As entradas que seleccionou engádense ao diario.</span><span class="sxs-lookup"><span data-stu-id="ea044-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="ea044-118">Na páxina **Novo diario**, introduza unha **Descrición** do diario de corrección e, a seguir, seleccione o separador **Correccións de entradas de tempo**.</span><span class="sxs-lookup"><span data-stu-id="ea044-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="ea044-119">Na sección **Novos valores para entradas de tempo**, actualice os campos coa información correcta segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="ea044-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="ea044-120">Por exemplo, pode cambiar o proxecto asignado ou o recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="ea044-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="ea044-121">Seleccione **Previsualización**.</span><span class="sxs-lookup"><span data-stu-id="ea044-121">Select **Preview**.</span></span> <span data-ttu-id="ea044-122">Na caixa de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ea044-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="ea044-123">No separador **Liñas de diario**, pode ver unha lista dos datos reais orixinais relacionados coas entradas de tempo seleccionadas que foron invertidas e as liñas correspondentes corrixidas que se crearon.</span><span class="sxs-lookup"><span data-stu-id="ea044-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="ea044-124">Se hai que facer correccións adicionais, repita os pasos 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="ea044-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="ea044-125">Todos os datos reais corrixidos terán os mesmos valores que seleccionou na sección **Novos valores das entradas de tempo**.</span><span class="sxs-lookup"><span data-stu-id="ea044-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="ea044-126">Se as correccións aparecen como se espera, seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="ea044-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="ea044-127">Na caixa de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ea044-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="ea044-128">Volva á zona **Vendas**, seleccione **Proxectos** e, a seguir, abra o proxecto para o que acaba de actualizar as entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="ea044-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="ea044-129">Na páxina **Proxectos**, no separador **Datos reais**, vexa os cambios que fixo.</span><span class="sxs-lookup"><span data-stu-id="ea044-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="ea044-130">Se o separador **Datos reais** non é visible, seleccione **Relacionado** > **Datos reais**.</span><span class="sxs-lookup"><span data-stu-id="ea044-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="ea044-131">Na lista **Vista asociada de datos reais**, pode ver que as entradas de tempo orixinais que foron invertidas aínda están na lista, do mesmo xeito que as entradas de tempo corrixidas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="ea044-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="ea044-132">Por exemplo, na seguinte gráfica, hai dúas partidas cunha cantidade de 8,00 que teñen débitos na columna Importe.</span><span class="sxs-lookup"><span data-stu-id="ea044-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="ea044-133">Ademais, hai dúas partidas cunha cantidade de -8,00 que amosan importes cobrados na columna Importe.</span><span class="sxs-lookup"><span data-stu-id="ea044-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="ea044-134">Estas correccións poñen a cantidade en cero.</span><span class="sxs-lookup"><span data-stu-id="ea044-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="ea044-135">Corrixir as entradas de gasto aprobadas</span><span class="sxs-lookup"><span data-stu-id="ea044-135">Correct approved expense entries</span></span>

<span data-ttu-id="ea044-136">Realice os seguintes pasos para corrixir unha ou varias entradas de gasto.</span><span class="sxs-lookup"><span data-stu-id="ea044-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="ea044-137">Na zona **Vendas**, no panel de navegación esquerdo, baixo **Transaccións**, seleccione **Gastos aprobados**.</span><span class="sxs-lookup"><span data-stu-id="ea044-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="ea044-138">Na lista **Gastos aprobados**, seleccione o proxecto que desexa corrixir e logo seleccione **Corrixir entradas**.</span><span class="sxs-lookup"><span data-stu-id="ea044-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="ea044-139">Crearase automaticamente un novo diario de corrección, co tipo asignado de **Corrección de gasto**.</span><span class="sxs-lookup"><span data-stu-id="ea044-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="ea044-140">Na páxina **Novo diario**, introduza unha **Descrición** para a corrección, e no separador **Corrección de gasto**, na sección **Novos valores para gastos**, seleccione os campos de datos que desexa corrixir para as liñas de gasto seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="ea044-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="ea044-141">Por exemplo, pode atribuír o gasto a outro **Proxecto** ou corrixir **Categoría de gasto**, **Data de gasto** ou **Recurso reservable**.</span><span class="sxs-lookup"><span data-stu-id="ea044-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="ea044-142">Seleccione **Previsualización**.</span><span class="sxs-lookup"><span data-stu-id="ea044-142">Select **Preview**.</span></span> <span data-ttu-id="ea044-143">Na caixa de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ea044-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="ea044-144">Verifique as correccións no separador **Liñas de diario**. Pode ver unha lista dos datos reais orixinais relacionados coas entradas de gasto seleccionadas que foron invertidas e as liñas correspondentes corrixidas que se crearon.</span><span class="sxs-lookup"><span data-stu-id="ea044-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="ea044-145">Se os valores corrixidos son os esperados, seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="ea044-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="ea044-146">Na caixa de diálogo, seleccione **Aceptar.**</span><span class="sxs-lookup"><span data-stu-id="ea044-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="ea044-147">Se os valores non se amosan como se espera, seleccione **Cancelar** para volver á lista **Gastos aprobados**.</span><span class="sxs-lookup"><span data-stu-id="ea044-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="ea044-148">Repita os pasos do 2 ao 5.</span><span class="sxs-lookup"><span data-stu-id="ea044-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="ea044-149">Os datos reais corrixidos terán os mesmos valores que seleccionou na sección **Novos valores dos gastos**.</span><span class="sxs-lookup"><span data-stu-id="ea044-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="ea044-150">Despois de confirmar o diario de correccións, desprácese ata o proxecto ou proxectos que actualizou para ver os seus cambios.</span><span class="sxs-lookup"><span data-stu-id="ea044-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="ea044-151">Na páxina do proxecto, no separador **Datos reais**, revise a **Visualización asociada dos datos reais**.</span><span class="sxs-lookup"><span data-stu-id="ea044-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="ea044-152">Aparecerán as entradas orixinais e as entradas corrixidas.</span><span class="sxs-lookup"><span data-stu-id="ea044-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="ea044-153">O seguinte gráfico mostra os importes orixinais das entradas de gastos e os correspondentes importes corrixidos das entradas de gastos.</span><span class="sxs-lookup"><span data-stu-id="ea044-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]