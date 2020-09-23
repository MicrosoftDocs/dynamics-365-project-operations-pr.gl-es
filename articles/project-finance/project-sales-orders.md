---
title: Pedidos de venda de proxectos para proxectos de tempo e material
description: Este tema explica como crear pedidos de venda baseados en proxectos para proxectos de tempo e material.
author: KimANelson
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
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751340"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="23d26-103">Pedidos de venda de proxectos para proxectos de tempo e material</span><span class="sxs-lookup"><span data-stu-id="23d26-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="23d26-104">Este tema describe como crear un pedido de venda para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="23d26-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="23d26-105">Os pedidos de venda só se poden crear para proxectos de tipo **tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="23d26-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="23d26-106">Se un proxecto de tempo e material ten varias fontes de financiamento no contrato do proxecto, debe habilitar o parámetro **Permitir pedidos de venda para proxectos con varias fontes de financiamento** na páxina **Parámetros de xestión de proxectos e contabilidade**.</span><span class="sxs-lookup"><span data-stu-id="23d26-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="23d26-107">A asistencia para pedidos de vendas de proxectos con varias fontes de financiamento está dispoñible a partir da versión da aplicación 10.0.2 e superior.</span><span class="sxs-lookup"><span data-stu-id="23d26-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="23d26-108">O parámetro para habilitar a asistencia para pedidos de venda de proxectos con varias fontes de financiamento eliminarase na onda da versión de abril de 2020, despois do cal a funcionalidade sempre estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="23d26-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="23d26-109">Pode crear pedidos de venda baseados en proxectos de dous xeitos:</span><span class="sxs-lookup"><span data-stu-id="23d26-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="23d26-110">Vaia ao propio proxecto.</span><span class="sxs-lookup"><span data-stu-id="23d26-110">Go to the project itself.</span></span> <span data-ttu-id="23d26-111">No panel Acción, seleccione **Xestionar > Tarefas do artigo > Pedido de venda**.</span><span class="sxs-lookup"><span data-stu-id="23d26-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="23d26-112">A información do proxecto será o pedido de venda predefinido do proxecto.</span><span class="sxs-lookup"><span data-stu-id="23d26-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="23d26-113">Se o contrato do proxecto ten máis dunha fonte de financiamento, deberá seleccionar a fonte de financiamento para configurar o cliente para o pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="23d26-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="23d26-114">Se só hai unha fonte de financiamento para o proxecto, o cliente configurarase automaticamente.</span><span class="sxs-lookup"><span data-stu-id="23d26-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="23d26-115">Vaia á páxina de lista **Todos os pedidos de venda** e cree un novo pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="23d26-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="23d26-116">Deberá seleccionar o proxecto para o pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="23d26-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="23d26-117">Despois de seleccionar o proxecto, configurarase o cliente desde a fonte de financiamento ou deberá seleccionar a fonte de financiamento se o contrato do proxecto ten varias fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="23d26-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

