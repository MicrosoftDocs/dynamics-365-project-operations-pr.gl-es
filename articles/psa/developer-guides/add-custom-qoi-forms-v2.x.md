---
title: Engadir novos formularios de entidade personalizada (Project Service Automation 2.x)
description: Este artigo ofrece información sobre como engadir formularios de entidades personalizados para oportunidades, cotizacións, pedidos ou facturas en Dynamics 365 Project Service Automation 2.x.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922726"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Engadir novos formularios de entidade personalizada (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Campo Tipo 

Dynamics 365 Project Service Automation utiliza o campo **Tipo** (**msdyn\_ordertype**) das entidades Oportunidade, Oferta, Pedido e Factura para distinguir as versións **baseadas en traballos** destas entidades das versións **baseadas en elementos** e **baseadas en servizos**. PSA trata as versións baseadas en traballos destas entidades. Moitas lóxicas empresariais do lado do cliente e do lado do servidor da solución dependo do campo **Tipo**. Por iso, é importante que o campo se inicie cun valor correcto cando se crean as entidades. Un valor incorrecto pode causar comportamentos incorrectos e é posible que algunhas lóxicas empresariais non funcionen correctamente.

## <a name="automatic-form-switching"></a>Cambio automático de formulario

Para evitar a posible corrupción de datos e comportamentos inesperados causados polo inicio e a edición incorrectos dos rexistros da entidade de vendas, PSA agora inclúe a lóxica para o cambio automático de formularios nos formularios listos para usar. Esta lóxica leva aos usuarios ao formulario correcto para traballar coa versión baseada en traballos ou calquera outro tipo de entidade de Oportunidade, Oferta, Pedido ou Factura. Cando un usuario abre a versión baseada en traballos dunha entidade Oportunidade, Oferta, Pedido ou Factura, o formulario cámbiase a **Información do proxecto**.

A lóxica de cambio automático de formulario depende do da asignación entre o valor **formId** e o campo **msdyn\_ordertype**. A esa asignación engadíronse todos os formularios listos para usar. Non obstante, os formularios personalizados deben engadirse manualmente para indicar que versión da entidade están destinados a tratar. Isto baséase no campo **msdyn\_ordertype**. Se o cambio de formularios falta na asignación, a lóxica cambiará ao formulario listo para usar, en función do valor que se garda no campo **msdyn\_ordertype** da entidade.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Engada formularios personalizados e active a lóxica de cambio de formularios

O seguinte exemplo mostra como engadir un formulario personalizado, **Información do meu proxecto**, para que funcione con oportunidades baseadas en traballos. O mesmo proceso úsase para engadir formularios personalizados para que funcionen con ofertas, pedidos e facturas.

Siga estes pasos para crear unha versión personalizada do formulario **Información do proxecto**.

1. Na entidade Oportunidade, abra o formulario **Información do proxecto** e garde unha copia co nome **Información do meu proxecto**.
2. Abra o novo formulario e, a seguir, nas propiedades, asegúrese de que estean presentes os scripts de inicio do formulario desde o formulario **Información do proxecto**. 

    > [!IMPORTANT]
    > Non elimine os scripts. En caso contrario, algúns datos poderían iniciarse incorrectamente.

3. Asegúrese de que o campo **Tipo** (**msdyn\_ordertype**) estea presente no formulario. 

    > [!IMPORTANT]
    > Non elimine este campo. En caso contrario, os scripts de inicio fallarán.

4. Atope o valor **formId** do novo formulario. Pode completar este paso de dúas maneiras:

    - Exporte o formulario **Información do meu proxecto** como parte dunha solución sen xestionar e, a seguir, busque o valor **formId** no ficheiro customization.xml da solución exportada.
    - Abra o formulario **Información do meu proxecto** no editor de formularios e, a seguir, busque o identificador único global (GUID) xunto ao parámetro **fromId** no URL, como se mostra na seguinte ilustración.

    ![O valor formId do novo formulario no URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Cree unha asignación **msdyn\_ordertype** para o valor **formId** editando o recurso web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Elimine o código do recurso e substitúao polo seguinte código.

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

6. Garde e publique as personalizacións.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
