---
title: Configurar a integración Project Operations por entidade legal
description: Este tema ofrece información sobre como configurar a integración por entidade legal en Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000074"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="a3b5b-103">Configurar a integración Project Operations por entidade legal</span><span class="sxs-lookup"><span data-stu-id="a3b5b-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="a3b5b-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="a3b5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a3b5b-105">Este tema guíalle polos pasos necesarios para configurar Dynamics 365 Project Operations por entidade legal.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="a3b5b-106">Activar claves de funcionalidade en Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="a3b5b-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="a3b5b-107">Complete os seguintes pasos para activar as funcionalidades requiridas.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="a3b5b-108">En Dynamics 365 Finance, vaia á área de traballo **Xestión de funcionalidades**.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="a3b5b-109">En **Lista de funcionalidades**, busque e active as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="a3b5b-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="a3b5b-110">**Activar varias liñas de contrato para un proxecto**</span><span class="sxs-lookup"><span data-stu-id="a3b5b-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="a3b5b-111">**Activar Project Operations en Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="a3b5b-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="a3b5b-112">Se non ve as **Claves de funcionalidade** na lista, verifique que a súa versión de Finance cumpra o requisito mínimo de versión (versión da aplicación 10.0.13 con todas as actualizacións de calidade aplicadas ou superior).</span><span class="sxs-lookup"><span data-stu-id="a3b5b-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="a3b5b-113">Seleccione **Comprobar se hai actualizacións** para actualizar a lista de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="a3b5b-114">Definir o escenario de despregamento de Project Operations para unha entidade legal</span><span class="sxs-lookup"><span data-stu-id="a3b5b-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="a3b5b-115">Pode activar Project Operationes en Dynamics 365 Customer Engagement a nivel de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="a3b5b-116">Pode ter unha entidade legal usando Project Operations en Dynamics 365 Customer Engagement para escenarios baseados en recursos/sen fornecemento.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="a3b5b-117">No mesmo ambiente, pode ter outra entidade legal que empregue Project Operations para escenarios de de produción/con fornecemento.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="a3b5b-118">En Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Configuración** > **Parámetros globais de Xestión e contabilidade de proxectos**.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="a3b5b-119">Na lista de entidades legais dispoñibles, seleccione as entidades onde hai varias liñas de contrato e activaranse as funcionalidades de Project Operationes en Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="a3b5b-120">Deixa sen seleccionar as entidades legais que empregarán Project Operations para escenarios de produción/con fornecemento.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="a3b5b-121">Só se pode seleccionar unha entidade legal se non ten ningún proxecto existente.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="a3b5b-122">Configurar os parámetros de Xestión e contabilidade de proxectos</span><span class="sxs-lookup"><span data-stu-id="a3b5b-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="a3b5b-123">Cada entidade legal que usa Projecto Operations en Dynamics 365 Customer Engagement precisa dun conxunto de parámetros predefinidos.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="a3b5b-124">Estes parámetros configúranse no separador **Projecto Operations** na páxina **Parámetros de Xestión e contabilidade de proxectos**.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="a3b5b-125">Os parámetros son:</span><span class="sxs-lookup"><span data-stu-id="a3b5b-125">The parameters are:</span></span>

  - <span data-ttu-id="a3b5b-126">**Valores predefinidos do tipo de facturación**: Project Operations emprega un conxunto fixo de valores predefinidos do tipo de facturación que se deben atribuñir ás propiedades de liña de Finance.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="a3b5b-127">Cree un rexistro para cada tipo de facturación: **Non especificado**, **Imputable**, **Non imputable**, **Gratuíto** e **Non dispoñible**.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="a3b5b-128">**Valores predefinidos de categoría de proxecto**: Seleccione as categorías de proxecto predefinidas que se empregarán para cada tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="a3b5b-129">Estes valores predefinidos utilizaranse no **Diario de integración de Project Operations** e nas estimacións onde non se especifica ningunha categoría de transacción para o datos real do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="a3b5b-130">**Previsións**: Seleccione o modelo de previsión que se utilizará para estimacións de tempo e gastos.</span><span class="sxs-lookup"><span data-stu-id="a3b5b-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]