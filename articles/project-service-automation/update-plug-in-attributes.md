---
title: Actualizar os atributos do complemento para incluír novas dimensións de prezos
description: Este tema fornece información sobre a actualización dos atributos do complemento para as dimensións de prezos.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751423"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="3966b-103">Actualizar os atributos do complemento para incluír novas dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="3966b-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="3966b-104">Se non está a usar as funcións de ofertas e contratación de Project Service Automation (PSA), pode omitir este tema.</span><span class="sxs-lookup"><span data-stu-id="3966b-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="3966b-105">Este tema asume que completou os procedementos nos temas [Crear campos e entidades personalizados](create-custom-fields-entities.md), [Engadir campos personalizados a configuración de prezos e entidades transaccionais](field-references.md) e [Configurar campos personalizados como dimensións de prezos](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="3966b-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="3966b-106">Se non completou eses procedementos, volva e compléteos e despois volva a este tema.</span><span class="sxs-lookup"><span data-stu-id="3966b-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="3966b-107">Cando se crea un detalle de liña de oferta na páxina **Liña de oferta** para unha liña de oferta do proxecto, o sistema crea dúas liñas de estimación en segundo plano: unha liña para o lado de custo da estimación e outra para o lado de vendas.</span><span class="sxs-lookup"><span data-stu-id="3966b-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="3966b-108">Isto é o mesmo para as liñas de contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="3966b-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3966b-109">Cando faga unha modificación da cantidade ou dun campo do lado do custo, este cambio propagarase ao lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="3966b-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="3966b-110">Isto é posible debido aos seguintes complementos que deben volver rexistrarse despois dun cambio nas dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="3966b-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="3966b-111">PreOperationContractLineDetailUpdate - Actualizacións **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3966b-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="3966b-112">PreOperationQuoteLineDetailUpdate - Actualizacións **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3966b-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="3966b-113">Os pasos seguintes explican o proceso de rexistro dos complementos.</span><span class="sxs-lookup"><span data-stu-id="3966b-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="3966b-114">Abra **PluginRegistrationTool** e conéctese á súa instancia en liña.</span><span class="sxs-lookup"><span data-stu-id="3966b-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="3966b-115">Prema **Buscar** e busque o complemento para actualizar.</span><span class="sxs-lookup"><span data-stu-id="3966b-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Captura de pantalla da árbore de busca](media/PRT-1.png)

3. <span data-ttu-id="3966b-117">Despois de atopar o complemento, seleccióneo e logo prema **Seleccionar en formulario principal**.</span><span class="sxs-lookup"><span data-stu-id="3966b-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="3966b-118">Seleccione o paso do complemento para actualizar, prema co botón dereito e logo seleccione **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="3966b-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Captura de pantalla do complemento para actualizar](media/PRT-2.png)
 
5. <span data-ttu-id="3966b-120">Na ventá de actualización, prema nos puntos suspensivos (**...**) nos atributos de filtrado.</span><span class="sxs-lookup"><span data-stu-id="3966b-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Captura de pantalla de información de configuración do paso existente Actualizar](media/PRT-3.png)
 
6. <span data-ttu-id="3966b-122">Seleccione as caixas de verificación do atributo de prezos</span><span class="sxs-lookup"><span data-stu-id="3966b-122">Select the pricing attribute check boxes.</span></span>

 ![Captura de pantalla que mostra a selección da caixa de verificación para os atributos de prezos](media/PRT-4.png)

7. <span data-ttu-id="3966b-124">Prema **Aceptar** para pechar a páxina e logo seleccione **Actualizar paso**.</span><span class="sxs-lookup"><span data-stu-id="3966b-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Captura de pantalla que mostra o botón "Actualizar paso"](media/PRT-5.png)
 
8. <span data-ttu-id="3966b-126">Repita este proceso para o segundo complemento, **PreOperationQuoteLineDetail - Actualización de msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3966b-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="3966b-127">Peche a ferramenta de rexistro de complementos.</span><span class="sxs-lookup"><span data-stu-id="3966b-127">Close the plug-in registration tool.</span></span>

