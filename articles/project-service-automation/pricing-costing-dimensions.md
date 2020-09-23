---
title: Páxina de inicio de dimensións de prezos e custos
description: Este tema ofrece unha visión xeral das dimensións dos prezos.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751367"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="143c0-103">Páxina de inicio de dimensións de prezos e custos</span><span class="sxs-lookup"><span data-stu-id="143c0-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="143c0-104">As dimensións que se usan en recursos humanos para configurar prezos e custos inclúense en dúas categorías:</span><span class="sxs-lookup"><span data-stu-id="143c0-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="143c0-105">Persoas</span><span class="sxs-lookup"><span data-stu-id="143c0-105">People</span></span>
- <span data-ttu-id="143c0-106">Traballo planificado</span><span class="sxs-lookup"><span data-stu-id="143c0-106">Planned work</span></span>

<span data-ttu-id="143c0-107">Por iso, hai dous tipos de valores de dimensión de prezos dispoñibles en Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="143c0-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="143c0-108">**Conxuntos de opcións** - Dimensións que son enumeracións fixas para un conxunto de valores.</span><span class="sxs-lookup"><span data-stu-id="143c0-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="143c0-109">**Valores baseados en entidades** - Dimensións que poden ser un conxunto variado de valores.</span><span class="sxs-lookup"><span data-stu-id="143c0-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="143c0-110">Dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="143c0-110">Pricing dimensions</span></span>

<span data-ttu-id="143c0-111">PSA envíase cun conxunto predefinido de dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="143c0-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="143c0-112">Podes velas indo a **Project Service** > **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="143c0-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="143c0-113">No rexistro de parámetros, no separador **Dimensións de prezos baseados na cantidade**, verifique que o rol, **msdyn_resourcecategory**, e a unidade organizativa de recursos, **msdyn_organizationalunit** teñan os campos **Aplicable a vendas** e **Aplicable a custo** establecidos en **Si**.</span><span class="sxs-lookup"><span data-stu-id="143c0-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="143c0-114">Isto permitirá establecer o prezo e o custo para cada combinación de roles e unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="143c0-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de pantalla dos parámetros de Project Service con "Aplicable a vendas" resaltado](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="143c0-116">Se estivo a usar os campos listos para usar de rol e unidade organizativa como dimensións de prezos antes da versión 3 de PSA, non haberá ningún cambio observable.</span><span class="sxs-lookup"><span data-stu-id="143c0-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="143c0-117">Pode seguir usando o Project Service como sempre.</span><span class="sxs-lookup"><span data-stu-id="143c0-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="143c0-118">Se precisa un prezo ou custo para os seus recursos usando atributos adicionais, pode crear campos, entidades e dimensións personalizados.</span><span class="sxs-lookup"><span data-stu-id="143c0-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="143c0-119">Para obter máis información, consulte os temas seguintes, pero teña en conta que debe completar os procedementos na orde que aparece a continuación:</span><span class="sxs-lookup"><span data-stu-id="143c0-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="143c0-120">Crear campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="143c0-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="143c0-121">Engadir campos personalizados a configuración de prezos e entidades transaccionais</span><span class="sxs-lookup"><span data-stu-id="143c0-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="143c0-122">Configurar campos personalizados como dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="143c0-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="143c0-123">Actualizar os atributos do complemento para incluír novas dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="143c0-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="143c0-124">Prezos do tempo de recursos humanos</span><span class="sxs-lookup"><span data-stu-id="143c0-124">Pricing human resource time</span></span>
<span data-ttu-id="143c0-125">Como unha organización valora o tempo dos recursos humanos é moitas veces unha consideración estratéxica importante que afecta directamente á rendibilidade da organización.</span><span class="sxs-lookup"><span data-stu-id="143c0-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="143c0-126">Traballe cos equipos financeiros e os responsables de prácticas cando a súa organización estea preparada para identificar como quere configurar os tipos de factura e custos para o tempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="143c0-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="143c0-127">Outras consideracións para fixar os prezos inclúen se hai que volver usar campos ou entidades que actualmente non teñen dimensións de prezos pero que se aplican como dimensión de prezos para a súa organización.</span><span class="sxs-lookup"><span data-stu-id="143c0-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="143c0-128">Campos como **Categoría de transacción** (**msdyn_transactioncategory**) e **Recurso reservable** ( **bookableresource**) son exemplos de dimensións do candidato.</span><span class="sxs-lookup"><span data-stu-id="143c0-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="143c0-129">Tamén debe considerar se a súa dimensión de prezos debe ser unha táboa ou un conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="143c0-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="143c0-130">Se prevé cambios nos valores dunha dimensión que serán máis de 10 ou 12 e necesita atributos adicionais nestes valores, pode crear unha entidade en lugar dun conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="143c0-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="143c0-131">Manter un conxunto de opcións, como engadir ou eliminar valores, require un administrador ou programador, mentres que a adición de novas filas a unha táboa pode facelo a maioría dos usuarios.</span><span class="sxs-lookup"><span data-stu-id="143c0-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="143c0-132">O seguinte exemplo mostra os tipos de facturación que se configuran en función do rol e da unidade organizativa de recursos á que pertenza o recurso.</span><span class="sxs-lookup"><span data-stu-id="143c0-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="143c0-133">As taxas de custo baséanse normalmente na banda salarial do empregado e a unidade organizativa á que pertenza.</span><span class="sxs-lookup"><span data-stu-id="143c0-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="143c0-134">Neste exemplo, as táboas de taxa de facturación e taxa de custo terán o seguinte aspecto.</span><span class="sxs-lookup"><span data-stu-id="143c0-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="143c0-135">**Exemplo de taxas de facturación**</span><span class="sxs-lookup"><span data-stu-id="143c0-135">**Sample bill rates**</span></span>

| <span data-ttu-id="143c0-136">Rol</span><span class="sxs-lookup"><span data-stu-id="143c0-136">Role</span></span>        | <span data-ttu-id="143c0-137">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="143c0-137">Org Unit</span></span>    |<span data-ttu-id="143c0-138">Unidade</span><span class="sxs-lookup"><span data-stu-id="143c0-138">Unit</span></span>      |<span data-ttu-id="143c0-139">Prezo</span><span class="sxs-lookup"><span data-stu-id="143c0-139">Price</span></span>      |<span data-ttu-id="143c0-140">Moeda</span><span class="sxs-lookup"><span data-stu-id="143c0-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="143c0-141">Programador</span><span class="sxs-lookup"><span data-stu-id="143c0-141">Developer</span></span>   | <span data-ttu-id="143c0-142">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="143c0-142">Contoso US</span></span>  |<span data-ttu-id="143c0-143">Hour</span><span class="sxs-lookup"><span data-stu-id="143c0-143">Hour</span></span> | <span data-ttu-id="143c0-144">200</span><span class="sxs-lookup"><span data-stu-id="143c0-144">200</span></span>|<span data-ttu-id="143c0-145">USD</span><span class="sxs-lookup"><span data-stu-id="143c0-145">USD</span></span>     |
| <span data-ttu-id="143c0-146">Programador</span><span class="sxs-lookup"><span data-stu-id="143c0-146">Developer</span></span>   | <span data-ttu-id="143c0-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="143c0-147">Contoso India</span></span> |<span data-ttu-id="143c0-148">Hour</span><span class="sxs-lookup"><span data-stu-id="143c0-148">Hour</span></span>|   <span data-ttu-id="143c0-149">112</span><span class="sxs-lookup"><span data-stu-id="143c0-149">112</span></span>|<span data-ttu-id="143c0-150">USD</span><span class="sxs-lookup"><span data-stu-id="143c0-150">USD</span></span>     |


<span data-ttu-id="143c0-151">**Exempo de taxas de custo**</span><span class="sxs-lookup"><span data-stu-id="143c0-151">**Sample cost rates**</span></span>

| <span data-ttu-id="143c0-152">Banda salarial</span><span class="sxs-lookup"><span data-stu-id="143c0-152">Salary Band</span></span>     | <span data-ttu-id="143c0-153">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="143c0-153">Org Unit</span></span>    |<span data-ttu-id="143c0-154">Unidade</span><span class="sxs-lookup"><span data-stu-id="143c0-154">Unit</span></span>      |<span data-ttu-id="143c0-155">Prezo</span><span class="sxs-lookup"><span data-stu-id="143c0-155">Price</span></span>      |<span data-ttu-id="143c0-156">Moeda</span><span class="sxs-lookup"><span data-stu-id="143c0-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="143c0-157">A miña empresa_Banda1</span><span class="sxs-lookup"><span data-stu-id="143c0-157">My company_Band1</span></span> | <span data-ttu-id="143c0-158">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="143c0-158">Contoso US</span></span>  |<span data-ttu-id="143c0-159">Hour</span><span class="sxs-lookup"><span data-stu-id="143c0-159">Hour</span></span> | <span data-ttu-id="143c0-160">145</span><span class="sxs-lookup"><span data-stu-id="143c0-160">145</span></span>|<span data-ttu-id="143c0-161">USD</span><span class="sxs-lookup"><span data-stu-id="143c0-161">USD</span></span>     |
| <span data-ttu-id="143c0-162">A miña empresa_Banda2</span><span class="sxs-lookup"><span data-stu-id="143c0-162">My company_Band2</span></span> | <span data-ttu-id="143c0-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="143c0-163">Contoso India</span></span> |<span data-ttu-id="143c0-164">Hour</span><span class="sxs-lookup"><span data-stu-id="143c0-164">Hour</span></span>|   <span data-ttu-id="143c0-165">67</span><span class="sxs-lookup"><span data-stu-id="143c0-165">67</span></span>|<span data-ttu-id="143c0-166">USD</span><span class="sxs-lookup"><span data-stu-id="143c0-166">USD</span></span>     |
