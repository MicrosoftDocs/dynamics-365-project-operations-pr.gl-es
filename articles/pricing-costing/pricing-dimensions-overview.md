---
title: Visión xeral das dimensións de prezos
description: Este tema fornece información sobre as dimensións de prezos en Dynamics 365 Project Operations.
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128461"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="5ed06-103">Visión xeral das dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="5ed06-103">Pricing dimensions overview</span></span>

<span data-ttu-id="5ed06-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="5ed06-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5ed06-105">As dimensións que se usan en recursos humanos para configurar prezos e custos inclúense en dúas categorías:</span><span class="sxs-lookup"><span data-stu-id="5ed06-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="5ed06-106">Persoas</span><span class="sxs-lookup"><span data-stu-id="5ed06-106">People</span></span>
- <span data-ttu-id="5ed06-107">Traballo planificado</span><span class="sxs-lookup"><span data-stu-id="5ed06-107">Planned work</span></span>

<span data-ttu-id="5ed06-108">Por iso, hai dous tipos de valores de dimensión de prezos dispoñibles:</span><span class="sxs-lookup"><span data-stu-id="5ed06-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="5ed06-109">**Conxuntos de opcións**: Dimensións que son enumeracións fixas para un conxunto de valores.</span><span class="sxs-lookup"><span data-stu-id="5ed06-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="5ed06-110">**Valores baseados en entidades**: Dimensións que poden ser un conxunto variado de valores.</span><span class="sxs-lookup"><span data-stu-id="5ed06-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="5ed06-111">Dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="5ed06-111">Pricing dimensions</span></span>

<span data-ttu-id="5ed06-112">Dynamics 365 Project Operations inclúese cun conxunto predefinido de dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="5ed06-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="5ed06-113">Pode ver estas dimensións de prezos indo a **Project Operations** > **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5ed06-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="5ed06-114">No rexistro de parámetros, no separador **Dimensións de prezos baseados na cantidade**, verifique que o rol, **msdyn_resourcecategory**, e a unidade organizativa de recursos, **msdyn_organizationalunit** teñan os campos **Aplicable a vendas** e **Aplicable a custo** establecidos en **Si**.</span><span class="sxs-lookup"><span data-stu-id="5ed06-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="5ed06-115">Con estes campos activados, pode establecer o prezo e o custo para cada combinación de roles e unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="5ed06-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="5ed06-116">Se precisa un prezo ou custo para os seus recursos usando atributos adicionais, pode crear campos, entidades e dimensións personalizados.</span><span class="sxs-lookup"><span data-stu-id="5ed06-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="5ed06-117">Prezos do tempo de recursos humanos</span><span class="sxs-lookup"><span data-stu-id="5ed06-117">Pricing human resource time</span></span>
<span data-ttu-id="5ed06-118">Como unha organización valora o tempo dos recursos humanos é moitas veces unha consideración estratéxica importante que afecta directamente á rendibilidade da organización.</span><span class="sxs-lookup"><span data-stu-id="5ed06-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="5ed06-119">Traballe cos equipos financeiros e os responsables de prácticas cando a súa organización estea preparada para identificar como quere configurar os tipos de factura e custos para o tempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="5ed06-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="5ed06-120">Outras consideracións para fixar os prezos inclúen se hai que volver usar campos ou entidades que actualmente non teñen dimensións de prezos pero que se aplican como dimensión de prezos para a súa organización.</span><span class="sxs-lookup"><span data-stu-id="5ed06-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="5ed06-121">Campos como **Categoría de transacción** (**msdyn_transactioncategory**) e **Recurso reservable** ( **bookableresource**) son exemplos de dimensións do candidato.</span><span class="sxs-lookup"><span data-stu-id="5ed06-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="5ed06-122">Considere se a súa dimensión de prezos debe ser unha táboa ou un conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="5ed06-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="5ed06-123">Se prevé cambios nos valores dunha dimensión que serán máis de 10 ou 12 e necesita atributos adicionais nestes valores, pode crear unha entidade en lugar dun conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="5ed06-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="5ed06-124">Manter un conxunto de opcións, como engadir ou eliminar valores, require un administrador ou programador, mentres que a adición de novas filas a unha táboa pode facelo a maioría dos usuarios.</span><span class="sxs-lookup"><span data-stu-id="5ed06-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="5ed06-125">O seguinte exemplo mostra os tipos de facturación que se configuran en función do rol e da unidade organizativa de recursos á que pertenza o recurso.</span><span class="sxs-lookup"><span data-stu-id="5ed06-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="5ed06-126">As taxas de custo baséanse normalmente na banda salarial do empregado e a unidade organizativa á que pertenza.</span><span class="sxs-lookup"><span data-stu-id="5ed06-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="5ed06-127">Neste exemplo, as táboas de taxa de facturación e taxa de custo terán o seguinte aspecto.</span><span class="sxs-lookup"><span data-stu-id="5ed06-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="5ed06-128">**Exemplo de taxas de facturación**</span><span class="sxs-lookup"><span data-stu-id="5ed06-128">**Sample bill rates**</span></span>

| <span data-ttu-id="5ed06-129">Rol</span><span class="sxs-lookup"><span data-stu-id="5ed06-129">Role</span></span>        | <span data-ttu-id="5ed06-130">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="5ed06-130">Org Unit</span></span>    |<span data-ttu-id="5ed06-131">Unidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-131">Unit</span></span>      |<span data-ttu-id="5ed06-132">Prezo</span><span class="sxs-lookup"><span data-stu-id="5ed06-132">Price</span></span>      |<span data-ttu-id="5ed06-133">Moeda</span><span class="sxs-lookup"><span data-stu-id="5ed06-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5ed06-134">Programador</span><span class="sxs-lookup"><span data-stu-id="5ed06-134">Developer</span></span>   | <span data-ttu-id="5ed06-135">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="5ed06-135">Contoso US</span></span>  |<span data-ttu-id="5ed06-136">Hour</span><span class="sxs-lookup"><span data-stu-id="5ed06-136">Hour</span></span> | <span data-ttu-id="5ed06-137">200</span><span class="sxs-lookup"><span data-stu-id="5ed06-137">200</span></span>|<span data-ttu-id="5ed06-138">USD</span><span class="sxs-lookup"><span data-stu-id="5ed06-138">USD</span></span>     |
| <span data-ttu-id="5ed06-139">Programador</span><span class="sxs-lookup"><span data-stu-id="5ed06-139">Developer</span></span>   | <span data-ttu-id="5ed06-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="5ed06-140">Contoso India</span></span> |<span data-ttu-id="5ed06-141">Hour</span><span class="sxs-lookup"><span data-stu-id="5ed06-141">Hour</span></span>|   <span data-ttu-id="5ed06-142">112</span><span class="sxs-lookup"><span data-stu-id="5ed06-142">112</span></span>|<span data-ttu-id="5ed06-143">USD</span><span class="sxs-lookup"><span data-stu-id="5ed06-143">USD</span></span>     |


<span data-ttu-id="5ed06-144">**Exempo de taxas de custo**</span><span class="sxs-lookup"><span data-stu-id="5ed06-144">**Sample cost rates**</span></span>

| <span data-ttu-id="5ed06-145">Banda salarial</span><span class="sxs-lookup"><span data-stu-id="5ed06-145">Salary Band</span></span>     | <span data-ttu-id="5ed06-146">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="5ed06-146">Org Unit</span></span>    |<span data-ttu-id="5ed06-147">Unidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-147">Unit</span></span>      |<span data-ttu-id="5ed06-148">Prezo</span><span class="sxs-lookup"><span data-stu-id="5ed06-148">Price</span></span>      |<span data-ttu-id="5ed06-149">Moeda</span><span class="sxs-lookup"><span data-stu-id="5ed06-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5ed06-150">A miña empresa_Banda1</span><span class="sxs-lookup"><span data-stu-id="5ed06-150">My company_Band1</span></span> | <span data-ttu-id="5ed06-151">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="5ed06-151">Contoso US</span></span>  |<span data-ttu-id="5ed06-152">Hour</span><span class="sxs-lookup"><span data-stu-id="5ed06-152">Hour</span></span> | <span data-ttu-id="5ed06-153">145</span><span class="sxs-lookup"><span data-stu-id="5ed06-153">145</span></span>|<span data-ttu-id="5ed06-154">USD</span><span class="sxs-lookup"><span data-stu-id="5ed06-154">USD</span></span>     |
| <span data-ttu-id="5ed06-155">A miña empresa_Banda2</span><span class="sxs-lookup"><span data-stu-id="5ed06-155">My company_Band2</span></span> | <span data-ttu-id="5ed06-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="5ed06-156">Contoso India</span></span> |<span data-ttu-id="5ed06-157">Hour</span><span class="sxs-lookup"><span data-stu-id="5ed06-157">Hour</span></span>|   <span data-ttu-id="5ed06-158">67</span><span class="sxs-lookup"><span data-stu-id="5ed06-158">67</span></span>|<span data-ttu-id="5ed06-159">USD</span><span class="sxs-lookup"><span data-stu-id="5ed06-159">USD</span></span>     |
