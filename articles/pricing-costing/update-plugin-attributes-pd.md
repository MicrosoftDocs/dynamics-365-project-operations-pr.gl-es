---
title: Actualizar os atributos do complemento con novas dimensións de prezos
description: Este tema fornece información sobre como actualizar os atributos do complemento para as dimensións de prezos.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274681"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="3a69b-103">Actualizar os atributos do complemento con novas dimensións de prezos</span><span class="sxs-lookup"><span data-stu-id="3a69b-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="3a69b-104">Este tema fornece información sobre como actualizar os atributos do complemento para as dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="3a69b-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="3a69b-105">Este tema só é aplicable ás funcionalidades de oferta e contrato en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3a69b-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3a69b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a69b-106">Prerequisites</span></span>
<span data-ttu-id="3a69b-107">Antes de completar os pasos deste tema, debe ter completado os procedementos dos seguintes temas:</span><span class="sxs-lookup"><span data-stu-id="3a69b-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="3a69b-108">Crear campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="3a69b-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="3a69b-109">Engadir campos personalizados á configuración de prezos e ás entidades transaccionais </span><span class="sxs-lookup"><span data-stu-id="3a69b-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="3a69b-110">[Configurar campos personalizados como dimensións de prezos](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="3a69b-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="3a69b-111">Se non completou eses procedementos, compléteos e despois volva a este tema.</span><span class="sxs-lookup"><span data-stu-id="3a69b-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="3a69b-112">Rexistrar un complemento</span><span class="sxs-lookup"><span data-stu-id="3a69b-112">Register a plug-in</span></span>
<span data-ttu-id="3a69b-113">Cando se crea un detalle de liña de oferta na páxina **Liña de oferta** dunha liña de oferta do proxecto, o sistema crea dúas liñas de estimación.</span><span class="sxs-lookup"><span data-stu-id="3a69b-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="3a69b-114">Unha liña é para o lado de custo da estimación e a outra liña é para o lado de vendas.</span><span class="sxs-lookup"><span data-stu-id="3a69b-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="3a69b-115">Isto é o mesmo para as liñas de contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="3a69b-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3a69b-116">Cando faga unha modificación da cantidade ou dun campo do lado do custo, este cambio farase tamén no lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="3a69b-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="3a69b-117">Isto é posible porque os complementos PreOperation de Quotelinedetail e as entidades de detalle de liña de contrato conectan atributos específicos do lado do custo co lado de vendas da transacción.</span><span class="sxs-lookup"><span data-stu-id="3a69b-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="3a69b-118">Se precisa que se fagan cambios nos valores das dimensións de prezos do lado de vendas tamén no lado do custo, deberán volver rexistrarse os seguintes complementos despois de facer cambios na dimensión de prezos.</span><span class="sxs-lookup"><span data-stu-id="3a69b-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="3a69b-119">Estes son os complementos para actualizar e volver rexistrar:</span><span class="sxs-lookup"><span data-stu-id="3a69b-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="3a69b-120">PreOperationContractLineDetailUpdate - **Actualiza msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3a69b-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="3a69b-121">PreOperationQuoteLineDetailUpdate - **Actualiza msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3a69b-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="3a69b-122">Complete os seguintes pasos para actualizar e volver rexistrar os complementos.</span><span class="sxs-lookup"><span data-stu-id="3a69b-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="3a69b-123">Abra **PluginRegistrationTool** e conécteo ao seu ambiente de Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3a69b-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="3a69b-124">Seleccione **Buscar** e escriba as primeiras letras do complemento que se vai actualizar.</span><span class="sxs-lookup"><span data-stu-id="3a69b-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="3a69b-125">Despois de atopar o complemento, seleccióneo e logo seleccione **Seleccionar en formulario principal**.</span><span class="sxs-lookup"><span data-stu-id="3a69b-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="3a69b-126">Seleccione o paso **Update msdyn_orderlinetransaction**, prema co botón dereito e logo seleccione **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="3a69b-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="3a69b-127">Na páxina de diálogo **Actualizar**, seleccione os puntos suspensivos (**...**) nos atributos de filtrado.</span><span class="sxs-lookup"><span data-stu-id="3a69b-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="3a69b-128">Ábrese a ventá de atributos de filtrado e ofrece unha lista de todos os atributos da entidade e as dimensións de prezos.</span><span class="sxs-lookup"><span data-stu-id="3a69b-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="3a69b-129">Marque as caixas de verificación dos atributos de dimensión de prezos.</span><span class="sxs-lookup"><span data-stu-id="3a69b-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="3a69b-130">Seleccione **Aceptar** para pechar a páxina e logo seleccione **Actualizar paso**.</span><span class="sxs-lookup"><span data-stu-id="3a69b-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="3a69b-131">Repita os pasos do 2 ao 7 para o segundo complemento, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="3a69b-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="3a69b-132">Para este complemento, debe actualizar o paso **Actualización de msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3a69b-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="3a69b-133">Peche **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="3a69b-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]