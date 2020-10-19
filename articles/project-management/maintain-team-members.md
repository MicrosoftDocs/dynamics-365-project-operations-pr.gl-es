---
title: Manter os membros do equipo
description: Este tema fornece información sobre a reserva de recursos nomeados para equipos de proxectos e atribuírlles tarefas.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961861"
---
# <a name="maintain-team-members"></a><span data-ttu-id="1d90b-103">Manter os membros do equipo</span><span class="sxs-lookup"><span data-stu-id="1d90b-103">Maintain team members</span></span>

<span data-ttu-id="1d90b-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1d90b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d90b-105">Pode engadir un recurso nomeado ao seu equipo de proxectos reservándoo directamente ao equipo.</span><span class="sxs-lookup"><span data-stu-id="1d90b-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="1d90b-106">En Dynamics 365 Project Operations, vaia a **Proxectos** e seleccione abrir o proxecto para o que vai reservar.</span><span class="sxs-lookup"><span data-stu-id="1d90b-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="1d90b-107">Na páxina **Proxecto**, no separador **Equipo**, seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="1d90b-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="1d90b-108">Na caixa de diálogo **Creación rápida de membro do equipo de proxecto**, seleccione o recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="1d90b-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="1d90b-109">O campo **Rol** encherase co rol predefinido do recurso se ten un atribuído.</span><span class="sxs-lookup"><span data-stu-id="1d90b-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="1d90b-110">Pode modificar o rol.</span><span class="sxs-lookup"><span data-stu-id="1d90b-110">You can change the role.</span></span> 
4. <span data-ttu-id="1d90b-111">Seleccione as datas desde e ata nas que se necesitará o recurso e seleccione o método de atribución da capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="1d90b-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="1d90b-112">No campo **Responsable de aprobación do proxecto**, seleccione **Si** se desexa que o membro do equipo sexa o responsable da a probación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1d90b-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="1d90b-113">O membro do equipo pode aprobar as entradas de tempo e gastos presentadas para este proxecto.</span><span class="sxs-lookup"><span data-stu-id="1d90b-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="1d90b-114">Seleccione **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="1d90b-114">Select **Save**.</span></span>

<span data-ttu-id="1d90b-115">Agora pode atribuír o recurso reservado a tarefas do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1d90b-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="1d90b-116">Na páxina **Proxecto**, no separador **Programación**, atribúa tarefas ao novo recurso.</span><span class="sxs-lookup"><span data-stu-id="1d90b-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="1d90b-117">O selector de recursos que se inicia desde o campo **Recursos** na grada de tarefas amosará os membros do equipo que pode seleccionar.</span><span class="sxs-lookup"><span data-stu-id="1d90b-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="1d90b-118">En Project Operations, as reservas de recursos e as tarefas non están ben emparelladas.</span><span class="sxs-lookup"><span data-stu-id="1d90b-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="1d90b-119">Cando utiliza o selector de recursos na programación, pode atribuír tarefas aos membros do equipo durante máis horas das que cobren as súas reservas no proxecto.</span><span class="sxs-lookup"><span data-stu-id="1d90b-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="1d90b-120">As diferenzas entre as reservas dos membros do equipo e as tarefas móstranse nos separadores **Equipo** e **Conciliación de recursos**.</span><span class="sxs-lookup"><span data-stu-id="1d90b-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="1d90b-121">Tamén pode conciliar as diferenzas entre reservas e tarefas de recursos a un nivel máis detallado.</span><span class="sxs-lookup"><span data-stu-id="1d90b-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="1d90b-122">Utilice o selector de recursos no separador **Programación** para buscar e seleccionar recursos reservables que xa non forman parte do equipo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="1d90b-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="1d90b-123">Estes recursos móstranse no selector de recursos como **Outros recursos**.</span><span class="sxs-lookup"><span data-stu-id="1d90b-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="1d90b-124">Cando fai unha selección, o recurso engádese ao equipo do proxecto e atribúese á tarefa, pero non se xeran reservas.</span><span class="sxs-lookup"><span data-stu-id="1d90b-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="1d90b-125">Pode usar a capacidade de extensión de recursos no separador **Reconciliación** ou o **Panel de programación** para reservar a capacidade do recurso para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="1d90b-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="1d90b-126">Despois de que un membro do equipo estea reservado no seu proxecto, pode usar **Manter reservas** ou o **Panel de programación** directamente para xestionar as súas reservas.</span><span class="sxs-lookup"><span data-stu-id="1d90b-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
