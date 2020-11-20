---
title: Comprender o estado do proxecto
description: Este tema fornece información sobre o estado atribuído aos proxectos en Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127291"
---
# <a name="understand-project-status"></a><span data-ttu-id="76cab-103">Comprender o estado do proxecto</span><span class="sxs-lookup"><span data-stu-id="76cab-103">Understand project status</span></span>

<span data-ttu-id="76cab-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="76cab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="76cab-105">A sección **Estado** da páxina **Entidade do proxecto** ofrece un resumo da saúde dun proxecto en función do custo e do esforzo.</span><span class="sxs-lookup"><span data-stu-id="76cab-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="76cab-106">Campos resumo do estado</span><span class="sxs-lookup"><span data-stu-id="76cab-106">Status summary fields</span></span>

- <span data-ttu-id="76cab-107">O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto.</span><span class="sxs-lookup"><span data-stu-id="76cab-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="76cab-108">Este campo emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente.</span><span class="sxs-lookup"><span data-stu-id="76cab-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="76cab-109">O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado.</span><span class="sxs-lookup"><span data-stu-id="76cab-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="76cab-110">O campo **Estado actualizado o** non é editable.</span><span class="sxs-lookup"><span data-stu-id="76cab-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="76cab-111">O valor deste campo é unha marca de tempo que indica cando se actualizou por última vez o estado.</span><span class="sxs-lookup"><span data-stu-id="76cab-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="76cab-112">Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da grade de rastrexo.</span><span class="sxs-lookup"><span data-stu-id="76cab-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="76cab-113">Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, estes campos actualízanse a **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="76cab-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="76cab-114">Cando o calendario e a varianza de custos para o nó raíz son negativos, estes campos configúranse en **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="76cab-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
