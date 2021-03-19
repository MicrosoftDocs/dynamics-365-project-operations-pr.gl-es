---
title: Configurar axustes de parámetros adicionais
description: Como configurar os parámetros adicionais en Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290762"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="0d8cc-103">Configurar os parámetros adicionais (Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="0d8cc-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0d8cc-104">Vez vez configurados os elementos dos temas anterior, debe definir parámetros adicionais de proxecto para usar cos seus proxectos.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="0d8cc-105">Ao instalar por primeira vez [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], creou unha configuración de parámetros para crear por primeira vez todos os rexistros necesarios para que [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] funcione.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="0d8cc-106">Agora é hora de volver e configurar campos adicionais para esta configuración.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="0d8cc-107">Terá que ter configurados os seguintes axustes:</span><span class="sxs-lookup"><span data-stu-id="0d8cc-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="0d8cc-108">Unidade organizativa</span><span class="sxs-lookup"><span data-stu-id="0d8cc-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="0d8cc-109">Frecuencia das facturas</span><span class="sxs-lookup"><span data-stu-id="0d8cc-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="0d8cc-110">Modelos de horas laborables</span><span class="sxs-lookup"><span data-stu-id="0d8cc-110">Work hours template</span></span>  
  
-   <span data-ttu-id="0d8cc-111">Lista de prezos</span><span class="sxs-lookup"><span data-stu-id="0d8cc-111">Price list</span></span>  
 
<span data-ttu-id="0d8cc-112">Neste paso tamén indicará que tipo de atribución de recurso desexa:</span><span class="sxs-lookup"><span data-stu-id="0d8cc-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="0d8cc-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-113">**Central**.</span></span> <span data-ttu-id="0d8cc-114">Só os xestores de recursos poden atribuír recursos a proxectos.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="0d8cc-115">**Híbrido**.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-115">**Hybrid**.</span></span> <span data-ttu-id="0d8cc-116">Os xestores de recursos, os xestores de proxectos e os xestores de contas poden atribuír recursos a proxectos.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="0d8cc-117">Para definir parámetros do proxecto:</span><span class="sxs-lookup"><span data-stu-id="0d8cc-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="0d8cc-118">Vaia a **Project Service > Parámetros**</span><span class="sxs-lookup"><span data-stu-id="0d8cc-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="0d8cc-119">Prema na configuración de parámetros que desexa configurar (a que creou cando instalou por primeira vez [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), ou prema **Nova** para crear unha nova.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="0d8cc-120">Na área **Xeral**, defina todas as opcións para os parámetros do proxecto.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="0d8cc-121">Na área **Lista de prezos**, prema en **+** para engadir unha lista de prezos, seleccione unha lista de prezos na lista despregable **Lista de prezos dos parámetros do proxecto** e, a seguir, prema **Gardar**.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="0d8cc-122">Prema no botón **Gardar** na parte inferior dereita da pantalla.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="0d8cc-123">Debe manterse o rexistro de parámetros do proxecto para que Project Service funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="0d8cc-124">Non se debería eliminar este rexistro.</span><span class="sxs-lookup"><span data-stu-id="0d8cc-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="0d8cc-125">Consulte tamén</span><span class="sxs-lookup"><span data-stu-id="0d8cc-125">See Also</span></span>  
 [<span data-ttu-id="0d8cc-126">Configurar recursos reservables</span><span class="sxs-lookup"><span data-stu-id="0d8cc-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]