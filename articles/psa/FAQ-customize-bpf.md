---
title: Como podo personalizar o fluxo do proceso de negocio nas fases do proxecto?
description: Unha visión xeral de como personalizar o fluxo do proceso de negocio de Project Stages.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993144"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="69d51-103">Como podo personalizar o fluxo do proceso de negocio nas fases do proxecto?</span><span class="sxs-lookup"><span data-stu-id="69d51-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="69d51-104">Existe unha limitación coñecida en versións anteriores da aplicación Project Service que consiste en que os nomes das fases no fluxo do proceso de negocio de fases dos proxecto deben coincidir exactamente cos nomes en inglés previstos (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="69d51-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="69d51-105">En caso contrario, a lóxica empresarial, que depende dos nomes de fase en inglés, non funciona conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="69d51-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="69d51-106">Por eso non ve accións familiares como **Mudar proceso** ou **Editar proceso** dispoñibles no formulario do proxecto, e non se recomienda a personalización do fluxo do proceso de negocio.</span><span class="sxs-lookup"><span data-stu-id="69d51-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="69d51-107">Esta limitación abordouse na versión 2.4.5.48 e posteriores.</span><span class="sxs-lookup"><span data-stu-id="69d51-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="69d51-108">Este artigo suxire solucións para versións anteriores se ten que personalizar o fluxo do proceso de negocio para versións anteriores.</span><span class="sxs-lookup"><span data-stu-id="69d51-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="69d51-109">A lóxica empresarial require unha coincidencia exacta cos nomes de fase en inglés.</span><span class="sxs-lookup"><span data-stu-id="69d51-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="69d51-110">O fluxo do proceso de negocio de fases dos proxecto inclúe unha lóxica empresarial que dirixe os comportamentos seguintes na aplicación:</span><span class="sxs-lookup"><span data-stu-id="69d51-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="69d51-111">Cando o proxecto está asociada a unha oferta, o código define o fluxo do proceso de negocio á fase **Quote**.</span><span class="sxs-lookup"><span data-stu-id="69d51-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="69d51-112">Cando o proxecto está asociada a un contrato, o código define o fluxo do proceso de negocio á fase **Plan**.</span><span class="sxs-lookup"><span data-stu-id="69d51-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="69d51-113">Cando o fluxo do proceso de negocio avanza á fase **Close**, o rexistro de proxecto está desactivado.</span><span class="sxs-lookup"><span data-stu-id="69d51-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="69d51-114">Cando o proxecto se desactiva, o formulario de proxecto e a estrutura de subdivisión do traballo (WBS) están definidas a só lectura, libéranse as reservas de recursos denominados e as listas de prezos asociadas desactívanse.</span><span class="sxs-lookup"><span data-stu-id="69d51-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="69d51-115">Esta lóxica empresarial depende dos nomes en inglés para as fases do proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="69d51-116">Este dependencia nos nomes de fase en inglés é o principal motivo polo que non se recomenda a personalización do fluxo do proceso de negocio nas fases do proxecto, e tamén pola que non ve accións de fluxo do proceso de negocio como **Cambiar proceso** ou **Editar proceso** na entidade do proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="69d51-117">Que ocorre se os nomes de fase non coinciden cos nomes en inglés?</span><span class="sxs-lookup"><span data-stu-id="69d51-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="69d51-118">Na versión da aplicación Project Service 1.x na plataforma 8.2, cando os nomes de fase do fluxo do proceso de negocio non coinciden cos nomes de fase en inglés exactamente, omítese a lóxica do negocio que define a fase correcta de ofertas ou contratos, ou que pecha o proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="69d51-119">Non se mostra ningunha mensaxe de erro.</span><span class="sxs-lookup"><span data-stu-id="69d51-119">No error messages are displayed.</span></span> <span data-ttu-id="69d51-120">Por tanto parece que pode personalizar o fluxo do proceso de negocio das fases do proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="69d51-121">No entanto, non verá ningún dos procesos automáticos que funcionan con ofertas, contratos, e pechar proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="69d51-122">Na versión da aplicación Project Service 2.4.4.30 ou anterior na plataforma 9.0, houbo un cambio arquitectónico considerable no fluxo do proceso de negocio que requeríu unha reescritura la lóxica empresarial do fluxo do proceso de negocio.</span><span class="sxs-lookup"><span data-stu-id="69d51-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="69d51-123">Como resultado, se os nomes de fase de proceso non coinciden cos nomes en inglés previstos, recibirá unha mensaxe de erro.</span><span class="sxs-lookup"><span data-stu-id="69d51-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="69d51-124">Por tanto, se desexa personalizar o fluxo do proceso de negocio de fases de proxecto para a entidade de proxecto, só pode engadir fases novas para o fluxo do proceso de negocio predefinido para a entidade de proxecto, mantendo as fases **Quote**, **Plan** e **Close** tal cual.</span><span class="sxs-lookup"><span data-stu-id="69d51-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="69d51-125">Esta restrición garante que non reciba erros da lóxica empresarial que esperen os nomes de fase no fluxo do proceso de negocio en inglés.</span><span class="sxs-lookup"><span data-stu-id="69d51-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="69d51-126">Na versión 2.4.5.48 ou posteriores, a lóxica empresarial descrita neste artigo eliminouse do fluxo do proceso de negocio predefinido para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="69d51-127">Actualizar a esa versión ou posteriores permitiralle personalizar ou substituir o fluxo do proceso de negocio predefinido por un dos seus propios.</span><span class="sxs-lookup"><span data-stu-id="69d51-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="69d51-128">Solucións para versións anteriores:</span><span class="sxs-lookup"><span data-stu-id="69d51-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="69d51-129">Se actualizar non é unha opción, pode personalizar o fluxo do proceso de negocio das fases do proxecto para a entidade de proxecto dunha das seguintes dúas maneiras:</span><span class="sxs-lookup"><span data-stu-id="69d51-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="69d51-130">Engada fases adicionais á configuración predefinida, e manteña os nomes de fase en inglés para **Quote**, **Plan** e **Close**.</span><span class="sxs-lookup"><span data-stu-id="69d51-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Captura de engadir fases á configuración predefinida](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="69d51-132">Cree o seu propio fluxo do proceso de negocio e convirtao en fluxo do proceso de negocio principal para a entidade de proxecto, que lle permite ter os nomes de fase que desexe.</span><span class="sxs-lookup"><span data-stu-id="69d51-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="69d51-133">No entanto, se desexa utilizar as mesmas fases de proxecto estándar **Quote**, **Plan** e **Close**, ten que facer algunhas personalizacións alonxadas dos nomes de fase personalizados.</span><span class="sxs-lookup"><span data-stu-id="69d51-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="69d51-134">A lóxica máis complexa está no proceso de peche do proxecto, que pode activar simplemente desactivando o rexistro de proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Personalización de BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="69d51-136">Consideracións adicionais da versión da aplicación Project Service 2.4.4.30 ou anterior no plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="69d51-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="69d51-137">En Project Service 2.4.4.30 ou anterior na plataforma 9.0, cun fluxo do proceso de negocio personalizada, o campo **Nome da fase** na entidade do proxecto utilizado na gráfica **Proxecto por fase** e nas visualizacións de lista de proxecto non se actualiza porque está emparellado ao fluxo do proceso de negocio nas fases do proxecto.</span><span class="sxs-lookup"><span data-stu-id="69d51-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="69d51-138">Para solucionar este problema, siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="69d51-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="69d51-139">Engada un campo personalizado para capturar a fase de fluxo do proceso de negocio actual se actualiza cando o usuario avanza a través do fluxo do proceso de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="69d51-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="69d51-140">Modifique a gráfica **Proxecto por fase** para que funcione co seu campo personalizado en vez da configuración predefinida.</span><span class="sxs-lookup"><span data-stu-id="69d51-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="69d51-141">Pasos para crear o seu propio fluxo do proceso de negocio para a entidade de proxecto</span><span class="sxs-lookup"><span data-stu-id="69d51-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="69d51-142">Para crear o seu propio fluxo do proceso de negocio para a entidade de proxecto, faga o seguinte:</span><span class="sxs-lookup"><span data-stu-id="69d51-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="69d51-143">Vaia a **Configuración** > **Centro de procesos**.</span><span class="sxs-lookup"><span data-stu-id="69d51-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="69d51-144">Non copie o fluxo do proceso de negocio nas fases do proxecto, porque iso tamén copia a lóxica empresarial de Project Service.</span><span class="sxs-lookup"><span data-stu-id="69d51-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Crear proceso](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="69d51-146">Utilice o Deseñador de procesos para crear os nomes de fase que desexe.</span><span class="sxs-lookup"><span data-stu-id="69d51-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="69d51-147">Se desexa a mesma funcionalidade que as fases predefinidas para **Quote**, **Plan** e **Close**, ten que creala baseándose nos seus nomes de fase do fluxo do proceso de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="69d51-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Captura do Deseñador de procesos utilizado para personalizar BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="69d51-149">No Deseñador de procesos, prema **Ordenar fluxo do proceso** para que o fluxo do proceso de negocio personalizada sexa o principal para a entidade de proxecto movéndoo enriba do fluxo do proceso de negocio nas fases do proxecto á parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="69d51-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="69d51-150">Captura da utilización de Ordenar fluxo do proceso</span><span class="sxs-lookup"><span data-stu-id="69d51-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="69d51-151">Estes pasos aplícanse a aplicación Project Service 2.4.4.30 ou anterior na plataforma 9.0.</span><span class="sxs-lookup"><span data-stu-id="69d51-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="69d51-152">Engada un novo campo personalizado á entidade de proxecto para capturar fases personalizada no seu fluxo do proceso de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="69d51-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="69d51-153">Deberá engadir lóxica empresarial (complementos/fluxo de traballo) para actualizar este campo cando a fase do fluxo do proceso de negocio personalizado se actualice.</span><span class="sxs-lookup"><span data-stu-id="69d51-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Captura de personalizar entidades de proxecto](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="69d51-155">Modifique a gráfica **Proxecto por fase** para usar os seus novos campos personalizados para fases.</span><span class="sxs-lookup"><span data-stu-id="69d51-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Captura de utilizar a gráfica de Proxecto por fase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="69d51-157">Modifique as visualizacións para que a entidade de proxecto inclúa o seu novo campo personalizado para fases.</span><span class="sxs-lookup"><span data-stu-id="69d51-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Captura de modificación de visualizacións na entidade de proxecto](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]