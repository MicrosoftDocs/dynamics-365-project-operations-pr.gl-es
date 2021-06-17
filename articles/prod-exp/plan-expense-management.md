---
title: Configurar a xestión de gastos
description: Este artigo describe as consideracións e as decisións que debe tomar durante o proceso de planificación antes de configurar a xestión de gastos en Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52538946c7260fad4076a64e8dc34fecf08b90cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005384"
---
# <a name="configure-expense-management"></a><span data-ttu-id="a6db9-103">Configurar a xestión de gastos</span><span class="sxs-lookup"><span data-stu-id="a6db9-103">Configure expense management</span></span>

<span data-ttu-id="a6db9-104">Este tema describe as consideracións e as decisións que debe tomar durante o proceso de planificación antes de configurar a xestión de gastos.</span><span class="sxs-lookup"><span data-stu-id="a6db9-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="a6db9-105">Na xestión de gastos, pode almacenar información sobre métodos de pago, solicitudes de viaxes, informes de gastos, políticas, etc.</span><span class="sxs-lookup"><span data-stu-id="a6db9-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="a6db9-106">Debido a que moitas das decisións que toma cando planifica a súa configuración para a xestión de gastos baséanse na xerarquía e na estrutura financeira da súa organización, debe consultar os documentos de planificación desas áreas.</span><span class="sxs-lookup"><span data-stu-id="a6db9-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="a6db9-107">Gastos entre empresas</span><span class="sxs-lookup"><span data-stu-id="a6db9-107">Intercompany expenses</span></span>

<span data-ttu-id="a6db9-108">Cando activa os gastos entre empresas, permite que as entidades legais e os empregados incorran en gastos por conta doutra entidade legal e cobren o pagamento da entidade legal de emprego dentro da súa organización.</span><span class="sxs-lookup"><span data-stu-id="a6db9-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="a6db9-109">Por exemplo, un empregado da entidade legal A completa un proxecto para a entidade legal B e o proxecto supón gastos relacionados con viaxes.</span><span class="sxs-lookup"><span data-stu-id="a6db9-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="a6db9-110">Se se activan os gastos entre empresas, o empregado pode presentar un informe de gastos que contabilizará o gasto na entidade legal B e os gastos deberán ser pagados pola entidade legal A. Se a súa organización non ten varias entidades legais, non o fará. Non ten que activar os gastos entre empresas.</span><span class="sxs-lookup"><span data-stu-id="a6db9-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="a6db9-111">**Decisión:** Quere activar os gastos entre empresas?</span><span class="sxs-lookup"><span data-stu-id="a6db9-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="a6db9-112">Xestión financeira</span><span class="sxs-lookup"><span data-stu-id="a6db9-112">Financial management</span></span>

<span data-ttu-id="a6db9-113">A xestión dos gastos está moi integrada coa xestión financeira da súa organización.</span><span class="sxs-lookup"><span data-stu-id="a6db9-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="a6db9-114">Moita da súa configuración para a xestión de gastos basearase nas decisións que tomou sobre as finanzas da súa organización.</span><span class="sxs-lookup"><span data-stu-id="a6db9-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="a6db9-115">As seguintes seccións describen as distintas áreas que requiren planificación e decisións, en función das decisións financeiras da súa organización e das orientacións do seu equipo directivo.</span><span class="sxs-lookup"><span data-stu-id="a6db9-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="a6db9-116">Dietas</span><span class="sxs-lookup"><span data-stu-id="a6db9-116">Per diems</span></span>

<span data-ttu-id="a6db9-117">Debe definir as dietas dos empregados que proporciona a súa organización.</span><span class="sxs-lookup"><span data-stu-id="a6db9-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="a6db9-118">Debido a que os dietas adoitan empregarse para cubrir gastos como comidas, aloxamento e outros gastos incidentais, pode crear regras para as dietas que ofrece a súa organización.</span><span class="sxs-lookup"><span data-stu-id="a6db9-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="a6db9-119">As taxas das dietas poden basearse na época do ano, na localización da viaxe ou en ambas.</span><span class="sxs-lookup"><span data-stu-id="a6db9-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="a6db9-120">Cando define unha regra de dietas, pode especificar que se reterá unha porcentaxe da taxa de dietas se un traballador recibe comidas ou servizos de cortesía.</span><span class="sxs-lookup"><span data-stu-id="a6db9-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="a6db9-121">Tamén pode definir os niveis de dietas para establecer un número mínimo e máximo de horas que a taxa de dietas se poden aplicar ás viaxes dun traballador.</span><span class="sxs-lookup"><span data-stu-id="a6db9-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="a6db9-122">**Decisións:**</span><span class="sxs-lookup"><span data-stu-id="a6db9-122">**Decisions:**</span></span>

- <span data-ttu-id="a6db9-123">Regras de dietas predefinidas para os primeiros e últimos días:</span><span class="sxs-lookup"><span data-stu-id="a6db9-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="a6db9-124">Cal é o número mínimo de horas que pode solicitar un empregado por día e aínda así recibir unha dieta?</span><span class="sxs-lookup"><span data-stu-id="a6db9-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="a6db9-125">Redúcese a cantidade que se ofrece para as comidas do primeiro día e do último día?</span><span class="sxs-lookup"><span data-stu-id="a6db9-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="a6db9-126">Se hai unha redución, cal é a porcentaxe da redución?</span><span class="sxs-lookup"><span data-stu-id="a6db9-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="a6db9-127">Redúcese a cantidade que se ofrece para o hotel do primeiro día e do último día?</span><span class="sxs-lookup"><span data-stu-id="a6db9-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="a6db9-128">Se hai unha redución, cal é a porcentaxe da redución?</span><span class="sxs-lookup"><span data-stu-id="a6db9-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="a6db9-129">Redúcese a cantidade que se ofrece para outros gastos no que se incorre o primeiro día e do último día?</span><span class="sxs-lookup"><span data-stu-id="a6db9-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="a6db9-130">Se hai unha redución, cal é a porcentaxe da redución?</span><span class="sxs-lookup"><span data-stu-id="a6db9-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="a6db9-131">Regras de dietas predefinidas:</span><span class="sxs-lookup"><span data-stu-id="a6db9-131">Default per diem rules:</span></span>

    - <span data-ttu-id="a6db9-132">Hai unha redución porcentual do subsidio de dietas para cada comida se, por exemplo, a comida é gratuíta?</span><span class="sxs-lookup"><span data-stu-id="a6db9-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="a6db9-133">Se hai unha redución, cal é a porcentaxe da redución por cada comida?</span><span class="sxs-lookup"><span data-stu-id="a6db9-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="a6db9-134">Calcúlase a redución das comidas por día, por viaxe ou polo número de comidas ao día?</span><span class="sxs-lookup"><span data-stu-id="a6db9-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="a6db9-135">Deberían redondearse as cantidades de dieta de xeito regular ou redondealas?</span><span class="sxs-lookup"><span data-stu-id="a6db9-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="a6db9-136">Calcúlanse as dietas nun período de 24 horas ou nun día natural?</span><span class="sxs-lookup"><span data-stu-id="a6db9-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="a6db9-137">Regras de dietas baseadas na localización:</span><span class="sxs-lookup"><span data-stu-id="a6db9-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="a6db9-138">As taxas de dietas varían segundo a localización?</span><span class="sxs-lookup"><span data-stu-id="a6db9-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="a6db9-139">Que localizacións se inclúen?</span><span class="sxs-lookup"><span data-stu-id="a6db9-139">What locations are included?</span></span>
    - <span data-ttu-id="a6db9-140">Se as taxas de dietas varían segundo a localización, para cada localización, que cantidade porcentual se proporciona para os seguintes tipos de gastos:</span><span class="sxs-lookup"><span data-stu-id="a6db9-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="a6db9-141">Comidas</span><span class="sxs-lookup"><span data-stu-id="a6db9-141">Meals</span></span>
        - <span data-ttu-id="a6db9-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="a6db9-142">Hotel</span></span>
        - <span data-ttu-id="a6db9-143">Outros gastos</span><span class="sxs-lookup"><span data-stu-id="a6db9-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="a6db9-144">Diarios e contas de xestión de gastos</span><span class="sxs-lookup"><span data-stu-id="a6db9-144">Expense management journals and accounts</span></span>

<span data-ttu-id="a6db9-145">A xestión de gastos require que utilice varios diarios e contas.</span><span class="sxs-lookup"><span data-stu-id="a6db9-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="a6db9-146">Debe decidir, por exemplo, se a mesma conta se usa para adiantos de efectivo e disputas de tarxetas de crédito.</span><span class="sxs-lookup"><span data-stu-id="a6db9-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="a6db9-147">**Decisións:**</span><span class="sxs-lookup"><span data-stu-id="a6db9-147">**Decisions:**</span></span>

- <span data-ttu-id="a6db9-148">En que diario de libro maior se contabilizan os informes de gastos aprobados?</span><span class="sxs-lookup"><span data-stu-id="a6db9-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="a6db9-149">Que conta se usa para adiantos de efectivo?</span><span class="sxs-lookup"><span data-stu-id="a6db9-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="a6db9-150">Os adiantos efectivo deberían contabilizarse inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="a6db9-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="a6db9-151">Métodos de pagamento</span><span class="sxs-lookup"><span data-stu-id="a6db9-151">Payment methods</span></span>

<span data-ttu-id="a6db9-152">Cando permite aos empregados incorrer en gastos en nome da súa empresa, debe definir os métodos de pagamento que os empregados teñen permiso para usar.</span><span class="sxs-lookup"><span data-stu-id="a6db9-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="a6db9-153">Por exemplo, pode permitir que os empregados utilicen efectivo ou unha tarxeta de crédito corporativa.</span><span class="sxs-lookup"><span data-stu-id="a6db9-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="a6db9-154">Tamén pode permitir que os empregados utilicen tarxetas de crédito persoais e logo reembolsarlles aos empregados.</span><span class="sxs-lookup"><span data-stu-id="a6db9-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="a6db9-155">Debe tomar as seguintes decisións para cada método de pagamento que permita.</span><span class="sxs-lookup"><span data-stu-id="a6db9-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="a6db9-156">**Decisións:**</span><span class="sxs-lookup"><span data-stu-id="a6db9-156">**Decisions:**</span></span>

- <span data-ttu-id="a6db9-157">Que métodos de pagamento están permitidos?</span><span class="sxs-lookup"><span data-stu-id="a6db9-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="a6db9-158">Quen é o responsable dos gastos do método de pagamento?</span><span class="sxs-lookup"><span data-stu-id="a6db9-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="a6db9-159">Hai algún tipo de conta compensada?</span><span class="sxs-lookup"><span data-stu-id="a6db9-159">Is there an offset account type?</span></span> <span data-ttu-id="a6db9-160">Se hai un tipo de conta compensada, cal é?</span><span class="sxs-lookup"><span data-stu-id="a6db9-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="a6db9-161">Se hai un tipo de conta compensada, cal é a conta?</span><span class="sxs-lookup"><span data-stu-id="a6db9-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="a6db9-162">Se o método de pagamento é unha tarxeta de crédito, debería empregarse só coas transaccións importadas?</span><span class="sxs-lookup"><span data-stu-id="a6db9-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="a6db9-163">Categorías de gasto e categorías compartidas</span><span class="sxs-lookup"><span data-stu-id="a6db9-163">Expense categories and shared categories</span></span>

<span data-ttu-id="a6db9-164">Cando os empregados crean un informe de gastos, cada gasto que rexistran debe asociarse a unha categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="a6db9-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="a6db9-165">As categorías de gastos derivan de categorías compartidas que se poden compartir entre as entidades legais da súa organización.</span><span class="sxs-lookup"><span data-stu-id="a6db9-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="a6db9-166">Estas categorías tamén se poden compartirse na xestión e contabilidade de proxectos, dependendo da forma na que se defina a súa organización.</span><span class="sxs-lookup"><span data-stu-id="a6db9-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="a6db9-167">En función da definición da súa organización e das orientacións do equipo de implementación, debe determinar se as categorías que se usan na xestión de gastos só se usarán na xestión de gastos ou se deben compartise entre a xestión e contabilidade de proxectos e a xestión de gastos.</span><span class="sxs-lookup"><span data-stu-id="a6db9-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="a6db9-168">Teña en conta que estas categorías pódense compartir entre Proxecto e Gasto ou Proxecto e Produción, pero non entre Gasto e Produción.</span><span class="sxs-lookup"><span data-stu-id="a6db9-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="a6db9-169">Debe tomar as seguintes decisións para cada categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="a6db9-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="a6db9-170">**Decisións:**</span><span class="sxs-lookup"><span data-stu-id="a6db9-170">**Decisions:**</span></span>

- <span data-ttu-id="a6db9-171">Que é a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-171">What is the expense category?</span></span> <span data-ttu-id="a6db9-172">Entre os exemplos inclúense as categorías de voos, hotel ou quilometraxe.</span><span class="sxs-lookup"><span data-stu-id="a6db9-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="a6db9-173">A categoría de gasto tamén se pode usar na xestión e contabilidade de proxectos?</span><span class="sxs-lookup"><span data-stu-id="a6db9-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="a6db9-174">Que é o tipo de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-174">What is the expense type?</span></span>
- <span data-ttu-id="a6db9-175">Cal é o método de pagamento predefinido para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="a6db9-176">Hai que detallar os gastos da categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="a6db9-177">Cal é a principal conta predefinida para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="a6db9-178">Cal é o grupo predeterminado do imposto sobre as vendas para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="a6db9-179">Permítense métodos adicionais de pagamento para a categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="a6db9-180">Se se permiten métodos adicionais de pagamento, cales son?</span><span class="sxs-lookup"><span data-stu-id="a6db9-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="a6db9-181">Hai subcategorías nesta categoría de gasto?</span><span class="sxs-lookup"><span data-stu-id="a6db9-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="a6db9-182">Se hai subcategorías, tamén debe tomar as seguintes decisións:</span><span class="sxs-lookup"><span data-stu-id="a6db9-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="a6db9-183">Está excluída algunha das subcategorías da recuperación de impostos?</span><span class="sxs-lookup"><span data-stu-id="a6db9-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="a6db9-184">Cal é o grupo do imposto sobre as vendas das subcategorías?</span><span class="sxs-lookup"><span data-stu-id="a6db9-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="a6db9-185">Se a categoría de gasto tamén se usa na xestión e contabilidade de proxectos, responda ás preguntas restantes.</span><span class="sxs-lookup"><span data-stu-id="a6db9-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="a6db9-186">Se non, vaia á seguinte sección.</span><span class="sxs-lookup"><span data-stu-id="a6db9-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="a6db9-187">Que contas de custos se utilizarán para os seguintes gastos?</span><span class="sxs-lookup"><span data-stu-id="a6db9-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="a6db9-188">Custo</span><span class="sxs-lookup"><span data-stu-id="a6db9-188">Cost</span></span>
    - <span data-ttu-id="a6db9-189">Asignación de nóminas</span><span class="sxs-lookup"><span data-stu-id="a6db9-189">Payroll allocation</span></span>
    - <span data-ttu-id="a6db9-190">WIP-valor de custo</span><span class="sxs-lookup"><span data-stu-id="a6db9-190">WIP-cost value</span></span>
    - <span data-ttu-id="a6db9-191">Elemento de custo</span><span class="sxs-lookup"><span data-stu-id="a6db9-191">Cost-item</span></span>
    - <span data-ttu-id="a6db9-192">WIP-elemento de valor de custo</span><span class="sxs-lookup"><span data-stu-id="a6db9-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="a6db9-193">Perda acumulada</span><span class="sxs-lookup"><span data-stu-id="a6db9-193">Accrued loss</span></span>
    - <span data-ttu-id="a6db9-194">WIP-perda acumulada</span><span class="sxs-lookup"><span data-stu-id="a6db9-194">WIP-accrued loss</span></span>

- <span data-ttu-id="a6db9-195">Que contas de ingresos se utilizarán para o seguinte?</span><span class="sxs-lookup"><span data-stu-id="a6db9-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="a6db9-196">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="a6db9-196">Invoiced revenue</span></span>
    - <span data-ttu-id="a6db9-197">Ingresos acumulados-valor de vendas</span><span class="sxs-lookup"><span data-stu-id="a6db9-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="a6db9-198">WIP-valor de vendas</span><span class="sxs-lookup"><span data-stu-id="a6db9-198">WIP-sales value</span></span>
    - <span data-ttu-id="a6db9-199">Ingresos acumulados-produción</span><span class="sxs-lookup"><span data-stu-id="a6db9-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="a6db9-200">WIP-produción</span><span class="sxs-lookup"><span data-stu-id="a6db9-200">WIP-production</span></span>
    - <span data-ttu-id="a6db9-201">Ingresos acumulados-beneficio</span><span class="sxs-lookup"><span data-stu-id="a6db9-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="a6db9-202">WIP-beneficio</span><span class="sxs-lookup"><span data-stu-id="a6db9-202">WIP-profit</span></span>
    - <span data-ttu-id="a6db9-203">Ingresos acumulados-subscrición</span><span class="sxs-lookup"><span data-stu-id="a6db9-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="a6db9-204">WIP-subscrición</span><span class="sxs-lookup"><span data-stu-id="a6db9-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="a6db9-205">Impostos</span><span class="sxs-lookup"><span data-stu-id="a6db9-205">Taxes</span></span>

<span data-ttu-id="a6db9-206">Para os impostos relacionados cos gastos, debe determinar o que está incluído ou activado nos informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="a6db9-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="a6db9-207">**Decisións:**</span><span class="sxs-lookup"><span data-stu-id="a6db9-207">**Decisions:**</span></span>

- <span data-ttu-id="a6db9-208">O imposto sobre as vendas está incluído nos importes dos gastos?</span><span class="sxs-lookup"><span data-stu-id="a6db9-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="a6db9-209">Debería activarse a recuperación de impostos sobre os gastos?</span><span class="sxs-lookup"><span data-stu-id="a6db9-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="a6db9-210">Cando planificaba o libro maior, se decidiu aplicar o imposto sobre as vendas dos Estados Unidos e usar as regras fiscais, non pode activar a recuperación de impostos sobre os gastos.</span><span class="sxs-lookup"><span data-stu-id="a6db9-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="a6db9-211">(Para aplicar as regras de impostos sobre vendas dos Estados Unidos e usar as regras fiscais, configure a opción **Aplicar regras de impostos sobre as vendas** en **Si**.)</span><span class="sxs-lookup"><span data-stu-id="a6db9-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="a6db9-212">Políticas</span><span class="sxs-lookup"><span data-stu-id="a6db9-212">Policies</span></span>

<span data-ttu-id="a6db9-213">Ao crear políticas de informes de gastos, pode axudar á súa organización a aforrar tempo e diñeiro cando os empregados incorran en gastos no seu nome.</span><span class="sxs-lookup"><span data-stu-id="a6db9-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="a6db9-214">As políticas axudan a garantir que os empregados permanecen dentro do orzamento, proporcionan toda a información requirida e gastan cartos só cando o necesiten.</span><span class="sxs-lookup"><span data-stu-id="a6db9-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="a6db9-215">Debe tomar as seguintes decisións para cada política de informe de gastos e cada política de aprobación de informe de gastos que cree.</span><span class="sxs-lookup"><span data-stu-id="a6db9-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="a6db9-216">**Decisións:**</span><span class="sxs-lookup"><span data-stu-id="a6db9-216">**Decisions:**</span></span>

- <span data-ttu-id="a6db9-217">Cal é o nome da política?</span><span class="sxs-lookup"><span data-stu-id="a6db9-217">What is the name of the policy?</span></span>
- <span data-ttu-id="a6db9-218">Para que serve a política de gastos?</span><span class="sxs-lookup"><span data-stu-id="a6db9-218">What is the expense policy for?</span></span>
- <span data-ttu-id="a6db9-219">Se anteriormente decidiu activar os gastos entre empresas, a que empresas da súa organización se aplicará esta política?</span><span class="sxs-lookup"><span data-stu-id="a6db9-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="a6db9-220">Cando entra en vigor a política?</span><span class="sxs-lookup"><span data-stu-id="a6db9-220">When does the policy become effective?</span></span>
- <span data-ttu-id="a6db9-221">Cando caduca a política?</span><span class="sxs-lookup"><span data-stu-id="a6db9-221">When does the policy expire?</span></span>
- <span data-ttu-id="a6db9-222">Cal é a regra da política?</span><span class="sxs-lookup"><span data-stu-id="a6db9-222">What is the policy rule?</span></span>
- <span data-ttu-id="a6db9-223">Cal é o resultado da regra da política?</span><span class="sxs-lookup"><span data-stu-id="a6db9-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]