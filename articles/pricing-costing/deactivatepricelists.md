---
title: Desactivar listas de prezos
description: Este tema explica como desactivar ou eliminar listas de prezos non usadas ou antigas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001334"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="0230e-103">Desactivar listas de prezos</span><span class="sxs-lookup"><span data-stu-id="0230e-103">Deactivate price lists</span></span> 

<span data-ttu-id="0230e-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="0230e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0230e-105">Para eliminar as listas de prezos antigas ou non usadas de Dynamics 365 Project Operations, hai dous pasos que debe completar.</span><span class="sxs-lookup"><span data-stu-id="0230e-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="0230e-106">Elimine ou borre a lista de prezos de páxinas específicas.</span><span class="sxs-lookup"><span data-stu-id="0230e-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="0230e-107">Desactive ou elimine a lista de prezos das listas de prezos activas da páxina **Listas de prezos**.</span><span class="sxs-lookup"><span data-stu-id="0230e-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="0230e-108">Debe completar os dous pasos para eliminar completamente unha lista de prezos.</span><span class="sxs-lookup"><span data-stu-id="0230e-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="0230e-109">Non é suficiente só realizar o paso 2, que consiste en eliminar ou desactivar directamente a lista de prezos da vista Listas de prezos activos.</span><span class="sxs-lookup"><span data-stu-id="0230e-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="0230e-110">Tamén debe eliminar a asociación desta lista de prezos de todos os lugares mencionados no paso 1.</span><span class="sxs-lookup"><span data-stu-id="0230e-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="0230e-111">Eliminar a lista de prezos de páxinas específicas</span><span class="sxs-lookup"><span data-stu-id="0230e-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="0230e-112">Para eliminar unha lista de prezos de Project Operations, vaia ás seguintes páxinas:</span><span class="sxs-lookup"><span data-stu-id="0230e-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="0230e-113">Páxna **Parámetros de proxecto** > separador **Listas de prezos**</span><span class="sxs-lookup"><span data-stu-id="0230e-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="0230e-114">Páxina **Unidade Organizativa** > grade **Listas de prezos**</span><span class="sxs-lookup"><span data-stu-id="0230e-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="0230e-115">Páxina **Conta** > grade **Listas de prezos de proxecto**</span><span class="sxs-lookup"><span data-stu-id="0230e-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="0230e-116">Páxina **Ofertas de proxecto** > grade **Listas de prezos de proxecto**: isto aplícase a todas as ofertas de proxectos activos.</span><span class="sxs-lookup"><span data-stu-id="0230e-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="0230e-117">Páxina **Contratos de proxecto** > grade **Listas de prezos de proxecto**: isto aplícase a todos os contratos de proxectos activos.</span><span class="sxs-lookup"><span data-stu-id="0230e-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="0230e-118">Para cada páxina, ten que seleccionar a lista de prezos que desexa eliminar e, a seguir, seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="0230e-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="0230e-119">Desactive ou elimine a lista de prezos da páxina Listas de prezos.</span><span class="sxs-lookup"><span data-stu-id="0230e-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="0230e-120">Para eliminar unha lista de prezos das listas de prezos activas, vaia a **Vendas** > **Clientes** > **Listas de prezos**.</span><span class="sxs-lookup"><span data-stu-id="0230e-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="0230e-121">Seleccione a lista de prezos que desexa eliminar e, a seguir, seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="0230e-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="0230e-122">Se fai referencia á lista de prezos nalgunha transacción existente, non poderá eliminala.</span><span class="sxs-lookup"><span data-stu-id="0230e-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="0230e-123">Se isto ocorre, pode desactivar a lista de prezos para que non apareza en ningunha vista.</span><span class="sxs-lookup"><span data-stu-id="0230e-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="0230e-124">Para desactivar a lista de prezos, seleccione de novo a lista de prezos e logo seleccione **Desactivar**.</span><span class="sxs-lookup"><span data-stu-id="0230e-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
