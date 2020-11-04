---
title: Pedidos de venda de proxectos para proxectos de tempo e material
description: Este tema explica como crear pedidos de venda baseados en proxectos para proxectos de tempo e material.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076117"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="e1acf-103">Pedidos de venda de proxectos para proxectos de tempo e material</span><span class="sxs-lookup"><span data-stu-id="e1acf-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e1acf-104">Este tema describe como crear un pedido de venda para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="e1acf-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="e1acf-105">Os pedidos de venda só se poden crear para proxectos de tipo **tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="e1acf-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="e1acf-106">Se un proxecto de tempo e material ten varias fontes de financiamento no contrato do proxecto, debe habilitar o parámetro **Permitir pedidos de venda para proxectos con varias fontes de financiamento** na páxina **Parámetros de xestión de proxectos e contabilidade**.</span><span class="sxs-lookup"><span data-stu-id="e1acf-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="e1acf-107">A asistencia para pedidos de vendas de proxectos con varias fontes de financiamento está dispoñible a partir da versión da aplicación 10.0.2 e superior.</span><span class="sxs-lookup"><span data-stu-id="e1acf-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="e1acf-108">O parámetro para habilitar a asistencia para pedidos de venda de proxectos con varias fontes de financiamento eliminarase na onda da versión de abril de 2020, despois do cal a funcionalidade sempre estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="e1acf-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="e1acf-109">Pode crear pedidos de venda baseados en proxectos de dous xeitos:</span><span class="sxs-lookup"><span data-stu-id="e1acf-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="e1acf-110">Vaia ao propio proxecto.</span><span class="sxs-lookup"><span data-stu-id="e1acf-110">Go to the project itself.</span></span> <span data-ttu-id="e1acf-111">No panel Acción, seleccione **Xestionar > Tarefas do artigo > Pedido de venda**.</span><span class="sxs-lookup"><span data-stu-id="e1acf-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="e1acf-112">A información do proxecto será o pedido de venda predefinido do proxecto.</span><span class="sxs-lookup"><span data-stu-id="e1acf-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="e1acf-113">Se o contrato do proxecto ten máis dunha fonte de financiamento, deberá seleccionar a fonte de financiamento para configurar o cliente para o pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="e1acf-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="e1acf-114">Se só hai unha fonte de financiamento para o proxecto, o cliente configurarase automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e1acf-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="e1acf-115">Vaia á páxina de lista **Todos os pedidos de venda** e cree un novo pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="e1acf-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="e1acf-116">Deberá seleccionar o proxecto para o pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="e1acf-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="e1acf-117">Despois de seleccionar o proxecto, configurarase o cliente desde a fonte de financiamento ou deberá seleccionar a fonte de financiamento se o contrato do proxecto ten varias fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="e1acf-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

