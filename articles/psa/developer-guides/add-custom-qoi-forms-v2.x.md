---
title: Engadir novos formularios de entidade personalizada (Project Service Automation 2.x)
description: Este tema fornece información sobre como engadir formularios de entidade personalizada para oportunidades, ofertas, pedidos ou facturas en Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007994"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="2e07d-103">Engadir novos formularios de entidade personalizada (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="2e07d-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="2e07d-104">Campo Tipo</span><span class="sxs-lookup"><span data-stu-id="2e07d-104">Type field</span></span> 

<span data-ttu-id="2e07d-105">Dynamics 365 Project Service Automation utiliza o campo **Tipo** (**msdyn\_ordertype**) das entidades Oportunidade, Oferta, Pedido e Factura para distinguir as versións **baseadas en traballos** destas entidades das versións **baseadas en elementos** e **baseadas en servizos**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="2e07d-106">PSA trata as versións baseadas en traballos destas entidades.</span><span class="sxs-lookup"><span data-stu-id="2e07d-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="2e07d-107">Moitas lóxicas empresariais do lado do cliente e do lado do servidor da solución dependo do campo **Tipo**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="2e07d-108">Por iso, é importante que o campo se inicie cun valor correcto cando se crean as entidades.</span><span class="sxs-lookup"><span data-stu-id="2e07d-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="2e07d-109">Un valor incorrecto pode causar comportamentos incorrectos e é posible que algunhas lóxicas empresariais non funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e07d-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="2e07d-110">Cambio automático de formulario</span><span class="sxs-lookup"><span data-stu-id="2e07d-110">Automatic form switching</span></span>

<span data-ttu-id="2e07d-111">Para evitar a posible corrupción de datos e comportamentos inesperados causados polo inicio e a edición incorrectos dos rexistros da entidade de vendas, PSA agora inclúe a lóxica para o cambio automático de formularios nos formularios listos para usar.</span><span class="sxs-lookup"><span data-stu-id="2e07d-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="2e07d-112">Esta lóxica leva aos usuarios ao formulario correcto para traballar coa versión baseada en traballos ou calquera outro tipo de entidade de Oportunidade, Oferta, Pedido ou Factura.</span><span class="sxs-lookup"><span data-stu-id="2e07d-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="2e07d-113">Cando un usuario abre a versión baseada en traballos dunha entidade Oportunidade, Oferta, Pedido ou Factura, o formulario cámbiase a **Información do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="2e07d-114">A lóxica de cambio automático de formulario depende do da asignación entre o valor **formId** e o campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="2e07d-115">A esa asignación engadíronse todos os formularios listos para usar.</span><span class="sxs-lookup"><span data-stu-id="2e07d-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="2e07d-116">Non obstante, os formularios personalizados deben engadirse manualmente para indicar que versión da entidade están destinados a tratar.</span><span class="sxs-lookup"><span data-stu-id="2e07d-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="2e07d-117">Isto baséase no campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="2e07d-118">Se o cambio de formularios falta na asignación, a lóxica cambiará ao formulario listo para usar, en función do valor que se garda no campo **msdyn\_ordertype** da entidade.</span><span class="sxs-lookup"><span data-stu-id="2e07d-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="2e07d-119">Engada formularios personalizados e active a lóxica de cambio de formularios</span><span class="sxs-lookup"><span data-stu-id="2e07d-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="2e07d-120">O seguinte exemplo mostra como engadir un formulario personalizado, **Información do meu proxecto**, para que funcione con oportunidades baseadas en traballos.</span><span class="sxs-lookup"><span data-stu-id="2e07d-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="2e07d-121">O mesmo proceso úsase para engadir formularios personalizados para que funcionen con ofertas, pedidos e facturas.</span><span class="sxs-lookup"><span data-stu-id="2e07d-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="2e07d-122">Siga estes pasos para crear unha versión personalizada do formulario **Información do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="2e07d-123">Na entidade Oportunidade, abra o formulario **Información do proxecto** e garde unha copia co nome **Información do meu proxecto**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="2e07d-124">Abra o novo formulario e, a seguir, nas propiedades, asegúrese de que estean presentes os scripts de inicio do formulario desde o formulario **Información do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="2e07d-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="2e07d-125">Non elimine os scripts.</span><span class="sxs-lookup"><span data-stu-id="2e07d-125">Don't remove the scripts.</span></span> <span data-ttu-id="2e07d-126">En caso contrario, algúns datos poderían iniciarse incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="2e07d-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="2e07d-127">Asegúrese de que o campo **Tipo** (**msdyn\_ordertype**) estea presente no formulario.</span><span class="sxs-lookup"><span data-stu-id="2e07d-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="2e07d-128">Non elimine este campo.</span><span class="sxs-lookup"><span data-stu-id="2e07d-128">Don't remove this field.</span></span> <span data-ttu-id="2e07d-129">En caso contrario, os scripts de inicio fallarán.</span><span class="sxs-lookup"><span data-stu-id="2e07d-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="2e07d-130">Atope o valor **formId** do novo formulario.</span><span class="sxs-lookup"><span data-stu-id="2e07d-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="2e07d-131">Pode completar este paso de dúas maneiras:</span><span class="sxs-lookup"><span data-stu-id="2e07d-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="2e07d-132">Exporte o formulario **Información do meu proxecto** como parte dunha solución sen xestionar e, a seguir, busque o valor **formId** no ficheiro customization.xml da solución exportada.</span><span class="sxs-lookup"><span data-stu-id="2e07d-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="2e07d-133">Abra o formulario **Información do meu proxecto** no editor de formularios e, a seguir, busque o identificador único global (GUID) xunto ao parámetro **fromId** no URL, como se mostra na seguinte ilustración.</span><span class="sxs-lookup"><span data-stu-id="2e07d-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![O valor formId do novo formulario no URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="2e07d-135">Cree unha asignación **msdyn\_ordertype** para o valor **formId** editando o recurso web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="2e07d-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="2e07d-136">Elimine o código do recurso e substitúao polo seguinte código.</span><span class="sxs-lookup"><span data-stu-id="2e07d-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="2e07d-137">Garde e publique as personalizacións.</span><span class="sxs-lookup"><span data-stu-id="2e07d-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]