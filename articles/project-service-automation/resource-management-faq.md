---
title: Preguntas frecuentes sobre xestión de recursos.
description: Este tema ofrece respostas a preguntas frecuentes sobre xestión de recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751437"
---
# <a name="resource-management-faq"></a><span data-ttu-id="7c5de-103">Preguntas frecuentes sobre xestión de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c5de-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="7c5de-104">Cal é a diferenza entre un membro do equipo e un requisito de recurso?</span><span class="sxs-lookup"><span data-stu-id="7c5de-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="7c5de-105">Un membro do equipo do proxecto pode ser atribuído a tarefas, reservado ou saturado e establecido como responsable de aprobación.</span><span class="sxs-lookup"><span data-stu-id="7c5de-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="7c5de-106">Pode existir un requisito de recurso sen membro do equipo do proxecto, como nota de demanda.</span><span class="sxs-lookup"><span data-stu-id="7c5de-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="7c5de-107">Cal é a diferenza entre o has horas propostas e as horas de reserva branda?</span><span class="sxs-lookup"><span data-stu-id="7c5de-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="7c5de-108">As horas propostas e as horas de reserva branda difiren en visibilidade.</span><span class="sxs-lookup"><span data-stu-id="7c5de-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="7c5de-109">As horas propostas só son visibles para os xestores de recursos e o xestor de proxectos que iniciaron a demanda mediante unha solicitude de recurso.</span><span class="sxs-lookup"><span data-stu-id="7c5de-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="7c5de-110">As horas de reserva branda son visibles para todos os que teñan acceso ao panel de programación.</span><span class="sxs-lookup"><span data-stu-id="7c5de-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="7c5de-111">Como podo ver as horas de reserva branda para os recursos dun equipo?</span><span class="sxs-lookup"><span data-stu-id="7c5de-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="7c5de-112">As reservas brandas se poden facer ao reservar un requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="7c5de-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="7c5de-113">Os recursos que teñen reservas brandas nun equipo do proxecto aparecen como membros do equipo que teñen horas de reserva branda.</span><span class="sxs-lookup"><span data-stu-id="7c5de-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="7c5de-114">Tamén se aparecen no panel de programación.</span><span class="sxs-lookup"><span data-stu-id="7c5de-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="7c5de-115">Como cambio as horas necesarias e as datas de inicio e finalización dun recurso (xenérico ou nomeado) que reservei?</span><span class="sxs-lookup"><span data-stu-id="7c5de-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="7c5de-116">Despois de reservar os recursos, seleccione **Manter reservas** para facer os cambios que se precisen.</span><span class="sxs-lookup"><span data-stu-id="7c5de-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="7c5de-117">Que tipos de recursos admite Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="7c5de-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="7c5de-118">**Usuario** e **Contacto** son os únicos tipos de recursos que admite Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7c5de-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="7c5de-119">Aínda que pode crear outro tipo de recursos (por exemplo, **Equipamento** e **Grupo**), non se admite ningún caso de uso global.</span><span class="sxs-lookup"><span data-stu-id="7c5de-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="7c5de-120">Que diferenza hai entre unha atribución e unha reserva?</span><span class="sxs-lookup"><span data-stu-id="7c5de-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="7c5de-121">As atribucións son a atribución de recursos ás tarefas do proxecto na programación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c5de-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="7c5de-122">Os recursos poden ser recursos reais ou xenéricos.</span><span class="sxs-lookup"><span data-stu-id="7c5de-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="7c5de-123">As reservas son a atribución branda o dura de recursos a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="7c5de-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="7c5de-124">As reservas duras consumen a capacidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="7c5de-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="7c5de-125">O ideal sería que, para os recursos reais, as reservas e as atribucións coincidisen, porque non difiren.</span><span class="sxs-lookup"><span data-stu-id="7c5de-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="7c5de-126">Non obstante, PSA non fai cumprir este acordo.</span><span class="sxs-lookup"><span data-stu-id="7c5de-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="7c5de-127">A vista Conciliación mostra a un xestor de proxectos lugares onde as reservas e atribucións dun recurso non coinciden.</span><span class="sxs-lookup"><span data-stu-id="7c5de-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
