---
title: Unidades e grupos de unidades
description: Este tema ofrece información sobre como crear unidades e grupos de unidades en Dynamics 365 Project Operations.
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277336"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="df11c-103">Unidades e grupos de unidades</span><span class="sxs-lookup"><span data-stu-id="df11c-103">Units and unit groups</span></span>

<span data-ttu-id="df11c-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="df11c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="df11c-105">As unidades son as cantidades ou medidas en que se venden os produtos ou servizos.</span><span class="sxs-lookup"><span data-stu-id="df11c-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="df11c-106">Por exemplo, se vende subministros para xardinería, é posible que venda sementes en unidades de paquetes, caixas e pallets.</span><span class="sxs-lookup"><span data-stu-id="df11c-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="df11c-107">Un grupo de unidades é unha recompilación destas unidades.</span><span class="sxs-lookup"><span data-stu-id="df11c-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="df11c-108">Para completar os pasos deste tema, asegúrese de que se lle atribuíu o rol de Administrador do sistema ou Xestor de Sales Professional ou que ten permisos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="df11c-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="df11c-109">Crear un grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="df11c-109">Create a unit group</span></span>

1. <span data-ttu-id="df11c-110">No mapa do sitio, seleccione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="df11c-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="df11c-111">Seleccione **Nova** e na caixa de diálogo **Crear grupo de unidades**, introduza o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="df11c-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="df11c-112">No campo **Unidade primaria**, introduza a unidade de medida común mínima en que se venderá o produto.</span><span class="sxs-lookup"><span data-stu-id="df11c-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="df11c-113">Por exemplo, pode introducir "peza" ou "onza".</span><span class="sxs-lookup"><span data-stu-id="df11c-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="df11c-114">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="df11c-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="df11c-115">Engadir unidades a un grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="df11c-115">Add units to a unit group</span></span>

1. <span data-ttu-id="df11c-116">Abra un grupo de unidades e, no separador **Relacionado**, seleccione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="df11c-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="df11c-117">Verá que a unidade primaria xa está engadida.</span><span class="sxs-lookup"><span data-stu-id="df11c-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="df11c-118">Seleccione **Engadir nova unidade** e, na páxina **Creación rápida: unidade**, no campo **Nome**, introduza o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="df11c-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="df11c-119">No campo **Cantidade**, introduza a cantidade que conterá a unidade.</span><span class="sxs-lookup"><span data-stu-id="df11c-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="df11c-120">Por exemplo, se unha caixa contén dúas pezas, introduza "2".</span><span class="sxs-lookup"><span data-stu-id="df11c-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="df11c-121">No campo **Unidade base**, seleccione unha unidade base para establecer a unidade de medida máis baixa para a unidade.</span><span class="sxs-lookup"><span data-stu-id="df11c-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="df11c-122">Por exemplo, podería seleccionar "peza".</span><span class="sxs-lookup"><span data-stu-id="df11c-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="df11c-123">Seleccione **Gardar**:</span><span class="sxs-lookup"><span data-stu-id="df11c-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]