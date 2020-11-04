---
title: Reservas fronte a atribucións
description: Este tema ofrece información sobre as diferenzas entre as reservas de recursos e as atribucións de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075981"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="8b879-103">Reservas fronte a atribucións</span><span class="sxs-lookup"><span data-stu-id="8b879-103">Bookings vs assignments</span></span>

<span data-ttu-id="8b879-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="8b879-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b879-105">As reservas son a atribución branda o dura de recursos a un proxecto.</span><span class="sxs-lookup"><span data-stu-id="8b879-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="8b879-106">As reservas duras consumen a capacidade dun recurso.</span><span class="sxs-lookup"><span data-stu-id="8b879-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="8b879-107">As atribucións son a atribución de recursos ás tarefas do proxecto na programación do proxecto.</span><span class="sxs-lookup"><span data-stu-id="8b879-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="8b879-108">Os recursos poden ser reais ou xenéricos.</span><span class="sxs-lookup"><span data-stu-id="8b879-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="8b879-109">O ideal sería que, para os recursos reais, as reservas e as atribucións coincidisen, porque non difiren.</span><span class="sxs-lookup"><span data-stu-id="8b879-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="8b879-110">Non obstante, Microsoft Dynamics Project Operations non fai cumprir este acordo.</span><span class="sxs-lookup"><span data-stu-id="8b879-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="8b879-111">A vista **Conciliación** mostra a un xestor de proxectos lugares onde as reservas e atribucións dun recurso non coinciden.</span><span class="sxs-lookup"><span data-stu-id="8b879-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
