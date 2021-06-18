---
title: Modelos de habilidades e competencias
description: Este tema ofrece información sobre como usar os modelos de habilidades e competencias.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008669"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="3caec-103">Modelos de habilidades e competencias</span><span class="sxs-lookup"><span data-stu-id="3caec-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3caec-104">As habilidades son características dos recursos que se comparten entre Dynamics 365 Project Service Automation e, se está presente, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="3caec-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="3caec-105">Para manter o repositorio de habilidades en Project Service Automation, diríxase a **Recursos** \> **Habilidades dos recursos**.</span><span class="sxs-lookup"><span data-stu-id="3caec-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Habilidades dos recursos](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="3caec-107">Usar modelos de habilidade para valorar os recursos</span><span class="sxs-lookup"><span data-stu-id="3caec-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="3caec-108">As habilidades dos recursos clasifícanse por modelos de competencia.</span><span class="sxs-lookup"><span data-stu-id="3caec-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="3caec-109">As clasificacións individuais están nun modelo de competencia.</span><span class="sxs-lookup"><span data-stu-id="3caec-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="3caec-110">Para crear un modelo de competencia, vaia a **Recursos** \> **Modelos de competencia** e logo seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="3caec-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="3caec-111">No novo modelo de clasificación, especifique o valor mínimo de clasificación, o valor máximo de clasificación e a entidade que se está clasificando.</span><span class="sxs-lookup"><span data-stu-id="3caec-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="3caec-112">Na subgrade **Valores de clasificación**, pode definir os diferentes valores de clasificación, desde o mínimo ata o máximo.</span><span class="sxs-lookup"><span data-stu-id="3caec-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definición de clasificación mínima e máxima](media/Resource-Management-image85.png)

<span data-ttu-id="3caec-114">Estes valores de clasificación móstranse nos filtros **Requisitos dos recursos**, **Panel de programación** e **Asistente de programación**.</span><span class="sxs-lookup"><span data-stu-id="3caec-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]