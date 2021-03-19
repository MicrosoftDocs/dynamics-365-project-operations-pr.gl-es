---
title: Anular listas de prezos de vendas de proxecto
description: Este tema ofrece información sobre como crear listas de prezos de venda personalizadas.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275536"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="70c50-103">Anular listas de prezos de vendas de proxecto</span><span class="sxs-lookup"><span data-stu-id="70c50-103">Override project sales price lists</span></span>

<span data-ttu-id="70c50-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="70c50-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="70c50-105">Listas de prezos de proxecto específicas do cliente</span><span class="sxs-lookup"><span data-stu-id="70c50-105">Customer-specific project price lists</span></span>

<span data-ttu-id="70c50-106">Os acordos de prezos específicos do cliente pódense configurar como listas de prezos do proxecto nun rexistro de conta en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="70c50-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="70c50-107">Para configurar unha lista de prezos de proxecto específica do cliente, na área **Vendas**, navegue ata o rexistro da conta.</span><span class="sxs-lookup"><span data-stu-id="70c50-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="70c50-108">Abra a páxina de lista **Contas**.</span><span class="sxs-lookup"><span data-stu-id="70c50-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="70c50-109">Localice e prema dúas veces nun rexistro de cliente para abrir a páxina de detalles **Conta**.</span><span class="sxs-lookup"><span data-stu-id="70c50-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="70c50-110">No separador **Listas de prezos de proxecto**, seleccione **+ Nova lista de prezos de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="70c50-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="70c50-111">Na páxina **Nova lista de prezos de proxecto**, seleccione unha lista de prezos no menú despregable.</span><span class="sxs-lookup"><span data-stu-id="70c50-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="70c50-112">Só as listas de prezos que teñen o contexto establecido en **Vendas** e cuxa moeda coincide coa moeda da conta están incluídas.</span><span class="sxs-lookup"><span data-stu-id="70c50-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="70c50-113">Poña un nome á asociación e, a seguir, seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="70c50-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="70c50-114">Créase unha lista de prezos de proxecto específica do cliente.</span><span class="sxs-lookup"><span data-stu-id="70c50-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="70c50-115">Esta lista de prezos usarase para predefinir os prezos do proxecto nas ofertas ou contratos de proxecto ou contratos creados para este cliente cando a data de creación da oferta ou contrato de proxecto entra dentro da data de efectividade da lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="70c50-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="70c50-116">Prezos personalizados en ofertas de proxecto</span><span class="sxs-lookup"><span data-stu-id="70c50-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="70c50-117">Nas ofertas de proxecto, pode ter prezos de proxectos que comecen cunha lista de prezos estándar predefinida que se obtén do cliente ou dos parámetros do proxecto.</span><span class="sxs-lookup"><span data-stu-id="70c50-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="70c50-118">Cando precisa un prezo personalizado para o traballo relacionado co proxecto cunha oferta concreta, pode obtelo na entidade asociada de listas de prezos de proxecto.</span><span class="sxs-lookup"><span data-stu-id="70c50-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="70c50-119">Complete os seguintes pasos para configurar os prezos do proxecto baseado en proxecto.</span><span class="sxs-lookup"><span data-stu-id="70c50-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="70c50-120">Abra a oferta de proxecto e seleccione o separador **Listas de prezos de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="70c50-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="70c50-121">Na subgrade, seleccione **Crear prezos personalizados**.</span><span class="sxs-lookup"><span data-stu-id="70c50-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="70c50-122">Todas as listas de prezos do proxecto que se anexan á oferta cópianse en novas listas de prezos.</span><span class="sxs-lookup"><span data-stu-id="70c50-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="70c50-123">Os nomes das novas listas de prezos reflicten o nome da oferta cun selo de data e hora para o momento no que se crearon estas listas de prezos.</span><span class="sxs-lookup"><span data-stu-id="70c50-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="70c50-124">Pode usar cada unha desas listas de prezos e actualizar os prezos da man de obra (prezo de rol) e de gasto (prezo de categoría).</span><span class="sxs-lookup"><span data-stu-id="70c50-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="70c50-125">Estes prezos só serán aplicables a esta oferta de proxecto.</span><span class="sxs-lookup"><span data-stu-id="70c50-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="70c50-126">Listas de prezos nun contrato do proxecto</span><span class="sxs-lookup"><span data-stu-id="70c50-126">Price lists on a project contract</span></span>

<span data-ttu-id="70c50-127">Nun contrato de proxecto, os prezos do proxecto sempre se predefinen como unha lista de prezos personalizada co nome do contrato e a o selo de data e hora de creación anexo ao nome.</span><span class="sxs-lookup"><span data-stu-id="70c50-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="70c50-128">Isto é certo se o contrato se creou cando se gañou a oferta ou se o contrato se creou desde cero.</span><span class="sxs-lookup"><span data-stu-id="70c50-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="70c50-129">Se é necesario, pode eliminar esta asociación á lista de prezos personalizada e asociar unha lista de prezos estándar ao contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="70c50-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="70c50-130">Cando asocia unha lista de prezos estándar ás listas de prezos do proxecto na oferta ou no contrato, calquera cambio realizado nos prezos da lista de prezos afectará a todas as ofertas e contratos que usen a lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="70c50-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]