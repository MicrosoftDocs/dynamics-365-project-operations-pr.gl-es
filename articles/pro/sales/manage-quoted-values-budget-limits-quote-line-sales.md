---
title: Visión xeral de liñas de oferta baseada en proxecto - lite
description: Este tema ofrece información sobre como liñas de oferta baseada en proxecto para o traballo do proxecto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272971"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="658e7-104">Visión xeral de liñas de oferta baseada en proxecto - lite</span><span class="sxs-lookup"><span data-stu-id="658e7-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="658e7-105">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="658e7-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="658e7-106">As liñas de oferta baseada en proxecto están deseñadas para axudar a estimar o traballo do proxecto nun compromiso.</span><span class="sxs-lookup"><span data-stu-id="658e7-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="658e7-107">A estrutura dunha liña de oferta baseada en proxecto amplíase para as estimacións do proxecto cos seguintes conceptos:</span><span class="sxs-lookup"><span data-stu-id="658e7-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="658e7-108">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="658e7-108">Billing Method</span></span>
- <span data-ttu-id="658e7-109">Asignación de tarefas e proxectos</span><span class="sxs-lookup"><span data-stu-id="658e7-109">Project and Task Mapping</span></span>
- <span data-ttu-id="658e7-110">Clases de transaccións incluídas</span><span class="sxs-lookup"><span data-stu-id="658e7-110">Included Transaction classes</span></span>
- <span data-ttu-id="658e7-111">Límite non superable</span><span class="sxs-lookup"><span data-stu-id="658e7-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="658e7-112">Configuración de imputabilidade.</span><span class="sxs-lookup"><span data-stu-id="658e7-112">Chargeability setup</span></span>
- <span data-ttu-id="658e7-113">Estimación mediante detalles da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="658e7-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="658e7-114">Clientes da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="658e7-114">Quote line Customers</span></span>

<span data-ttu-id="658e7-115">A seguinte táboa ofrece información sobre os campos do separador **Xeral** da liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="658e7-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="658e7-116">Estes campos axudan a establecer as bases para unha estimación detallada e completa do traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="658e7-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="658e7-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="658e7-117">**Field**</span></span> | <span data-ttu-id="658e7-118">**Descrición**</span><span class="sxs-lookup"><span data-stu-id="658e7-118">**Description**</span></span> | <span data-ttu-id="658e7-119">**Impacto descendente**</span><span class="sxs-lookup"><span data-stu-id="658e7-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="658e7-120">Nome</span><span class="sxs-lookup"><span data-stu-id="658e7-120">Name</span></span> | <span data-ttu-id="658e7-121">O nome da liña de oferta que debería axudarlle a identificar o compoñente discreto da oferta que se estima.</span><span class="sxs-lookup"><span data-stu-id="658e7-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="658e7-122">Copiado á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-123">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="658e7-123">Billing Method</span></span> | <span data-ttu-id="658e7-124">Nunha oferta creada a partir dunha oportunidade, este valor copiase desde campo correspondente na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="658e7-125">Este campo inclúe os dous principais modelos de contratación admitidos por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="658e7-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="658e7-126">- Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="658e7-126">- Fixed price</span></span></br><span data-ttu-id="658e7-127">- Tempo e material.</span><span class="sxs-lookup"><span data-stu-id="658e7-127">- Time and material.</span></span>| <span data-ttu-id="658e7-128">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-129">Project</span><span class="sxs-lookup"><span data-stu-id="658e7-129">Project</span></span> | <span data-ttu-id="658e7-130">Use este campo opcional para identificar o proxecto que se usará para entregar o traballo neste compromiso.</span><span class="sxs-lookup"><span data-stu-id="658e7-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="658e7-131">Cando un proxecto está asignado a unha liña de oferta, axuda a configurar tarefas imputables e tamén a traer unha estimación baseada no proxecto á liña de oferta como detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="658e7-132">Cando un proxecto non está asignado a unha liña de oferta baseada en proxecto, a estimación debe crearse manualmente creando cada detalle da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="658e7-133">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="658e7-134">Tarefas incluídas</span><span class="sxs-lookup"><span data-stu-id="658e7-134">Included Tasks</span></span> | <span data-ttu-id="658e7-135">Indica se esta liña de oferta se usa para todas ou algunhas das tarefas do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="658e7-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="658e7-136">Este campo ten os seguintes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="658e7-136">This field has the following possible values:</span></span></br><span data-ttu-id="658e7-137">- Todas as tarefas do proxecto</span><span class="sxs-lookup"><span data-stu-id="658e7-137">- All project tasks</span></span></br><span data-ttu-id="658e7-138">- Só tarefas do proxecto seleccionadas</span><span class="sxs-lookup"><span data-stu-id="658e7-138">- Selected project tasks only</span></span></br><span data-ttu-id="658e7-139">Un valor en branco neste campo equivale á opción **Todas as tarefas do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="658e7-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="658e7-140">Cando se selecciona **Só as tarefas do proxecto seleccionadas**, na páxina do proxecto, o separador **Configuración da facturación das tarefas** permítelle seleccionar tarefas específicas para asocialas a esta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="658e7-141">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-142">Incluír tempo</span><span class="sxs-lookup"><span data-stu-id="658e7-142">Include Time</span></span> | <span data-ttu-id="658e7-143">O indicador **Si**/**Non** indica se as transaccións de tempo ou os custos laborais do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="658e7-144">O valor **Non** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="658e7-145">O valor **Si** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="658e7-146">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-147">Incluír gasto</span><span class="sxs-lookup"><span data-stu-id="658e7-147">Include Expense</span></span> | <span data-ttu-id="658e7-148">O indicador **Si**/**Non** indica se os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="658e7-149">O valor **Non** indica que os custos de gastos do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="658e7-150">O valor **Si** indica que os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="658e7-151">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-152">Incluír taxa</span><span class="sxs-lookup"><span data-stu-id="658e7-152">Include Fee</span></span> | <span data-ttu-id="658e7-153">O indicador **Si**/**Non** indica se as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="658e7-154">O valor **Non** indica que as taxas do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="658e7-155">O valor **Si** indica que as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="658e7-156">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-157">Cantidade ofertada</span><span class="sxs-lookup"><span data-stu-id="658e7-157">Quoted Amount</span></span> | <span data-ttu-id="658e7-158">Esta é a cantidade que se ofertará ao cliente por todo o traballo previsto nesta liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="658e7-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="658e7-159">Nunha oferta creada a partir dunha oportunidade, este valor copiase desde o campo **Orzamento do cliente** correspondente na liña de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="658e7-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="658e7-160">Cando a liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="658e7-161">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-162">Imposto estimado</span><span class="sxs-lookup"><span data-stu-id="658e7-162">Estimated Tax</span></span> | <span data-ttu-id="658e7-163">Este é un campo editable para que o usuario poida engadir o importe do imposto estimado na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="658e7-164">Cando unha liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="658e7-165">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-166">Importe da oferta despois de impostos</span><span class="sxs-lookup"><span data-stu-id="658e7-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="658e7-167">Este campo é o importe da liña de oferta despois do imposto e é só de lectura.</span><span class="sxs-lookup"><span data-stu-id="658e7-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="658e7-168">O importe deste campo calcúlase como *Importe da oferta + Imposto*.</span><span class="sxs-lookup"><span data-stu-id="658e7-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="658e7-169">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-170">Límite non superable</span><span class="sxs-lookup"><span data-stu-id="658e7-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="658e7-171">Este campo é editable e só está dispoñible en liñas de oferta baseada en proxecto que teñan un método de facturación de **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="658e7-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="658e7-172">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="658e7-173">Orzamento do cliente</span><span class="sxs-lookup"><span data-stu-id="658e7-173">Customer Budget</span></span> | <span data-ttu-id="658e7-174">Este campo é editable e cópiase desde o campo correspondente na liña de oferta se a oferta se creou a partir dunha oportunidade.</span><span class="sxs-lookup"><span data-stu-id="658e7-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="658e7-175">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="658e7-176">Regras de validación para campos do separador Xeral das liñas de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="658e7-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="658e7-177">**Regra 1**: Se o campo **Tarefas incluídas** está en branco ou se está definido como **Todas as tarefas do proxecto**, inclúese un proxecto na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="658e7-178">**Regra 2**: Se o campo **Tarefas incluídas** campo está en branco ou se está definido como **Todas as tarefas do proxecto**, un proxecto e unha clase de transacción determinada só se poden incluír nunha liña de oferta baseada en proxecto dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="658e7-179">**Regra 3**: Se o campo **Tarefas incluídas** campo está en branco ou se está definido como **Só as tarefas do proxecto seleccionadas**, un proxecto e unha clase de transacción determinada só se poden incluír en varias liñas de oferta baseada en proxecto dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="658e7-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="658e7-180">**Regra 4**: Se unha oportunidade ten varias ofertas, pode haber liñas de oferta de diferentes ofertas que fan referencia ao mesmo proxecto e inclúen a mesma clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="658e7-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="658e7-181">**Regra 5**: Se as ofertas non pertencen á mesma oportunidade, non poden incluír o mesmo proxecto e clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="658e7-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="658e7-182">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="658e7-183">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="658e7-184">
                    <strong>Liña de oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="658e7-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="658e7-186">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="658e7-187">
                    <strong>Incluír tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="658e7-188">
                    <strong>Incluír gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="658e7-189">
                    <strong>Incluír</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="658e7-190">
                    <strong>Cota</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="658e7-191">
                    <strong>Válido/Non válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="658e7-192">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="658e7-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-193">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-194">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-195">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-196">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-197">En branco</span><span class="sxs-lookup"><span data-stu-id="658e7-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-198">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-199">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-200">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-201">Non válido</span><span class="sxs-lookup"><span data-stu-id="658e7-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-202">Infracción da regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="658e7-202">Violation of Rule #2.</span></span> <span data-ttu-id="658e7-203">O tempo, o gasto e as taxas do proxecto P1 inclúense nas liñas de oferta QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="658e7-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-204">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-205">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-206">QL2</span><span class="sxs-lookup"><span data-stu-id="658e7-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-207">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-208">En branco</span><span class="sxs-lookup"><span data-stu-id="658e7-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-209">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-210">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-211">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-212">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-213">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-214">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-215">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-216">En branco</span><span class="sxs-lookup"><span data-stu-id="658e7-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-217">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-218">No</span><span class="sxs-lookup"><span data-stu-id="658e7-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-219">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-220">Non válido</span><span class="sxs-lookup"><span data-stu-id="658e7-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-221">Infracción da regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="658e7-221">Violation of Rule #2.</span></span> <span data-ttu-id="658e7-222">O tempo e as taxas do proxecto P1 inclúense nas liñas de oferta QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="658e7-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-223">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-224">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-225">QL2</span><span class="sxs-lookup"><span data-stu-id="658e7-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-226">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-227">En branco</span><span class="sxs-lookup"><span data-stu-id="658e7-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-228">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-229">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-230">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-231">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-232">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-233">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-234">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-235">En branco</span><span class="sxs-lookup"><span data-stu-id="658e7-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-236">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-237">No</span><span class="sxs-lookup"><span data-stu-id="658e7-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-238">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-239">Válido</span><span class="sxs-lookup"><span data-stu-id="658e7-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="658e7-240">O tempo e as taxas do proxecto P1 están incluídos en QL1.</span><span class="sxs-lookup"><span data-stu-id="658e7-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="658e7-241">O gasto no proxecto P1 está incluído en QL2.</span><span class="sxs-lookup"><span data-stu-id="658e7-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="658e7-242">Non hai superposición no que se inclúe en cada liña de oferta e é válido.</span><span class="sxs-lookup"><span data-stu-id="658e7-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-243">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-244">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-245">QL2</span><span class="sxs-lookup"><span data-stu-id="658e7-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-246">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-247">En branco</span><span class="sxs-lookup"><span data-stu-id="658e7-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-248">No</span><span class="sxs-lookup"><span data-stu-id="658e7-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-249">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-250">No</span><span class="sxs-lookup"><span data-stu-id="658e7-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-251">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-252">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-253">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-254">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-255">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="658e7-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-256">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-257">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-258">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-259">Non válido</span><span class="sxs-lookup"><span data-stu-id="658e7-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-260">Infracción da regra n.º 2. anterior</span><span class="sxs-lookup"><span data-stu-id="658e7-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="658e7-261">Q1 inclúe tempo, gastos e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="658e7-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="658e7-262">QL2 inclúe tempo, gastos e taxas para todo o proxecto P1 e superponse co incluído en Q1.</span><span class="sxs-lookup"><span data-stu-id="658e7-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-263">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-264">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-265">QL2</span><span class="sxs-lookup"><span data-stu-id="658e7-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-266">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-267">En branco</span><span class="sxs-lookup"><span data-stu-id="658e7-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-268">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-269">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-270">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-271">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-272">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-273">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-274">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-275">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="658e7-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-276">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-277">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-278">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-279">Válido</span><span class="sxs-lookup"><span data-stu-id="658e7-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-280">Segundo a regra n.º 3 anterior,</span><span class="sxs-lookup"><span data-stu-id="658e7-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="658e7-281">Q1 inclúe tempo, gastos e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="658e7-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="658e7-282">QL2 inclúe tempo, gastos e taxas para un subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="658e7-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="658e7-283">A única validación adicional é no subconxunto de tarefas en QL1 que son diferentes do subconxunto de tarefas en QL2.</span><span class="sxs-lookup"><span data-stu-id="658e7-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="658e7-284">Isto garante que non haxa superposicións.</span><span class="sxs-lookup"><span data-stu-id="658e7-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="658e7-285">O sistema faino cando as tarefas están asociadas.</span><span class="sxs-lookup"><span data-stu-id="658e7-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-286">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-287">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-288">QL2</span><span class="sxs-lookup"><span data-stu-id="658e7-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-289">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-290">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="658e7-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-291">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-292">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-293">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-294">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-295">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-296">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-297">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-298">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="658e7-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-299">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-300">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-301">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="658e7-302">Válido</span><span class="sxs-lookup"><span data-stu-id="658e7-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-303">Segundo a regra n.º 5, Q1 e Q2 son dúas ofertas da mesma oportunidade, polo que ambas poden estimar para os mesmos compoñentes dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="658e7-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-304">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-305">T2</span><span class="sxs-lookup"><span data-stu-id="658e7-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-306">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-307">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-308">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="658e7-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-309">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-310">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-311">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-312">O1</span><span class="sxs-lookup"><span data-stu-id="658e7-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-313">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-314">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-315">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-316">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="658e7-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-317">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-318">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-319">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="658e7-320">Válido</span><span class="sxs-lookup"><span data-stu-id="658e7-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="658e7-321">Segundo a regra n.º 4, Q1 e Q2 son dúas ofertas de diferentes oportunidades, polo que non poden estimar para os mesmos compoñentes do mesmo proxecto.</span><span class="sxs-lookup"><span data-stu-id="658e7-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="658e7-322">O2</span><span class="sxs-lookup"><span data-stu-id="658e7-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="658e7-323">T1</span><span class="sxs-lookup"><span data-stu-id="658e7-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-324">QL1</span><span class="sxs-lookup"><span data-stu-id="658e7-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-325">P1</span><span class="sxs-lookup"><span data-stu-id="658e7-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="658e7-326">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="658e7-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-327">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="658e7-328">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="658e7-329">Si</span><span class="sxs-lookup"><span data-stu-id="658e7-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="658e7-330">Non válido</span><span class="sxs-lookup"><span data-stu-id="658e7-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]