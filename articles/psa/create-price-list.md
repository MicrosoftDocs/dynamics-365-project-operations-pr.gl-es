---
title: Crear unha lista de prezos
description: Como crear una lista de prezos en Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf75286fd1837e27a9b6053ccb21b60771ee197d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076168"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="e8fdb-103">Crear unha lista de prezos (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e8fdb-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e8fdb-104">As listas de prezos fornecen un modelo que os xestores de contas poden utilizar para a creación de ofertas e proxectos, e para establecer os custos dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="e8fdb-105">Fornecen unha lista de elementos de liña de roles e gastos, e os prezos que se van aplicar a cada un.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="e8fdb-106">Pode crear varias listas de prezos para manter estruturas de prezos independentes para diferentes rexións nas que venderá os seus produtos ou para diferentes canles de venda.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="e8fdb-107">É aconsellable crear polo menos unha lista de prezos para cada moeda coa que ten intención de facturar aos seus clientes.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="e8fdb-108">Para crear estimacións de actividades financeiras para entregar o traballo, asegúrese de que cada proxecto ten unha lista de seguridade de prezos de custo e vendas.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="e8fdb-109">Configurar unha lista de rezos de vendas e custos predefinida que se aplique a todos os proxectos creados na súa organización.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="e8fdb-110">As listas de prezos dependen das categorías de gastos e roles, polo que antes de crear unha lista de prezos, asegúrese de ter configuradas as categorías de gastos e roles que desexa utilizar ao crear a lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="e8fdb-111">Vaia a **Project Service > Listas de prezos**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="e8fdb-112">Prema **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="e8fdb-113">En **Contexto** , seleccione se esta lista de prezos é para **Custo** , **Compra** ou **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-113">In **Context** , select whether this price list is for **Cost** , **Purchase** , or **Sales**.</span></span>  
  
4.  <span data-ttu-id="e8fdb-114">En **Nome** , introduza un nome para a lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-114">In **Name** , enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="e8fdb-115">En **Moeda** , seleccione a moeda que se vai utilizar para facturación ou custos.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-115">In **Currency** , select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="e8fdb-116">En **Unidade de tempo** , especifique o período de tempo ao que se aplica o prezo, como día ou horas.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-116">In **Time Unit** , specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="e8fdb-117">Encha a **Data de Comezo** , **Data de Fin** e **Descrición** segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-117">Fill in the **Start Date** , **End Date** , and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="e8fdb-118">Prema **Gardar** para crear o rexistro e poder editalo.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="e8fdb-119">Para engadir un prezo de rol á lista de prezos, prema **+** en **Prezos de rol**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="e8fdb-120">No panel **Prezos de rol** , encha os detalles e, a seguir, prema en **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e8fdb-121">Continúe a engadir prezos de rol segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="e8fdb-122">Ao acabar, prema **Gardar** na parte inferior dereita da pantalla.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="e8fdb-123">Para engadir un prezo de categoría de custo á lista de prezos, prema **+** en **Categoría de prezos**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="e8fdb-124">No panel **Prezos de categoría de transaccións** , encha os detalles e, a seguir, prema en **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e8fdb-125">Continúe a engadir prezos de categoría segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="e8fdb-126">Ao acabar, prema **Gardar** na parte inferior dereita da pantalla.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="e8fdb-127">Para engadir elementos da lista de prezos á lista de prezos, prema **+** en **Elementos da Lista de Prezos**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="e8fdb-128">No panel **Elemento da lista de prezos** , encha os detalles e, a seguir, prema en **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e8fdb-129">Continúe a engadir elementos da lista de prezos segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="e8fdb-130">Ao acabar, prema **Gardar** na parte inferior dereita da pantalla.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="e8fdb-131">Para engadir relacións de zonas de vendas á lista de prezos, prema **+** en **Relacións de zonas de vendas**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="e8fdb-132">Na ventá **Nova conexión** , encha os detalles e, a seguir, prema en **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="e8fdb-133">Continuar a engadir relacións de zonas de vendas segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="e8fdb-134">Ao acabar, prema **Gardar** na parte inferior dereita da pantalla.</span><span class="sxs-lookup"><span data-stu-id="e8fdb-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e8fdb-135">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="e8fdb-135">See Also</span></span>  
 [<span data-ttu-id="e8fdb-136">Configurar Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e8fdb-136">Configure Project Service Automation</span></span>](../psa/configure.md)
