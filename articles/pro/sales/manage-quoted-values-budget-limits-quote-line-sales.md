---
title: Visión xeral de liñas de oferta baseada en proxecto
description: Este tema ofrece información sobre como liñas de oferta baseada en proxecto para o traballo do proxecto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369869"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="fd907-103">Visión xeral de liñas de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="fd907-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="fd907-104">_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="fd907-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fd907-105">As liñas de oferta baseada en proxecto están deseñadas para axudar a estimar o traballo do proxecto nun compromiso.</span><span class="sxs-lookup"><span data-stu-id="fd907-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="fd907-106">A estrutura dunha liña de oferta baseada en proxecto amplíase para as estimacións do proxecto cos seguintes conceptos:</span><span class="sxs-lookup"><span data-stu-id="fd907-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="fd907-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="fd907-107">Billing Method</span></span>
- <span data-ttu-id="fd907-108">Asignación de tarefas e proxectos</span><span class="sxs-lookup"><span data-stu-id="fd907-108">Project and Task Mapping</span></span>
- <span data-ttu-id="fd907-109">Clases de transaccións incluídas</span><span class="sxs-lookup"><span data-stu-id="fd907-109">Included Transaction classes</span></span>
- <span data-ttu-id="fd907-110">Límite non superable</span><span class="sxs-lookup"><span data-stu-id="fd907-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="fd907-111">Configuración de imputabilidade.</span><span class="sxs-lookup"><span data-stu-id="fd907-111">Chargeability setup</span></span>
- <span data-ttu-id="fd907-112">Estimación mediante detalles da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="fd907-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="fd907-113">Clientes da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="fd907-113">Quote line Customers</span></span>

<span data-ttu-id="fd907-114">A seguinte táboa ofrece información sobre os campos do separador **Xeral** da liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd907-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="fd907-115">Estes campos axudan a establecer as bases para unha estimación detallada e completa do traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd907-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="fd907-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="fd907-116">**Field**</span></span> | <span data-ttu-id="fd907-117">**Descrición**</span><span class="sxs-lookup"><span data-stu-id="fd907-117">**Description**</span></span> | <span data-ttu-id="fd907-118">**Impacto descendente**</span><span class="sxs-lookup"><span data-stu-id="fd907-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fd907-119">Nome</span><span class="sxs-lookup"><span data-stu-id="fd907-119">Name</span></span> | <span data-ttu-id="fd907-120">O nome da liña de oferta que lle axuda a identificar o compoñente discreto da oferta que se está a estimar.</span><span class="sxs-lookup"><span data-stu-id="fd907-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="fd907-121">Copiado á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-122">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="fd907-122">Billing Method</span></span> | <span data-ttu-id="fd907-123">Nunha oferta creada a partir dunha oportunidade, este valor copiase desde campo correspondente na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="fd907-124">Este campo inclúe os dous principais modelos de contratación admitidos por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="fd907-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="fd907-125">- Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="fd907-125">- Fixed price</span></span></br><span data-ttu-id="fd907-126">- Tempo e material.</span><span class="sxs-lookup"><span data-stu-id="fd907-126">- Time and material.</span></span>| <span data-ttu-id="fd907-127">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-128">Project</span><span class="sxs-lookup"><span data-stu-id="fd907-128">Project</span></span> | <span data-ttu-id="fd907-129">Use este campo opcional para identificar o proxecto que se usará para entregar o traballo neste compromiso.</span><span class="sxs-lookup"><span data-stu-id="fd907-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="fd907-130">Cando un proxecto está asignado a unha liña de oferta, axuda a configurar tarefas imputables e tamén a traer unha estimación baseada no proxecto á liña de oferta como detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="fd907-131">Cando un proxecto non está asignado a unha liña de oferta baseada en proxecto, a estimación debe crearse manualmente creando cada detalle da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="fd907-132">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="fd907-133">Tarefas incluídas</span><span class="sxs-lookup"><span data-stu-id="fd907-133">Included Tasks</span></span> | <span data-ttu-id="fd907-134">Indica se esta liña de oferta se usa para todas ou algunhas das tarefas do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fd907-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="fd907-135">Este campo ten os seguintes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="fd907-135">This field has the following possible values:</span></span></br><span data-ttu-id="fd907-136">- Todas as tarefas do proxecto</span><span class="sxs-lookup"><span data-stu-id="fd907-136">- All project tasks</span></span></br><span data-ttu-id="fd907-137">- Só tarefas do proxecto seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fd907-137">- Selected project tasks only</span></span></br><span data-ttu-id="fd907-138">Un valor en branco neste campo equivale á opción **Todas as tarefas do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="fd907-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="fd907-139">Cando **Só tarefas do proxecto seleccionadas** está seleccionado na páxina do proxecto, o separador **Configuración de facturación de tarefas** permítelle seleccionar tarefas específicas para asocialas a esta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="fd907-140">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-141">Incluír tempo</span><span class="sxs-lookup"><span data-stu-id="fd907-141">Include Time</span></span> | <span data-ttu-id="fd907-142">Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta as transaccións de tempo ou os custos laborais do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fd907-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-143">O valor **Non** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-144">O valor **Si** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fd907-145">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-146">Incluír gasto</span><span class="sxs-lookup"><span data-stu-id="fd907-146">Include Expense</span></span> | <span data-ttu-id="fd907-147">Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta os custos de gasto do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fd907-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-148">O valor **Non** indica que os custos de gastos do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-149">O valor **Si** indica que os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fd907-150">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-151">Incluír material</span><span class="sxs-lookup"><span data-stu-id="fd907-151">Include Material</span></span> | <span data-ttu-id="fd907-152">Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta os custos de material do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fd907-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-153">Un valor **Non** indica que os custos de material non se incluirán na estimación deste contrato.</span><span class="sxs-lookup"><span data-stu-id="fd907-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-154">Un valor **Si** indica que os custos de material non se incluirán na estimación deste contrato.</span><span class="sxs-lookup"><span data-stu-id="fd907-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fd907-155">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-156">Incluír taxa</span><span class="sxs-lookup"><span data-stu-id="fd907-156">Include Fee</span></span> | <span data-ttu-id="fd907-157">Un valor **Si**/**Non** indica se se incluirán na estimación desta liña de oferta as taxas do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fd907-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-158">O valor **Non** indica que as taxas do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fd907-159">O valor **Si** indica que as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fd907-160">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-161">Cantidade ofertada</span><span class="sxs-lookup"><span data-stu-id="fd907-161">Quoted Amount</span></span> | <span data-ttu-id="fd907-162">Esta é a cantidade que se lle ofrecerá ao cliente por todo o traballo previsto nesta liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd907-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="fd907-163">Nunha oferta creada a partir dunha oportunidade, este valor copiase desde o campo **Orzamento do cliente** correspondente na liña de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="fd907-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="fd907-164">Cando a liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="fd907-165">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-166">Imposto estimado</span><span class="sxs-lookup"><span data-stu-id="fd907-166">Estimated Tax</span></span> | <span data-ttu-id="fd907-167">Este é un campo editable para que o usuario poida engadir o importe do imposto estimado na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="fd907-168">Cando unha liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="fd907-169">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-170">Importe da oferta despois de impostos</span><span class="sxs-lookup"><span data-stu-id="fd907-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="fd907-171">Este campo é o importe da liña de oferta despois do imposto e é só de lectura.</span><span class="sxs-lookup"><span data-stu-id="fd907-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="fd907-172">O importe deste campo calcúlase como *Importe da oferta + Imposto*.</span><span class="sxs-lookup"><span data-stu-id="fd907-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="fd907-173">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-174">Límite non superable</span><span class="sxs-lookup"><span data-stu-id="fd907-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="fd907-175">Este campo é editable e só está dispoñible en liñas de oferta baseada en proxecto que teñan un método de facturación de **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="fd907-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="fd907-176">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fd907-177">Orzamento do cliente</span><span class="sxs-lookup"><span data-stu-id="fd907-177">Customer Budget</span></span> | <span data-ttu-id="fd907-178">Este campo é editable e cópiase desde o campo correspondente na liña de oferta se a oferta se creou a partir dunha oportunidade.</span><span class="sxs-lookup"><span data-stu-id="fd907-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="fd907-179">Este valor copiase na liña de contrato do proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="fd907-180">Regras de validación para campos do separador Xeral das liñas de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="fd907-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="fd907-181">**Regra 1**: Se o campo **Tarefas incluídas** está en branco ou se está definido como **Todas as tarefas do proxecto**, inclúese un proxecto na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="fd907-182">**Regra 2**: Se o campo **Tarefas incluídas** campo está en branco ou se está definido como **Todas as tarefas do proxecto**, un proxecto e unha clase de transacción determinada só se poden incluír nunha liña de oferta baseada en proxecto dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="fd907-183">**Regra 3**: Se o campo **Tarefas incluídas** campo está en branco ou se está definido como **Só as tarefas do proxecto seleccionadas**, un proxecto e unha clase de transacción determinada só se poden incluír en varias liñas de oferta baseada en proxecto dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="fd907-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="fd907-184">**Regra 4**: Se unha oportunidade ten varias ofertas, pode haber liñas de oferta de diferentes ofertas que fan referencia ao mesmo proxecto e inclúen a mesma clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="fd907-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="fd907-185">**Regra 5**: Se as ofertas non pertencen á mesma oportunidade, non poden incluír o mesmo proxecto e clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="fd907-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="fd907-186">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="fd907-187">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="fd907-188">
                    <strong>Liña de oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="fd907-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="fd907-190">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="fd907-191">
                    <strong>Incluír tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="fd907-192">
                    <strong>Incluír gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="fd907-193">
                    <strong>Incluír material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="fd907-194">
                    <strong>Incluír</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="fd907-195">
                    <strong>Cota</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="fd907-196">
                    <strong>Válido/Non válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="fd907-197">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fd907-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-198">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-199">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-200">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-201">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-202">En branco</span><span class="sxs-lookup"><span data-stu-id="fd907-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-203">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-204">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-205">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-206">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-207">Non válido</span><span class="sxs-lookup"><span data-stu-id="fd907-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-208">Infracción da regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="fd907-208">Violation of Rule #2.</span></span> <span data-ttu-id="fd907-209">O tempo, o gasto e as taxas do proxecto P1 inclúense nas liñas de oferta QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-210">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-211">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-212">QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-213">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-214">En branco</span><span class="sxs-lookup"><span data-stu-id="fd907-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-215">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-216">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-217">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-218">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-219">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-220">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-221">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-222">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-223">En branco</span><span class="sxs-lookup"><span data-stu-id="fd907-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-224">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-225">No</span><span class="sxs-lookup"><span data-stu-id="fd907-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-226">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-227">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-228">Non válido</span><span class="sxs-lookup"><span data-stu-id="fd907-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-229">Infracción da regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="fd907-229">Violation of Rule #2.</span></span> <span data-ttu-id="fd907-230">O tempo, o material e as taxas do proxecto P1 inclúense nas liñas de oferta QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-231">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-232">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-233">QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-234">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-235">En branco</span><span class="sxs-lookup"><span data-stu-id="fd907-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-236">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-237">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-238">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-239">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-240">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-241">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-242">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-243">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-244">En branco</span><span class="sxs-lookup"><span data-stu-id="fd907-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-245">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-246">No</span><span class="sxs-lookup"><span data-stu-id="fd907-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-247">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-248">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-249">Válido</span><span class="sxs-lookup"><span data-stu-id="fd907-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-250">O tempo, o material e as taxas do proxecto P1 inclúense en QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="fd907-251">O gasto no proxecto P1 está incluído en QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="fd907-252">Non hai superposición no incluído en cada liña de oferta e, polo tanto, é válido.</span><span class="sxs-lookup"><span data-stu-id="fd907-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-253">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-254">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-255">QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-256">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-257">En branco</span><span class="sxs-lookup"><span data-stu-id="fd907-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-258">No</span><span class="sxs-lookup"><span data-stu-id="fd907-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-259">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-260">No</span><span class="sxs-lookup"><span data-stu-id="fd907-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-261">No</span><span class="sxs-lookup"><span data-stu-id="fd907-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-262">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-263">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-264">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-265">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-266">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fd907-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-267">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-268">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-269">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-270">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-271">Non válido</span><span class="sxs-lookup"><span data-stu-id="fd907-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-272">Infracción da regra n.º 2</span><span class="sxs-lookup"><span data-stu-id="fd907-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="fd907-273">Q1 inclúe tempo, material, gastos e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="fd907-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="fd907-274">QL2 inclúe tempo, gastos e taxas para todo o proxecto P1 e, polo tanto, solápase co incluído en Q1.</span><span class="sxs-lookup"><span data-stu-id="fd907-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-275">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-276">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-277">QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-278">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-279">En branco</span><span class="sxs-lookup"><span data-stu-id="fd907-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-280">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-281">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-282">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-283">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-284">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-285">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-286">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-287">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-288">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fd907-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-289">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-290">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-291">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-292">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-293">Válido</span><span class="sxs-lookup"><span data-stu-id="fd907-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-294">Segundo a regra n.º 3</span><span class="sxs-lookup"><span data-stu-id="fd907-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="fd907-295">Q1 inclúe tempo, material, gastos e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="fd907-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fd907-296">QL2 inclúe tempo, material, gastos e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="fd907-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fd907-297">A única validación adicional arredor do subconxunto de tarefas en QL1, que é diferente do subconxunto de tarefas en QL2 para garantir que non haxa superposición.</span><span class="sxs-lookup"><span data-stu-id="fd907-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="fd907-298">O sistema faino cando as tarefas están asociadas.</span><span class="sxs-lookup"><span data-stu-id="fd907-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-299">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-300">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-301">QL2</span><span class="sxs-lookup"><span data-stu-id="fd907-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-302">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-303">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fd907-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-304">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-305">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-306">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-307">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-308">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-309">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-310">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-311">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-312">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="fd907-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-313">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-314">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-315">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-316">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-317">Válido</span><span class="sxs-lookup"><span data-stu-id="fd907-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-318">Segundo a regra n.º 5, Q1 e Q2 son dúas ofertas na mesma oportunidade, polo que ambas poden estimar para os mesmos compoñentes dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd907-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-319">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-320">T2</span><span class="sxs-lookup"><span data-stu-id="fd907-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-321">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-322">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-323">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="fd907-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-324">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-325">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-326">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-327">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-328">O1</span><span class="sxs-lookup"><span data-stu-id="fd907-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-329">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-330">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-331">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-332">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="fd907-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-333">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-334">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-335">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-336">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-337">Non válido</span><span class="sxs-lookup"><span data-stu-id="fd907-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fd907-338">Segundo a regra n.º 4, Q1 e Q2 son dúas ofertas en oportunidades diferentes, polo que non poden estimar para os mesmos compoñentes dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="fd907-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="fd907-339">O2</span><span class="sxs-lookup"><span data-stu-id="fd907-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="fd907-340">T1</span><span class="sxs-lookup"><span data-stu-id="fd907-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="fd907-341">QL1</span><span class="sxs-lookup"><span data-stu-id="fd907-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-342">P1</span><span class="sxs-lookup"><span data-stu-id="fd907-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="fd907-343">Todas as tarefas do proxecto ou en branco</span><span class="sxs-lookup"><span data-stu-id="fd907-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="fd907-344">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="fd907-345">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fd907-346">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fd907-347">Si</span><span class="sxs-lookup"><span data-stu-id="fd907-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
