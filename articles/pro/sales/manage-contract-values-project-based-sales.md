---
title: Visión xeral de liñas de contrato baseado en proxecto
description: Este tema ofrece información sobre o traballo con liñas de contrato baseado en proxecto.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858156"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="4e1a8-103">Visión xeral de liñas de contrato baseado en proxecto</span><span class="sxs-lookup"><span data-stu-id="4e1a8-103">Project-based contract lines overview</span></span>

<span data-ttu-id="4e1a8-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="4e1a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4e1a8-105">As liñas de contrato baseado en proxecto en Dynamics 365 Project Operations están deseñadas para manter os acordos de estimación e facturación de compoñentes específicos do traballo do proxecto nun compromiso.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="4e1a8-106">A estrutura dunha liña de contrato baseado en proxecto amplíase para estimacións de proxecto e escenarios de facturación cos seguintes conceptos:</span><span class="sxs-lookup"><span data-stu-id="4e1a8-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="4e1a8-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="4e1a8-107">Billing method</span></span>
- <span data-ttu-id="4e1a8-108">Asignación de tarefas e proxectos</span><span class="sxs-lookup"><span data-stu-id="4e1a8-108">Project and task mapping</span></span>
- <span data-ttu-id="4e1a8-109">Clases de transaccións incluídas</span><span class="sxs-lookup"><span data-stu-id="4e1a8-109">Included transaction classes</span></span>
- <span data-ttu-id="4e1a8-110">Límite non superable</span><span class="sxs-lookup"><span data-stu-id="4e1a8-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="4e1a8-111">Configuración de imputabilidade.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-111">Chargeability setup</span></span>
- <span data-ttu-id="4e1a8-112">Estimacións utilizando os detalles da liña do contrato</span><span class="sxs-lookup"><span data-stu-id="4e1a8-112">Estimates using contract line details</span></span>
- <span data-ttu-id="4e1a8-113">Cliente da liña de contrato</span><span class="sxs-lookup"><span data-stu-id="4e1a8-113">Contract line customers</span></span>

<span data-ttu-id="4e1a8-114">A seguinte táboa inclúe os campos do separador **Xeral** de liñas de contrato baseado en proxecto que axudan a establecer as bases para unha estimación detallada e completa e arranxos de facturación para o traballo baseado en proxecto.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="4e1a8-115">Campo</span><span class="sxs-lookup"><span data-stu-id="4e1a8-115">Field</span></span> | <span data-ttu-id="4e1a8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e1a8-116">Description</span></span> | <span data-ttu-id="4e1a8-117">Impacto descendente</span><span class="sxs-lookup"><span data-stu-id="4e1a8-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4e1a8-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-118">**Name**</span></span> | <span data-ttu-id="4e1a8-119">Nome da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-119">Name of the contract line.</span></span> <span data-ttu-id="4e1a8-120">Isto identifica o compoñente discreto do contrato que se está a estimar.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="4e1a8-121">Para un contrato de proxecto creado a partir dunha oferta, este valor cópiase a partir dun valor correspondente da liña de oferta baseada en proxecto.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="4e1a8-122">O nome copiado á liña de factura do proxecto que se crea a partir desta liña de contrato cando se crea a factura.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="4e1a8-123">**Método de facturación**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-123">**Billing Method**</span></span> | <span data-ttu-id="4e1a8-124">Nun contrato de proxecto creado a partir dunha oferta, este valor cópiase a partir do campo correspondente da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="4e1a8-125">Este é un conxunto de opcións que representa os dous principais modelos de contratación admitidos por Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4e1a8-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="4e1a8-126">- **Prezo fixo**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-126">- **Fixed Price**</span></span></br><span data-ttu-id="4e1a8-127">- **Hora e material**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-127">- **Time and Material**</span></span> | <span data-ttu-id="4e1a8-128">Baseado no método de facturación da liña de contrato referenciada, procesarase a transacción real.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="4e1a8-129">Se a liña de contrato á que fai referencia o dato real ten un método de facturación de tempo e material, e créanse rexistros de datos reais de custo e vendas non facturadas.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="4e1a8-130">Se a liña de contrato referenciada polo dato real ten un método de facturación de prezo fixo, só se crea un dato real de custo.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="4e1a8-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-131">**Project**</span></span> | <span data-ttu-id="4e1a8-132">Use este campo para identificar o proxecto que se usará para entregar o traballo neste compromiso.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="4e1a8-133">Este valor usarase xunto con **Tarefas incluídas** e **Clases de transaccións incluídas** para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="4e1a8-134">**Tarefas incluídas**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-134">**Included Tasks**</span></span> | <span data-ttu-id="4e1a8-135">Indica se esta liña de contrato inclúe todas as tarefas de proxecto para o proxecto seleccionado ou só un subconxunto das tarefas.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="4e1a8-136">Este é un conxunto de opcións que ten os seguintes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="4e1a8-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="4e1a8-137">- **Todas as tarefas do proxecto**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-137">- **All Project Tasks**</span></span></br><span data-ttu-id="4e1a8-138">- **Só as tarefas de proxecto seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="4e1a8-139">Un valor en branco neste campo é igual a seleccionar **Todas as tarefas do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="4e1a8-140">Se está seleccionado **Só tarefas seleccionadas**, pode seleccionar tarefas específicas e asocialas a esta liña de contrato no separador **Configuración de facturación de tarefas** na páxina **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="4e1a8-141">O valor utilizarase xunto coas clases **Proxecto** e **Transacción incluída** para resolver a referencia da liña de contrato nun dato real ou un rexistro de liña estimado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="4e1a8-142">**Incluír tempo**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-142">**Include Time**</span></span> | <span data-ttu-id="4e1a8-143">Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato as transaccións de tempo ou os custos laborais do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="4e1a8-144">O valor **Non** indica que as transaccións de tempo ou o custo laboral non se incluirán nesta liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="4e1a8-145">O valor **Si** indica que o farán.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="4e1a8-146">Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="4e1a8-147">**Incluír gasto**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-147">**Include Expense**</span></span> | <span data-ttu-id="4e1a8-148">Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato os custos de gasto do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="4e1a8-149">O valor **Non** indica que o custo de gasto non se incluirá nesta liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="4e1a8-150">O valor **Si** indica que o farán.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="4e1a8-151">Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="4e1a8-152">**Incluír materiais**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-152">**Include Materials**</span></span> | <span data-ttu-id="4e1a8-153">Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato os custos de material do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="4e1a8-154">Un valor **Non** indica que os custos de material non se incluirán nesta liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="4e1a8-155">O valor **Si** indica que o farán.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="4e1a8-156">Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="4e1a8-157">**Incluír taxa**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-157">**Include Fee**</span></span> | <span data-ttu-id="4e1a8-158">Un valor **Si**/**Non** indica se se incluirán nesta liña de contrato as taxas de gasto do proxecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="4e1a8-159">O valor **Non** indica que as taxas non se incluirán nesta liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="4e1a8-160">O valor **Si** indica que o farán.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="4e1a8-161">Este valor úsase xunto co proxecto para resolver a referencia da liña de contrato nun rexistro de liña real ou estimado.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="4e1a8-162">**Importe contratado**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-162">**Contracted Amount**</span></span> | <span data-ttu-id="4e1a8-163">Nunha liña de contrato de prezo fixo, este importe é o valor acordado que se facturará ao cliente por todos os compoñentes de traballo asociados a esta liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="4e1a8-164">Nunha liña de contrato de tempo e material, este importe é un valor estimado do que se facturará ao cliente por todos os compoñentes de traballo asociados a esta liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="4e1a8-165">Nun contrato de proxecto que se crea a partir dunha oferta, este valor cópiase a partir do campo correspondente da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="4e1a8-166">Cando unha liña de contrato baseado en proxecto ten detalles de liña, este campo está bloqueado para a súa edición e resúmese a partir do importe nos detalles da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="4e1a8-167">Cando a liña de contrato ten detalles de liña, este valor pode modificarse cambiando os importes nos detalles da liña.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="4e1a8-168">Nunha liña de contrato de prezo fixo, este valor úsase para xerar o importe antes de impostos sobre os fitos periódicos de facturación.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="4e1a8-169">**Imposto estimado**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-169">**Estimated Tax**</span></span> | <span data-ttu-id="4e1a8-170">O usuario pode editar este campo para introducir o importe do imposto estimado na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="4e1a8-171">Cando unha liña de contrato baseado en proxecto ten detalles de liña, este campo está bloqueado para a súa edición e resúmese a partir do importe do imposto nos detalles da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="4e1a8-172">Cando a liña de contrato ten detalles de liña, este valor pode modificarse cambiando os importes do imposto nos detalles da liña.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="4e1a8-173">Nunha liña de contrato de prezo fixo, este valor úsase para xerar o imposto sobre os fitos periódicos de facturación.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="4e1a8-174">**Importe contratado despois de impostos**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="4e1a8-175">O importe la liña de contrato despois de impostos.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-175">The contract line amount after tax.</span></span> <span data-ttu-id="4e1a8-176">Este campo é de só lectura e calcúlase como **Importe contratado + Imposto**.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="4e1a8-177">Nunha liña de contrato de prezo fixo, este valor úsase para xerar fitos periódicos de facturación.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="4e1a8-178">**Límite non superable**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="4e1a8-179">O usuario pode editar este campo e só está dispoñible en liñas de contrato baseado en proxecto que teñen un método de facturación de tempo e material establecido.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="4e1a8-180">O usuario pode editar este campo.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-180">The user can edit this field.</span></span> <span data-ttu-id="4e1a8-181">Cando un dato real de tempo e material fai referencia a esta liña de contrato por tempo e material, o importe real avalíase fronte ao límite non superable na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="4e1a8-182">Esta avaliación complétase despois de contabilizar as cantidades xa gastadas e contabilizadas.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="4e1a8-183">**Orzamento do cliente**</span><span class="sxs-lookup"><span data-stu-id="4e1a8-183">**Customer Budget**</span></span> | <span data-ttu-id="4e1a8-184">Este campo é editable e cópiase do campo correspondente na liña de oferta se o contrato se creou a partir dunha oferta.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="4e1a8-185">Este campo só se usa para obter información e non ten ningunha importancia descendente.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="4e1a8-186">Regras de validación das opcións do separador Xeral das liñas de contrato baseado en proxecto</span><span class="sxs-lookup"><span data-stu-id="4e1a8-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="4e1a8-187">Regra 1: Se o campo **Tarefas incluídas** está en branco ou definido como **Todas as tarefas do proxecto**, todas as tarefas do proxecto están incluídas na liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="4e1a8-188">Regra 2: Cando o campo **Tarefas incluídas** está en branco ou está definido de xeito explícito en **Todas as tarefas do proxecto**, un proxecto e unha determinada clase de transaccións só se poden incluír nunha liña de contrato baseado en proxecto dun contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="4e1a8-189">Regra 3: Cando o campo **Tarefas incluídas** está definido en **Só as tarefas do proxecto seleccionadas**, un proxecto e unha determinada clase de transaccións poden incluírse en varias liñas de contrato baseado en proxecto dun contrato.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="4e1a8-190">
                    <strong>Contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4e1a8-191">
                    <strong>Liña de contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4e1a8-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="4e1a8-193">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4e1a8-194">
                    <strong>Incluír tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4e1a8-195">
                    <strong>Incluír gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4e1a8-196">
                    <strong>Incluír materiais</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4e1a8-197">
                    <strong>Incluír</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="4e1a8-198">
                    <strong>Cota</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="4e1a8-199">
                    <strong>Válido/Non válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="4e1a8-200">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1a8-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-201">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-202">CL1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-203">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-204">En branco</span><span class="sxs-lookup"><span data-stu-id="4e1a8-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-205">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-206">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-207">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-208">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-209">Non válido</span><span class="sxs-lookup"><span data-stu-id="4e1a8-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-210">Infracción da regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-210">Violation of Rule #2.</span></span> <span data-ttu-id="4e1a8-211">O tempo, os gastos, os materiais e as taxas do proxecto P1 inclúense nas dúas liñas de contrato CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-212">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-213">CL2</span><span class="sxs-lookup"><span data-stu-id="4e1a8-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-214">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-215">En branco</span><span class="sxs-lookup"><span data-stu-id="4e1a8-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-216">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-217">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-218">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-219">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-220">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-221">CL1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-222">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-223">En branco</span><span class="sxs-lookup"><span data-stu-id="4e1a8-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-224">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-225">No</span><span class="sxs-lookup"><span data-stu-id="4e1a8-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-226">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-227">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-228">Non válido</span><span class="sxs-lookup"><span data-stu-id="4e1a8-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-229">Infracción da regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-229">Violation of Rule #2.</span></span> <span data-ttu-id="4e1a8-230">O tempo, os materiais e as taxas do proxecto P1 inclúense nas dúas liñas de contrato CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-231">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-232">CL2</span><span class="sxs-lookup"><span data-stu-id="4e1a8-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-233">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-234">En branco</span><span class="sxs-lookup"><span data-stu-id="4e1a8-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-235">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-236">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-237">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-238">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-239">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-240">CL1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-241">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-242">En branco</span><span class="sxs-lookup"><span data-stu-id="4e1a8-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-243">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-244">No</span><span class="sxs-lookup"><span data-stu-id="4e1a8-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-245">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-246">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-247">Válido</span><span class="sxs-lookup"><span data-stu-id="4e1a8-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-248">O tempo, os materiais e as taxas do proxecto P1 inclúense en CL1.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="4e1a8-249">O gasto no proxecto P1 está incluído en CL2.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="4e1a8-250">Non hai superposición no incluído en cada liña de contrato e, polo tanto, é válido.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-251">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-252">CL2</span><span class="sxs-lookup"><span data-stu-id="4e1a8-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-253">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-254">En branco</span><span class="sxs-lookup"><span data-stu-id="4e1a8-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-255">No</span><span class="sxs-lookup"><span data-stu-id="4e1a8-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-256">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-257">No</span><span class="sxs-lookup"><span data-stu-id="4e1a8-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-258">No</span><span class="sxs-lookup"><span data-stu-id="4e1a8-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-259">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-260">CL1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-261">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-262">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="4e1a8-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-263">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-264">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-265">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-266">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-267">Non válido</span><span class="sxs-lookup"><span data-stu-id="4e1a8-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-268">Infracción da regra n.º 2</span><span class="sxs-lookup"><span data-stu-id="4e1a8-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="4e1a8-269">C1 inclúe tempo, materiais, gastos e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4e1a8-270">CL2 inclúe o tempo, os materiais, os gastos e as taxas para todo o proxecto P1 e, polo tanto, superponse co incluído en C1.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-271">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-272">CL2</span><span class="sxs-lookup"><span data-stu-id="4e1a8-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-273">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-274">En branco</span><span class="sxs-lookup"><span data-stu-id="4e1a8-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-275">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-276">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-277">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-278">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-279">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-280">CL1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-281">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-282">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="4e1a8-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-283">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-284">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-285">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-286">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-287">Válido</span><span class="sxs-lookup"><span data-stu-id="4e1a8-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1a8-288">Segundo a regra n.º 3</span><span class="sxs-lookup"><span data-stu-id="4e1a8-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="4e1a8-289">C1 inclúe tempo, gastos, materiais e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4e1a8-290">CL2 inclúe tempo, gastos, materiais e taxas nun subconxunto de tarefas do proxecto P1.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4e1a8-291">A única validación adicional arredor do subconxunto de tarefas en CL1 é diferente do subconxunto de tarefas en CL2 para garantir que non haxa superposicións alí.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="4e1a8-292">O sistema faino cando as tarefas están asociadas.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1a8-293">C1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4e1a8-294">CL2</span><span class="sxs-lookup"><span data-stu-id="4e1a8-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-295">P1</span><span class="sxs-lookup"><span data-stu-id="4e1a8-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="4e1a8-296">Só tarefas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="4e1a8-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-297">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4e1a8-298">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-299">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4e1a8-300">Si</span><span class="sxs-lookup"><span data-stu-id="4e1a8-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
