---
title: Contratos do proxecto
description: Este tema ofrece exemplos dos contratos de proxecto que pode crear para varios tipos de proxectos e fontes de financiamento e de como pode xestionar os contratos e facturar aos clientes do proxecto.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999759"
---
# <a name="project-contracts"></a><span data-ttu-id="6dd27-103">Contratos do proxecto</span><span class="sxs-lookup"><span data-stu-id="6dd27-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dd27-104">Este artigo ofrece exemplos dos contratos de proxecto que pode crear para varios tipos de proxectos e fontes de financiamento e de como pode xestionar os contratos e facturar aos clientes do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="6dd27-105">O tipo de proxecto que cree para un contrato de proxecto determina o método que se usa para facturar aos clientes do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="6dd27-106">Pode cambiar un contrato de proxecto e o proxecto relacionado, pero non pode cambiar o tipo de proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="6dd27-107">Ao usar un contrato de proxecto, pode facturar un ou máis proxectos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6dd27-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="6dd27-108">O contrato do proxecto tamén axuda a garantir un procedemento de facturación uniforme para cada subproxecto dunha estrutura de proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="6dd27-109">Todo proxecto que se facturará debe estar asociado a un contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="6dd27-110">A configuración dun contrato de proxecto aplícase a todos os proxectos e subproxectos asociados a ese contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="6dd27-111">Un contrato de proxecto pode especificar unha ou máis fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="6dd27-112">Polo tanto, pode dividir a facturación entre varios patrocinadores, establecer límites de financiamento para que non se facture ás fontes de financiamento máis dun importe especificado e configurar regras de financiamento para cobrar gastos.</span><span class="sxs-lookup"><span data-stu-id="6dd27-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="6dd27-113">Financiamento para contratos de proxectos</span><span class="sxs-lookup"><span data-stu-id="6dd27-113">Funding for project contracts</span></span>
<span data-ttu-id="6dd27-114">Algúns contratos de proxecto especifican que varias partes comparten a responsabilidade de financiar os custos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="6dd27-115">Aquí van algúns exemplos:</span><span class="sxs-lookup"><span data-stu-id="6dd27-115">Here are some examples:</span></span>

-   <span data-ttu-id="6dd27-116">Un gran cliente que ten varias divisións solicita que o financiamento dun proxecto se divida por división.</span><span class="sxs-lookup"><span data-stu-id="6dd27-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="6dd27-117">A súa empresa comparte os custos dun gran proxecto cunha organización externa.</span><span class="sxs-lookup"><span data-stu-id="6dd27-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="6dd27-118">Un proxecto de carreteira está cofinanciado por dous concellos.</span><span class="sxs-lookup"><span data-stu-id="6dd27-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="6dd27-119">Un proxecto de ponte está financiado por unha subvención do goberno e unha corporación privada.</span><span class="sxs-lookup"><span data-stu-id="6dd27-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="6dd27-120">En Dynamics 365 Finance, pode dividir a facturación dunha única transacción ou un proxecto completo entre varios clientes, subvencións ou organizacións.</span><span class="sxs-lookup"><span data-stu-id="6dd27-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="6dd27-121">Nos proxectos que teñen varios patrocinadores, todas as partes que contribúen ao financiamento dun proxecto de financiamento avanzado chámanse fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="6dd27-122">Despois de que un cliente, organización ou subvención se defina como unha fonte de financiamento, pódese asignar a unha ou máis regras de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="6dd27-123">As regras de financiamento conteñen os criterios que determinan como se asignan os cargos ás distintas fontes de financiamento dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="6dd27-124">Debido a que os artigos almacenados, como os que aparecen nas solicitudes de compra e nos pedidos de compra, non se poden dividir, o importe do custo non se pode dividir entre varias fontes de financiamento no momento da distribución.</span><span class="sxs-lookup"><span data-stu-id="6dd27-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="6dd27-125">Polo tanto, o valor da fonte de financiamento segue sendo 0 (cero) ata que se contabilice a emisión do inventario.</span><span class="sxs-lookup"><span data-stu-id="6dd27-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="6dd27-126">Cando se contabiliza a emisión do inventario, o importe do custo distribúese segundo as regras de distribución da conta para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="6dd27-127">Aquí ten algúns pasos que pode seguir para facer máis doado dividir a facturación entre varias fontes de financiamento:</span><span class="sxs-lookup"><span data-stu-id="6dd27-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="6dd27-128">Especifique que todas as transaccións que se introducen nun proxecto utilizan a mesma moeda de vendas que o contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="6dd27-129">Configure límites de financiamento para que non se facture a unha fonte de financiamento máis dun importe especificado para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="6dd27-130">Configure as regras de financiamento e os límites de financiamento para cada traballador, artigo, categoría, grupo de categorías e tipo de transacción (ou para todos os tipos de transacción).</span><span class="sxs-lookup"><span data-stu-id="6dd27-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="6dd27-131">Seleccione as datas opcionais de inicio e fin para definir o período en que cada regra de financiamento é válida.</span><span class="sxs-lookup"><span data-stu-id="6dd27-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="6dd27-132">Especifique a porcentaxe da que é responsable cada fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="6dd27-133">Especifique que fonte de financiamento é responsable de redondear as diferenzas causadas polos cálculos de asignación de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="6dd27-134">Configure regras que determinen como se facturan os custos do proxecto a clientes externos e se cargan ás organizacións internas.</span><span class="sxs-lookup"><span data-stu-id="6dd27-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="6dd27-135">Rexistre as transaccións nunha conta de financiamento en espera ata que se poida obter financiamento adicional ou ata que decida asumir os custos internamente.</span><span class="sxs-lookup"><span data-stu-id="6dd27-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="6dd27-136">Para determinar que grupo fiscal se asocia a unha transacción, búscase no proxecto unha atribución de grupo fiscal.</span><span class="sxs-lookup"><span data-stu-id="6dd27-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="6dd27-137">Se non se realizou ningunha atribución de grupo fiscal ao nivel do proxecto, búscase no contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="6dd27-138">Exemplo: Varias fontes de financiamento (simple)</span><span class="sxs-lookup"><span data-stu-id="6dd27-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="6dd27-139">A seguinte táboa ofrece escenarios para xestionar a asignación de financiamento entre varias fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="6dd27-140">Estes escenarios baséanse nos seguintes supostos:</span><span class="sxs-lookup"><span data-stu-id="6dd27-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="6dd27-141">A configuración de prioridades inclúese na asignación de fondos antes de que se apliquen outros criterios de regras de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="6dd27-142">Non se especificou un intervalo de datas para definir o período cando a regra de financiamento é válida.</span><span class="sxs-lookup"><span data-stu-id="6dd27-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dd27-143"><strong>Escenario</strong></span><span class="sxs-lookup"><span data-stu-id="6dd27-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="6dd27-144"><strong>Fonte de financiamento</strong></span><span class="sxs-lookup"><span data-stu-id="6dd27-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="6dd27-145"><strong>Porcentaxe de asignación</strong></span><span class="sxs-lookup"><span data-stu-id="6dd27-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="6dd27-146"><strong>Prioridade de asignación</strong></span><span class="sxs-lookup"><span data-stu-id="6dd27-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dd27-147">Vostede quere asignar custos a unha fonte de financiamento ata esgotar os seus fondos, asignar custos a unha segunda fonte de financiamento ata esgotar os seus fondos e, finalmente, asignar os custos restantes a unha terceira fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6dd27-148">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="6dd27-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="6dd27-149">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="6dd27-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="6dd27-150">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="6dd27-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-151">100 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-151">100%</span></span></li>
<li><span data-ttu-id="6dd27-152">100 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-152">100%</span></span></li>
<li><span data-ttu-id="6dd27-153">100 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-154">1</span><span class="sxs-lookup"><span data-stu-id="6dd27-154">1</span></span></li>
<li><span data-ttu-id="6dd27-155">2</span><span class="sxs-lookup"><span data-stu-id="6dd27-155">2</span></span></li>
<li><span data-ttu-id="6dd27-156">3</span><span class="sxs-lookup"><span data-stu-id="6dd27-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dd27-157">Vostede quere destinar o 75 por cento dos custos a unha fonte de financiamento e o 25 por cento a unha segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="6dd27-158">Cando se esgota calquera desas fontes de financiamento, quere pagar os custos restantes dunha terceira fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6dd27-159">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="6dd27-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="6dd27-160">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="6dd27-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="6dd27-161">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="6dd27-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-162">75 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-162">75%</span></span></li>
<li><span data-ttu-id="6dd27-163">25 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-163">25%</span></span></li>
<li><span data-ttu-id="6dd27-164">100 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-165">1</span><span class="sxs-lookup"><span data-stu-id="6dd27-165">1</span></span></li>
<li><span data-ttu-id="6dd27-166">1</span><span class="sxs-lookup"><span data-stu-id="6dd27-166">1</span></span></li>
<li><span data-ttu-id="6dd27-167">2</span><span class="sxs-lookup"><span data-stu-id="6dd27-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dd27-168">Vostede quere destinar o 75 por cento dos custos a unha fonte de financiamento e o 25 por cento a unha segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="6dd27-169">Cando se esgota calquera desas fontes de financiamento, quere dividir os custos restantes entre unha terceira fonte de financiamento e unha cuarta fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6dd27-170">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="6dd27-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="6dd27-171">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="6dd27-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="6dd27-172">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="6dd27-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="6dd27-173">Fonte de financiamento 4</span><span class="sxs-lookup"><span data-stu-id="6dd27-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-174">75 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-174">75%</span></span></li>
<li><span data-ttu-id="6dd27-175">25 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-175">25%</span></span></li>
<li><span data-ttu-id="6dd27-176">50 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-176">50%</span></span></li>
<li><span data-ttu-id="6dd27-177">50 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-178">1</span><span class="sxs-lookup"><span data-stu-id="6dd27-178">1</span></span></li>
<li><span data-ttu-id="6dd27-179">1</span><span class="sxs-lookup"><span data-stu-id="6dd27-179">1</span></span></li>
<li><span data-ttu-id="6dd27-180">2</span><span class="sxs-lookup"><span data-stu-id="6dd27-180">2</span></span></li>
<li><span data-ttu-id="6dd27-181">2</span><span class="sxs-lookup"><span data-stu-id="6dd27-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dd27-182">Vostede quere destinar o primeiro 25 por cento dos custos a unha fonte de financiamento e o resto a unha segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6dd27-183">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="6dd27-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="6dd27-184">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="6dd27-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-185">25 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-185">25%</span></span></li>
<li><span data-ttu-id="6dd27-186">100 %</span><span class="sxs-lookup"><span data-stu-id="6dd27-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6dd27-187">1</span><span class="sxs-lookup"><span data-stu-id="6dd27-187">1</span></span></li>
<li><span data-ttu-id="6dd27-188">2</span><span class="sxs-lookup"><span data-stu-id="6dd27-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="6dd27-189">Exemplo: Varias fontes de financiamento (complexo)</span><span class="sxs-lookup"><span data-stu-id="6dd27-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="6dd27-190">Vostede ten tres fontes de financiamento que desexa empregar na seguinte orde:</span><span class="sxs-lookup"><span data-stu-id="6dd27-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="6dd27-191">Usar a fonte de financiamento 2 e a fonte de financiamento 3 por igual ata esgotar a fonte de financiamento 2.</span><span class="sxs-lookup"><span data-stu-id="6dd27-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="6dd27-192">Continuar usando a fonte de financiamento 3 ata esgotala.</span><span class="sxs-lookup"><span data-stu-id="6dd27-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="6dd27-193">Usar a fonte de financiamento 1 despois de esgotar a fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="6dd27-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="6dd27-194">Para lograr este obxectivo, debe facer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dd27-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="6dd27-195">Configurar límites de financiamento para a fonte de financiamento 2 e a fonte de financiamento 3, polas súas respectivas cantidades.</span><span class="sxs-lookup"><span data-stu-id="6dd27-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="6dd27-196">Crear as seguintes regras de financiamento:</span><span class="sxs-lookup"><span data-stu-id="6dd27-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="6dd27-197">Regra 1 (Prioridade 1): Asignar o 50 por cento das transaccións á fonte de financiamento 2 e o 50 por cento á fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="6dd27-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="6dd27-198">Regra 2 (Prioridade 2): Asignar o 100 por cento das transaccións á fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="6dd27-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="6dd27-199">Regra 3 (Prioridade 3): Asignar o 100 por cento das transaccións á fonte de financiamento 1.</span><span class="sxs-lookup"><span data-stu-id="6dd27-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="6dd27-200">Esta configuración funciona porque as transaccións se contrastan con regras e límites para determinar se algunha delas se aplica á transacción.</span><span class="sxs-lookup"><span data-stu-id="6dd27-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="6dd27-201">Se non se aplican regras nin límites específicos á transacción, aplícase a regra Todas as transaccións.</span><span class="sxs-lookup"><span data-stu-id="6dd27-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="6dd27-202">A regra Todas as transaccións coincide con todas as transaccións.</span><span class="sxs-lookup"><span data-stu-id="6dd27-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="6dd27-203">Se se atopa unha regra que coincide cunha transacción, a porcentaxe que se asignou nesa regra aplicase primeiro, pero só despois de que as coincidencias se contrasten con calquera límite establecido.</span><span class="sxs-lookup"><span data-stu-id="6dd27-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="6dd27-204">Se se cumpriu un límite e se esgotan os fondos dunha fonte de financiamento, non se terá en conta a regra de financiamento asociada ao límite de financiamento e o programa comproba a seguinte regra que se aplica.</span><span class="sxs-lookup"><span data-stu-id="6dd27-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="6dd27-205">Nalgúns casos, só unha parte dunha transacción pode asignarse baixo unha regra.</span><span class="sxs-lookup"><span data-stu-id="6dd27-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="6dd27-206">Isto podería ocorrer porque se alcanza un límite cando se asigna a transacción.</span><span class="sxs-lookup"><span data-stu-id="6dd27-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="6dd27-207">Neste caso, só se asigna unha determinada cantidade segundo esa regra, por exemplo, o 50 por cento a cada fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="6dd27-208">É o caso da regra 1, que se describe anteriormente nesta sección.</span><span class="sxs-lookup"><span data-stu-id="6dd27-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="6dd27-209">O resto asígnase segundo a seguinte regra da secuencia.</span><span class="sxs-lookup"><span data-stu-id="6dd27-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="6dd27-210">A seguinte táboa examina este escenario con máis detalle.</span><span class="sxs-lookup"><span data-stu-id="6dd27-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dd27-211"><strong>Foco</strong></span><span class="sxs-lookup"><span data-stu-id="6dd27-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="6dd27-212"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="6dd27-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dd27-213">Regras de financiamento</span><span class="sxs-lookup"><span data-stu-id="6dd27-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="6dd27-214">Regra 1 (Prioridade 1): Todas as transaccións.</span><span class="sxs-lookup"><span data-stu-id="6dd27-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="6dd27-215">Asigne á fonte de financiamento 2 o 50 % e á fonte de financiamento 3 o 50 %.</span><span class="sxs-lookup"><span data-stu-id="6dd27-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="6dd27-216">Regra 2 (Prioridade 2): Todas as transaccións.</span><span class="sxs-lookup"><span data-stu-id="6dd27-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="6dd27-217">Asigne á fonte de financiamento 3 o 100 %.</span><span class="sxs-lookup"><span data-stu-id="6dd27-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="6dd27-218">Regra 3 (Prioridade 2): Todas as transaccións.</span><span class="sxs-lookup"><span data-stu-id="6dd27-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="6dd27-219">Asigne á fonte de financiamento 1 o 100 %.</span><span class="sxs-lookup"><span data-stu-id="6dd27-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dd27-220">Límites de financiamento</span><span class="sxs-lookup"><span data-stu-id="6dd27-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="6dd27-221">Límite da fonte de financiamento 1 = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="6dd27-222">Límite da fonte de financiamento 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="6dd27-223">Límite da fonte de financiamento 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dd27-224">Transacción 1</span><span class="sxs-lookup"><span data-stu-id="6dd27-224">Transaction 1</span></span></td>
<td><span data-ttu-id="6dd27-225"><strong>Importe da transacción:</strong> 100,00<strong>Financiamento:</strong> A transacción só se paga segundo a regra 1, porque a transacción se paga totalmente despois de aplicarse a regra 1.</span><span class="sxs-lookup"><span data-stu-id="6dd27-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="6dd27-226">A transacción finánciase equitativamente entre a fonte de financiamento 2 e a fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="6dd27-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="6dd27-227">Fonte de financiamento 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="6dd27-228">Fonte de financiamento 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dd27-229">Transacción 2</span><span class="sxs-lookup"><span data-stu-id="6dd27-229">Transaction 2</span></span></td>
<td><span data-ttu-id="6dd27-230"><strong>Importe da transacción:</strong> 5000,00<strong>Financiamento:</strong> A transacción págase segundo as tres regras.</span><span class="sxs-lookup"><span data-stu-id="6dd27-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="6dd27-231"><strong>Regra 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="6dd27-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="6dd27-232">Fonte de financiamento 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="6dd27-233">Fonte de financiamento 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="6dd27-234">
<strong>Regra 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="6dd27-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="6dd27-235">Fonte de financiamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="6dd27-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="6dd27-236">
<strong>Regra 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="6dd27-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="6dd27-237">Fonte de financiamento 1: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="6dd27-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dd27-238">Total de fondos que se distribúen para cada fonte de financiamento</span><span class="sxs-lookup"><span data-stu-id="6dd27-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="6dd27-239">Fonte de financiamento 1: 3850,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="6dd27-240">Fonte de financiamento 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="6dd27-241">Fonte de financiamento 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="6dd27-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="6dd27-242">Regras de facturación</span><span class="sxs-lookup"><span data-stu-id="6dd27-242">Billing rules</span></span>
<span data-ttu-id="6dd27-243">Cando negocia un contrato de proxecto cun cliente, vostede define como e cando pode facturar ao cliente o traballo nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="6dd27-244">Despois de configurar o contrato do proxecto e o proxecto, pode configurar as regras de facturación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="6dd27-245">As regras de facturación baséanse nos termos do proxecto que se especifican no contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="6dd27-246">As regras de facturación que pode crear dependen das condicións do contrato do proxecto e do tipo de proxecto, como Tempo e material ou Prezo fixo, que vostede asocia á regra de facturación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="6dd27-247">Pode crear máis dunha regra de facturación para un contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="6dd27-248">Tamén pode asignar unha regra de facturación a varios proxectos asociados ao mesmo contrato de proxecto e con condicións de facturación similares.</span><span class="sxs-lookup"><span data-stu-id="6dd27-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="6dd27-249">Pode configurar os seguintes tipos de regras de facturación:</span><span class="sxs-lookup"><span data-stu-id="6dd27-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="6dd27-250">**Unidade de entrega** - Facture a un cliente cando complete unha unidade de entrega.</span><span class="sxs-lookup"><span data-stu-id="6dd27-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="6dd27-251">Vostede define as unidades de entrega no contrato.</span><span class="sxs-lookup"><span data-stu-id="6dd27-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="6dd27-252">**Progreso** - Facture a un cliente cando complete unha porcentaxe especificada do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="6dd27-253">Pode configurar unha regra de facturación para calcular automaticamente a porcentaxe de traballo realizado ou pode calcular manualmente a porcentaxe de traballo rematado e o importe para facturar ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dd27-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="6dd27-254">**Fito** - Facture a un cliente o importe total dun fito do proxecto cando se alcance o fito.</span><span class="sxs-lookup"><span data-stu-id="6dd27-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="6dd27-255">**Tarifa** - Facture a un cliente os seus servizos máis unha comisión de xestión, que normalmente é unha porcentaxe do custo dos servizos.</span><span class="sxs-lookup"><span data-stu-id="6dd27-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="6dd27-256">**Tempo e material** - Facture a un cliente polo valor do tempo e os materiais que se utilizan nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="6dd27-257">Para todo tipo de regras de facturación, pode especificar unha porcentaxe de retención que se deduce das facturas dos clientes ata que un proxecto alcanza a fase acordada.</span><span class="sxs-lookup"><span data-stu-id="6dd27-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="6dd27-258">A porcentaxe de retención do pagamento especifícase no contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="6dd27-259">O importe calcúlase en función do valor total das liñas nunha factura do cliente e réstase del.</span><span class="sxs-lookup"><span data-stu-id="6dd27-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="6dd27-260">Para as regras de facturación **Tempo e material** e **Progreso**, pode atribuír categorías imputables.</span><span class="sxs-lookup"><span data-stu-id="6dd27-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="6dd27-261">As categorías imputables indican as transaccións que deben incluírse nas facturas dos clientes.</span><span class="sxs-lookup"><span data-stu-id="6dd27-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="6dd27-262">Cando estea listo para facturar ao cliente, o importe a facturar polo proxecto calcúlase en función das regras de facturación e xérase unha proposta de factura do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="6dd27-263">As seguintes seccións ofrecen exemplos que mostran como configurar e xestionar as regras de facturación dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="6dd27-264">Exemplo: Crear unha regra de facturación baseada no número de unidades entregadas</span><span class="sxs-lookup"><span data-stu-id="6dd27-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="6dd27-265">A súa organización asina un contrato para proporcionar un total de cinco sesións de formación aos empregados dun cliente cun custo de 10 000 por sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="6dd27-266">Vostede factura ao cliente despois de cada sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="6dd27-267">Cando configura as regras de facturación do contrato, usa os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6dd27-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="6dd27-268">A unidade de entrega é unha sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="6dd27-269">O prezo unitario é de 10 000 por sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="6dd27-270">O número total de unidades é de cinco sesións de formación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="6dd27-271">Cando remate unha sesión de formación, pode crear unha factura por 10 000 para a primeira unidade que se entregou e enviar a factura ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dd27-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="6dd27-272">Exemplo: Crear unha regra de facturación baseada nunha porcentaxe especificada de finalización do proxecto (cálculo manual)</span><span class="sxs-lookup"><span data-stu-id="6dd27-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="6dd27-273">A súa organización, unha empresa de consultoría de software, asina un contrato cun cliente para desenvolver parte dun produto que o cliente está a desenvolver.</span><span class="sxs-lookup"><span data-stu-id="6dd27-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="6dd27-274">A súa organización acepta entregar o código do software nun período de seis meses.</span><span class="sxs-lookup"><span data-stu-id="6dd27-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="6dd27-275">O cliente comprométese a pagar á súa organización un total de 100 000 polo traballo.</span><span class="sxs-lookup"><span data-stu-id="6dd27-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="6dd27-276">Vostede crea unha regra de facturación para facturar ao cliente en función da porcentaxe de traballo finalizado no proxecto, segundo se especifica no contrato.</span><span class="sxs-lookup"><span data-stu-id="6dd27-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="6dd27-277">Ao final do primeiro mes, reúnese co cliente para determinar a porcentaxe de traballo realizado.</span><span class="sxs-lookup"><span data-stu-id="6dd27-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="6dd27-278">Despois de que vostede e o cliente revisen o proxecto, decide que o proxecto está completado nun 15 por cento.</span><span class="sxs-lookup"><span data-stu-id="6dd27-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="6dd27-279">Vostede crea unha factura por 15 000 (15 por cento de 100 000) e envíaa ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dd27-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="6dd27-280">Exemplo: Crear unha regra de facturación baseada nunha porcentaxe especificada de finalización do proxecto (cálculo automático)</span><span class="sxs-lookup"><span data-stu-id="6dd27-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="6dd27-281">A súa organización, unha empresa de desenvolvemento de software, acepta desenvolver un paquete de contabilidade de nóminas para un cliente por 30 000.</span><span class="sxs-lookup"><span data-stu-id="6dd27-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="6dd27-282">O cliente comprométese a pagar á súa organización segundo a porcentaxe do traballo finalizada.</span><span class="sxs-lookup"><span data-stu-id="6dd27-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="6dd27-283">Vostede calcula que os custos do proxecto son 20 000.</span><span class="sxs-lookup"><span data-stu-id="6dd27-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="6dd27-284">O contrato do proxecto especifica as categorías de traballo que vostede usa no proceso de facturación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="6dd27-285">Vostede configura regras de facturación que calculan automaticamente os importes da factura para a porcentaxe de traballo que se completa para cada categoría.</span><span class="sxs-lookup"><span data-stu-id="6dd27-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="6dd27-286">Vostede configura un orzamento para cada categoría:</span><span class="sxs-lookup"><span data-stu-id="6dd27-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="6dd27-287">**Desenvolvemento** - Custo de 15 000 e ingresos de 20 000</span><span class="sxs-lookup"><span data-stu-id="6dd27-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="6dd27-288">**Instalación** - Custo de 5000 e ingresos de 10 000</span><span class="sxs-lookup"><span data-stu-id="6dd27-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="6dd27-289">Cando crea unha factura de cliente por primeira vez, o importe da factura calcúlase automaticamente en función da seguinte información:</span><span class="sxs-lookup"><span data-stu-id="6dd27-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="6dd27-290">Despois dun mes, o traballador do proxecto envía unha folla de control horario para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="6dd27-291">O custo das horas do traballador é de 5000 para o desenvolvemento e 1000 para a instalación.</span><span class="sxs-lookup"><span data-stu-id="6dd27-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="6dd27-292">Os traballos de desenvolvemento remataron nun 33 por cento (5000 de custo real/15 000 de custo orzamentario) e os traballos de instalación remataron nun 20 por cento (1000 de custo real/5000 de custo orzamentario).</span><span class="sxs-lookup"><span data-stu-id="6dd27-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="6dd27-293">O importe da factura de 8667 calcúlase automaticamente (33 por cento de 20 000 + 20 por cento de 10 000).</span><span class="sxs-lookup"><span data-stu-id="6dd27-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="6dd27-294">Vostede crea unha factura por 8667 e envíaa ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dd27-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="6dd27-295">Exemplo: Crear unha regra de facturación baseada en fitos acordados</span><span class="sxs-lookup"><span data-stu-id="6dd27-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="6dd27-296">A súa organización, unha empresa de consultoría de xestión, acepta realizar investigacións de mercado para un produto de consumo que o cliente ten previsto vender.</span><span class="sxs-lookup"><span data-stu-id="6dd27-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="6dd27-297">O cliente comprométese a utilizar os seus servizos durante un período de tres meses, a partir de marzo, e comprométese a pagarlle á organización 50 000.</span><span class="sxs-lookup"><span data-stu-id="6dd27-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="6dd27-298">O proxecto ten tres fitos:</span><span class="sxs-lookup"><span data-stu-id="6dd27-298">The project has three milestones:</span></span>

-   <span data-ttu-id="6dd27-299">Fito 1: Recompilar datos de consumidores - 31 de marzo</span><span class="sxs-lookup"><span data-stu-id="6dd27-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="6dd27-300">Fito 2: Analizar os datos dos consumidores - 30 de abril</span><span class="sxs-lookup"><span data-stu-id="6dd27-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="6dd27-301">Fito 3: Presentar unha proposta de viabilidade do produto - 31 de maio</span><span class="sxs-lookup"><span data-stu-id="6dd27-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="6dd27-302">O cliente acepta pagarlle á súa organización 10 000 polo primeiro fito, 20 000 polo segundo e 20 000 polo terceiro.</span><span class="sxs-lookup"><span data-stu-id="6dd27-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="6dd27-303">Cando configura o contrato do proxecto, acepta facturar ao cliente en función do fito completado.</span><span class="sxs-lookup"><span data-stu-id="6dd27-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="6dd27-304">A configuración da regra de facturación inclúe os seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="6dd27-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="6dd27-305">Definir os fitos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-305">Define the project milestones.</span></span>
-   <span data-ttu-id="6dd27-306">Definir o importe que debe facturar ao cliente cando se complete cada fito.</span><span class="sxs-lookup"><span data-stu-id="6dd27-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="6dd27-307">Cando se completa o primeiro fito o 31 de marzo, vostede marca o fito como rematado e, a seguir, crea unha factura por 10 000 e envíaa ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dd27-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="6dd27-308">Non pode crear unha factura para un fito ata que o marque como finalizado.</span><span class="sxs-lookup"><span data-stu-id="6dd27-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="6dd27-309">Exemplo: Crear unha regra de facturación baseada en servizos máis unha tarifa de xestión</span><span class="sxs-lookup"><span data-stu-id="6dd27-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="6dd27-310">A súa organización, unha empresa de consultoría de xestión, acepta realizar investigacións de mercado para avaliar a viabilidade dun produto que o cliente, unha empresa de venda polo miúdo, está a desenvolver.</span><span class="sxs-lookup"><span data-stu-id="6dd27-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="6dd27-311">Os termos do acordo especifican que proporcionará os servizos dos seus tres principais consultores de xestión, que realizarán a investigación en función do tempo e dos materiais.</span><span class="sxs-lookup"><span data-stu-id="6dd27-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="6dd27-312">O cliente comprométese a pagar 100 por hora, máis unha tarifa de xestión do 10 por cento polas horas de consulta que se cargan ao proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="6dd27-313">Cando configure o contrato do proxecto, cree unha regra de facturación para engadir unha tarifa de xestión do 10 por cento ás horas de consulta que se carguen ao proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="6dd27-314">Cando crea unha factura para o cliente, factúrase ao cliente unha tarifa de xestión do 10 por cento máis o custo das horas de consultoría.</span><span class="sxs-lookup"><span data-stu-id="6dd27-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="6dd27-315">Por exemplo, se os tres consultores traballaron un total de 200 horas no proxecto, créase unha factura por 22 000 baseada no seguinte cálculo:</span><span class="sxs-lookup"><span data-stu-id="6dd27-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="6dd27-316">200 horas a 100 por hora = 20 000</span><span class="sxs-lookup"><span data-stu-id="6dd27-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="6dd27-317">10 por cento de tarifa de xestión = 2 000</span><span class="sxs-lookup"><span data-stu-id="6dd27-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="6dd27-318">Importe total da factura = 22 000</span><span class="sxs-lookup"><span data-stu-id="6dd27-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="6dd27-319">Se as tarifas son tributables para un cliente e vostede selecciona un grupo de impostos sobre as vendas no contrato do proxecto, o grupo de impostos sobre as vendas introdúcese automaticamente nunha regra de facturación para as tarifas.</span><span class="sxs-lookup"><span data-stu-id="6dd27-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="6dd27-320">Exemplo: Crear unha regra de facturación polo valor do tempo e dos materiais</span><span class="sxs-lookup"><span data-stu-id="6dd27-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="6dd27-321">A súa organización, unha empresa de consultoría de software, acepta proporcionar cinco consultores técnicos para traballar nun proxecto de desenvolvemento de software para un cliente durante os próximos seis meses.</span><span class="sxs-lookup"><span data-stu-id="6dd27-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="6dd27-322">O cliente comprométese a pagar 150 por cada hora de consultoría, máis o custo do material de oficina.</span><span class="sxs-lookup"><span data-stu-id="6dd27-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="6dd27-323">A súa organización envía unha factura ao cliente ao final de cada mes.</span><span class="sxs-lookup"><span data-stu-id="6dd27-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="6dd27-324">Cando configura o contrato do proxecto, acepta facturar ao cliente cada mes o tempo e os materiais do proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="6dd27-325">Crea unha regra de facturación que inclúe a seguinte información:</span><span class="sxs-lookup"><span data-stu-id="6dd27-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="6dd27-326">O período do contrato é de seis meses.</span><span class="sxs-lookup"><span data-stu-id="6dd27-326">The contract period is six months.</span></span>
-   <span data-ttu-id="6dd27-327">O tempo de consultoría calcúlase a un prezo de 150 por hora.</span><span class="sxs-lookup"><span data-stu-id="6dd27-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="6dd27-328">O material de oficina factúrase ao custo e o custo total do proxecto non debe superar os 10 000.</span><span class="sxs-lookup"><span data-stu-id="6dd27-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="6dd27-329">Vostede crea unha factura de cliente ao final de cada mes natural durante o proxecto.</span><span class="sxs-lookup"><span data-stu-id="6dd27-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="6dd27-330">Durante o primeiro mes, os consultores do proxecto rexistran un total de 800 horas.</span><span class="sxs-lookup"><span data-stu-id="6dd27-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="6dd27-331">O custo do material de oficina que se carga ao proxecto é de 2.000.</span><span class="sxs-lookup"><span data-stu-id="6dd27-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="6dd27-332">Polo tanto, a finais de mes crea unha factura por 122 000, que se calcula como 800 horas a 150 por hora, máis 2000 para material de oficina.</span><span class="sxs-lookup"><span data-stu-id="6dd27-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]