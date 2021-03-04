---
title: Modelos de habilidades e competencias
description: Este tema ofrece información sobre como usar os modelos de habilidades e competencias.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: c7da8b2a7eda51b2aa7cf04e325a92f33d834efc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147471"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="30de5-103">Modelos de habilidades e competencias</span><span class="sxs-lookup"><span data-stu-id="30de5-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="30de5-104">As habilidades son características dos recursos que se comparten entre Dynamics 365 Project Service Automation e, se está presente, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="30de5-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="30de5-105">Para manter o repositorio de habilidades en Project Service Automation, diríxase a **Recursos** \> **Habilidades dos recursos**.</span><span class="sxs-lookup"><span data-stu-id="30de5-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Habilidades dos recursos](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="30de5-107">Usar modelos de habilidade para valorar os recursos</span><span class="sxs-lookup"><span data-stu-id="30de5-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="30de5-108">As habilidades dos recursos clasifícanse por modelos de competencia.</span><span class="sxs-lookup"><span data-stu-id="30de5-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="30de5-109">As clasificacións individuais están nun modelo de competencia.</span><span class="sxs-lookup"><span data-stu-id="30de5-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="30de5-110">Para crear un modelo de competencia, vaia a **Recursos** \> **Modelos de competencia** e logo seleccione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="30de5-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="30de5-111">No novo modelo de clasificación, especifique o valor mínimo de clasificación, o valor máximo de clasificación e a entidade que se está clasificando.</span><span class="sxs-lookup"><span data-stu-id="30de5-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="30de5-112">Na subgrade **Valores de clasificación**, pode definir os diferentes valores de clasificación, desde o mínimo ata o máximo.</span><span class="sxs-lookup"><span data-stu-id="30de5-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definición de clasificación mínima e máxima](media/Resource-Management-image85.png)

<span data-ttu-id="30de5-114">Estes valores de clasificación móstranse nos filtros **Requisitos dos recursos**, **Panel de programación** e **Asistente de programación**.</span><span class="sxs-lookup"><span data-stu-id="30de5-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
