---
title: Páxina de inicio de dimensións de prezos e custos
description: Este tema ofrece unha visión xeral das dimensións dos prezos.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368879"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="78c77-103">Páxina de inicio de dimensións de prezos e custos</span><span class="sxs-lookup"><span data-stu-id="78c77-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="78c77-104">As dimensións empregadas para fixar os prezos e os custos da man de obra en organizacións baseadas en proxectos están influenciadas polos seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="78c77-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="78c77-105">Persoas que fan traballos similares á súa experiencia, rol ou zona xeográfica</span><span class="sxs-lookup"><span data-stu-id="78c77-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="78c77-106">Traballo que se realizará de xeito similar á súa complexidade ou hora do día</span><span class="sxs-lookup"><span data-stu-id="78c77-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="78c77-107">Dada a natureza típica destes atributos do traballo e das persoas necesarias para realizar o traballo, hai dous tipos de valores de dimensión de prezos dispoñibles en Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="78c77-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="78c77-108">**Conxuntos de opcións**: Atributos que son enumeracións fixas para un conxunto de valores.</span><span class="sxs-lookup"><span data-stu-id="78c77-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="78c77-109">**Valores baseados en entidades**: Atributos que poden ter un conxunto variado de valores que son finitos pero que poden cambiar co paso do tempo.</span><span class="sxs-lookup"><span data-stu-id="78c77-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="78c77-110">Dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="78c77-110">Pricing dimensions</span></span>

<span data-ttu-id="78c77-111">PSA envíase cun conxunto predefinido de dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="78c77-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="78c77-112">Podes velas indo a **Project Service** > **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="78c77-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="78c77-113">No rexistro de parámetros, no separador **Dimensións de prezos baseados na cantidade**, verifique que o rol, **msdyn_resourcecategory**, e a unidade organizativa de recursos, **msdyn_organizationalunit** teñan os campos **Aplicable a vendas** e **Aplicable a custo** establecidos en **Si**.</span><span class="sxs-lookup"><span data-stu-id="78c77-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="78c77-114">Isto permitirá establecer o prezo e o custo para cada combinación de roles e unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="78c77-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de pantalla dos parámetros de Project Service con "Aplicable a vendas" resaltado](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="78c77-116">Se estivo a usar os campos listos para usar de rol e unidade organizativa como dimensións de prezos antes da versión 3 de PSA, non haberá ningún cambio observable.</span><span class="sxs-lookup"><span data-stu-id="78c77-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="78c77-117">Pode seguir usando o Project Service como sempre.</span><span class="sxs-lookup"><span data-stu-id="78c77-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="78c77-118">Se precisa un prezo ou custo para os seus recursos usando atributos adicionais, pode crear campos, entidades e dimensións personalizados.</span><span class="sxs-lookup"><span data-stu-id="78c77-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="78c77-119">Para obter máis información, consulte os temas seguintes, pero teña en conta que debe completar os procedementos na orde que aparece a continuación:</span><span class="sxs-lookup"><span data-stu-id="78c77-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="78c77-120">Crear campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="78c77-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="78c77-121">Engadir campos personalizados a configuración de prezos e entidades transaccionais</span><span class="sxs-lookup"><span data-stu-id="78c77-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="78c77-122">Configurar campos personalizados como dimensións de prezos </span><span class="sxs-lookup"><span data-stu-id="78c77-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="78c77-123">Actualizar os atributos do complemento para incluír novas dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="78c77-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="78c77-124">Prezos do tempo de recursos humanos</span><span class="sxs-lookup"><span data-stu-id="78c77-124">Pricing human resource time</span></span>
<span data-ttu-id="78c77-125">Como unha organización valora o tempo dos recursos humanos é moitas veces unha consideración estratéxica importante que afecta directamente á rendibilidade da organización.</span><span class="sxs-lookup"><span data-stu-id="78c77-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="78c77-126">Traballe cos equipos financeiros e os responsables de prácticas cando a súa organización estea preparada para identificar como quere configurar os tipos de factura e custos para o tempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="78c77-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="78c77-127">Outras consideracións para fixar os prezos inclúen se hai que volver usar campos ou entidades que actualmente non teñen dimensións de prezos pero que se aplican como dimensión de prezos para a súa organización.</span><span class="sxs-lookup"><span data-stu-id="78c77-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="78c77-128">Campos como **Categoría de transacción** (**msdyn_transactioncategory**) e **Recurso reservable** ( **bookableresource**) son exemplos de dimensións do candidato.</span><span class="sxs-lookup"><span data-stu-id="78c77-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="78c77-129">Considere se a súa dimensión de prezos debe ser unha táboa ou un conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="78c77-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="78c77-130">Se prevé cambios nos valores dunha dimensión que serán máis de 10 ou 12 e necesita atributos adicionais nestes valores, podería crear unha entidade en lugar dun conxunto de opcións.</span><span class="sxs-lookup"><span data-stu-id="78c77-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="78c77-131">Manter un conxunto de opcións, como engadir ou eliminar valores, require un administrador ou programador, mentres que a adición de novas filas a unha táboa pode facelo a maioría dos usuarios empresariais.</span><span class="sxs-lookup"><span data-stu-id="78c77-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="78c77-132">O seguinte exemplo mostra os tipos de facturación que se configuran en función do rol e da unidade organizativa de recursos á que pertenza o recurso.</span><span class="sxs-lookup"><span data-stu-id="78c77-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="78c77-133">As taxas de custo baséanse normalmente na banda salarial do empregado e a unidade organizativa á que pertenza.</span><span class="sxs-lookup"><span data-stu-id="78c77-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="78c77-134">Neste exemplo, as táboas de taxa de facturación e taxa de custo terán o seguinte aspecto.</span><span class="sxs-lookup"><span data-stu-id="78c77-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="78c77-135">**Exemplo de taxas de facturación**</span><span class="sxs-lookup"><span data-stu-id="78c77-135">**Sample bill rates**</span></span>

| <span data-ttu-id="78c77-136">Rol</span><span class="sxs-lookup"><span data-stu-id="78c77-136">Role</span></span>        | <span data-ttu-id="78c77-137">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="78c77-137">Org Unit</span></span>    |<span data-ttu-id="78c77-138">Unidade</span><span class="sxs-lookup"><span data-stu-id="78c77-138">Unit</span></span>      |<span data-ttu-id="78c77-139">Prezo</span><span class="sxs-lookup"><span data-stu-id="78c77-139">Price</span></span>      |<span data-ttu-id="78c77-140">Moeda</span><span class="sxs-lookup"><span data-stu-id="78c77-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="78c77-141">Programador</span><span class="sxs-lookup"><span data-stu-id="78c77-141">Developer</span></span>   | <span data-ttu-id="78c77-142">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="78c77-142">Contoso US</span></span>  |<span data-ttu-id="78c77-143">Hora</span><span class="sxs-lookup"><span data-stu-id="78c77-143">Hour</span></span> | <span data-ttu-id="78c77-144">200</span><span class="sxs-lookup"><span data-stu-id="78c77-144">200</span></span>|<span data-ttu-id="78c77-145">USD</span><span class="sxs-lookup"><span data-stu-id="78c77-145">USD</span></span>     |
| <span data-ttu-id="78c77-146">Programador</span><span class="sxs-lookup"><span data-stu-id="78c77-146">Developer</span></span>   | <span data-ttu-id="78c77-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="78c77-147">Contoso India</span></span> |<span data-ttu-id="78c77-148">Hora</span><span class="sxs-lookup"><span data-stu-id="78c77-148">Hour</span></span>|   <span data-ttu-id="78c77-149">112</span><span class="sxs-lookup"><span data-stu-id="78c77-149">112</span></span>|<span data-ttu-id="78c77-150">USD</span><span class="sxs-lookup"><span data-stu-id="78c77-150">USD</span></span>     |


<span data-ttu-id="78c77-151">**Exempo de taxas de custo**</span><span class="sxs-lookup"><span data-stu-id="78c77-151">**Sample cost rates**</span></span>

| <span data-ttu-id="78c77-152">Banda salarial</span><span class="sxs-lookup"><span data-stu-id="78c77-152">Salary Band</span></span>     | <span data-ttu-id="78c77-153">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="78c77-153">Org Unit</span></span>    |<span data-ttu-id="78c77-154">Unidade</span><span class="sxs-lookup"><span data-stu-id="78c77-154">Unit</span></span>      |<span data-ttu-id="78c77-155">Prezo</span><span class="sxs-lookup"><span data-stu-id="78c77-155">Price</span></span>      |<span data-ttu-id="78c77-156">Moeda</span><span class="sxs-lookup"><span data-stu-id="78c77-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="78c77-157">A miña empresa_Banda1</span><span class="sxs-lookup"><span data-stu-id="78c77-157">My company_Band1</span></span> | <span data-ttu-id="78c77-158">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="78c77-158">Contoso US</span></span>  |<span data-ttu-id="78c77-159">Hora</span><span class="sxs-lookup"><span data-stu-id="78c77-159">Hour</span></span> | <span data-ttu-id="78c77-160">145</span><span class="sxs-lookup"><span data-stu-id="78c77-160">145</span></span>|<span data-ttu-id="78c77-161">USD</span><span class="sxs-lookup"><span data-stu-id="78c77-161">USD</span></span>     |
| <span data-ttu-id="78c77-162">A miña empresa_Banda2</span><span class="sxs-lookup"><span data-stu-id="78c77-162">My company_Band2</span></span> | <span data-ttu-id="78c77-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="78c77-163">Contoso India</span></span> |<span data-ttu-id="78c77-164">Hora</span><span class="sxs-lookup"><span data-stu-id="78c77-164">Hour</span></span>|   <span data-ttu-id="78c77-165">67</span><span class="sxs-lookup"><span data-stu-id="78c77-165">67</span></span>|<span data-ttu-id="78c77-166">USD</span><span class="sxs-lookup"><span data-stu-id="78c77-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]