---
title: Requisitos da reserva branda
description: Este tema fornece información sobre como cumprir requisitos de reserva branda.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124096"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="fe3bd-103">Requisitos da reserva branda</span><span class="sxs-lookup"><span data-stu-id="fe3bd-103">Soft-book requirements</span></span>

<span data-ttu-id="fe3bd-104">Pódese facer unha reserva dura dun requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="fe3bd-105">Unha reserva dura crea unha proposta que consume a capacidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="fe3bd-106">A proposta é remitida ao solicitante para a súa aprobación.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="fe3bd-107">Unha reserva branda engade provisionalmente un recurso a un equipo de proxecto e ten un estado diferente no panel de programación, pero non consume a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="fe3bd-108">Para facer unha reserva branda dun recurso, configure o campo **Estado da reserva** en **Branda**.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![O estado da reserva establecido en Branda](media/Resource-Management-image77.png)

<span data-ttu-id="fe3bd-110">Cando o separador **Equipo** está na vista **Membros nomeados do equipo**, o recurso aparece alí.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="fe3bd-111">As horas con reserva branda aparecen na columna **Horas con reserva branda**.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Horas con reserva branda na vista de membros nomeados do equipo](media/Resource-Management-image78.png)

<span data-ttu-id="fe3bd-113">Non se poden atribuír os membros do equipo cunha reserva branda a tarefas.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-113">Soft-booked team members can be assigned to tasks.</span></span>

![Membro do equipo cunha reserva branda atribuído a una tarefa.](media/Resource-Management-image79.png)

<span data-ttu-id="fe3bd-115">No separador **Conciliación**, non se amosan reservas para un recurso con reserva branda, porque o separador **Conciliación** considera só as reservas duras.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Recurso con reserva branda sen reservas no separador Conciliación](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="fe3bd-117">Non pode facer unha reserva branda dun recurso desde un requisito xerado cun membro xenérico do equipo.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="fe3bd-118">No panel de programación, úsase unha cor diferente para reservas brandas para un recurso.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Reservas brandas no panel de programación](media/Resource-Management-image81.png)

<span data-ttu-id="fe3bd-120">Para converter unha reserva branda en unha reserva dura, no panel de programación, prema co botón dereito do rato sobre a reserva branda e logo seleccione **Cambiar estado** \> **Reserva dura** \> **Dura**.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Cambio do estado da reserva a dura](media/Resource-Management-image82.png)

<span data-ttu-id="fe3bd-122">A reserva cambia e o estado cámbiase no panel de programación.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="fe3bd-123">Como o estado da reserva é agora **Dura**, o recurso móstrase como reservado e axústase a súa capacidade e dispoñibilidade.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="fe3bd-124">Pode usar o mesmo método para cancelar unha reserva dura ou unha reserva branda no panel de programación.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="fe3bd-125">Para converter un recurso con reserva branda en reserva dura no separador **Equipo** do proxecto, seleccione o recurso e logo seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Comando Confirmar](media/Resource-Management-image83.png)
