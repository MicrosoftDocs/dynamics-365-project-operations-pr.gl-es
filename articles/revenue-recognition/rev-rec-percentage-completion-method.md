---
title: Proxectos de estimación de ingresos a prezo fixo
description: Este tema fornece información sobre os ingresos a prezo fixo en proxectos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013799"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="b9cae-103">Proxectos de estimación de ingresos a prezo fixo</span><span class="sxs-lookup"><span data-stu-id="b9cae-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="b9cae-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="b9cae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b9cae-105">Cando crea unha liña de contrato de proxecto cos seguintes atributos en Dynamics 365 Project Operations en Microsoft Dataverse, o sistema crea automaticamente un proxecto de estimación de ingresos a prezo fixo.</span><span class="sxs-lookup"><span data-stu-id="b9cae-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="b9cae-106">A información deste proxecto baséase no seguinte:</span><span class="sxs-lookup"><span data-stu-id="b9cae-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="b9cae-107">Un método de facturación a prezo fixo.</span><span class="sxs-lookup"><span data-stu-id="b9cae-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="b9cae-108">Un proxecto asociado.</span><span class="sxs-lookup"><span data-stu-id="b9cae-108">An associated project.</span></span>
  - <span data-ttu-id="b9cae-109">Polo menos un fito definido no separador **Programación de facturas** na páxina **Liña de contrato do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="b9cae-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="b9cae-110">Revisar proxectos de estimacións de ingresos a prezo fixo</span><span class="sxs-lookup"><span data-stu-id="b9cae-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="b9cae-111">Para revisar os proxectos de estimación de ingresos a prezo fixo, complete os seguintes pasos:</span><span class="sxs-lookup"><span data-stu-id="b9cae-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="b9cae-112">No ambiente de Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Proxectos de estimación de ingresos a prezo fixo**.</span><span class="sxs-lookup"><span data-stu-id="b9cae-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="b9cae-113">Seleccione o proxecto que desexa ver e prema dúas veces en **ID do proxecto de estimación** para abrir o rexistro e revisar os detalles do proxecto.</span><span class="sxs-lookup"><span data-stu-id="b9cae-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="b9cae-114">Expanda o separador **Proxecto**. Verá un proxecto na grade **Proxectos seleccionados**.</span><span class="sxs-lookup"><span data-stu-id="b9cae-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="b9cae-115">O sistema usa isto como proxecto predefinido porque é o proxecto asociado á liña de contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="b9cae-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="b9cae-116">Para cambiar a asociación, seleccione proxectos adicionais e engádaos á grade **Proxectos seleccionados**.</span><span class="sxs-lookup"><span data-stu-id="b9cae-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="b9cae-117">Se se seleccionan varios proxectos nesta grade, a porcentaxe de finalización do proxecto e as estimacións de ingresos calcúlanse conxuntamente para todos os proxectos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="b9cae-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="b9cae-118">O custo do proxecto, o perfil de ingresos, o modelo de custo e o código do período pódense configurar manualmente.</span><span class="sxs-lookup"><span data-stu-id="b9cae-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="b9cae-119">Se non se configuran manualmente, os valores son os predefinidos durante o primeiro cálculo de estimación do proxecto empregando as regras configuradas para os perfís de custos e ingresos do proxecto.</span><span class="sxs-lookup"><span data-stu-id="b9cae-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]