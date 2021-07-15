---
title: Integración de Microsoft Project Client
description: Planificar e manter un programa de proxectos pode ser complexo, polo que os xestores de proxectos precisan empregar ferramentas que os axuden a xestionar esta tarefa. A integración con Microsoft Project Client proporciona apoio para abrir e xestionar unha estrutura de subdivisión do traballo do proxecto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269833"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="d4314-104">Integración de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d4314-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4314-105">Planificar e manter un programa de proxectos pode ser complexo, polo que os xestores de proxectos precisan empregar ferramentas que os axuden a xestionar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="d4314-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="d4314-106">A integración con Microsoft Project Client proporciona apoio para abrir e xestionar unha estrutura de subdivisión do traballo do proxecto.</span><span class="sxs-lookup"><span data-stu-id="d4314-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="d4314-107">O xestor do proxecto pode publicar os cambios de novo na estrutura de subdivisión do traballo do proxecto de Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="d4314-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="d4314-108">Se está a usar a actualización de xullo (versión 10.0.4), debe instalar KB 4054797 e 4055884.</span><span class="sxs-lookup"><span data-stu-id="d4314-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="d4314-109">Configurar o suplemento Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d4314-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="d4314-110">Para activar a integración con Microsoft Project Client, é necesario instalar o suplemento Microsoft Dynamics 365 na aplicación Microsoft Project do cliente do usuario.</span><span class="sxs-lookup"><span data-stu-id="d4314-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="d4314-111">Isto faise abrindo o **espazo de traballo de xestión de proxectos**.</span><span class="sxs-lookup"><span data-stu-id="d4314-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="d4314-112">• Prema **Configurar o suplemento do cliente do proxecto** desde a sección **Ligazóns** > **Configuración** da área de traballo.</span><span class="sxs-lookup"><span data-stu-id="d4314-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="d4314-113">• Prema **Abrir** e, a seguir, prema **Executar** cando se lle solicite.</span><span class="sxs-lookup"><span data-stu-id="d4314-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="d4314-114">Abrir e editar un borrador de estrutura de subdivisión do traballo existente en Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d4314-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="d4314-115">Se un proxecto en Dynamics 365 Finance xa ten unha estrutura de subdivisión do traballo creada, a estrutura de subdivisión do traballo pódese abrir na aplicación Microsoft Project Client se a estrutura de subdivisión de traballo está nun estado de borrador.</span><span class="sxs-lookup"><span data-stu-id="d4314-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="d4314-116">Para abrir desde a páxina **Proxecto**, prema a ligazón **Abrir en Microsoft Project** desde o separador **Planificar**. Esta páxina tamén se pode abrir desde a aplicación Microsoft Project Client premendo **Abrir** no separador **Microsoft Dynamics 365**. Seleccione **Persoa xurídica** e **Proxecto** na lista.</span><span class="sxs-lookup"><span data-stu-id="d4314-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="d4314-117">Se está a usar Internet Explorer como explorador, terá que premer **Gardar** para abrir manualmente desde a localización á que se descargou o ficheiro.</span><span class="sxs-lookup"><span data-stu-id="d4314-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="d4314-118">Ou prema **Gardar e abrir** para abrir o ficheiro en Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d4314-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="d4314-119">Non cambie o nome do ficheiro cando o garde.</span><span class="sxs-lookup"><span data-stu-id="d4314-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="d4314-120">Antes de facer ningunha edición no ficheiro usando Microsoft Project Client, debe comprobalo. Prema **Comprobar** no separador **Microsoft Dynamics 365**. Isto evitará que outros usuarios editen a estrutura de subdivisión do traballo desde Finanzas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d4314-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="d4314-121">Para publicar a estrutura de subdivisión do traballo despois de completar as edicións, prema **Rexistrar** no separador **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="d4314-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="d4314-122">Se un equipo do proxecto xa se engadiu ao proxecto en Finanzas, a lista de recursos encherase cos membros do equipo.</span><span class="sxs-lookup"><span data-stu-id="d4314-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="d4314-123">Se aínda non se engadiu un equipo de proxecto ao proxecto, pode seleccionar recursos e crear o equipo dentro de Microsoft Project Client premendo o botón **Recursos** no separador **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="d4314-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="d4314-124">Os seguintes datos sincronizaranse de novo con Finanzas como parte do proceso de rexistro:</span><span class="sxs-lookup"><span data-stu-id="d4314-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="d4314-125">•   Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="d4314-125">•   Task name</span></span>

<span data-ttu-id="d4314-126">•   Data de inicio</span><span class="sxs-lookup"><span data-stu-id="d4314-126">•   Start date</span></span>

<span data-ttu-id="d4314-127">•   Data de finalización</span><span class="sxs-lookup"><span data-stu-id="d4314-127">•   Finish date</span></span>

<span data-ttu-id="d4314-128">•   Predecesores</span><span class="sxs-lookup"><span data-stu-id="d4314-128">•   Predecessors</span></span>

<span data-ttu-id="d4314-129">•   Nomes de recursos</span><span class="sxs-lookup"><span data-stu-id="d4314-129">•   Resource names</span></span>

<span data-ttu-id="d4314-130">•   Categoría</span><span class="sxs-lookup"><span data-stu-id="d4314-130">•   Category</span></span>

<span data-ttu-id="d4314-131">•   Categoría do recurso</span><span class="sxs-lookup"><span data-stu-id="d4314-131">•   Resource category</span></span>

<span data-ttu-id="d4314-132">•   Horas laborables</span><span class="sxs-lookup"><span data-stu-id="d4314-132">•   Work hours</span></span>

<span data-ttu-id="d4314-133">•   Notas</span><span class="sxs-lookup"><span data-stu-id="d4314-133">•   Notes</span></span>

<span data-ttu-id="d4314-134">•   Prioridade</span><span class="sxs-lookup"><span data-stu-id="d4314-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="d4314-135">Se engade outras columnas ao seu ficheiro de Microsoft Project Client, non se gardarán no ficheiro e non se amosarán cando se abra de novo o ficheiro.</span><span class="sxs-lookup"><span data-stu-id="d4314-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="d4314-136">Crear a estrutura de subdivisión do traballo para un proxecto existente usando Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d4314-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="d4314-137">Para crear unha nova estrutura de subdivisión do traballo usando Microsoft Project Client, siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="d4314-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="d4314-138">Abra Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d4314-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d4314-139">No separador **Microsoft Dynamics 365**, prema **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="d4314-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="d4314-140">Seleccione a **Persoa xurídica** para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="d4314-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="d4314-141">Seleccione o **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="d4314-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="d4314-142">Prema **Consultar** no separ **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="d4314-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="d4314-143">Cando estea listo para publicalo en Finanzas, prema **Rexistrar** no separador **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="d4314-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="d4314-144">Substituír a estrutura de subdivisión do traballo existente para un proxecto existente usando Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d4314-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="d4314-145">Para crear unha nova estrutura de subdivisión do traballo usando Microsoft Project Client e substituír unha estrutura de subdivisión do traballo existente por un proxecto existente, siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="d4314-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="d4314-146">Abra Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d4314-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d4314-147">Crear o programa en Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d4314-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="d4314-148">No separador **Microsoft Dynamics 365**, prema **Gardar cambios** > **Substituír o proxecto existente**.</span><span class="sxs-lookup"><span data-stu-id="d4314-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="d4314-149">Seleccione a **Persoa xurídica** para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="d4314-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="d4314-150">Seleccione o **Proxecto**.</span><span class="sxs-lookup"><span data-stu-id="d4314-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="d4314-151">Prema **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d4314-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="d4314-152">Crear un novo proxecto desde dentro de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d4314-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="d4314-153">Abra Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d4314-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d4314-154">Crear o programa en Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d4314-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="d4314-155">No separador **Microsoft Dynamics 365**, prema **Gardar cambios** > **Gardar a novo proxecto**.</span><span class="sxs-lookup"><span data-stu-id="d4314-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="d4314-156">Seleccione a **Persoa xurídica** para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="d4314-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="d4314-157">Introduza o **ID do proxecto**, se é necesario.</span><span class="sxs-lookup"><span data-stu-id="d4314-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="d4314-158">Introduza o **nome de proxecto**.</span><span class="sxs-lookup"><span data-stu-id="d4314-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="d4314-159">Seleccione o **Tipo de proxecto**, **Grupo do proxecto** e o **ID do contrato do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="d4314-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="d4314-160">Como alternativa, pode crear un novo contrato de proxecto premendo **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d4314-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="d4314-161">Seleccione o **Calendario** que se usará para os recursos.</span><span class="sxs-lookup"><span data-stu-id="d4314-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="d4314-162">Prema en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d4314-162">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d4314-163">O complemento Project Client non admite os seguintes caracteres no formato de ID do proxecto:</span><span class="sxs-lookup"><span data-stu-id="d4314-163">The Project Client add-in doesn’t support the following characters in the project ID format:</span></span>
> 
>   - <span data-ttu-id="d4314-164">Guión baixo</span><span class="sxs-lookup"><span data-stu-id="d4314-164">Underscore</span></span>
>   - <span data-ttu-id="d4314-165">Punto</span><span class="sxs-lookup"><span data-stu-id="d4314-165">Period</span></span>
>   - <span data-ttu-id="d4314-166">Barra espazadora</span><span class="sxs-lookup"><span data-stu-id="d4314-166">Space</span></span>
>   - <span data-ttu-id="d4314-167">Barra</span><span class="sxs-lookup"><span data-stu-id="d4314-167">Slash</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
