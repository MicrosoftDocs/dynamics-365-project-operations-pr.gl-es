---
title: Definir calendarios de proxectos
description: Este tema ofrece información sobre o uso dun calendario do proxecto para rastrexar a programación do proxecto.
author: ruhercul
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286966"
---
# <a name="define-project-calendars"></a><span data-ttu-id="aae89-103">Definir calendarios de proxectos</span><span class="sxs-lookup"><span data-stu-id="aae89-103">Define project calendars</span></span>

<span data-ttu-id="aae89-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="aae89-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aae89-105">Para crear unha programación de proxecto, créase un modelo de calendario de proxecto que define o número de horas de traballo para adaptar por día na programación e os peches de empresa.</span><span class="sxs-lookup"><span data-stu-id="aae89-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="aae89-106">Para crear un modelo de calendario de proxecto, asocie un modelo de traballo ao campo **Modelo de calendario** para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="aae89-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="aae89-107">Siga estes pasos para crear un modelo de traballo.</span><span class="sxs-lookup"><span data-stu-id="aae89-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="aae89-108">No panel de navegación esquerdo, seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="aae89-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="aae89-109">Na páxina de lista **Recursos**, abra un rexistro de usuario e, a seguir, seleccione **Mostrar horas laborables**.</span><span class="sxs-lookup"><span data-stu-id="aae89-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="aae89-110">Asegúrese de permitir ventás emerxentes na páxina do navegador.</span><span class="sxs-lookup"><span data-stu-id="aae89-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="aae89-111">Isto permítelle ver as horas laborables establecidas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="aae89-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="aae89-112">No separador **Vista mensual**, seleccione **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="aae89-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="aae89-113">Aparece unha lista de tres opcións:</span><span class="sxs-lookup"><span data-stu-id="aae89-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="aae89-114">Nova programación semanal</span><span class="sxs-lookup"><span data-stu-id="aae89-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="aae89-115">Programación de traballo para un día</span><span class="sxs-lookup"><span data-stu-id="aae89-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="aae89-116">Tempo libre</span><span class="sxs-lookup"><span data-stu-id="aae89-116">Time Off</span></span>

4. <span data-ttu-id="aae89-117">Seleccione **Nova programación semanal** e logo configure as opcións para esta programación de recursos.</span><span class="sxs-lookup"><span data-stu-id="aae89-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="aae89-118">Pode definir unha programación semanal recorrente, parámetros horarios diarios, peches de negocio e moito máis.</span><span class="sxs-lookup"><span data-stu-id="aae89-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="aae89-119">Estableza o intervalo de datas, seleccione **Gardar** e, a seguir, seleccione **Pechar**.</span><span class="sxs-lookup"><span data-stu-id="aae89-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="aae89-120">Volva á páxina de lista **Recursos** e seleccione o recurso para o que estableceu as horas laborables.</span><span class="sxs-lookup"><span data-stu-id="aae89-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="aae89-121">Seleccione **Establecer calendario como** para configurar o modelo de traballo.</span><span class="sxs-lookup"><span data-stu-id="aae89-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="aae89-122">Na caixa de diálogo **Modelo de traballo**, introduza un nome para o modelo de traballo e, a seguir, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="aae89-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="aae89-123">Agora pode asociar o modelo de traballo a un modelo de calendario de proxecto.</span><span class="sxs-lookup"><span data-stu-id="aae89-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]