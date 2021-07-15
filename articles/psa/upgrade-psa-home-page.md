---
title: Actualizar a páxina de inicio
description: Este tema mostra onde atopar información importante sobre as funcións novas e modificadas en Dynamics 365 Project Service Automation e o proceso para actualizar á versión máis recente.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8fc820d8fa0e421cdc963f391133e7311de96982
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368519"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="75bff-103">Actualizar a páxina de inicio</span><span class="sxs-lookup"><span data-stu-id="75bff-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="75bff-104">Actualizar da versión 2.x ou 1.x á versión 3.x de PSA</span><span class="sxs-lookup"><span data-stu-id="75bff-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="75bff-105">Novas instancias</span><span class="sxs-lookup"><span data-stu-id="75bff-105">New instances</span></span>

<span data-ttu-id="75bff-106">A partir do 17 de maio de 2019, cando se selecciona Project Service Automation durante a subministración dunha nova instancia, a versión 3.x instálase por defecto.</span><span class="sxs-lookup"><span data-stu-id="75bff-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="75bff-107">Instancias existentes</span><span class="sxs-lookup"><span data-stu-id="75bff-107">Existing instances</span></span>

<span data-ttu-id="75bff-108">Anteriormente, os clientes que tiñan unha instancia da versión 2.x de PSA e necesitaban actualizar á versión 3.x, que é a versión de PSA baseada na interface de cliente unificada (UCI) de PSA, debían contactar co servizo de asistencia de Microsoft e proporcionar os detalles da súa instancia, de xeito que o servizo de asistencia podía habilitar a instancia para a actualización á versión 3.x.</span><span class="sxs-lookup"><span data-stu-id="75bff-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="75bff-109">A partir do 1 de marzo de 2020, os clientes que teñan unha instancia de PSA versión 2.x e necesiten actualizar á versión 3.x, poderán actualizar as súas instancias directamente desde o portal de administración sen ter que contactar coa asistencia técnica de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="75bff-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="75bff-110">A versión 3.x de PSA inclúe cambios significativos.</span><span class="sxs-lookup"><span data-stu-id="75bff-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="75bff-111">Foi creada no marco Interface unificada para axudar a proporcionar unha experiencia de usuario mellorada.</span><span class="sxs-lookup"><span data-stu-id="75bff-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="75bff-112">A aplicación rediseñada ofrece unha interface de usuario (IU) uniforme e segue principios de deseño sensibles para unha visualización óptima en calquera tamaño de pantalla ou dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75bff-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="75bff-113">Houbo outros cambios ao longo da aplicación.</span><span class="sxs-lookup"><span data-stu-id="75bff-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="75bff-114">Algunhas das áreas que foron modificadas inclúen fixación de prezos, reservas e atribución de recursos, tempo, gastos e aprobacións.</span><span class="sxs-lookup"><span data-stu-id="75bff-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="75bff-115">Antes de comezar o proceso de actualización, recomendámoslle que realice as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="75bff-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="75bff-116">Verifique se Dynamics 365 Field Service e Project Service Automation están instalados na instancia identificada.</span><span class="sxs-lookup"><span data-stu-id="75bff-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="75bff-117">Se se instalan ambas solucións, ten que planificar a actualización antes de continuar co uso regular da instancia.</span><span class="sxs-lookup"><span data-stu-id="75bff-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="75bff-118">Revise coidadosamente os seguintes temas.</span><span class="sxs-lookup"><span data-stu-id="75bff-118">Carefully review the following topics.</span></span> <span data-ttu-id="75bff-119">O coñecemento e a comprensión dos cambios entre versións axudaranlle co proceso de actualización.</span><span class="sxs-lookup"><span data-stu-id="75bff-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="75bff-120">Estes temas fornecen información sobre os cambios importantes en PSA, xunto con consideracións e recomendacións para planificar a súa actualización á versión 3.x.</span><span class="sxs-lookup"><span data-stu-id="75bff-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="75bff-121">Novidades ou cambios na versión 3 de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="75bff-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="75bff-122">Consideracións sobre a actualizaciñon - Project Service Automation versión 2.x ou 1.x a versión 3</span><span class="sxs-lookup"><span data-stu-id="75bff-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="75bff-123">Actualice a súa instancia de illamento de procesos para avaliar os cambios na súa instalación antes de actualizar a súa instancia de produción.</span><span class="sxs-lookup"><span data-stu-id="75bff-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="75bff-124">Despois de revisar os temas mencionados anteriormente e estar preparado para actualizar a PSA versión 3.x ou a versión baseada en UCI, envíe unha solicitude ao servizo de asistencia de Microsoft para que a actualización estea dispoñible desde o centro de administración.</span><span class="sxs-lookup"><span data-stu-id="75bff-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="75bff-125">Na súa solicitude, indique os detalles da súa instancia.</span><span class="sxs-lookup"><span data-stu-id="75bff-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="75bff-126">Versións máis antigas de PSA (versión PSA 2.x) nunha instancia de nova creación</span><span class="sxs-lookup"><span data-stu-id="75bff-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="75bff-127">A partir do 17 de maio de 2019, todas as novas instancias terán UCI como cliente predefinido.</span><span class="sxs-lookup"><span data-stu-id="75bff-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="75bff-128">Para o aliñamento con este cambio, PSA versión 3.x e Field Service versión 8.x subministraranse por defecto, porque estas versións están deseñadas para funcionar co cliente UCI.</span><span class="sxs-lookup"><span data-stu-id="75bff-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="75bff-129">A partir do 1 de marzo de 2020, os clientes de Dynamics PSA xa non poderán crear un novo ambiente con versións anteriores de PSA, por exemplo PSA versión 2.x ou inferior.</span><span class="sxs-lookup"><span data-stu-id="75bff-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="75bff-130">Calquera novo ambiente consistirá en obter só a versión 3.x de PSA.</span><span class="sxs-lookup"><span data-stu-id="75bff-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="75bff-131">Para obter a mellor experiencia cando usa versións máis antigas das aplicacións Field Service e PSA, vaia á páxina **Configuración do sistema** e para o campo **Usar a nova Interface unificada (recomendado)**, seleccione **Non** xa que estas versións non están deseñadas para cargarse correctamente en UCI.</span><span class="sxs-lookup"><span data-stu-id="75bff-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="75bff-132">Despois de desactivar UCI, pode abrir e executar estas versións de Field Service e PSA empregando o antigo cliente web.</span><span class="sxs-lookup"><span data-stu-id="75bff-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]