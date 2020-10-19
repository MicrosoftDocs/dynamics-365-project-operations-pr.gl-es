---
title: Liñas de oferta baseadas en proxecto
description: Este tema ofrece información sobre como liñas de oferta baseada en proxecto para o traballo do proxecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906163"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="c206d-103">Liñas de oferta baseadas en proxecto</span><span class="sxs-lookup"><span data-stu-id="c206d-103">Project-based quote lines</span></span>

<span data-ttu-id="c206d-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="c206d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c206d-105">As liñas de oferta baseada en proxecto están deseñadas para axudar a estimar o traballo do proxecto nun compromiso.</span><span class="sxs-lookup"><span data-stu-id="c206d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c206d-106">A estrutura dunha liña de oferta baseada en proxecto amplíase para as estimacións do proxecto cos seguintes conceptos:</span><span class="sxs-lookup"><span data-stu-id="c206d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c206d-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="c206d-107">Billing Method</span></span>
- <span data-ttu-id="c206d-108">Asignación de proxectos</span><span class="sxs-lookup"><span data-stu-id="c206d-108">Project Mapping</span></span>
- <span data-ttu-id="c206d-109">Clases de transaccións incluídas</span><span class="sxs-lookup"><span data-stu-id="c206d-109">Included Transaction classes</span></span>
- <span data-ttu-id="c206d-110">Límite non superable</span><span class="sxs-lookup"><span data-stu-id="c206d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c206d-111">Configuración de imputabilidade.</span><span class="sxs-lookup"><span data-stu-id="c206d-111">Chargeability setup</span></span>
- <span data-ttu-id="c206d-112">Estimación mediante detalles da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="c206d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c206d-113">Clientes da liña de oferta</span><span class="sxs-lookup"><span data-stu-id="c206d-113">Quote line Customers</span></span>

<span data-ttu-id="c206d-114">A seguinte táboa ofrece información sobre os campos do separador **Xeral** da liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="c206d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c206d-115">Estes campos axudan a establecer as bases para unha estimación detallada e completa do traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="c206d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c206d-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="c206d-116">**Field**</span></span> | <span data-ttu-id="c206d-117">**Relevancia, finalidade e orientación**</span><span class="sxs-lookup"><span data-stu-id="c206d-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="c206d-118">**Impacto descendente**</span><span class="sxs-lookup"><span data-stu-id="c206d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c206d-119">Nome</span><span class="sxs-lookup"><span data-stu-id="c206d-119">Name</span></span> | <span data-ttu-id="c206d-120">O nome da liña de oferta que debería axudarlle a identificar o compoñente discreto da oferta que se estima.</span><span class="sxs-lookup"><span data-stu-id="c206d-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c206d-121">Copiado á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-122">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="c206d-122">Billing Method</span></span> | <span data-ttu-id="c206d-123">Nunha oferta creada a partir dunha oportunidade, este valor copiase desde campo correspondente na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c206d-124">Este campo inclúe os dous modelos de contratación principais admitidos por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c206d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c206d-125">- Prezo fixo</span><span class="sxs-lookup"><span data-stu-id="c206d-125">- Fixed price</span></span></br><span data-ttu-id="c206d-126">- Tempo e material.</span><span class="sxs-lookup"><span data-stu-id="c206d-126">- Time and material.</span></span>| <span data-ttu-id="c206d-127">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-128">Project</span><span class="sxs-lookup"><span data-stu-id="c206d-128">Project</span></span> | <span data-ttu-id="c206d-129">Use este campo opcional para identificar o proxecto que se usará para entregar o traballo neste compromiso.</span><span class="sxs-lookup"><span data-stu-id="c206d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c206d-130">Cando un proxecto está asignado a unha liña de oferta, axuda a configurar tarefas imputables e tamén a traer unha estimación baseada no proxecto á liña de oferta como detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c206d-131">Cando un proxecto non está asignado a unha liña de oferta baseada en proxecto, a estimación debe crearse manualmente creando cada detalle da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c206d-132">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-133">Incluír tempo</span><span class="sxs-lookup"><span data-stu-id="c206d-133">Include Time</span></span> | <span data-ttu-id="c206d-134">O indicador **Si**/**Non** indica se as transaccións de tempo ou os custos laborais do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c206d-135">O valor **Non** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c206d-136">O valor **Si** indica que as transaccións de tempo ou o custo laboral do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c206d-137">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-138">Incluír gasto</span><span class="sxs-lookup"><span data-stu-id="c206d-138">Include Expense</span></span> | <span data-ttu-id="c206d-139">O indicador **Si**/**Non** indica se os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c206d-140">O valor **Non** indica que os custos de gastos do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c206d-141">O valor **Si** indica que os custos de gastos do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c206d-142">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-143">Incluír taxa</span><span class="sxs-lookup"><span data-stu-id="c206d-143">Include Fee</span></span> | <span data-ttu-id="c206d-144">O indicador **Si**/**Non** indica se as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c206d-145">O valor **Non** indica que as taxas do proxecto seleccionado non se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c206d-146">O valor **Si** indica que as taxas do proxecto seleccionado se incluirán na estimación nesta liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c206d-147">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-148">Cantidade ofertada</span><span class="sxs-lookup"><span data-stu-id="c206d-148">Quoted Amount</span></span> | <span data-ttu-id="c206d-149">Esta é a cantidade que se ofertará ao cliente por todo o traballo previsto nesta liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="c206d-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c206d-150">Nunha oferta creada a partir dunha oportunidade, este valor copiase desde o campo **Orzamento do cliente** correspondente na liña de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="c206d-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c206d-151">Cando a liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c206d-152">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-153">Imposto estimado</span><span class="sxs-lookup"><span data-stu-id="c206d-153">Estimated Tax</span></span> | <span data-ttu-id="c206d-154">Este é un campo editable para que o usuario poida engadir o importe do imposto estimado na liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c206d-155">Cando unha liña de oferta baseada en proxecto ten detalles da liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c206d-156">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-157">Importe da oferta despois de impostos</span><span class="sxs-lookup"><span data-stu-id="c206d-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="c206d-158">Este campo é o importe da liña de oferta despois do imposto e é só de lectura.</span><span class="sxs-lookup"><span data-stu-id="c206d-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c206d-159">O importe deste campo calcúlase como *Importe da oferta + Imposto*.</span><span class="sxs-lookup"><span data-stu-id="c206d-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c206d-160">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-161">Límite non superable</span><span class="sxs-lookup"><span data-stu-id="c206d-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="c206d-162">Este campo é editable e só está dispoñible en liñas de oferta baseada en proxecto que teñan un método de facturación de **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="c206d-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c206d-163">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c206d-164">Orzamento do cliente</span><span class="sxs-lookup"><span data-stu-id="c206d-164">Customer Budget</span></span> | <span data-ttu-id="c206d-165">Este campo é editable e cópiase desde o campo correspondente na liña de oferta se a oferta se creou a partir dunha oportunidade.</span><span class="sxs-lookup"><span data-stu-id="c206d-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c206d-166">Este valor de campo se copia á liña de contrato de proxecto que se crea a partir desta liña de oferta cando se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c206d-167">Regras de validación para campos do separador Xeral das liñas de oferta baseada en proxecto</span><span class="sxs-lookup"><span data-stu-id="c206d-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c206d-168">**Regra 1**: Unha determinada clase de transacción no proxecto seleccionado só se pode incluír nunha liña de oferta baseada en proxecto dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="c206d-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c206d-169">**Regra 2**: Se unha oportunidade ten varias ofertas, pode haber liñas de oferta de diferentes ofertas que fan referencia ao mesmo proxecto e inclúen a mesma clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="c206d-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c206d-170">**Regra 3**: Se as ofertas non pertencen á mesma oportunidade, non poden incluír o mesmo proxecto e clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="c206d-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="c206d-171">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c206d-172">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c206d-173">
                    <strong>Liña de oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c206d-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c206d-175">
                    <strong>Incluír tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c206d-176">
                    <strong>Incluír gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c206d-177">
                    <strong>Incluír</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c206d-178">
                    <strong>taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="c206d-179">
                    <strong>Válido/Non válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="c206d-180">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c206d-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c206d-181">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-182">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-183">QL1</span><span class="sxs-lookup"><span data-stu-id="c206d-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-184">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-185">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-186">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-187">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-188">Non válido</span><span class="sxs-lookup"><span data-stu-id="c206d-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-189">Infracción da regra n.º 1.</span><span class="sxs-lookup"><span data-stu-id="c206d-189">Violation of Rule #1.</span></span> <span data-ttu-id="c206d-190">O tempo, o gasto e as taxas do proxecto P1 inclúense nas dúas liñas de oferta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="c206d-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c206d-191">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-192">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-193">QL2</span><span class="sxs-lookup"><span data-stu-id="c206d-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-194">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-195">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-196">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-197">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-197">Yes</span></span> </p>
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
<span data-ttu-id="c206d-198">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-199">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="c206d-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-201">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-202">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-203">No</span><span class="sxs-lookup"><span data-stu-id="c206d-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-204">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-205">Non válido</span><span class="sxs-lookup"><span data-stu-id="c206d-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-206">Infracción da regra n.º 1.</span><span class="sxs-lookup"><span data-stu-id="c206d-206">Violation of Rule #1.</span></span> <span data-ttu-id="c206d-207">O tempo e as taxas do proxecto P1 inclúense nas dúas liñas de oferta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="c206d-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c206d-208">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-209">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-210">QL2</span><span class="sxs-lookup"><span data-stu-id="c206d-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-211">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-212">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-213">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-214">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-214">Yes</span></span> </p>
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
<span data-ttu-id="c206d-215">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-216">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-217">QL1</span><span class="sxs-lookup"><span data-stu-id="c206d-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-218">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-219">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-220">No</span><span class="sxs-lookup"><span data-stu-id="c206d-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-221">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-222">Válido</span><span class="sxs-lookup"><span data-stu-id="c206d-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="c206d-223">O tempo e as taxas do proxecto P1 están incluídos en QL1.</span><span class="sxs-lookup"><span data-stu-id="c206d-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="c206d-224">O gasto no proxecto P1 está incluído en QL2.</span><span class="sxs-lookup"><span data-stu-id="c206d-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="c206d-225">Non hai superposición no que se inclúe en cada liña de oferta, polo que é válido.</span><span class="sxs-lookup"><span data-stu-id="c206d-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c206d-226">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-227">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-228">QL2</span><span class="sxs-lookup"><span data-stu-id="c206d-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-229">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-230">No</span><span class="sxs-lookup"><span data-stu-id="c206d-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-231">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-232">No</span><span class="sxs-lookup"><span data-stu-id="c206d-232">No</span></span> </p>
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
<span data-ttu-id="c206d-233">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-234">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-235">QL1</span><span class="sxs-lookup"><span data-stu-id="c206d-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-236">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-237">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-238">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-239">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-240">Non válido</span><span class="sxs-lookup"><span data-stu-id="c206d-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-241">Infracción da regra n.º 1. anterior</span><span class="sxs-lookup"><span data-stu-id="c206d-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="c206d-242">Q1 inclúe o tempo, os gastos e as taxas para todo o proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="c206d-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c206d-243">QL2 inclúe tempo, gastos e taxas para todo o proxecto P1 e superponse co incluído en Q1.</span><span class="sxs-lookup"><span data-stu-id="c206d-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c206d-244">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-245">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-246">QL2</span><span class="sxs-lookup"><span data-stu-id="c206d-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-247">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-248">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-249">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-250">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-250">Yes</span></span> </p>
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
<span data-ttu-id="c206d-251">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-252">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-253">QL1</span><span class="sxs-lookup"><span data-stu-id="c206d-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-254">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-255">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-256">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-257">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c206d-258">Válido</span><span class="sxs-lookup"><span data-stu-id="c206d-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-259">Segundo a regra n.º 2, Q1 e Q2 son dúas ofertas da mesma oportunidade, polo que ambas poden estimar para os mesmos compoñentes dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="c206d-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c206d-260">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-261">T2</span><span class="sxs-lookup"><span data-stu-id="c206d-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-262">QL1 en Q2</span><span class="sxs-lookup"><span data-stu-id="c206d-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-263">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-264">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-265">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-266">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-266">Yes</span></span> </p>
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
<span data-ttu-id="c206d-267">O1</span><span class="sxs-lookup"><span data-stu-id="c206d-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-268">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-269">QL1</span><span class="sxs-lookup"><span data-stu-id="c206d-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-270">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-271">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-272">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-273">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c206d-274">Válido</span><span class="sxs-lookup"><span data-stu-id="c206d-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c206d-275">Segundo a regra n.º 3, Q1 e Q2 son dúas ofertas de diferentes oportunidades, polo que non poden estimar para os mesmos compoñentes do mesmo proxecto.</span><span class="sxs-lookup"><span data-stu-id="c206d-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c206d-276">O2</span><span class="sxs-lookup"><span data-stu-id="c206d-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c206d-277">T1</span><span class="sxs-lookup"><span data-stu-id="c206d-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-278">QL1</span><span class="sxs-lookup"><span data-stu-id="c206d-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-279">P1</span><span class="sxs-lookup"><span data-stu-id="c206d-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-280">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c206d-281">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c206d-282">Si</span><span class="sxs-lookup"><span data-stu-id="c206d-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c206d-283">Non válido</span><span class="sxs-lookup"><span data-stu-id="c206d-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

