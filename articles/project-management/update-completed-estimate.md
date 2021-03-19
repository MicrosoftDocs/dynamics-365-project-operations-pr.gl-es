---
title: Actualizar estimación ao finalizar
description: Este tema ofrece información sobre a actualización da proxección do esforzo nun proxecto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286426"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="27004-103">Actualizar estimación ao finalizar</span><span class="sxs-lookup"><span data-stu-id="27004-103">Update estimate at completion</span></span>

<span data-ttu-id="27004-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="27004-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="27004-105">É frecuente que un xestor de proxectos revise as estimacións orixinais dunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="27004-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="27004-106">As novas proxeccións de proxectos son a percepción das estimacións do xestor dun proxecto, segundo o estado actual dun proxecto.</span><span class="sxs-lookup"><span data-stu-id="27004-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="27004-107">Non obstante, non recomendamos que os xestores de proxectos modifiquen os números da liña base, porque a liña base a fonte de verdade establecida para a as estimacións de custo e programación do proxecto que todos os implicados no proxecto acordaron.</span><span class="sxs-lookup"><span data-stu-id="27004-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="27004-108">Hai dous xeitos de que un xestor de proxecto poida volver a proxectar o esforzo das tarefas:</span><span class="sxs-lookup"><span data-stu-id="27004-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="27004-109">Anular o tempo estimado para finalizar (ETC) predefinido cunha nova estimación do esforzo restante real da tarefa.</span><span class="sxs-lookup"><span data-stu-id="27004-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="27004-110">Anular a porcentaxe de progreso predefinida cunha nova estimación do progreso real da tarefa.</span><span class="sxs-lookup"><span data-stu-id="27004-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="27004-111">Cada un destes enfoques provoca un novo cálculo do ETC, a estimación ao completar (EAC) e a porcentaxe de progreso da tarefa, e a varianza de esforzo proxectado nunha tarefa.</span><span class="sxs-lookup"><span data-stu-id="27004-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="27004-112">Calcúlanse de novo o EAC, ETC e a porcentaxe de progreso nas tarefas resumo, e producen unha nova proxección da varianza do esforzo.</span><span class="sxs-lookup"><span data-stu-id="27004-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]