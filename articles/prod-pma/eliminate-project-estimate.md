---
title: Eliminar unha estimación de proxecto
description: Este tema ofrece información sobre como eliminar unha estimación do proxecto unha vez finalizado.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270676"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="b357a-103">Eliminar unha estimación de proxecto</span><span class="sxs-lookup"><span data-stu-id="b357a-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b357a-104">As estimacións de proxecto fornecen a visualización financeira para o traballo estimado e programado para un proxecto.</span><span class="sxs-lookup"><span data-stu-id="b357a-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="b357a-105">Para traballar con estimacións dun proxecto, debe anexalo a un proxecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="b357a-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="b357a-106">Un proxecto de estimación baséase sempre nun proxecto existente, pero moitos proxectos poden referirse a un único proxecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="b357a-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="b357a-107">Só se poden anexar proxectos de prezo fixo e de investimento para estimar proxectos, e estes proxectos deben pertencer ao mesmo grupo de proxectos que o proxecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="b357a-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="b357a-108">Para eliminar un proxecto de estimación, debe estar completo.</span><span class="sxs-lookup"><span data-stu-id="b357a-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="b357a-109">Os seguintes pasos explican como eliminar unha estimación.</span><span class="sxs-lookup"><span data-stu-id="b357a-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="b357a-110">Vaia a **Xestión e contabilidade de proxectos** > **Todos os proxectos** e abra o proxecto.</span><span class="sxs-lookup"><span data-stu-id="b357a-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="b357a-111">No separador **Xestionar**, seleccione **Estimacións** e na páxina **Estimación** seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="b357a-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="b357a-112">Na páxina **Eliminar estimación** no separador **Xeral**, configure as seguintes opcións:</span><span class="sxs-lookup"><span data-stu-id="b357a-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="b357a-113">**Código do período**: Seleccione o código do período para escoller os proxectos de estimación axeitados.</span><span class="sxs-lookup"><span data-stu-id="b357a-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="b357a-114">**Data da estimación**: Seleccione a data da estimación axeitada para a eliminación.</span><span class="sxs-lookup"><span data-stu-id="b357a-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="b357a-115">**Eliminar con advertencias de WIP**: Active esta opción para proporcionar unha notificación cando se elimine unha estimación asociada a un traballo en curso (WIP).</span><span class="sxs-lookup"><span data-stu-id="b357a-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="b357a-116">Cando esta opción non está activada, a eliminación non pode continuar se existen transaccións non estimadas.</span><span class="sxs-lookup"><span data-stu-id="b357a-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="b357a-117">Esta opción só está dispoñible cando se aplica a eliminación a un proxecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="b357a-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="b357a-118">Non está dispoñible se está a usar anotacións periódicas.</span><span class="sxs-lookup"><span data-stu-id="b357a-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="b357a-119">Esta configuración funciona coa configuración do separador **Estimación** na páxina **Parámetros do proxecto**, no grupo de campos **Permitir a eliminación cando existen transaccións non estimadas**.</span><span class="sxs-lookup"><span data-stu-id="b357a-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="b357a-120">**Establecer a fase como Finalizada**: Active esta opción para establecer a fase do proxecto de estimación en **Finalizada** despois de executar a eliminación.</span><span class="sxs-lookup"><span data-stu-id="b357a-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="b357a-121">**Imprimir lista de estimacións**: Seleccione a información que se incluirá cando se imprima a lista de estimacións.</span><span class="sxs-lookup"><span data-stu-id="b357a-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="b357a-122">**Mostrar Infolog**: Active esta opción para amosar o Infolog.</span><span class="sxs-lookup"><span data-stu-id="b357a-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="b357a-123">**Data de contabilización**: Elixa a data de contabilización no libro maior da estimación.</span><span class="sxs-lookup"><span data-stu-id="b357a-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="b357a-124">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b357a-124">Select **OK**.</span></span>
5. <span data-ttu-id="b357a-125">Despois de completar o proceso de eliminación, o proxecto de estimación eliminado móstrase cun valor negativo.</span><span class="sxs-lookup"><span data-stu-id="b357a-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="b357a-126">Se non pretendía eliminar unha estimación, pode seleccionar a estimación eliminada e seleccionar **Inverter eliminación**.</span><span class="sxs-lookup"><span data-stu-id="b357a-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]