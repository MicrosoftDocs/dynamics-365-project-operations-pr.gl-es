---
title: Actualizar os atributos do complemento para incluír novas dimensións de prezos
description: Este artigo ofrece información sobre a actualización dos atributos do complemento para as dimensións de prezos.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913204"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Actualizar os atributos do complemento para incluír novas dimensións de prezos

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Se non estás a usar as funcións de cotización e contratación de Project Service Automation (PSA), podes omitir este artigo.

Este artigo asume que completou os procedementos dos artigos, [Crear campos e entidades personalizados](create-custom-fields-entities.md),[Engade campos personalizados á configuración de prezos e ás entidades transaccionais](field-references.md), e [Configura campos personalizados como dimensións de prezos](set-up-pricing-dimensions.md). Se non completaches eses procedementos, volve e complétaos e despois volve a este artigo.

Cando se crea un detalle de liña de oferta na páxina **Liña de oferta** para unha liña de oferta do proxecto, o sistema crea dúas liñas de estimación en segundo plano: unha liña para o lado de custo da estimación e outra para o lado de vendas. Isto é o mesmo para as liñas de contrato do proxecto.

Cando faga unha modificación da cantidade ou dun campo do lado do custo, este cambio propagarase ao lado das vendas. Isto é posible debido aos seguintes complementos que deben volver rexistrarse despois dun cambio nas dimensións de prezos.

- PreOperationContractLineDetailUpdate - Actualizacións **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Actualizacións **msdyn_quotelinetransaction**.

Os pasos seguintes explican o proceso de rexistro dos complementos.

1. Abra **PluginRegistrationTool** e conéctese á súa instancia en liña.
2. Prema **Buscar** e busque o complemento para actualizar.

 ![Captura de pantalla da árbore de busca.](media/PRT-1.png)

3. Despois de atopar o complemento, seleccióneo e logo prema **Seleccionar en formulario principal**.

4. Seleccione o paso do complemento para actualizar, prema co botón dereito e logo seleccione **Actualizar**.

 ![Captura de pantalla do complemento para actualizar.](media/PRT-2.png)
 
5. Na ventá de actualización, prema nos puntos suspensivos (**...**) nos atributos de filtrado.

 ![Captura de pantalla de información de configuración do paso existente Actualizar.](media/PRT-3.png)
 
6. Seleccione as caixas de verificación do atributo de prezos

 ![Captura de pantalla que mostra a selección da caixa de verificación para os atributos de prezos.](media/PRT-4.png)

7. Prema **Aceptar** para pechar a páxina e logo seleccione **Actualizar paso**.

 ![Captura de pantalla que mostra o botón "Actualizar paso".](media/PRT-5.png)
 
8. Repita este proceso para o segundo complemento, **PreOperationQuoteLineDetail - Actualización de msdyn_quotelinetransaction**.

9. Peche a ferramenta de rexistro de complementos.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
